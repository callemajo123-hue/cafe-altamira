# Reto · Página de catas `eventos.html` (5.0)

Café Altamira organiza catas de café y necesita una página para anunciarlas e
inscribir a los asistentes. Créala **desde cero** en `eventos.html`, reutilizando
`css/estilos.css`. El verificador **no** revisa esta página: tú escribes tu propia
lista de verificación y demuestras que se cumple.

## Lo que debe tener la página

1. Mismo encabezado y navegación que `index.html` (con un enlace a `eventos.html`
   en las dos páginas y `aria-current="page"` en el de la página actual), enlace
   "Saltar al contenido", `<main>` y `<footer>`.
2. Un único `<h1>` y encabezados sin saltos de nivel.
3. **3 catas** como `<article>`, cada una con `<h3>`, una fecha en
   `<time datetime="2026-11-20T16:00">`, cupos y precio.
4. Un **formulario de inscripción** con:
   - nombre y correo con `<label>` asociado y `required`;
   - la cata elegida como grupo de `radio` dentro de `<fieldset>` con `<legend>`;
   - una casilla "Acepto el tratamiento de datos" (`checkbox` con su `label`);
   - `<button type="submit">`.
5. Al menos una imagen con `alt` descriptivo y una decorativa con `alt=""`.

## Lo que debes entregar

- `eventos.html` funcionando y enlazada desde `index.html`.
- En este mismo archivo, debajo de **Mi lista de verificación**, escribe **5 o más**
  verificaciones propias con el formato Dado / cuando / entonces y marca `[x]` las
  que comprobaste. Ejemplo:
  `- [x] Dado que estoy en el formulario, cuando presiono Tab, entonces paso por nombre, correo, cada cata y el botón, en ese orden.`
- Captura de Lighthouse (pestaña Accesibilidad) de `eventos.html` con **90 o más**,
  guardada como `evidencias/lighthouse-eventos.png`.
- `node verificar.js` sigue en 40/40 (no rompiste lo guiado).

## Rúbrica

| Criterio | Valor |
|---|---|
| Estructura semántica: landmarks, h1 único, orden de encabezados, `article` + `time` | 1.5 |
| Formulario accesible: labels, `fieldset`/`legend`, `required`, botón real, uso con teclado | 1.5 |
| Lista de verificación propia (5+, Dado/cuando/entonces) y captura de Lighthouse ≥ 90 | 1.0 |
| `index.html` sigue en 40/40 y la navegación entre páginas funciona | 1.0 |
| **Total** | **5.0** |

---

## Mi lista de verificación

- [x] Dado que abro `eventos.html`, cuando reviso los encabezados, entonces hay un solo `<h1>` ("Catas de café") y los niveles bajan sin saltos (h1 → h2 → h3).
- [x] Dado que estoy en la sección "Próximas catas", cuando reviso cada cata, entonces es un `<article>` con su `<h3>`, una fecha en `<time datetime>`, los cupos y el precio.
- [x] Dado que reviso los landmarks, cuando abro DevTools → Accessibility, entonces encuentro banner (`<header>`), navegación "Principal", principal (`<main id="contenido">`) e información de contenido (`<footer>`).
- [x] Dado que estoy en el formulario, cuando hago clic en el texto "Nombre completo", "Correo electrónico", el nombre de una cata o "Acepto el tratamiento de datos", entonces se enfoca o se marca el campo asociado (cada `label for` coincide con su `id`).
- [x] Dado que las catas son opciones excluyentes, cuando reviso el formulario, entonces están en un grupo de `radio` con el mismo `name`, dentro de un `<fieldset>` con `<legend>`.
- [x] Dado que envío el formulario vacío, cuando presiono "Inscribirme", entonces el navegador no lo envía y me pide nombre, correo, cata y aceptar el tratamiento de datos (`required`).
- [x] Dado que reviso las imágenes, cuando inspecciono el `alt`, entonces la foto de la finca tiene un `alt` descriptivo y el grano del logo tiene `alt=""` porque es decorativo.
- [x] Dado que estoy en `index.html` o en `eventos.html`, cuando uso el menú, entonces el enlace "Catas" lleva a `eventos.html`, los demás llevan a `index.html`, y la página actual tiene `aria-current="page"`.
- [x] Dado que analizo `eventos.html` con Lighthouse (Accesibilidad), cuando termina el análisis, entonces el puntaje es 90 o más (obtuve 100, ver `evidencias/lighthouse-eventos.png`).
- [x] Dado que corro `node verificar.js`, cuando termina, entonces `index.html` sigue en 40/40.
- [ ] Dado que cargo `eventos.html`, cuando presiono Tab por primera vez, entonces aparece el enlace "Saltar al contenido" y al presionar Enter el foco pasa al `<main>`.
- [ ] Dado que estoy en el formulario, cuando presiono Tab, entonces paso por nombre, correo, el grupo de catas (las flechas cambian la opción), la casilla de datos y el botón, en ese orden y con el foco siempre visible.
