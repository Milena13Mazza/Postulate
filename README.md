# Postulate

Generador de CV, carta de presentación y email de postulación, adaptados automáticamente a cada aviso de trabajo que pegues.

Es una app de una sola página (HTML + CSS + JS), sin backend ni servidor: corre entera en el navegador.

## Qué hace

1. **Cargás tu perfil una vez** — subís tu CV en PDF (la app precompleta lo que puede leer) o lo completás a mano: datos de contacto, experiencia, educación, idiomas y tus habilidades con tu nivel real (Avanzado / Intermedio / Básico).
2. **Pegás el texto de un aviso de trabajo.**
3. La app genera:
   - Un **CV en PDF** (texto real y seleccionable, compatible con lectores ATS) y en TXT, con las habilidades que pide el aviso destacadas primero y tu experiencia reordenada por relevancia.
   - Una **carta de presentación** (PDF y TXT).
   - Un **email de postulación** (HTML) con links a tu portfolio, LinkedIn y WhatsApp.
4. Detecta automáticamente:
   - El **tono** del aviso (casual, formal o neutro) y adapta el saludo y la apertura del email/carta.
   - Si el aviso **pide tu pretensión salarial**, y agrega esa sección al CV.
   - Si el puesto **no coincide** con tu perfil, y te avisa antes de que postules a algo que no tiene sentido.

## Cómo usarla

### Opción A — Abrirla directo
Descargá `index.html` y abrilo con cualquier navegador (doble clic). No necesita instalación.

### Opción B — GitHub Pages
1. Subí este repo a GitHub.
2. Andá a **Settings → Pages**, elegí la rama `main` y la carpeta raíz (`/`).
3. GitHub te va a dar una URL tipo `https://tu-usuario.github.io/postulate/` para usarla desde cualquier dispositivo.

## Guardar tu perfil entre usos

Una vez que cargás tu perfil, podés **exportarlo como JSON** (botón "Exportar") y la próxima vez **importarlo** en vez de resubir el PDF y completar todo de nuevo. El archivo se guarda en tu computadora, no en ningún servidor.

## Notas importantes

- **Todo corre en tu navegador.** Ningún dato (tu CV, tus datos de contacto, el aviso que pegás) sale de tu computadora ni se envía a ningún servidor — no hay backend.
- **El parseo del PDF es heurístico**, no usa IA: busca patrones de texto (secciones típicas como "Experiencia", "Educación", etc.). Funciona mejor con CVs con secciones claras. Siempre revisá y corregí los datos en el formulario antes de guardar tu perfil.
- Requiere conexión a internet la primera vez que se carga (para traer las fuentes y las librerías `jsPDF` y `pdf.js` desde un CDN).

## Stack

HTML, CSS y JavaScript vanilla. Librerías externas (vía CDN):
- [jsPDF](https://github.com/parallax/jsPDF) — generación de PDFs.
- [pdf.js](https://mozilla.github.io/pdf.js/) — lectura de texto de PDFs subidos.

## Licencia

MIT — ver [LICENSE](LICENSE).
