# Consultas_1_SQL
introduccion a las consultas a una BD usando el lenguaje SQL

## Base de datos: Ventas
## Tabla: Cliente

![Tabla Cliente](tabla_Cliente.png 'Tabla Cliente')

## Instruccion SELECT
- permite seleccionar datos de una tabla.
- su formato es: 'SELECT CAMPOS_tabla FROM nombre tabla``

## Consulta N°  1

1. Para visualizar toda la información que contiene la tabla Cliente se puede incluir con la introducción SELECT el caracter **\*** o cada uno de los campos de la tabla.

- `SELECT * FROM Cliente`
![consulta1](consulta1_1.png "consulta 1  - 1")

- `SELECT identificacion, nombre, apellidos, direccion, telefono,ciudad_nac, fecha_nac FROM Cliente`
![consulta1](consulta1_2.png "consulta 1  - 2")

### consulta N° 2

2. Para visualizar solamente la identificacion del Cliente: `SELECT identificacion FROM Cliente`
![consulta2](consulta2.png "consulta 2")

### consulta N°3

3. Si se desea obtener los registros cuya identificacion sea mayor o igual a 150, se debe utilizar la cláusula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * FROM Cliente WHERE identificacion>=150`
![consulta3](consulta3.png "consulta 3")

### consulta N°4

4. se desea obtener los registros cuyos apellidos sean Vanegas o Celina, se debe utilizar el operador `IN` Que especifica los registros de una tabla. 

`SELECT apellidos FROM cliente WHERE apellidos IN('vanegas', 'celina')`
![Consulta4](consulta4.png " consulta 4")

O se puede utilizar el operador `OR`
`SELECT apellidos FROM cliente WHERE apellidos ='vanegas'OR apellidos = 'celina'`
![Consulta4 1](consulta4_1.png " consulta 4 1")

### Consulta No. 5

5. Se desea obtener los registros cuya identificacion sea menor de 110 y la ciudad sea  Cali, se debe utilizar el operador `AND`

`SELECT * FROM Cliente WHERE identificacion<=110 AND ciudad_nac = 'Cali'`

![Consultas5](consultas_5.png "consulta 5")

### consulta No. 6

6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador 'LIKE' que utiliza los patrones `%´"(todos) y `_` (caracter).

`SELECT * FROM Cliente WHERE nombre LIKE 'A%'`

![Consultas6](consulta6.png "consulta 6")

### consulta No. 7

7. se desea obtener los registros cuyos nombres contengan la letra 'a'

`SELECT * FROM Cliente WHERE nombre LIKE '%a%'`

![Consultas7](consulta7.png "consulta 7")
