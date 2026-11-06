# Audio Spectrum Lab

Herramientas independientes en Python para prácticas de audio y análisis espectral:

- **Audio Spectrum Analyzer**: análisis de archivos WAV, FFT, picos espectrales,
  estimación de fundamental y armónicos, espectrograma y captura/grabación
  desde una entrada de audio.
- **Audio Signal Generator**: generador auxiliar de señales senoidales,
  cuadradas, triangulares y diente de sierra; permite combinar dos frecuencias
  y guardar el resultado en WAV.
- **samples/**: carpeta para organizar audios de prácticas.

El generador es una herramienta complementaria. El analizador puede utilizarse
de forma independiente con archivos WAV.

## Requisitos

- Windows 10/11 (probado en el entorno de desarrollo con Python 3.12).
- Python 3.10 o posterior recomendado.
- Dependencias indicadas en `requirements.txt`.

## Instalación en Windows

Abre CMD en la carpeta del proyecto y ejecuta:

```bat
py -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Ejecutar el analizador

```bat
python audio_spectrum_analyzer.py
```

## Ejecutar el generador auxiliar

En otra ventana de CMD:

```bat
python audio_signal_generator.py
```

Los dos programas son independientes y pueden ejecutarse simultáneamente.

## Uso básico recomendado

1. Abre el generador y crea una senoide de 1.000 Hz.
2. Guarda la señal como WAV desde el generador.
3. Abre el analizador, carga ese WAV y pulsa **Analizar**.
4. Explora las pestañas de espectro, picos, armónicos y espectrograma.
5. Para análisis en directo, selecciona una entrada de audio disponible en Windows.

La captura en tiempo real depende de los dispositivos, controladores y permisos
de audio del equipo. La función de captura directa del sonido reproducido por
Windows puede requerir una entrada de loopback o una configuración específica
del controlador; no está garantizada en todos los equipos.

## Samples

Copia tus archivos WAV en `samples/`. El programa permite abrir archivos WAV
desde cualquier ubicación. Los audios de terceros solo deben publicarse si
sus licencias permiten redistribución; documenta siempre su procedencia en
`samples/SOURCES.md`.

## Estructura

```text
Audio_Spectrum_Lab/
├── audio_spectrum_analyzer.py
├── audio_signal_generator.py
├── requirements.txt
├── README.md
├── LICENSE
└── samples/
    ├── README.md
    └── SOURCES.md
```

## Estado del proyecto

Versión de cierre del desarrollo: analizador basado en la rama 2.5 y generador 1.0.
Las funciones principales se han desarrollado para uso didáctico. El proyecto
debe probarse en cada equipo antes de utilizarlo en una práctica evaluable.

## Licencia

El código de este proyecto se distribuye bajo la licencia **MIT**. El texto
íntegro está en el archivo `LICENSE` y también puede consultarse desde el menú
**Ayuda > Licencia MIT** de cada aplicación.

Copyright (c) 2026 Santiago Borrero Ortiz.

La licencia MIT se aplica al código del proyecto. No concede automáticamente
derechos sobre archivos WAV, muestras, imágenes, marcas o materiales de terceros
que se añadan a `samples/`. Cada recurso externo debe conservar su propia
licencia y atribución; consulta `samples/SOURCES.md`.
