# M.plugin.Magnify

Plugin que permite realizar un efecto de zoom o de lupa sobre una o varias capas

![Imagen1](./img/imagenPlugin.png)

# Dependencias

- magnify.ol.min.js
- magnify.ol.min.css


```html
 <link href="../../plugins/magnify/magnify.ol.min.css" rel="stylesheet" />
 <script type="text/javascript" src="../../plugins/magnify/magnify.ol.min.js"></script>
```

# Parámetros

- El constructor se inicializa con un JSON de options con los siguientes atributos:

- **layers**. String que contiene el nombre de las capas que se quieren seleccionar del mapa. A estas capas se les aplicará el filtro de lupa. Si este campo está vacío, el efecto lupa se aplicará a todas las capas.

- **position**. Indica la posición donde se mostrará el plugin.
  - 'TL':top left
  - 'TR':top right (default)
  - 'BL':bottom left
  - 'BR':bottom right

- **zoom**. campo numérico que define el zoom inicial.

- **zoomMax**. campo numérico que define el nivel maximo de zoom.

# Eventos

# Otros métodos

# Ejemplos de uso

```javascript
   const map = M.map({
     container: 'map'
   });

   const mp = new M.plugin.Magnify({
        layers: '',
        postition: 'TL',
      });

   map.addPlugin(mp);
```

```javascript
const mp = new Magnify({
  layers: 'provincias,fondo,Sevilla',
  zoom: 3,
  zoomMax: 20
});

map.addPlugin(mp);
```

```javascript
const mp = new Magnify({});

map.addPlugin(mp);
```
