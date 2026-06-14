## 🎯 Objetivo del Proyecto
Este proyecto tiene como objetivo analizar el comportamiento histórico de los usuarios de la empresa de telecomunicaciones **ConnectaTel**. A través de técnicas de limpieza de datos, análisis exploratorio (EDA) y segmentación, se busca entender los patrones de consumo (llamadas, mensajes y minutos) para identificar los perfiles de clientes más valiosos, detectar anomalías (heavy users) y generar recomendaciones estratégicas orientadas a la optimización de los planes tarifarios (Básico y Premium).

## 📂 Datasets Utilizados
El análisis se fundamenta en dos conjuntos de datos principales:
* **`users`**: Contiene la información demográfica de los clientes y el plan tarifario al que están suscritos (edad, tipo de plan, fecha de alta, etc.).
* **`usage`**: Registro transaccional detallado del consumo de los usuarios, categorizado por tipo de evento (llamadas, mensajes de texto, datos de internet), junto con sus respectivas duraciones o volúmenes de consumo.

## 🛠️ Etapas del Análisis
El proyecto se desarrolló siguiendo un flujo de trabajo estructurado para ciencia de datos utilizando **Python (Pandas, Matplotlib, Seaborn)**:

1. **Limpieza y Preparación de Datos:** * Corrección de tipos de datos y estandarización de fechas.
   * Tratamiento de valores nulos mediante análisis de causalidad (Missing At Random - MAR) vinculados a la naturaleza del servicio.
2. **Feature Engineering (Ingeniería de Características):** * Construcción de un perfil unificado por usuario consolidando las métricas totales de uso mediante operaciones vectorizadas y agrupaciones (`groupby`).
3. **Análisis Exploratorio de Datos (EDA):** * Generación de estadísticas descriptivas para entender la distribución porcentual de los planes y el comportamiento general.
4. **Visualización y Detección de Outliers:** * Creación de histogramas para visualizar distribuciones (con asimetría positiva en el uso) y diagramas de caja (Boxplots) aplicando el **método IQR** para la identificación de *Heavy Users*.
5. **Segmentación de Clientes:** * Clasificación lógica de usuarios en clústeres de consumo (`Bajo uso`, `Uso medio`, `Alto uso`) y rangos demográficos (`Joven`, `Adulto`, `Adulto Mayor`).
6. **Insights Estratégicos:** * Traducción de los hallazgos estadísticos en recomendaciones ejecutivas de negocio para estrategias de *upselling* y diseño de productos.

## 🚀 Cómo Ejecutar el Notebook

La forma más rápida y sencilla de explorar este análisis es a través de **Google Colab**, ya que no requiere configuración de entorno local.

**Opción A: Abrir en Google Colab**
1. Descarga el archivo `.ipynb` de este repositorio.
2. Ve a [Google Colab](https://colab.research.google.com/).
3. Selecciona la pestaña **"Subir"** (Upload) y arrastra el archivo `.ipynb`.
4. Asegúrate de cargar también los archivos `.csv` de los datasets en el panel de archivos lateral izquierdo de Colab antes de ejecutar las celdas.

**Opción B: Ejecución Local (Jupyter Notebook / VS Code)**
1. Clona este repositorio: `git clone [URL_DEL_REPOSITORIO]`
2. Navega a la carpeta del proyecto.
3. Asegúrate de tener instaladas las dependencias necesarias:
   ```bash
   pip install pandas numpy matplotlib seaborn
