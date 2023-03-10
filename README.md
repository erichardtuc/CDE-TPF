# Cloud Data Engineering - Trabajo Practico Final

Alumno: Emiliano Richard

## Descripcion del problema

El dataset elegido posee un listado de talleres (workshops), clientes y sus respectivos vehiculos (Camiones y Colectivos).
Utilizando el Algoritmo de K-nearest-neighbors(KNN) se procedio a entrenar un modelo de ML para luego mediante un endpoint si se envia la ubicacion geografica (latitud y longitud) se devuelve el mejor taller para realizar los servicios y las reparaciones de las unidades adquiridas.

##  Arquitectura AWS

- `Amazon S3`: Se utilizo este servicio para disponer de los datasets en AWS y guardar los datos procesados para usarse en el entrenamiento.
- `Amazon SageMaker`: Se instancio un notebook donde se realizar el procesamiento y limpieza de los datasets con el fin de crear un endpoint con el modelo de ML.
- `Amazon Lambda`: Se utiliza para instanciar el endpoint creado.
- `Amazon API Gateway`: "Es la puerta principal" donde el usuario puede enviar los datos para que este le devuelva la prediccion.

### Diagrama

![Diagrama AWS](https://user-images.githubusercontent.com/15094926/209726826-c325e2fd-351d-413f-bda8-7a9a2b67fb8c.png)
