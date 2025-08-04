# Telecom_X_Desafio_2

# Análisis Predictivo de Cancelación de Clientes

Este proyecto tiene como objetivo analizar un conjunto de datos de clientes de una empresa de telecomunicaciones para predecir la cancelación del servicio (churn) y proporcionar estrategias de retención basadas en los hallazgos.

##  Descripción del Proyecto

El proyecto realiza un análisis completo siguiendo las mejores prácticas de ciencia de datos para entender los factores que influyen en la decisión de un cliente de dejar el servicio. Se implementan y comparan diferentes modelos de machine learning para crear un sistema predictivo.

##  Datos

- **Fuente**: `datos_tratados.csv`
- **Contenido**: Información de clientes incluyendo:
  - Características demográficas (género, edad, estado civil)
  - Detalles del servicio (tipo de contrato, servicios contratados)
  - Información de facturación (cargos mensuales y totales)
  - Estado de cancelación del servicio

##  Análisis Realizado

### 1. Preprocesamiento de Datos
- Eliminación de columnas innecesarias
- Codificación de variables categóricas
- Estandarización de variables numéricas
- Análisis de desbalanceo de clases

### 2. Análisis Exploratorio
- Matriz de correlación entre variables
- Análisis específico de variables clave:
  - Relación entre tipo de contrato y cancelación
  - Impacto de los cargos totales en la retención

### 3. Modelado Predictivo
Se entrenaron y compararon dos modelos diferentes:

#### Modelo 1: Regresión Logística
- Requiere normalización de datos
- Proporciona coeficientes interpretables
- Útil para entender la dirección de influencia de las variables

#### Modelo 2: Random Forest
- No requiere normalización
- Captura relaciones no lineales complejas
- Proporciona importancia de variables basada en reducción de impureza

### 4. Evaluación de Modelos
- División en conjuntos de entrenamiento (80%) y prueba (20%)
- Validación cruzada estratificada (5 folds)
- Métricas de evaluación:
  - Exactitud (Accuracy)
  - Precisión
  - Recall (Sensibilidad)
  - F1-Score
  - Área bajo la curva ROC (ROC AUC)
  - Matriz de confusión

### 5. Análisis de Importancia de Variables
- Coeficientes en Regresión Logística
- Importancia en Random Forest
- Comparación entre modelos

##  Resultados Clave

### Principales Factores de Cancelación Identificados:
1. **Tipo de contrato**: Los contratos mensuales tienen mayor tasa de cancelación
2. **Cargos y gastos**: Clientes con cargos muy bajos o muy altos tienden a cancelar
3. **Servicios contratados**: Más servicios generalmente significan mayor fidelidad
4. **Tiempo de servicio**: Clientes nuevos son más propensos a cancelar

### Desempeño de Modelos:
- Random Forest generalmente mostró mejor rendimiento en F1-Score y ROC AUC
- Ambos modelos fueron evaluados robustamente mediante validación cruzada
- No se encontró evidencia clara de overfitting

##  Estrategias de Retención Propuestas

1. **Estrategias Contractuales**:
   - Incentivar contratos a largo plazo
   - Programa de fidelización para clientes mensuales

2. **Estrategias de Valor Agregado**:
   - Paquetes de servicios combinados
   - Mejora de servicios premium

3. **Estrategias de Monitoreo**:
   - Sistema de alerta temprana basado en el modelo predictivo
   - Intervención personalizada para clientes de alto riesgo

## 🛠️ Tecnologías Utilizadas

- **Lenguaje**: Python 3
- **Librerías principales**:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
  - imbalanced-learn

##  Estructura del Repositorio

├── datos_tratados.csv # Conjunto de datos
├── analisis_churn.ipynb # Notebook principal con el análisis completo
└── README.md # Este archivo
