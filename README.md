# Tarea Teoria cuantica basica Observables y Medidas

En este trabajo, estoy desarrollando una serie de simulaciones y cálculos relacionados con sistemas cuánticos, basándome en el **Capítulo 4** del libro *Quantum Computing for Computer Scientists*. La idea principal es modelar el comportamiento de sistemas cuánticos en términos de vectores de estado (kets) y observables, aprovechando las herramientas matemáticas que proporciona la teoría cuántica, como la representación matricial de los observables, valores propios, y la evolución temporal de los estados. El objetivo final es resolver una serie de problemas propuestos en el libro y añadir ejemplos prácticos.

Capítulo 4: Retos de Programación y Ejemplos

1. Amplitud de transición
He comenzado por definir un vector de estado \(|\psi\rangle\) que describe una partícula confinada en un conjunto de posiciones discretas. La primera tarea fue calcular la **probabilidad de encontrar la partícula en una posición particular** en función del vector de estado. Posteriormente, definí una función que, dado otro vector de estado \(|\phi\rangle\), calcularía la **probabilidad de transición** de \(|\psi\rangle\) a \(|\phi\rangle\). Utilizando el producto interno entre ambos estados, puedo determinar la amplitud de transición y, a partir de esto, obtener la probabilidad.

Código: He implementado las funciones que calculan tanto la probabilidad de encontrar la partícula en una posición como la probabilidad de transición entre dos estados cuánticos. Utilicé ejemplos con kets definidos por vectores complejos, lo que me permitió comprobar que los cálculos son correctos.

2. Media y Varianza de un Observable Hermitiano
En la segunda parte, el desafío fue comprobar si una matriz es hermitiana, lo que significa que es igual a su traspuesta conjugada. Los observables en la mecánica cuántica se representan mediante matrices hermitianas, por lo que esta verificación es clave. Luego, se desarrollaron las funciones para calcular la **media (expectativa)** de un observable dado un estado y, además, la varianza, que mide la dispersión de los resultados de una medición cuántica.

Código: He implementado la función `es_hermitiana()` para verificar si una matriz es hermitiana. También creé funciones para calcular la media y varianza de un observable. Estos cálculos están basados en operaciones matriciales entre el observable y el vector de estado. Los ejemplos incluían matrices sencillas y kets en forma de superposiciones.

3. Valores propios y probabilidades de transición
En la siguiente sección, pasé a calcular los **valores propios (eigenvalues)** y **vectores propios (eigenvectors)** de un observable. Esto es importante porque en un sistema cuántico, cuando se mide un observable, el sistema colapsa a uno de sus estados propios con una probabilidad que depende del estado cuántico antes de la medición. Las probabilidades de transición hacia estos vectores propios están dadas por el cuadrado del producto interno entre el estado inicial y los autoestados.

Código: Implementé una función que, dada una matriz observable y un vector de estado, calcula los valores propios y las probabilidades de transición hacia los vectores propios. Utilicé el ejemplo de un observable hermitiano simple con valores propios conocidos, y los resultados concuerdan con las expectativas teóricas.

4. Evolución temporal (dinámica del sistema)
En esta parte, desarrollé una simulación de la **evolución temporal** de un sistema cuántico. Para esto, consideré una serie de operadores unitarios \(U_n\) que actúan sobre un estado inicial. Estos operadores representan la evolución del sistema en el tiempo, y su aplicación sucesiva al estado inicial produce el estado final.

Código: He definido una función que toma una lista de operadores unitarios y un estado inicial, y calcula el estado final después de aplicar todos los operadores. Utilicé ejemplos con matrices como el operador Pauli-X y el operador de fase, demostrando cómo evolucionan los estados bajo la acción de estos operadores.

Ejercicios del Libro

En el capítulo 4 también se incluyen varios ejercicios, de los cuales he comenzado a resolver algunos de los más importantes:

Ejercicio 4.3.1: Me pidió encontrar todas las probabilidades de transición del estado \(|\psi\rangle\) hacia los diferentes autoestados de un observable. El concepto clave aquí es que la probabilidad de transición está dada por el cuadrado del valor absoluto del producto interno entre el estado \(|\psi\rangle\) y cada uno de los autoestados \(|e_i\rangle\). Este ejercicio me ayudó a poner en práctica los conceptos de valores propios y probabilidades de transición.

Código: Implementé los cálculos descritos y verifiqué la correcta implementación de las funciones para obtener los resultados correctos.

Ejercicio 4.3.2: Este ejercicio me pidió repetir los cálculos del ejercicio anterior y, además, **graficar la distribución de probabilidad de los valores propios. El gráfico resultante muestra las probabilidades de transición del estado inicial hacia cada uno de los autoestados, lo que proporciona una representación visual de la probabilidad cuántica.

Código: Usé la librería `matplotlib` para generar una gráfica de barras que muestra las probabilidades de transición en función de los valores propios. Esto permitió visualizar los resultados de manera más clara.
