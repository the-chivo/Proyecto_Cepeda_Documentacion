# Documentacion proyecto Cepeda

### Unity version: 6-3 LTS (6000.3.0f1)

## Tipo de escena

La escena es 3D pero para acceder a todas las caracteristicas en 2d del motor si no las ofrece de primeras clickar: window --> Package Management --> Package Management y dentro de la ventana que se abre instalar todo lo relacionado con el 2D. Despues reabrir el proyecto si es necesario.

## Sprites(Fondo, personajes y animaciones)

Toda la parte grafica en 2d estara gestionada en Sprite haciendo uso de Sprite renderer para los personajes y tileMaps para l# escenarios. Es necesario tener un TileSet que no es mas que un png con todos los sprites que se quieran usar, puede ser para un personaje con sus animaciones o un escenario con todos su bloques. En itchio hay muchos samples gratis. Los que estoy usando de momento son:
* Para los fondos: https://finalbossblues.itch.io/cloud-city-tileset
* Para el player: https://github.com/kiyama14/tutorial-art

## Fondo

Dentro de la carpeta de los fondos hay un png llamado tile_set con un monton de sprites de fondos, arrastramos esa imagen a asests de nuestro proyecto en una carpeta o lo que quieras.
Al clicar el tileset se nos abrira el inspectgor y es necesario hacer los siguiente cambios:
* Sprite MOde: Multiple
* Pixels Per Unit: 16
* Filtrer Mode: Point(No Filter)
* Compression: None
Inportante clicar en apply despues de los cambios.
En el inspector veremos un boton llamado Sprite Editor, es con lo que vamos a separar la imagen en pequeños sprites del tamaño deseado, en este caso como es para un fondo los cortaremos como cuadrado al tamaño de cada "cuadrito".
Al abrir el editor clicar en Slice arriba a la izquierda y en Type cambiar a Grid by Cell Size y en pixel size el eje x en 16 y el eje y en 16 y clicar el boton Slice y Aply.

![Imagen](Images/editorCap.png)

Veremos que nuestro png se ha separado en bloques individuales.

Para enpezar a pintar el fondo debemos de crear un: 2D Object ---> TileMap ---> Rectangular

Se nos creara un grid y nuestro fondo dentro del grid que lo llamaremos background o nonCollisionLow.
Para enpezar a pintar necesitamos una Tile Palete que es una ventanita, para sacarla vamos a: Window ---> 2D ---> Tile Palete.

Se nos abrira esta ventana:

![Imagen](Images/tilePalete.png)

Clicamos en Create New Palete le asignamos el nombre(background) y clicamos en create, pedira un folder, lo mejor es crear una carpeta en Assets la llamamos Tiles y lo selecionamos.

Seleccionamos el tileSet que teniamos previamente sliceado y lo arrastramos a la Tile Palete


![Imagen](Images/tileMover.png)


Nos pedira un folder, seleccionaremos el folder llamado Tiles que creamos antes.
Una vez hecho ya tenemos todas las herramientas necesarias para pintar el backGround


