# Página personal de Mariano Rojas

Blog, CV e investigación. Construido con Jekyll; los posts pueden escribirse como notebooks de Jupyter (`_notebooks/`) o en Markdown (`_posts/`).

Basado en [grey-area/fastpages-website](https://github.com/grey-area/fastpages-website), derivado a su vez de [fastpages](https://github.com/fastai/fastpages). El código está bajo la licencia Apache 2.0 (ver `LICENSE`); el contenido (posts, CV, PDFs) es de Mariano Rojas.

## Escribir un post

- **Notebook:** `_notebooks/AAAA-MM-DD-titulo.ipynb`. La primera celda markdown es el encabezado (ver `_templates/` y `_action_files/README.md`).
- **Markdown:** `_posts/AAAA-MM-DD-titulo.md` con front matter de Jekyll (`layout: post`, `title`, `description`, `categories`).

`image:` en el encabezado necesita la barra inicial: `/images/blog_posts/x.png`.

Al hacer push a `master`, el workflow `.github/workflows/ci.yaml` convierte los notebooks, construye el sitio y lo publica en la rama `gh-pages`.

## Ver en local

```
make server   # http://localhost:4000 (requiere Docker)
make stop
```

## Archivos clave

| ruta | qué es |
|---|---|
| `_config.yml` | título, usuario, URL, menú y redes |
| `_pages/about.md` | página "Sobre mí" |
| `_pages/publications.html` | investigación |
| `misc/cv.pdf` | el CV que muestra la página CV |
| `images/foto.jpg` | foto del About |
| `_sass/minima/custom-styles.scss` | colores, tipografía y diseño |
