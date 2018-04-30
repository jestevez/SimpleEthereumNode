# Nodo de ethereum con API

## Introducción

Este proyecto es un nodo básico de Ethereum preparado para conectarse a un **Bootnode** de una red privada.

El protocolo de consenso utilizado es POA (Proof of Authority).

El **Bootnode** que además es nodo firmante se puede encontrar en:

[Bootnode de Ethereum con API](https://github.com/gbarcomu/EthereumWithAPI.git)

## Puesta en marcha

En primer lugar cambiar la dirección IP para que coincida con el **Bootnode** con el script "changeEnodeIP" en la carpeta "utils":

```
./changeEnodeIP.sh xxx.xxx.xxx.xxx
```

Para construir el contenedor ejecutar el siguiente comando en el directorio raíz del proyecto.

```
docker build .
```

Para ponerlo en marcha ejecutar también en el directorio raíz

```
docker-compose up
```

### Dependencias

Únicamente es necesario tener instalado **Docker** y **Docker Compose**

## Puertos utilizados

* 30303 para la conexión con otros nodos de Ethereum

## Ejecución

Acceder al interior del contenedor docker mediante el comando:

```
docker exec -ti <nombre del contenedor> bash
```

Ejecutar la consola de **geth** con el comando:

```
geth attach /opt/data/geth.ipc
```

Una lista completa de los comandos que se pueden ejecutar en esta consola se encuentra en el repositorio oficial de **Ethereum**:

[Documentación Geth](https://github.com/ethereum/go-ethereum/wiki/geth)



