# NexaG Software Factory — Landing

Landing page profesional de **NexaG Software Factory** (Astro).

## Stack

- [Astro](https://astro.build/) 7
- CSS propio con la paleta de marca
- Formulario de contacto vía [FormSubmit](https://formsubmit.co/) → `lukassvergara@gmail.com`
- CTAs a [Calendly](https://calendly.com/nexag/15min)

## Desarrollo local

Requiere Node.js 22+.

```bash
npm install
npm run dev
```

Build de producción:

```bash
npm install
npm run build
npm run preview
```

La salida estática queda en `dist/`. Esa carpeta es lo que se sube a producción.

## Deploy a producción

Sitio configurado: `https://nexag.com.ar` (`astro.config.mjs` → `site`).

1. Asegurate de estar en la rama lista para prod (`main`).
2. Generá el build:
   ```bash
   npm ci
   npm run build
   ```
3. Publicá el contenido de `dist/` en tu hosting estático (Cloudflare Pages, Netlify, Firebase Hosting, etc.).

### Cloudflare Pages (recomendado)

Desde la raíz del repo:

```bash
npx wrangler pages deploy dist --project-name=nexag-landing
```

O conectá el repo en el dashboard de Cloudflare Pages:

- Framework preset: Astro
- Build command: `npm run build`
- Output directory: `dist`
- Branch de producción: `main`

### Checklist pre-deploy

- [ ] Logo final en `public/logo.png` (PNG transparente)
- [ ] Favicon en `public/favicon.png`
- [ ] FormSubmit confirmado en `lukassvergara@gmail.com`
- [ ] Calendly `https://calendly.com/nexag/15min` activo
- [ ] DNS de `nexag.com.ar` apuntando al hosting

## Contacto / FormSubmit

La primera vez que alguien envíe el formulario, FormSubmit pide confirmar el email destino. Revisá la bandeja de `lukassvergara@gmail.com` y aceptá el enlace de activación.
