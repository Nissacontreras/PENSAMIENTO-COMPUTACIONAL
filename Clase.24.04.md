# Aclaraciones solemne

1. En Github existen diferentes tipos de archivo que uno puede crear. Para los apuntes en clases se debe usar .md este es el que se usa para texto y les aceptará el formato con markdown.
2. Es importante llevar las bitácoras al día, tanto la carpeta de cada sesión, como también ejercicios y desafíos.
3. Para agregar código de programación en los apuntes de clases, se debe usar también el formato de markdown. Se hace:
    * '''código''' (bloque de código)  
    *  'código p5' (Se usa entre medio de una oración)
4. Comentar el código de manera formal.
5. angleMode(DEGREES) solo configura el modo de medir los ángulos en grados.


___

## Encargo de la clase pasada 

```
let angulo=0; //Creo una variable llamada angulo y le asigno el valor 0
let x=0; //Creo una variable x y le asigno el valor 0
let y=0; //Creo una variable y y le asigno el valor 0
let creceEllip=0; //Creo una variable llamada creceEllip y le asigno el valor 0
let giraRect=0; //Creo una variable llamada giraRect y le asigno el valor 0
let font; //Creo una variable llamada font
let img; //Creo una variable llamada img

function preload() { //Función para cargar imágenes 
  img = loadImage('flor.jpg'); //Creo la variable para colocar mi imagen
}

function setup() { //Función que se ejecuta una sola vez al inicio del programa
  createCanvas(450, 600); //Crea un lienzo de 450 en x, 600 en y
  angleMode(DEGREES); //Activa el modo ángulos para los arcos
}

function draw() { //Función que se ejecuta en loop constantemente
  background(247, 237, 218); //Pinta el fondo de color crema en valores RGB
  
  //Texto "nip" escrito en 4 líneas, cada una en un color diferente.
  textSize(17); //Asigna el tamaño del texto en 17 px
  fill(237, 114, 170); //Pinta el texto en color rosado claro en valores RGB
  text('nip', 120, 530); //Escribe el texto en las coordenadas x,y
  fill(217, 76, 121); //Pinta el texto en color rosado en valores RGB
  text('nip', 120, 550); //Escribe el texto en las coordenadas x,y
  fill(191, 69, 108); //Pinta el texto en color rosado oscuro claro en valores RGB
  text('nip', 120, 570); //Escribe el texto en las coordenadas x,y
  fill(145, 51, 81); //Pinta el texto en color burdeo en valores RGB
  text('nip', 120, 590); //Escribe el texto en las coordenadas x,y
  
  angulo = angulo+2; 
  x = x+1;
  y = y+0.5;
  creceEllip = creceEllip+1; 
  giraRect = giraRect+1
  
  noStroke(); //Elimina el borde de las figuras
  
  push(); //Comienza un estado de "capa"
  translate(x, y); //Se traslada la figura desde el punto de origen de x,y
  fill(0); //Pinta la figura de color negro
  rect(90, 120, 270, 8); //Crea un rectángulo delgado horizontalmente en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  
  fill(120, 94, 61); //Pinta la figura de color cafe en valores RGB
  arc(225, 350, 270, 270, 0, 180); //Crea un arco en las coordenadas x,y
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Crea las figuras desde el centro
  fill(0); //Pinta la figura de color negro
  
  if (mouseIsPressed === true) { //Condicional: Si se presiona el mouse se cumple lo siguente
  fill(227, 154, 177); //Si lo anterior se cumple, se pinta el rectángulo de color rosado en valores RGB
  rect(170, 415, 10, 188); //Crea un rectángulo en las coordenadas x,y
  } else if (mouseX > 150 && mouseX < 200 && mouseY > 310 && mouseY < 510) { //Condicional: Si el valor de mouseX es mayor a 150 y menor a 200, además el valor de mouseY es mayor que 310 y menor a 510 se cumple lo siguente
  noFill(); //Si lo anterior se cumple no se pinta el rectángulo
  rect(170, 415, 10, 188); //Crea un rectángulo en las coordenadas x,y
  } else {
  fill(0); //Si nada de lo anterior se cumple, se pinta el rectángulo negro
  rect(170, 415, 10, 188); //Crea un rectángulo en las coordenadas x,y
  }
  pop(); //Se cierra el estado de "capa"
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Crea las figuras desde el centro
  stroke(227, 154, 177); //Asigna el color rosado al borde de la figura en valores RGB
  strokeWeight(5); //Asigna el grosor del borde en 5 px
  
  if (mouseIsPressed === true) { //Condicional: Si se presiona el mouse se cumple lo siguente
  fill(120, 94, 61); //Si lo anterior se cumple, se pinta la figura de color cafe en valores RGB
  ellipse(260, 240, 150, 150); //Crea un círculo grande en las coordenadas x,y
  } else if (mouseX > 180 && mouseX < 340 && mouseY > 160 && mouseY < 315) { //Condicional: Si el valor de mouseX es mayor a 180 y menor a 340, además el valor de mouseY es mayor que 160 y menor a 315 se cumple lo siguente
  noFill(); //Si lo anterior se cumple no se pinta el círculo
  ellipse(260, 240, 150, 150); //Crea un círculo grande en las coordenadas x,y
  } else {
  fill(227, 154, 177); //Si nada de lo anterior se cumple, se pinta el círculo de color rosado en valores RGB
  ellipse(260, 240, 150, 150); //Crea un círculo grande en las coordenadas x,y
  }   
  pop(); //Se cierra el estado de "capa"
 
  fill(227, 154, 177); //Pinta la figura de color rosado en valores RGB
  ellipse(260, 60, 50, 50); //Crea un círculo pequeño en las coordenadas x,y 
  ellipse(400, 240, 50, 50); //Crea un círculo pequeño en las coordenadas x,y 
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Las figuras se crean desde el centro
  translate(260,240); //Se trasladan las figuras desde el punto de origen de x,y
  rotate(angulo); //Rota la figura según el ángulo definido
  fill(237, 114, 170);  //Pinta la figura de color rosado claro en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en en las coordenadas x,y
  
  rotate(angulo+2); //Rota la figura según el ángulo definido
  fill(217, 76, 121); //Pinta la figura de color rosado en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+3); //Rota la figura según el ángulo definido
  fill(191, 69, 108); //Pinta la figura de color rosado oscuro en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+4); //Rota la figura según el ángulo definido
  fill(145, 51, 81); //Pinta la figura de color burdeo en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+6); //Rota la figura según el ángulo definido
  fill(99, 35, 56); //Pinta la figura de color burdeo medio en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+8); //Rota la figura según el ángulo definido
  fill(61, 21, 35); //Pinta la figura de color burdeo oscuro en valores RGB
  rect(0, 0, 5, 154); //Crea un rectangulo delgado en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Las figuras se crean desde el centro
  translate(260, 60); //Se trasladan las figuras desde el punto de origen de x,y
  rotate(angulo); //Rota la figura según el ángulo definido
  fill(237, 114, 170); //Pinta la figura de color rosado claro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en en las coordenadas x,y
  
  rotate(angulo+2); //Rota la figura según el ángulo definido
  fill(217, 76, 121); //Pinta la figura de color rosado en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+3); //Rota la figura según el ángulo definido
  fill(191, 69, 108); //Pinta la figura de color rosado oscuro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+4); //Rota la figura según el ángulo definido
  fill(145, 51, 81); //Pinta la figura de color burdeo en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+6); //Rota la figura según el ángulo definido
  fill(99, 35, 56); //Pinta la figura de color burdeo medio en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+8); //Rota la figura según el ángulo definido
  fill(61, 21, 35); //Pinta la figura de color burdeo oscuro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Las figuras se crean desde el centro
  translate(400, 240); //Se trasladan las figuras desde el punto de origen de x,y
  rotate(angulo); //Rota la figura según el ángulo definido
  fill(237, 114, 170); //Pinta la figura de color rosado claro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en en las coordenadas x,y
  
  rotate(angulo+2); //Rota la figura según el ángulo definido
  fill(217, 76, 121); //Pinta la figura de color rosado en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+3); //Rota la figura según el ángulo definido
  fill(191, 69, 108); //Pinta la figura de color rosado oscuro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+4); //Rota la figura según el ángulo definido
  fill(145, 51, 81); //Pinta la figura de color burdeo en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+6); //Rota la figura según el ángulo definido
  fill(99, 35, 56); //Pinta la figura de color burdeo medio en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  
  rotate(angulo+8); //Rota la figura según el ángulo definido
  fill(61, 21, 35); //Pinta la figura de color burdeo oscuro en valores RGB
  rect(0, 0, 3, 50); //Crea un rectangulo delgado en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  push(); //Comienza un estado de "capa"
  translate(70, 170); //Se traslada la figura desde el punto de origen de x,y
  scale(mouseX/50); //Ajusta el tamaño de la figura según la posición x del mouse 
  ellipse(0, 0, 50, 50); //Crea un círculo pequeño en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  push(); //Comienza un estado de "capa"
  rectMode(CENTER); //Las figuras se crean desde el centro
  translate(320, 430); //Se traslada la figura desde el punto de origen de x,y
  rotate(giraRect*30); //Rota la figura según el ángulo definido
  fill(191, 69, 108, 200); //Pinta la figura de color rosado con transparencia en valores RGB
  square(0, 0, 140); //Crea un cuadrado en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  push(); //Comienza un estado de "capa"
  imageMode(CENTER); //Situa la imagen desde el centro
  image(img, 320, 430, 100, 100); //Coloca la imagen en las coordenadas x,y
  pop(); //Se cierra el estado de "capa"
  
  fill(0); //Pinta la figura de color negro
  rect(150, 80, 5, 430); //Crea un rectángulo delgado verticalmente en las coordenadas x,y
  rect(135, 80, 5, 430); //Crea un rectángulo delgado verticalmente en las coordenadas x,y
  rect(120, 80, 5, 430); //Crea un rectángulo delgado verticalmente en las coordenadas x,y
  
}
```
![Encargo4](https://github.com/user-attachments/assets/185e695e-0cd7-4fad-9fd3-90f9360e5759) 


___

# 4 pilares fundamentales 

**1. Descomposición**

"Dividir para conquistar"  
Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y manejables.  
* **En diseño:** No hago todo de una vez. Primero creo una parte, después la otra, luego veo cómo se relacionan entre sí y, al final, agrego los detalles.
* **En el código:** Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante, tienes una función dibujarIconos() y otra calcularDiferencia(), etc.

___

**2. Reconocimiento de patrones**  

"Encontrar similitudes"  
Es observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una lógica constante, podemos automatizarlo.
* **En diseño:** Para representar muchas cosas, no necesito dibujarlas una por una. Por ejemplo, si quiero mostrar muchos árboles, no tengo que dibujar cada uno desde cero, basta con repetir la misma forma cambiando su posición en el espacio.
* **En el código:** Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por ti con solo tres líneas.

___

**3. Abstracción**

"Lo importante vs. el detalle"  
Es filtrar la información que es innecesaria y quedarse solo con las características que definen el problema. Es crear una representación simbólica de la realidad.  
* **En diseño:** No necesito representar todo para transmitir una idea. A veces basta con una figura que se encoge cuando me acerco con el mouse para que se entienda.
* **En el código:** Se traduce en el uso de Variables y la función map(). Una posición de mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.

___

**4. Algoritmo**

"La receta paso a paso"  
Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el "plan de acción" que debe seguir el sistema.  
* **En diseño:** Es el flujo de la experiencia. "Si el usuario hace esto, pasa aquello; si no, pasa esto otro”.
* **En el código:** Se traduce en el Diagrama de Flujo y en las Condicionales (if/else). Es el mapa lógico que conecta todas las partes   anteriores.

___

# Tipos de interacción

1. Interacción discreta (Eventos)  
Es cuando ocurre un evento específico (clic) y el sistema responde con una acción única (aparecen círculos). Es un interruptor de "encendido/apagado" o "acción/reacción".

En el código: Se suele usar dentro de la función mousePressed() o con un if(mouseIsPressed).

2. Interacción Continua (Input de Datos)  
Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad
de hacer algo especifico (clic).

En el código: Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad
de algo.

___

# Funciones Propias

Las **Funciones propias** nos permiten darle modularidad al código.  Y reusabilidad, que nos permite repetir el código.  
Son unas especies de carpetas, para separar cada elemento del código. Cada "carpeta" va a contener cierta acción. 

Ej: function Nombredelafunción(){}

___

## Desafío 1 durante clases

```
let x=0; // Declaro e inicializo la variable x y le asigno el valor 0
let y=0; // Declaro e inicializo la variable y y le asigno el valor 0
let speedX=3; // Declaro e inicializo la variable speedX y le asigno el valor 3
let speedY=6; // Declaro e inicializo la variable speedY y le asigno el valor 6

function setup() { // Esta función de inicio que se ejecuta una sola vez cuando comienza el programa
  createCanvas(400, 400); // Crea un lienzo de 400 px en x, 400 px en y
}

function draw() { // Esta es la función que se ejecuta en loop 60 veces por segundo
  background(217, 30, 123); // Agrego un color fucsia al fondo en valores RGB 
  
  // Llamamos a nuestros módulos (funciones)
  dibujarObjetos();
  moverObjetos();
  comprobarBordes();
  
}
  
function dibujarObjetos() {
  noStroke(); // Configuro que la elipse no tiene borde
  fill(255, 191, 15); // Asigno el color naranjo a la figura en valores RGB
  ellipse(x, 200, 50, 50); // Creo una ellipse en la posición de variable x, y, ancho y alto
  

  fill(255, 191, 15); // Asigno el color naranjo a la figura en valores RGB
  ellipse(200, y, 90, 90); // Creo una ellipse en la posición de variable x, y, ancho y alto
}
  
function moverObjetos() {
  x=x+speedX // La variable x va a ser igual a la variable x + la variable speedX
  y=y+speedY // La variable y va a ser igual a la variable y + la variable speedY
}
  
function comprobarBordes() {
  // Rebote horizontal
  if (x > width || x < 0) { // Si x es mayor que el ancho del lienzo  (400) o x es menor que 0
  print("fueradecuadro") // Imprime en la consola la cadena de texto "fuera de cuadro"
  speedX = speedX * -1; // La variable speedX va a ser igual a la variable speedX multiplicado por -1
  }
  
  // Rebote vertical
  if (y > height || y < 0) { // Si y es mayor que el ancho del lienzo  (400) o y es menor que 0
  print("fueradecuadro") // Imprime en la consola la cadena de texto "fuera de cuadro"
  speedY = speedY * -1; // La variable speedY va a ser igual a la variable speedY multiplicado por -1
  }
}
```

![Pelotita con rebote](https://github.com/user-attachments/assets/d604e28e-c209-4ae3-90dc-6cdcf317cc90)

___

## Desafío 2 durante clases

```
let pelota = {
  x: 300,
  y: 200,
  Xspeed: 4,
  Yspeed: 3,
}

function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(209, 56, 114);
  DibujarFiguras();
  Rebote();
  Movimiento();
}

function DibujarFiguras() {
  stroke(70, 162, 247);
  strokeWeight(4);
  fill(40, 199, 64);
  ellipse(pelota.x, pelota.y, 24, 24);
}

function Movimiento() {
  pelota.x = pelota.x + pelota.Xspeed;
  pelota.y = pelota.y + pelota.Yspeed;
}

function Rebote() {
  if (pelota.x > width || pelota.x < 0) {
    pelota.Xspeed = pelota.Xspeed * -1;
  }
  if (pelota.y > height || pelota.y < 0) {
    pelota.Yspeed = pelota.Yspeed * -1;
  }
}
```

![Rebotes](https://github.com/user-attachments/assets/12199635-064d-467e-bd3a-3d37c2a05a91) 
___

# Solemne 2

1. El objetivo es demostrar:  
* Razonamiento lógico  
* Pensamiento sistémico

Diseñar un:  
"Organismo visual" en p5.js que funcione mediante reglas preestablecidas para visibilizar una problemática de genero.

Lo más importante es cómo traduces un problema social a una regla de comportamiento computacional.

2. Debe contener los 4 pilares fundamentales

* Descomposición: ¿Dividiste tu problemática en partes más pequeñas y manejables (funciones)?
* Reconocimiento de Patrones: ¿Usaste ciclos para crear estructuras o repeticiones con sentido (loops -for)?
* Abstracción: ¿Lograste que un movimiento o cambio visual represente un concepto real (ej. usar map para que el mouse represente "presión social")?
* Algoritmos: ¿Tu diagrama de flujo explica paso a paso cómo funciona tu sistema?

# INSTRUCCIONES

1.Pensar en una problemática de género que les interese. (Ej: La desigualdad en los honorarios entre hombres y mujeres, los estrictos cánones de belleza en las mujeres, los femicidios en Chile, la disforia de género, etc.)

2.Luego diseñar (idear) un sketch en movimiento, que represente (metafóricamente) o que nos ayude a visualizar de manera gráfica ese problema.

3.Hacer un diagrama de flujo de su idea. (Diseño de sistema)

4.Programar un sketch en p5.js de 400x400 pixeles. (Cómo mínimo) 

___

## El sketch debe incluir como mínimo: 

* 4 variables creadas por mi  
* 2 variables Integradas en p5.js (ej: width, height, mouseX)  
* 4 figuras geométricas diferentes  
* 2 imágenes  
* Texto  
* función random() y 1 función map()  
* rotate, translate y scale protegidos por push() y pop()
* 3 Sentencias condicionales (if, else if, else), (puede ser solo if o else if) 
* 1 bucle for (ideal para patrones o repetición de elementos)  
* 2 funciones propias definidas fuera de draw()  
* 1 interacciones con el usuario (ej: mouseIsPressed, keyPressed, etc)

___

## Entrega

La carpeta de entrega debe contener 3 links.

1. El primero sera un link a un repositorio en Github que presente la Solemne de forma detallada y en lenguaje formal. (REPO SOLEMNE)
2. El segundo sera un link al Sketch en p5.js con permiso de edición.
3. El tercero sera el link al repositorio de la bitácora de clases, este debe contener todas las clases, desde Historia de la Computación en adelante.

___

## Repositorio de la Solemne 
Debe contener:

### 1. Diagrama de Flujo (Imagen en PNG )
Un diagrama digital (Figma, Miro, etc.) que no solo diga "X aumenta", sino que explique la regla de diseño.  
* Ejemplo: "SI el usuario se acerca al centro, ENTONCES el texto se vuelve ilegible (representando el acoso)".

### 2. Código en Github
Un repositorio que incluya un archivo sketch.js. El código debe estar identado y, sobre todo, comentado. Los comentarios deben ser detallados, deben cumplir con que no solo que funcione, sino que se entienda cómo funciona.

### 3. Documentación (README.md)
Debe incluir:

**1. Información del proyecto**
Nombre del proyecto.
Autor/a.

**2. Descripción objetiva**  
Lo que se ve, sin interpretación  
Responder:  

¿Qué es el proyecto?  
¿Qué aparece en pantalla?  
¿Qué elementos visuales hay?  

**Ejemplo:** formas, colores, movimientos, textos, etc.

**3. Descripción conceptual**  
La idea detrás del proyecto  
Responder:  

¿Cuál es la idea central?  
¿Cómo se relaciona con el sistema visual?  
¿Cuál es la regla principal? “A mayor interacción, menor visibilidad”  
¿Cómo conecta esto con la problemática de género?  

**Idea clave:** conectar lo técnico con lo social.  

**4. Input / Output / Sistema**   
Input (entrada):    
¿Qué datos recibe el sistema?    
Ej: mouse, teclado, tiempo, posición  

Proceso:  
¿Qué hace el sistema con esos datos?  

Output (salida):  
¿Qué se ve como resultado? 

**Ejemplo:**  
Input: movimiento del mouse  
Proceso: aumenta distorsión  
Output: imagen se vuelve ilegible  

**5. Pensamiento computacional**  
Qué incluir:

Reglas del sistema:  
Inputs  
Procesos  
Outputs  

Explicación de la interacción:  
¿Cómo el usuario afecta el sistema?

**Idea clave:** explicar la lógica completa del comportamiento.

**6. Referentes**  
Listado y breve descripción de referentes visuales, teóricos o históricos.

**7. Link al sketch en P5.js en formato EDITABLE**

____

# Pauta de evaluación

![PautaEvaluación](https://github.com/user-attachments/assets/31d0c15d-5241-4d0e-9673-f91ba94e61f9)  

___

## Entregar antes de la clase del 24 de Mayo

