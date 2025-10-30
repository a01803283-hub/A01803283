# Datos
temperaturas = [20, 22, 19, 25, 23, 18, 21]
dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"]

# a. Temperatura media
suma_temp = sum(temperaturas)
cant_dias = len(temperaturas)
temp_media = suma_temp / cant_dias

print("Temperatura promedio:", temp_media)

# b. Días por arriba o por debajo de la media
print("Comparación con la media:")
i = 0
for temp in temperaturas:
    dia = dias[i]
    if temp > temp_media:
        print(dia, "es mas alta.")
    if temp < temp_media:
        print(dia, "es mas baja.")
    else:
        print(dia, "sigue igual.")
    i = i + 1

# Datos
estudiantes = ["Leonel", "Rodri", "Diego", "Alex", "Pedro", "Lucho"]
promedios = [95.5, 78.0, 62.5, 88.0, 50.0, 70.0]
NOTA_APROBATORIA = 70.0

# a. Promedio general
suma_proms = sum(promedios)
total_alumnos = len(estudiantes)
promedio_general = suma_proms / total_alumnos
print("\nPromedio general:", promedio_general)

# b. Porcentaje de aprobados
aprobados_contador = 0
for prom in promedios:
    if prom >= NOTA_APROBATORIA:
        aprobados_contador = aprobados_contador + 1

porcentaje_aprobados = (aprobados_contador / total_alumnos) * 100
print("Porcentaje de aprobados:", porcentaje_aprobados, "%")

# c. Lista de reprobados
reprobados = []
j = 0
for prom in promedios:
    if prom < NOTA_APROBATORIA:
        reprobados.append(estudiantes[j])
    j = j + 1

print("Reprobados:", reprobados)

# Datos
articulos = ["Leche", "Huevos", "Pan", "lubricante", "condones"]
comprado = [False, True, False, False, False]

print("\n Lista de Compras")

# a. Desplegar artículos no comprados (y guardar su posición)
pendientes = []
indices = []
k = 0
for estado in comprado:
    if estado == False:
        pendientes.append(articulos[k])
        indices.append(k)
    k = k + 1

print("Artículos que te faltan:", pendientes)

# b. y c. Preguntar y actualizar
if len(pendientes) > 0:
    p = 0
    for articulo_pendiente in pendientes:
        indice_original = indices[p]
        respuesta = input("¿Ya compraste " + articulo_pendiente + "? (S/N): ").lower()

        if respuesta == 's':
            comprado[indice_original] = True
            print(articulo_pendiente, "marcado como comprado.")
        p = p + 1

print("\n Lo que compraste", comprado)
