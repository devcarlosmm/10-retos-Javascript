# Miniretos Javascript

Serie de 10 miniretos de javascript con el objetivo de reforzar los conocimientos en Javascript.
Retos sacados desde la pagina: https://github.com/yersoncp/js-fronteros-miniretos-t1

## Reto Nº 1:

Cree una función que repita una cadena n-veces. 'n' es un entero positivo. El primer parámetro es la cadena que se repetirá, y el segundo es la cantidad de veces que se repetirá.

```javascript
repeat("hello", 2); // returns 'hellohello'
repeat(".", 3); // returns '...'
repeat("cat", 1); // returns 'cat'
```

## Reto Nº 2:

Cree una función que devuelva el número mayor en una matriz de números. La matriz siempre tendrá al menos 1 número.

```javascript
largest([1, 2, 3, 4, 5]); // returns 5
largest([-100, Infinity, 5, 2, 7218902]); // returns Infinity
largest([0]); // returns 0
```

## Reto Nº 3

Cree una función que enmascara una cadena de números, por ejemplo el número de tarjeta de crédito. Todos los números, excepto los últimos 4, deben reemplazarse con el carácter #.

```javascript
mask("123456789"); // returns '#####6789'
mask("12345"); // returns '#2345'
mask("1234"); // returns '1234'
mask(""); // returns ''
```

## Reto Nº 4

El número de serie de diversos tickets consta de letras seguidos de nùmeros. Cree una función que permita añadir +1 a la parte numérica final del ticket.

```javascript
incrementTicket("AF4575"); // returns 'AF4576'
incrementTicket("TP0005"); // returns 'TP0006'
incrementTicket("HEP00049"); // returns 'HEP00050'
incrementTicket("RB0000"); // returns 'RB0001'
```

## Reto Nº 5

Los alfabetos disfrutan hacer olas en el futbol. Ayúdalo creando una función que convierta una cadena a una matriz donde una letra mayúscula significa que está de pie.

1. La cadena de entrada siempre estará en minúscula
2. Si el carácter de la cadena es un espacio en blanco, páselo como si fuera un asiento vacío.

```javascript
wave("hola"); // return ["Hola", "hOla", "hoLa", "holA"]
wave("gol peru"); // return ["Gol peru", "gOl peru", "goL peru", "gol Peru", "gol pEru", "gol peRu", "gol perU"]
wave(""); // return [];
```

## Reto Nº 6

**Érase una vez, en un camino a través del viejo oeste salvaje...**

Un hombre recibió instrucciones para ir de un punto a otro. Las instrucciones eran "NORTE", "SUR", "OESTE", "ESTE". Claramente, "NORTE" y "SUR" son opuestos, "OESTE" y "ESTE" también. Ir en una dirección y regresar en la dirección opuesta es un esfuerzo innecesario. Dado que este es el salvaje oeste, con un clima terrible y poca agua, es importante ahorrar energía, de lo contrario, ¡podría morir!

Las instrucciones dadas al hombre son, por ejemplo:

```
["NORTE", "SUR", "SUR", "ESTE", "OESTE", "NORTE"]
```

Inmediatamente puede ver que ir "NORTE" y luego "SUR" no es razonable, ¡mejor quédese en el mismo lugar! El camino se convierte en ["SUR", "ESTE", "OESTE", "NORTE"]. Ahora, "ESTE" y "OESTE" se anula entre sí. Luego "SUR" y "NORTE" no son directamente opuestos pero se vuelven directamente opuestos después de la reducción de "ESTE" y "OESTE".

La tarea es darle al hombre una versión simplificada del plan.

```javascript
reducePlan(["SUR", "NORTE", "ESTE", "OESTE", "ESTE"]);
// return ["ESTE"]

reducePlan(["NORTE", "SUR", "SUR", "ESTE", "OESTE", "NORTE"]);
// return []

reducePlan(["ESTE", "SUR", "SUR", "NORTE", "NORTE", "OESTE"]);
// return []
```

## Reto Nº 7

En un momento crucial, una cantidad **'n'** de personas forman un círculo para finalmente quedar sólo un sobreviviente, lamentablemente el resto será ejecutado por la justicia que a elegido la [Permutación de Josefo](https://en.wikipedia.org/wiki/Josephus_problem) para hallar al único sobreviviente.

El conteo comienza alrededor del círculo en una dirección. Cada persona en la posición **'k'** es ejecutada. El procedimiento se repite con las personas restantes hasta que sólo quede una persona y se libere.

**Ejemplo:**

```javascript
josephusSurvivor(7, 3);
//Si n=7 personas en un círculo y cada k=3 son ejecutadas

1, 2, 3, 4, 5, 6, 7; // Secuencia inicial
1, 2, 4, 5, 7; // 3 y 6 ejecutados
1, 4, 5; // 2 y 7 ejecutados
1, 4; // 5 ejecutado
4; // 1 ejecutado, el sobreviviente es 4
```

Ya sabes que hacer, encuentra al sobreviviente. Si hay solo una persona tomar como sobreviviente único.

```javascript
josephusSurvivor(7, 3); // return 4
josephusSurvivor(41, 3); // return 31
josephusSurvivor(1, 2); // return 1
```

## Reto Nº 8

Suma números, no hay nada mas que decir.

- Las entradas siempre serán numeros

```javascript
sum(2); // return 2
sum(1)(3); // return 4
sum(2)(5)(3); // return 10
sum(1)(0)(3)(2); // return 6
```

## Reto Nº 9

John ha invitado a algunos amigos a una fiesta. Su lista es, según nombres y apellidos:

```
['Fredy Corwill', 'Wilfredo Corwill', 'Barney Tornbull',
'Betty Tornbull', 'Ben Tornbull', 'Raphael Corwill',
'Alfredo Corwill'];
```

- Ordenar de forma alfabética por apellido.
- Si los apellidos son iguales, ordenar por nombre.
- El resultado es una lista ordenada de 'apellidos y nombres'.

```javascript
partyList([
  "Fredy Corwill",
  "Wilfredo Corwill",
  "Barney Tornbull",
  "Betty Tornbull",
  "Ben Tornbull",
  "Raphael Corwill",
  "Alfredo Corwill",
]);
/* return:
[
  'Corwill Alfredo',
  'Corwill Fredy',
  'Corwill Raphael',
  'Corwill Wilfredo',
  'Tornbull Barney',
  'Tornbull Ben',
  'Tornbull Betty'
]
*/

partyList([
  "Alexis Wahl",
  "John Bell",
  "Victoria Schwarz",
  "Abba Dorny",
  "Grace Meta",
  "Ann Arno",
  "Madison STAN",
  "Alex Cornwell",
  "Lewis Kern",
  "Megan Stan",
  "Alex Korn",
]);
/*
Return:
[
  'Arno Ann',
  'Bell John',
  'Cornwell Alex',
  'Dorny Abba',
  'Kern Lewis',
  'Korn Alex',
  'Meta Grace',
  'Schwarz Victoria',
  'STAN Madison',
  'Stan Megan',
  'Wahl Alexis'
]
*/
```

## Reto Nº 10:

Obtener el segundo número mas grande. Eso es todo.

- La entrada siempre tendrá 2 o más números.

```javascript
getSecondLargest([2, 4, 7]); // return 4
getSecondLargest([3, 5, 6, 7, 7]); // return 6
```

---
