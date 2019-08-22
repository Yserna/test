# test

# lab-Memory-API
file:///home/yenni/LabSO/Lab-Memory-API/1.png

Memory API
En este laboratorio ganará algún grado de familiaridad con la asignación de memoria (memory allocation). Para el caso, ustedd escribirá algunos programas con bugs. Luego, usará algunas herramientas para localizar los bugs que usted ha insertado. De este modo se familiarizará con algunas de estas herramientas para un uso futuro. Estas herramientas son: el debuger (gdb) y el memory-bug detector (valgrind).

Questions
Escriba un programa simple llamado null.c que cree un puntero a un entero, llevelo a null y entonces intente desreferenciarlo (esto es, asignarle un valor). Compile este programa llamado null. ¿Qué pasa cuando usted ejecuta este programa?

Compile el programa del ejercicio anterior usando información de simbolos (con la flag -g). Al hacer esto se esta poniendo mas informacion en el ejecutable para permitir al debugger acceder a informacion util sobre los nombres de las variables y cosas similares. Ejecute el programa bajo el debugger digitando en consola (para el caso) gdb null y entonces una vez el gdb este corriendo ejecute run. ¿Qué muestra gdb?

Haga uso de la herramienta valgrind en el programa empleado en los puntos anteriores. Se usará la herramienta memcheck que es parte de valgrind para analizar lo que pasa: valgrind --leak-check=yes null. ¿Qué pasa cuando corre esto?, Â¿Puede usted interpretar la salida de la herramienta anterior?

Escriba un programa sencillo que asigne memoria usando malloc() pero olvide liberarla antes de que el programa termina. ¿Qué pasa cuando este programa se ejecuta?, ¿Puede usted usar gdb para encontrar problemas como este?, ¿Que dice acerca de Valgrind (de nuevo use este con la bandera --leak check=yes)?

Escriba un programa que cree un array de enteros llamado data de un tamaño de 100 usando malloc; entonces, lleve el data[100] a 0. ¿Qué pasa cuando este programa se ejecuta?, ¿Qué pasa cuando se corre el programa usando valgrind?, ¿El programa es correcto?

Codifique un programa que asigne un array de enteros (como arriba), luego lo libere, y entonces intente imprimir el valor de un elemento del array. ¿El programa corre?, ¿Que pasa cuando hace uso de valgrind?

Ahora pase un funny value para liberar (e.g. un puntero en la mitad del array que usted ha asignado) ¿Qué pasa?, ¿Ústed necesita herramientas para encontrar este tipo de problemas?
