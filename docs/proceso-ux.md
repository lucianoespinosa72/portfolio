# Proceso UX/UI — Portfolio

Material base para el archivo de Figma (research) y para el PDF del proceso (máx. 10 slides).
Los puntos marcados con ✏️ los tenés que completar vos con datos reales.

---

## 1. Usuario objetivo

**Visitantes principales:** reclutadores técnicos y líderes de diseño de empresas de software/agencias que buscan perfiles junior o pasantes UX/UI con base en front-end.

**Qué necesitan encontrar en menos de 30 segundos:**
1. Quién soy y qué rol busco (hero).
2. Si estoy disponible (badge).
3. Prueba de que sé diseñar con proceso (un caso de estudio).
4. Cómo contactarme (CTA siempre visible en el header).

### Proto-persona

> **Carolina Méndez, 34 años · Product Design Lead en una software factory de Rosario**
> - **Objetivo:** cubrir una pasantía UX/UI que también pueda maquetar.
> - **Contexto:** revisa ~40 portfolios por búsqueda, muchos desde el celular entre reuniones.
> - **Frustraciones:** portfolios que son solo capturas lindas sin proceso; tener que buscar el mail; sitios lentos.
> - **Necesita:** ver rápido el rol, un caso con problema → proceso → resultado, y el contacto.
> - **Frase:** "Si en un minuto no entiendo qué hace y cómo piensa, paso al siguiente."

### Escenario de uso

Carolina recibe el link del portfolio por LinkedIn mientras viaja. Lo abre en el celular, lee el hero ("Desarrollador Front-end & UX/UI", "Disponible para pasantías"), baja hasta Proyectos, abre el caso de mecanicos app y ve un producto real publicado, con decisiones de diseño justificadas. Toca "Hablemos" en el menú, copia el mail y le escribe para agendar una entrevista. Todo en menos de 3 minutos.

---

## 2. Benchmark (3 portfolios)

