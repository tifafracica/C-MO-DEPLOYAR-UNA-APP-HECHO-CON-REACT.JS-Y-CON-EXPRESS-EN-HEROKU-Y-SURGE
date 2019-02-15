# COMO DEPLOYAR UN PROYECTO HECHO CON REACT.JS Y CON EXPRESS EN HEROKU Y SURGE.

## HEROKU CLI

ABRIR UNA CUENTA EN HEROKU

Instalar Heroku en tu computadora:

[descargar aqui](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)

## SURGE
[ABRIR UNA CUENTA EN SURGE](https://surge.sh/)

Instalar surge globalmente

`npm install --global surge`


### Se deploya en dos partes, el servidor (backend) y el cliente (frontend).

## DEPLOYAR EL BACKEND
* vayan a su carpeta donde tienen el backend y lo abren en la consola, después deben hacer lo siguiente:
`git init`

`git add .`

`git commit -m “zaraza”`

`heroku create`

`git push heroku master`

* aquí se genera una URL

## DEPLOYAR EL FRONTEND
* deben modificar la ruta URL de cada fetch que tienen sus componentes, con la nueva Ruta que les dió Heroku.

Ejemplo

así lo teníamos antes:
`fetch('https://localhost:3000/api/items/?q=' + name) y demás zaraza`    

así lo tenemos que colocar:
`fetch('https://enigmatic-inlet-77181.herokuapp.com/api/items/?q=' + name) y demás zaraza`
       
* en la carpeta del cliente, lo abrimos en la consola y escribir el siguiente comando npm run build (esto genera una carpeta build en su carpeta de cliente)
* en la carpeta build la abren por consola y escriben el comando surge ahí creamos el link que podrán usar! super chevere!
