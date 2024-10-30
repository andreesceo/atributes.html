# Atributos en HTML

## `accesskey="(shortkey)"`
Permite asignar un atajo de tecla que activa el elemento como si se tratase de una acción `onclick`.

## `autofocus`
Indica que un input debe tener el foco de atención desde el momento en que se carga la página web.

## `contenteditable="true"`
Indica que un texto es editable por el usuario.

## `data-*`
Crea pseudoelementos nacientes del elemento actual para uso variable posterior en CSS.

## `dir="ltr/rtl"`
Posiciona el texto a la izquierda (ltr) o a la derecha (rtl) según la estructura cultural del idioma en el que se desea construir la página web o para simple decoración justificada.

## `draggable="true/false"`
Especifica si un elemento puede ser arrastrable fuera de la página web como archivo.

## `enterkeyhint="(word)"`
Asigna una palabra clave que se visualiza en el teclado virtual del usuario, es decir, para teclados virtuales.

## `inert`
Desactiva cualquier tipo de interacción con el elemento, como foco, clics, seleccionamiento, arrastre, etc. Importante mencionar que `inert` no reemplaza el seleccionamiento de textos como lo hace la propiedad CSS `user-select: none`.

## `input-mode=""`
El atributo `inputmode` sugiere el tipo de teclado virtual que el navegador debería mostrar cuando un usuario está editando el contenido. Se utiliza principalmente en elementos `<input>`, pero también puede aplicarse en cualquier elemento que sea `contenteditable`.

### Ejemplo de uso de `inputmode`
```html
<form>
  <!-- Entrada de texto estándar -->
  <label for="text-input">Texto:</label>
  <input id="text-input" type="text" inputmode="text"><br>

  <!-- Entrada numérica decimal -->
  <label for="decimal-input">Decimal:</label>
  <input id="decimal-input" type="text" inputmode="decimal"><br>

  <!-- Entrada numérica -->
  <label for="numeric-input">Numérico:</label>
  <input id="numeric-input" type="text" inputmode="numeric"><br>

  <!-- Entrada telefónica -->
  <label for="tel-input">Teléfono:</label>
  <input id="tel-input" type="tel" inputmode="tel"><br>

  <!-- Entrada de búsqueda -->
  <label for="search-input">Buscar:</label>
  <input id="search-input" type="search" inputmode="search"><br>

  <!-- Entrada de correo electrónico -->
  <label for="email-input">Correo:</label>
  <input id="email-input" type="email" inputmode="email"><br>

  <!-- Entrada de URL -->
  <label for="url-input">URL:</label>
  <input id="url-input" type="url" inputmode="url"><br>
</form>
```

## `itemid`
El atributo `itemid` y los microdatos en general ayudan a los motores de búsqueda a entender mejor tu contenido. También son útiles internamente para correlacionar datos en bases de datos o sistemas de búsqueda.

### Ejemplo de uso de `itemid`
```html
<!-- Producto principal -->
<div itemscope itemtype="https://schema.org/Product" itemid="urn:product:12345">
  <h2 itemprop="name">Cámara Fotográfica</h2>
  <p itemprop="description">Cámara fotográfica digital con zoom óptico de 10x y grabación de video en alta definición.</p>
  <img src="camera.jpg" itemprop="image" alt="Cámara Fotográfica" />
  <p itemprop="offers" itemscope itemtype="https://schema.org/Offer">
    Precio: <span itemprop="price">$499.99</span>
  </p>
</div>
```

## `title`
Proporciona información adicional sobre un elemento cuando el usuario coloca el cursor sobre él (hover). Mejora la accesibilidad y la experiencia del usuario.

### Ejemplo práctico
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Atributo Title</title>
</head>
<body>
  <p title="Este es un párrafo con una descripción adicional.">Pasa el ratón sobre este texto para ver el título.</p>
  <a href="https://www.ejemplo.com" title="Visita Ejemplo.com">Visita Ejemplo.com</a>
</body>
</html>
```

### Explicación
- **Párrafo con title**: El texto "Pasa el ratón sobre este texto para ver el título" muestra un tooltip con la descripción "Este es un párrafo con una descripción adicional" al pasar el cursor.
- **Enlace con title**: El texto "Visita Ejemplo.com" muestra un tooltip con "Visita Ejemplo.com" al pasar el cursor sobre el enlace.

## `translate`
Permite controlar si un contenido debe ser traducido por herramientas de traducción.

### Ejemplo práctico
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Receta de Tacos al Pastor</title>
</head>
<body>
  <!-- Este texto puede ser traducido -->
  <h1 translate="yes">Receta Tradicional</h1>

  <!-- Este texto no debe ser traducido -->
  <h2 translate="no">Tacos al Pastor</h2>

  <!-- El resto del contenido puede ser traducido -->
  <p translate="yes">Descubre cómo preparar los auténticos tacos al pastor con nuestra receta paso a paso.</p>
</body>
</html>
```

### Explicación
- **translate="yes"**: Los textos estarán disponibles para ser traducidos.
- **translate="no"**: El nombre del plato "Tacos al Pastor" se mantendrá sin traducir.
