Estás trabajando como analista para Zuber, una nueva empresa de viajes compartidos que se está lanzando en Chicago. Tu tarea es encontrar patrones en la información disponible. Quieres comprender las preferencias de los pasajeros y el impacto de los factores externos en los viajes.

Estudiarás una base de datos, analizarás los datos de los competidores y probarás una hipótesis sobre el impacto del clima en la frecuencia de los viajes.

Descripción de los datos
Una base de datos con información sobre viajes en taxi en Chicago:

tabla neighborhoods: datos sobre los barrios de la ciudad

name: nombre del barrio
neighborhood_id: código del barrio
tabla cabs: datos sobre los taxis

cab_id: código del vehículo
vehicle_id: ID técnico del vehículo
company_name: la empresa propietaria del vehículo
tabla trips: datos sobre los viajes

trip_id: código del viaje
cab_id: código del vehículo que opera el viaje
start_ts: fecha y hora del inicio del viaje (tiempo redondeado a la hora)
end_ts: fecha y hora de finalización del viaje (tiempo redondeado a la hora)
duration_seconds: duración del viaje en segundos
distance_miles: distancia del viaje en millas
pickup_location_id: código del barrio de recogida
dropoff_location_id: código del barrio de finalización
tabla weather_records: datos sobre el clima

record_id: código del registro meteorológico
ts: fecha y hora del registro (tiempo redondeado a la hora)
temperature: temperatura cuando se tomó el registro
description: breve descripción de las condiciones meteorológicas, por ejemplo, "lluvia ligera" o "nubes dispersas"
Esquema de la tabla
image

Nota: no existe una conexión directa entre las tablas trips y weather_records en la base de datos. Pero aún puedes usar JOIN y vincularlos usando la hora en la que comenzó el viaje (trips.start_ts) y la hora en la que se tomó el registro meteorológico (weather_records.ts).

Ya has completado la primera parte del proyecto: escribiste un código para analizar los datos meteorológicos de un sitio web. Ahora vas a hacer la segunda y tercera parte:

Ejercicios de 1 a 3: Análisis exploratorio de datos

Ejercicios de 4 a 6: Prueba la hipótesis de que la duración de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos

Paso 4. Análisis exploratorio de datos (Python)

Además de los datos que recuperaste en las tareas anteriores te han dado un segundo archivo. Ahora tienes estos dos CSV:

/datasets/project_sql_result_01.csv. contiene los siguientes datos:

company_name: nombre de la empresa de taxis

trips_amount: el número de viajes de cada compañía de taxis el 15 y 16 de noviembre de 2017. 

/datasets/project_sql_result_04.csv. contiene los siguientes datos:

dropoff_location_name: barrios de Chicago donde finalizaron los viajes

average_trips: el promedio de viajes que terminaron en cada barrio en noviembre de 2017.

 Para estos dos datasets ahora necesitas

importar los archivos
estudiar los datos que contienen
asegurarte de que los tipos de datos sean correctos
identificar los 10 principales barrios en términos de finalización del recorrido
hacer gráficos: empresas de taxis y número de viajes, los 10 barrios principales por número de finalizaciones
sacar conclusiones basadas en cada gráfico y explicar los resultados
Paso 5. Prueba de hipótesis (Python)

/datasets/project_sql_result_07.csv — el resultado de la última consulta. Contiene datos sobre viajes desde el Loop hasta el Aeropuerto Internacional O'Hare. Recuerda, estos son los valores de campo de la tabla:

start_ts: fecha y hora de la recogida
weather_conditions: condiciones climáticas en el momento en el que comenzó el viaje
duration_seconds: duración del viaje en segundos
Prueba la hipótesis:

"La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos".

Decide por tu cuenta dónde establecer el nivel de significación (alfa).

Explica:

cómo planteaste las hipótesis nula y alternativa
qué criterio usaste para probar las hipótesis y por qué
¿Cómo será evaluado mi proyecto?
Estos son los criterios de evaluación del proyecto. Léelos atentamente antes de empezar a trabajar.

Esto es lo que buscará el revisor del proyecto al evaluar tu proyecto:

cómo recuperas los datos del sitio web
cómo creas slices de datos
cómo agrupas los datos
si usas correctamente los diversos métodos para combinar datos
cómo formulas las hipótesis
qué criterios utilizas para probar las hipótesis y por qué
a qué conclusiones llegas
si dejas comentarios en cada paso