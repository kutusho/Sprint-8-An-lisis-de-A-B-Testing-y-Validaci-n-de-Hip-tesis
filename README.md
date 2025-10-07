# Sprint 8 – Análisis de A/B Testing y Validación de Hipótesis

## 📄 Descripción
Proyecto correspondiente al **Sprint 8 del Bootcamp de Data Analytics – TripleTen**, centrado en la **validación estadística de hipótesis** mediante **pruebas A/B**.  
El objetivo fue determinar si una **nueva versión de una página web o producto digital** incrementa las conversiones respecto al diseño actual, aplicando métodos de prueba estadística y visualización analítica.

---

## 🎯 Objetivo
Comprobar, con base en evidencia estadística, si las diferencias observadas entre los grupos A y B son significativas y pueden atribuirse al cambio implementado, en lugar del azar.

---

## 🧩 Contexto del caso
Una compañía digital ejecutó un experimento A/B para evaluar una nueva versión de su proceso de compra.  
Los grupos fueron:
- **Grupo A:** versión original del flujo de compra.  
- **Grupo B:** versión mejorada con ajustes en la interfaz y nuevos elementos de confianza.

Los datos contienen información sobre visitantes, conversiones y tráfico dividido equitativamente entre los grupos.

---

## 🧠 Metodología

1. **Preparación de datos**
   - Limpieza y verificación de consistencia (duplicados, valores nulos, conversión de tipos).  
   - Verificación de tamaño muestral y balance entre grupos.  

2. **Definición de hipótesis**
   - H₀ : no existe diferencia significativa en la tasa de conversión.  
   - H₁ : la tasa de conversión del grupo B es mayor que la del A.  

3. **Cálculos y pruebas**
   - Cálculo de la **tasa de conversión** = `orders / visitors`.  
   - Prueba de hipótesis mediante **t-test de Welch** (p < 0.05 → rechazo de H₀).  
   - Validación de supuestos: normalidad (Shapiro–Wilk) y homogeneidad de varianzas (Levene).  

4. **Visualización**
   - Histogramas y boxplots comparativos de tasas de conversión.  
   - Distribución de diferencias y cálculo del intervalo de confianza al 95 %.

---

## 📊 Resultados principales
- **Grupo A:** tasa de conversión = 4.35 %.  
- **Grupo B:** tasa de conversión = 5.02 %.  
- **p-value = 0.013 < 0.05** → la diferencia es estadísticamente significativa.  
- Intervalo de confianza [0.004 – 0.012] confirma una mejora real de conversión.  
- Conclusión: la versión B mejora la conversión en ~15 % frente a la A.

---

## 📈 Conclusiones
El experimento A/B demostró de forma cuantitativa que la modificación propuesta impacta positivamente en la conversión.  
La metodología estadística aplicada garantiza que las decisiones de negocio se basen en evidencia y no en percepciones subjetivas.  
Se recomienda desplegar la versión B y continuar monitoreando resultados en cohortes mensuales.

---

## 🧰 Herramientas y tecnologías
- **Python:** pandas · numpy · scipy · matplotlib · seaborn  
- **Análisis:** A/B Testing, Welch t-test, intervalos de confianza, EDA  
- **Visualización:** comparativas y distribuciones  
- **Entorno:** Jupyter Notebook / Google Colab  
- **Control de versiones:** Git · GitHub

---
