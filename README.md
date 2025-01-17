# GITHUB-DEV-NETWORK-ANALYSIS

## Descripción

Este proyecto presenta una red social de desarrolladores basada en datos recopilados de la API pública de GitHub en junio de 2019. Los nodos representan desarrolladores que han destacado al menos 10 repositorios, y las conexiones entre ellos son relaciones de seguidores mutuos. Se incluyen atributos de los nodos basados en información como ubicación, repositorios destacados, empleador y dirección de correo electrónico. La tarea principal es la clasificación binaria de nodos para predecir si un desarrollador se especializa en desarrollo web o aprendizaje automático.

### Propiedades de la red
- **Dirigida**: No.
- **Atributos de nodos**: Sí.
- **Atributos de aristas**: No.
- **Etiquetas de nodos**: Sí, binarias.
- **Temporal**: No.
- **Nodos**: 37,700.
- **Aristas**: 289,003.
- **Densidad**: 0.001.
- **Transitividad**: 0.013.

### Tareas posibles
- Clasificación binaria de nodos.
- Predicción de enlaces.
- Detección de comunidades.
- Visualización de redes.

## Estructura del Proyecto

### Directorios Principales
- **datos/**: Contiene los datos originales y procesados.
- **metricas/**: Contiene los resultados de las métricas calculadas.
- **tablas/**: Almacena tablas fusionadas y transformadas.
- **Proyecto/**: Contiene notebooks de análisis y procesamiento.

### Archivos Destacados

#### **Calculo_metricas.ipynb**
Este notebook calcula varias métricas de red, como:
- Centralidad (grado, cercanía, intermediación).
- Coeficiente de agrupamiento y triángulos.
- Comunidades (modularidad, partición por intermediación de aristas).
- Núcleos (núcleos centrales).

#### **Creacion_de_tablas.ipynb**
Este notebook fusiona y procesa las métricas calculadas en tablas completas. También genera diferentes conjuntos de datos:
- Con todos los atributos.
- Sin atributos de agrupamiento.
- Sin atributos de comunidad.
- Sin atributos de núcleos.
- Sin atributos de centralidad.

#### **Estudio_de_metricas_naive_bayes.ipynb**
Analiza el impacto de las diferentes métricas en el rendimiento del modelo de Naive Bayes. Se evalúa la importancia de:
- Atributos de agrupamiento.
- Atributos de comunidad.
- Atributos de núcleos.
- Atributos de centralidad.

## Tecnologías y Bibliotecas
- Python.
- NetworkX: Análisis de redes.
- pandas: Manipulación de datos.
- scikit-learn: Modelado y validación.
- Matplotlib: Visualización de datos.

## Instrucciones de Uso

### Requisitos
1. Python 3.8 o superior.
2. Instalar las siguientes dependencias ejecutando:
   ```bash
   pip install networkx pandas matplotlib scikit-learn joblib
   ```

### Ejecución
1. Colocar los datos en la carpeta `datos/`.
2. Ejecutar `Calculo_metricas.ipynb` para generar las métricas.
3. Ejecutar `Creacion_de_tablas.ipynb` para crear las tablas procesadas.
4. Ejecutar el entrenamiento de los modelos con sus hiperparámetros.
5. Analizar los resultados.

### Resultados Esperados
- Tablas procesadas con atributos relevantes.
- Evaluación del modelo Naive Bayes sobre diferentes configuraciones.


## Proyecto elaborado por David Guillén y Luis Giraldo.
