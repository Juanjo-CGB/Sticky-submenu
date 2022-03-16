# Sticky submenú

Fijar un elemento mediante posicionamiento 'sticky' cuando no es descendiente directo del contenedor

## Descripción

El posicionamiento sticky puede considerarse un híbrido de los posicionamientos relativo y fijo. Un elemento con posicionamiento sticky es tratado como un elemento posicionado relativamente hasta que cruza un umbral especificado, en cuyo punto se trata como fijo hasta que alcanza el límite de su padre. 

En el siguiente ejemplo...

```css
.sticky { 
    position: sticky; 
    top: 0; 
}
```

...se posicionaría el elemento con la clase `sticky` relativamente hasta que el viewport sea desplazado de tal manera que ese elemento esté a 0 píxeles del borde superior del elemento contenedor. Cuando se supere ese umbral, el elemento se fijaría a 0 píxeles de ese elemento contenedor y permanecerá adherido (sticky) a todo lo largo de la altura de su padre.

**Pero, ¿qué pasaría si quisiéramos fijar un elemento con posicionamiento sticky a un ancestro que no fuera el contenedor padre?**

Veamos el siguiente ejemplo...

```html
<body>
    <header>
        <div class="publicidad">
            ...
        </div>
        <nav class="nav">
            <ul class="nav__menu">
                <li class="nav__menu-link">...</li>
                <li class="nav__menu-link">...</li>
                <li class="nav__menu-link">...</li>
            </ul>
        </nav>        
    </header>
<body>
```

...en el que queremos fijar el menú de navegación con la clase `nav` a lo largo de toda la página, es decir, a lo largo de la altura del `body`. Como hemos visto anteriormente, el elemento con este tipo de posicionamiento se fijaría únicamente a lo largo de la altura del padre, en nuestro caso del `header` y eso no es exactamente lo que deseamos. Una posible solución sería aplicar la clase `sticky` al `header` en lugar de al elemento `nav` para que el menú se fijara a lo largo de toda la página. Pero en este caso estaríamos fijando en la parte superior todo el contenido del `header`, es decir, el elemento con la clase `publicidad` también quedaría fijado, y eso tampoco es exactamente lo que deseamos.

**Pero entonces, ¿cómo podemos solucionar este problema?**

En este repositorio encontrarás una alternativa para poder solventar el inconveniente planteado.


## Construido con

**Javascript:** Interactividad

**HTML:** Estructura

**CSS:** Estilos

## Documentación

[Documentación](https://juanjo-cgb.github.io/Sticky-submenu/)


