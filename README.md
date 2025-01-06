#!/bin/bash

# Elimina file1 si existe
rm file1 2>/dev/null

# Define un umbral (aunque en este caso no se usa en el cálculo)
e=22

# Procesa esportistes.csv para calcular el promedio de la columna 4
awk -F, '
BEGIN {
    tot = 0; # Inicializa el acumulador
}
{
    tot += $4; # Suma los valores de la columna 4 (edades)
}
END {
    print "Total = " tot / NR; # Calcula el promedio (suma total / número de registros)
}' esportistes.csv

# Pregunta 1 del control de AWK
