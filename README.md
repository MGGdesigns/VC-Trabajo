# Visión por Computador: Trabajo de Curso

### Autores

- [@Mauro Gómez Guillén](https://github.com/MGGdesigns)
- [@Santiago Santana Martínez](https://github.com/Tiago1615)

## Tabla de Contenidos

- [Paquetes necesarios](#paquetes-necesarios)
- [Introducción](#introducción)
- [Funcionalidades](#funcionalidades)
- [Procedimiento](#procedimiento)
- [Resultado](#resultado)
- [Referencias Bibliográficas](#referencias-bibliográficas)

---

## Paquetes necesarios

- **Librerías**:
  - opencv-python
  - mediapipe
  - numpy
  - pynput
  - pygame

```bash
pip install opencv-python
```


```bash
pip install mediapipe
```


```bash
pip install numpy
```

```bash
pip install pynput
```

```bash
pip install pygame
```

## Introducción:
Este proyecto implementa un sistema de seguimiento de articulaciones y control interactivo en tiempo real. Usando MediaPipe para capturar y analizar movimientos del cuerpo, el programa permite la interacción con un entorno virtual a través de gestos, simulando un control avanzado mediante movimientos corporales.

El sistema integra calibración dinámica de movimientos y reacciones en tiempo real, proporcionando un entorno adaptable y accesible para experimentos de interacción hombre-máquina.

---

## Funcionalidades

- **Calibración de Ángulos Corporales:** Calibra ángulos entre puntos clave del cuerpo (nariz, hombros, codos, muñecas, caderas, etc.) en cinco direcciones (frontal, arriba, abajo, derecha e izquierda).
- **Seguimiento en Tiempo Real:** Rastrea articulaciones clave y calcula ángulos dinámicamente para interpretar gestos.
- **Control por Gestos:**
  - **Movimientos Corporales:** Controla acciones virtuales simulando pulsaciones de teclado y clics del ratón.
  - **Gestos Complejos:** Gestos predefinidos, como levantar brazos o mover la cabeza, desencadenan diferentes acciones.
- **Interfaz Gráfica con Indicadores:**
  - Visualización de ángulos calculados con barras de progreso dinámicas.
  - Instrucciones en pantalla adaptativas, como mensajes para comenzar la calibración o salir del programa.
- **Reproducción de Sonidos:** Reproduce sonidos específicos durante la calibración para guiar al usuario.

## Procedimiento

### Flujo del Sistema

- **Inicio y Calibración:**

  - El usuario inicia el sistema y realiza una calibración en cinco direcciones: frontal, arriba, abajo, derecha e izquierda.
  - Los ángulos promedio de cada dirección se almacenan para usarlos como referencia.

- **Seguimiento en Tiempo Real:**

   - Los fotogramas se capturan desde la cámara y se procesan para detectar las posiciones de las articulaciones clave.
   - Los ángulos calculados se comparan con los valores calibrados para interpretar gestos.

- **Control Interactivo:**

  - Basado en los gestos detectados, el programa simula pulsaciones de teclas o movimientos del ratón.
  - Por ejemplo:
    - Brazos hacia arriba: Simula caminar hacia adelante.
    - Cabeza hacia la izquierda o derecha: Controla el movimiento horizontal del ratón.
    - Cabeza hacia arriba o abajo: Controla el movimiento vertical del ratón.

- **Indicadores Visuales y de Audio:**

  - Los ángulos calculados se muestran en pantalla junto con barras de progreso y colores que reflejan el estado actual.
  - Sonidos específicos guían al usuario durante la calibración.

## Resultado

El sistema permite una interacción fluida entre movimientos corporales y acciones virtuales. Se puede usar para experimentos de control por gestos o para aplicaciones de accesibilidad.

A continuación, se muestra un vídeo donde se puede ver el sistema en funcionamiento:

[Vídeo](https://drive.google.com/file/d/1iKo10wYJH7Nm5jcZo9w7fywJ7Pk4nWPn/view)

---

## Referencias Bibliográficas

- Documentación
  - [Documentación de MediaPipe](https://mediapipe.readthedocs.io/en/latest/)
  - [Documentación OpenCV](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html)
  - [Documentación de Pynput](https://pynput.readthedocs.io/en/latest/)
  - [Documentación de Pygame](https://www.pygame.org/docs/)
  - [Documentación de la asignatura VC](https://github.com/otsedom/otsedom.github.io/tree/main/VC)
- Sonidos
  - [Sonido de 'OK' (The Notification Email)](https://pixabay.com/sound-effects/search/confirmation/)
  - [Sonido de finalización (Level Passed)](https://pixabay.com/sound-effects/search/confirmation/)
  - [Música de calibración](https://pixabay.com/sound-effects/search/confirmation/)
- Inspiración
  - [Ejemplo de uso similar](https://www.youtube.com/watch?v=nMx1VlgjfBw)
  - [Motivación inicial](https://www.youtube.com/watch?v=y4wu-DnhQZ4)

---