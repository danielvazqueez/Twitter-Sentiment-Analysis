# Twitter Analisis de Sentimiento

## ¿Que hace el proyecto?

### Primera parte
El proyecto consiste en entrenar diferentes modelos para el reconocimiento de lenguaje natural y hacer una clasificación dependiendo si el texto es positivo o negativo.
Para la primera parte del proyecto se realizo siguiendo el siguiente tutorial: https://www.youtube.com/watch?v=FLZvOKSCkxY&list=PLQVvvaa0QuDf2JswnfiGkliBInZnIC4HL. Cambiando
la información que se estaba usando para entrenar los modelos a una proporcionada por Kaggle de Tweets.

Una vez construidos los modelos, se realiza el analisis de sentimiento en los Tweets en tiempo real usando la API de Twitter y se grafican también en tiempo real a manera de ver si los tweets de un tema en especifico son más negativos o más positivos o neutral

---
## Extras del proyecto
Se realizaron diferentes funcionalidades aparte del modelo principal como parte de la exploración del proyecto

### Red neuronal recurrente 

### Analisis de Comentarios de Amazon
La sección de sentiment analysisi en reseñas de Amazon emplea los mismos modelos de clasificación que se utilizaron para tweets pero para reseñas de productos de Amazon. Se usa la calificación en estrellas (1-5) para determinar si el valor real de la reseña es positivo o negativo. Las reseñas con 3 estrellas o menos son consideradas negativas, mientras que las de 4 y 5 son positivas. Partiendo de eso, se balanceó la cantidad de reseñas positivas y negativas para que la distribución fuera 50/50, y se aplicó el modelo de sentiment analysisi ya entrenado para tweets. El resultado fue muy malo, logrando un accuracy de apenas el 53%. Con este resultado, podemos concluir que no se puede construir un modelo que se comporte favorablemente a través de todas las aplicaciones imaginables, y que para aplicar un modelo de NLP se debe entrenar específicamente para cada caso de uso. Para mejorar la precisión, sería necesario entrenar el modelo con datos de reseñas y obtener una cantidad mayor de datos distribuidos entre negativos y positivos, ya que la base de datos utilizada era casi 90% de datos positivos, siendo el 78% de 5 estrellas.

### Analisis de Comentarios de Youtube relacionado a likes y dislikes
El documento de sentiment analysis en YouTube emplea diversos modelos de clasificación de texto entrenados con la base de datos de Twitter para realizar dicha clasificación en comentarios de videos de YouTube. La intención de dicho programa no es de analizar el rendimiento de estos modelos (esto se realizó anteriormente obteniendo valores de accuracy cercana al 80%), sino de analizar la relación entre el porcentaje de comentarios positivos (100 * positivos / (postivios + negativos)) y el mismo de likes (100 * likes / (likes + dislikes)).

En cuanto a los resultados, se esperaba obtener una tendencia relativamente lineal que demostrase algún grado de correlación. No obstante, no se encontró ninguna tendencia o relación entre ambas variables, aunque esto no necesariamente significa que no valió la pena el desarrollo del modelo, puesto a que se pueden realizar diversas observaciones sobre los resultados (como una mayor tendencia en comentarios negativos que dislikes), el tipo de texto en los comentarios (como el hecho que son más cortos que Twitter y tienen una peor redacción y claridad), y acerca de los propios modelos (como las limitaciones de emplear algoritmos entrenados en una red social en otra).

### Reconocimiento de voz para el analisis de sentimiento
El proposito de agregar esta parte era para extender las aplicaciones que le podemos dar a nuestro modelo en diferentes escenarios de la vida cotidiana. El modelo de analisis de texto nos permite aplicarlo en conversaciones o grabaciones al convertir estas en texto y despues pasarlas por nuestro analisis de sentimiento. Un ejemplo claro en el que creemos que se puede aplicar es en llamadas de servicio a cliente para medir el sentimiento de la conversacion de los clientes a lo largo de la llamada y ver como se comporta este.
Para realizar el reconocimiento de voz se utilizaron 2 librerias para ver cual era mejor al reconocer el lenguaje. La primera fue la API de Google Speech y la segunda es la libreria de Speech Recognition proveida por python.

## ¿Por qué es útil el proyecto?
El proyecto nos permite ver las diferentes técnicas que existen para el reconocimiento de Lenguaje Natural y ver las ventajas y desventajas de cada uno de ellas. 
En los extras del proyecto intentamos a aplicar nuestros modelos a otros dominios para intentar hacer una predicción en un diferente contexto, sin embargo vemos que el rendimiento no es el esperado al que estabamos viendo con los tweets.
Esto se puede deber a múltiples factores ya que la información no esta muy bien balanceada o puede ser que el lenguaje informal y cotidiano de Twitter no se pueda aplicar a las reseñas de productos en Amazon o a comentarios en videos de Youtube.

## ¿Como empezar a desarrollar para el proyecto?
Se realizaron diferentes notebooks donde cada una esta relacionada a las diferentes técnicas o fuentes de información que se realizaron por cada integrante del equipo

## Para más información del proyecto
Para más información de este proyecto y de las aplicaciones que se investigaron dejamos unos links con las fuentes que resultaron de mucha ayuda para el desarrollo de este proyecto

https://www.kaggle.com/datasnaek/youtube?select=USvideos.csv
https://www.kaggle.com/c/twitter-sentiment-analysis2

## Contribuidores del proyecto
- Luis Daniel Vazquez (luis_060198@hotmail.com)
- Johan André Caballero (Johan.morlesin@gmail.com)
- Oscar Peña (oscarp_98@hotmail.com)
- Rodrigo Montero Castro (a01177008@itesm.mx)

