# Práctica de PostgreSQL: Cambios de Precios con Trazabilidad

Este proyecto implementa y demuestra la lógica de negocio en PostgreSQL para gestionar el catálogo de una tienda digital mediante una **Función Escalar**, un **Procedimiento Almacenado** y un **Trigger de Auditoría**.

---

## Informes
* **Versión de PostgreSQL:** PostgreSQL 18.0 (o superior)
* **Base de datos utilizada:** Base de datos propia de catálogo / Chinook

---

## Contexto del Caso
El objetivo es permitir ajustes porcentuales de precio sobre el catálogo de productos/pistas sin alterar los datos históricos de facturación.
1. **Cálculo previo:** Permite calcular el precio resultante sin alterar las tablas.
2. **Actualización controlada:** Modifica únicamente el registro seleccionado tras validar existencia y parámetros.
3. **Auditoría transparente:** Registra automáticamente cualquier cambio efectivo de precio con los datos del usuario y fecha/hora.

---

## Estructura del Repositorio

```text
.
├── README.md
└── sql/
    ├── 01_preparacion.sql
    ├── 02_funcion_escalar.sql
    ├── 03_procedimiento.sql
    ├── 04_trigger_y_funcion.sql
    └── 05_pruebas.sql
