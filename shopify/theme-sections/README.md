# Secciones del tema Shopify (tienda de ventiladores)

Copia versionada de las secciones personalizadas del tema **"Copia de Zendrop"** (tema en vivo / MAIN)
de la tienda Shopify. Estos archivos **no** forman parte del sitio de oposiciones; se guardan aquí
como respaldo y control de versiones del trabajo de la tienda.

## Cambio incluido en esta rama

**Problema:** al elegir un color del AirClip, la imagen del producto no cambiaba (se quedaba siempre
con la misma foto), lo que reducía la conversión.

**Solución (colores reales por variante):**

- `velta-airclip.liquid`
  - La galería ahora tiene una imagen principal con `id="heroImg"`.
  - Cada muestra de color (`col(...)`) recibe la URL de la foto real de esa variante y, al pulsarla,
    cambia `heroImg` a la foto real y salta a la primera diapositiva.
  - Fotos reales (CDN de la propia tienda):
    - White → `a47bdd814253aaeb3ae5f4439688.png`
    - Green → `d6bf6d57438c912c22197400f435.jpg`
    - Pink  → `6a7534e1482d8107a6a22c079bb1.jpg`

- `velta-miniturbo.liquid`
  - El selector del **AirClip de regalo** (al comprar 2 Mini Turbo) ahora muestra una miniatura con
    la foto real de cada color (White / Green / Pink) en vez de solo un emoji.

## Cómo desplegar al tema en vivo

Las herramientas automáticas no pueden escribir sobre el tema publicado (MAIN). Para aplicarlo:

1. Shopify admin → **Online Store → Themes → "Copia de Zendrop" → Edit code**.
2. Abrir `sections/velta-airclip.liquid` y `sections/velta-miniturbo.liquid`.
3. Sustituir el contenido por el de estos archivos (o aplicar los bloques cambiados).
4. Guardar. (Alternativa: duplicar el tema, aplicar y publicar la copia.)
