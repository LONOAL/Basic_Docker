# Readme para la Práctica con Docker y Ubuntu en Visual Studio Code

¡Bienvenido a esta práctica de Docker utilizando la imagen de Ubuntu en Visual Studio Code! Aquí encontrarás una guía paso a paso para realizar las tareas requeridas. Sigue estos pasos para completar la práctica de manera exitosa.

## Requisitos previos
Asegúrate de tener instalados los siguientes programas en tu sistema:
- Visual Studio Code
- Docker

## Instrucciones

### 1. Descarga la imagen de Ubuntu y comprueba que está en tu equipo

Para comenzar, abre una terminal en Visual Studio Code y ejecuta el siguiente comando para descargar la imagen de Ubuntu desde el registro de Docker:

```bash
docker pull ubuntu
```

Luego, verifica que la imagen se haya descargado correctamente:

```bash
docker images
```
### 2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre

Ahora, crea un contenedor sin asignarle un nombre con el siguiente comando:

```bash
docker run -di ubuntu 
```

Para verificar si el contenedor está en ejecución y obtener su nombre, ejecuta el siguiente comando:

```bash
docker ps
```

### 3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Cómo puedes acceder a él?

Crea un nuevo contenedor con el nombre 'dam_ubu1' utilizando el siguiente comando:

```bash
docker run -di --name dam_ubu1 ubuntu
```

Para acceder al contenedor, puedes utilizar el siguiente comando:

```bash
docker exec -it dam_ubu1 bash
```

### 4. Ayuda - Comprueba la dirección IP y realiza un ping a google.com

Dentro del contenedor 'dam_ubu1', instala las herramientas necesarias:

```bash
apt update
```
---
```bash
apt install net-tools
```
---
```bash
apt install iputils-ping
```

Verifica la dirección IP utilizando el siguiente comando:

```bash
ifconfig
```

Luego, intenta hacer un ping a google.com para comprobar la conectividad de red:

```bash
ping google.com
```

