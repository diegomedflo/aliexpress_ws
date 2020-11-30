# aliexpress_ws

Descripción

Este es un repositorio que descarga información de productos de Aliexpress (https://es.aliexpress.com/).
La información que recolecta el script es: 
- Nombre del producto
- Url de imagen
- Url del producto
- Precio antiguo
- Precio oferta


Instrucciónes de Uso:
Debe recibir los siguientes parametros dentro de la función:

- product -> Producto a buscar en aliexpress (por defecto = 'smartphone').
- min price -> Precio mínimo a considerar (por defecto = 0).
- max_price -> Precio máximo a considerar (por defecto = 99999).
- black_list -> Lista de palabras para ignorar, por si desea ignorar todos los productos que tengan cierta lista de palabras como 'usado' (por defecto = []).
- filename -> Nombre del archivo a crear con la información de los productos. (por defecto = 'aliexpress_ws').
- freeproxy -> Si desea usar una función que descarga proxies gratuitos, True. Si desea usar sus propios proxies, False
- route -> Ruta donde descargar y leer los proxies gratuitos descargados o ruta donde están sus proxies propios.

Preguntas Frecuentes
¿Cómo calcula el precio si Aliexpress brinda un rango de precios?
Aliexpress brinda un rango de precios y a veces un precio único. Lo que hace el código es calcular el precio promedio del límite inferior y límite superior, una vez calculado el promedio se le incrementa el envío. Así es cómo se calcula el precio final estimado.

¿Porqué demora tanto?
Dentro del repositorio, hay una función llamada download_free_proxies que descarga proxies gratuitos. El código debe ejecutarse con proxies para evitar el baneo de la ip. Al usar proxies gratuitos el response es largo. Puedes usar tus propios proxies.

