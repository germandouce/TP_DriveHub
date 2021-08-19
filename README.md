# TP_DriveHub - FIUBA

Gestor de archivos de Drive y Gmail que permite entre otras, descargar, subir y mover archivos de Drive y recibir mails descargando sus adjuntos todo desde la terminal local del sistema.

## Creditos

El trabajo fue realizado por un equipo de 5 personas: 4 estudiantes ( https://github.com/Adonisrq94, https://github.com/GianImpedovo, https://github.com/AntonellaRanelli y https://github.com/germandus ) y una tutora ( https://github.com/ ) que nos guió y ayudo a solucionar algunos pequeños problemas que fueron surgiendo. 


## Objetivo del Proyecto

Crear un programa implementando las API's Drive y Gmail de Google que funcione de interfaz entre el usuario, Drive y Gmail con el objetivo de agilizar la recepción y almacenamiento de archivos utilizando las APIS homonimas de Google. El programa deberá estar pensado para que los archivos provenientes de Gmail puedan almacenarse de manera local y remota (Drive) a través del uso de herramientas del menu principal. Entre ellas, listar, generar, subir y sincronizar archivos.

## Organización

Para abordar el proyecto nos apoyamos en los 4 esquemas propuestos en la consigna: Sistema de Carpetas, Sistema de Archivos, Funcionalidades de Drive y Funcionalidades de Gmail. A su vez, para cumplir con los requisitos especificados también desarrollamos un menú que consta de los siguientes puntos:

1. Listar archivos de la carpeta actual
2. Crear archivos
3. Subir archivos/ carpetas
4. Descargar un archivo/ carpeta
5. Sincronizar
6. Generar carpeta de una evaluación
7. Actualizar entregas de alumnos vía mail
8. Salir

## Funcionalidades principales

* **Gmail**: 
A través de la API Gmail permite la recepción de evaluaciones (archivos), su descompresión y una validación del formato de las mismas.
* **Drive**: 
Utilizando la API Drive permite, además de navegar entre los archivos y carpetas de la nube, subir, descargar, crear y moverlos entre los directorios que especifique el usuario.
* **Sistema de Archivos**:
Posibilita la creación de carpetas y archivos con distintas extensiones.
* **Sistema de Carpetas**:
Se encarga del "matcheo" de archivos, creacion de carpetas anidadas de evaluación y asignación de profesores a alumnos sin "matchear" a partir de la información recibida del mail.
(ligado directamente a la consigna. ver: https://github.com/germandus/TP_DriveHub/blob/main/TP2_1C2021.pdf).

## Distribucion de archivos en la Repo

* **main.py**: 
Contiene la logica principal del envío y recepción de mails, el menu principal del programa y los sitemas de carpetas y archivos.
* **funcionalidad_drive.py**: 
Contiene la logica principal de las funcionalidades de Drive del programa.
* **service_drive.py**:
Contiene la Lógica que permite la generacón de Tokens para la conexion de la aplicacion con la API Drive.
* **service_gmail.py**:
Contiene la Lógica que permite la generacón de Tokens para la conexion de la aplicacion con la API Gmail.
* **TP2_1C2021.pdf**:
Contiene la consigna del TP. Incuye también los diagramas de flujo (esquemas) mencionados anteriormente con los que se estructuró y se realizó la división de tareas en el equipo.
* **instrucciones.pdf**:
Contiene una serie de instrucciones para el manejo del envio y recepción de mails desde la aplicación.

## Puesta en funcionamiento de la aplicación (Conexion con API Drive y API Gmail de Google)

1. Crear un poyecto en "Google Cloud Platform"
2. Descargar el archivo "client_secret_'random_str'.apps.googleusercontent.com.json" y guardarlo como "client_secret.json". 
3. Al correr el programa principial desde "main.py", el archivo client secret será leido por service_drive.py y service_gmail.py y se generaran los tokens necesarios para que cada usuario pueda utiizar las API Drive y API Gmail de Google.