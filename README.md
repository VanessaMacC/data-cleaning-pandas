# data-cleaning-pandas

Una vez importadas las librerias necesarias para  cargar el archivo csv y poder analizar el df, procedemos a visualizar la estructura para poder establecer las hipótesis.

Importamos el archivo csv.
Fuente: <https://www.kaggle.com/teajay/global-shark-attacks>

Usamos shape para saber el número total de registros y columnas.

Visualizamos las columnas para seleccionar posteriormente las que serán significativas para nuestra hipótesis.

Visualizamos el df con head para conocer los datos con los que vamos a trabajar.

Creamos la columna decada para agrupar los años desde 1960, década en la que se vivió un boom de este deporte tras el parón de la Segunda Guerra Mundial con pd.cut:
Fuente: <https://www.biosurfcamp.com/es/la-historia-del-surf-su-evolucion-y-origenes-hasta-la-actualidad/#:~:text=unos%20pocos%20valientes.-,Renacimiento%20del%20surf%3A%20Siglo%20XX,esta%20recuperaci%C3%B3n%20de%20sus%20costumbres>

Hipótesis 1:
“El mayor número de ataques de tiburón se produjo a surfistas"

Sobreescribo el df para quedarme con las columnas que son más significativas.

Quitamos el espacio que hay detrás de la columna 'Species' con rename y rstrip.

Se vuelve a analizar el tipo de datos de los registros y la info general del df de cara a trabajar los datos nulos.

Cambiamos el tipo de dato en la columna Decade con astype.

Comprobamos si existen duplicados para quedarnos con los datos correctos con duplicated.

Comprobamos si el número de duplicados de la columna Case Number que actúa como ID
afecta al resto de columnas para eliminar sólo los duplicados completos.

Creamos una función para eliminar sólo aquellas filas en los que realmente hay un duplicado.

Compruebo el número de nulos de las columnas del nuevo df con isnull.

Eliminamos las columnas que tienen más de 2500 valores nulos en ellas con drop.

Cambio los valores nulos de la columna Decade a 0 con fillna.

Cambiamos el  tipo de dato de las columnas Year y Decade a entero con astype.

Comprobamos cuál es la actividad que tiene mayor impacto en los ataques de tiburón con value_counts.

Filtramos por la Actividad Surfing para quedarnos con los datos que nos interesan.

Hipótesis 2
"Estados Unidos es el país con más ataques de tiburones a surfistas"

Comprobamos cuál es el país que tiene mayor impacto en los ataques de tiburón con value_counts.

Se agrupa con groupby por ataques por país y año y se pinta la muestra de los 5 primeros países con display y un plot.

Hipótesis 3
"El número de casos ataques a surfistas en Estados Unidos y Australia aumenta cada década"

Comprobamos los años que tienen mayor impacto en los ataques de tiburón con value_counts.

Agregamos por País y década haciendo un count de los años.

Pintamos con display el nuevo df y con plot sacamos el gráfico de barras.

En conclusión, el mayor número de ataques se da en surfitas americanos y los ataques han aumentado en las últimas décadas.

Y para terminar, como dijo Bethany Hamilton: "Mi pasión por el surf era mayor que mi miedo a los tiburones", así a coger olas!!!

<https://www.youtube.com/watch?v=2s4slliAtQU>