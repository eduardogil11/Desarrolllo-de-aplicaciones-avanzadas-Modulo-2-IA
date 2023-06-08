# Desarrolllo-de-aplicaciones-avanzadas-Modulo-2-IA
Repositorio Módulo 2 Inteligencia Artificial

# Implementación de Data augmentation Pokemon
### De un Dataset que ya existia obtuve varias imágenes de los diferentes Pokemon que existen y cree mi propio Dataset clasificando a los Pokemon por 3 tipos Water, Fire, Grass.

* Para poder ver el Dataset creado podemos descargar la carpeta "Actividad Data Augmentation Pokemon" o entrar al link del Drive donde se encuentra el Dataset: "https://drive.google.com/drive/folders/1olB6nF12ulosWk_j1BZL-ldGxeiyXDbN?usp=sharing".
* No es necesario descargar el Dataset, ya que la implementación se conecta a Drive para extraer el Dataset desde ahí.
* Para poder probar la implementación del Data Augmentation Pokemon necesitamos descargar el Jupyter Notebook llamado "Data_augmentation_pokemon"
* O podemos entrar directo al Notebook desde GitHub y ver los resultados.
* Posteriormente corremos el Notebook..

# Red Neuronal
Para este proyecto se hicieron las pruebas con tres redes neuronales.
* La primera fue una red neuronal convolucional que tiene tres capas concolucionales, 2 capas densas y un dropout.
* La segunda se hizo la prueba con el modelo VGG16 que este ya esta pre-entrenado y cuenta con 16 capas de profundidad conectadas en sequencia.
* La tercera se probo con el modelo VGG19 que de igual forma este ya esta pre-entrenado y cuenta con 19 capas de profundidad conectadas en sequencia.

# Cambios
Algunos de los cambios que se fueron realizando al paso del tiempo, fue principalmente quitar una de las clases que se tenían que fue la de Electric, ya que daba muchos problemás en los modelos. Después se realizaron cambio el los tres modelos, para el caso de la red neuronal convolucional se agregaron más capas convolucionales, para el modelo VGG16 se aumento la capa densa y se agrego un dropout y para el caso del modelo VGG19 se agregaron dos dropout y en todos los modelos se adapto para que no fuera binario y fuera categorical debido a la cantidad de clases que se tiene.

# Resultados
Como podemos observar en los tres modelos nuestro test accuracy est bastante similar en las tres situaciones saliendo como el mejor el modelo VGG16 y el peor el VGG19, pero para nuestro accuracy de entrenamiento el que llego a salir más alto fue nuestro modelo VGG19. Esto nos dice que nuestro modelo si esta llegando a aprender pero en los tres modelos llegamos a tener overffiting, esto pasa al tener unas imagenes complicadas, ya que como se menciona al inicio se contaba con una clase de Pokemon Electic, pero esta se decidio eliminar por la cantidad de problemas que causaba reconoceindo todos los Pokemon como Electric y obteniendo test accuracy super bajos como de 23. Al quitarla se logro aumentar considerablemente el test accuracy aunque todavía tenía overfitting y al visualizar las matrices de confusión podemos ver que las tres eran difentes dandonos más Pokemon en una clase que en otra. Este principal problema es por la complejidad que tiene los Pokemon, ya que si nos metemos a indagar en el dataset podemos observar que a pesar de que los Pokemon de Water son casi todos azules, los Pokemon de Fire son casi todos rojos o naranjas y los Pokemon de Grass son casi todos verdes, hay algunos Pokemon que tienen diferentes colores un ejemplo sencillo es que por ejemplo existe un Pokemon que es de tipo Water y tiene una forma de pez, pero es completamente verde, esta situación llega a suceder en las 3 clases existentes. Otro de los problemás principales que tenía la clase Electric es que los Pokemon eran casi todos amarillos, pero tenían formas super diferentes cada Pokemon como podía llegar a ser una rata amarrila, hasta podía ser un pescado blanco de tipo Electric, esto no pasa mucho en las 3 clases que se tienen, ya que casi todos los Pokemon de tipo agua tienen formas de animales maritimos, los tipos Fire y Grass tienen una forma de ser particulares cada tipo. Pienso que estos 3 tipos son más sencillos y faciles que los de más tipos de Pokemon que existen, ya que son los tipos principales del juego, pero si nos ponemos a observar en los 18 tipos de Pokemon que hay vamos a obsevar que entre más raro sea el tipo de Pokemon más complejidad va a tener.
Por último, podríamos lograr que mejoren los modelos mejorando los datos, ya que como observamos el principal problema no son los modelos porque estos si aprender, lo que podriamos hacer es agregar algo particular de cada tipo de Pokemon como sus ataques al dataset, para que este le sea más simple de identificar de que tipo de Pokemon y no se tenga el problema del overfitting.
