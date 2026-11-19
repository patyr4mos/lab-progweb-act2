# d’Invité — Sitio web de invitaciones digitales

**Actividad 2. Desarrollo de un sitio web responsivo, semántico y accesible**
Laboratorio de Programación Web · UANL FIME · Agosto–Diciembre 2026
Autora: Patricia Lizeth Ramos Ortiz (matrícula 2161739)

🔗 **Sitio publicado:** https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/

## Objetivo

Construir y publicar un sitio web responsivo con HTML5 semántico y CSS moderno, aplicando principios de usabilidad, accesibilidad y validación de estándares. El caso elegido es **d’Invité**, un pequeño negocio de invitaciones web (digitales) para eventos como XV años, bodas y bautizos.

## Tecnologías

- HTML5 semántico (`header`, `nav`, `main`, `section`, `article`, `aside`, `footer`)
- CSS3 con **Flexbox** (encabezado, navegación, botones, pie de página) y **Grid** (hero, tarjetas, paquetes, contacto)
- Variables CSS, `clamp()` y media queries
- Git y GitHub Pages para el despliegue
- Sin frameworks ni librerías externas (sin JavaScript)

## Estructura del proyecto

```
├── index.html        # Inicio
├── servicios.html    # Servicios / paquetes
├── contacto.html     # Contacto (formulario)
├── css/styles.css    # Estilos
├── assets/           # Imágenes SVG (invitación de ejemplo y favicon)
├── docs/             # Capturas para este README
└── README.md
```

## Vistas del sitio

1. **Inicio:** presentación del negocio, cómo funciona y lo que incluye una invitación.
2. **Servicios:** paquetes Básico ($299), Completo ($549) y Premium ($899 MXN), pago único.
3. **Contacto:** formulario con etiquetas, validación nativa y datos de contacto.

## Diseño responsivo

- Enfoque fluido: contenedor con `min()`, tipografía con `clamp()` y cuadrículas `auto-fit`.
- **Breakpoints:** `860px` (tablet: el hero y el contacto pasan a una columna) y `600px` (teléfono: navegación centrada, botones a ancho completo, encabezado no fijo).
- Probado en vista de escritorio (1280 px) y móvil (390 px) con las herramientas de desarrollo del navegador.

| Página | Escritorio | Móvil |
|---|---|---|
| Inicio | ![Inicio escritorio](docs/index-escritorio.png) | ![Inicio móvil](docs/index-movil.png) |
| Servicios | ![Servicios escritorio](docs/servicios-escritorio.png) | ![Servicios móvil](docs/servicios-movil.png) |
| Contacto | ![Contacto escritorio](docs/contacto-escritorio.png) | ![Contacto móvil](docs/contacto-movil.png) |

## Accesibilidad aplicada

- `lang="es"`, títulos descriptivos por página y jerarquía de encabezados correcta (un `h1` por página; `h2` y `h3` en orden).
- Enlace “Saltar al contenido principal” y navegación con `aria-label` y `aria-current="page"`.
- Texto alternativo en la imagen principal (`alt`) y título/descripción en el SVG.
- Todos los campos del formulario con `<label>` asociado, indicación de campos obligatorios y texto de ayuda con `aria-describedby`.
- Contraste de color alto (texto `#3A2A2F` sobre `#FBF1F2`; botones blancos sobre `#8E2F52`, relación aproximada 7:1).
- Foco visible en enlaces, botones y campos; se respeta `prefers-reduced-motion`.
- Navegable completamente con teclado; tamaños de texto relativos (`rem`).

## Resultados de validación

| Herramienta | Resultado |
|---|---|
| W3C Markup Validation Service — `index.html` | _(pega aquí el resultado, p. ej. “No errors or warnings”)_ |
| W3C Markup Validation Service — `servicios.html` | _(resultado)_ |
| W3C Markup Validation Service — `contacto.html` | _(resultado)_ |
| W3C CSS Validation Service — `styles.css` | _(resultado)_ |

Capturas de la validación: _(agrega las imágenes en `docs/` y enlázalas aquí)_.

## Cómo ejecutarlo localmente

Abre `index.html` en el navegador (no requiere servidor).

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio público en GitHub y sube todos los archivos de esta carpeta.
2. En **Settings → Pages**, elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
3. Espera un minuto: el sitio quedará en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`.

## Notas

- El formulario usa `mailto:` porque el sitio es estático y no tiene servidor; para recibir solicitudes automáticamente se podría integrar un servicio de formularios.
- El correo, el teléfono y la ubicación son datos de ejemplo para el proyecto.
