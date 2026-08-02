# telecom-analysis
# Análisis de Comportamiento de Clientes - ConnectaTel 📱📊

## 🎯 Objetivo del Proyecto
El objetivo de este proyecto es evaluar el comportamiento de los clientes de la empresa de telecomunicaciones **ConnectaTel** en Latinoamérica (con datos hasta 2024). A través de la exploración, limpieza y análisis de datos, se construyó un perfil estadístico de los usuarios, se detectaron comportamientos atípicos (outliers) y se crearon segmentos de clientes. Esto con el fin de identificar patrones de consumo y proponer recomendaciones comerciales estratégicas.

## 📂 Datasets Utilizados
El análisis se basa en tres conjuntos de datos principales:
*   **`plans.csv`**: Información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
*   **`users_latam.csv`**: Información demográfica y de cuenta de los clientes (edad, ciudad, fecha de registro, plan, churn).
*   **`usage.csv`**: Detalle del uso real de los servicios por usuario (llamadas, duración y mensajes).

## 🛠️ Etapas del Análisis Realizadas
1.  **Carga y Exploración Inicial:** Importación de librerías (`pandas`, `seaborn`, `matplotlib`, `numpy`) y revisión de la estructura de los DataFrames.
2.  **Identificación de Problemas de Calidad:** Detección de valores nulos (Missing At Random) y valores inválidos (sentinels como `-999` y `?`).
3.  **Limpieza de Datos:** Imputación de nulos usando la mediana, estandarización de sentinels a `pd.NA` y corrección de fechas futuras imposibles (ej. año 2026).
4.  **Estadísticas de Resumen (Summary Statistics):** Agrupación de datos de consumo por usuario (`groupby`) y cálculo de métricas clave (total de llamadas, mensajes y minutos).
5.  **Visualización y Detección de Outliers:** Creación de histogramas y boxplots usando `seaborn` para entender la distribución de los datos y detectar "Heavy Users" mediante el método del Rango Intercuartílico (IQR).
6.  **Segmentación de Clientes:** Clasificación de usuarios mediante reglas lógicas (`np.where` y funciones `apply`) en grupos por **Nivel de Uso** (Bajo, Medio, Alto) y **Edad** (Joven, Adulto, Adulto Mayor).
7.  **Insights Ejecutivos:** Traducción de los hallazgos técnicos en recomendaciones de negocio accionables para los stakeholders.

## 🚀 Cómo ejecutar el notebook
La forma más sencilla de revisar y ejecutar este código es utilizando **Google Colab**:
1. Descarga el archivo `.ipynb` de este repositorio.
2. Abre [Google Colab](https://colab.research.google.com/).
3. Ve a `Archivo` > `Subir notebook` y selecciona el archivo descargado.
4. Asegúrate de cargar la carpeta `/datasets/` con los archivos CSV en el entorno de Colab (en el panel izquierdo de "Archivos"), o ajusta las rutas de lectura en el código según tu entorno local.

## ⚙️ Guía de Reproducción (Entorno Local)
Si prefieres ejecutarlo en tu máquina local:
1. Clona este repositorio:
   ```bash
   git clone https://github.com/TU_USUARIO/TU_REPOSITORIO.git
Asegúrate de tener instalado Python 3.x y Jupyter Notebook.
Instala las dependencias necesarias ejecutando:
code
Bash
pip install pandas numpy matplotlib seaborn
Abre la terminal en la carpeta del proyecto y ejecuta:
code
Bash
jupyter notebook
Abre el archivo del proyecto y ejecuta las celdas secuencialmente (Shift + Enter).
code
Code
### Fin de la copia

***

### 💡 Últimos pasos:
1. Crea un archivo llamado `README.md` en tu repositorio de GitHub.
2. Pega el texto de arriba.
3. **¡OJO!** Asegúrate de cambiar donde dice `TU_USUARIO/TU_REPOSITORIO.git` por el link real de tu GitHub.

¡Y listo! Tienes un proyecto de análisis de datos de principio a fin, con código limpio, conclusiones de negocio y una documentación impecable. ¡Mucho éxito!
