---
title: Análisis de galerías — Prompt + Respuesta
---

Prompt (original):

Teniendo en cuenta mis líneas de diseño y decisiones técnicas descritas en `project-brief.md` y `project-inspiration.md` (y respetando los tokens de `assets/css/_variables.css`), analiza estos 5 portfolios de ilustradores [https://postcards.mono.studio/
https://www.bigdirty.agency/
https://www.orlionstudio.com/
https://www.joyzhong.com/
https://adriannehuang.format.com/].

Para cada uno, evalúa:

1. Diseño Visual (Awwwards criteria)
   - Estética general (1-10)
   - Tipografía y jerarquía
   - Uso de color y contraste
   - Composición y espaciado

2. UX de Galería
   - Facilidad para explorar proyectos
   - Claridad de navegación
   - Información por proyecto (título, descripción, tags)
   - Call-to-actions efectivos

3. Técnica
   - Tipo de layout (grid, masonry, custom)
   - Responsive behavior
   - Performance (carga de imágenes)
   - Micro-interacciones

4. Insights Accionables (aplicables a mi brief)
   - 3 patrones que puedo reutilizar sin copiar (con explicación)
   - 3 riesgos/antipatrones a evitar (con explicación)
   - 2 decisiones concretas para mi galería (layout + contenido), justificadas con mi `project-brief.md`

Devuelve:
- Tabla comparativa (Diseño / UX / Técnica)
- “Decisiones para mi proyecto” (bullets)
- Checklist de verificación (qué revisar al implementarlo)

---

Respuesta completa (análisis):

Resumen breve
- Sitios analizados: Postcards (mono.studio), BigDirty (bigdirty.agency), Orlion Studio, Joy Zhong, Adrianne Huang (Format).
- Objetivo: identificar patrones transferibles para tu portafolio de ilustración respetando accesibilidad, mobile-first y tokens CSS.

Análisis por sitio

1) Postcards — https://postcards.mono.studio/
- Diseño Visual (6/10): estética moderna y experimental; tipografía grande y escultórica; contraste variable (algunas composiciones con bajo contraste). Espaciado generoso pero juego de capas puede sentirse denso.
- UX de Galería: navegación narrativa más que lista; exploración curiosa pero no siempre clara la entrada a cada proyecto; pocos metadatos visibles por tarjeta; CTAs implícitos (clic imagen para abrir).
- Técnica: layout custom / canvas-like; comportamiento responsive adaptativo; posible uso intensivo de JS (puede sufrir en performance); micro-interacciones ricas (hover/entradas animadas).
- Insights accionables:
  - Patrones reuse: 1) Entrada por imagen grande que invita a ‘tocar’ el proyecto; 2) Micro-animaciones al hover para dar vida; 3) Transiciones entre estados que conectan miniaturas y detalles.
  - Riesgos: 1) Depender de JS pesado — afecta accesibilidad y performance; 2) contrastes bajos en capas — incumple WCAG; 3) navegación poco clara para usuarios que buscan info rápida.
  - Decisiones (mi brief): Layout: tarjeta hero por proyecto en grid asimétrico (masonry ligero) para destacar piezas fuertes. Contenido: mostrar título + rol + 1 línea de descripción en la tarjeta; respetar alt y etiquetas accesibles.

2) BigDirty — https://www.bigdirty.agency/
- Diseño Visual (8/10): tipografía contundente, voz de marca fuerte; buen uso de imágenes y espacio; color con contraste alto en textos principales.
- UX de Galería: estructura tipo case-by-case (cada sección comunica proceso y precio); navegación directa hacia contacto; cada proyecto tiene buen contexto cuando se explora.
- Técnica: layout clásico en columnas con secciones verticales; responsive consistente; imágenes optimizadas en CDN; micro-interacciones sutiles (entradas y CTAs visibles).
- Insights accionables:
  - Patrones reuse: 1) Jerarquía tipográfica clara para separar título/proceso/resultados; 2) CTA visible y persistente (contacto/book a call); 3) Secciones de proceso breve dentro del case study.
  - Riesgos: 1) Si todo es muy marcado, puede restar foco a la obra visual; 2) Precios y procesos muy visibles — no siempre deseable en portafolio público; 3) Uso de imágenes grandes sin placeholder puede penalizar LCP.
  - Decisiones (mi brief): Layout: grid con filas modulares y una CTA fija (ej. “Ver proyecto / Contactar”) en el header. Contenido: incluir breve proceso y precio opcional en fichas de proyecto según tipo de encargo.

3) Orlion Studio — https://www.orlionstudio.com/
- Diseño Visual (7/10): paleta vibrante y composición orientada a objetos; tipografía coherente; buen equilibrio entre tienda y portfolio.
- UX de Galería: explorable, con links rápidos a piezas y shop; navegación híbrida shop/portfolio puede confundir, pero facilita conversión (compra de prints).
- Técnica: grid simple con quick-views; responsive sólido; performance variable según many product images; micro-interactions en quick view y hover.
- Insights accionables:
  - Patrones reuse: 1) CTA de compra/print integrado al portfolio (si vendes prints); 2) Quick-view para ver info sin salir de la galería; 3) Categorías/tags visibles para filtrar.
  - Riesgos: 1) Mezclar e-commerce y portafolio puede desviar atención creativa; 2) Filtros confusos si no están bien etiquetados; 3) Imágenes sin lazy-loading pueden penalizar performance.
  - Decisiones (mi brief): Layout: grid con quick-view modal y filtro por tipo/tags. Contenido: añadir tags y una línea de contexto (cliente/encargo/rol) para cada pieza.

