# reto-8
# 3 funciones con lambda
    # 1. Verificar si un número entero es código ASCII de una vocal minúscula
    es_vocal_ascii = lambda n: chr(n) in "aeiou"

    # Ejemplos:
    print("Ejercicio 1: ¿El número 97 es ASCII de una vocal minúscula?", es_vocal_ascii(97))  # True ('a')
    print("Ejercicio 1: ¿El número 98 es ASCII de una vocal minúscula?", es_vocal_ascii(98))  # False ('b')

# Función factorial en forma de lambda usando recursión (Reto #6, punto 4)

    factorial_lambda = lambda n: 1 if n <= 1 else n * factorial_lambda(n - 1)

    # Ejemplo de uso
    if __name__ == "__main__":
        n = int(input("Ingrese un número natural: "))
        print(f"El factorial de {n} es: {factorial_lambda(n)}")

# Determinar si un número es positivo, negativo o cero.
    es_positivo = lambda x: x > 0
    es_negativo = lambda x: x < 0
    es_cero = lambda x: x == 0
    
  # Area de un triangulo.
    area_triangulo = lambda b, h: (b * h) / 2
    base = float(input("Ingrese la base: "))
    altura = float(input("Ingrese la altura: "))
    print(f"Área del triángulo: {area_triangulo(base, altura)}")
# argumentos no definidos (3 funciones)
 # "Escriba un programa que pida 5 números reales y calcule la el promedio, el promedio multiplicativo,v y la raíz cúbica del menor número." La función utilizada fué la siguiente
     def promedio(a, b, c, d, e):
        return (a + b + c + d + e) / 5

# Funcion recursiva para pontencia

    def potencia(base: int, exponente: int) -> int:
        if exponente == 0:
            return 1
        else:
            return base * potencia(base, exponente - 1)

  # Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo
    def triangulo(*args):
        if len(args) != 3:
            return False
        a, b, c = args
        return a + b > c and a + c > b and b + c > a

    if __name__ == "__main__":
        a = int(input("Ingrese el primer lado: "))
        b = int(input("Ingrese el segundo lado: "))
        c = int(input("Ingrese el tercer lado: "))
    
        if triangulo(a, b, c):
            print("Con estos lados sí se puede formar un triángulo.")
        else:
            print("Con estos lados no se puede formar un triángulo.")
