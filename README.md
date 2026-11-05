# ATM Digital - V2

Aplicación de consola desarrollada en C# que simula el funcionamiento de un cajero automático con flujo bancario básico. La versión actual corresponde a una evolución del proyecto base y agrega validación de acceso, manejo de saldo, depósitos, retiros y historial de operaciones.

## Funcionalidades incluidas

- Validación de acceso por número de cuenta de prueba.
- Límite de intentos para acceder a la cuenta.
- Estado de cuenta activo/inactivo.
- Consulta del saldo disponible.
- Depósitos con validación del monto.
- Retiros con validación de fondos suficientes.
- Historial de movimientos de la operación.
- Menú interactivo en consola con bucle de ejecución.
- Datos de cliente y nombre bancario fijos para demostración.

## Flujo del programa

Al iniciar, la aplicación:

1. Muestra una bienvenida y la opción de ingreso de cuenta.
2. Valida si el número introducido coincide con la cuenta activa.
3. Si la cuenta es válida, presenta el menú principal.
4. Permite consultar saldo, depositar, retirar y revisar el historial.
5. Continúa ejecutándose hasta que el usuario elige salir.

## Operaciones disponibles

### 1. Consulta de saldo
Muestra el saldo disponible actual en la cuenta.

### 2. Depósito a cuenta
- Solicita el monto a ingresar.
- Verifica que sea mayor que cero.
- Suma el valor al saldo actual.
- Registra el movimiento en el historial.

### 3. Retiro
- Solicita el monto a retirar.
- Verifica que el valor sea válido y mayor que cero.
- Comprueba que exista suficiente saldo.
- Resta el monto del balance.
- Guarda la operación en el historial.

### 4. Historial de movimientos
Muestra la lista de movimientos realizados durante la sesión, con numeración secuencial.

### 5. Salir
Finaliza el menú y termina la ejecución del programa.

## Datos de prueba

La aplicación cuenta con un cliente de ejemplo y una cuenta activa en modo demostración:

- Nombre del cliente: `Christopher Portorreal`
- Saldo inicial: `RD$25,000.00`
- Cuenta activa de prueba: `1`
- Cuenta inactiva de prueba: `2`

> La cuenta activa se habilita únicamente cuando se ingresa `1`, por lo que el flujo de validación está pensado para demostración y pruebas en consola.

## Requisitos

- .NET 10 SDK

## Cómo ejecutar

Desde la raíz del repositorio, ejecuta:

```bash
dotnet run --project ATMProject/ATMProject.csproj
```

## Estructura del proyecto

```text
ATM-V1/
├── README.md
├── atm.psc
├── sin_titulo.psc
└── ATMProject/
    ├── ATMProject.csproj
    ├── Program.cs
    ├── bin/
    └── obj/
```

La lógica principal está en [ATMProject/Program.cs](ATMProject/Program.cs) y la configuración del proyecto en [ATMProject/ATMProject.csproj](ATMProject/ATMProject.csproj).

## Tecnologías utilizadas

- C#
- .NET 10
- Consola interactiva

## Alcance del proyecto

Este proyecto tiene fines educativos y demuestra conceptos fundamentales de programación en C# como:

- variables y constantes
- validación de entrada de usuario
- estructuras condicionales
- bucles
- métodos reutilizables
- listas y manejo de historiales
- operaciones con saldo bancario en memoria

No implementa autenticación real, persistencia de datos ni conexiones con servicios bancarios externos.
