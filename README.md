# SOLIDARIO - PWA para campaña solidaria

App web progresiva (PWA) para difundir la campaña de Sofía por WhatsApp.

## Archivos incluidos

```
solidario/
├── index.html      ← App principal (todo el código)
├── manifest.json   ← Config PWA (nombre, iconos, colores)
├── sw.js           ← Service Worker (modo offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Cómo publicar (GRATIS en 5 minutos)

### Opción A — Netlify Drop (más fácil)
1. Ir a https://app.netlify.com/drop
2. Arrastrar la carpeta `solidario/` completa
3. ¡Listo! Te da una URL pública tipo `https://solidario-abc123.netlify.app`
4. Podés cambiar el nombre en Settings → Domain

### Opción B — GitHub Pages (gratis y permanente)
1. Crear cuenta en github.com
2. Nuevo repositorio → subir todos los archivos
3. Settings → Pages → Source: main branch / root
4. URL: `https://tu-usuario.github.io/solidario`

### Opción C — Vercel
1. Ir a https://vercel.com
2. "Deploy" → arrastrá la carpeta
3. URL lista en segundos

## Cómo usar la app

1. Abrir la URL en el celular
2. En Android: el navegador ofrece "Instalar app" automáticamente
3. En iPhone: Safari → botón Compartir ⬆️ → "Agregar a pantalla de inicio"
4. Dentro de la app:
   - Tocá el área de imagen y cargá la foto de la campaña
   - El mensaje ya está listo (podés editarlo)
   - Tocá "Compartir en WhatsApp" → se abre WhatsApp con la imagen y el mensaje
   - Elegí contactos o grupos y enviá

## Personalizar el mensaje por defecto

En `index.html`, buscar esta línea:
```
id="message-text"
```
Y cambiar el texto del textarea.

## Agregar la URL real de la app en el mensaje

En `index.html`, en el textarea del mensaje, reemplazar:
```
[enlace a tu app]
```
Por la URL pública de tu app (ej: `https://solidario.netlify.app`).

## Funcionalidades

- ✅ PWA instalable en Android e iPhone
- ✅ Funciona offline (Service Worker)
- ✅ Carga imagen de campaña desde galería
- ✅ Comparte imagen + mensaje via WhatsApp (Web Share API)
- ✅ Fallback a wa.me si no hay Web Share
- ✅ Mensaje editable
- ✅ Contador de veces compartido (guardado en el dispositivo)
- ✅ Estimación de alcance
- ✅ Instrucciones de instalación para iOS
- ✅ Diseño mobile-first cálido y emotivo

## Tecnología

- HTML/CSS/JS puro (sin frameworks, carga instantánea)
- Web Share API para compartir imagen nativa
- Service Worker para modo offline
- localStorage para persistir el contador
