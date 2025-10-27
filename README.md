# Predicción de Falla en Juntas Tóricas del Challenger 🚀

Este proyecto analiza los datos históricos de los lanzamientos de los transbordadores espaciales de la NASA para predecir la probabilidad de falla de las juntas tóricas (O-rings) en función de la temperatura. El análisis se centra en el contexto del trágico accidente del transbordador espacial Challenger en 1986.

##  Contexto: El Accidente del Transbordador Espacial Challenger 🛰️💥

El 28 de enero de 1986, el transbordador espacial **Challenger** se desintegró trágicamente tan solo 73 segundos después de su lanzamiento, resultando en la pérdida de sus siete tripulantes. La causa principal del desastre fue una falla catastrófica en una de las **juntas tóricas** del cohete acelerador sólido (SRB) derecho.

La investigación posterior, llevada a cabo por la "Comisión Presidencial sobre el Accidente del Transbordador Espacial Challenger", reveló que la NASA había cometido errores graves en la toma de decisiones, ignorando las advertencias de los ingenieros sobre los riesgos de lanzar el transbordador a temperaturas inusualmente bajas. El día del lanzamiento, la temperatura en Cabo Cañaveral era de 31°F (-0.5°C), muy por debajo de las temperaturas de lanzamientos anteriores.

## ¿Qué son las Juntas Tóricas? 🤔

Las **juntas tóricas** (conocidas en inglés como *O-rings*) son anillos de goma diseñados para asegurar la estanqueidad y evitar fugas de fluidos (líquidos o gases) entre dos piezas. En el caso de los cohetes aceleradores del transbordador, su función era sellar las uniones entre los diferentes segmentos del cohete para evitar que los gases calientes de la combustión se escaparan.

El material de estas juntas era sensible a la temperatura. Con el frío extremo 🥶 del día del lanzamiento, las juntas tóricas perdieron su elasticidad, volviéndose rígidas y frágiles. Esto impidió que sellaran correctamente la unión, permitiendo que una llama se filtrara y provocara una reacción en cadena que terminó con la desintegración del vehículo.

## Análisis de Datos del Notebook 📊

El Jupyter Notebook de este repositorio (`NASA_Challenger_Predicción_de_Falla_en_Juntas_Toricas.ipynb`) realiza un análisis de regresión logística para modelar la relación entre la temperatura de lanzamiento y la probabilidad de falla de las juntas tóricas.

Los pasos principales del análisis son:
1.  **Carga de Datos 💾:** Se utiliza un DataFrame de Pandas con datos históricos de 24 lanzamientos previos, registrando la temperatura (°F) y si ocurrió (1) o no (0) una falla en la junta tórica.
2.  **Visualización 📈:** Se crea un gráfico de dispersión para observar la tendencia: a menor temperatura, mayor es la incidencia de fallas.
3.  **Modelo de Regresión Logística 🧠:** Se entrena un modelo de regresión logística binaria utilizando la temperatura como variable predictora y la falla de la junta tórica como variable objetivo.
4.  **Predicción 🔮:** Se utiliza el modelo entrenado para predecir la probabilidad de falla a la temperatura de 31°F, la temperatura del día del fatídico lanzamiento.

### Resultados 🎯

El modelo de regresión logística predice una **probabilidad de falla del 99.60%** para una temperatura de lanzamiento de 31°F.

```python
Predicción de la probabilidad de falla según el modelo a 31 grados: 0.9960
