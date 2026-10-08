# Enten

Entreno, nutrición, pasos y ayuno en una sola app, con un coach que conoce tus datos.

Toda la app está en `Enten.html` (un único archivo, sin compilar). Funciona de dos formas:

| | Dentro de Claude (artefacto) | Fuera de Claude (tu propia web) |
|---|---|---|
| Enlace | `https://claude.ai/artifact/A3Q9gNMtn6fZvSutEPRBBT` | `https://marcos08pr-ops.github.io/mi-artefacto-app/Enten.html` |
| Coach, escáner de comida e importar rutina | Con tu cuenta de Claude, sin clave | Con tu clave de la API de Anthropic (se cobra aparte) |
| Dónde se guardan los datos | En tu cuenta de Claude | Solo en ese navegador |
| Pantalla de inicio del iPhone | Icono de Claude y, según cómo la añadas, barra de Safari | Icono Σ y pantalla completa |

## Usar Enten sin tener Claude abierto

### 1. Publica la app con GitHub Pages (una vez)

1. Fusiona esta rama en `main`.
2. En GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)` → **Save**.
3. A los uno o dos minutos la app está en `https://marcos08pr-ops.github.io/mi-artefacto-app/Enten.html`.

GitHub Pages gratis necesita que el repositorio sea público. El código no contiene datos tuyos ni claves: tus datos y tu clave se quedan en el navegador.

### 2. Crea una clave de API

1. Entra en <https://console.anthropic.com>, añade saldo en **Billing** y crea una clave en **API Keys**.
2. Abre Enten en esa dirección → **Ajustes → IA sin Claude → Añadir** y pega la clave (`sk-ant-…`).

La clave se guarda solo en ese navegador y la app la envía únicamente a `api.anthropic.com`. Cada consulta al coach se cobra en tu cuenta de la API, no en tu suscripción de Claude. El coach usa Claude Opus 5.5 con esfuerzo bajo para que las respuestas sean rápidas y baratas.

### 3. Añádela a la pantalla de inicio

En el iPhone, abre la dirección en **Safari → Compartir → Añadir a pantalla de inicio**. Se instala con el icono Σ y se abre a pantalla completa, sin la barra de Safari. Pon la clave de API **dentro de la app ya instalada**, porque guarda sus datos aparte de Safari.

### Pasar tus datos de una versión a otra

Las dos versiones no comparten datos. Para llevarte lo que tienes en la versión de Claude: **Ajustes → Exportar copia** en la de Claude y **Ajustes → Importar** en la nueva.

## Archivos

- `Enten.html`: la app completa.
- `apple-touch-icon.png`: icono Σ (1024 × 1024).
- `manifest.webmanifest`: hace que la app se pueda instalar a pantalla completa.

## Publicar cambios en el artefacto de Claude

El artefacto se actualiza volviendo a publicar `Enten.html` con `apple-touch-icon.png` y `manifest.webmanifest` como archivos adjuntos, en la misma URL.
