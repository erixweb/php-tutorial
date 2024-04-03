# Tutorial PHP

### ETIQUETA PHP

Antes de escribir código PHP, necesitas abrir la etiqueta `php` de la siguiente manera

```php
<?php
    // tu código
?>
```

### ECHO

Para escribir en la pantalla un mensaje en PHP se usa `echo`

```php
<?php
    echo "¡Hola mundo!";
?>
```

### Operaciones

Como en cualquier lenguaje de programación, en PHP puedes hacer cálculos.

```php
<?php
    echo 4 + 2;
    echo 4 * 2;
    echo 4 / 2;
?>
```

O operaciones más complejas como:

```php
<?php
    echo (4 + 2) * 2 * (1.1 * 2);
?>
```

> Los parentesis no son cosa de PHP, es el orden matemático PEMDAS (Paréntesis, Exponentes, Multiplicación y División, Suma y Resta).

### Variables

Para crear variables en PHP, lo haríamos de esta forma:

```php
<?php
    $name = "Erik";
?>
```

También, para poner en pantalla estas variables:

```php
<?php
    echo $name;
?>
```

También sería válido usar comillas dobles (`""`) pero no comillas simples (`''`)

```php
<?php
    echo "$name";
?>
```

### Concatenamiento

Para ajuntar dos strings (cadenas de texto) en PHP, no se usa el `+` como se haría en JavaScript, sinó que se usa el `.`

```php
<?php
    echo "Hola " . "mundo";
?>
```

### If, else y else if

Para hacer condiciones en PHP debes usar, principalmente, el `if`.

```php
<?php
    $age = 24;

    if ($age < 18) {
        echo "Eres menor";
    }
?>
```

En caso de que no se cumpla la condición, se usa el `else`

```php
<?php
    $age = 24;

    if ($age < 18) {
        echo "Eres menor de edad";
    } else {
        echo "Eres mayor de edad";
    }
?>
```

En caso de querer varias condiciones con diferentes respuestas, se usaría el `elseif` o `else if`, ambos sinónimos.

```php
<?php
    $age = 24;

    if ($age < 18) {
        echo "Eres menor de edad";
    } else if ($age >= 50) {
        echo "Eres bastante mayor ya";
    } else {
        echo "Eres mayor de edad";
    }
?>
```

En el caso de que quieras comprar no números si no strings:

```php
<?php
    $name = "Erik";
    $administrador = "Erik";

    // Se busca si tu nombre es igual al del administrador
    if ($name === $administrador) {
        echo "Eres el administrador";
    } else {
        echo "Eres un usuario";
    }
?>
```

### Arrays

Para crear listas de elementos o arrays en PHP, se puede crear usando la palabra `array` o como en JavaScript, usando `[]`

```php
<?php
    $objetos = ["Lápiz", "Ratón", "Ordenador"];
?>
```

Si quieres escribir uno de los elementos en pantalla, usa `echo` seleccionando el `indice` (posición) del elemento

```php
<?php
    $objetos = ["Lápiz", "Ratón", "Ordenador"];
    // Indice 0 = Lápiz
    echo $objetos[0]; // Lápiz
?>
```

### Iterar arrays

Para iterar nuestra lista, lo haríamos de la siguiente manera

```php
<?php
    $objetos = ["Lápiz", "Ratón", "Ordenador"];

    foreach ($objetos as $objeto) {
        echo "Objeto: $objeto <br />";
    }
?>
```

Este código devolverá

```
Objeto: Lápiz
Objeto: Ratón
Objeto: Ordenador
```

### Funciones de strings

### str_starts_with

Para saber cómo comienza un string en PHP, se usa str_starts_with

```php
<?php
    $mensaje = "Hola, esto es un mensaje";

    if (str_starts_with($mensaje, "Hola")) {
        echo "El mensaje comienza por Hola";
    } else {
        echo "El mensaje no comienza por Hola";
    }
?>
```

#### strtolower

Para convertir un string a minúsculas, se usa la función `strtolower`

```php
<?php
    $mensaje = "HOLA, Esto ES un mensaJe";
    // Esto devuelve hola, esto es un mensaje
    echo strtolower($mensaje);
?>
```

#### strtolower

Para convertir un string a mayúsculas, se usa la función `strtoupper`

```php
<?php
    $mensaje = "hola, esto es un mensaje";
    // Esto devuelve HOLA, ESTO ES UN MENSAJE
    echo strtoupper($mensaje);
?>
```
