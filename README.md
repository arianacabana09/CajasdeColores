# Cuadros de colores con funciones de Sass

> PASOS A SEGUIR
* Crea en un archivo html 6 divs, cada uno con id diferente.
```html
<body>
  <div id="uno"></div>
  <div id="dos"></div>
  <div id="tres"></div>
  <div id="cuatro"></div>
  <div id="cinco"></div>
  <div id="seis"></div>
</body>
```
* Crea la estructura correspondiente de **src** y dentro del archivo **main.scss** crea la variable para almacenar un color base
```scss
$color-base: red;
```

* En una clase declara atributos para los cuadros y aplícalo como un **@extend**
```scss
.cuadro{
  height: 100px;
  float: left;
  width: 15%;
  margin: 1px;
}

#uno, #dos, #tres, #cuatro, #cinco, #seis {
  @extend .cuadro;
}
```

* En cada id prueba algunas funciones de colores de sass
```scss
#uno{
  background-color: $color-base;
}
#dos{
  background-color: lighten($color-base, 10%);
}
#tres{
  background-color: darken($color-base, 10%);
}
#cuatro{
  background-color: desaturate($color-base, 80%);
}
#cinco{
  background-color: complement($color-base);
}
#seis{
  background-color: invert($color-base);
}
```

> El resultado en el archivo **main.css** sera:
* Código compilado
```scss
.cuadro, #uno, #dos, #tres, #cuatro, #cinco, #seis {
  height: 100px;
  float: left;
  width: 15%;
  margin: 1px;
}

#uno {background-color: red; }
#dos {background-color:#f33; }
#tres {background-color:#c00; }
#cuatro {background-color:#966; }
#cinco {background-color:cyan; }
#seis {background-color:cyan; }
```


> DEMO
[Cuadro de Colores](https://arianacabana09.github.io/CajasdeColores/)
