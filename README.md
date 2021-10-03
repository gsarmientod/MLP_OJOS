# MLP_OJOS
Detección de ojos con Pytorch aplicando MLP.  
  
  Muchos de los sistemas de reconocimiento de personas por medio de imágenes utilizan la ubicación de puntos importantes en la cara, con el objetivo de identificar la ubicación del rostro. Algunos puntos importantes son los ojos, la nariz y la boca, a partir de ellos es posible definir las coordenadas entre las cuales se encuentra ubicada la cara de la persona. La detección de estos puntos es escencial para los algoritmos de reconocimimiento facial.  
   
  El objetivo de este notebook es realizar un sistemas de identificación de la ubicación de los ojos a partir de imágenes.Para ello, implementamos un modelo de redes neuronales MLP para utilizando un conjunto de 1236 imagenes que fueron previamente etiquetdas por el proyecto "GI4E - Gaze Interaction for Everybody" de la Universidad Pública de Navarra, dispuesta en el siguiente link: https://www.unavarra.es/gi4e/databases/gi4e/. 

Esta base de datos contiene 1236 imagenes en formato png de 103 personas con una resolución de 800×600 pixeles, cada persona cuenta con 12 imagenes. Cada imagen viene acompañada de su etiqueta en los ojos, de tal manera que cada una de las imagenes tiene un archivo .txt asociado agrupado por persona, con la siguiente información: x1 y1 x2 y2 x3 y3 x4 y4 x5 y5 x6 y6, en donde:

    * Los puntos (x1,y1) corresponden a las coordenadas de la parte externa de la cornea en el ojo izquierdo
    * Los puntos (x2,y2) corresponden a las coordenadas del centro del iris del ojo izquierdo 
    * Los puntos (x3,y3) corresponden a las coordenadas de la parte interna de la cornea en el ojo izquierdo
    * Los puntos (x4,y4) corresponden a las coordenadas de la parte externa de la cornea en el ojo derecho
    * Los puntos (x5,y5) corresponden a las coordenadas del centro del iris del ojo derecho 
    * Los puntos (x6,y6) corresponden a las coordenadas de la parte interna de la cornea en el ojo derecho

De esta manera el objetivo de este ejercicio es predicir los valores de x1 y1 x2 y2 x3 y3 x4 y4 x5 y5 x6 y6. Las imagenets contiene personas distintas, con gafas, sin gafas mirando en diferentes direcciones.


Estas imagenes fueron reescaladas y se utilizaron como entrenamiento de un modelo de redes neuronales Multy Layer Perceptron con el objeto de obtener las coordenadas de los ojos. Depués de entrenado el modelo, se evaluó su desempeño.
