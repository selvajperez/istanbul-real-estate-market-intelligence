# Real Estate Market Intelligence — Istanbul 2026

Análisis exploratorio del mercado inmobiliario de Estambul orientado a identificar diferencias de valor entre distritos y barrios, analizar posibles drivers del precio por m² y detectar micro-mercados que merecen una investigación más profunda.

El proyecto combina **Python para exploración y validación de datos** con **Power BI para análisis interactivo y visualización**.

## 🎯 Objetivo

Transformar un dataset de aproximadamente **25.000 propiedades** en un caso de Market Intelligence capaz de responder:

- ¿Cómo varía el precio por m² entre distritos y barrios?
- ¿Qué características de las propiedades están asociadas con diferencias de valor?
- ¿Cómo se relacionan antigüedad y precio por m²?
- ¿Qué barrios se encuentran por debajo o por encima de la referencia de su distrito?

El objetivo no es predecir precios ni afirmar que una propiedad es una oportunidad de inversión, sino identificar patrones y candidatos que puedan orientar análisis posteriores.

## 🔎 Exploración y calidad de datos

Antes de construir el dashboard se realizó una etapa exploratoria para evaluar:

- volumen y variedad de variables;
- métricas disponibles;
- posibilidades de segmentación;
- relaciones entre variables;
- potencial analítico del dataset;
- calidad y consistencia de los campos.

Durante la preparación se detectaron variables que requerían normalización de escala y se conservaron los valores originales, creando campos corregidos para el análisis.

También se identificaron variables con problemas de calidad o valores atípicos que no fueron utilizadas como drivers principales hasta poder validarlas adecuadamente.

## 📊 Dashboard

El reporte final se organizó en **tres páginas**.

### 1. Overview

Vista ejecutiva del mercado:

- ~25.000 propiedades
- precio mediano
- precio por m² mediano
- comparación del precio por m² entre distritos

Permite obtener rápidamente una lectura general de la estructura geográfica del mercado.

![Overview](dashboard/01-Overview.png)

### 2. Market Explorer

Página interactiva para explorar micro-mercados y posibles drivers de valor.

Incluye:

- **583 barrios**
- antigüedad mediana
- análisis de antigüedad vs. precio por m²
- tamaño de burbuja como indicador de oferta
- condición del edificio
- tipo de calefacción
- pertenencia a complejo residencial
- segmentación por distrito

El objetivo es explorar cómo diferentes características y localizaciones se relacionan con el valor unitario de las propiedades.

![Market Explorer](dashboard/02-Market-Explorer.png)

### 3. Opportunities

Compara cada barrio con la referencia de precio por m² de su propio distrito.

El análisis identificó:

- **270 barrios bajo la referencia**
- **313 barrios sobre la referencia**

Se presentan rankings de los barrios con mayores desvíos negativos y positivos.

Estos resultados se interpretan como **candidatos para investigación**, no como propiedades automáticamente infravaloradas o sobrevaloradas.

![Opportunities](dashboard/03-Opportunities.png)

## 💡 Hallazgos

El análisis permitió observar:

- diferencias importantes de precio por m² entre distritos;
- una elevada granularidad geográfica, con 583 barrios;
- patrones diferenciados según antigüedad y características del edificio;
- segmentos con distintos niveles de precio según condición y sistemas de calefacción;
- barrios cuyo precio por m² se desvía considerablemente de la referencia de su distrito.

La comparación barrio–distrito permite pasar de una lectura general del mercado a una lógica de **micro-market intelligence**.

## ⚠️ Limitaciones

Los desvíos respecto del precio del distrito no representan por sí solos oportunidades de inversión.

Factores como estado, antigüedad, superficie, ubicación específica y calidad de los datos deben considerarse antes de realizar una valoración inmobiliaria.

Además, algunas variables presentan datos faltantes o inconsistencias, por lo que fueron excluidas o utilizadas con cautela.

## 🛠️ Herramientas

- Python
- Pandas
- Jupyter / Google Colab
- Power BI
- DAX
- Power Query
- Git / GitHub

## 📁 Estructura

- `analysis/` — análisis exploratorio en Python
- `dashboard/` — capturas y PDF del dashboard
- `data/` — información sobre la fuente de datos

## 👩‍💻 Autor

**Selva J. Pérez — WildSoft**

Proyecto desarrollado como caso de portfolio de **Data Analytics & Business Intelligence**.# istanbul-real-estate-market-intelligence
