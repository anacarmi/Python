# Python Class 
### 19-10-2019 


Es importante conocer los datos y platicarlos con el cliente para saber si las fechas son string, o los datos estan en cierto con

--

`def count_rows(rows):`

`return len(rows)`

`by_date = data.groupby('dom').apply(count_rows)`

`by_date`



<img width="541" alt="Screen Shot 2019-10-19 at 9 58 04 AM" src="https://user-images.githubusercontent.com/47669890/67148005-0cf9f200-f260-11e9-84f2-416a51725c0a.png">

<img width="273" alt="Screen Shot 2019-10-19 at 9 56 11 AM" src="https://user-images.githubusercontent.com/47669890/67148006-0ec3b580-f260-11e9-8ad5-be1d9a53a171.png">

Lo que se hace es contar los renglones y agruparlos dependiendo del número del día para despues poder hacer una gráfica de que tanta frecuencia se viaja en tal día.


## MATLAB
Import matlab as mtb 

`mtb.hist()
mtb.bar()
mtb.plot()`

al final se pone `mtb.show()` para que se muestre

## Agrupar informacion en Matriz

`by_h_w = data.groupby('weekday hour'.split()).apply(count_rows).unstack()`

`by_h_w`

Este código hace que se muestre el número de viajes de los datos por hora del día cada día de la semana. 
el `.split()` sirve para dividir las horas del día de los días de la semana en dos listas para luego aplicar el `.apply(count_rows)` donde el apply es la función que llama lo que ya se aplicó antes de count_rows, que es que cuenta los renglones de la base de datos que se repite la misma hr. Luego, el `unstack()` es para poner en tipo tabla.

