# sprint7-final-project ConnectaTel - Análisis y Segmentación de Clientes

## Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de uso de los clientes de ConnectaTel mediante técnicas de limpieza, exploración y transformación de datos, con el fin de identificar patrones de consumo, segmentar usuarios y generar recomendaciones para el negocio.

## Datasets Utilizados

El proyecto utiliza los siguientes conjuntos de datos:

### users
Contiene información de los clientes:
- user_id
- first_name
- last_name
- age
- city
- reg_date
- plan
- churn_date

### usage
Contiene el historial de uso de los clientes:
- id
- user_id
- type (call o text)
- date
- duration
- length

### plans
Contiene la información de los planes disponibles:
- Básico
- Premium

## Etapas del Análisis

### 1. Exploración Inicial
- Revisión de estructura de datos.
- Identificación de tipos de variables.
- Detección de valores nulos.

### 2. Limpieza de Datos
- Tratamiento de valores faltantes.
- Corrección de sentinels:
  - age = -999
  - city = "?"
- Identificación y corrección de fechas fuera de rango.
- Validación de consistencia de datos.

### 3. Análisis Exploratorio
- Distribución de edades.
- Distribución de mensajes enviados.
- Distribución de llamadas realizadas.
- Distribución de minutos consumidos.
- Comparación entre planes Básico y Premium.

### 4. Detección de Outliers
- Uso del método IQR.
- Evaluación de valores atípicos.
- Decisión de conservar los outliers al representar usuarios reales de alto consumo.

### 5. Ingeniería de Variables
- Cálculo de:
  - cantidad de mensajes
  - cantidad de llamadas
  - minutos totales de llamada
- Agregación de métricas por usuario.

### 6. Segmentación de Clientes
Clasificación de usuarios según su nivel de uso:

- Bajo uso
- Uso medio
- Alto uso

Además, se generaron grupos de edad para facilitar el análisis de segmentos.

### 7. Insights y Recomendaciones
- Identificación de segmentos de alto valor.
- Oportunidades de fidelización.
- Recomendaciones para diseño de planes y campañas comerciales.

## Cómo Ejecutar el Proyecto

### Google Colab

1. Descargar el archivo `.ipynb`.
2. Abrir Google Colab.
3. Seleccionar:
   - Archivo → Subir notebook.
4. Cargar los datasets requeridos.
5. Ejecutar las celdas en orden.

## Guía de Reproducción

Para reproducir los resultados:

1. Cargar los datasets originales.
2. Ejecutar las etapas de limpieza.
3. Ejecutar el análisis exploratorio.
4. Generar las variables agregadas por usuario.
5. Aplicar la segmentación de clientes.
6. Ejecutar las visualizaciones y análisis finales.
7. Revisar las conclusiones y recomendaciones obtenidas.

## Principales Hallazgos

- Se detectaron y corrigieron valores inválidos y sentinels.
- Los usuarios de alto consumo representan el segmento de mayor valor para el negocio.
- No se observaron diferencias significativas de edad entre los planes Básico y Premium.
- Los outliers identificados corresponden a usuarios reales de alto uso y fueron conservados.
- La segmentación permite diseñar estrategias de fidelización y personalización de planes.

## Tecnologías Utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook
