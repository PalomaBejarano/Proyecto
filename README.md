# Proyecto

Esta es una función básica para calcular particiones binarias (es una de las más sencillas que uso para las investigaciones que hago en mi doctorado).





```
ParticionBinaria= function(x, iter){ #Acepta un vector de puntos x, devuelve la particion binaria entre los puntos de x despues de un numero de iteraciones
  
  for(t in 1:iter){
    
    n=2*length(x)-1
    z=rep(0,n)
    v=rep(0,length(x)-1)
    tam = length(x)
    cont1 = 1
    cont2 = 1
    
    for (j in 1:tam){
      v[cont1] = 0.5*(x[j]+x[j+1])
      cont1 = cont1 + 1
    }
    
    for (i in 1:(tam-1)){
      z[cont2] = x[i]
      z[cont2+1] = v[i]
      cont2 = cont2+2
    }
    z[cont2] = x[tam]
    x=z

    }
  return(z)
  
  #Por ejemplo
  #ParticionBinaria(c(0,),3) ```
  