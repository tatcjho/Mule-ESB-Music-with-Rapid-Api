# Implementación de Mule con Rapi Api

## ¿Qué es Mule ESB?
Mule, el motor de tiempo de ejecución de Anypoint Platform, es un bus de servicio empresarial (ESB) ligero basado en Java y una plataforma de integración que permite a los desarrolladores conectar aplicaciones de forma rápida y sencilla, lo que les permite intercambiar datos. Permite una fácil integración de los sistemas existentes, independientemente de las diferentes tecnologías que utilicen las aplicaciones, incluidos JMS, Web Services, JDBC, HTTP y más. El ESB se puede implementar en cualquier lugar, puede integrar y organizar eventos en tiempo real o por lotes, y tiene conectividad universal.

## Ventajas
Las ventajas de usar mule son:
* Creación y alojamiento de servicios: exponga y aloje servicios reutilizables, utilizando el ESB como un contenedor de servicios ligero
* Mediación de servicios: proteja los servicios de los formatos y protocolos de mensajes, separe la lógica empresarial de la mensajería y habilite llamadas de servicio independientes de la ubicación
* Enrutamiento de mensajes: enrute, filtre, agregue y vuelva a secuenciar los mensajes según el contenido y las reglas
* Transformación de datos: intercambie datos en distintos formatos y protocolos de transporte

	

## ¿Qué es Rapi Api?

RapidAPI, el mercado de API más grande del mundo, es utilizado por más de un millón de desarrolladores para buscar, probar y conectarse a miles de API, todo con una sola cuenta, clave de API y SDK.

Encuentre las API que necesita para su proyecto, incruste la API en su aplicación y realice un seguimiento del uso de todas sus API a través de un solo panel. Si crea una API, use RapidAPI para ponerla a disposición de más de 1 millón de desarrolladores que ya utilizan nuestro Marketplace.

## Implementación
Nuestro proyecto trata sobre la creación de un sistema distribuido en la web, bajo arquitectura SOA, en el que se implemente un proceso de negocio , el mismo que deberá implicar a un mínimo de tres proveedores de distintos servicios, el cual se ejemplificará en la creación de un sistema distribuido bajo la arquitectura de SOA que permitirá a un usuario poderse registrar, loguear y posteriorimente elegir servicios que le pueda ayudar a crear una cita perfecta, en este caso tiene que escoger por la decoración, música y comida, de esta manera permitirá enviar una invitación a su cita con todos los campos seleccionados. Cabe recalcar, que esta aplicación se desarrollo en base al confinamiento y la preservación del distanciamiento social que se ve evidenciado por el COVID-19. 

Utilizamos la api de shazam para que el usuario escoja una cancion donde se puede evidenciar en la invitacion a su cita.

### Shazam API
Su API le proporciona herramientas para encontrar identificar cualquier cancion, descubrir artistas, letas de canciones, videos, y playlist.

 
## PASOS 

#### PASO 1: 
##### Instalación de AnypointStudio: https://www.mulesoft.com/lp/dl/studio
Posterior a la descarga, se instala normalmente seleccionando donde queremos nuestro carpeta de trabajo  y abrimos. 
La arqutiectura que se visualiza a continuación es un HTTP listener, donde indicaremos el puerto, el path de nuestro servicio que obtendremos y la direccion a la que enviaremos. El request hace referencia a la obtención del enlace de Rapi API con todas sus credenciales que necesitamos, ademas del encabezado y otros requerimientos.
![1](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/1.PNG)

### Arquitectura Mule ESB Musica with Rapi Api
![2](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/2.PNG)


### Configuracion del listener
1) A continuación ponemos el path del servicio a obtener y seguido de "/" ponemos el parametro que queremos obtener.
![2](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/3.PNG)

2) A continuación configuramos el puerto y el host. 
![3](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/4.PNG)


### Configuracion del request
1) Configuración de la url que obtenemos de la api 
![4](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/5.PNG)

2) Configuración del path y del método  
![5](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/6.PNG)


1) Configuración de la url que obtenemos de la api 
![6](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/7.PNG)


### Ejecución
![7](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/8.PNG)

### Pruebas
2) Ingresamos a través del navegador, con el host, el puerto y la solicitud que enviamos como se visualiza a continuación:  
![8](https://github.com/tatcjho/Mule-ESB-Music-with-Rapid-Api/blob/main/SOA%20MUSICA/9.PNG)

En este ejemplo agregamos la palabra "one" y obtuvimos el resultado. 

