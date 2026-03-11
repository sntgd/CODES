# CODES
Python Process
# Nivel 1 - Funciones sin parámetros ni retorno
import random

def edad():
    edad_usuario = input("Ingresa tu edad: ")
    print("Tu edad es:", edad_usuario, "años")


def suma():
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
    resultado = num1 + num2
    print("La suma es:", resultado)


def num_aleatorio():
    numero = random.randint(1, 100)
    
    while True:
        intento = int(input("Adivina el número entre 1 y 100: "))
        
        if intento < numero:
            print("El número es mayor")
        elif intento > numero:
            print("El número es menor")
        else:
            print("¡Felicitaciones, adivinaste el número!")
            break


def contador_vocales():
    cadena = input("Ingresa una cadena: ")
    vocales = "aeiouAEIOU"
    contador = 0

    for letra in cadena:
        if letra in vocales:
            contador += 1

    return contador



edad()
suma()
num_aleatorio()

v = contador_vocales()
print("Número de vocales:", v)

-------------------------------
# Nivel 2 - Funciones con parámetros, pero sin retorno
def palindromo(palabra):
    palabra = palabra.lower()  
    if palabra == palabra[::-1]:
        return True
    else:
        return False


def calcular_potencia(base, exponente):
    resultado = base ** exponente
    print("El resultado es:", resultado)


def calcular_media(lista):
    media = sum(lista) / len(lista)
    print("La media es:", media)


print(palindromo("reconocer"))  
print(palindromo("python")) 



calcular_potencia(2, 3) 

calcular_media([10, 20, 30, 40]) 

-------------------------------------
# Nivel 3 - Funciones con parámetros y retorno
import math

def invertir_cadena(cadena):
    return cadena[::-1]


def mayor_de_tres_numeros(numero1, numero2, numero3):
    return max(numero1, numero2, numero3)


def calcular_area(radio, altura):
    area = 2 * math.pi * radio * altura + 2 * math.pi * radio**2
    return area


def buscar_palabra(cadena, palabra):
    if palabra in cadena:
        return True
    else:
        return False


print(invertir_cadena("Hola"))  

print(mayor_de_tres_numeros(10, 25, 7))  

print(calcular_area(3, 5))  

print(buscar_palabra("Me gusta programar en Python", "Python"))

-----------------------------------------------------------------
# Nivel 4 - Funciones con múltiples parámetros y retorno
def promedio(*numeros):
    return sum(numeros) / len(numeros)


def multiplicar_lista(lista, numero):
    nueva_lista = []
    for elemento in lista:
        nueva_lista.append(elemento * numero)
    return nueva_lista


def mayor_de_varios_numeros(*numeros):
    return max(numeros)


def calcular_mediana(*numeros):
    lista = sorted(numeros)
    n = len(lista)

    if n % 2 == 1:
        return lista[n // 2]
    else:
        return (lista[n // 2 - 1] + lista[n // 2]) / 2


def contar_ocurrencias(cadena, palabra):
    return cadena.count(palabra)


print(promedio(10, 20, 30, 40))  

print(multiplicar_lista([1, 2, 3, 4], 2))  

print(mayor_de_varios_numeros(5, 12, 8, 20, 3))  

print(calcular_mediana(1, 3, 5, 7, 9))  
print(calcular_mediana(1, 3, 5, 7))     

print(contar_ocurrencias("hola hola mundo hola", "hola"))

------------------------------------------------------------
# Taller de Atributos y Metodos 
# GATO
class Animal:
    def __init__(self, nombre, especie, edad, color):
        self.nombre = nombre
        self.especie = especie
        self.edad = edad
        self.color = color

    def hacer_sonido(self):
        print(self.nombre, "está haciendo un sonido.")

    def mostrar_info(self):
        print(self.nombre, self.especie, self.edad, self.color)


gato = Animal("Michi", "Felino", 2, "Negro")

gato.hacer_sonido()
gato.mostrar_info()
# VEHICULOS

class Vehiculo:
    def __init__(self, marca, modelo, color, velocidad):
        self.marca = marca
        self.modelo = modelo
        self.color = color
        self.velocidad = velocidad

    def acelerar(self):
        print("La moto está acelerando")

    def frenar(self):
        print("La moto está frenando")


moto = Vehiculo("Yamaha", "R15", "Azul", 180)

moto.acelerar()
moto.frenar()

-----------------------------------------

carro = Vehiculo("Toyota", "Corolla", "Rojo", 200)

carro.acelerar()
carro.frenar()

----------------------------------------------------
# COMIDA
class Comida:
    def __init__(self, nombre, pais, calorias, precio):
        self.nombre = nombre
        self.pais = pais
        self.calorias = calorias
        self.precio = precio

    def servir(self):
        print("Sirviendo", self.nombre)

    def mostrar_precio(self):
        print("Precio:", self.precio)


bandeja_paisa = Comida("Bandeja Paisa", "Colombia", 1200, 25000)

-----------------------------------------------------------------

# ARBOL 
class Arbol:
    def __init__(self, tipo, altura, edad, color):
        self.tipo = tipo
        self.altura = altura
        self.edad = edad
        self.color = color

    def crecer(self):
        print("El árbol está creciendo")

    def dar_sombra(self):
        print("El árbol da sombra")


pino = Arbol("Pino", 10, 5, "Verde")

------------------------------------------------------

# LIBRO
class Libro:
    def __init__(self, titulo, autor, paginas, genero):
        self.titulo = titulo
        self.autor = autor
        self.paginas = paginas
        self.genero = genero

    def leer(self):
        print("Leyendo", self.titulo)

    def informacion(self):
        print(self.titulo, self.autor)


novela = Libro("Cien años de soledad", "Gabriel Garcia Marquez", 400, "Novela")

