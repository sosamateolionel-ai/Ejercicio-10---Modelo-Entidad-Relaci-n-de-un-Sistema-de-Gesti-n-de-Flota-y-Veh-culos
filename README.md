# Ejercicio 10 - Modelo Entidad-Relación de un Sistema de Gestión de Flota y Vehículos

## Descripción
Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión de flotas y transporte[cite: 6]. El modelo permite administrar vehículos, choferes, viajes, asignación de personal, registro de cargas de combustible y control de mantenimientos en talleres[cite: 6].

## Entidades y atributos

### 1. Vehiculo
Representa los vehículos o unidades de transporte que componen la flota.
- **id_vehiculo**: identificador único del vehículo[cite: 6].
- **tipo vehiculo**: categoría o clase de vehículo[cite: 6].
- **marca**: marca fabricante[cite: 6].
- **modelo**: modelo del vehículo[cite: 6].
- **kilometraje**: distancia recorrida acumulada[cite: 6].
- **patente**: número de matrícula o patente[cite: 6].

### 2. Chofer
Representa al personal de conducción autorizado.
- **id_chofer**: identificador único del chofer[cite: 6].
- **categoria_licencia**: tipo de licencia habilitante[cite: 6].
- **legajo**: número de legajo laboral[cite: 6].
- **vencimiento_licencia**: fecha de expiración de la licencia[cite: 6].
- **nombre**: nombre completo del chofer[cite: 6].

### 3. Viaje
Representa los trayectos o servicios de transporte realizados por los vehículos.
- **id_viaje**: identificador único del viaje[cite: 6].
- **id_vehiculo**: identificador del vehículo asignado[cite: 6].
- **origen**: punto de partida[cite: 6].
- **destino**: punto de llegada[cite: 6].
- **estado**: estado actual del viaje (ej. en curso, finalizado, programado)[cite: 6].
- **fecha hora salida**: fecha y hora de partida[cite: 6].
- **fecha hora llegada**: fecha y hora de llegada[cite: 6].

### 4. Cargar combustible
Representa los repostajes de combustible realizados a los vehículos.
- **id_carga**: identificador único de la carga[cite: 6].
- **id_vehiculo**: identificador del vehículo abastecido[cite: 6].
- **cantidad litros**: volumen de combustible cargado[cite: 6].
- **precio por litro**: costo unitario del combustible[cite: 6].
- **costo total**: valor total de la carga[cite: 6].
- **estacion servicio**: nombre o ubicación de la estación[cite: 6].

### 5. Asignacion chofer
Entidad asociativa que vincula a los choferes con los viajes y sus roles específicos.
- **id_viaje**: identificador del viaje[cite: 6].
- **legajo**: legajo del chofer asignado[cite: 6].
- **rol**: función o rol del chofer en el viaje (ej. principal, acompañante)[cite: 6].

### 6. Mantenimiento
Representa las reparaciones o revisiones técnicas realizadas a las unidades.
- **id_mantenimiento**: identificador único del mantenimiento[cite: 6].
- **id_vehiculo**: identificador del vehículo intervenido[cite: 6].
- **tipo_mantenimiento**: clasificación del servicio (ej. preventivo, correctivo)[cite: 6].
- **respuesto**: repuestos utilizados en la reparación[cite: 6].
- **costo total**: valor económico del mantenimiento[cite: 6].
- **ingreso**: fecha y hora de entrada al taller[cite: 6].
- **salida**: fecha y hora de salida del taller[cite: 6].

### 7. Taller
Representa los talleres mecánicos o centros de servicio contratados.
- **id_taller**: identificador único del taller[cite: 6].
- **nombre**: nombre del taller[cite: 6].
- **direccion**: ubicación física del establecimiento[cite: 6].
- **telefono**: número de contacto[cite: 6].

## Relaciones y cardinalidades
- **Vehiculo – Cargar combustible (Necesita / 1:N)**: un vehículo realiza múltiples cargas de combustible a lo largo de su operación[cite: 6].
- **Vehiculo – Viaje (Incluye / 1:N)**: un vehículo puede realizar diversos viajes en distintos periodos[cite: 6].
- **Viaje – Asignacion chofer (Necesita / 1:N)**: un viaje requiere la asignación de uno o más choferes a través de la entidad asociativa[cite: 6].
- **Asignacion chofer – Chofer (Contiene / 1:N)**: vincula el registro de asignación con la información personal y de legajo del chofer[cite: 6].
- **Vehiculo – Mantenimiento (Necesita / 1:N)**: un vehículo puede registrar varias intervenciones de mantenimiento a lo largo de su vida útil[cite: 6].
- **Mantenimiento – Taller (1:N)**: los mantenimientos se llevan a cabo y se asocian a un taller mecánico específico[cite: 6].

## Objetivo
Diseñar una base de datos robusta para la gestión logística de flotas, permitiendo controlar el estado de los vehículos, planificar viajes y asignar choferes, registrar consumos de combustible y realizar un seguimiento detallado de los costos y servicios de mantenimiento en talleres[cite: 6].

