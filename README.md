# Docker-Kubernates-PostgresWithDocker

## Correr un contenedor

```
doker run imageName
```

## Descargar una imagen que ya tenias en la maquina y si no existe, tambien lo hace

$ docker pull imageName 

## Ver todas los contenedores que estan almacenadas en la maquina local 

$ docker images 

## contenedores que estan siendo corridos en la maquina local 

$ docker ps

## contenedores que corrieron hace algun tiempo (no son el historial completo)

$ docker ps -a 

## observar los logs de las imagenes

$ docker logs dockerName

## Parar los contenedores

$ docker stop dockerName

## crear un contenedor 

$ docker build -t perficientProject .

## para correr la aplicacion con Docker 

$ docker run -dp 8080:8080 perficienttraining -d

## Ver imagenes con nombres especificos

$ docker images |grep nameImage

## Persistir en los datos, es decir, para no iniciar el contenedor de 0 sigo, poder seguir tabajando sobre el mismo

$ docker run -d -v C:\Users\brayan.burgosd\Documents\PerficientTraining -p 8080:8080 perficienttraining

## Con esta linea, NO debo de para mi app para poder hacer cambios en el codigo, para y volver a correr

docker run -d -v C:\Users\brayan.burgosd\Documents\PerficientTraining -p 8080:8080 -v \Users\brayan.burgosd\Documents\PerficientTraining perficienttraining
bf16e3c39b7b60505577ef1da7125201e9c27ef58ee175f3dae65b3d50973134

## compartir las images en internet

## Verificar que en la app de docker, ya te hubieses logeado y luego:

$ docker login

## Tagear con la version de la imagen

$ docker tag - iddelaimagen:v2 perficienttrainingv2

## Pusear la imagen al repositorio de docker 

$ docker push nombredelaimagen 


## Como crear una red de docker

## crear una nueva red 

$ docker network create networkperficienttraining

## Como usar postgres desde un contenedor de Docker 

1. Buscar una imagen de postgres en dockerhub

$ docker run -p 5432:5432 --name persistenceperficienttraining -v C:\Users\brayan.burgosd\Documents\PerficientTraining\posgrest:/var/lib/postgresql/data2 -e POSTGRES_PASSWORD=secret  postgres

$ docker exec -it persistenceperficienttraining psql -U postgres

https://refactorizando.com/ejemplo-spring-data-postgresql-docker/
https://github.com/4SoftwareDevelopers/demo-crud-spring-boot/tree/develop/


$ CREATE DATABASE perficientProject

## Como correr el docker compose que se creo por cmd 

$ docker-compose up

## Kubernates

version de kubernate 

$ kubectl version --client=true
