# 🎓 Predicción del Rendimiento Estudiantil mediante Regresión Lineal

## 🎯 Objetivo del Proyecto

Este proyecto final del Diplomado **Bedu-Santander** tiene como objetivo principal construir un modelo de **Regresión Lineal Múltiple** robusto en $\\mathbf{R}$ (ejecutado en un *Jupyter Notebook*) para predecir el **Índice de Rendimiento** de los estudiantes basándose en sus hábitos y antecedentes.

El modelo alcanzó un coeficiente de determinación ($\\mathbf{R^2}$) de **$0.98$**, demostrando una capacidad predictiva excepcionalmente alta y la relevancia de las variables seleccionadas.

-----

## 📊 Metodología y Resultados Clave

### 1\. Conjunto de Datos

  * **Origen:** Dataset de rendimiento estudiantil de **Kaggle**.
  * **Tamaño:** 10,000 observaciones.
  * **Variables Utilizadas:**

| Variable (Predictora) | Tipo | Descripción |
| :--- | :--- | :--- |
| **`Hours.Studied`** | *integer* | Horas semanales dedicadas al estudio. |
| **`Previous.Scores`** | *integer* | Puntuación obtenida en exámenes o cursos previos. |
| **`Extracurricular.Activities`** | *character* | Indicador de participación en actividades extracurriculares. |
| **`Sleep.Hours`** | *integer* | Horas de sueño promedio. |
| **`Sample.Question.Papers.Practiced`** | *integer* | Cantidad de exámenes de muestra o guías practicadas. |
| **Variable Objetivo:** **`Performance.Index`** (*numeric*) | Índice de rendimiento final del estudiante (la variable a predecir). |

### 2\. Análisis y Modelado

  * **Técnica:** Regresión Lineal Múltiple.
  * **Entorno:** Análisis realizado con $\\mathbf{R}$ dentro de un *Jupyter Notebook* (`.ipynb`).
  * **Preprocesamiento Clave:** La variable categórica `Extracurricular.Activities` fue transformada a formato numérico (variable *dummy*) para su inclusión en el modelo.
  * **Resultado Principal:**
      * **$R^2$ (Coeficiente de Determinación):** $\\mathbf{0.98}$
      * **Interpretación:** El **98%** de la variabilidad en el `Performance.Index` puede ser explicado por las variables predictoras incluidas en el modelo.
      * **Conclusión:** Las horas dormidas la noche anterior casi no tienen efectos en el desempeño pero sí los resultados previos.

-----

## 🛠️ Estructura del Repositorio

```
.
├── Student_Performance.csv       # El dataset original de Kaggle.
├── Student_Regression.ipynb      # El Jupyter Notebook con todo el código R, análisis y resultados.
└── README.md
```

## ⚙️ Cómo Replicar el Análisis

El análisis está contenido en el *Jupyter Notebook* y utiliza $\\mathbf{R}$.

### 1\. Instalación y Carga de Librerías

Se recomienda usar la librería `pacman` para instalar y cargar fácilmente las dependencias.

```r
# Instalar pacman si es la primera vez que se usa
if (!requireNamespace("pacman", quietly = TRUE)) {
    install.packages("pacman")
}

# Cargar/Instalar las librerías necesarias para el proyecto
pacman::p_load(
    glmnet,    # Para modelos de regresión avanzados o exploratorios (Ridge/Lasso)
    graphics,  # Librería base de R para gráficos
    caret,     # Herramientas de entrenamiento y evaluación de modelos
    ggplot2    # Visualización de datos de alta calidad
)
```

### 2\. Ejecutar el Notebook

Abre el archivo **`Student_Regression.ipynb`** directamente en **Google Colaboratory** o descárgalo para usarlo en tu entorno local de **Jupyter** para ver el código $\\mathbf{R}$ paso a paso y ejecutar el modelo.

-----

## 🤝 Autor y Contacto

  * **Autor:** Pablo Natera Bravo
  * **Diplomado:** Bedu-Santander - Conéctate a la Era Digital Data Scientist
  * **LinkedIn:** [[Pablo Natera](https://www.linkedin.com/in/pablo-natera-464531299)]
