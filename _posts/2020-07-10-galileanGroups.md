---
layout: post
title: Grupos Galileanos y el Principio de la Relatividad
image: galileo_galilei.jpg
---

## Introducción

En el corazón de la mecánica analítca hay dos hechos experimentales que son fundamentales: el _principio de la relatividad Galileana_ y el _principio de la determinación de Newton_.  En resumen, estos establecen lo siguiente:
- **Principio de Relatividad**:
  - Todas las leyes de la física en todos los instantes de tiempo son iguales en todos los marcos de referencia inercial.
  - Todos los marcos de referencia que cuyo movimiento es rectilineo y uniforme respecto a un marco de referencia inercial son inerciales
- **Principio de la Determinación**:
  - La posición y velocidad inicial(es decir, el estado inicial) determina de manera única todo el movimiento del sistema.

Ademas de eso, también observamos que el espacio es tri-dimensional y euclideano(esto quiere decir que la distancia entre dos puntos en este espacio es la que te enseñaron en escuela superior) y el tiempo es uni-dimensional y siempre se mueve hacia delante.

Normalmente cuando se menciona el principio de relatividad siempre se cree que fue Einstein quien lo desarrolló. Sin embargo, las nociones inciales fueron desarrolladas por Galileo Galilei y expuestas en el 1638 en su libro Dos Nuevas Ciencias. Su motivación para desarrollarla salió del problema de una bola rodando por una rampa y el movimiento de proyéctiles. De estos tambien introduce la ley de la _composicionalidad de la velocidad_, donde la descripción del movimiento de un objeto se puede "romper" en movimientos separados respecto a cada componente de su velocidad. 

La necesidad del principio de la relatividad es evidene cuando notamos que sin el no podriamos establecer leyes o teorias físicas que sean consistentes en cualquier situacion. La física es la misma en San Juan que en Tokyo, y es la misma la de hoy que la que los cavernícolas observaban milenios atrás. Matemáticamente, esto trae ciertos trucos que nos ayudan a simplificar el razonamiento siempre y cuando estos principios se cumplan.

## El Grupo Galileano

Para poder entender mejor la naturaleza matemática de lo que acabamos de hablar, establecemos algunas definiciones útiles:
- **Espacio Afín N-Dimensional**: denotado como $$A^{n}$$, se distingue de $$\mathbb{R}^{n} $$ en que este no tiene un origen fijo. Los desplazamientos paralelos en este espacio forman $$\mathbb{R}^{n}$$. La suma de dos elementos en $$A^{n}$$ no tiene sentido ya que no hay origen, pero su resta si y es un vector en $$\mathbb{R}^{n}$$.
  
- **Estructura Euclideana sobre $$\mathbb{R}^{n}$$**: basicamente el producto escalar $$\langle x , y \rangle = \left\Vert x - y \right\Vert$$. Esto nos ayuda a definir la distancia entre dos puntos en un espacio vectorial $$\mathbb{R}^{n}$$.
- **Espacio Euclideano**: un espacio afín con una estructura euclideana.

Por ultimo, definimos el Espacio-Tiempo Galileano, cuya estructura es compuesta de:
- **Universo** - Un espacio afín de 4 dimensiones $$A^{4}$$. Los puntos en este espacio se conocen como eventos y sus desplazamientos paralelos forman un espacio vectorial $$\mathbb{R}^{4}$$.
- **Tiempo** - Una relación lineal $$t : \mathbb{R}^{4}  \rightarrow \mathbb{R} $$ que va desde el espacio vectorial de desplazamientos paralelos del universo al eje real del tiempo. El intervalo de tiempo entre un evento $$a$$ y $$b$$ tal que $$a, b \in A^{4}$$ es el numero real $$t(b-a)$$. Dos eventos se consideran simultáneos si $$t(b-a) = 0$$ y el conjunto de eventos simultaneos forman un subespacio afín $$A^{3}$$ del Universo.
- **Métrica** - Definición de distancia entre dos eventos simultáneos: $$ \rho(a,b) = \left\Vert a - b \right\Vert = \sqrt{\left(a-b, a-b\right)};$$  $$a,b \in A^{3}$$  
  Osea, un producto escalar en $$\mathbb{R}^{3}$$ Esto implica que los espacios afínes antes mencionados son todos Euclideanos.
  
Un espacio $$A^{4}$$ que posea estas propiedades de espacio-tiempo es un **Espacio Galileano**. Las transformaciones que affines que preservan los intervalos de tiempo entre eventos y la distancia entre eventos simultáneos se conocen como **Transformaciones Galileanas**. Note que estas tienen un constreñimiento adicional que las transformaciones affines típicas, pues por lo general una transformación afín no tiene que preservar la longitud entre dos puntos en un espacio afín, solo que preserve la linea(es decir, que no se curveen) y sus paralelismos. 

