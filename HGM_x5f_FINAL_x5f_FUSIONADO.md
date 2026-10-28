# HGM — Hilos Geométricos Métricos con Eje Central

**Autor:** Jeampierre Aveiga (Guayaquil, EC)  
**Fecha de esta versión:** 28 de octubre de 2026  
**Estado:** Marco geométrico y computacional experimental.  
**Licencia:** MIT  
**Nota de autoría:** Texto ordenado con ayuda de IA (Meta AI y ChatGPT) para claridad, concepto original del eje central HGM y acumulación que genera métrica 4D es del autor.

---

## Resumen

HGM es un marco experimental que estoy desarrollando para representar y estudiar estructuras geométricas mediante hilos.

La idea central que propongo es:
- Existe un **Hilo Geométrico Métrico (HGM)** que funciona como **eje central / columna vertebral**.
- Alrededor de ese eje se acumula una **red de hilos 1D**.
- La **métrica 4D del espacio-tiempo** emergería de la acumulación: densidad, orientación y trenzado de los hilos alrededor del eje central.

  Idea formal (hipótesis de trabajo):
  g_μν(x) = η_μν + ∫ K(x - X_i(s)) * T_ij(s) ds
  Donde K es kernel de acumulación y T_ij es orientación del hilo.

El objetivo es desarrollar una representación tridimensional eficiente que permita estudiar relaciones métricas, deformaciones y, en etapas posteriores, posibles aplicaciones a modelización de espacio-tiempo.

---

## Fundamento Conceptual

HGM representa estructuras geométricas mediante hilos cuyos puntos y relaciones permiten estudiar la geometría.

Elementos centrales:
1.  **Hilo como unidad 1D:** Representado en coordenadas 3D como X(s), con curvatura y torsión calculables.
2.  **Eje Central HGM:** Variante arquitectónica principal. El eje central ordena causalidad y sirve como backbone. La red de hilos se organiza a su alrededor.
3.  **Acumulación que genera 4D:** La métrica no se impone, emerge del promedio ponderado de hilos alrededor del eje (densidad + orientación + trenza).

Las variantes arquitectónicas, incluido el modelo con eje central, se identifican explícitamente como parte de este documento.

---

## Estado de Desarrollo

- Implementación en Python con herramientas de construcción geométrica: B-Splines (scipy), KDE para acumulación, integración RK45 (tolerancia 1e-8), numba para performance.
- Experimentos iniciales: 1 hilo orbitando, 2 hilos interactuando.
- Objetivo a corto plazo (6-8 semanas): Maya estable de 100 hilos.

**Aclaración importante:** La validación de una estructura geométrica no implica, por sí misma, la validación de un modelo físico relativista completo. Las pruebas geométricas deben acompañarse de condiciones, tolerancias y limitaciones.

---

## Objetivos de Investigación / Tests de Vida o Muerte

Se investigará si HGM puede:

1.  **Recuperar límites conocidos:** N hilos random -> espacio plano (Minkowski). N hilos apretados -> Schwarzschild (1 - 2M/r).
2.  **Propagar ondas a c:** Una perturbación en la maya debe viajar a c isotrópico.
3.  **Conservar energía:** Cruce de hilos no debe crear energía.
4.  **Regularizar alta curvatura (hipótesis):** Se explorará si la densidad de hilos alrededor del eje satura a valor finito en regiones de alta curvatura, evitando divergencia a infinito sin necesidad de excisión (como hace SXS). Cuestión abierta.
5.  **Memoria geométrica (hipótesis):** Se investigará si la red guarda deformación finita tras paso de onda (efecto memoria BMS). Cuestión abierta.
6.  **Entropía y información (hipótesis):** Se explorará si la información puede almacenarse como patrón topológico de trenzado alrededor del eje HGM. La resolución de la paradoja de información de Hawking es una cuestión abierta que requiere formulación y comparación con resultados establecidos. No se afirma como resuelta.

---

## Eficiencia y Motivación

Los simuladores actuales de Relatividad General completa (SXS Collaboration, Spectral Einstein Code - SpEC) requieren supercomputadoras y semanas para 2 agujeros negros (mismatch mediano entre resoluciones 4e-4). Wolfram Physics Project (hipergrafo) y LQG (spin networks) proponen espacio tejido pero sin eje central y con arquitectura all-to-all muy pesada.

HGM propone arquitectura con eje central que reduce complejidad de O(N^3) a O(N), con objetivo de permitir simulación de fusión de 3 agujeros negros + supermasivo en PC de gama alta en <1 día. No se presenta como reemplazo de GR, sino como método numérico complementario de bajo costo para exploración rápida.

---

## Reproducibilidad y Atribución

- Cada versión identificará cambios, resultados verificables y contribuciones.
- Código, definiciones matemáticas, experimentos e hipótesis se distinguen claramente.
- Este documento registra la descripción de HGM que el autor presenta en la fecha indicada; no implica que todas las propiedades físicas propuestas hayan sido demostradas. Las propiedades 4, 5 y 6 son hipótesis de trabajo.

**Contacto:** Jeampierre Aveiga - Guayaquil, EC - 2026

MIT License - Cualquiera puede usar, modificar y citar manteniendo autoría original.
