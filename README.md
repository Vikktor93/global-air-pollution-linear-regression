# Proyecto N°2: Análisis de la Contaminación del Aire con un Modelo de Regresión Lineal Simple

<p align="left">
   <img src="https://img.shields.io/badge/Status-En%20Desarrollo-green?style=plastic">
   <img src="https://img.shields.io/badge/Python-3776AB?style=plastic&logo=python&logoColor=white"/>
   <img src="https://img.shields.io/badge/Jupyter-%23e58f1a.svg?style=plastic&logo=Jupyter&logoColor=white"/>

<img src="./assets/banner.png"/>

Este proyecto tiene como objetivo aplicar un flujo completo de análisis de datos sobre el dataset [Global Air Pollution](https://www.kaggle.com/datasets/hasibalmuzdadid/global-air-pollution-dataset) de Kaggle, utilizando técnicas de **Análisis Exploratorio de Datos (EDA)**, **Limpieza de Datos**, y un modelo de **Regresión Lineal Simple**.

## Descripción del Dataset

Este dataset incluye los valores de los principales contaminantes del aire:
- **CO AQI Value**: Índice de calidad del aire para monóxido de carbono.
- **Ozone AQI Value**: Índice de calidad del aire para ozono.
- **NO2 AQI Value**: Índice de calidad del aire para dióxido de nitrógeno.
- **PM2.5 AQI Value**: Índice de calidad del aire para partículas finas (PM2.5).
- **AQI Value**: Índice de calidad del aire general.
- **AQI Category**: Categoría que indica el nivel de contaminación del aire (Good, Moderate, Unhealthy, etc.).

El objetivo del análisis es identificar los contaminantes más importantes en diferentes ciudades, y preparar los datos para análisis futuros mediante procesos de limpieza, transformación, y visualización.

## Estructura del Proyecto

La estructura del proyecto es la siguiente:
```
global-air-pollution-analysis/
├── assets/                       # Carpeta que contiene imágenes o activos para el README
│   └── banner.png                # Imagen del banner utilizado en el README.md
├── data/                         # Carpeta que contiene los datasets originales y limpios
│   ├── global_air_pollution.csv  # Dataset original
│   └── dataset_clean.csv         # Dataset limpio generado tras la limpieza de datos
├── notebooks/                    # Notebooks de Jupyter con el análisis y transformación de datos
│   ├── 001_Analisis_Exploratorio.ipynb     # Análisis exploratorio de los datos
│   ├── 002_Limpieza_de_Datos.ipynb         # Limpieza de datos
│   └── 003_Regresión_Lineal.ipynb          # Modelo de Regresión Lineal y Conclusiones
├── README.md                     # Archivo de documentación del proyecto
```

### 1. **Análisis Exploratorio (`001_Analisis_Exploratorio.ipynb`)**
En este notebook, se realiza una exploración inicial del dataset:
- Carga y revisión del contenido del dataset.
- Exploración de las distribuciones de las variables numéricas mediante histogramas.
- Identificación de posibles relaciones entre variables numéricas con un mapa de calor de correlación.

### 2. **Limpieza de Datos (`002_Limpieza_de_Datos.ipynb`)**
Este notebook se enfoca en limpiar el dataset para prepararlo para un análisis en la etapa de Transformación de Daots:
- Eliminación de valores nulos.
- Relleno de datos faltantes en columnas clave (por ejemplo, se completa la columna "Country" con el valor más frecuente).
- Eliminación de duplicados.
- Verificación de los tipos de datos y corrección de formatos, si es necesario.

### 3. **Modelo de Regresión Lineal (`003_Regresion_Lineal.ipynb`)**
En este notebook se aplica un modelo de **Regresión Lineal Simple** para analizar la relación entre las concentraciones de **Ozone AQI Value** y **PM2.5 AQI Value**.
   - **Objetivos**:
     - Seleccionar variables para el modelo de regresión.
     - Ajustar un modelo de regresión lineal simple.
     - Calcular los coeficientes del modelo (pendiente e intersección).
     - Evaluar el modelo utilizando métricas estadísticas como el **Error Cuadrático Medio (MSE)** y el **Coeficiente de Determinación (R²)**.
   - **Contenido**:
     - Visualización de la relación entre **Ozone AQI** y **PM2.5 AQI**.
     - Ajuste de la recta de regresión y cálculo de los coeficientes.
     - Interpretación del coeficiente de correlación de Pearson (**r**), que mide la relación entre las dos variables.
     - Evaluación del modelo mediante el cálculo del MSE y R².

## Requisitos Previos

Para ejecutar los notebooks y replicar el análisis, necesitas instalar las siguientes dependencias:

`pip install numpy pandas matplotlib seaborn scikit-learn`

## Cómo Usar Este Repositorio
1. Clona este repositorio en tu dispositivo local:
`git clone https://github.com/Vikktor93/global-air-pollution-linear-regression.git`
2. Abre los notebooks en Jupyter Notebook, JupyterLab o tu IDE favorito.
3. Sigue los notebooks en el orden sugerido para entender todo el flujo del análisis.

## Licencia
