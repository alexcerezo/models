# models — Prueba práctica de GitHub Models

## Resumen

Este repositorio contiene una prueba práctica (testing/demo) basada en la documentación y herramientas de GitHub Models. No es un repositorio de iniciación: es el registro de una serie de experimentos y verificaciones realizadas por el autor.

Fecha de la prueba: 2025-11-10

Archivo principal usado: `models-demo.yml`

## Qué se hizo (lista de comprobación)

- Crear el prompt "summarizer" (prompt summarizer) y verificar su salida.
- Editar el prompt para introducir datos de prueba (test data) y añadir evaluadores que midan la calidad de la salida.
- Instalar la extensión de modelos `gh-models` en GitHub CLI y confirmar su funcionamiento.
- Ejecutar un prompt mediante la GitHub CLI y validar la respuesta del modelo.
- Crear, editar, aplicar y borrar un preset (ejemplos de presets y gestión básica).
- Creación y uso de variables en presets/prompts.
- Comparar diferentes modelos usando una lista de prompts para evaluar consistencia y calidad.
- Documentar y explicar el uso de evaluators (evaluadores) y cómo se usaron en la prueba.
- Anotar que las GitHub Copilot Extensions han quedado deprecadas en este contexto y ajustar flujos en consecuencia.
- Implementar un ejemplo de GitHub Actions que resume el contenido de un issue usando el prompt summarizer.

## Propósito

Registrar los pasos y artefactos generados durante la prueba para poder reproducirlos y evaluarlos. Los resultados permiten comparar modelos, verificar presets y validar flujos automatizados (Actions/CLI).

## Cómo reproducir / verificar rápidamente

1. Abrir `models-demo.yml` para revisar los prompts, presets y variables usados.
2. Instalar la extensión de modelos en GitHub CLI (si no está instalada):
	- `gh extension install <gh-models-extension>` (ver documentación local/instalador si aplica).
3. Ejecutar uno de los prompts del `models-demo.yml` mediante la CLI y comprobar la salida.
4. Revisar los evaluadores incluidos: ejecutar con datos de prueba y revisar métricas/resultados.
5. Revisar el ejemplo de GitHub Actions (carpeta `.github/workflows/` si existe) que resume un issue; disparar la Action o ejecutar localmente con act/runner si es necesario.

Notas: algunos pasos requieren credenciales (tokens) y acceso a servicios externos. No se incluyen secretos en este repositorio.

## Observaciones y decisiones importantes

- La prueba incluye comparaciones entre modelos para una lista de prompts específicos; los resultados y notas de observación deberían guardarse como artefactos o en subcarpetas para análisis posteriores.
- Las GitHub Copilot Extensions se han deprecado para algunos flujos; se documentó el impacto y se ajustaron ejemplos hacia el uso directo de `gh-models` y Actions.

## Archivos relevantes

- `models-demo.yml` — fichero principal con prompts, presets y variables usados durante la prueba.
- `.github/workflows/` — (opcional) ejemplo de GitHub Action que resume un issue.

