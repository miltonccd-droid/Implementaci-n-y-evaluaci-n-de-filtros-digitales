# Implementación y evaluación de filtros digitales

**Autor:** Milton Caballero Diaz

Proyecto académico que genera una señal compuesta con ruido blanco y compara filtros digitales pasa bajos, pasa altos y pasa bandas.

## Requisitos
- Python 3.10 o superior
- NumPy, SciPy y Matplotlib

## Instalación y ejecución
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
pip install -r requirements.txt
python filtros_digitales.py
```

El programa crea la carpeta `resultados/` con las gráficas de la señal de entrada, las salidas filtradas, la respuesta en frecuencia y la comparación espectral.

## Diseño
- Muestreo: 1000 Hz; duración: 2 s.
- Señal útil: componentes de 5, 50 y 180 Hz.
- Ruido: blanco gaussiano, semilla fija 42.
- Filtros IIR Butterworth de orden 4: pasa bajos 30 Hz, pasa altos 100 Hz y pasa bandas 40–70 Hz.
- Se incluye también un ejemplo FIR pasa bajos de 101 coeficientes con ventana Hamming.
- `sosfiltfilt`/`filtfilt` aplican filtrado de fase cero fuera de línea.

## Estructura
- `filtros_digitales.py`: código fuente.
- `resultados/`: gráficas generadas por el programa.
- `informe_actividad.docx`: informe académico.

## Publicación en GitHub
Crea un repositorio vacío y ejecuta:
```bash
git init
git add .
git commit -m "Implementación de filtros digitales"
git branch -M main
git remote add origin https://github.com/USUARIO/REPOSITORIO.git
git push -u origin main
```
Sustituye la URL de ejemplo por la URL de tu repositorio.
