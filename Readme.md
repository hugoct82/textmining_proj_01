# Trabajo practico de Textmining

## Problema a resolver

Generar un sistema que identifique los temas mas relevantes dentro del ambito de las noticias diarias.


Iniciamos el proyecto generando un entorno virtual $virtualenv .env_t01



## Explicación de notebooks ipynb

### Notebook 01-captura.ipynb

A partir de la linea "1- Fuente de datos" se generán los scripts para extración, limpieza y persistencia de los datos.

Trabajaremos sobre noticias de indole economica, utilizaremos la fuentes RSS.
Se genera:

- la selección de las fuentes de noticias economicas nacionales e internacionales.
- función para extraer los datos con manejo de excepciones, en caso de que no sea posible extraer el contenido se indica por pantalla aquel que no lo permite.
- función de limpieza de los datos extraidos. Se analiza la estructura de los datos extraido para identificar lo que se requiere limpiar.
- función que guarda los datos dentro de la carpeta datos, con un formato de fecha_noticias_economicas_nacionales (o internacionales)

### Notebook 02-con-drive.ipynb

A partir de la linea "Versión final" se realizan el script que Autentica, crea carpeta, genera el servicio y envia los datos extraido a google drive.
Así mismo se incluye un script que solo sube los documentos nuevos.


## Exploración de uso de colab desde visual studio code
Dado que los modelos de claisificación requieren de GPU para que corran de manera mas rapida. Se analiza la posibilidad de incluir el entorno de colab en visual studio code. Se realizó una prueba en el notebook 07-con-colab.ipynb; dado que se requiere de una configuración del entorno y para esto se requiere tiempo para probar se decide avanzar con el uso del entorno de colab directo .


Recurso leido: https://www.freecodecamp.org/news/how-to-use-google-colab-with-vs-code/
Intrucciones
!pip install colabcode

ejecutar por consola
sudo bash install.sh

Luego en 07-con-colab se incluye:
from colabcode import ColabCode

ColabCode(port=10000, password="pass")


