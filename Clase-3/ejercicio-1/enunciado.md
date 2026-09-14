# Ejercicio 1 — Arreglar los tamaños

Esta página tiene **siete problemas de tamaño**. Están marcados con un número en `estilos.css`.

**No toques `index.html`.**

| # | Qué está mal | Pista |
|---|---|---|
| 1 | `width` + `max-width` para una sola idea | `min(a, b)` devuelve el más chico |
| 2 | `height: 100vh` en el hero | Dos arreglos en una línea: `min-height`, y `svh` |
| 3 | `font-size: 42px` en el título | `clamp()`, entre `1.75rem` y `3rem` |
| 4 | `clamp(1.05rem, --texto-grande, 1.35rem)` | Le falta algo para ser un valor |
| 5 | Tres `font-size` en `px` | `rem` |
| 6 | `clamp(2.5rem, 2vw, 1.4rem)` | Leelo en voz alta: mínimo, preferido, máximo |
| 7 | `width: 100vw` en la lista | Mirá la barra de abajo del navegador |

## Cómo saber si está bien

- **A 375 px no se puede arrastrar la página para el costado.**
- Arrastrás el ancho de 320 a 1600 y el título **se mueve y se frena** en los dos extremos.
- El subtítulo también se mueve. (Si no se mueve, el problema 6 sigue ahí.)
- La bajada es más grande que el texto normal. (Si no, el problema 4 sigue ahí.)

## Para los tres `clamp()`

El preferido casi siempre es `Xrem + Yvw`:

- la parte en **`rem`** escucha al **usuario** (el tamaño de letra del sistema),
- la parte en **`vw`** escucha a la **pantalla**.

Sólo con `vw`, si el usuario agranda la letra, no pasa nada.

## Verificar

```bash
bin/verificar-maquetado.py materias/interaccion-moviles/clases/clase-03/ejercicios/01-fluido
```

## Si terminaste antes

Poné el tamaño de fuente de Chrome en "Muy grande" (Configuración → Apariencia → Tamaño de fuente —
**no** es el zoom) y recargá. Si hiciste todo bien, la página crece entera y sigue entrando.
