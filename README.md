# HTML5

HTML es el lenguaje de marcado que define el contenido que se ve a través del navegador web.

## Software recomendados
- Navegador web: Google Chrome Mozilla Firefox
- Editor de código: Atom, Sublime Text, Visual Studio Code, VIM

## Configuración inicial para crear un HTML
- Crear un nuevo archivo llamado index.html en la ruta principal

  ```html
  index.html
  ```

  Para definir una estructura inicial de HTML, se debe hacer de la siguiente manera

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
   Contenido
  </body>
  </html>
  ```
  Esa es la estructura básica, pero se puede usar "Emmet Abbreviation" para iniciar la estructura de HTML más rápido

  ```html
  ! (para la estructura básica) 
  ```

  ## Acerca de Emmet Abbreviation
  Es una abreviación que se usa para HTML y CSS, esto con el fin de estructurar el HTML mucho más rápido y de una forma dinámica

  ```html
  ul#menu>li.items*4>a{Objetos $}
  ```

  De esta forma estoy indicando que quiero crear una etiqueta "ul" y quiero asignarle un "id" llamado menu, usando ">" estoy diciendo que dentro del "ul" quiero crear una etiqueta tipo "li" y asignarle una clase llamada "items", uso * 4, para indicar que quiero crear 4 elementos de etiqueta "li" con una clase llamada "items" luego uso ">" para indicar que en cada una de la lista, crear una etiqueta de "a" y usando "{Items $}" estoy indicando que dentro de la etiqueta "a", quiero que su contenido diga "Items" y como son varias listas, agregará un número por cada lista. Ejemplo: Lista 1, Lista 2, Lista 3 y Lista 4.

  ```html
  <ul id="menu">
        <li class="items"><a href="">Items 1</a></li>
        <li class="items"><a href="">Items 2</a></li>
        <li class="items"><a href="">Items 3</a></li>
        <li class="items"><a href="">Items 4</a></li>
    </ul>
  ```

  - Para aprender más acerca de la "Abreviación Emmet" mirar este recurso: https://emmet.io/
  - Para saber y aprender los atajos de Visual Studio Code en Windows, ver el siguiente recurso: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
  - Para el caso de Mac, mirar el siguiente recurso: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
  - Para el caso de Linux, mirar el siguiente recurso: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf

  - Documentación de HTML de Mozilla: https://developer.mozilla.org/en-US/docs/Web/HTML
  - Documentación para las etiquetas de HTML y sus atributos: https://htmlreference.io/

## Etiquetas (Abre y cierre)
Las etiquetas dentro del HTML, es algo que se va a estar usando la mayoría del tiempo, ya que con estas es que definimos el cuerpo del HTML, existen muchas etiquetas de HTML, dentro de la sección de recursos, se encuentra un enlace para la documentación de las etiquetas de HTML.

```html
<> (Etiqueta que indica para abrir)
```
```html
</> (Etiqueta que indica para cerrar)
```

No todas las etiquetas tienen abrir y cerrar, hay algunas que siki son de abrir, como las etiquetas tipo meta, entre otras.

```html
<meta>
```

### Como se estructura un HTML y sus partes
Debemos comenzar con la cabezera, es decir, desde la etiqueta head

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

En la etiqueta "head", va toda la parte de enlaces externos, como etiquetas "link", estas contienen en algunos casos, fuentes, íconos, favicon.
Cualquier enlace externo, irá en la parte del "head"

```html
<body>

</body>
```

Dentro de la etiqueta "body", se encuentra todo el contenido, estructura y maquetado de una página, esto lo hace la etiqueta principal de cada sitio.

```html
<html lang='es'>
</html>
```

Podemos observar que todo está envuelto por la etiqueta "html", vemos que esta por defecto se le agrega un atriburto llamado "lang" Language: el cual es el idioma que toma como base la página.

### Como puedo importar scripts

Para import scripts dentro del html, debemos ubicarnos al final de la etiqueta "body", de esta manera

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

Vemos que debajo de la etiqueta de cierre del "body", está la etiqueta de cierre de "html", ahí debemos enlazar los archivos de los scripts, y lo hacemos de la siguiente manera.

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
<script type="module" src="/main.js"></script>
</html>
```

Al igual que todas las etiquetas, la etiqueta "script" tiene sus propios atributos, verificar la documentación.

Así como importamos un script, podemos escribir código JavaScript, dentro de la etiqueta "script".

```html
<script>
    const a = 4
    const b = 4

    const aux = a + b

    window.alert(`El resultado de las 2 variables es: ${aux}`)
</script>
```