## Práctica Módulo Devops KeepCoding BootCamp.

La práctica de este modulo consiste básicamente en la creación de un servidor y el despliegue de una serie de aplicaciones en el mismo.

El primer paso a realizar es la creación de un nuevo "servidor". Para realizar esta tarea se opta por la utilización del servicio EC2 que ofrece AWS (Amazoon Web Services).

Se crea una nueva "instancia" de servidor con una configuración inicial a la que se ha utilizado en las clases del módulo:

###Características del Servidor:
1.- **S.O**: Ubuntu 16.04
2.- **

Una vez creada la instancia del servidor se genera el **certificado** necesario para poder realizar la conexión a través del servicio de **ssh** con el comando comando:

`ssh -i <certificado.pem> ubuntu@<nombre_del_dominio>`

Donde **<certificado.pem>** es el certificado que se ha generado y **<nombre_del_dominio>** es el dominio que AWS he creado para nosotros, en este caso:

DNS: **ec2-34-241-15-53.eu-west-1.compute.amazonaws.com**

Del mismo modo AWS también proporciona una dirección IP pública para poder realizar las conexiones o mejor dicho, las peticiones a nuestro servidor:

IP: **34.241.15.53**

Una vez el servidor se ha creado y esta en funcionamiento es hora de realizar la instalación de Nginx que es el encargado de realizar el papel de **servidor web** de aquellos *sites* y *app's* que desplegemos.

Para instalar Nginx basta con utilizar el comando:

`sudo apt-get install nginx`
