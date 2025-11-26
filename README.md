# Staffy PWA

Este paquete contiene una Progressive Web App (PWA) lista para instalar en tu iPhone.

## 📂 Estructura
- `index.html` → Página principal
- `manifest.json` → Configuración de la PWA
- `service-worker.js` → Cache básico para soporte offline
- `icons/` → Iconos genéricos azul con "S"

## 🚀 Instalación

### Opción A: Subdirectorio /staffy-pwa/
1. Sube la carpeta `staffy-pwa` tal cual a tu hosting, de forma que quede accesible en:
   - `https://tu-dominio.com/staffy-pwa/`
2. Abre esa URL en Safari en tu iPhone.
3. Pulsa **Compartir → Añadir a pantalla de inicio**.
4. Verás el icono azul con la "S" y la app se abrirá en modo standalone.

### Opción B: Raíz del dominio
Si la sirves en la raíz (ej: `https://tu-dominio.com/`), cambia en `manifest.json`:
- `"start_url": "/"`
- `"scope": "/"`

Y ajusta también el `BASE_PATH` del `service-worker.js` si es necesario.

## i️ Notas
- Puedes reemplazar los iconos en `icons/` por tus propios diseños.
- El `service-worker.js` cachea los archivos básicos para carga rápida.
