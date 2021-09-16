# Big-Data-Analytics-Taller-1
Repositorio del primer taller de Big Data con el reporte de las partes realizadas.

# Parte 1 y 2
Hadoop se encuentra optimizado para ser ejecutado en sistemas operativos basados en el kernel Linux y requiere de la JVM (Java Virtual Machine) para su ejecución.

Si no dispone de un sistema operativo Linux, descargue e instale VirtualBox o VMWare.
Cree una máquina virtual e instale sobre esta un sistema operativo basado en Linux como Ubuntu.
Siga los pasos dispuestos en esta guía para desplegar Hadoop en modo pseudo-distribuido. También puede apoyarse de la guía oficial que encuentra en la página de Apache.

MapReduce es el componente de Hadoop que se encarga de procesar grandes volúmenes de datos de manera distribuida y escalable.

Una vez instalado Hadoop, en la guía oficial de Apache, sección “Execution”, pasos 4 al 7, encontrará las instrucciones para correr un programa de ejemplo. Ejecútelo, intente analizar los logs que se muestran en consola así como los archivos generados en la carpeta output. También puede ser útil analizar el código fuente del ejemplo. Responda:
¿Qué resultados generó el programa y cuales son los pasos MapReduce que implementa?

![Screenshot (1123)](https://user-images.githubusercontent.com/81723932/133597750-893ac331-83fa-4943-bbd7-67848c55a546.png)
![Screenshot (1124)](https://user-images.githubusercontent.com/81723932/133598433-9d5e023d-fd37-4218-9d9d-9f308cc4f6c9.png)
![Screenshot (1125)](https://user-images.githubusercontent.com/81723932/133598484-18429e30-b75c-4708-a638-5818abb297f1.png)
![Screenshot (1126)](https://user-images.githubusercontent.com/81723932/133598586-dfb03514-73e4-4914-b393-88d66b31d1b9.png)
![Screenshot (1127)](https://user-images.githubusercontent.com/81723932/133598679-313ec3f9-3f90-413e-9ffc-107d189cce30.png)
![Screenshot (1128)](https://user-images.githubusercontent.com/81723932/133598761-d9926219-d34d-4c85-9e67-8e024934d47f.png)
![Screenshot (1129)](https://user-images.githubusercontent.com/81723932/133598963-330afedf-7ef3-4ae8-a0d0-8083ca28f7c9.png)

Poniendo de un lado los logs de la cantidad de las operaciones de los bytes leidos y escritos; tenemos un par de logs que nos informan de la cantidad de veces que se hizo la operacion de "map" y la operacion "reduce", entre otros que nos muestran cuantos bytes se dividieron/combinaron/registraron. Los pasos irian asi: toma de datos, mapeo, shuffle (aunque su log aparece despues, es solo el de errores), reduccion, salida (output).

En el mismo jar de ejemplos encontrará otros algoritmos con los que puede experimentar. Cargue al HDFS cualquier documento en texto plano (un poema, un libro, una canción, etc.) y ejecute el programa WordCount. Realice el mismo análisis anterior. Responda:
¿Qué resultados generó el programa y cuales son los pasos MapReduce que implementa?

![Screenshot (1130)](https://user-images.githubusercontent.com/81723932/133599139-6aa0fa75-09c9-480b-9c02-87fcb9c285c3.png)
![Screenshot (1131)](https://user-images.githubusercontent.com/81723932/133599328-7d50e8ec-18d5-400c-bd12-ec909223bbed.png)
![Screenshot (1132)](https://user-images.githubusercontent.com/81723932/133599520-5ab4e374-0dfc-482a-b4b8-80c83d7daf48.png)
![Screenshot (1133)](https://user-images.githubusercontent.com/81723932/133599606-d0b62720-ae4a-46f7-a739-2cd0455b34f7.png)

Es basicamente identica a la anterior excepto que no realiza el proceso de map y reduce dos veces, y los archivos output cambiaron.


# Parte 3
En los últimos años, Spark ha ganado una importante popularidad respecto a Hadoop/MapReduce para procesamiento distribuido de datos. La clave de Spark es su procesamiento en memoria. También tiene la ventaja de que puede ser programado en otros lenguajes más compactos como Scala, Python y R.

En una nueva máquina Linux, deseablemente, siga las instrucciones dispuestas en esta guía para instalar Spark en Ubuntu.
Revise el código de WordCount dispuesto como ejemplo en la web oficial de Spark y entiéndalo para que realice los cálculos de conteo de palabras sin tener en cuenta mayúsculas/minúsculas y signos de puntuación.

Ejecute los códigos original y extendido en PySpark y analice los resultados.

![Screenshot (1135)](https://user-images.githubusercontent.com/81723932/133601334-a22b8bf9-2190-439a-97ef-70c443dfb873.png)
![Screenshot (1136)](https://user-images.githubusercontent.com/81723932/133601730-86901c7a-5720-44fd-9156-75f229550a92.png)
![Screenshot (1137)](https://user-images.githubusercontent.com/81723932/133601785-37ffc514-32d4-4962-a1b7-be1cf8fc7628.png)
![Screenshot (1138)](https://user-images.githubusercontent.com/81723932/133601832-0d97cc34-5603-49f8-8fb5-256ada4ba5fb.png)
![Screenshot (1139)](https://user-images.githubusercontent.com/81723932/133602212-45423a47-69bd-4179-bb96-8c5c300161df.png)
![Screenshot (1140)](https://user-images.githubusercontent.com/81723932/133602256-5ea69d6b-9c80-4e7b-ab43-b1c1ca5446a7.png)
![Screenshot (1141)](https://user-images.githubusercontent.com/81723932/133602309-95935bca-60ba-4ac5-b542-9062a7adb5f8.png)
![Screenshot (1142)](https://user-images.githubusercontent.com/81723932/133602386-fb0c7234-cb34-4bd8-ad2b-b8b962b058d6.png)

Sets de palabras fueron creadas con el string de la palabra y un numero identificador para el set que se la asigno, aunque la version Scala no muestar dicho numero en el txt creado.

# Parte 4
Como con cualquier otra herramienta, desarrollar un programa de computador desde la interfaz de línea de comandos es una labor tediosa. Por lo general, los desarrolladores recurren a entornos de desarrollo (IDE) que ofrecen gran variedad de apoyos a la codificación en términos de evaluación de sintaxis, debugging, conexión con recursos externos, entre muchos otros.

Dentro de la máquina virtual, en la carpeta de su preferencia, clone el repositorio localizado en este link. Este repositorio contiene 2 scripts que serán trabajados más adelante así como una carpeta data con un archivo TXT. Sobre esta misma carpeta descargue y descomprima el archivo ubicado aquí.

Dentro del mundo de Python y el análisis de datos, Jupyter Notebooks es una de las herramientas de desarrollo más ampliamente usadas. Descargue e instale Anaconda en la misma máquina virtual en donde instaló Spark.

Este paquete de software, entre muchas otras cosas, contiene el entorno de desarrollo Jupyter Notebook. Para iniciarlo, desde una terminal y ubicado sobre la misma carpeta en la que clono el repositorio previamente, digite el comando: jupyter lab --ip=0.0.0.0.

Desde la misma máquina o desde otra máquina virtual o física abra un navegador web y diríjase a: http://<puerto>:8888/lab/. Si todo va bien hasta este punto, desde la página web que se abre debería poder visualizar la estructura de archivos del repositorio clonado.

![Screenshot (1143)](https://user-images.githubusercontent.com/81723932/133606127-d4cf65b9-5f45-4729-a74d-05fae60c025e.png)
  
Ejecute los scripts spark-basics.ipynb y spark-data-analysis.ipynb. Analice cada archivo y detalle los elementos más importantes de cada uno.
  
spark-basics.ipynb:
  
![Screenshot (1144)](https://user-images.githubusercontent.com/81723932/133606235-5fdc19bd-166e-4407-9005-28546604f942.png)
![Screenshot (1145)](https://user-images.githubusercontent.com/81723932/133606378-2043d639-c403-4065-9468-15bab3b26ca4.png)
![Screenshot (1146)](https://user-images.githubusercontent.com/81723932/133606445-6572c68e-498c-4694-82de-7cc9183503bd.png)
![Screenshot (1147)](https://user-images.githubusercontent.com/81723932/133606642-c91dabe5-0f8b-49b5-a37d-c3e7a212fc4a.png)
![Screenshot (1148)](https://user-images.githubusercontent.com/81723932/133606739-1e0d635b-a6ed-4e9a-b20e-09fac0c282da.png)
![Screenshot (1149)](https://user-images.githubusercontent.com/81723932/133606792-c8960d9c-39d2-4922-9b2c-ea4b244088b4.png)
![Screenshot (1150)](https://user-images.githubusercontent.com/81723932/133606834-f211435e-42ac-4edf-aafe-119e3bbf59e0.png)
  
Lo que sucede en la primera seccion es simplemente la carga de datos de diferentes tipos, la secciones mas importantes serian las de operaciones RDD en donde se mapea, filtra y reduce los sets de data;  y la ultima seccion la cual es para agrupar y ordenar la cantidad de veces que se repitio una palabra en orden ascendente.

spark-data-analysis.ipynb:
  
![Screenshot (1151)](https://user-images.githubusercontent.com/81723932/133607247-cf17e2cd-021a-4ab8-a87f-fbab4400a805.png)
![Screenshot (1152)](https://user-images.githubusercontent.com/81723932/133607340-caf3880a-e379-424d-bcec-72433067bff8.png)
![Screenshot (1153)](https://user-images.githubusercontent.com/81723932/133607392-a44915de-8769-475d-b0b4-1b2744ad6503.png)
![Screenshot (1154)](https://user-images.githubusercontent.com/81723932/133607444-7b485807-af8f-4f12-b179-665540d57e6c.png)
![Screenshot (1155)](https://user-images.githubusercontent.com/81723932/133607594-7f38a558-da2a-4dbd-b50f-8e1f181b4afd.png)
![Screenshot (1156)](https://user-images.githubusercontent.com/81723932/133607683-41a52011-787d-4368-bc04-e9b0b4dc55ac.png)
![Screenshot (1157)](https://user-images.githubusercontent.com/81723932/133607763-2a40e853-5d54-41dc-a8c0-417ea227b7ef.png)
![Screenshot (1158)](https://user-images.githubusercontent.com/81723932/133607829-9748a050-da85-466e-b972-0edcea556f63.png)
  
En este caso la seccion de la seccion de carga de datos es mas importante debido a que en esta se especificara la forma en la cual deben ser manejados los datos por los comandos RDD mas alante en el programa, en la segunda seccion con excepcion de una par de comandos necesarios para la visualizacion de las graficas, el resto de comandos son muy standard para lo que concierna SQL y su manera de recopilar informacion, la tercera seccion simplemente guarda los sets de datos obtenidos en la segunda seccion en un directorio de JSONs, asi que diria que todos los comandos en la segunda seccion son la parte mas importante ya que estos son los que compilan la informacion a guardar.
  
 Masters y Workers:
  
![Screenshot (1159)](https://user-images.githubusercontent.com/81723932/133607890-9edc91f7-1ffd-41fe-a8d8-7c545c864088.png)
![Screenshot (1160)](https://user-images.githubusercontent.com/81723932/133607932-cd4ec067-ed75-4690-9016-5a115de80e52.png)



