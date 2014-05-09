#! encoding: UTF-8
import matplotlib.pyplot as pl
import time
import timeit
import modulo
import pylab as dibujo

x=[10,50,100,150,500,550,1000]
y=[]
m=[]
e=[]
nro_test=20
umbral=0.0000001


if __name__=="__main__":
   import sys
   f=open("tiempo y errores", 'w')
#print "Introduzca el nombre del fichero para almacenar los resultados:"
#nombre_fichero= raw_input();
   
   for i in x: 
      start=time.time()
      pe=modulo.error(i,nro_test,umbral)
      finish=time.time()-start
      print "El porcentaje de error es de: %5.3f" %pe
      print "El tiempo que tarda en realizarse es: %14.13f" %finish
      y=y+[finish]
      e=e+[pe]
      f.write(str(finish) + '\n')
      f.write(str(pe) + '\n')
   f.close()
   
   print y
   

   
   
 #  graf1= pl.subplot(211)
 #  pl.plot(e,umbral, 'r--')
 #  pl.xlabel("Porcentaje")
 #  pl.ylabel("Umbral")
   
   graf2=pl.subplot(212)
   pl.plot(x,y, 'r--')
   pl.xlabel("Intervalos")
   pl.ylabel("Tiempo")
   
   pl.savefig("Graficas.eps", dpi=72)
   pl.show()