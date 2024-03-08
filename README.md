# Rust-basics

Una pequeña guia personal de Rust

- Imprimir en la consola (print):

```
fn main() {
    println!("Hola, mundo!");
}
```

- Crear variables y realizar operaciones:

```
fn main() {
    // Declarar variables
    let numero1 = 5;
    let numero2: i32 = 10;  // Especificar el tipo de variable

    // Sumar dos variables e imprimir el resultado
    let suma = numero1 + numero2;
    println!("La suma es: {}", suma);

    // Restar dos variables e imprimir el resultado
    let resta = numero1 - numero2;
    println!("La resta es: {}", resta);

    // Multiplicar dos variables e imprimir el resultado
    let multiplicacion = numero1 * numero2;
    println!("La multiplicación es: {}", multiplicacion);

    // Dividir dos variables e imprimir el resultado
    let division = numero1 / numero2;
    println!("La división es: {}", division);
}
```

- Cadenas de texto (Strings):

```
fn main() {
    let saludo = "Hola, ";
    let nombre = String::from("Rust");

    // Concatenar cadenas e imprimir el resultado
    let mensaje = saludo.to_string() + &nombre;
    println!("{}", mensaje);
}

```

- Entrada del usuario:

```
use std::io;

fn main() {
    println!("Ingrese un número:");

    let mut input = String::new();
    io::stdin().read_line(&mut input).expect("Error al leer la entrada");

    let numero: i32 = match input.trim().parse() {
        Ok(num) => num,
        Err(_) => {
            println!("Por favor, ingrese un número válido.");
            return;
        }
    };

    println!("Número ingresado: {}", numero);
}

```