El conjunto de todas estas transformaciones en este espacio es entonces el *Grupo Galileano*.

## Transformaciones Galileanas
Consideremos un _Espacio de Coordenadas Galileano_, es decir, el producto cartesiano entre el eje real de tiempo y el espacio vectorial real $$\mathbb{R} \times \mathbb{R}^{3}$$. Entonces las instancias de transformaciones galileanas son:
1. Movimiento uniforme a velocidad $$\pmb{v}$$:  
   $$g_{1}(t, \pmb{x}) = (t, \pmb{x} + \pmb{v}t)$$
2. Traslación del origen:  
   $$g_{2}(t, \pmb{x}) = (t + a, \pmb{x} + \pmb{k})$$
3. Rotación de ejes de coordenadas:  
   $$g_{3}(t, \pmb{x}) = (t, R\pmb{x})$$  
   donde $$R \in O(3) $$ es una matriz ortogonal

Las transformaciones afínes se pueden generalizar a la forma:  
  $$G(t, \pmb{x}) = A[t, \pmb{x}]^\intercal + \pmb{K} $$

Donde $$A$$ es una matriz $$\mathbb{R}^{4 \times 4}$$. En su forma general, esta transformación puede rotar, cambiar escalas y trasladar. Para facilitar el análisis, consideremos que tiene la matriz $$A$$ tiene la forma:  
  $$ A =  \begin{bmatrix} A_{11} & A{12} \\ A_{21} & A_{22} \end{bmatrix}$$  
Los requisitos, como ya sabemos, es que para que esto sea una transformación galileana tiene que preservar distancias entre eventos simultáneos e intervalos de tiempo entre eventos. Para que se puedan preservar las distancias, $$A_{22}$$ debe ser una matriz ortogonal $$O(3)$$. Para preservar las distancias de tiempo, "evaluemos" la segunda linea del producto de la matriz con un intervalo arbitrario $$t_{2} - t_{1}$$ y distancia $$x_{2} - x_{1}$$ y luego eso nos tiene que dar el mismo intervalo de tiempo:  
 $$ A_{11}(t_{2} - t_{1}) + A_{12}(x_{2} - x_{1}) = t_{2} - t_{1} $$

En la ecuación vemos que para que la igualdad se mantenga, $$A_{11} = 1$$ y $$A_{12} = 0$$. Para generar movimientos uniformes de un espacio de coordenadas, $$A_{21} = \pmb{v}$$ y por ultimo, para generar traslaciones de origen:  
$$\pmb{K} = [a, \pmb{k}]^\intercal$$

Asi que la forma general y única de una transformación galileana es:
$$ G: \begin{bmatrix} t \\ \pmb{x} \end{bmatrix} \rightarrow \begin{bmatrix} 1 & 0 \\ \pmb{v} & R \end{bmatrix} \begin{bmatrix} t \\ \pmb{x} \end{bmatrix} + \begin{bmatrix} a \\ \pmb{k} \end{bmatrix} $$

Todos los espacios galileanos son mutuamente isomórficos y son isomórficos a $$\mathbb{R} \times \mathbb{R}^{3}$$

## Constreñimientos Relativisticos en el Movimiento
Habiendo ya estudiado el Grupo Galileano, ahora tenemos que preguntarnos: ¿Cómo eso influye las ecuaciones de movimiento de un sistema?

Primero definamos el movimiento de manera matemática. Sea $$\pmb{x}_{i} : I \rightarrow \mathbb{R}^{n}$$ donde $$I = [a, b] \in \mathbb{R}$$ es un intervalo de tiempo y supongamos que $$ x \in \mathcal{C}^{\infty} $$, osea, continuamente diferenciable aunque para estos propositos solo necesitamos que la funcion sea hasta dos veces diferenciable. 
Naturalmente, su primera y segunda derivada corresponden a la velocidad y acceleración del sistema. A esta función tambien se le conoce como "linea del mundo" o trayectoria, y aunque la primera suena mas chévere y dramática voy a utilizar la segunda porque es mas práctica. Esta función describe el movimiento de una particula $$i = (1, 2, \dots, n)$$ en un sistema de coordenadas galileano. 
Dada una posición y velocidad inicial, la segunda ley de Newton establece que existe únicamente una función $$F_{i} : \mathbb{R}^{N} \times \mathbb{R}^{N} \times \mathbb{R}$$ $$N = 3n$$ tal que:  
 $$ \ddot{\pmb{x}}_{i}(t) = F_{i}(\pmb{\pmb{x}, \dot{\pmb{x}}}, t)$$  
