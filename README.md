# SERVICIOS CON DOCKER SWARM 
## Pasos para la realización del trabajo:
### Crear los dockerfile de los servidores apache y node luego de codear dichos servidores
- El comando utilizado para crear el servidor apache fue: 
```sh
docker build -t image_apache .
```
- El comando utilizado para crear el servidor node fue: 
```sh
docker build -t image_node .
```
### Preparar el archivo .yml para desplegar los servicios
- El archivo .yml en este caso se llama: "servicios.yml"
- Se preparó el archivo luego de haber hecho pruebas en los servidores con la base de datos
### Crear los servicios con Docker Swarm
- Para crear los servicios hay que pasarle las imagenes creadas de cada servidor a los servicios que correrán dichas imagenes
- Para desplegar los servicios se utiliza el comando: 
```sh
docker stack deploy -c servicios.yml services
``` 
Donde servicios.yml es el archivo .yml con la configuracion para el despliegue y services es el nombre de los servicios