# galindo-prueba-rimac
 Prueba técnica

Este trabajo es parte de un reto técnico.
Cada uno de los endpoints han sido probados usando la herramienta Postman. Tener en cuenta que es necesario contar con la carpeta comprimida 'axios.zip' descargada en la PC, para poder agregarla mediante la consola de LAMBDA como una CAPA. Posteriormente dicha capa debe ser agregada a las funciones LAMBDA getPersonaje y addPersonaje. Esto permite usar AXIOS para conectar con el api de SWAPI 


Se diseñaron 5 endpoints:

1) https://rmhdsofxni.execute-api.us-east-1.amazonaws.com/verPersonajeSwapi/{id}
2) https://rmhdsofxni.execute-api.us-east-1.amazonaws.com/agregarPersonaje
3) https://rmhdsofxni.execute-api.us-east-1.amazonaws.com/listarPersonajesBD
4) https://rmhdsofxni.execute-api.us-east-1.amazonaws.com/modificarPersonaje
5) https://rmhdsofxni.execute-api.us-east-1.amazonaws.com/borrarPersonaje

Explicación:
1) Ver Personaje Swapi: Este endpoint GET permite ver el estado inicial de un personaje del api SWAPI, colocando su id en dicha api (1,2,3,... etc)

2) Agregar Personaje a BD: Este endpoint POST permite almacenar a un personaje del api Swapi en la BD DynamoDB. Se debe enviar como body un json indicando el valor del id del personaje que se desea almacenar.
Ejemplo body:
{
    "id":"1"
}

3) Listar Personajes BD: Este endpoint GET permite listar a todos los personajes que han sido almacenados en la BD DynamoDB mediante el endpoint nro 2

4) Modificar Personaje en BD: Este endpoint POST permite modificar 4 campos de un personaje en la BD DynamoDB. Se debe enviar como body un json indicando 5 valores del personaje que se desea modificar.
Ejemplo body:
{
    "id":"1",
    "nombre":"Luke Skywalker 2",
    "altura": "169",
    "color_cabello":"rubio",
    "masa":"69"
}

5) Borrar Personaje en BD: Este endpoint POST permite borrar un personaje en la BD DynamoDB. Se debe enviar como body un json indicando el valor del id del personaje que se desea borrar.
Ejemplo body:
{
    "id":"1"
}

