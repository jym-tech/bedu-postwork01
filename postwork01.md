## Agregar la imagen de la página de matcha

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Aqui va la informacion importante pero no visible en el navegador -->
        <meta charset="utf-8">
        <title>
            Matcha WebPage
        </title>
        <!-- Aqui va el codigo de estilos, cuando no hay archivo CSS 
        <style>
            h1 {
                color: #025157;
            }
        </style>
        -->
        <!-- vinculo con archivo CSS -->
        <link rel="stylesheet" href="styles.css" type="text/css"> 

    </head>
    <body>
        <!-- Esto es lo que se vera en el navegador -->
        <h1> Build your blog. Build your bussiness. </h1>
        <p class="text-title">
            Instantly publish articles, drive more traffic, grow your email list, 
            and see your blog's impact on sales
        </p>
        <form>
            <input type="email" />
            <button class="btn-submit" type="submit">
                Try it now ⇒
            </button>
        </form>
        <p class="text-promo"> Start publishing today with a <strong>free 7-day trial.</strong> </p>
        <p class="text-info"> <strong>No credit card</strong> required. </p>
        <img class="img-capterra" src="https://ignos.blog/wp-content/uploads/2021/04/capterra.png" alt="capterra image" />
        <img class="img-matcha" src="https://getmatcha.com/wp-content/uploads/2019/09/intro_group_image.png" alt="matcha image"/>

    </body>
</html> 
```

```css
body {
    background-color: #fffbf7;
}

h1 {
    color: #46484c;
    text-align: center;
}

p {
    color: #8b8b8bcc;
    font-family: Verdana;
    font-size: 20px;
}

button {
    color: #fff;
    background-color: #025157;
}

img {
    display: block;
    margin-left: 15%;
    max-width: 70%;
}

.img-capterra{
    max-width: 40%;
    margin-left: 30%;
}
```

#### Ejecución

![ejecucion-imagen](/sitio01.png)

## Practica con CSS Dinner

![juego-imagen](/game01.png)

# CSS

## Uso de la propiedad `max-width`

La propiedad `max-width` se usa para definir cual será el valor máximo de un elemento.

Esto ayuda a que el valor usado en propiedad `width` sea mas grande que el indicado en `max-width`.

#### Ejemplo:

Se tiene un `div` anidado, pensemos que el `div `con `id` contenido1 es el "padre", tiene un `width` de 300px, el `div` con `id` contenido2 es el "hijo", tiene un `width` de 100%, con esta configuración le indicamos que los 300px del `div` padre los tiene el `div` hijo y solo se mostrara el `div` hijo por ser el que esta al interior, al indicar la propiedad `max-width` en 150 px, se muestran ambos `div`, primero el `div` hijo con 150px y luego el `div` padre con 150px, sumados ambos dan los 300px que tiene el `div` padre.

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Bedu-TEST</title>
    <link rel="stylesheet" href="styles.css" type="text/css">
  </head>
  <body>
    <div id="contenido1">
      <div id="contenido2">
        <h1>BEDU practica postwork</h1>
      </div>
    </div>
  </body>
</html>
```

```css
#contenido1 {
  background: blue;
  width: 300px;
}

#contenido2 {
  background: yellow;
  width: 100%;
  max-width: 150px;
}
```

## Uso de la propiedad `border`

Con la propiedad border podemos dar un estilo de línea para los cuatro lados que conforman un elemento.

#### Ejemplo:

Se contruye una tablade dos filas y dos columnas, donde se aplica un estilo de línea solida color rojo en el contorno y cada campo tiene un estilo de línea punteado color azul.

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Bedu-TEST</title>
    <link rel="stylesheet" href="styles.css" type="text/css">
  </head>
  <body>
   <!-- Uso de la propiedad border -->
    <table>
        <tr>
          <td>sesion01</td>
          <td>sesion02</td>
        </tr>
        <tr>
          <td>git y terminal</td>
          <td>html y css</td>
        </tr>
    </table>
  </body>
</html>
```

```css
/* Uso de la propiedad border */
table {
  border-width: 2px;
  border-style: solid;
  border-color: red;
}

tr, td {
  padding: 5px;
  border-width: 2px;
  border-style: dotted;
  border-color: blue;
}
```

# HTML

## Uso del elemento `section`

Nos ayuda a estructurar mejor un contenido, indicando a que parte de un esquema corresponde, al referirnos a un esquema, hablamos de un índice que son una serie de temas con subsecciones relacionadas.

La diferencia con el elemento `div` es que `section` es para especificar contenidos, englobando elementos que son de un mismo tema y `div` es un contenedor genérico. Por ejemplo en un blog, los comentarios pueden englobarse en una seccion.

#### Ejemplo:

Contruir un índice con los dos primeros temas del curso de BEDU, indicando cada tema dentro de un elemento section.

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Bedu-TEST</title>
    <link rel="stylesheet" href="styles.css" type="text/css">
  </head>
  <body>
    <!-- Uso de elemento section -->
    <section>
      <h1>Tema 1</h1>
      <p>Git y Terminal</p>
    </section>
    <section>
      <h1>Tema 2</h1>
      <p>HTML y CSS</p>
    </section>
  </body>
</html>
```

## Uso del elemento `figure`

El elemento `figure` identifica contenido que no depende de otro  contenido, es usado para referenciar imagenes, videos, parrafos, etc.

Lo anterior nos indica que es posible mover estos elementos sin afectar el documento base.

#### Ejemplo:

Crear un elemento `figure` con la imagen de BEDU, incorporando `figcaption` para indicar el título después de la imagen.

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Bedu-TEST</title>
    <link rel="stylesheet" href="styles.css" type="text/css">
  </head>
  <body>
    <!-- Uso de elemento figure -->
    <figure>
      <img src="https://app.bedu.org/assets/images/logo-bedu-black@3x.svg" alt="img-bedu">
      <figcaption> Bienvenidos al curso desarrollo web </figcaption>
    </figure>
    <p>En este curso aprenderemos mucho sobre GIT, HTML y CSS</p>
  </body>
</html>
```
