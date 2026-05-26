# ZonaG Fitness — Landing Page

Sitio estático listo para desplegar en Vercel.

## Estructura

```
zonag-fitness/
├── index.html         Página completa (HTML + CSS + JS)
├── favicon.ico        Favicon multi-tamaño (símbolo G)
├── fonts/             Tipografía de marca self-hosted
│   └── haboro-condensed-extrabold.woff2   (HYROX, subset Latín+ES)
├── images/            Fotos y logos referenciados desde index.html
│   ├── crossfit.png
│   ├── delso.png
│   ├── hyrox.png
│   ├── hyrox2.png
│   ├── luis_fer.png
│   ├── logo-zonag-morado.png
│   └── logo-zonag-neon.png
├── icons/             Favicons en distintos tamaños (PNG)
│   ├── favicon-16.png
│   ├── favicon-32.png
│   ├── favicon-48.png
│   ├── favicon-192.png
│   ├── favicon-512.png
│   └── apple-touch-icon.png
└── README.md
```

## Despliegue en Vercel

Tres caminos posibles, según prefieras:

### Opción A — Drag & drop (más rápido)

1. Entra a https://vercel.com/new
2. Arrastra la carpeta `zonag-fitness/` al área de drop
3. Vercel detecta que es un sitio estático y publica. No necesita configuración.

### Opción B — Git (recomendado para iterar)

1. Subir esta carpeta a un repo de GitHub/GitLab
2. En Vercel: New Project → Importar el repo
3. Framework preset: **Other** (sitio estático puro)
4. Build command: dejar vacío
5. Output directory: dejar vacío (la raíz)
6. Deploy

### Opción C — Vercel CLI

```bash
cd zonag-fitness
npx vercel
```

Sigue las instrucciones (login, nombre del proyecto, scope). En "framework preset" elige `Other`.

## Editar contenido sin tocar HTML

Casi todo el copy vive en una sola constante `CONFIG` dentro de `index.html`
(la encuentras buscando `CONFIG = {`). Para cambiar precios, textos, links de
WhatsApp, horarios o coaches, edita ese objeto.

## Cambiar fotos

1. Reemplaza el archivo en `images/` manteniendo el mismo nombre, **o**
2. Edita las constantes al inicio del `<script>`:
   ```js
   const PHOTO_HERO         = './images/luis_fer.png';
   const PHOTO_HYROX_GYM    = './images/hyrox2.png';
   const PHOTO_COACH_LUISFER = './images/luis_fer.png';
   const PHOTO_COACH_DELSO  = './images/delso.png';
   const PHOTO_WOD          = './images/crossfit.png';
   ```

## Pendientes marcados en el código

Buscando `PENDIENTE` en `index.html` salen los puntos sin completar:

- Foto de Fuerza
- Foto y descripción de Yoga
- Credenciales e Instagram de cada coach
- Fotos reales para Leidy, Marwill, Nicolas
- Testimonios reales (los actuales son ejemplos)
- 6 fotos cuadradas para la grilla de Instagram
