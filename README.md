# Telecom_operator_performance

En este proyecto se propone una función que brinda a los supervisores información sobre los operadores menos eficaces. En el cual genere campos calculados utilizando indicadores de desempeño de otras industrias y adaptandolas a este caso en concreto para establecer una calificación porcentual, para posteriormente utilizar los tres indicadores propuestos para clasificar a los operadores, identificando a los operadores con menor desempeño.

Conforme a los comentarios de los supervisores se considera a un operador ineficiente si:
- si tiene una gran cantidad de llamadas entrantes perdidas (internas y externas)
- y un tiempo de espera prolongado para las llamadas entrantes.
- Además, si se supone que un operador debe realizar llamadas salientes, un número reducido de ellas también será un signo de ineficacia.

## Herramientas y tipo de proyecto

![Static Badge](https://img.shields.io/badge/sklearn-blue?style=for-the-badge)
 | ![Static Badge](https://img.shields.io/badge/pandas-blue?style=for-the-badge&logo=pandas)
 | ![Static Badge](https://img.shields.io/badge/matplotlib.pyplot-blue?style=for-the-badge)
 | ![Static Badge](https://img.shields.io/badge/seaborn-blue?style=for-the-badge)
 | ![Static Badge](https://img.shields.io/badge/ETL-blue?style=for-the-badge)| 

## Metodología
- **Preprocesamiento de datos:**
Se estandarizaron los nombres de las columnas, se verificaron y limpiaron los valores ausentes y duplicados.
Se unieron ambas tablas 

- **Analisis Exploratorio de datos (EDA):**
Se establecerieron indicadores mediante el calculo de campos calculados de las columnas existentes para cada operador.
  - Indicador de llamadas perdidas por operador
  - Indicador para el tiempo de espera
  - Indicador de llamadas salientes por operador
  - Evaluación de los operadores usando los tres indicadores.
-**Pruebas de hipotesis:**
   - Hipotesis #1: Existe una relación entre la cantidad de llamadas perdidas y los diferentes planes.
   - Hipotesis #2: Los operadores eficientes realizan más llamadas salientes. Utilizando prueba t de dos muestras. comparando los promedios.

## Visualizaciones destacadas


-Tabla de clasificación de operadores
En esta tabla podemos observar como los operadores son calificados y obtienen una calificación final donde son evaluados.  
![image](https://github.com/user-attachments/assets/40358ac5-1700-4217-8cef-e7372536c8b1)

-Reporte para supervisores en Tableau  

Mediante este dashboard se presentan la evaluación de los indicadores, se puede visualizar tanto por grupos como por operador para visualizar sus datos.
![image](https://github.com/user-attachments/assets/9be3aa5b-8a6c-42d5-8bc7-b60eb857dbaa)
[Dashboard](https://public.tableau.com/app/profile/luis.enrique.diaz.rojas/viz/Dashboard_telecom_17308317422890/Dashboard1)



## Conclusiones y recomendaciones
Logramos crear indicadores que nos sirvan para evaluar la eficiencia de los operadores de una empresa.

- llamadas perdidas
- tiempo de espera
- llamadas salientes
Y como logramos comprobar en nuestras hipotesis, tenemos una relación entre los diferentes planes y las llamadas perdidas, quedaria explorar la distribución de los operadores novatos para equilibrar los planes y mejorar la eficiencia en los tres grupos. En el caso, de la segunda hipotesis, nos sirvio para corroborar que nuestro indicador de llamadas salientes realmente tiene algun impacto. Donde comprobamos que existe relación entre los operadores eficacez y el número de llamadas. Finalmente, la clasificación que se realizo nos sirvio de ayuda para reducir el grupo de operadores a los cuales hay que prestar atención y capacitarlos.

Otras recomendaciones serian:

- Tenemos un gran número de registros sin número de usuario, sin embargo, no contamos con información suficiente para relacionarlos. Por lo que se recomienda verificar que los datos esten correctamente capturados.  
- Aumentar la capacitación, si bien nuestro grupo de operadores ineficientes es de 56 operadores, la población de operadores regulares supera por mucho a la de eficientes. por lo que requieren atención.  
- Establecer los objetivos conforme a la medias obtenidas con estos indicadores para que los operadores intenten llegar a estos números y así puedan mejorar.
