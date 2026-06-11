# Go Detailing — Web

Web premium de detailing a domicilio en el Alt Empordà. Una sola página (`index.html`), responsive, lista para GitHub Pages.

## Estructura

```
index.html          → la web
404.html            → página de error con tu estilo
sitemap.xml         → mapa del sitio para Google
robots.txt          → instrucciones para buscadores
assets/
  img/              → imágenes (ahora hay PLACEHOLDERS, sustitúyelos)
  video/            → vídeo del hero (opcional)
```

## Publicar en GitHub Pages

1. Sube TODO (con la carpeta `assets`) a un repositorio.
2. En el repo: **Settings → Pages → Source: Deploy from a branch → rama `main` / carpeta `/root`**.
3. En unos minutos tu web estará online.

## IMPORTANTE: sustituir las imágenes

En `assets/img/` hay imágenes de relleno (placeholders) para que la web no se vea rota.
Sustitúyelas por las tuyas REALES manteniendo EXACTAMENTE el mismo nombre de archivo:

| Archivo | Qué es | Tamaño recomendado |
|---|---|---|
| `logo-godetailing.png` | Logo (fondo transparente) | alto ~90px |
| `favicon.png` | Icono pestaña navegador | 64×64 |
| `apple-touch-icon.png` | Icono iPhone | 180×180 |
| `og-godetailing.jpg` | Imagen al compartir (WhatsApp/redes) | 1200×630 |
| `hero-detailing.jpg` | Foto grande de cabecera | 1600×900 |
| `antes-detailing.jpg` | Antes (slider) | 1200×900 |
| `despues-detailing.jpg` | Después (slider) | 1200×900 |
| `cta-detailing.jpg` | Fondo sección final | 1600×900 |
| `galeria-*.jpg` (9) | Fotos de trabajos | 800×800 (cuadradas) |

Consejo: exporta las fotos en JPG, ancho máximo ~1600px y peso < 400 KB cada una, para que la web cargue rápido.

## Vídeo en el hero (opcional)

1. Sube el vídeo a `assets/video/` (ej. `hero-detailing.mp4`).
2. En `index.html`, busca el comentario "FONDO DEL HERO": comenta el `<img>` y descomenta el bloque `<video>`.

## Dominio

Todo apunta a `https://www.godetailing.es/` (canonical, og:url, og:image, JSON-LD,
`sitemap.xml` y `robots.txt`). El dominio personalizado se fija con el archivo `CNAME`
de la raíz, que contiene `www.godetailing.es`.

### Conectar el dominio (el dominio está en Hostinger, no en Wix)

En el panel **DNS de Hostinger** para `godetailing.es`:

1. **Borra** el registro **A** del apex que apunta a Wix (`185.230.63.107`) y crea
   estos 4 registros **A** (host `@`) hacia GitHub Pages:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. Cambia el **CNAME** de `www` de `pointing.wixdns.net` a `terulet.github.io`.

Luego, en GitHub → **Settings → Pages → Custom domain**: `www.godetailing.es` y activa
**Enforce HTTPS** (el certificado lo emite GitHub automáticamente).

Con los 4 A records, `godetailing.es` (sin www) redirige solo a `www.godetailing.es`.
Cuando la web nueva funcione, se puede cancelar el plan de Wix sin perder el dominio.

## Datos de contacto integrados

- WhatsApp: +34 694 27 01 66
- Email: GoDetailingit@gmail.com
- Instagram / TikTok: @godetailingit
- Zona: Roses, Empuriabrava, Figueres y Alt Empordà
