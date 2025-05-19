# Funciones Intermedias 

#### 1. Actualizar valores en diccionarios y listas
~~~
matriz = [ [10, 15, 20], [3, 7, 14] ]
cantantes = [
    {"nombre": "Ricky Martin", "pais": "Puerto Rico"},
    {"nombre": "Chayanne", "pais": "Puerto Rico"}
]
ciudades = {
    "México": ["Ciudad de México", "Guadalajara", "Cancún"],
    "Chile": ["Santiago", "Concepción", "Viña del Mar"]
}
coordenadas = [
    {"latitud": 8.2588997, "longitud": -84.9399704}
]
~~~
'''
Cambia el valor de 3 en matriz por 6. Una vez realizado el cambio tu matriz debería ser: [ [10, 15, 20], [6, 7, 14] ]
Cambia el nombre del primer cantante de “Ricky Martin” a “Enrique Martin Morales”
En ciudades, cambia “Cancún” por “Monterrey”
En las coordenadas, cambia el valor de “latitud” por 9.9355431

'''
~~~
matriz[1][0] = 6
print(matriz)
print()
cantantes[0]["nombre"] = "Enrique Martin Morales"
print(cantantes)
print()
ciudades["México"][2] = "Monterrey"
print(ciudades)
print()
coordenadas[0]['latitud'] = 9.9355431
print(coordenadas)
~~~
#### 2. Iterar a través de una lista de diccionarios

'''
Crea la función iterarDiccionario(lista) que reciba una lista de diccionarios y recorra cada diccionario de la lista e imprima cada llave y el valor correspondiente. Por ejemplo:

'''
~~~
cantantes = [
    {"nombre": "Ricky Martin", "pais": "Puerto Rico"},
    {"nombre": "Chayanne", "pais": "Puerto Rico"},
    {"nombre": "José José", "pais": "México"},
    {"nombre": "Juan Luis Guerra", "pais": "República Dominicana"}
]

def iterarDiccionario(lista):
    for diccionario in lista:
        salida = []
        for clave, valor in diccionario.items():
            salida.append(f"{clave} - {valor}")
        print(", ".join(salida))
print()
iterarDiccionario(cantantes)
~~~
#Imprime "nombre": "Ricky Martin", "pais": "Puerto Rico" (está bien si lo imprime en líneas separadas)

#BONUS: Que aparezcan en este formato:
'''
nombre - Ricky Martin, pais - Puerto Rico
nombre - Chayanne, pais - Puerto Rico
nombre - José José, pais - México
nombre - Juan Luis Guerra, pais - República Dominicana
'''

#### 3. Obtener valores de una lista de diccionarios
~~~
def iterarDiccionario2(llave, lista):
    for diccionario in lista:
        if llave in diccionario:
            print(diccionario[llave])
        else:
            print(f"La clave '{llave}' no existe en el diccionario.")
print()
iterarDiccionario2("nombre", cantantes)
~~~
'''

Crea la función iterarDiccionario2(llave, lista) que reciba una cadena con el nombre de una llave y una lista de diccionarios. La función debe imprimir el valor almacenado para esa clave de cada diccionario que se encuentra en la lista. Por ejemplo, iterarDiccionario2(“nombre”, cantantes) debe de imprimir:

Ricky Martin
Chayanne
José José
Juan Luis Guerra
'''
print()
iterarDiccionario2("pais", cantantes) 
print()
'''
Otro ejemplo: iterarDiccionario2(“pais”, cantantes) debe de imprimir:

Puerto Rico
Puerto Rico
México
República Dominicana

'''

#### 4. Iterar a través de un diccionario con valores de lista

'''
Crea una función imprimirInformacion(diccionario) que reciba un diccionario en donde los valores son listas. La función debe imprimir el nombre de cada clave junto con el tamaño de su lista y seguido de esto los valores de la lista para esa clave. Por ejemplo:

'''
~~~
costa_rica = {
    "ciudades": ["San José", "Limón", "Cartago", "Puntarenas"],
    "comidas": ["gallo pinto", "casado", "tamales", "chifrijo", "olla de carne"]
}

def imprimirInformacion(diccionario):
    for clave, lista in diccionario.items():
        print(f"{len(lista)} {clave.upper()}")
        for elemento in lista:
            print(elemento)
        print() 

imprimirInformacion(costa_rica)
~~~
'''
##### imprime:
4 CIUDADES
San José
Limón
Cartago
Puntarenas

5 COMIDAS
gallo pinto
casado
tamales
chifrijo
olla de carne
'''
