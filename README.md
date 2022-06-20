# OpenData_TrabajoPractico  Ricardo Schutz
Para empezar se importan las libreriras de: pandas, from bs4 BeautifulSoup, y de requests. 
Las mismas posibilitarian el scraping. Primeeramente definimos la variable url con el link de la pagina a scrapear
Luego con la libreria de r request insrtamos la url de la pagina a realizar el scrapping.
Para saber si esta todo en orden, obtenemos el estado del codigo, si el output es "200" esta todo en orden
Posteriormente visualizamos el contenido y utilizamos la libreria "soup" = BeautifulSoup(content).
Imprimimos el soup para chequear que el codigo trajo correctamente todo el html de la pagina web.
Posteriormente encontramos los bloques donde se encuentra la informacion de los productos, guardando en la 
variable results. Para ello se fefine una funcion para obtener  los datos de la pagina web, definiendo el tag 
principal a utilizar (esto se hace manualmente inspeccionando el codigo html de la pagina de "RoofingMegaStore"). 
Una vez definido el tag principal "('a', {'class':'product-list__link gtmTrack0020'}) " procedemos a buscar los 
tags y sentenciar los datos que deseamos obtener, que en este caso son el nombre del producto, el precio y el precio por m2.
Una vez obtenido  los datos, se crea un data frame con la libreria "pandas", al ver el data frame limpiamos el codigo para 
que no realice llamados a las simbologias seleccionadas, en nuestro caso = '£'. Finalmente se guarda la tabla en un 
archivo .csv. 

