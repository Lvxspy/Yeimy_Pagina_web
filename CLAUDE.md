# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the site

This is a static HTML/CSS site with no build step. Open `Yeimy rose/index.html` directly in a browser, or serve it with any static server:

```bash
python3 -m http.server 8080 --directory "Yeimy rose"
# then open http://localhost:8080/index.html
```

## Architecture

All site files live under `Yeimy rose/`:

- `index.html` — main portfolio page (hero, about, gallery grid, techniques, Instagram CTA, footer). Full HTML document linking to `css/index.css`.
- `detalle_obra.html` … `detalle_obra6.html` — one detail page per artwork. Full HTML documents linking to `css/estilos.css`.
- `css/index.css` — all styles for the main portfolio page.
- `css/estilos.css` — shared styles used by all detail pages (reset, typography, layout, `.btn-back`, footer).
- `imagenes/` — artwork photos (`obras.jpg`, `obras 2.jpg` … `obras 6.jpg`).

### Color palette

| Role | Value |
|---|---|
| Background warm white | `#fdf8f2` |
| Primary text dark brown | `#2a1f1a` |
| Accent orange-red | `#e76f51` |
| Secondary orange | `#f4a261` |
| Teal accent | `#2a9d8f` |
| Yellow accent | `#e9c46a` |
| Body text muted brown | `#5a4035` |

### Fonts

Google Fonts: `Playfair Display` (headings/titles, serif) and `Lato` (body, sans-serif).

### Navigation

Gallery items in `index.html` link to individual detail pages by filename (`detalle_obra.html`, `detalle_obra2.html`, …). Detail pages link back with `<a href="index.html">`.
