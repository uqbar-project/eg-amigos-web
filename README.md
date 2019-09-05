# Taller Maquetado Web

## Etapa 4: ¡Refactor de css!

En lugar de presentar los resultados como filas de una tabla, vamos a tratar de representar a cada persona con una tarjeta: el layout tiene que cambiar

- la foto podemos ubicarla a la izquierda
- a la derecha podemos poner: la persona con letra más grande, el apodo con un tamaño más pequeño y en gris, y un recuadro con la cantidad de años en los que nos conocemos.

Esto cambia a priori el html, porque la información será diferente y recordemos que html es un lenguaje que sirve para describir el contenido de una página.

Pero además, no queremos una tabla, la tarjeta debería ser lo suficientemente representativa...

Cambiamos el html a

```html
<section>
    <div class="tarjeta">
      <div class="foto">
        <img src="images/dodain.jpg" class="foto">
      </div>
      <div class="datos">
        <div class="titulo">Fernando Dodino</div>
        <div class="subtitulo">Dodain</div>
        <div class="badge">5</div>
      </div>
    </div>
    <div class="tarjeta">
      <div class="foto">
        <img src="images/jorgito.png" class="foto">
      </div>
      <div class="datos">
        <div class="titulo">Jorge Silva</div>
        <div class="subtitulo">Sorje</div>
        <div class="badge">6</div>
      </div>
    </div>
    <div class="tarjeta">
      <div class="foto">
        <img src="images/drB.jpg" class="foto">
      </div>
      <div class="datos">
        <div class="titulo">Pablo Beláustegui</div>
        <div class="subtitulo">Dr.B</div>
        <div class="badge">10</div>
      </div>
    </div>
  </section>
```

¿Y cómo se ve?

![inicial](extra/tarjeta.png)

Bueno, está mal pero no taaan mal.

## Cambiando el layout

Display flex nos puede ayudar a ordenar la tarjeta:

- primero necesitamos que la tarjeta tenga layout horizontal
- luego los datos deben tener un layout vertical
