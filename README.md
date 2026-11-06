# IA – Predicción de rotación de personal

Proyecto de Machine Learning para **Superior Cleaning Services**: estima, al cierre de cada mes, la probabilidad de que cada colaborador activo deje la empresa en los **próximos 3 meses**, usando el historial de planillas 2016–2025 (datos anonimizados).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guzmanjmanuel/IA_prediccionDeRotacion/blob/main/notebooks/prediccion_rotacion.ipynb)

## Estructura
| Ruta | Contenido |
|---|---|
| `data/planillas_2016_2025_limpio.csv.gz` | Planillas limpias y anonimizadas (513,813 registros, CSV comprimido) |
| `notebooks/prediccion_rotacion.ipynb` | Notebook completo: problema, dataset, limpieza, preprocesamiento, modelos, métricas y respuestas |

## Resultados (prueba 2023 – jun 2025)
| Modelo | ROC‑AUC | PR‑AUC | F1 | Captura top 10 % |
|---|---|---|---|---|
| Iteración 1: Regresión logística | 0.676 | 0.162 | 0.242 | 21.0 % |
| Iteración 2: Gradient Boosting + variables ampliadas | **0.694** | **0.177** | **0.261** | **23.9 %** |

## Ejecutar en Colab
El notebook descarga el CSV directamente de este repositorio.
- **Repositorio público:** no requiere configuración.
- **Repositorio privado:** en Colab, abre 🔑 *Secretos*, crea `GITHUB_TOKEN` con un token de GitHub (permiso de lectura de contenido del repo) y habilita el acceso al notebook.