| Portfolio | Qué funciona | Qué no funciona |
|---|---|---|
| Portfolio de referencia del docente | Arquitectura clara one-page, navegación por anclas, métricas arriba | ✏️ (ej.: estética oscura muy genérica, poco énfasis en proceso UX) |
| [brittanychiang.com](https://brittanychiang.com) | Jerarquía tipográfica impecable, navegación lateral fija, muy rápida | Muy centrado en código; los proyectos no cuentan el proceso |
| ✏️ Uno de [Bestfolios](https://www.bestfolios.com) | ✏️ | ✏️ |

**Conclusiones para mi diseño:**
- Mantener la estructura one-page con anclas (más rápido para reclutadores).
- Priorizar **casos de estudio** con resultado medible, no repositorios.
- Contacto accesible desde cualquier punto (CTA en el header).

---

## 3. Concepto visual

**3 palabras clave:** **Futurista · Preciso · Cercano**

| Palabra | Color | Tipografía | Imágenes / UI |
|---|---|---|---|
| **Futurista** | Fondo azul-noche `#0a0b14` con acento lima neón `#c6ff3d` (en vez del gris/azul típico) | JetBrains Mono para datos y etiquetas, estilo "terminal/HUD" | Grilla de fondo, anillos tipo HUD, brillos (glow) en hover |
| **Preciso** | Paleta corta: 1 primario, 1 secundario, neutros y estados | Escala 1.25 estricta, Space Grotesk geométrica | Grilla de 4/8 px, numeración 01–05 en secciones |
| **Cercano** | Violeta `#9d90ff` como secundario cálido; modo claro disponible | Textos en voseo, frases cortas | Retrato ilustrado, citas de usuarios en el caso de estudio |

**Diferenciación con la referencia:** aunque ambos son oscuros, este diseño usa otra paleta (azul-violeta + lima en lugar de la de referencia), otra tipografía, grilla HUD de fondo, numeración de secciones y un **toggle claro/oscuro**.

✏️ Moodboard: armá en Figma un frame con 8–12 imágenes (interfaces sci-fi, HUDs, Dribbble "dark neon dashboard", fotos de luces de ciudad) y las muestras de color/tipografía.

---

## 4. Arquitectura de información

### Sitemap

```
Inicio (index.html)
├── Header (logo · Skills · Proyectos · Experiencia · Sobre mí · Contacto · GitHub · tema)
├── #inicio       Hero
├── (métricas)    Highlights
├── #skills       Skills (4 categorías)
├── #proyectos    Proyectos (3)
│    └── caso-estudio.html  → MecanicosApp (problema · proceso · solución · resultado)
├── #experiencia  Timeline
├── #sobre-mi     Sobre mí + 3 principios
├── #contacto     CTA + mail + redes + formulario (demostrativo)
└── Footer
404.html
```

**Justificación del orden:** Proyectos va antes que Experiencia porque, para un perfil junior, los casos de estudio son la prueba más fuerte (lo que el reclutador busca primero).

### Card sorting simple

✏️ Hacelo con 3–5 personas en FigJam (o en papel): dales tarjetas con estos contenidos y pediles que las agrupen y nombren los grupos.

Tarjetas: *Figma · HTML/CSS · Python · MecanicosApp · Qué Delicia! Pastelería · Puerto Pádel · Vaxler · Licenciatura · Principios de trabajo · Foto · Email · LinkedIn · Disponibilidad · Ubicación*

Registrá: grupos que formaron, nombres que les pusieron y qué cambiaste (ej.: "Disponibilidad y ubicación se agruparon con la presentación → van al hero").

---

## 5. Wireframes y design system en Figma (checklist)

- [ ] Wireframes baja fidelidad — página completa en **mobile (375)** y **desktop (1280)**.
- [ ] Paleta: primario, secundario, neutros, estados (success / warning / error) — usar los tokens del README.
- [ ] Escala tipográfica (12 → 61 px) con Space Grotesk y JetBrains Mono.
- [ ] Grilla: mobile 4 col / gutter 16 · tablet 8 col / gutter 24 · desktop 12 col / gutter 32, máx. 1152 px.
- [ ] Espaciado: 4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96.
- [ ] Componentes: **botón en 4 estados** (default, hover, focus, active) primario y ghost · tag · tarjeta de proyecto · ítem de timeline · input (default, hover, focus, error).
- [ ] Prototipo alta fidelidad mobile + desktop, con navegación entre secciones y **menú mobile** prototipado.

Tip: sacá capturas del sitio en 375 y 1280 y usalas como guía para que Figma y el sitio queden iguales (se comparan en la corrección).

---

## 6. Test de usabilidad

**Participantes:** mínimo 3 (ideal 5). ✏️ Nombre/perfil de cada uno (ej.: "P1 — compañero de 4.º año", "P2 — desarrolladora, 28").
**Sobre:** prototipo de Figma (mobile).
**Método:** moderado, pensar en voz alta, 10–15 min por persona.

| # | Tarea | Métrica |
|---|---|---|
| T1 | "Encontrá el email de contacto." | Éxito / tiempo |
| T2 | "Abrí el proyecto más reciente y decime qué problema resolvía." | Éxito / tiempo |
| T3 | "¿Está disponible para trabajar? ¿Dónde vive?" | Éxito |
| T4 | "Desde el celular, andá a la sección de experiencia." | Éxito / errores |
| T5 | "Cambiá el sitio a modo claro." | Éxito |

Al final: "¿Qué fue lo que más te costó?" y "Del 1 al 5, ¿qué tan fácil fue usarlo?"

### Hallazgos y cambios (✏️ completar con lo que pase en tus tests)

| Hallazgo | Usuarios | Severidad | Cambio aplicado |
|---|---|---|---|
| ej.: No veían el CTA de contacto en mobile | 2/3 | Alta | Se agregó botón "Hablemos" dentro del menú mobile |
| ej.: No sabían que la tarjeta era clickeable | 2/3 | Media | Toda la tarjeta clickeable + flecha animada en hover |
| ✏️ | | | |

---

## 7. Estructura sugerida del PDF (máx. 10 slides)

1. Portada — nombre, rol, URL del sitio.
2. Usuario objetivo — proto-persona + escenario.
3. Benchmark — tabla de 3 portfolios.
4. Concepto — 3 palabras + moodboard.
5. Arquitectura — sitemap + resultado del card sorting.
6. Wireframes — mobile y desktop.
7. Design system — paleta, tipografía, componentes.
8. Test de usabilidad — tareas y hallazgos.
9. Cambios aplicados + **comparación Figma vs sitio** (2 secciones lado a lado).
10. Resultado — captura Lighthouse mobile + links (sitio, repo, Figma).
