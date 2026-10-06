# ¿Qué tengo cerca? (GPS + Wikipedia)

Una sola página estática: sin servidor, sin claves de API y sin coste.

## Cómo funciona
1. Lee tu posición con el GPS del móvil.
2. Pregunta a la API de Wikipedia por los artículos geolocalizados cerca (radio elegible).
3. Los muestra ordenados por distancia, con foto, resumen y enlace.
4. Con la brújula activada, la flecha de cada lugar indica hacia dónde está respecto a donde apuntas el móvil.

## Publicarla gratis (necesita HTTPS para el GPS)

**Netlify Drop (lo más rápido, sin cuenta de Git):**
entra en app.netlify.com/drop y arrastra la carpeta `monumentos-gps`.

**GitHub Pages:**
sube `index.html` a un repositorio y activa Pages en Settings → Pages.

**Cloudflare Pages:** crea un proyecto y sube la carpeta.

Abre luego la URL HTTPS desde el móvil y acepta el permiso de ubicación.

## Probar en el ordenador
Doble clic en `index.html` puede bloquear el GPS. Mejor:
```
cd monumentos-gps
python3 -m http.server 8000
```
y abre http://localhost:8000 (localhost cuenta como entorno seguro).

## Atribución
Los textos de Wikipedia se publican bajo licencia CC BY-SA; la app ya incluye el enlace
al artículo original en cada ficha.
