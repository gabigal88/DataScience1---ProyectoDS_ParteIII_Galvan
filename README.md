# DataScience1---ProyectoDS_ParteIII_Galvan

Descripción de la temática abordada:

Se trata de una base de datos de una supertienda y/o supermercado que opera a lo largo de todo latinoamérica y contiene ventas y entregas de distintos productos de oficina.

A su vez, estos datos están divididos en segmentos según compradores y categorías y subcategorías de producto, así como también a que lugar geográfico fueron enviados y cuando (fecha) se realizó la venta y/o entrega abarcando un rango de fechas desde el año 2015 a inicios del año 2019

Descripción de la hipótesis:

Motivado por el “reemplazo” y “transición” de soportes físicos a virtuales dentro de lo que respecta a oficinas o lugares de trabajos administrativos es que los clientes han destinado recursos a transformación tecnológica, a su vez, existe una diversificación desde grandes empresas a más pequeñas y hasta empresas del tipo unipersonales, que produce una expansión de las ventas de equipamientos de oficina

Por otro lado, se presume que en Argentina este escenario ha tenido mayor crecimiento que en Brasil y México

En base a esto, se plantea la hipótesis de que el crecimiento interanual de las ventas de la categoría tecnología han sido mayores en Argentina en comparacion con Brasil y Mexico


Desarrollo:

* Se desarrolla un modelo que permita comparar el crecimiento interanual entre 3 paises para la categoria tecnología, y a su vez prediga las ventas para 2019 para estos 3 paises

* Para el desarrollo del modelo, es utiliza XGBRegressor, ya que se lo considera ideal para predecir valores continuos como ventas, precios, demanda, etc, (en este caso ventas)
* Al utilizar este modelo de regresion, las metricas derivadas son MSE y R2 para calcular el error en la predicción.

Resultados y concluciones:

* Evaluación del modelo XGBoost (2015–2018):
    RMSE: 0.81 --> si el modelo predice $100, el valor real podría estar entre $72 y $138, dependiendo del caso, es considerado alto
    R²: 0.43 --> El modelo explica el 43% de la variabilidad en las ventas. El otro 57% se debe a factores que el modelo no está capturando, es considerado bajo

* Si bien los valores de RMSE y R2 no son considerados optimos, cuando se evalua la predicción se observa que para Brasil y Mexico presenta cierta linealidad mientras que para Argentina se hay un salto grande.

* Para la validacion de hipotesis, se calcula el crecimiento interanual entre los paises mas la prediccion 2019, de la cual se concluye que efectivamente Argentina ha tenido mayor crecimiento en terminos porcentuales.
      Argentina:
      2015 → 2016: -1.95%
      2016 → 2017: 52.54%
      2017 → 2018: 88.00%
      2018 → 2019: 698.14%

      México:
      2015 → 2016: 38.96%
      2016 → 2017: -3.36%
      2017 → 2018: 11.00%
      2018 → 2019: 4.55%

      Brasil:
      2015 → 2016: 69.60%
      2016 → 2017: -8.79%
      2017 → 2018: 51.70%
      2018 → 2019: 53.99%