4) Joy Zhong — https://www.joyzhong.com/
- Diseño Visual (8/10): estética limpia y alegre; tipografía cuidada y jerarquía clara; paleta suave y contrastes bien trabajados.
- UX de Galería: navegación clara, proyectos listados con enlaces directos a estudios de caso; buena separación entre hero copy y trabajos; CTAs discretos pero presentes.
- Técnica: grid modular y secciones con animaciones ligeras; buen responsive; uso eficiente de GIFs/AVIF para animaciones pequeñas; micro-interactions limpias.
- Insights accionables:
  - Patrones reuse: 1) Hero + grid de proyectos con entradas directas; 2) Micro-copy que contextualiza cada trabajo; 3) Animaciones ligeras que no comprometen accesibilidad.
  - Riesgos: 1) Demasiadas animaciones pequeñas pueden saturar si no son sutiles; 2) Dependencia de formatos no compatibles en navegadores antiguos; 3) Contenido insuficiente por proyecto si solo hay imágenes.
  - Decisiones (mi brief): Layout: card grid con hero introductorio y filtrado por tema. Contenido: por tarjeta mostrar título, resumen 1 línea, tags y enlace a case-study con proceso y resultados.

5) Adrianne Huang (Format) — https://adriannehuang.format.com/
- Diseño Visual (7/10): formato de portafolio tradicional; foco en obra con poco ruido; tipografía neutra.
- UX de Galería: navegación directa a proyectos; información compacta; ideal para portfolios fotográficos/series ilustrativas.
- Técnica: layout grid clásico; responsive y optimizado por la plataforma (Format); lazy-loading y versiones optimizadas de imagen.
- Insights accionables:
  - Patrones reuse: 1) Presentación minimal que deja protagonismo a la imagen; 2) Navegación por colección/serie; 3) Uso de plantillas para acelerar publicación.
  - Riesgos: 1) Exceso de minimalismo puede dejar usuario sin contexto; 2) Falta de llamadas a la acción (contratar/contactar); 3) Dependencia de plataforma limita personalización.
  - Decisiones (mi brief): Layout: grid minimal con foco en grandes imágenes, pero añado overlays con metadatos accesibles. Contenido: proyecto con galería de imágenes + texto contextual y link de contacto visible.

Comparativa rápida (tabla resumida)

| Sitio | Diseño (1-10) | UX de Galería (1-5) | Técnica (layout) |
|---|---:|---:|---|
| Postcards | 6 | 3 | Custom / canvas-like (JS pesado)
| BigDirty | 8 | 4 | Column/section-based, CDN images
| Orlion Studio | 7 | 4 | Grid + quick-view, shop integrations
| Joy Zhong | 8 | 5 | Modular grid, lightweight animations
| Adrianne Huang | 7 | 4 | Platform grid (Format), lazy-loading

Decisiones para tu proyecto (resumen justificadas con `project-brief.md`)
- Layout: Grid modular responsive (mobile-first) con tarjetas que muestran imagen principal, título, rol y una línea de descripción; añadir quick-view/modal para ver más sin abandonar la galería. Justificación: encaja con tu objetivo de mostrar trabajos para clientes, facilita exploración rápida y respeta la estrategia mobile-first y accesibilidad.
- Contenido: Cada tarjeta debe incluir: título, rol/cliente, año, 1–2 líneas de contexto y tags; la página de proyecto mostrará proceso (breve), 3–6 imágenes optimizadas y call-to-action para contacto. Justificación: ofrece suficiente contexto para clientes, alinea con las metas de accesibilidad y estructura semántica en `project-brief.md`.

Checklist de verificación (implementación)
- Mobile-first: las tarjetas deben adaptarse a una columna en móvil y 2–3 columnas en tablet/desktop.
- Accesibilidad: roles ARIA, teclado para navegar la galería, focus states visibles, `alt` en todas las imágenes.
- Performance: lazy-loading, tamaños `srcset`, generar AVIF/WebP y placeholders LQIP.
- Diseño consistente: usar tokens en `assets/css/_variables.css` para color/espaciado/typografía.
- Contenido por tarjeta: título, rol, 1 línea de resumen, tags.
- CTA: botón visible para ver case study y botón de contacto persistente en header/footer.
- Micro-interactions: animaciones sutiles y preferiblemente CSS-first; reducir animaciones JS pesadas.

Notas finales
- Evita copiar estéticas; extrae patrones (jerarquía tipográfica, CTAs persistentes, quick-view) y adáptalos a tu voz y tokens CSS.

---

Fin del análisis.
