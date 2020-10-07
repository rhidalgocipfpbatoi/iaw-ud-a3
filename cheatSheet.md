# Conociendo el Lenguaje Php (III) - CheatSheet
Estructuras de control de flujo: Salto y Repetición

#### 1. Estructuras de salto (if, else, switch)
#### 1.1 `if`
La estructura de control `if` permite la ejecución condicional de una instrucción o bloque de ellas.
Sintaxis:
```php
<?php

if (condicion_es_cierta) {
    bloque_de_sentencias
}
``
?>
```
**Ejemplo:**
El siguiente ejemplo mostraría "a es mayor que b" si la variable `$a` es mayor que ``$b``:

```php
<?php``

$a = 10;
$b = 5;

if ($a > $b) {
    echo "a es mayor que b";
}

?>
```
#### 1.2 `if..else`
Añade la cláusula `else` para especificar una instrucción o bloque de instrucciones a ejecutar en caso de que no
se cumpla la condición.

**Sintaxis:**

```php
<?php

if (condicion_es_cierta) {
    bloque_de_sentencias_1
} else {
    bloque_de_sentencias_2
}

?>
```

**Ejemplo:**
El siguiente ejemplo puede mostrar "a es mayor que b" si la variable `$a` es mayor que `$b` o "a NO es mayor que b" en caso contrario.
 ```php
<?php

$a = 1;
$b = 5;

if ($a > $b) {
    echo "a es mayor que b";
} else {
    echo "a NO es mayor que b";
}

?>
```

#### 1.3 `else if`
Permite concatenar condiciones no superpuestas

**Sintaxis:**
```php
<?php

if (condición_1) {
    bloque_de_sentencias_1
} elseif (condición_2) {
    bloque_de_sentencias_2
} else {
    bloque_de_sentencias_3
}

?>
```
**Ejemplo:**
```php
<?php

$a = 1;
$b = 1;

if ($a > $b) {
    echo "a es mayor que b";
} elseif ($a == $b) {
    echo "a es igual que b";
} else {
    echo "a es menor que b";
}

?>
```

#### 1.4 ``switch``

**Sintaxis:**
```php
<?php

switch ($variable) {
    case valor1:
        bloque_de_sentencias_1
        break;

    case valor2:
        bloque_de_sentencias_2
        break;

    default:
        bloque_de_sentencias_3
}

?>
```

Esta estructura de control es equivalente a:
```php
<?php

if ($variable == valor1) {
    bloque_de_sentencias_1
} elseif ($variable == valor2) {
    bloque_de_sentencias_2
} else {
    bloque_de_sentencias_3
}

?>
```
**Ejemplo:**
```php
<?php

$numero = 2;

switch ($numero) {
    case 1:
        echo "La variable es igual a 1";
        break;
    case 2:
        echo "La variable es igual a 2";
        break;
    default:
        echo "La variable es un número dstinto a 1 y 2";
}
?>
```
### 2. Estructuras de repetición (for, while, do-while)
#### 2.1 `for`

**Sintaxis:**
```php
for (expr1; expr2; expr3) {
    sentencias;
}
```
Ejemplo:
El siguiente ejemplo muestra los números del 1 al 10.

```php
<?php

for ($i = 1; $i <= 10; $i++) {
    echo $i;
    echo "<br>";
}

?>
```
**Ejemplo:**
El siguiente ejemplo muestra los números del 10 al 1.
```php
<?php

for ($i = 10; $i >= 1; $i--) {
    echo $i;
    echo "<br>";
}

?>
```
#### 2.2 `while`

**Sintaxis:**
```php
while (condicion_es_verdadera) {
    sentencias;
}
```

Ejemplo:
El siguiente ejemplo muestra los números del 1 al 10.
```php
<?php

$i = 1;
while ($i <= 10) {
    echo $i;
    echo "<br>";
    $i++;
}

?>
```
**Ejemplo:**
El siguiente ejemplo muestra los números del 10 al 1.
```php
<?php

$i = 10;
while ($i >= 1) {
    echo $i;
    echo "<br>";
    $i--;
}

?>
```
#### 2.3 `do...while`
```php
do {
    sentencias;
} while (condicion_es_verdadera)
```

Ejemplo:
El siguiente ejemplo muestra los números del 1 al 10.
```php
<?php

$i = 1;
do {
    echo $i;
    echo "<br>";
    $i++;
} while ($i <= 10);

?>
```
**Ejemplo:**
El siguiente ejemplo muestra los números del 10 al 1.
```php
<?php

$i = 10;
do {
    echo $i;
    echo "<br>";
    $i--;
} while ($i >= 1);

?>
```

