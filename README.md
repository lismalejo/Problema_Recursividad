En este problema, dado un conjunto de monedas de diferentes denominaciones y un monto objetivo, se busca determinar de cuántas formas distintas se puede obtener ese monto usando las monedas disponibles.

Descripción del código:
La función cambio_de_moneda toma tres parámetros: monedas (una lista de las denominaciones de monedas disponibles), cantidad (el monto objetivo que se desea obtener) e indice (el índice actual de la lista de monedas que se está considerando).
En el caso base, si la cantidad es 0, significa que se ha encontrado una combinación válida para obtener el monto objetivo, por lo que se devuelve 1.
Si la cantidad es negativa o el índice es mayor o igual a la longitud de la lista de monedas, significa que no hay más monedas disponibles para considerar o que la cantidad no puede ser alcanzada con las monedas disponibles, por lo que se devuelve 0.
En el caso recursivo, se consideran dos opciones: incluir la moneda actual en la combinación y restar su valor a la cantidad, o excluir la moneda actual y mantener la cantidad sin cambios. Se llama recursivamente a la función con estas dos opciones y se suma el resultado de ambas.
Esto se repite recursivamente hasta considerar todas las combinaciones posibles. El resultado final será el número de formas distintas de obtener la cantidad objetivo usando las monedas disponibles.
