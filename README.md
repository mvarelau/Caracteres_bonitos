# Caracteres_bonitos
### Reto 12
## Punto 1
1. **`endswith(suffix[, start[, end]])`**:
   - Devuelve `True` si mi cadena termina con el pedazo que le digo; si no, me lanza un `False`.

2. **`startswith(prefix[, start[, end]])`**:
   - Si mi cadena comienza con lo que le indico, me devuelve `True`; si no, me suelta un `False`.

3. **`isalpha()`**:
   - Me dice si toda mi cadena está formada solo por letras y no está vacía. Si es así, me devuelve un optimista `True`; si no, me baja el ánimo con un `False`.

4. **`isalnum()`**:
   - Revisa si todos mis caracteres son alfanuméricos (letras o números) y además, que mi cadena no esté vacía. Si todo está en orden, me aplaude con un `True`; de lo contrario, me señala el error con un `False`.

5. **`isdigit()`**:
   - Indaga si todos mis caracteres son números y, claro, que la cadena no esté vacía. Si cumple ambos requisitos, me dice que sí con un `True`; si algo falla, me niega con un `False`.

6. **`isspace()`**:
   - Comprueba si mi cadena solo tiene espacios en blanco y no está vacía. Si es así, me lanza un entusiasta `True`; de lo contrario, me desanima con un `False`.

7. **`istitle()`**:
   - Me confirma si mi cadena es un título, es decir, si todas las palabras comienzan con mayúsculas y el resto de las letras son minúsculas. Si mi cadena tiene esa elegancia, me celebra con un `True`; si no, me corrige con un humilde `False`.

8. **`islower()`**:
   - Revisa si todos los caracteres de mi cadena son minúsculas y, claro, que mi cadena no esté vacía. Si todo es pequeño, me sonríe con un `True`; si hay algo en mayúsculas, me pone en mi lugar con un `False`.

9. **`isupper()`**:
   - Verifica si todos mis caracteres son mayúsculas y que mi cadena no esté vacía. Si todo está gritando, me grita de vuelta con un `True`; si hay algo susurrando, me calla con un `False`.

## Punto 2
Para procesar el archivo de usa un ```open``` y se inicializa una variable para leerlo y posteriormente lo convierto en un string para poderlo procesar como tal. Se hace un conteo de las vocales una por unac on la función ```string.count()```
```python
file = open('romeo.txt')
string=str(file.read())
a=string.count("a")
e=string.count("e")
i=string.count("i")
o=string.count("o")
u=string.count("u")
print(a,e,i,o,u)
```
Ahora lo mismo pero con las consonantes:
```python
b = cadena.count("b")
c = cadena.count("c")
d = cadena.count("d")
f = cadena.count("f")
g = cadena.count("g")
h = cadena.count("h")
j = cadena.count("j")
k = cadena.count("k")
l = cadena.count("l")
m = cadena.count("m")
n = cadena.count("n")
p = cadena.count("p")
q = cadena.count("q")
r = cadena.count("r")
s = cadena.count("s")
t = cadena.count("t")
v = cadena.count("v")
w = cadena.count("w")
x = cadena.count("x")
y = cadena.count("y")
z = cadena.count("z")
print(b, c, d, f, g, h, j, k, l, m, n, p, q, r, s, t, v, w, x, y, z)
```
Para contar la frecuencia de las palabras se utiliza una libreria llamada collections, esta puede identificar las palabras que más se repiten, dependiendo de cuantas se le indiquen.
```python

import collections

def palabras_repetidas(archivo):

    with open(archivo, "r") as file:
        texto = file.read()
        palabras = texto.split()# e agreagn las palabras a una lista 

        contador = collections.Counter(palabras)
        for palabra, veces in contador.most_common(50):#most_comon es una función que hace la cuenta de las palabras más comunes 
            print(f"La palabra '{palabra}' se repite {veces} veces.")


if __name__ == "__main__":
    palabras_repetidas("romeo.txt")

```

