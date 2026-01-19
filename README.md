# Proyecto_Informe_de_Felicidad_Mundial
El objetivo del proyecto es analizar los datos del World Happiness Report para el periodo comprendido entre 2015 y 2019. El análisis busca identificar patrones, tendencias y correlaciones entre el "Happiness Score"  y diversas variables socioeconómicas y de calidad de vida, con el fin de comprender mejor los factores que contribuyen al bienestar.

# Análisis del World Happiness Report (2015-2019)

## Descripción del Proyecto
Este proyecto tiene como objetivo analizar los datos del World Happiness Report para el período comprendido entre 2015 y 2019. A través de la carga, limpieza, preprocesamiento y análisis de datos, se buscan identificar patrones, tendencias y correlaciones entre el "Happiness Score" (Índice de Felicidad) y diversas variables socioeconómicas y de calidad de vida. El fin es comprender mejor los factores que contribuyen al bienestar global y la evolución de la felicidad a lo largo de estos años.

## Fuentes de Datos
Los datos utilizados provienen de los informes anuales del World Happiness Report, disponibles como archivos CSV separados para cada año (2015, 2016, 2017, 2018, 2019).

## Metodología
El análisis se realizó siguiendo los siguientes pasos:

1.  **Carga y Unificación de Datos**: Se cargaron los cinco archivos CSV (uno por año) en DataFrames de Pandas. Se añadió una columna 'Year' a cada DataFrame para identificar el año correspondiente y luego se concatenaron en un único DataFrame (`df_all_years`).
2.  **Estandarización de Columnas**: Se renombraron las columnas de los DataFrames individuales para asegurar la uniformidad en sus nombres antes de la concatenación, facilitando el análisis consistente entre años.
3.  **Limpieza y Preprocesamiento de Datos**: Se realizó una inspección exhaustiva de los valores nulos. Columnas con alta predominancia de nulos y menos relevantes para el análisis principal (como 'Region', 'Standard Error', 'Lower/Upper Confidence Interval', etc.) fueron eliminadas. Posteriormente, se eliminaron filas con nulos restantes en columnas clave para mantener la integridad de los datos.
4.  **Análisis Exploratorio de Datos (EDA)**: Se realizaron visualizaciones y cálculos estadísticos para entender la distribución de las variables y las relaciones entre ellas. Esto incluyó:
    *   Evolución del Índice de Felicidad Promedio y la Esperanza de Vida Saludable Promedio por año.
    *   Cálculo y visualización de la matriz de correlación entre las variables principales.
    *   Análisis de la relación entre 'GDP per Capita' y 'Happiness Score', y entre 'Social Support' y 'GDP per Capita' mediante gráficos de dispersión.
    *   Identificación de los 5 países más y menos felices en 2019.
    *   Histograma de la distribución del 'Happiness Score'.

## Hallazgos Clave

*   **Tendencia Temporal**: Tanto el Índice de Felicidad promedio como la Esperanza de Vida Saludable promedio mostraron una caída notable en 2017, seguida de una recuperación constante y un pico en 2019. Esto sugiere que hubo factores globales significativos en 2017 que afectaron el bienestar.
*   **Correlaciones Fuertes con la Felicidad**: El `Happiness Score` está muy fuertemente correlacionado con el `GDP per Capita` (0.79), `Healthy Life Expectancy` (0.78) y `Social Support` (0.75). La `Freedom to Make Life Choices` también muestra una correlación positiva (0.57).
*   **Factores Menos Influyentes**: La `Generosidad` (0.16) tuvo una correlación débil, y la `Percepción de Corrupción` (-0.38) una correlación negativa moderada, indicando que una menor corrupción se asocia a mayor felicidad.
*   **PIB per Cápita y Felicidad**: Existe una relación directa y fuerte entre el desarrollo económico (medido por `GDP per Capita`) y el `Happiness Score`. Países nórdicos se destacan con altos valores en ambos, mientras que países menos desarrollados muestran lo contrario.
*   **Apoyo Social y Economía**: La correlación entre `Social Support` y `GDP per Capita` es positiva pero moderada (0.59), lo que implica que, aunque los países más ricos suelen tener mejor apoyo social, otros factores también influyen en esta relación.
*   **Países Extremos (2019)**: Finlandia, Dinamarca, Noruega, Islandia y Países Bajos fueron los más felices, mientras que Afganistán, República Centroafricana, Sudán del Sur, Tanzania y Ruanda fueron los menos felices.
*   **Distribución de la Felicidad**: La mayoría de los países se encuentran en un rango medio de felicidad (entre 4 y 7), con pocos en los extremos de muy baja o muy alta felicidad.

## Tecnologías Utilizadas
*   Python 3.x
*   Pandas (para manipulación y análisis de datos)
*   Matplotlib (para visualización de datos)
*   Seaborn (para visualización de datos)



```

