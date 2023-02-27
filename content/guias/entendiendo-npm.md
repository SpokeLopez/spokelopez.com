+++
title = "Entendiendo NPM de Node.js"
description = "Instalación de npm e incializando un proyecto con npm"
tags = [
    "javascript",
    "npm",
]
date = "2023-02-08"
categories = [
    "Frontend",
    "Desarrollo",
]
menu = "main"
+++
## NPM (Node Package Manager)

En al día a día como frontend, es normal encontrarte con proyectos que funcionen con la ayuda de dependencias en **NPM**, es esto lo que me ah llevado a tener una lista de comandos que les quiero compartir en un futuro post, pero antes me gustaría dejarte una introducción de lo que es **NPM** este post.

**NPM** es un gestor de paquetes creado en lenguaje **javascript** y es de las partes mas importantes de **Node.js**, gracias a el se obtiene cualquier libreria a traves de código.

## Las principales ventajas

Las ventajas que eh encontrado al utilizar **NPM** en un proyecto son:

    1. Adaptar los paquetes según la necesidad el proyecto
    2. La descarga de las herramientas es inmediata
    3. Poder ejecutar distintas versiones del mismo paquete en el mismo proyecto
    4. Restringir actualizaciones de las versiones del paquete o incluso restringirlos para producción o desarrollo

## ¿Como instalar npm en tu equipo?

Para empezar debes instalar **Nodejs** en tu equipo accediendo al [sitio web ](https://nodejs.org/es/)y descargando **Node.js**. Al terminar la instalación, se revisa que todo este ok, para esto abrimos la *cmd* de **Windows** o la terminal de **Linux** / **Mac** y escribes el siguiente comando:

```shell
node --version
```

Como resultado obtendrás la version instalada en tu equipo, por ejemplo:

```shell
v18.12.1
```

E igualmente al instalar **Node.js** viene incluido **NPM**, asi que ahora escribimos el mismo comando pero con npm:

```shell
npm --version
```

Como resultado obtendrás igualmente la version instalada en tu equipo, por ejemplo:

```shell
9.4.1
```

Y asi, finalmente tienes instalado **Node** y **NPM** en tu equipo.

## Inicializando tu proyecto con NPM

Para inicializar tu proyecto con **NPM** es necesario estar en una carpeta desde la terminal, en mi caso tengo la carpeta curso-npm y procedemos a ejecutar el comando:

```shell
npm init
```

Ahora tendrás que hacer una serie de configuraciones para tu proyecto, empezando por el nombre:

```shell
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (curso-npm)
```

Puedes definir un nuevo nombre o directamente dar enter y seguira el nombre de nuestra carpeta. Inmediatamente nos pedirá mas configuraciones, igualmente que con el paso anterior puedes dar solo enter para continuar, procedere a explicártelas a continuacion:

```shell
Press ^C at any time to quit.
package name: (curso-npm)
version: (1.0.0)
description: Proyecto de prueba para entrada en el blog
entry point: (index.js)
test command:
git repository:
keywords:
author: spokelopez
license: (ISC)
```

Por ahora todas las configuraciones del proyecto no tienen mucha relevancia para el post ya que el mismo nombre nos dice a que se refieren, incluso puedes saltar estas configuraciones con el comando:

```shell
npm init -y
```

Y tendrás el mismo resultado, lo que logras con esta configuración es generar el archivo *package.json* para nuestro proyecto.

Como información extra, si quieres tener una información detallada sobre las configuraciones anteriores puedes ejecutar en tu terminal o cmd:

```shell
npm help init
```
## Fichero package.json

Este fichero tendrá toda la información de las dependencias de tu proyecto, es un simple fichero de texto en formato *json*, en este existen diferentes campos que veremos a continuación:



```shell
{
  "name": "curso-npm",
  "version": "1.0.0",
  "description": "Proyecto de prueba para entrada en el blog",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "spokelopez",
  "license": "ISC"
}
```

- *name* : Nombre del proyecto, librería o paquete. Es recomendable que coincida con el repositorio
- *version* : Versión del proyecto o del paquete
- *description* : Descripción breve del proyecto o paquete
- *main* : Punto de entrada del proyecto. Suele ser `index.js` (en node) o `index.html` (en browser)
- *scripts* : scripts del proyecto, para distintos fines
- *author* : Nombre del autor del proyecto o paquete
- *license* : Tipo de licencia del proyecto o paquete, por defecto es **ISC**

El siguiente post incluirá la lista de comandos que me han ayudado en el día a día y un pequeño ejemplo de un proyecto utilizando dependencias.