# 🐤 pollito.debug()

> Tu patito debugger más paciente. Le explicás tu bug línea por línea... y de repente lo encontrás solito.

![Pollito en modo chat](screenshots/chat.png)

## Qué es

Una web de **rubber duck debugging** con personaje. **Pollito** te escucha mientras le cuentas tu código. No te da la respuesta: te hace preguntas para que la encuentres vos.

La técnica del patito de goma es real. Explicar tu problema en voz alta, paso a paso, suele revelar el error sin que nadie te lo diga. Pollito es esa goma, pero con acento boliviano y método socrático.

## Características

- 🌍 **Trilingüe** — Español, Inglés y Sueco. Cambias de idioma desde la barra superior.
- 💬 **Chat con Pollito** — clasifica tu mensaje (bug, frustración, saludo, resuelto...) y responde desde bancos de frases curados por categoría e idioma.
- 📖 **Blog** — sección de artículos sobre la técnica y el debugging.
- 🎮 **Estética retro terminal** — pixel art, scanlines y tipografías Press Start 2P, VT323 y JetBrains Mono.
- 🪶 **Sin paso de build** — un único HTML más su runtime. React y Babel se cargan desde unpkg en tiempo de ejecución.

![Versión en sueco](screenshots/sv2.png)

## Cómo correrlo

El runtime usa `fetch`, así que el sitio **necesita servirse por HTTP**. Abrir el archivo con doble clic (`file://`) no funciona.

En local:

```bash
# desde la carpeta del proyecto
python -m http.server 8000
# luego abre http://localhost:8000
```

En producción sirve cualquier host estático: GitHub Pages, Netlify, Cloudflare Pages o tu propio servidor.

## Estructura

```
├── index.html        # la web (renómbralo desde "Pollito Debug.dc.html")
├── support.js        # runtime dc: parser + cargador de React
└── screenshots/
    ├── chat.png
    └── sv2.png
```

## Notas técnicas

- El chat es **scripted**, no usa un modelo de IA. Las respuestas salen de bancos por categoría e idioma.
- Necesita conexión a internet para cargar React y Babel desde CDN.

## Licencia

_Pendiente de elegir (por ejemplo MIT)._
