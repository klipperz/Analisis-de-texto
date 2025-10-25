# Análisis Comparativo de Discursos de Posesión Presidencial

Este repositorio contiene un análisis de Procesamiento de Lenguaje Natural (PLN) que compara los discursos de posesión presidencial de **Gustavo Petro (2022)** y **Álvaro Uribe Vélez (2002)**.

El objetivo es diseccionar la retórica y la estructura discursiva de dos momentos y visiones políticas cruciales para Colombia. El problema abordado es cómo las métricas lingüísticas pueden cuantificar las diferencias en el estilo de liderazgo: un discurso centrado en la **movilización social** versus uno centrado en el **orden estatal**.

## Metodología

Para ir más allá de la simple lectura, aplicamos una metodología de minería de texto detallada en el notebook `Text_mining.ipynb`:

1.  **Análisis Estructural (Sin spaCy):** Conteo de palabras, frases y párrafos para establecer la complejidad sintáctica de cada texto.
2.  **Limpieza y Lematización:** Uso de `spaCy` para normalizar los textos, lematizar (obtener la raíz de la palabra) y filtrar *stopwords* (ej. "el", "de", "que").
3.  **Frecuencias Temáticas:** Identificación de los términos más comunes para revelar los conceptos centrales de cada plataforma política.
4.  **Análisis Gramatical (POS Tagging):** Clasificación de palabras por función (sustantivos, verbos, adjetivos) para entender si domina el lenguaje de la **acción**, la **descripción** o la **cosa**.
5.  **Extracción de Tripletas SVO:** Identificación de las relaciones Sujeto-Verbo-Objeto para aislar las afirmaciones y argumentos fundamentales de cada discurso.

## Textos Analizados

* **Discurso 1: Gustavo Petro (2022)**
    * *Fuente:* [Presidencia de la República de Colombia](https://www.presidencia.gov.co/prensa/Paginas/Palabras-del-Presidente-de-la-Republica-Gustavo-Petro-Urrego-al-tomar-220807.aspx#mainContent)

* **Discurso 2: Álvaro Uribe Vélez (2002)**
    * *Fuente:* [Legado Álvaro Uribe](https://www.legadouribe.com/wp-content/uploads/2020/06/Discurso-21.pdf)

## Hallazgos Principales

El análisis cuantitativo revela que las diferencias se concentran en la estructura de la oración y el enfoque léxico.

### 1. Estructura y Densidad Sintáctica

* **Fragmentación similar:** Ambos discursos (Petro: 109 párrafos; Uribe: 96 párrafos) utilizan una alta fragmentación, una técnica retórica común para la oralidad.
* **La diferencia clave:** La complejidad se mide en la **longitud de la frase**.
    * **Petro (15.6 Palabras/Frase):** Estilo ágil, conversacional, prioriza la claridad y la presentación modular de ideas.
    * **Uribe (22.1 Palabras/Frase):** Estilo denso, requiere un mayor uso de subordinación y estructuras complejas para encadenar múltiples argumentos en una misma unidad sintáctica, asemejándose a un informe programático.

### 2. Temas Centrales (Frecuencias)

El léxico dominante define la agenda.

* **Petro:** Se enfoca en `paz`, `vida`, `pueblo`, `sociedad` y `cambio`. El discurso es humanista y de transformación social.
* **Uribe:** Se centra en `seguridad`, `democracia`, `libertad`, `crecimiento` y `Estado`. El foco es institucional, legal y económico.
<img width="790" height="427" alt="Image" src="https://github.com/user-attachments/assets/a541048d-76a6-4646-ae5a-2892739e4152" />
<img width="790" height="427" alt="Image" src="https://github.com/user-attachments/assets/5b96c4fb-07a8-4331-8c27-2ab2ac2293fd" />
### 3. Argumentación (SVO)

La extracción de tripletas SVO confirma la intención comunicativa de cada líder:

* **Petro:** Las afirmaciones son más aspiracionales y filosóficas (ej. centradas en la 'esperanza' como un agente activo).
* **Uribe:** Las afirmaciones son causales y definitorias. El argumento se basa en establecer las condiciones necesarias para el orden (ej. la 'seguridad' subsiste con 'garantías'; el 'periodismo' se ejerce con 'libertad').

## Herramientas Utilizadas

* **re**
* **spaCy**
* **WordCloud** y **Matplotlib**
