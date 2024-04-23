# PacManIA
Uso me métodos de IA para jugar al juego PacMan

Introducción
El trabajo futuro se centrará en desarrollar una inteligencia artificial capaz de jugar Pac-Man de manera autónoma y completar niveles de manera eficiente. El problema principal a abordar es la complejidad inherente del juego, que incluye la navegación en un laberinto dinámico mientras se evitan los fantasmas y se recolectan puntos. La solución propuesta consistirá en diseñar un algoritmo de aprendizaje por refuerzo que permita a la IA aprender estrategias efectivas para navegar el laberinto, evitar a los fantasmas y maximizar la puntuación. Esto implicará el uso de técnicas avanzadas de aprendizaje automático y la integración de sistemas de percepción para analizar el entorno del juego en tiempo real. El objetivo final es crear una IA que pueda adaptarse a diferentes situaciones de juego y demostrar un alto nivel de rendimiento en la tarea de completar niveles de Pac-Man de manera autónoma.


Descripción del ambiente: En este juego los estados y las acciones son finitas y específicas, por lo que trabajamos con un ambiente discreto. Además, en el escenario del juego los fantasmas toman acciones aleatorias y PacMan tiene una selección de acciones para tomar en cada estado, las pildoras de invulnerabilidad y la comida de Pacman aparece y desaparece, por lo que se trata de un ambienete dinámico. Por último, el conjunto de acciones que pueda tomar el jugador puede llevar a distintos tipos de resultados, por ejemplo si Pacman se mueve hacia arriba puede o no encontrar comida o una píldora de invulnerabilidad, así como también avanzar o no, dependiendo si no se encuentra con un muro, debido a esto definimos nuestro ambiente como Estocástico.

Representación del ambiente: El escenario del juego se representará por una matriz bidimensional de objetos compuesta por una lista de listas. Se accede a los datos a través de grid[x][y] donde (x,y) son posiciones en un mapa de Pacman con x horizontal, y vertical y el origen (0,0) en la esquina inferior izquierda.

Descripción de las acciones que puede tomar el agente: El/Los agentes podrán tomar las siguientes acciones discretas: 
North: Moverse hacia el norte.
South: Moverse hacia el sur.
East: Moverse hacia el este.
West: Moverse hacia el oeste.
Stop: Detenerse en su posición actual.

Estas acciones son discretas ya que el agente puede seleccionar una de estas direcciones de movimiento en cada paso. El dominio de cada acción es el conjunto de direcciones posibles en el tablero de Pacman, es decir, el conjunto de las cuatro direcciones cardinales (norte, sur, este, oeste) y la acción de detenerse.

Representación concreta de las acciones: La representación concreta de las acciones en este caso sería utilizando un conjunto de pares dirección-vector para representar las direcciones de movimiento. Se guarda la posición del vector (x,y) del jugador y la dirección definida en la clase 'Directions' que tomará. Estas constantes son strings que representan las direcciones de movimiento: "North", "South", "East", "West" y "Stop". Por lo tanto, la estructura de datos utilizada para representar estas acciones es simplemente un conjunto de strings.

Integrantes:
Juan Henderson
Sebastián Rosas
Franco Espinosa
Andrés Lartiga
