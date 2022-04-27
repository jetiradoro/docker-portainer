# Descripción

Generación de contenedor **DOCKER** a través de archivo **DOCKER COMPOSE** para levantar el servicio 
**PORTAINER** para la gestión visual de contenedores docker. 

## Referencia de documentación

- https://www.portainer.io/

# Instalación

1. Clonar el proyecto localmente 
2. Copiar el archivo `.env.example` a uno nuevo llamado `.env`
3. Configurar las variables de entorno segun la necesidad de cada uno
4. Insertar la entrada correspondiente en el archivo `/etc/hosts`
```bash 
sudo nano /etc/hosts
```

```bash 
127.0.0.1 portainer.loc
```

>Donde *portainer.loc* sería el nombre del domino que hayáis puesto en la variable de entorno DOCKER_DOMAIN


Las variables **NET_EXTERNAL** y **VOLUME_EXTERNAL** hacen referencia a si el volumen o la red son compartidos con otros contenedores.

5. Cuando estén todos los archivos con la configuración deseado solo queda levantar el contenedor
`docker-compose up -d`