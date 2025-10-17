# 📸 Análisis y Clasificación de Rostros: Visión por Computador con OpenCV

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)](https://opencv.org/)
[![dlib](https://img.shields.io/badge/dlib-808080?style=flat&logo=python&logoColor=white)](http://dlib.net/python.html)
[![Pillow](https://img.shields.io/badge/Pillow-4A4A4A?style=flat&logo=python&logoColor=white)](https://pillow.readthedocs.io/en/stable/)

Este proyecto aborda el desarrollo de técnicas de **Visión por Computador (Computer Vision)** para el **análisis y clasificación de rostros humanos** utilizando la librería líder **OpenCV**. El enfoque principal es la detección, pre-procesamiento, y clasificación de imágenes faciales, así como la implementación de análisis avanzado de marcos faciales y detección de estado (ej. ojos abiertos/cerrados).

---

## 🎯 Objetivos y Alcance del Proyecto

El proyecto tiene como objetivo principal implementar y evaluar diversas técnicas de clasificación y análisis facial, utilizando una base de datos de rostros (referencia: Georgia Tech Face Database). El alcance incluye:

1.  **Detección Facial:** Uso de OpenCV para localizar rostros dentro de una imagen.
2.  **Pre-procesamiento:** Estandarización de imágenes y división del *dataset*.
3.  **Clasificación:** Implementación de algoritmos tradicionales de reconocimiento facial.
4.  **Análisis Avanzado:** Utilización de `dlib` para la extracción de puntos clave (*landmarks*) del rostro.
5.  **Aplicaciones en Video:** Demostración de las técnicas en captura de video en tiempo real.

---

## 🧠 Metodología y Técnicas Implementadas

### 1. Preparación y Estandarización de Datos
* **Dataset:** Se utilizó como referencia la base de imágenes de **Georgia Tech** (`http://www.anefian.com/research/gt_db.zip`).
* **División del Dataset:** Se implementaron funciones que utilizan las bibliotecas `shutil` y `os` para organizar y dividir la base de datos en conjuntos de entrenamiento y prueba.
* **Estandarización de Imágenes:** Se estandarizaron todas las imágenes a una misma medida, empleando **algoritmos de interpolación** para asegurar la calidad y efectividad del pre-procesamiento.

### 2. Reconocimiento y Clasificación
Se exploraron e implementaron generalidades de algoritmos tradicionales de reconocimiento facial, lo que permitió establecer *benchmarks* de rendimiento:
* **Eigenfaces:** Basado en la descomposición de valores propios.
* **Fisherfaces:** Un enfoque que optimiza la discriminación entre clases.
* **LBPH (Local Binary Patterns Histograms):** Un método que captura la textura local de la imagen.

### 3. Análisis Facial Detallado (Landmarks)
Se utilizó la biblioteca **dlib** para la localización precisa de puntos de referencia en el rostro:
* **Marcos Faciales:** Se obtuvieron los **puntos del rostro humano** (*facial landmarks*).
* **Anotaciones y Medidas:** Con estos puntos, se realizaron **anotaciones** en los rostros y se tomaron medidas específicas.
* **Ratio Ocular (Aspect Ratio):** Se calculó el aspecto de razón de los ojos para determinar la proporción de apertura/cierre, lo que es útil para alimentar bases de datos de aplicaciones de detección de fatiga.

### 4. Aplicación en Tiempo Real
* El proyecto culmina con el establecimiento de una de las aplicaciones más importantes: el **análisis facial en captura de video**.
* Se trabajó con recursos de `io`, `IPython` y la biblioteca **Pillow** para manejar la entrada de video y procesar las imágenes cuadro por cuadro.

---

## 📚 Librerías Clave

| Librería | Uso Principal |
| :--- | :--- |
| **OpenCV (`cv2`)** | Detección facial principal, procesamiento de imágenes y estandarización. |
| **dlib** | Localización de puntos de referencia (*landmarks*) y extracción de características faciales. |
| **Pillow (`PIL`)** | Manejo y procesamiento de imágenes, especialmente en flujos de video. |
| **os / shutil** | Gestión y organización del sistema de archivos, crucial para dividir los datasets. |
| **io / IPython** | Recursos utilizados para la captura y visualización de datos en tiempo real (video). |

---

## 📈 Conclusión del Aprendizaje

El proyecto demostró la versatilidad de **OpenCV y dlib** en tareas de visión por computador, desde la clasificación básica con algoritmos como Eigenfaces hasta el análisis avanzado de la geometría facial en tiempo real. La capacidad de estandarizar y pre-procesar datos de imágenes de manera efectiva es fundamental para obtener *benchmarks* sólidos y modelos de análisis robustos.
