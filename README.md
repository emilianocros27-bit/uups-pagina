# Página UUPS! (estructura tipo nike.com/mx)

Abre `index.html` en el navegador. Necesita internet solo para cargar las tipografías (Saira, Space Mono y el respaldo de títulos).

## Qué se replicó
La estructura, medidas, colores y comportamiento del home de nike.com/mx: barra superior, header fijo, hero a sangre con titular condensado, carrusel de productos, segundo hero, mosaico de dos columnas, sección de categorías y footer. El código está escrito desde cero (HTML + CSS + JS en un solo archivo).

## Qué se reemplazó
- **Logo:** no hay ninguno. El hueco está en `.logo-slot` (arriba a la izquierda) para cuando tengas el tuyo.
- **Fotos:** las 5 de esta carpeta, recortadas en `assets/`.
- **Tipografías:** Schoolbully para títulos y nombre de marca (archivo en `assets/schoolbully.ttf`; mientras no esté, se usa Patrick Hand SC) Saira para el texto y Space Mono para precios y el cupón de promoción.
- **Iconos:** Lucide Animated (21st.dev, licencia MIT): carrito y flechas, con su animación al pasar el cursor.
- **Textos, productos y precios:** propios ($150 MXN el par).

## Qué quedó fuera
Buscador, menús desplegables, cuenta, favoritos y pago. La bolsa solo cuenta pares en pantalla; el cobro real va en Shopify.

## Antes de publicar
Las fotos de producto parecen ser del proveedor: confirma que puedes usarlas o cámbialas por fotos tuyas.

## Publicación
Se sirve en Cloudflare Workers (`uups.emicros.workers.dev`): el Worker `uups` toma los archivos de este repositorio (rama `main`) y los entrega con su tipo de contenido. Para actualizar la página basta con subir cambios a `main`; Cloudflare los cachea unos minutos.
