# fase5resultadoanalisisdedatos
desarrollar un algoritmo de detección de fraudes en transacciones financieras con una precisión superior al 98

# Algoritmo de detección de fraudes en transacciones financieras

# Datos de ejemplo: montos de transacciones
montos = [50, 100, 150, 200, 250, 500, 1000, 1500, 2000]

# Calcular la media y la desviación estándar de los montos
media = sum(montos) / len(montos)
desviacion_estandar = (sum((monto - media) ** 2 for monto in montos) / len(montos)) ** 0.5

# Definir el umbral de detección basado en la desviación estándar
umbral_desviacion = 2 * desviacion_estandar  # Umbral de 2 desviaciones estándar

# Identificar transacciones sospechosas
transacciones_sospechosas = []
for monto in montos:
    if abs(monto - media) > umbral_desviacion:
        transacciones_sospechosas.append(monto)

# Mostrar las transacciones sospechosas
print("Transacciones sospechosas:")
for transaccion in transacciones_sospechosas:
    print(transaccion)

