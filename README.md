# sql-select-fundamentals

Práctica de consultas SQL básicas con SELECT y alias para la extracción de datos de ventas de TechStore.

## ¿Por qué es mala práctica usar SELECT * en producción?

Aunque SELECT * es útil cuando queremos explorar rápidamente una tabla, en producción es mejor seleccionar solamente las columnas que necesitamos.

Una de las razones es el rendimiento: traer todas las columnas puede consumir más recursos y hacer las consultas más lentas, especialmente cuando trabajamos con tablas grandes.

También afecta la mantenibilidad, ya que si en el futuro se agregan nuevas columnas a la tabla, SELECT * las incluirá automáticamente aunque no sean necesarias para el análisis.

Además, seleccionar columnas específicas ayuda a evitar exponer información que no necesitamos utilizar.

Por ejemplo, en lugar de:

```sql
SELECT * FROM sales;
```

## ¿Por qué son importantes los alias para un stakeholder no técnico?

Los alias permiten presentar los nombres de las columnas de una forma más clara para las personas que utilizan la información pero no conocen la estructura técnica de la base de datos.

Por ejemplo:

```sql
SELECT total_amount AS monto_total
FROM sales;
```

De esta manera, una persona del equipo de Finanzas puede interpretar directamente `monto_total`, en lugar de tener que conocer el significado técnico de `total_amount`.
