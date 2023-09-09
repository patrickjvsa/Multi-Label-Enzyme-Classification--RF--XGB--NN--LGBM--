# Predicción de Compatibilidad Enzima-Sustrato con Modelos de Machine Learning

Este código se centra en la predicción de la compatibilidad de enzimas con sustratos utilizando modelos de Machine Learning. 
El problema se encuentra enmarcado en una competencia de Kaggle llamada "Playground Series: Predict Enzyme Substrate Compatibility" (https://www.kaggle.com/competitions/playground-series-s3e18).

# Datos:
Los datos utilizados en este informe se obtuvieron de un modelo de aprendizaje profundo entrenado en la clasificación de etiquetas múltiples de sustratos enzimáticos. El conjunto de datos presentado en la competencia consta de características seleccionadas del conjunto de datos original que resultaron ser las más informativas para el problema dado.

# Descripción del Problema:
Las enzimas son proteínas que participan en reacciones químicas, catalizando procesos y reduciendo la energía necesaria para que ocurran en un tiempo más corto. En general, las reacciones químicas son catalizadas de la siguiente manera:

Enzima libre + Sustrato (moléculas) →
Complejo enzima-sustrato → Producto + Enzima libre

La promiscuidad de enzimas es un concepto que trata sobre la falta de especificidad de las enzimas en la elección del sustrato. Un sustrato enzimático es simplemente una molécula estructuralmente identificable que puede unirse y ser modificada por la enzima. Esto significa que otras moléculas estructuralmente similares al sustrato original también pueden hacer que las enzimas actúen sobre ellas.

Sin embargo, existe un límite a la similitud de las moléculas (sustratos). De lo contrario, todas las enzimas tendrían el potencial de catalizar cualquier sustrato. A partir de esta limitación, es posible clasificar las enzimas según sus diferencias. En este contexto, se puede entrenar un modelo para predecir si las moléculas (sustratos) son compatibles con diferentes tipos de enzimas.

# Resolución:
Para resolver el problema, se proponen diversos algoritmos/modelos de ML. De forma general, se
inicia con los modelos más simples hasta llegar a los ensamblados. En particular, se utiliza: i)
Regresión Logística; ii) Árboles de Decisión; iii) Redes Neuronales Feed-forward; iv) Random Forest;
y v) Gradient Boost.

# Conclusión:
En base a los resultados obtenidos en los distintos modelos de clasificación, se decide escoger a
Gradient Boost como el de mejor desempeño, basado en su AUC-ROC superior al resto de modelos.

En particular, su capacidad para manejar datos desequilibrados y relaciones no
lineales (como los de esta muestra) y reducir tanto el sesgo como la varianza lo convierten en una
opción poderosa. Por otro lado, Gradient Boost puede ser sensible a datos ruidosos y el
tiempo de entrenamiento es mayor debido a su naturaleza secuencial.
