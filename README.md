# Sitio RAYO INCC

Plantilla HTML personalizada para la marca RAYO INCC. Incluye homepage, catálogo, páginas de servicios, eventos y contacto adaptadas al estilo de la marca.

## Ejecutar en local

1. Clona este repositorio y abre la carpeta del proyecto.
2. Sirve los archivos con un servidor estático (por ejemplo `npx serve`, `python -m http.server` o la extensión Live Server de VSCode).
3. Abre `http://localhost:3000` (o el puerto indicado) y navega por los archivos `.html`.

## Actualizar colores corporativos

La paleta principal está declarada en dos ubicaciones para mantener compatibilidad con CSS y SCSS:

- `assets/scss/_variables.scss`: variables Sass `$color-primary` y `$color-secondary`.
- `assets/css/style.css`: variables CSS `--color-primary` y `--color-secondary`, además de referencias en botones y enlaces.

Cambia los valores hexadecimales en ambos archivos, guarda y vuelve a cargar el sitio. Si utilizas un pipeline Sass, recompila los estilos para que `style.css` herede los nuevos valores.

## Agregar o editar productos en la tienda

1. Duplica un bloque de producto dentro de `shop.html` y actualiza el nombre, precio y descripción.
2. Sube la imagen correspondiente a `assets/img/product/` y referencia el archivo en el `img` del producto.
3. Repite la referencia del producto en otras páginas si deseas destacarlo (por ejemplo en `index.html` o secciones destacadas).
4. Asegúrate de mantener textos y precios en bolívares o dólares según la estrategia comercial.

## Mantener la página de eventos

- La lista de eventos se encuentra en `eventos.html`. Edita los elementos del listado y las tarjetas para agregar nuevas fechas o modificar información.
- Actualiza las fotografías de la sección reemplazando los comentarios `<!-- Reemplazar ... -->` con imágenes propias en `assets/img/...`.
- Ajusta el formulario de sugerencias si necesitas recopilar nuevos datos (campos adicionales, opciones de selección, etc.).

## Información de contacto

- La página `contact.html` concentra los botones hacia WhatsApp e Instagram y el formulario de contacto. Actualiza los enlaces y los textos desde ese archivo cuando cambien los datos.
- Los datos de contacto del pie de página se repiten en varias páginas; edítalos directamente en cada archivo o centralízalos usando los fragmentos de `includes/` si decides integrarlos con un motor de plantillas.

## Publicar cambios

1. Verifica tus modificaciones en local y ejecuta los chequeos necesarios.
2. Crea un commit descriptivo y súbelo a tu repositorio remoto (`git add`, `git commit`, `git push`).
3. Si publicas con GitHub Pages o un hosting estático, apunta la raíz del sitio a esta carpeta y vuelve a desplegar.
4. Para servidores propios, sube el contenido de la carpeta al hosting o sincroniza mediante FTP/rsync.

## Recursos adicionales

- Logo de la marca: `assets/img/logo/logo-1.png`.
- Fragmentos reutilizables (head, navbar y footer) en `includes/` para integraciones con motores de plantillas.
