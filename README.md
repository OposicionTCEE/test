# Test (primer ejercicio)

Banco de preguntas del test de la oposición TCEE, clasificadas por tema del **tercer ejercicio**.
Lo usa la pestaña **Test** del Panel Oposición (extensión de VS Code en el repositorio `main`).
Se descarga y sincroniza junto a `main`, `temario` y `progreso` con la tarea *Sincronizar*.

## Contenido

- `preguntas.json`: un único fichero con todas las preguntas.
- `img/`: las imágenes que usan algunas preguntas.

```json
{
  "puntuacion": { "acierto": 1, "error": -0.3333, "blanco": 0 },
  "examenes": [ { "nombre": "Examen oficial de marzo de 2025 - OEP 2024 - Modelo A", "fecha": "2025-03", "preguntas": 46 } ],
  "preguntas": [
    {
      "id": "3B2601",
      "tema": "3.B.26",
      "enunciado": "… (las fórmulas van entre \\( … \\))",
      "opciones": [ { "id": "A", "text": "…" }, { "id": "B", "text": "…" }, { "id": "C", "text": "…" }, { "id": "D", "text": "…" } ],
      "correctas": ["D"],
      "tipo": "single | multi",
      "examen": "Examen oficial de enero de 2020 - OEP 2019",
      "numero": 33,
      "fecha": "2020-01",
      "imagen": "img/….png | null",
      "imagen_falta": true,
      "justificacion": ""
    }
  ]
}
```

- `tipo: "multi"`: hay que marcar todas las correctas, y solo ellas.
- `imagen_falta: true`: la pregunta usa una imagen que no está en `img/`. El panel avisa de ello.
- `justificacion`: queda vacía mientras no se escriba. Si se rellena, el panel la muestra al corregir.

Las respuestas que das en el panel **no se guardan aquí**, sino en el repositorio privado `progreso` (`progreso/test/<Mac>.json`).

## Estado (4 de octubre de 2026)

- 595 preguntas de 88 temas, procedentes de 13 exámenes oficiales (2011–2025).
  En cada examen solo están las preguntas clasificadas en un tema del tercer ejercicio: no son exámenes completos.
- Sin preguntas: 3.A.1 y 3.A.15.
- Faltan 14 de las 16 imágenes, las que eran `.webp`.

## Añadir o corregir preguntas

Pídeselo a Claude Code, que debe:
1. Respetar el formato de arriba.
2. Mantener los `id` existentes, porque el historial de respuestas depende de ellos.
3. Comprobar que cada letra de `correctas` existe en `opciones`.
