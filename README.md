# ¿Qué es Git ?

Tal vez te lo hayas preguntado, tal vez no. Git es una de las herramientas
más utilizadas para manejar código fuente en proyectos de software. Pero
puede ser utilizado para otras cosas, como manejar el historial de una 
imagen que estás editando en photoshop, hacer cambios, hacer versiones
basadas en ciertos cambios, hacer [poemas](https://youtu.be/BCQHnlnPusY)
y muchas cosas mas!

Cualquier cosa que parezca - o bien, sea - un archivo podrá ser revisado 
y *cuidado* por **git**.

al final veremos github.

# historia
git fue creado por uno de los legendarios en la historia de la computación
(al menos en mi opinión). Fue creado para simplemente manejar otro proyecto
que Linus (Torvalds) tenía: **Linux**,*una versión libre y open source de un
kernel para sistemas Unix/posix*. El chiste es que, como su proyecto -Linux-
era tan inmenso, no podía manejar el desarrollo de manera fácil, o al menos 
una en la que le gustara. Por eso creó git, para permitir la facilitación del
manejo de código fuente de Linux.

# what

Git es un software que te permite registrar y 'espiar' el historial de un archivo.
Esto no quiere decir que cuando instales Git te espiará. Como desarrollador, tu
tienes el control de decirle a *git* **qué** archivo quieres trackear y cuáles **no**
quieres que trackee. Git te permitirá viajar en el pasado, hacer registros de 
cómo era tu proyecto en x o y día, entre otros. Pero me estoy adelantando demasiado.

Un scm, o source control manager, te permitirá colaborar con otras personas en un
proyecto de software. Realmente, eso es todo lo que necesitamos para crear nuestro
código. No tenemos que tener a un 'secretario' que anote todo el código para que 
no se pierda. No tenemos que tener usbs del proyecto. Podemos utilizar el Internet
y hacer un proyecto de Git remoto a través de servicios como Github.

# use

Cómo usar git ? Bueno, es bastante sencillo. Hoy en día puedes descargar algo como
[github desktop](https://desktop.github.com/) para manejar proyectos de git, pero podrías
también instalar git así nomas y utilizarlo desde una shell o una línea de comandos
( pa que parezcan hackers).

Todavía no descargues Github desktop! Es mucho más importante que primero sepas
qué pasa en git.

Primero que nada cuando creamos un proyecto de git (`git init tecbot-code`) se generará
una nueva carpeta, aparentemente conteniendo nada. Pero de hecho, contendrá un
directorio 'escondido' en donde se guardará la información de git. Este directorio se
llama `.git`. Ahora que ya hemos creado un repo(sitorio) podremos agregar archivos,
cualquier tipo. Usualmente agregaremos archivos de código fuente (es decir, archivos
que son legibles por humanos, no compilados). Puedes agregar archivos con cualquier
nombre. Pero espera! No creas que mágicamente git ya se habrá comunicado con el equipo
y haya creado y compartido un repositorio remoto. Primero deberás *agregar* los archivos
a git. Tendrás que decirle **oye git, quiero empezar a grabar el historial de este archivo**
Y entonces git te dirá, bueno pues, tendré este archivo en cuenta para cada commit.
Espera, qué es un commit ? Bueno, es una palabra difícil de traducir al español. Literalmente,
quiere decir **comprometerse**. Cada vez que realizas un `commit` le estás diciendo a 
git, oye quiero que te *comprometas* decirme qué le pasó a mi archivo en este momento (en el
momento en el que se realizó el commit). Cada vez que haces un commit estás diciéndole a git,
oye, git, quiero que me digas qué cambios han habido para todos estos archivos.

Cada vez que realices un commit, git no añadirá automáticamente tus archivos. Tu ya le has
dicho a git una primera vez de qué archivos quieres trackear el historial, pero no le has
dicho de *qué* archivo quieres registrar un historial. Es decir, para cada commit, puedes
decidir qué historial de qué archivo registrar. Podrías estar trabajndo en el archivo A,
pero no lo has terminado. Pero ayer hiciste cambios al archivo B y los has terminado. Puedes
realizar un commit sólo registrando el archivo B y hacer un push (sincronizar con un repo
remoto de git) y enseñar los cambios a tus compañeros sólo del archivo B.

Realmente no usaremos opciones muy complejas de git, pero algo que también estaremos utilizando son
ramas. Branches, en inglés. Imagínate las ramas en un arbol, en invierno. Se le han caído todas
las hojas. A simple vista, parecen todas iguales, unas arriba, otras abajo y otras a la derecha.
Conforme te vas acercando, puedes ver que hay unos animales viviendo en algunas ramas, algunas
están rotas, otrás tienen texturas raras, otrás están apunto de caerse. El punto es, conforme te 
vas acercando a cada rama verás que son diferentes. En esta analogía me refiero con las ramas 
a los commits. El árbol siendo nuestro proyecto de git. En terminología de source control
managers, una rama o 'branch' será una serie de commits en git. Las commits pueden empezar desde
cierto punto en tu historial. Es decir, puedo tener una branch `master` que será la principal. Pero
si alguien quiere hacer cambios o simplemente quiere 'jugar' con el código sin que deje de funcionar
para los demás, puede crear su propia branch para poder hacer cambios empezando desde la última
commit al momento de crearlo. y también cuando mis compañeros hayan revisado mi código podremos
decir, ah, este código es perfecto, hay que unirlo a la branch `master`. O también pueden decir,
necesita unos cambios por aquí y por hayá, los hacemos y lo unimos a la branch master.

Git también nos permite hacer magia negra, lo que decía de irnos al pasado, e incluso cambiarlo! y 
por lo tanto cambiar el futuro! 

Para poder colaborar en el código, deberás crear una cuenta de [github](https://github.com) también
puedes seguir algunos de los tutoriales que probablemente te aparecerán si eres nuevo en github
para entender cómo funcionan las cosas.

# github
github permite tener un repositorio en 'la nube' y te permite colaborar con otras personas,
ver de manera grafica quien hizo que, cuando lo hizo, etc. Para manejar las tareas dentro de un
proyecto de software podremos utilizar los 'Issues' para generar tickets describiendo los problemas,
asignando a programadores para hacer tareas y resolviendolos cuando ya esten en el codigo.

# recursos
- [Git and Github for poets](https://thecodingtrain.com/beginners/git-and-github/)
- 
