# Proyecto: TuNominaYa - Programación Orientada a Objetos

Este proyecto es el Laboratorio 4 de POO, donde corregimos un código "legacy" para que funcione en un entorno Cloud (GitHub Codespaces).

## 1. Justificación de la Herencia
La herencia en este sistema nos permite centralizar los datos comunes de todos los trabajadores (nombre, apellido y seguro social) en la clase `Empleado`. 
Al usar `extends Empleado` en clases como `EmpleadoAsalariado` o `EmpleadoPorHoras`, no tenemos que repetir esas variables. Simplemente heredamos lo que ya funciona y nos enfocamos en el cálculo específico de cada sueldo.

## 2. Justificación del Polimorfismo
En la clase `PruebaSistemaNomina`, usamos el polimorfismo al recorrer un arreglo de tipo `Empleado`. 
Aunque el arreglo es general, al ejecutar `empleados[i].ingresos()`, Java identifica automáticamente si el objeto es de tipo comisión, horas o asalariado y ejecuta el método de cálculo correcto para cada uno. Esto hace que el código sea flexible y fácil de ampliar.

## 3. Consulta: Herencia Múltiple en Java
Java **no permite** la herencia múltiple (heredar de dos clases al mismo tiempo) para evitar el "Problema del Diamante", que causa errores cuando dos padres tienen métodos iguales.
Para solucionar esto, Java utiliza las **Interfaces** mediante la palabra `implements`, permitiendo que una clase adquiera comportamientos de varios lados de forma segura.