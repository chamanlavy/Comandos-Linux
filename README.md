# Cómo saber qué versión de Linux tenemos?

*Como muchos saben, hay muchas (muuuuchaaaaassss) versiones de Linux* y a veces se nos hace muy difícil poder distinguir una de otra distro. Vamos, con más de once entornos gráficos distintos, con 5379 distros oficiales a la fecha y las customizaciones que hacen los usuarios hacen que sea realmente muy difícil saber a la rápida.

Por ello, me animé a dejar este minitutorial express para que sepas fácilmente con qué sistema operativo estás trabajando (y así no cometer errores al momento de ingresar los comandilos)

**Advertencia: nunca está de más decir que siempre es bueno pedir ayuda en caso de no saber con exactitud lo que uno está haciendo**
(te lo dice alguien que en más de una ocasión dejó su distro tan muerta como un ladrillo)

## Screenfetch

1- Abrir terminal (a veces funciona con ctrl + alt + f3, o en otros casos con f12)
2- En el terminal intentar instalar el siguiente programa digitando el siguiente comando:

  ~~~
sudo get-apt install screenfetch

~~~

Si funciona, entonces eso significa que es la distribución que estamos usando es de las más conocidas (Debian, las mil distros de Ubuntu, Elementary OS o Linuxmint)

**Pero antes de continuar ... qué es Screenfetch?**

Es sencillo! Screenfetch es un programa (o una utilidad de líneas de comandos) que muestran gráfica y amigablemente los datos asociados a tu versión de Linux. Con Screenfetch puedes obtener la siguiente información:

- nombre de la distro
- versión del kernel
- uptime
- paquetes instalados en el sistema
- nombre y versión del shell
- resolución de pantalla
- nombre y versión del entorno de escritorio
- administrador de ventana
- tema, tipografía
- información de CPU, GPU y memoria RAM

Si por alguna razón no funciona este comando o arroja un msj de error, prueba con este comando (de funcionar, sería una distro derivada de Fedora o Red Hat)

  ~~~
sudo dnf install screenfetch

~~~

Y si aún así no funciona, prueba con el comando de abajo (de funcionar, sería una distro derivada de Arch Linux o Manjaro)

  ~~~
sudo pacman install screenfetch

~~~

(en el caso de que no funcione, podemos probar con un comando que dejaré más adelante ;)

3- Una vez instalado el programa, simplemente escribimos "screenfetch"

~~~
screenfetch

~~~

Y nos aparecerá información gráfica en el terminal, gracias a una simpática combinación de colores y caracteres en formato ASCII, con el logo y los datos antes mencionados!

![Captura de muestra](https://4.bp.blogspot.com/-5M9piCn9EOg/WSBtVzFd_XI/AAAAAAAAJqM/bxauZsYVWMkA9XXSxKvr1RVvtNsdg-YLQCLcB/s640/06%2BPantheon%2Bterminal.jpg)


**Pero ... y si no pude instalar screenfetch?**

En ese caso, podemos usar un comando más sencillo.


## Uname

Este comando es muy potente, ya que no sólo funciona en Linux (tb en FreeBSD), y a diferencia de screeenfetch no necesitas permisos de superusuario.

~~~
uname -a

~~~

En el caso que quieras probar con información que te puede mostrar el comando UNAME, puedes copiar el código de abajo y el terminal te dará todas las opciones disponibles.

~~~
uname --help

~~~

Por ejemplo, al ingresar ese comando en el terminal de mi pc, me aparece la siguiente información:

>Linux atlas 5.4.0-62-generic #70~18.04.1-Ubuntu SMP Tue Jan 12 17:18:00 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux

Eso significa que mi equipo cuenta con sistema "linux", se llama "atlas", posee el kernel 5.4 genérico y -supuestamente- está basado en Ubuntu 18.04.
Además, la última actualización por terminal fue el 12-ene a las 5:18, y la arquitectura de mi equipo es una x-86 con procesador 64 bits. *Sexy, no es cierto?*


## Entonces, cuál opción debo elegir?

Excelente pregunta! En mi caso, prefiero siempre *ambas*, y en el orden mostrado. Porqué? muy sencillo: Screenfetch muestra info que no puede mostrar UNAME, y UNAMe no muestra información del todo exacta (por ejemplo, en mi pc tengo Elementary OS que es una distro derivada de Ubuntu y Debian ... pero UNAME la reconoce como Ubuntu). Por ello mi consejo sería ejecutar ambas, ya que la combinación de esos tres comandos te ayudará a obtener rápidamente la información del equipo que estás usando. Siempre y cuando tengas la clave SUDO o que tengas permisos de administrador.

>Espero te sirva mi minitutorial! próximamente subiré un tutorial para instalar la última versión de python en Linux y cómo instalar Rstudio en Elementary OS.
>Personalmente, me encantan esos dos temas porque hay muy poca info sobre ello y tras mucho tiempo de pelear con el pc, pude ganar esta batalla ... *al menos >hasta que liberen la versión 6 de Elementary OS*.

Cualquier duda o consulta, puedes escribirme a mi [perfil de Linkedin](https://www.linkedin.com/in/carlos-chaman/)
