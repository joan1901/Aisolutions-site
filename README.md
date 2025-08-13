# AI Solutions — Sitio estático (sin build)

> Mono-página **lista para publicar** con Tailwind CDN. Idioma: español (España).

## Estructura
```
/index.html
/logo.png                  # placeholder — reemplazar por el logo real
/panel.mp4                 # placeholder — reemplazar por el vídeo real
/favicon.svg
/og-cover.svg              # 1200x630 (Open Graph)
/robots.txt
/sitemap.xml
/images/proyecto-1.svg
/images/proyecto-2.svg
/images/proyecto-3.svg
/README.md
```

## Reemplazos rápidos
- **logo.png** → Pon tu logo en `/logo.png` (ideal ≥ 512×512). El HTML tiene comentarios indicando el punto de reemplazo.
- **panel.mp4** → Sustituye `/panel.mp4` por tu demo (ideal H.264 + AAC, ≤ 4–8MB). El hero usa `autoplay muted loop` + fallback de click con sonido.

## Deploy
- Sube la carpeta tal cual a tu hosting/Netlify/Vercel/Nginx/Apache.
- Asegúrate de servir `text/xml` para `sitemap.xml` y `text/plain` para `robots.txt`.
- Si publicas en `https://a-i-solutions.org/`, los metadatos ya están listos (canonical, OG/Twitter). Si no, edita URL en `<head>` y `sitemap.xml`.

## QA / Criterios de aceptación
- **Lighthouse** escritorio: Performance/SEO/Best Practices/Accessibility ≥ 90.
- **Sin build**: Tailwind via CDN.
- **Formulario** (FormSubmit) envía a `Contacto@a-i-solutions.org` y redirige a `index.html?sent=1#contacto` mostrando el aviso.
- **Imágenes**: todos los SVG cargan; los 3 de Proyectos usan gradiente brand1→brand2.
- **SEO/JSON-LD**: válidos (prueba en Rich Results Test).
- **Robots/Sitemap**: accesibles desde raíz. `sitemap.xml` → `<lastmod>2025-08-13</lastmod>`.

## Notas de accesibilidad
- `alt` descriptivos, contraste alto sobre fondo oscuro.
- Estructura semántica: un `h1`, subsecciones con `h2`.
- Botón overlay con `aria-label` para reproducir vídeo con sonido.

## Créditos
- Tipografía **Inter** (Google Fonts, `display=swap`).
- Fondo con **mesh** (radiales suaves) basado en la paleta.