y cuya solución determina el movimiento del sistema de $$n$$-partículas. Note que $$\pmb{x}$$ es el conjunto de todas las $$\pmb{x}_{i}$$. 

Debido a que $$F_{i}$$ esta definida en un sistema de coordenadas inercial, esta debe ser tambien _invariante_ las transformaciones Galileanas. 
### Invarianza al Tiempo
Si $$x = h(t)$$ es una solución a la ecuación de Newton, entonces $$x = h(t+a)$$ también lo es, lo que implica que $$F_{i}$$ pierde su dependencia del tiempo en un sistema coordenado inercial y como $$F_{i}$$ es una descripción del sistema, entonces tambien implica que _las leyes de la fīsica son constantes_.
$$  \ddot{\pmb{x}}_{i}(t) = F_{i}(\pmb{\pmb{x}, \dot{\pmb{x}}})$$ 
### Invarianza a Traslaciones en el Espacio
Similar a como empezamos anteriormente, si $$x = h(t)$$ es una solución entonces $$x = h(t) + vt + k $$ también lo es. Esto lo que implica es que $$F_{i}$$ no depende de posiciones absolutas o de velocidades absolutas. Es decir, solo depende de posiciones y velocidades relativas:
$$  \ddot{\pmb{x}}_{i}(t) = F_{i}(\pmb{x}_{j} - \pmb{x}_{k} , \dot{\pmb{x}}_{j} - \dot{\pmb{x}}_{k} )$$

Es decir, el espacio es _homogeneo_, las leyes de la física son iguales en todos lados.

### Invarianza a Rotaciones

Sea $$R: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$$ una transformación ortogonal, y $$x$$ una solución, entonces $$Rx$$ tambien es una solución. 
Osea que:  
$$\begin{align*} R\ddot{\pmb{x}}_{i}(t) & = RF_{i}(\pmb{x}_{j} - \pmb{x}_{k} , \dot{\pmb{x}}_{j} - \dot{\pmb{x}}_{k} ) \\ \ddot{\pmb{x}}_{i}(t) & = F_{i}(R(\pmb{x}_{j} - \pmb{x}_{k}) , R(\dot{\pmb{x}}_{j} - \dot{\pmb{x}}_{k}) ) \end{align*}$$

Lo cual implica que el espacio es isotrópico, no importa la dirección en la que rotes el experimento(el cual presumimos que es un sistema cerrado), las leyes de la física siguen siendo las mismas.

## "Derivación" de la Primera Ley de Newton

La Primera Ley de Newton, o la Ley de Inercia, es una consecuencia de todo lo que hemos visto. Repasemos que es lo que dice:
>En ausencia de fuerzas, una particula viaja en movimiento uniforme rectilíneo en un sistema de coordenadas inercial

Es decir, que el sistema no exprimenta ninguna acceleración. Pues veamos como explicamos eso con el Principio de Relatividad.

Supongamos que tenemos una particula cuya trayectoria en un sistema de coordenadas inercial es $$\pmb{x} : I \rightarrow \mathbb{R}^{3}$$. Entonces, por segunda ley de Newton, tenemos una función $$F : \mathbb{R}^{3} \times \mathbb{R}^{3} \times \mathbb{R}$$ tal que:  
$$\ddot{\pmb{x}}(t) = F(\pmb{\pmb{x}, \dot{\pmb{x}}}, t)$$ 
Sin embargo, por invarianza al tiempo, tenemos:  
$$\ddot{\pmb{x}}(t) = F(\pmb{\pmb{x}, \dot{\pmb{x}}})$$ 
Por invarianza a traslación en el espacio, podemos mover el origen del sistema de coordenadas a la particula tal que:  

$$\ddot{\pmb{x}}(t) = F(0, 0)$$  
Lo cual implica que la fuerza es alguna constante, pues pierde sus dependencias en posicion, velocidad y tiempo. Por invarianza a la rotación  
$$ RF(0,0) = F(0, 0) $$  
Cuando unico esto es cierto para un vector constante es cuando es igual a cero(o cuando no hay rotación, pero eso es trivial). Por lo tanto:  
$$ \ddot{\pmb{x}}(t) = 0 $$   
Lo cual implica que la particula viaja a velocidad constante. Asi que la Ley de Inercia es una consecuencia del Principio de Relatividad de Galileo.