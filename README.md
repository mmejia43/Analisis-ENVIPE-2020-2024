# Analisis-ENVIPE-2020-2024

Análisis histórico de indicadores de la ENVIPE 2020-2024 para Querétaro, comparados con los resultados de México y la Ciudad de México. El proyecto incluye procesamiento de datos, estimaciones estadísticas y visualizaciones desarrolladas en R.

## Instrucciones de ejecución

### 1. Descargar las bases de datos

Descargar las bases de datos de la Encuesta Nacional de Victimización y Percepción sobre Seguridad Pública (ENVIPE) correspondientes a los años 2021, 2022, 2023, 2024 y 2025 desde el portal oficial del INEGI:

https://www.inegi.org.mx/programas/envipe/X/#microdatos

- Sustituya la letra "X" por el año de la edición que desea descargar (2021, 2022, 2023, 2024 o 2025).

Al descargar cada edición, asegúrese de obtener las bases de datos en formato CSV.

### 2. Extraer los archivos descargados

Una vez descargados los archivos correspondientes a cada año, extraiga el contenido de las carpetas comprimidas.

Dentro de cada carpeta encontrará los siguientes archivos:

- THogar
- TMod_Vic
- TPer_Vic1
- TPer_Vic2
- TSDem
- TVivienda

Todos estos archivos se encuentran en formato CSV y serán utilizados para la ejecución del análisis.

### 3. Renombrar los archivos

Para evitar conflictos entre bases de datos de diferentes años, es necesario agregar al final del nombre de cada archivo un guión bajo seguido los dos últimos dígitos del año correspondiente.

Ejemplo para renombrar los archivos de la base de datos de la ENVIPE 2021:

- THogar → THogar_21
- TMod_Vic → TMod_Vic_21
- TPer_Vic1 → TPer_Vic1_21
- TPer_Vic2 → TPer_Vic2_21
- TSDem → TSDem_21
- TVivienda → TVivienda_21

Repita el mismo procedimiento para los años 2022, 2023, 2024 y 2025 utilizando los sufijos correspondientes (_22, _23, _24 y _25).

Al finalizar este paso, deberá contar con archivos como:

- THogar_21, THogar_22, THogar_23, THogar_24 y THogar_25
- TMod_Vic_21, TMod_Vic_22, TMod_Vic_23, TMod_Vic_24 y TMod_Vic_25
- TPer_Vic1_21, TPer_Vic1_22, TPer_Vic1_23, TPer_Vic1_24 y TPer_Vic1_25
- TPer_Vic2_21, TPer_Vic2_22, TPer_Vic2_23, TPer_Vic2_24 y TPer_Vic2_25
- TSDem_21, TSDem_22, TSDem_23, TSDem_24 y TSDem_25
- TVivienda_21, TVivienda_22, TVivienda_23, TVivienda_24 y TVivienda_25

### 4. Organizar los archivos

Una vez renombradas todas las bases de datos, coloque los archivos en la misma carpeta donde se encuentran:

- Analisis_ENVIPE_2020-2024.Rmd
- Los demás archivos incluidos en este repositorio

No es necesario modificar rutas dentro del archivo R Markdown. Únicamente asegúrese de que todas las bases de datos, el archivo .Rmd y los demás archivos del repositorio se encuentren en la misma carpeta de trabajo.

### 5. Ejecutar el proyecto

Una vez que las bases de datos estén correctamente descargadas, renombradas y organizadas:

- Abra el archivo Analisis_ENVIPE_2020-2024.Rmd en RStudio.
- Verifique que el archivo se encuentre en la misma ubicación que las bases de datos y los demás archivos del repositorio.
- Ejecute el documento o genere el archivo PDF mediante la opción Knit de RStudio.

### Solución de problemas

Si el documento no se ejecuta correctamente, compruebe que todas las librerías requeridas se encuentren instaladas en R.

En particular, asegúrese de contar con los paquetes tinytex y rmarkdown. En caso de no tenerlos instalados, ejecute los siguientes comandos en la consola de R:

```r
install.packages("tinytex")
install.packages("rmarkdown")
```

### Soporte:
Si después de seguir las instrucciones anteriores continúa presentando problemas durante la ejecución del proyecto, puede comunicarse conmigo para recibir orientación y apoyo.

## Consideraciones

Durante el desarrollo de este proyecto se utilizaron herramientas de inteligencia artificial como apoyo para tareas de programación y depuración de código. Sin embargo, la selección de variables, el planteamiento metodológico, el análisis de resultados y las conclusiones presentadas son responsabilidad de los autores del proyecto.

El uso de estas herramientas tuvo como finalidad facilitar el desarrollo técnico del trabajo y no sustituir el criterio analítico ni la interpretación de los resultados.
