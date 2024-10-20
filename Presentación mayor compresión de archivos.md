 👋 Hola, soy Yosmel379
 Mostrando en el video de abajo una demostración del algoritmo que cree de compresión de lograr mayor compresión 100% en los datos sin pérdida de información.

https://www.youtube.com/watch?v=_4CuL5q6Glk&t=6s


Les compartiré este otro que es sin pérdida de información para que vean que si se puede comprimir más y un documento pdf explicando y pruebas.


  Documento explicaciones en archivo .pdf
  
https://www.mediafire.com/file/q4itlgynb1zvqnc/Explicando-algoritmo-DualPhaseCompress.pdf/file


Nuevo contenido entre líneas

--------------------------------------------------------------------------------------------
Para hacer pruebas ver compresión programa ejecutable .exe

https://www.mediafire.com/file/4p0b54noj50mc3l/DualPhaseCompress_nz.exe/file

El programa en las reglas se puede modificar para comprimir en distintos tipos de compresión abajo estara el archivo .py para ello.



Programa para modificar archivo .py

https://www.mediafire.com/file/zka2jy4yr625j61/DualPhaseCompress_nz.py/file

--------------------------------------------------------------------------------------------


Algoritmo de compresión DualPhaseCompress


[      'datos a hex'      ]

      
tabla

0=1111

1=1010

2=00

3=01

4=10

5=11

6=000

7=001

8=010

9=011

A=100

B=101

C=110

D=111

E=0000

F=0001



reglas

1111 cambiar '0' siguiente

1010 cambiar '01' siguiente

00 cambiar '' siguiente

01 cambiar '1' siguiente

10 siguiente

11 siguiente

000 siguiente

001 siguiente

010 siguiente

011 siguiente

100 siguiente

101 siguiente

110 siguiente

111 siguiente

0000 siguiente

0001 cambiar '00'siguiente


compresión

5    7       1        5   A      F       0       0        1       2     7      B = 48bits

11  001  1010  11  100  0001 1111 1111  1010  00   001  101 = 38bits =20.83bits


compresión

('11', '001', '01', '11') ('100', '00', '0', '0') ('01', '', '001', '101') = 16bits = 66.67%


descomprimir


reglas

0   cambiar '1111' siguiente

01 cambiar '1010' siguiente

''  cambiar '00' siguiente
     
1  cambiar '01' siguiente

10 siguiente

11 siguiente

000 siguiente

01 siguiente

010 siguiente

011 siguiente

100 siguiente

101 siguiente

110 siguiente

111 siguiente

0000 siguiente

00   cambiar '0001' siguiente


reconstruir

('11', '001', '01', '11') ('100', '00', '0', '0') ('01', '', '001', '101')


realizado

('11', '001', '1010', '11') ('100', '0001', '1111', '1111') ('1010', '00', '001', '101')


datos

11  001  1010  11  100  0001 1111 1111 1010 00 001 101
 5    7      1        5    A     F        0       0      1       2   7     B = 48bits 



Mostré esto como referencia.

Espero sus opiniones.



