KPI (Key Performance Indicator) Es un indicador que muestra de manera cuantificable el desempeño de una medida
en este caso lo podremos medir viendo la diferencia entre la anterior web y la nueva
- Completion Rate: The proportion of users who reach the final ‘confirm’ step.
TEST:
    - total usuarios:                               25722	
    - porcentaje de usuarios que llega a confirm:   14.46%

CONTROL:
    - total usuarios:                               17505	
    - porcentaje de usuarios que llega a confirm:   17.93%

Conclusión: 
    Al cambiar la estrategia de marketing, aumentan los usuarios que acceden a la web, pero disminuye la captación un 3.47%



- Time Spent on Each Step: The average duration users spend on each step.
Resultado:

	process_step	time_spend

0	confirm	            NaN
1	start	            33.940854
2	step_1	            35.633517
3	step_2	            86.724563
4	step_3	            114.965693

Conclusión: 
Los usuarios que pasan de start a step_1, la duración media es de aproximadamente 34 segundos
Los usuarios que pasan del step_1 al step_2, la duración media es de aproximadamente 36 segundos
Los usuarios que pasan del step_2 al step_3, la duración media es de aproximadamente 87 segundos
Y los usuarios que terminan el proceso y pasan de step_3 a confirm, es de aproximadamente 2 minutos


- Error Rates: If there’s a step where users go back to a previous step, it may indicate confusion or an error. You should consider moving from a later step to an earlier one as an error.

    process_step	    user_error	    total_errors	    total_steps     error_rate
1	    step_1	            1.0	            8893	            68410	        13.00
3	    step_3	            1.0	            4654	            48675	        9.56
2	    step_2	            1.0	            4534	            56855	        7.97
0	    confirm	            1.0	            159	                43214	        0.37


Conclusión:
El step que genera más confusión y más errores es el step_1 donde casi el 13% de los usuarios vuelven a la página anterior
después va el step_3 con casi un 10% de los usuarios
posteriormente el step_2 con un 8%
Y la pagina confirm no tiene confusión ya que no da error ni el 0.4% de veces



HYPOTHESIS Testing

1.
H0 --> TEST completion rate == CONTROL completion rate
H1 --> TEST completion rate != CONTROL completion rate

2.
H0 --> Diference between TEST completion rate and CONTROL completion rate is at least 5%
H1 --> Diference between TEST completion rate and CONTROL completion rate is more than 5%

3.
H0 --> Gender is important between TEST and CONTROL
H1 --> Gender is NOT important between TEST and CONTROL