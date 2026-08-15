# CLAUDE.md

Este archivo guía a Claude (vía Claude Code) en el trabajo sobre este repositorio.
Es un sitio web educativo para el curso **Estadística 1**, donde el profesor aloja
ejercicios y tutoriales que luego comparte con sus estudiantes mediante un enlace.

## Objetivo del proyecto

Crear y mantener una página web **didáctica, intuitiva y sobria** que sirva como
repositorio central de material de estudio de Estadística 1: ejercicios resueltos,
guías paso a paso, tutoriales conceptuales y (opcionalmente) ejercicios interactivos
de autoevaluación.

El público objetivo son **estudiantes universitarios/de pregrado** que acceden al
sitio desde el celular o la laptop para repasar antes de un examen o practicar un tema.

## Principios de diseño (no negociables)

1. **Sobriedad ante todo**: nada de colores estridentes, gradientes llamativos,
   animaciones innecesarias ni "ruido" visual. Paleta reducida (2-3 colores base +
   neutros), tipografía clara, mucho espacio en blanco.
2. **Didáctica primero**: cada ejercicio o tutorial debe tener una estructura
   predecible (ver más abajo). El estudiante nunca debe sentirse perdido.
3. **Intuitiva**: la navegación debe entenderse sin instrucciones. Máximo 2-3
   clics para llegar a cualquier contenido. Menú claro por unidades/temas.
4. **Mobile-first**: muchos estudiantes entrarán desde el celular. Todo debe
   verse bien en pantallas pequeñas.
5. **Contenido matemático legible**: las fórmulas deben renderizarse correctamente
   (usar KaTeX o MathJax), no como imágenes borrosas ni texto plano con símbolos raros.
6. **Carga rápida y sin fricción**: sin login obligatorio, sin popups, sin
   dependencias pesadas. Es un sitio estático que se comparte por link.

## Stack técnico sugerido

- **HTML/CSS/JS estático** (o un generador simple tipo Astro/Eleventy) — no se
  necesita backend ni base de datos, ya que es contenido curado por el profesor.
- **KaTeX** para renderizar notación matemática (más liviano que MathJax).
- Despliegue simple en **GitHub Pages, Netlify o Vercel** (gratuito, un solo enlace
  fijo para compartir con los estudiantes).
- Sin frameworks pesados salvo que el contenido crezca mucho; priorizar simplicidad
  y mantenibilidad por sobre sofisticación técnica.

## Estructura del contenido

Organizar por **unidades temáticas** de Estadística 1, por ejemplo:

1. Estadística descriptiva (medidas de tendencia central y dispersión)
2. Probabilidad básica
3. Variables aleatorias y distribuciones
4. Distribuciones muestrales
5. Estimación (puntual y por intervalos)
6. Introducción a pruebas de hipótesis

Cada **unidad** tiene su propia página/carpeta con:
- Breve introducción teórica (2-3 párrafos, sin sobrecargar)
- Tutorial paso a paso de al menos un ejemplo resuelto
- Lista de ejercicios propuestos, cada uno con:
  - Enunciado claro
  - Nivel de dificultad (básico / intermedio / avanzado)
  - Solución oculta por defecto (desplegable tipo "Ver solución") para fomentar
    que el estudiante intente resolverlo primero

## Estructura de archivos (referencia)

```
/
├── index.html              # Página de inicio con índice de unidades
├── unidades/
│   ├── 01-descriptiva/
│   │   ├── index.html      # Teoría + tutorial
│   │   └── ejercicios.html
│   ├── 02-probabilidad/
│   └── ...
├── assets/
│   ├── css/style.css       # Estilos globales (paleta sobria)
│   └── js/main.js
└── CLAUDE.md
```

## Convenciones de escritura de contenido

- Español neutro, tono cercano pero profesional (como un profesor explicando en clase).
- Usar notación estándar de estadística (con KaTeX): $\bar{x}$, $\sigma$, $H_0$, etc.
- Cada ejercicio resuelto debe mostrar el razonamiento paso a paso, no solo el
  resultado final.
- Evitar jerga innecesaria; cuando se introduzca un término nuevo, definirlo brevemente.

## Qué evitar

- Publicidad, trackers o scripts de terceros no esenciales.
- Diseños "cargados" (muchas tarjetas de colores, iconos decorativos sin función).
- Dependencia de librerías que compliquen el despliegue estático.
- Contenido sin revisar: siempre verificar que las soluciones matemáticas sean
  correctas antes de publicarlas.

## Tareas típicas que se le pedirán a Claude en este repo

- Agregar una nueva unidad temática con su teoría, tutorial y ejercicios.
- Ajustar estilos manteniendo la sobriedad del diseño.
- Mejorar la navegación o el índice general.
- Revisar/corregir el renderizado de fórmulas.
- Optimizar para que se vea bien en celular.

Cuando falte información específica (ej. paleta de colores exacta, nombre del
curso/profesor, número de unidades), Claude debe proponer una opción razonable
y sobria por defecto, en lugar de detener el trabajo pidiendo aclaraciones.
