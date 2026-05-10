# Viruland

Sitio web de **Viruland** — tejidos a crochet únicos e irrepetibles, hechos a mano en Buenos Aires, Argentina.

## Stack

- HTML5 + CSS3 + JavaScript vanilla — sin frameworks, sin dependencias
- Google Fonts: Cormorant Garamond · Cinzel Decorative · Jost
- Deploy: GitHub Pages (u hosting estático)

## Estructura

```
viruland/
│
├── index.html                  # Catálogo principal (cardigans, carteras, sobre mí, contacto)
├── style.css                   # Estilos globales compartidos por todas las páginas
│
├── cardigan-xxl-liviano.html   # Páginas de detalle de producto
├── cardigan-xxl-invierno.html
├── cardigan-l-negro.html
├── cardigan-l-pasteles.html
├── cardigan-l-amanecer.html
├── volero-sm.html
├── poncho-xl.html
│
├── fotos/                      # Media: fotos (.jpg/.jpeg) y videos (.mp4)
│
├── .gitignore
└── README.md
```

## Funcionalidades

- **Catálogo con videos** — cada producto tiene un video que muestra el frame del medio, pausado. El usuario lo reproduce manualmente.
- **Páginas de producto individuales** — carrusel de media mixta (foto + video), acordeón de información, lightbox de pantalla completa.
- **Lazy loading** — los videos usan `preload="metadata"` y solo se cargan completamente cuando el usuario los reproduce.
- **Intersection Observer** — los videos se pausan al salir del viewport.
- **Tags de stock** — "En stock" / "A pedido" visible en catálogo y en cada página.
- **Responsive** — mobile-first, grid adaptable.
- **WCAG 2.2 AA** — contraste de colores verificado.

## Correr localmente

No requiere servidor ni instalación. Abrí `index.html` directamente en el browser.

```bash
# O con cualquier servidor estático, por ejemplo:
npx serve .
python -m http.server 8000
```

## Deploy en GitHub Pages

1. Subir el repo a GitHub
2. Settings → Pages → Source: `main` branch, carpeta `/` (root)
3. El sitio queda disponible en `https://<usuario>.github.io/<repo>/`

> Los videos pesados en `fotos/` pueden ralentizar el clone. Considerá usar Git LFS para los `.mp4` si el repo crece mucho.

## Contacto

[viruland.com.ar](https://viruland.com.ar) · WhatsApp: +54 9 11 7239-1267
