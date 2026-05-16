# entorno_greka

> *El lenguaje no es un instrumento. Es el lugar donde el pensamiento ocurre.*

Una familia de diccionarios standalone. Cada uno es un solo archivo HTML.
Sin dependencias. Sin servidor. Sin tracking. Doble clic y funciona.

---

## Los cuatro diccionarios

| Repositorio | Lengua / Campo | Entradas | Descripción |
|---|---|---|---|
| [sensus-latinus](https://github.com/trco/sensus-latinus) | Latín · Griego clásico | 27 | Etimología PIE, modos Aficionado/Estudiante/Profesor, comparación romance |
| [sensus-graecus](https://github.com/trco/sensus-graecus) | Griego clásico | 25+ | Filosofía presocrática, clásica y helenística. Logos, physis, polis, mimesis |
| [sensus-semansis](https://github.com/trco/sensus-semansis) | Griego · IA | 40 | Reflexión sobre creatividad artificial. #ReflejosHíbridos |
| [sensus-nepantla](https://github.com/trco/sensus-nepantla) | Spanglish | 12 + carteles | Frontera lingüística. Anzaldúa, Freire, biopolítica computacional |

---

## Arquitectura común

Todos los diccionarios del Entorno Greka comparten tres principios:

**1. Standalone puro**
Un solo archivo `.html`. CSS y JavaScript embebidos. Sin npm, sin bundler,
sin framework, sin conexión a internet necesaria. Puede vivir en una USB,
en un teléfono sin datos, en una computadora de biblioteca pública.

**2. Diseño como posición**
La forma no es decoración. Cada diccionario tiene una identidad visual
que corresponde a su ontología:
- SENSUS LATINUS / GRAECUS → Paula Scher: tipografía como imagen, monocromático,
  diagonales. El póster que es un diccionario.
- SENSUS SEMANSIS → Negro profundo, términos griegos sobre IA. El espejo sin compasión.
- SENSUS NEPANTLA → Terracota, neón, caliche. La paleta de la frontera.
  DoNotTryToReadThis.

**3. Progressive disclosure**
El contenido se despliega según el nivel del lector. No hay información
oculta: hay información que espera el momento adecuado.

---

## Instalar cualquiera de los cuatro

```bash
# Opción A — clonar
git clone https://github.com/trco/sensus-latinus.git

# Opción B — descargar el HTML directamente
# → ir al repositorio → click en index.html → Download raw file

# Opción C — usar directamente desde GitHub Pages
# (ver cada repositorio para el link)
```

Después: **doble clic sobre el archivo HTML**. No se necesita nada más.

---

## El corpus teórico

Cada diccionario opera desde una tradición diferente:

**SENSUS LATINUS / GRAECUS**
Lewis & Short, Liddell-Scott-Jones, Perseus Digital Library, Logeion.
Etimología PIE según Watkins y de Vaan. Filosofía griega desde los
presocráticos hasta el helenismo.

**SENSUS SEMANSIS**
Filosofía del lenguaje, semiótica, filosofía de la mente.
La pregunta central: si la creación ya no requiere experiencia,
¿qué queda de lo humano en el acto de crear?

**SENSUS NEPANTLA**
Gloria Anzaldúa — *Borderlands / La Frontera* (1987)
Paulo Freire — *Pedagogía del oprimido* (1968)
Guillermo Bonfil Batalla — *México profundo* (1987)
Guy Debord — *La sociedad del espectáculo* (1967)
Michel Foucault · Giorgio Agamben · György Lukács

---

## Schema canónico

Cada entrada del Entorno Greka sigue un schema JSON interno
con los campos mínimos obligatorios:

```json
{
  "id": "string",
  "lemma": "string",
  "lang": "latin | greek | spanglish",
  "pos": "string",
  "themes": ["I",...],
  "level": "basico | intermedio | avanzado",
  "defs": [{ "text": "string", "audience": "string" }],
  "etym": { "pie": "string", "path": [], "notes": "string" },
  "example": { "quote": "string", "author": "string", "work": "string" },
  "sources": [{ "type": "string", "title": "string", "confidence": "string" }]
}
```

Los campos `researchNotes`, `negativeTheologyTags`, `famousPhrases`
y `thesis` son extensiones específicas por diccionario.

---

## Roadmap

- [ ] ARIA completo en los cuatro standalones
- [ ] Modo black & white / alto contraste
- [ ] Frases latinas célebres — sección independiente en SENSUS LATINUS
- [ ] Investigaciones de teología negativa — SENSUS GRAECUS / SENSUS LATINUS
- [ ] Base de datos JSON externa + compilador HTML automático
- [ ] SENSUS _____ — el quinto diccionario (pendiente)

---

## Licencia

`CC BY-NC-SA 4.0`
Libre para uso y adaptación no comercial con atribución.
Los derivados deben mantener la misma licencia.

---

## Autor

**Rei García / KhaosLiminal**
Morelia, Michoacán, México
Entorno Greka · 2026

---

*Cuatro archivos HTML. Cuatro ontologías. Una sola pregunta:*
*¿qué es lo que el lenguaje guarda cuando creemos que solo comunica?*
