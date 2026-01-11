# Modelado Numérico de Fluidos y Equilibrio Hidrostático

Este repositorio contiene un conjunto de herramientas de simulación desarrolladas en **Python** para la resolución de Ecuaciones Diferenciales Ordinarias (ODEs) aplicadas a fenómenos de transporte y estructuras en equilibrio.

El proyecto se centra en la implementación "from scratch" (sin cajas negras) de integradores numéricos para modelar comportamientos físicos complejos.

## Resumen

El código aborda dos problemas fundamentales de la física computacional con aplicaciones en ingeniería:

1.  **Dinámica de Fluidos (Enfoque Lagrangiano):** Simulación de la evolución temporal y trayectoria de elementos de fluido bajo campos de fuerza externos.
2.  **Estructuras en Equilibrio Hidrostático:** Resolución de la Ecuación de Lane-Emden para modelar perfiles de densidad y presión en sistemas autogravitantes politrópicos (gases/fluidos).

## Características Técnicas

* **Integradores Propios:** Implementación manual de algoritmos **Runge-Kutta de 4to orden (RK4)** y **Heun** para asegurar control total sobre la convergencia y estabilidad numérica.
* **Análisis de Sensibilidad:** Automatización de barridos de parámetros (índice politrópico $n$) para estudiar distintos escenarios físicos.
* **Visualización Interactiva:** Uso de `Matplotlib` e `Ipywidgets` para la generación de gráficos dinámicos y análisis de resultados en tiempo real.
* **Manejo de Singularidades:** Tratamiento numérico robusto para condiciones de borde con divergencia (como en el origen de coordenadas esféricas).

## Lenguaje y librerías

* **Lenguaje:** Python 3.x
* **Cálculo Numérico:** NumPy
* **Visualización:** Matplotlib
* **Matemática Simbólica:** SymPy
* **Interactividad:** Ipywidgets

## Estructura del Código

El notebook principal (`Modelado_Numerico_Fluidos_y_Equilibrio.ipynb`) se divide en:

### Módulo 1: Dinámica Temporal (Método de Heun)
Implementación de un esquema predictor-corrector para resolver ecuaciones de movimiento. Se analizan trayectorias en el espacio de fases y evolución temporal.

### Módulo 2: Equilibrio Hidrostático (Método RK4)
Simulación de la estructura interna de fluidos autogravitantes.
* **Input:** Condiciones iniciales de densidad central y ecuación de estado politrópica.
* **Output:** Perfiles radiales de densidad adimensional ($\theta$) y determinación de la superficie del fluido (radio de anulación de presión).
* **Cálculo de Masa:** Integración numérica para obtener la masa total del sistema en función del índice politrópico.

## Instalación y Ejecución

Para correr este proyecto localmente:

1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/NOMBRE_DEL_REPO.git](https://github.com/TU_USUARIO/NOMBRE_DEL_REPO.git)
   ```
2. Instalar librerías
   ```bash
   pip install numpy matplotlib sympy ipywidgets
   ```

## Resultados destacados:

El simulador permite visualizar cómo la variación del índice politrópico ($n$) afecta la compresibilidad y distribución de masa del fluido, recuperando soluciones analíticas conocidas (como $n=0$, $n=1$, $n=5$) y aproximando soluciones numéricas para casos complejos. Tal como se observa en la siguiente imágen:
<img width="866" height="547" alt="image" src="https://github.com/user-attachments/assets/1d9b2c20-3075-4ce3-977e-66a4f34aae38" />

## Autores:

Luis Alberto Diaz - Estudiante de Ciencias Físicas - FCEyN (UBA)
Facundo Ottero Zappa - Estudiante de Ciencias Físicas - FCEyN (UBA)
