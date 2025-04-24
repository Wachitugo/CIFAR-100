# CIFAR-100
# 🧠 Clasificación de Imágenes con CIFAR-100 y Redes Neuronales

Este repositorio presenta un proyecto de clasificación de imágenes basado en el conjunto de datos **CIFAR-100**, utilizando un modelo de **Perceptrón Multicapa (MLP)** desarrollado con **TensorFlow/Keras**.

---

## 📊 Sobre el Proyecto

**CIFAR-100** es un dataset ampliamente utilizado en tareas de visión por computadora, compuesto por **60,000 imágenes a color de 32x32 píxeles**, organizadas en **100 clases distintas**.  
Este proyecto implementa un clasificador basado en MLP, incluyendo técnicas de regularización y optimización para mejorar el rendimiento.

---

## 🧠 Arquitectura del Modelo

El modelo está compuesto por las siguientes capas y técnicas:

- **Normalización por lotes** en la capa de entrada  
- **Capas densas** con activación **GELU**:
  - Primera capa: 800 unidades
  - Segunda capa: 600 unidades
- **Regularización**:
  - L2 (λ = 1e-3) en ambas capas
  - Dropout: 0.6 (primera capa), 0.3 (segunda capa)
- **Capa de salida**: activación **Softmax** para clasificación multiclase

---

## 🚀 Rendimiento del Modelo

- **Precisión en entrenamiento**: 43.38%  
- **Precisión en validación**: 31.20%

A pesar de usar una arquitectura MLP (en lugar de CNNs) y trabajar con imágenes de baja resolución, el modelo logra resultados competitivos gracias a una cuidadosa configuración y ajuste.

---

## 📁 Estructura del Repositorio

CIFAR-100/
├── data/
│   ├── meta/
│   │   └── meta
│   ├── test/
│   │   └── test
│   ├── train/
│   │   └── train
│   ├── .gitkeep
│   └── cifar-100-python.tar.gz
├── env/
├── notebook/
│   ├── .ipynb_checkpoints/
│   │   ├── CIFAR_100_DEFINITIVO.ipynb
│   │   ├── CIFAR-checkpoint.ipynb
│   │   
│   ├── .gitignore
│   ├── README.md
│   └── requirements.txt

---

## 🔍 Análisis y Conclusiones

El análisis del rendimiento del modelo ofrece los siguientes puntos clave:

- 📉 **Sobreajuste moderado**: Se observa una diferencia de ~12 puntos porcentuales entre la precisión en entrenamiento y validación.
- ✅ **Buena calibración**: El modelo muestra alta confianza en predicciones correctas, lo que indica una calibración adecuada.
- 🎯 **Desafíos inherentes al dataset**: La gran cantidad de clases (100) y la similitud visual entre muchas de ellas hacen que la clasificación sea especialmente compleja.

---

## 🚀 Posibles Mejoras

Algunas líneas futuras de trabajo y mejora del modelo incluyen:

- 🧱 Implementar arquitecturas **CNN** adaptadas específicamente para visión por computadora.
- 🔄 Aplicar **data augmentation** para mejorar la generalización del modelo.
- 🧠 Utilizar **transfer learning** con modelos preentrenados en datasets grandes.
- ⚙️ Experimentar con otros optimizadores como **Adam** o **RMSprop**.
- 🤝 Implementar técnicas de **ensamblado de modelos** para combinar múltiples clasificadores.

---

## 📚 Referencias

- [CIFAR-100 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)  
- Regularización en Deep Learning  
- Arquitecturas CNN para Clasificación de Imágenes

