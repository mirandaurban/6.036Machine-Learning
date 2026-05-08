# Álgebra lineal

## Vectores

Un vector es un objeto matemático con:

- magnitud
- dirección



**Representación en Python**

```python
import numpy as np

v = np.array([1, 2, 3])
```



Un vector puede representar:

- una posición
- una dirección
- características de un dato
- embeddings
- inputs de un modelo



Ejemplo:

```python
# Representación de las características de un usuario a manera de vector
usuario = np.array([
    edad,
    altura,
    horas_ejercicio
])
```



### Conceptos importantes

#### Dimensión

Cantidad de elementos del vector.

```python
v = np.array([1, 2, 3])

# dimensión = 3
```

#### Magnitud

Tamaño o longitud del vector.

Fórmula:

\[
||v|| = \sqrt{x_1^2 + x_2^2 + ... + x_n^2}
\]

Ejemplo:

```python
v = np.array([3, 4])

magnitud = np.linalg.norm(v)

print(magnitud)
# 5
```

#### Dirección

Describe hacia dónde apunta el vector.

Dos vectores pueden tener:
- misma dirección
- distinta magnitud

### Operaciones básicas

#### Suma de vectores

```python
a = np.array([1, 2])
b = np.array([3, 4])

resultado = a + b

print(resultado)
# [4 6]
```

#### Multiplicación por escalar

```python
v = np.array([1, 2])

resultado = v * 3

print(resultado)
# [3 6]
```

#### Producto punto

Mide relación o similitud entre vectores. También puede interpretarse como:

- combinación ponderada
- score
- proyección

**Fórmula**
\[
a \cdot b = \sum_i a_i b_i
\]

**Representación manual**

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

resultado = (
    1 * 4 +
    2 * 5 +
    3 * 6
)

print(resultado)
# 32
```

**Representación en programación**

```python
resultado = np.dot(a, b)

print(resultado)
# 32
```

---

# Matrices

Una matriz es una colección organizada de números.

Puede verse como:
- tabla de datos
- conjunto de vectores
- transformación matemática

**Representación en Python**

```python
A = np.array([
    [1, 2],
    [3, 4]
])
```

## Conceptos importantes

### Dimensiones

Las matrices tienen:

- filas
- columnas

Ejemplo:

```python
A.shape
# (2, 2)
# O sea, 2 filas y 2 columnas
```

### Filas vs columnas

En ML normalmente:

- filas = ejemplos/datos
- columnas = features/características

Ejemplo:

| Edad | Altura | Peso |
| ---- | ------ | ---- |
| 20   | 170    | 65   |
| 25   | 180    | 80   |

** filas = personas
** columnas = características

## Operaciones básicas

### Multiplicación matricial

Combina información entre matrices. Una **regla importante**, el número de columnas de la primera matriz debe ser igual al número de filas de la segunda.

```python
A = np.array([
    [1, 2],
    [3, 4]
])

B = np.array([
    [5],
    [6]
])

resultado = A @ B

print(resultado)

# Resultado
[[17]
 [39]]
```

Puede representar:

- transformación de datos
- combinación de información
- aplicación de pesos
- propagación en redes neuronales

### Transformaciones lineales

Las matrices pueden transformar vectores.

Ejemplos:
- rotar
- escalar
- deformar
- proyectar



# Relación con Machine Learning

Los vectores representan:

- features
- embeddings
- inputs
- pesos

Las matrices representan:

- datasets
- transformaciones
- batches
- parámetros

---

# Ejercicios

## Básicos

- sumar vectores
- calcular magnitud
- implementar producto punto manualmente

---

## Intermedios

- multiplicación matriz-vector
- multiplicación matriz-matriz
- normalizar vectores

---

## Aplicados a ML

- similitud entre usuarios
- mini sistema de recomendación
- representación de dataset como matriz
