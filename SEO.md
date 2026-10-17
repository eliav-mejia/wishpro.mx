# SEO — wishpro.mx

Guía de referencia: `builds/seo/seo-guide.pdf` (estructura HTML, meta etiquetas, H1–H3, nav + ul, alt de imágenes).
Este documento resume cómo se aplica en wishpro.mx. Actualizado 2026-10-16.

## Estrategia

Wishpro (México) vende cuidado personal con estándares profesionales. Cada estándar tiene su página, que responde a
una búsqueda concreta de quien compara productos.

| Página | Búsquedas objetivo |
|---|---|
| Portada `/` | Wishpro, cuidado profesional, fórmulas de laboratorio |
| `/productos/` | estándares de cuidado personal profesional |
| `/productos/envase-grado-medico.html` | envase de grado médico cosméticos |
| `/productos/principios-activos.html` | principios activos cuidado de la piel |
| `/productos/formulas-de-laboratorio.html` | fórmulas de laboratorio |
| `/productos/libre-de-parabenos.html` | productos sin parabenos México |
| `/productos/no-probado-en-animales.html` | cruelty free México |
| `/productos/dermatologicamente-probado.html` | dermatológicamente probado |

## Reglas para cada página

1. `<html lang="es-MX">`, `charset`, `viewport`.
2. `<title>` de **50–60 caracteres** (`<Tema> — Wishpro`) y descripción de **150–160**, únicos.
3. `<link rel="canonical">` absoluta `https://wishpro.mx/...`.
4. Open Graph + `twitter:card`.
5. JSON-LD en el `<head>`.
6. Un solo `<h1>`; `<h2>` por sección y `<h3>` en tarjetas (en `/productos/` hay un `<h2 class="sr-only">` antes de la cuadrícula).
7. Menú como `<nav>` + `<ul class="nav-links">`.
8. Enlaces internos limpios: `./`, `productos/`, `../`, `../#contacto` (nunca `index.html`).

## Etiquetas usadas

| Página | og:type | twitter:card | JSON-LD |
|---|---|---|---|
| Portada | website | summary | `Organization` (Wishpro México, email, país) + `WebSite` |
| `/productos/` y cada estándar | website | summary | `BreadcrumbList` |

Comunes: `og:site_name` = Wishpro, `og:locale` = es_MX. No hay `og:image` porque el sitio no tiene imágenes.

## Archivos de rastreo

- `robots.txt`: todo permitido; anuncia el sitemap.
- `sitemap.xml`: lista a mano (8 URLs). Añade cada página nueva.

## Pendiente

- Sin imágenes: añadir fotos de producto (WebP, con `alt` y `width`/`height`) y una imagen social de 1200 × 630 px
  para `og:image`, y cambiar `twitter:card` a `summary_large_image`.
- Cuando haya productos concretos con precio, añadir JSON-LD `Product` en sus páginas.
- La carpeta no es un repositorio git todavía.
