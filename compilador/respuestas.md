

1-

El proceso de compilación se realiza en 4 etapas:

1.1- Pre-procesa y traduce el lenguaje de C a assembler
1.2- Se realiza una optimizacion a un lenguaje intermendio.
1.3- Optimizacion de Hardware. y creacion del objeto. ".o"
1.4- Enlazar al objeto ".o" y generar .exe, se puede linkear de forma estatica(Lo copia al main) o dinamica(Le da la ubicacion).

2-se Pre-Porcesa con gcc -E calculator.c -o calculator.pp.c, esto hace que se declaren las funciones y le dice a futuros pasos que no haga nada hasta que llegue el fin del proceso. Informa que las funciones son externas y las guarda para que puedan ser linkeadas al final.

3- Se observa, el lenguaje assembler, el cual traduce C a un lenguaje intermedio como es el asm. Estan precentes las funciones call pintf y call numbers.


4- Obtenermos un codigo binario que al verlo con nm tenemos: 000000000000003c T add_numbers
0000000000000000 T main (definido en el texto)
                 U printf (No definido)
.

5- Se genera en este paso un archivo.e, que sera nuestro ejecutable el cual al verlo con nm, tenemos muchos mas desciptores comparado con los del objeto.
