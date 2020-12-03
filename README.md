# Tema5

###### En esta asignación se solicita modificar el archivo L5.ipynb para que el servidor esté vacío por no más del 10% del tiempo. Se hicieron varios códigos y se simuló el programa para verificar la funcionalidad del mismo. 

###### Lo primero que se hizo fue tomar en cuenta que para que el servidor no esté vacío por más del 90% del tiempo, el servidor debe tener un cliente o más en el sistema. Siendo así, se puede utilizar la fórmula que aparece en la teoría al inicio de este laboratorio. Haciendo uso de esta, nos damos cuenta de que para que la condición solicitada se cumpla, el servidor deberá tener al menos 2.11 usuarios por minuto. 

###### Con respecto al código, se hicieron varios cambios. Se modificó el umbral par calcular el tiempo en el que no hay usuarios. Para esto P = 0 y debe indicarse al for que hay que sumar cada momento en el que la cantidad de usuarios es igual a P = 0. 

          # Recorrido del vector temporal y conteo de clientes (estado n)
                for i, c in enumerate(t):
                n += c # sumar (+1) o restar (-1) al estado
                Xt[i] = n
                if Xt[i] == P: 
                frecuencia += 1
                
 ###### Se actualizó el valor que da la condición máxima para cuando se cumple que el servido esté vacío por más del 10%
                if fraccion <= 0.1:
                    print('\t Sí cumple con la especificación.')
                else:
                    print('\t No cumple con la especificación.') 
