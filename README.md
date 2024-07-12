# Análisis, Diseño y Documentación de la Base de Datos "El Gran Chaparral"

## Introducción
Este repositorio contiene la estructura, diseño lógico y físico de la base de datos para "El Gran Chaparral", un negocio de campos deportivos de fulbito.

## Estructura del Repositorio
El repositorio está organizado de la siguiente manera:
- `scripts/`: Scripts SQL para la creación de tablas, inserción de datos y consultas.
- `reportes/`: Archivos SQL con consultas para generar reportes.
- `documentacion/`: Documentación relacionada con el diseño y análisis de la base de datos.

## Análisis de Requerimientos
### Requerimientos del Negocio
- Gestión de clientes y trabajadores.
- Reservas de espacios deportivos.
- Facturación y control de pagos.

## Diseño Lógico de la Base de Datos


### Descripción de Tablas
#### `CLIENTE`
- `IDCLI`: Identificador único del cliente.
- `NOMCLI`: Nombre del cliente.
- `APECLI`: Apellido del cliente.
- `NUMDOCCLI`: Número de documento del cliente.
- `TELCLI`: Teléfono del cliente.
- `EMACLI`: Email del cliente.
- `IDTIPDOC`: Tipo de documento del cliente.
- `CODUBI`: Código de ubigeo del cliente.

#### `DISPONIBILIDAD_ESPACIO`
- `IDDISESP`: Identificador único de la disponibilidad de espacio deportivo.
- `FECHORINCDISESP`: Fecha y hora de inicio de la disponibilidad.
- `FECHORFINDISESP`: Fecha y hora de fin de la disponibilidad.
- `IDESPDEP`: Identificador del espacio deportivo disponible.

#### `ESPACIO_DEPORTIVO`
- `IDESPDEP`: Identificador único del espacio deportivo.
- `DISESPDEP`: Disponibilidad del espacio deportivo.
- `NUMESPDEP`: Número del espacio deportivo.
- `ACCESPDEP`: Accesorios disponibles en el espacio deportivo.

#### `RESERVA`
- `IDRES`: Identificador único de la reserva.
- `CODRES`: Código único de la reserva.
- `ESTPAGRES`: Estado de pago de la reserva.
- `PRERES`: Precio de la reserva.
- `FECHORINCRES`: Fecha y hora de inicio de la reserva.
- `FECHORFINRES`: Fecha y hora de fin de la reserva.
- `DURRES`: Duración de la reserva en minutos.
- `TIPDEPRES`: Tipo de deporte de la reserva.
- `IDCLI`: Identificador del cliente que realizó la reserva.
- `IDTRA`: Identificador del trabajador asociado a la reserva.
- `IDESPDEP`: Identificador del espacio deportivo reservado.

#### `TIPO_DOCUMENTO`
- `IDTIPDOC`: Identificador único del tipo de documento.
- `NOMTIPDOC`: Nombre del tipo de documento.

#### `TRABAJADOR`
- `IDTRA`: Identificador único del trabajador.
- `NOMTRA`: Nombre del trabajador.
- `APETRA`: Apellido del trabajador.
- `NUMDOCTRA`: Número de documento del trabajador.
- `TELTRA`: Teléfono del trabajador.
- `EMATRA`: Email del trabajador.
- `IDTIPDOC`: Tipo de documento del trabajador.
- `CODUBI`: Código de ubigeo del trabajador.

#### `UBIGEO`
- `CODUBI`: Código de ubigeo.
- `DEPUBI`: Departamento.
- `PROUBI`: Provincia.
- `DISUBI`: Distrito.

## Diseño Físico de la Base de Datos
### Creación de Tablas
Los scripts de creación de tablas se encuentran en la rama documentación.

### Inserción de Datos
Los scripts de inserción de datos se encuentran en `scripts/DF_BD1_241_FULBITO_JOSEZEGARRA.sql`.


## Conclusiones
El diseño y estructura de la base de datos "El Gran Chaparral" permite gestionar eficazmente las reservas, clientes y trabajadores del negocio de campos deportivos de fulbito.
