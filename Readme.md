## CSS

### Introduction a CSS

1. Selector:  Define a que elemento le vamos a agregar estilos.

```css
h2 {
}
```

2. Propiedad: es la caracteristica de un elemento. Por ejemplo: color, size o margin.
```css
h2 {
  color:
}
```

3. Valor: es lo que define a la propiedad.

```css
h2 {
  color: red
}
```

* Estilos en Línea
```html
<h2 style="color: blue; border: 1 px solid red">Hello World!</h2>
```

* Uso de la Etiqueta `style`
```html
  <style>
    h2 {
      color: red
    }
  </style>

  <h2>Hello World!</h2>
```

* Uso de file `*.css`
```css
h2 {
  color: red;
  border: 1px solid black;
}
```


`index.html`
```html
  <head>
    <link rel="stylesheet" href="./style.css" />
  </head>
```

* Comentarios en CSS
```css
/*
  comments
*/
```

* Selectores
1. Selector de tipo etiqueta
`h2 {}`

2. Selector de tipo class
`.title {}`

3. Selector de tipo id
`#title {}`

4. Selector universal
`* {}`

* Selectores Combinadores
```html
<div class="primary">
  <div class="secondary">
    <h2 class="title">Inside 2H2</h2>
  </div>
  <h2 class="title">OutSide  1H2</h2>
</div>
```

1. Combinador de descendiente ( )space: realiza cambios en todas etiquetas que se encuentren dentro

```css
.primary .title {
  color: green;
  font-size: 50px;
}
```

<img src='./assets/combinator-desc.png' alt="combinator desc" />

2. Combinador de hijos directos (>):

```css
.primary > .title {
  color: green;
  font-size: 40px;
}
```

<img src='./assets/combinator-direct-child.png' alt="combinator-direct-child desc" />

### Herencia Cascada 
Define que estilo va a predominar en caso de haber mas de un selector que cambie los estilos de mas de un elemento. Los ultimos estilos sobreescribiran a los primeros.

```html
<h2 class="title">Hello Word!</h2>
```

```css
.title {
  color: red;
}

.title {
  color: green;
}
```
