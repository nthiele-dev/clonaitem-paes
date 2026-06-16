# Clonaítem PAES

Generador de ítemes clonados desde pruebas DEMRE, con soporte LaTeX y justificación de distractores.

## Despliegue en Vercel (paso a paso)

### Paso 1 — Crear cuenta GitHub
1. Ve a https://github.com y crea una cuenta gratuita
2. Haz clic en **New repository**
3. Nombre: `clonaitem-paes`
4. Marca **Public** y haz clic en **Create repository**

### Paso 2 — Subir los archivos a GitHub
1. En tu nuevo repositorio, haz clic en **uploading an existing file**
2. Sube los 3 archivos manteniendo la estructura de carpetas:
   - `api/generate.js`
   - `public/index.html`
   - `vercel.json`
3. Haz clic en **Commit changes**

### Paso 3 — Conectar con Vercel
1. Ve a https://vercel.com y crea cuenta con tu GitHub
2. Haz clic en **Add New Project**
3. Importa el repositorio `clonaitem-paes`
4. Haz clic en **Deploy** (sin cambiar nada más)

### Paso 4 — Agregar tu API key de Anthropic
1. En Vercel, ve a tu proyecto → **Settings** → **Environment Variables**
2. Agrega:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** tu API key de https://console.anthropic.com
3. Haz clic en **Save**
4. Ve a **Deployments** → haz clic en los 3 puntos → **Redeploy**

### Paso 5 — Usar la app
- Tu app estará en: `https://clonaitem-paes.vercel.app` (o similar)
- Comparte esa URL con quien quieras
- Funciona en móvil, tablet y PC sin instalar nada

## Estructura del proyecto

```
clonaitem-paes/
├── api/
│   └── generate.js      ← Proxy hacia Anthropic API (resuelve CORS)
├── public/
│   └── index.html       ← App completa con LaTeX y MathJax
└── vercel.json          ← Configuración de rutas Vercel
```

## Características
- ✅ Sin CORS — el proxy en Vercel hace las llamadas a Anthropic
- ✅ LaTeX renderizado con MathJax
- ✅ Múltiples PDFs sin límite
- ✅ 3 variantes por ítem (fácil/medio/difícil)
- ✅ Clave y justificación de distractores
- ✅ Funciona en móvil

## Costo
- Vercel: **gratis** (plan hobby)
- Anthropic API: ~$0.05–0.15 USD por generación de 20 ítemes
- Los créditos gratuitos de Anthropic cubren cientos de generaciones
