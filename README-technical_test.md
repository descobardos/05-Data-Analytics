# Prueba técnica X - Analytic

## Información entregada (datasets en carpeta Tablas)

La siguiente tabla contiene en cada fila un registro eventos de mantención.
- _**Eventos.csv**_:
    - Unnamed: 0 -> enumeración de las filas
    - Equipo -> Identificación de equipo
    - Fecha Inicio Evento -> Inicio de mantención
    - Fecha Fin Evento -> Fin de mantención
    - Duración -> Duración de mantención
    - Motivo Nivel 1 -> Información mantención
    - Motivo Nivel 2 -> Información mantención
    - Motivo Nivel 3 -> Información mantención
    - Motivo Nivel 4 -> Información mantención
    - Motivo Nivel 5 -> Información mantención
    - Modo de Falla -> Información mantención
    - Especialidad -> Información mantención
    - Turnos -> Turno a cargo de mantención

La siguiente tabla contiene en cada fila un registro del valores de los sensores para cada equipo.
- _**Tabla estado.csv**_:
    - Unnamed: 0 -> enumeración de las filas
    - Fecha -> fecha del resgistro
    Además el resto de las columnas contienen los distintos valores de los sensores de los equipos.
    Columnas ejemplo para el equipo ID7:
    - Potencia Motor Chancador Obsoleto y Nuevo (Umbral aprox. 14/07/2021) Terciario 2 ID7 - Hp
    - Horometro Chancador Obsoleto y Nuevo (Umbral aprox. 14/07/2021) Terciario 2 ID7 - Hr
    - Energia Acumulada Chancador Obsoleto y Nuevo (Umbral aprox. 14/07/2021) Terciario 2 ID7 - MWh
    - Corriente Motor Chancador Obsoleto y Nuevo (Umbral aprox. 14/07/2021) Terciario 2 ID7 - Amp

## Problema

El cliente quiere que hagamos modelos de mantenimiento predictivo para los 2 equipos más críticos, sin embargo, ellos no saben cuáles son estos 2 equipos, ni tienen una especie de ranking de equipos.

1. Cómo primera fase del proyecto, necesitamos determinar cuáles son. (argumentar)
2. Calcular kpis de interés (los que considere útiles).
3. Realizar modelo predictivo de fallas (clasificatorio y/o de regresión o no supervisado), argumentando la elección.
4. Explique cómo realizó la selección de features relevantes para determinar fallas.
5. Entregué comentarios finales a partir de los resultados obtenidos.

*Observaciones*
> A tabla _**Eventos.csv**_ falta considerar la tabla _**detenciones 20-21.csv**_
>
> Importante considerar a la hora de juntar las tablas:
>
> En tabla _**Eventos.csv**_:
> - Columna con Fecha Inicio Evento y Fecha Fin Evento.
> - Columna *Turnos* con valores *Turno A/B*
> - Identificador de equipos en columna *Equipo* con valores *ID0*
> - Información del tipo de evento en columnas *Motivo Nivel 1, Motivo Nivel 2, Motivo Nivel 3, Motivo Nivel 4, Motivo Nivel 5, Modo de Falla, Especialidad*.

>
> En tabla _**detenciones 20-21.xlsx**_:
> - Columna con fecha, otra columna con hora de inicio, otra con hora de fin (ambas horas en formato AM/PM).
> - Columna *Turno* con valores *A/B*
> - Identificador de equipos en columna *Equipos*
> - Información del tipo de evento en columna *Evento*

> **Si considera que no es necesario utilizar tal tabla, argumente por qué** 