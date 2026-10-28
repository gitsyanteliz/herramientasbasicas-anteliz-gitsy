# Análisis de popularidad de canciones en Spotify

**Autora:** Gitsy Anteliz
**Curso:** Herramientas básicas para el Análisis de Datos (UTN.BA)
**Cohorte:** Septiembre – Noviembre 2026

## Objetivo
Descubrir qué características se relacionan con la popularidad de las canciones en Spotify, respondiendo tres preguntas:
1. ¿Qué géneros tienen mayor popularidad?
2. ¿Las canciones más bailables son más populares?
3. ¿Las canciones con letra explícita son más o menos populares?

**Hipótesis:** las canciones con letra explícita son más populares.

## Dataset
Spotify Tracks Dataset (Kaggle, autor maharshipandya): 114.000 canciones con su género, popularidad (0 a 100) y características de audio. Se tomó una muestra aleatoria de 10.000 canciones (random_state=42, para que el resultado sea reproducible).

## Pasos realizados
1. **Limpieza (Python):** revisé tipos, vacíos y duplicados. Quité la columna `Unnamed: 0` (solo era un número de fila) y 1 canción que dura 0 segundos y no tiene artista, álbum ni nombre (valor imposible, 0,01 % de la muestra). Las 1.430 canciones con popularidad 0 (14,3 %) no las borré: las marqué como "Dudoso" y comparé los resultados con y sin ellas.
2. **Análisis y gráficos:** promedios por grupo, correlación, gráfico de barras, dispersión y boxplot.
3. **Dashboard (Power BI):** 3 KPIs, 2 gráficos y un filtro por género.

## Hallazgos principales
- **Géneros:** pop-film es el más popular (promedio 59,6), seguido de k-pop (57,1) y chill (52,4). Cada promedio se basa en entre 73 y 105 canciones.
- **Bailabilidad:** la correlación con la popularidad es casi nula (0,05), así que ser más bailable prácticamente no se relaciona con ser más popular.
- **Letra explícita:** las explícitas son un poco más populares (35,9 vs. 32,6). La hipótesis se apoya, pero débilmente.

**Limitaciones:** la popularidad mide cuánto se escucha una canción en el momento de la recolección; en el dataset, "False" en explícitas incluye canciones de las que no se sabe. Los resultados muestran asociaciones, no causas.

## Herramientas
Python (pandas, matplotlib, seaborn) en Google Colab · Power BI Desktop · GitHub

## Archivos
- [Notebook del análisis](notebooks/TP_Final_Spotify.ipynb)
- [Dashboard en PDF](dashboard/TP_Final_Spotify_dashboard.pdf) · [Archivo de Power BI](dashboard/TP_Final_Spotify_dashboard.pbix)
- [Datos: fuente y licencia](data/raw/README.md)

## Fuente y licencia de los datos
[Spotify Tracks Dataset – Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset). Licencia: Open Database (ODbL); contenidos © de sus autores. Proyecto académico de Gitsy Anteliz, 2026.
