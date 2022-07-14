### Desafio 2 - Grupo 7

El objetivo del desafio 2 es predecir el precio por metro cuadrado de las propiedades de múltiples barrios de CABA y algunos de zona norte del Dataset provisto por Properatti aplicando una *Regresión Lineal Múltiple con Modelos Regularizados (Lasso y Ridge) y Sin Regularizar*. 

El objectivo de aplicar los métodos de regularización Lasso y Ridge es probar si el modelo mejora, tanto en sus métricas como en la cantidad de variables explicativas. En ambos casos utilizamos la técnica de Cross Validation para encontrar el mejor alpha para el conjunto de datos.

Las transformaciones y limpieza de datos más relevantes que realizamos son:

1. Completamos la columna rooms extrayendo con `Regex` de la columna description.
2. Eliminamos outliers utilizando rangos intercuartiles.
3. Seleccionamos los barrios en cuestión a partir de la columna_placename.
4. Creamos nuevas columnas que transformaremos a dummies determinando si la propiedad en cuestión tiene piscina, balcon, estacionamiento, si es a estrenar, si tiene subte, metrobus, o tren cerca, y si cuenta con seguridad.
5. Calculamos la superficie descubierta de cada propiedad.
