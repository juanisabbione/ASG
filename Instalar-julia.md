# Instalar Julia en Debian/Ubuntu

&nbsp;
## Chequear arquitectura de la computadora


Chequear cuál es la *arquitectura* de la computadora en una terminal utilizando el comando `uname -i`.
	
Si la máquina es de 64 bits, se leerá:

	juani@sigma:~$ uname -i
	x86_64
	
Y si la máquina es 32 bits se leerá:

	juani@sigma:~$ uname -i
	i386

*Nota*: En mi computadora, `juani` es el nombre de mi usuario, y `phi` es el nombre de mi computadora.

## Instalar Julia


1. Descargar el archivo comprimido `.tar.gz` que contiene los archivos binarios del Julia "Generic Linux Binaries for x86" que corresponde a la arquitectura de la maquina (64 o 32 bits) de la página oficial de [Julia (link)](https://julialang.org/downloads/). El archivo debe ser descargado en algún lugar adecuado, por ejemplo en `juani@sigma:~/Julia` o en `juani@sigma:~/Julia`.

2. Descomprimir y extraer el archico comprimido utilizando por ejemplo:

	tar -xvzf julia-x.y.z-linux-x86\_64.tar.gz
	
donde `x.y.z` es lo que marca la versión actual del Julia. Esto va a extraer todos los archivos a un directorio llamado `julia-x.y.z`, que será lo que llamemos `directorio de Julia`. 

3. Hacer que Julia corra desde cualquier directorio en el que uno esté parado. Para ello, tenemos que hacer "visible" el archivo ejecutable `<directorio de Julia>/bin/julia` en todo lados. Para esto, usar una de las sguientes dos opciones.
	1. Hacer un link simbólico en algún lugar del `PATH`, como por ejemplo en `/usr/local/bin`:
