# ClassicNeuralNets-AssociativeMemory: Hopfield, LAM y BAM para el Reconocimiento de Letras del Alfabeto Latino bajo Ruido y Variación de Funciones de Activación

Este proyecto explora el uso de **redes neuronales asociativas** para el reconocimiento y recuperación de patrones en condiciones con y sin ruido. Se implementaron y evaluaron diferentes arquitecturas (Hopfield, LAM y BAM) con funciones de activación simétrica y asimétrica, midiendo su robustez frente a perturbaciones internas y externas.  

---

## Objetivos
- Implementar y analizar redes neuronales asociativas clásicas.  
- Evaluar el desempeño de las redes frente a distintos niveles y tipos de ruido.  
- Comparar la robustez y exactitud de cada arquitectura bajo condiciones controladas.  

---

## Arquitecturas Implementadas
1. **Red de Hopfield**  
   - Funciones de activación: simétrica y asimétrica.  
   - Se analizó la recuperación de patrones en condiciones con ruido bajo y alto.  

2. **Red LAM (Linear Associative Memory)**  
   - Funciones de activación: simétrica y asimétrica.  
   - Evaluada con ruido inducido y ruido de forma.  

3. **Red BAM (Bidirectional Associative Memory)**  
   - Funciones de activación: simétrica y asimétrica.  
   - Entrenamiento y pruebas con diferentes perturbaciones.  

---

## Principales Experimentos
- **Sin ruido**: se midió la capacidad de memorizar y recuperar patrones almacenados.  
- **Ruido inducido**: factores de aleatoriedad de **0.2** y **0.75**.  
- **Ruido de forma**: alteraciones estructurales externas a los patrones.  

---

## Resultados Destacados
- **Hopfield**  
  - Función simétrica: alto desempeño con ruido bajo/alto.  
  - Función asimétrica: resultados ineficientes (salidas saturadas).  

- **LAM**  
  - Escalón asimétrico: **100% de exactitud** en entrenamiento sin ruido y con ruido inducido.  
  - Escalón simétrico: **0% de exactitud**, convergiendo siempre a un único patrón saturado.  

- **BAM**  
  - Escalón simétrico: **100% de exactitud** en entrenamiento y ruido inducido.  
  - Escalón asimétrico: **0% de exactitud**, con salidas saturadas en vectores de unos.  

---

## Análisis Comparativo
- Las **perturbaciones internas** (ruido inducido) fueron toleradas exitosamente por LAM y BAM con activación asimétrica/simétrica respectivamente.  
- Las **perturbaciones externas** (ruido de forma) redujeron drásticamente la exactitud al **25%**, mostrando la vulnerabilidad de ambas redes a cambios estructurales en los patrones.  
- Se observaron casos de **saturación**:
  - LAM simétrica: convergencia a un único patrón dominante.  
  - BAM asimétrica: salidas uniformes de unos.  

---

## Conclusiones
- La robustez de las redes asociativas depende fuertemente del **tipo de activación** y del **tipo de perturbación**.  
- **LAM con activación asimétrica** y **BAM con activación simétrica** mostraron los mejores resultados en condiciones de ruido interno.  
- Ninguna de las arquitecturas evaluadas resultó efectiva frente a **ruido externo estructural**, lo que plantea oportunidades de mejora para aplicaciones en escenarios reales.  

---

## Tecnologías 
Se emplearon las siguientes librerías y versiones de Python:
- **Python 3.11.13** 
- **NumPy** → operaciones matemáticas y manejo de arreglos.  
- **Matplotlib** → visualización de datos.  
- **cv2** → carga y procesamiento de imágenes.  

---

## Autores
- Ing. Alyson Melissa Sánchez Serratos
- Ing. Miguel Ángel Pérez Ávila

---
 ## Ejecución
1. Clonar este repositorio para visualizar los notebooks de jupyter con las implementaciones y el reporte presentado:  
   ```bash
   git clone https://github.com/TGMAPA/ClassicNeuralNets-AssociativeMemory.git
   cd ClassicNeuralNets-AssociativeMemory
