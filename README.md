# AI-STEAM Network — Diagramas / Diagrams

Colección de diagramas interactivos de la aplicación **AI-STEAM Network** (CEICE / CECU), en
español e inglés. Cada diagrama es un HTML autocontenido: se abre en el navegador, con vistas
guiadas, búsqueda, tema claro/oscuro, zoom y exportación a imagen.

Interactive diagrams of the **AI-STEAM Network** application (CEICE / CECU), in Spanish and
English. Every diagram is a self-contained HTML file: guided views, search, light/dark theme,
zoom and image export.

**Sitio publicado / Published site:** https://jsmiragregori.github.io/AI-STEAM-DIAGRAMS/

Punto de entrada / Entry point: [`index.html`](index.html) (selector Español / English).

## Índice / Index

| # | Tema / Topic | Tipo / Type | Español | English |
|---|---|---|---|---|
| 01 | Arquitectura y flujo de publicación / Architecture and publishing flow | Arquitectura | [Abrir](01-arquitectura-ai-steam.es.html) | [Open](01-arquitectura-ai-steam.en.html) |
| 02 | Visita pública / Public visit | Secuencia | [Abrir](02-visita-publica.es.html) | [Open](02-visita-publica.en.html) |
| 03 | Publicación de contenido / Content publishing | Secuencia | [Abrir](03-publicacion-contenido.es.html) | [Open](03-publicacion-contenido.en.html) |
| 04 | Flujo editorial / Editorial workflow | Flujo de trabajo | [Abrir](04-flujo-editorial.es.html) | [Open](04-flujo-editorial.en.html) |
| 05 | Datos y multilingüismo / Data and multilingual content | Flujo de datos | [Abrir](05-datos-multilingues.es.html) | [Open](05-datos-multilingues.en.html) |
| 06 | Seguridad y cumplimiento / Security and compliance | Arquitectura | [Abrir](06-seguridad-cumplimiento.es.html) | [Open](06-seguridad-cumplimiento.en.html) |
| 07 | Arquitectura interna del sitio público / Internal architecture of the public site | Arquitectura | [Abrir](07-arquitectura-sitio-publico.es.html) | [Open](07-arquitectura-sitio-publico.en.html) |
| 08 | Defensa en profundidad / Defence in depth | Flujo de datos | [Abrir](08-defensa-en-profundidad.es.html) | [Open](08-defensa-en-profundidad.en.html) |
| 09 | Sesiones del panel / Panel sessions | Ciclo de vida | [Abrir](09-ciclo-sesion-panel.es.html) | [Open](09-ciclo-sesion-panel.en.html) |
| 10 | Puertas de calidad / Quality gates | Flujo de trabajo | [Abrir](10-puertas-calidad.es.html) | [Open](10-puertas-calidad.en.html) |

## Estructura / Structure

| Fichero / File | Contenido / Content |
|---|---|
| `index.html` | Índice con selector de idioma / Language-switching index |
| `*.es.html`, `*.en.html` | Diagramas entregados, autocontenidos / Delivered, self-contained diagrams |
| `*.es.*.json`, `*.en.*.json` | Especificaciones fuente de cada diagrama / Source specifications |
| `*.visual-check.json` | Recibos de verificación en navegador: 4 resoluciones × 2 temas, con SHA-256 del artefacto / Browser verification receipts |

## Generación / Generation

Los diagramas se generan con la skill **archify** a partir de las especificaciones `*.json`
(calidad `showcase`, 9/9 comprobaciones, 0 errores y 0 avisos). El flujo es:

```bash
node bin/archify.mjs validate <tipo> <spec.json> --quality showcase
node bin/archify.mjs deliver  <tipo> <spec.json> <salida.html> --quality showcase
```

Los diagramas **01** y **06** citan código del repositorio privado **AI-STEAM-CONTENT**, y el **07**
cita código de **AI-STEAM-VANILLA**; para regenerarlos con verificación de evidencia hay que añadir
`--repo-root <ruta al repositorio correspondiente>`.

The diagrams are generated with the **archify** skill from the `*.json` specifications
(`showcase` quality, 9/9 checks, 0 errors and 0 warnings). Diagrams **01** and **06** cite code
from the private **AI-STEAM-CONTENT** repository and **07** cites **AI-STEAM-VANILLA**; add
`--repo-root <path to the matching repository>` to regenerate them with evidence verification.

La aplicación, sus fuentes y su documentación viven en **AI-STEAM-CONTENT**; este repositorio
solo publica los diagramas. / The application, its sources and its documentation live in
**AI-STEAM-CONTENT**; this repository only publishes the diagrams.

## Nota / Note

La interfaz fija del visor (botones, leyenda del navegador) está en inglés por limitación de la
herramienta; el contenido de los diagramas está en español e inglés. / The fixed viewer UI
(buttons, navigation legend) is in English due to a tool limitation; the diagram content is in
Spanish and English.

Publicado con GitHub Pages desde la rama `main` (raíz del repositorio). / Published with GitHub
Pages from the `main` branch (repository root).
