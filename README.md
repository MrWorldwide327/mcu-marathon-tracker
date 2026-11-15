# MCU Marathon Tracker — Camino a Doomsday

**Interactive tracker for a chronological MCU marathon: progress tracking, ratings, data export/import and an animated content-map visualization. Actively maintained.**

🔗 **Live demo:** `https://<tu-usuario>.github.io/<nombre-del-repositorio>/`  *(sustituye por tu enlace real)*

Single-file web app (vanilla HTML/CSS/JS, no dependencies, no build step, no tracking, no third-party images).

---

## English

### What it does
- **50 titles in in-universe chronological order**, from *Eyes of Wakanda* to *Spider-Man: Brand New Day*, so you arrive prepared for *Avengers: Doomsday* (18 Dec 2026). Films and the series that actually matter for the main storyline.
- **Progress checklist**: mark titles as watched; series track **each episode** and show a completion bar.
- **Half-star ratings** (0–5 in 0.5 steps). A series rating is the **average of its episode ratings**, rounded to the nearest half star.
- **Animated content map** (HTML canvas): the main timeline as a mesh of nodes that react to the cursor or touch. Selecting a node opens its sheet plus a sub-network with related content (shorts, spin-offs, other universes), drawn as *before* / *after* branches.
- **Countdown** to the premiere of *Avengers: Doomsday*.
- **Export / import** of your progress as text, with a **versioned format** that automatically migrates backups made with older versions of the title list.
- **Local persistence** (`localStorage`) with graceful fallback if the browser blocks storage.
- **Light / dark theme**, responsive layout, safe-area support, and `prefers-reduced-motion` respected.

### Privacy
Your progress is stored **only in your own browser**. Nothing is sent to any server, and there are no analytics or cookies. Use *Export* to move your progress to another device.

### Technical notes
- One static file (`index.html`, ~70 KB). Works on any static host (GitHub Pages, Netlify, Cloudflare Pages…).
- Data model with explicit versioning (`PAYLOAD_VERSION`) and chained ID migrations, so inserting a new title never corrupts existing progress.
- Canvas rendering with idle motion, pointer/touch interaction, bounds clamping and responsive re-layout.
- When opened inside claude.ai, the same file can optionally sync progress across devices through the platform's per-user storage; on any other host it uses `localStorage` only.

---

## Español

### Qué hace
- **50 títulos en orden cronológico interno** (de *Eyes of Wakanda* a *Spider-Man: Brand New Day*) para llegar preparado a *Avengers: Doomsday* (18 de diciembre de 2026): películas y las series que realmente importan para la trama principal.
- **Checklist de progreso**, con seguimiento **por episodio** en las series y barra de avance.
- **Valoraciones con medias estrellas**; la nota de una serie es la **media de sus episodios**, redondeada a la media estrella más cercana.
- **Mapa animado de contenido** (canvas): malla de nodos que reacciona al cursor o al tacto, con una sub-red de contenido relacionado (cortos, spin-offs, otros universos) en ramas *antes* / *después*.
- **Cuenta atrás** hasta el estreno.
- **Exportar / importar** progreso en formato versionado, con migración automática de copias antiguas.
- Guardado local en el navegador, tema claro/oscuro y diseño adaptable a móvil.

### Privacidad
Tu progreso se guarda **solo en tu navegador**. No se envía a ningún servidor ni hay analítica. Usa *Exportar* para llevarlo a otro dispositivo.

---

## Mantenimiento

Proyecto vivo: la lista se actualiza con los nuevos estrenos y las correcciones de cronología. Cada cambio queda registrado en el historial de commits.

## Aviso legal

Proyecto de fans sin ánimo de lucro, no afiliado a Marvel ni a Disney. Marvel, sus personajes y los títulos citados pertenecen a sus respectivos propietarios. La página solo muestra títulos y texto propio, sin imágenes de terceros.
