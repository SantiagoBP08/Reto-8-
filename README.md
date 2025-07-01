# RETO #8
Desarrolle la mayoría de los ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_08 en slack.

## 1. De los retos anteriores selecciona 3 funciones y escribelas en forma de lambdas.

funcion 1:

    # Función factorial en forma de lambda usando recursión (Reto #6, punto 4)
    
    factorial_lambda = lambda n: 1 if n <= 1 else n * factorial_lambda(n - 1)

    # Ejemplo de uso
    if __name__ == "__main__":
        n = int(input("Ingrese un número natural: "))
        print(f"El factorial de {n} es: {factorial_lambda(n)}")
        
funcion 2:

    import math

    # Función lambda para calcular el perímetro (Reto #5, punto 2)
    
    calcular_perimetro_lambda = lambda r, a, b: (2 * a) + b + (2 * math.pi * r)

    # Ejemplo de uso
    if __name__ == "__main__":
        r = float(input("Ingrese el radio (r): "))
        a = float(input("Ingrese la altura (a): "))
        b = float(input("Ingrese la base (b): "))
        perimetro = calcular_perimetro_lambda(r, a, b)
        print(f"El perímetro total de la figura es: {perimetro}")

funcion 3:

    # Función lambda para determinar si un número es par (Reto #6, punto 2)
    es_par = lambda x: x % 2 == 0

    # Ejemplo de uso
    if __name__ == "__main__":
        numero = int(input("Ingrese un número: "))
        if es_par(numero):
            print(f"El número {numero} es par.")
        else:
            print(f"El número {numero} es impar.")


## 2. De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).

funcion 1: Función para calcular el perímetro (Reto #5, punto 2)

    import math

    def calcular_perimetro_args(*args):
        """
        Calcula el perímetro usando los valores en *args: (r, a, b).
        """
        if len(args) < 3:
            return "Faltan parámetros: se necesitan r, a, b."
        r, a, b = args[0], args[1], args[2]
        return 2 * a + b + 2 * math.pi * r

    # Ejemplo de uso
    if __name__ == "__main__":
        print(calcular_perimetro_args(3, 4, 5))  # Calcula el perímetro
        print(calcular_perimetro_args(3, 4))     # Faltan parámetros

funcion 2: Función factorial usando recursión (Reto #6, punto 4)

    def factorial_args(*args):
        """
        Calcula el factorial del primer número ingresado en *args.
        """
        if len(args) < 1:
            return "No se proporcionó ningún número."
        n = args[0]
        factorial = 1
        while n > 1:
            factorial *= n
            n -= 1
        return factorial

    # Ejemplo de uso
    if __name__ == "__main__":
        print(factorial_args(5))  # 120
        print(factorial_args())   # No se proporcionó ningún número.
    
funcion 3: Función para determinar si un número es par (Reto #6, punto 2)

    def es_par_args(*args):
    """
    Determina si el primer número ingresado en *args es par.
    """
    if len(args) < 1:
        return "No se proporcionó ningún número."
    return args[0] % 2 == 0

    # Ejemplo de uso
    if __name__ == "__main__":
        print(es_par_args(4))  # True
        print(es_par_args(7))  # False

## 3. Escriba una función recursiva para calcular la operación de la potencia.

    def potencia_recursiva(base, exponente):
        if exponente == 0:
            return 1  # Caso base
        elif exponente < 0:
            return 1 / potencia_recursiva(base, -exponente)  # Manejo de exponentes negativos
        return base * potencia_recursiva(base, exponente - 1)  # Caso recursivo

    # Ejemplo de uso
    if __name__ == "__main__":
        base = float(input("Ingrese la base: "))
        exponente = int(input("Ingrese el exponente: "))
        resultado = potencia_recursiva(base, exponente)
        print(f"{base}^{exponente} = {resultado}")

## 4. Utilice la siguiente plantilla de código para contar el tiempo:

    import time

    # Fibonacci iterativo
    def fibonacci_iterativo(n):
        if n <= 1:
            return n
        a, b = 0, 1
        for _ in range(n - 1):
            a, b = b, a + b
        return b

    # Fibonacci recursivo
    def fibonacci_recursivo(n):
        if n <= 1:
            return n
        return fibonacci_recursivo(n - 1) + fibonacci_recursivo(n - 2)

    # Comparar tiempos
    if __name__ == "__main__":
        num = int(input("Ingrese el número de Fibonacci: "))

        # Tiempo iterativo
        start_time = time.time()
        iter_result = fibonacci_iterativo(num)
        iter_time = time.time() - start_time
        print(f"Fibonacci iterativo (n={num}): {iter_result}, tiempo: {iter_time:.6f} segundos")

        # Tiempo recursivo
        start_time = time.time()
        rec_result = fibonacci_recursivo(num)
        rec_time = time.time() - start_time
        print(f"Fibonacci recursivo (n={num}): {rec_result}, tiempo: {rec_time:.6f} segundos")

        # Diferencia de tiempo
        print(f"Diferencia de tiempo: {rec_time - iter_time:.6f} segundos")

## 5. Crear cuenta en stackoverflow y adjuntar imagen en el repositorio
![1c8d733b-288e-449f-9174-2c4fb51aa520](https://github.com/user-attachments/assets/c6be4015-5482-4f6c-883e-bcf41cc25f46)

## 6. Cosas de adultos....ir a linkedin y crear perfil....NO IMPORTA que estén iniciando, si tienen tiempo para redes poco útiles como fb, insta, o tiktok tienen tiempo para crear un perfil mamalón. Dejar enlace en el repositorio.

enlace: https://www.linkedin.com/in/brandon-santiago-barriga-penaloza-092379372/

Aca terminariamos con el reto 8, Gracias.
