# Ejercicio entregable del TP 4

## Contexto

Elon Musk decide abrir su taller espacial para permitirle a las familias que puedan ir a conocerlo. Luego de abierta la inscripción, 5000 familias se anotan para realizar la visita. Debido a la gran demanda de público decide establecer un número de 100 días durante los cuales aceptará visitas. Sabiendo que el taller tiene una capacidad diaria acotada (de 340 personas), Elon debe distribuir a los visitantes durante los 100 días. Para esto, solicita a cada familia que le informe 8 días (en orden de preferencia) en los cuales preferirían realizar la visita, y cuántas personas conforman el grupo familiar.

Por ejemplo, la familia Pérez tiene 3 miembros, y sus preferencias son [33, 25, 10, 62, 48, 53, 66, 78]. El día 33 es el día preferido para los Perez, de no ser posible ir el 33, el segundo día preferido es el 25, y así sucesivamente. 

Dado que no todas las personas podrán asistir el día que prefieren, Elon decide crear un bono compensatorio para las familias que no son asignadas al día que eligieron como prioritario.

Elon nos pide que diseñemos un programa que permita determinar qué familias deberán ser invitadas en cada uno de los 100 días para minimizar el monto total de los bonos compensatorios, considerando que: todas las familias deben poder visitar el taller en alguno de los 8 días que indicaron como preferidos, y cada familia será invitada un único día.

## Datos de entrada

Se anotaron 5000 familias para visitar el taller, cada una eligió entre 8 días de los disponibles en el orden en que prefieren realizar la visita.

Se sabe que el taller estará abierto 100 días consecutivos y que la disponibilidad diaria es de 340 personas.

El bono compensatorio se aplica únicamente a la familia que no es asignada en el primer día elegido como prioritario y se calcula utilizando la siguiente fórmula:

`bono = U$S 25 + (U$S 10 * Grupo Familiar) + (U$S 5 * Dia asignado)`

## Características de la solución

Se considera válida a una solución si:

1. No supera el tope de capacidad diaria para ninguno de los días disponibles.

1. Cada familia es asignada a un único día para realizar la visita.

1. Todas las familias son asignadas para realizar la visita en algunos de sus días preferidos.


Se considera óptima a una solución si:

1. Es una solución válida.

1. Se consigue obtener el mínimo costo total del bono compensatorio.


Se sabe que, para el caso de prueba provisto, el mínimo costo total del bono compensatorio es 29035.

## Consigna

1. Implementar un programa que obtenga una solución válida al problema planteado, resultando en el cronograma de familias por día y calcule el monto total a disponer en bonos compensatorios.

1. Realizar un proceso que, a partir de una solución válida, intente mejorar esa solución mediante alguna transformación local cuyo costo computacional no supere una función cuadrática - O (N^2).

1. Realizar un breve informe que contenga: 

    1. Las ideas que se consideraron para obtener una solución válida (incluyendo aquellas que fueron descartando en el proceso).

    1. Una explicación del algoritmo que se utilizó para obtener una solución válida, justificando su elección.

    1. Las transformaciones aplicadas a la solución válida, justificando su elección.