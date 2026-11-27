# Laboratorio de Física

## Cómo abrirlo
1. Descomprime la carpeta completa.
2. Abre `index.html` en Chrome o Edge.
3. Selecciona el módulo desde los botones superiores.
4. Pulsa **Activar música** para escuchar el ambiente. Puedes silenciarlo y regular el volumen desde la misma página.

## Cómo añadir una simulación nueva
1. Crea una carpeta dentro de `modules/`. Ejemplo: `modules/ondas/`.
2. Dentro crea `index.html` con el HTML, CSS y JavaScript de la nueva simulación.
3. Abre `modules.js` y agrega una línea al arreglo `LAB_MODULES`, por ejemplo:

   `{ id: "ondas", name: "Ondas", entry: "modules/ondas/index.html" }`

4. Guarda los archivos y vuelve a cargar `index.html`.

No necesitas modificar el código de las simulaciones existentes ni la estructura de navegación. Cada módulo se abre dentro de un iframe independiente.

## Correcciones del péndulo
- El eje temporal de θ(t) usa valores numéricos reales, no etiquetas redondeadas a décimas.
- La gráfica temporal representa pares (tiempo, ángulo) en un eje X lineal.
- Reiniciar limpia también los datos visibles de las dos gráficas.
- Chart.js se redimensiona cuando cambia el tamaño de la ventana.

## Música
- El audio se genera en el navegador con Web Audio API.
- No se reproduce automáticamente: debes pulsar el botón.
- El navegador debe permitir sonido y no estar silenciado.
- El volumen se controla con el deslizador.
- No se reproduce una canción comercial ni se descarga un archivo de audio.

## Nota
Las librerías de diseño y gráficas se cargan desde CDN, por lo que necesitas conexión a internet para que se vean correctamente.
