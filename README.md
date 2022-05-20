# Practicando SASS

Hemos podido utilizar sus ventajas como:

- Nesting y & (anidamiento de selectores)
- @import (para importar estilos de otros archivos SASS)
- Variables (que se crean con \$) y operaciones
- @extend (extender propiedades de clases)
- @mixins (agregar css personalizadas) e @include
- Condicionales @if
- Bucle @each y maps

Una vez instalado Node, hacemos la instalación de SASS con el siguiente comando en la Terminal:

```
npm install -g sass
```

Creamos un ambiente de desarrollo con NPM (administrador de paquetes de Node) estando en nuestra carpeta root.

```
npm init
```

Se nos preguntaran varias cosas mediante la Terminal pero solo bastan con darle a Enter a todo. Una vez que finaliza se nos creará el archivo _package.json_ donde tenemos que agregar la siguiente línea dentro de la opción _script_.

```
"script": {
  "start": "sass style.scss ./css/style.min.css -w --no-source-map -s compressed"
}
```

"start" vendría siendo un alias del comando que le sigue a continuación.

- **sass**: nombre del paquete
- **style.scss**: archivo de entrada
- **./css/style.css**: archivo de salida (dentro de una carpeta llamada "css")
- **-w**: SASS estará observando los cambios en tiempo real (watching)
- **--no-source-map**: Evitar generar el archivo .map
- **-s compressed**: Indica que nuestro archivo de salida estará minificado

Para ejecutar SASS y que corra en segundo plano, escribimos en la Terminal el siguiente comando:

```
npm start
```
