# Temperaturas
# Crear matriz 3D: [ciudad][semana][día]
# Ejemplo: 2 ciudades, 2 semanas, 7 días por semana

temperaturas = [
    [   # Ciudad 1
        [22, 24, 21, 23, 25, 26, 24],   # Semana 1
        [23, 25, 22, 24, 26, 27, 25]    # Semana 2
    ],
    [   # Ciudad 2
        [18, 19, 20, 21, 19, 18, 20],   # Semana 1
        [21, 22, 23, 20, 22, 21, 19]    # Semana 2
    ]
]

ciudades = ["Quito", "Guayaquil"]
dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"]

# Calcular promedio por ciudad y semana con bucles anidados
for i in range(len(temperaturas)):  # Recorrer ciudades
    print(f"\nPromedios de temperatura en {ciudades[i]}:")
    for j in range(len(temperaturas[i])):  # Recorrer semanas
        suma = 0
        for k in range(len(temperaturas[i][j])):  # Recorrer días
            suma += temperaturas[i][j][k]
        
        promedio = suma / len(temperaturas[i][j])
        print(f"  Semana {j+1}: {promedio:.2f} °C")


