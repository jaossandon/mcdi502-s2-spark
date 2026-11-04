# MCDI502 · Sumativa 2 · Taller I: Apache Spark

**Curso:** MCDI502 Gestión de Datos y Tecnologías Big Data, Magíster en Ciencia de Datos (UNAB)

**Integrantes:** Fernanda Ovalle Román · Sebastián Cajales Cid · César Lorca Bacián · Jorge Álvarez Ossandón

Taller práctico de **RDDs, DataFrames y Spark SQL** con datos históricos de los Juegos Olímpicos (deportistas, equipos, eventos, juegos y resultados).

## Cómo ejecutarlo

1. Abrir [Google Colab](https://colab.research.google.com) → **Archivo → Abrir cuaderno → pestaña GitHub**.
2. Pegar `jaossandon/mcdi502-s2-spark` y elegir `notebooks/mcdi502_s2_grupoX.ipynb`.
3. **Entorno de ejecución → Ejecutar todas.**

El notebook instala Java y Spark y descarga los datos desde este repositorio sin pasos manuales.

## Estructura

```
mcdi502-s2-spark/
├── data/          # datos originales entregados por el profesor (sin modificar)
├── notebooks/     # notebook entregable (mcdi502_s2_grupoX.ipynb)
├── docs/          # resumen de la pauta y guion del video
├── .gitignore
└── README.md
```

## Datos (`data/`)

| Archivo | Contenido | Observación |
|---|---|---|
| `deportista.csv` | deportistas 1 al 67.786 | sin encabezado; 0 = dato faltante en edad/altura/peso |
| `deportista2.csv` | deportistas 67.787 al 135.571 | mismo formato que el anterior |
| `equipo.csv` | id, equipo, sigla | |
| `evento.csv` | cod_evento, evento, deporte_id | 280 líneas entre comillas completas (se leen como texto) |
| `resultados.csv` | resultado_id, medalla, deportista_id, juego_id, evento_id | separado por `;` |
| `juegos.json` | juego_id, ano, temporada, ciudad | `temporada` trae el año y `ciudad` trae Verano/Invierno |

## Contenido del notebook

1. Configuración del entorno (Java, Spark, SparkSession/SparkContext)
2. RDDs: creación y unión (ID 3.1)
3. RDDs: transformaciones (ID 3.2)
4. DataFrames: creación e integración (ID 3.1)
5. Paralelismo (ID 3.4)
6. Inspección del DataFrame (ID 3.1)
7. Columnas calculadas (ID 3.3)
8. Agregaciones (ID 3.3)
9. Conclusiones