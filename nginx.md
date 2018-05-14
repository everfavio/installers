# Instalacion de nginx

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

# paso 1
Instalamos los paquetes necesarios

> sudo apt-get install -y dirmngr gnupg
> sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 561F9B9CAC40B2F7
> sudo apt-get install -y apt-transport-https ca-certificates

Agregamos el repositorio
> sudo sh -c 'echo deb https://oss-binaries.phusionpassenger.com/apt/passenger jessie main > /etc/apt/sources.list.d/passenger.list'
sudo apt-get update

Instalamos Passenger y nginx
>sudo apt-get install -y nginx-extras passenger
# paso 2

Habilitamos el módulo passenger y reniciamos nginx
Editamos /etc/nginx/nginx.conf y descomentamos  "include /etc/nginx/passenger.conf;". se debe ver de esta manera:
> \#include /etc/nginx/passenger.conf;
