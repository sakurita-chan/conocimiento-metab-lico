[script. js.txt](https://github.com/user-attachments/files/20274204/script.js.txt)[style. css.txt](https://github.com/user-attachments/files/20274202/style.css.txt)[index. html.txt](https://github.com/user-attachments/files/20274199/index.html.txt)# conocimiento-metab-lico
[Uploading<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Desaf�o Metab�lico</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<div class="container">
<h1>Desaf�o Metab�lico</h1>
<div id="pregunta-contenedor">
<p id="pregunta"></p>
<ul id="opciones-contenedor">
<li><button class="opcion" data-respuesta="A">A. </button></li>
<li><button class="opcion" data-respuesta="B">B. </button></li>
<li><button class="opcion" data-respuesta="C">C. </button></li>
<li><button class="opcion" data-respuesta="D">D. </button></li>
</ul>
</div>
<div id="resultado-contenedor" class="oculto">
<p id="resultado-texto"></p>
<button id="siguiente-pregunta">Siguiente Pregunta</button>
</div>
<div id="final-contenedor" class="oculto">
<h2>�Juego Terminado!</h2>
<p id="puntuacion-final"></p>
<button id="reiniciar-juego">Reiniciar Juego</button>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
 index. html.txt…]()
![incorrecto 2](https://github.com/user-attachments/assets/7ba3edd2-8f5d-4a61-b73f-035bcc092f24)
![incorrecto 1](https://github.com/user-attachments/assets/c4c3a125-eb92-4077-b8dc-8b62bc73f4ec)
![correcto 2](https://github.com/user-attachments/assets/2d04b9f4-33e0-49f7-b300-ff0575614ea8)
![correcto 1](https://github.com/user-attachments/assets/a404620f-0b3c-40e7-8302-57a5ac1c0230)
[Uplbody {
font-family: sans-serif;
background-color: #e0f7fa; /* Azul claro */
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
margin: 0;
}
.container {
background-color: #fff; /* Blanco */
padding: 30px;
border-radius: 8px;
box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
text-align: center;
}
h1 {
color: #00838f; /* Un tono de azul m�s oscuro para el t�tulo */
margin-bottom: 20px;
animation: fadeIn 1s ease-in-out; /* Animaci�n de entrada para el t�tulo */
}
#pregunta-contenedor {
margin-bottom: 20px;
animation-name: slideInLeft;
animation-duration: 0.5s;
animation-timing-function: ease-out;
}
#pregunta {
font-size: 1.2em;
color: #333;
margin-bottom: 15px;
}
#opciones-contenedor {
list-style: none;
padding: 0;
}
#opciones-contenedor li {
margin-bottom: 10px;
}
.opcion {
padding: 10px 20px;
border: 1px solid #b2ebf2; /* Borde azul claro */
border-radius: 5px;
cursor: pointer;
background-color: #b2ebf2; /* Fondo azul claro */
color: #333;
font-size: 1em;
transition: background-color 0.3s ease, color 0.3s ease;
animation: pulse 0.7s infinite alternate; /* Animaci�n sutil para los botones */
}
.opcion:hover {
background-color: #80deea; /* Un tono de azul m�s oscuro al pasar el rat�n */
color: #fff;
}
.correcto {
background-color: #aaffaa !important;
animation: tada 1s ease-in-out;
}
.incorrecto {
background-color: #ffaaaa !important;
animation: shake 0.5s ease-in-out;
}
.oculto {
display: none;
}
#resultado-contenedor {
margin-top: 20px;
font-weight: bold;
animation: fadeIn 0.5s ease-in-out;
}
#resultado-imagen {
width: 80px;
height: 80px;
margin-bottom: 10px;
}
#siguiente-pregunta, #reiniciar-juego {
padding: 10px 20px;
background-color: #00acc1; /* Otro tono de azul */
color: white;
border: none;
border-radius: 5px;
cursor: pointer;
font-size: 1em;
margin-top: 15px;
transition: background-color 0.3s ease;
animation: slideInUp 0.5s ease-out;
}
#siguiente-pregunta:hover, #reiniciar-juego:hover {
background-color: #00838f;
}
#final-contenedor {
margin-top: 20px;
animation: zoomIn 0.5s ease-in-out;
}
#puntuacion-final {
font-size: 1.2em;
font-weight: bold;
margin-bottom: 15px;
}
/* Definici�n de animaciones */
@keyframes fadeIn {
from { opacity: 0; }
to { opacity: 1; }
}
@keyframes slideInLeft {
from { transform: translateX(-100%); opacity: 0; }
to { transform: translateX(0); opacity: 1; }
}
@keyframes pulse {
0% { transform: scale(1); }
100% { transform: scale(1.05); }
}
@keyframes tada {
0% { transform: scale(1); }
10%, 20% { transform: scale(0.9) rotate(-3deg); }
30%, 50%, 70%, 90% { transform: scale(1.1) rotate(3deg); }
40%, 60%, 80% { transform: scale(1.1) rotate(-3deg); }
100% { transform: scale(1) rotate(0); }
}
@keyframes shake {
0%, 100% { transform: translateX(0); }
10%, 30%, 50%, 70%, 90% { transform: translateX(-10px); }
20%, 40%, 60%, 80% { transform: translateX(10px); }
}
@keyframes slideInUp {
from { transform: translateY(50px); opacity: 0; }
to { transform: translateY(0); opacity: 1; }
}
@keyframes zoomIn {
from { transform: scale(0); opacity: 0; }
to { transform: scale(1); opacity: 1; }
}oading style. css.txt…]()
[const preguntas = {
"GLUCOLISIS": [
{
"pregunta": "�Cu�l es la mol�cula inicial en la gluc�lisis?",
"opciones": ["Glucosa", "Piruvato", "Lactato", "Acetil-CoA"],
"respuesta": "A",
"animacion": "slideInDown" // Ejemplo de animaci�n espec�fica
},
{
"pregunta": "�Qu� enzima cataliza la fosforilaci�n de la glucosa a
glucosa-6-fosfato?",
"opciones": ["Fosfofructoquinasa-1", "Hexoquinasa/Glucoquinasa", "Piruvato
quinasa", "Aldolasa"],
"respuesta": "B",
"animacion": "fadeIn"
},
// ... m�s preguntas
],
"FERMENTACI�N L�CTICA Y ALCOH�LICA": [
// ... preguntas
{
"pregunta": "�Qu� organismo es com�nmente utilizado en la fermentaci�n
alcoh�lica?",
"opciones": ["E. coli", "Lactobacillus", "S. cerevisiae", "Streptococcus"],
"respuesta": "C",
"animacion": "slideInRight"
}
],
// ... m�s temas con sus preguntas y animaciones
};
const imagenesAcierto = ["./img/correcto1.png", "./img/correcto2.png", "./img/correcto3.png"];
// Rutas a tus im�genes de acierto
const imagenesError = ["./img/incorrecto1.png", "./img/incorrecto2.png",
"./img/incorrecto3.png"]; // Rutas a tus im�genes de error
let temas = Object.keys(preguntas);
let temaActualIndice = 0;
let preguntaActualIndice = 0;
let puntuacion = 0;
const container = document.querySelector('.container');
const preguntaElemento = document.getElementById('pregunta');
const opcionesContenedor = document.getElementById('opciones-contenedor');
const resultadoContenedor = document.getElementById('resultado-contenedor');
const resultadoTexto = document.getElementById('resultado-texto');
const resultadoImagen = document.createElement('img'); // Crear elemento de imagen
resultadoImagen.id = 'resultado-imagen';
resultadoContenedor.insertBefore(resultadoImagen, resultadoTexto); // Insertar antes del
texto
const siguientePreguntaBoton = document.getElementById('siguiente-pregunta');
const finalContenedor = document.getElementById('final-contenedor');
const puntuacionFinalTexto = document.getElementById('puntuacion-final');
const reiniciarJuegoBoton = document.getElementById('reiniciar-juego');
function mostrarPregunta() {
const temaActual = temas[temaActualIndice];
const preguntaActual = preguntas[temaActual][preguntaActualIndice];
preguntaElemento.textContent = preguntaActual.pregunta;
// Aplicar animaci�n a la pregunta
preguntaElemento.style.animation = ''; // Resetear animaci�n anterior
void preguntaElemento.offsetWidth; // Forzar un reflow para que la nueva animaci�n se
active
preguntaElemento.style.animation = `${preguntaActual.animacion || 'fadeIn'} 0.5s
ease-in-out`;
opcionesContenedor.innerHTML = ''; // Limpiar opciones anteriores
preguntaActual.opciones.forEach((opcion, indice) => {
const li = document.createElement('li');
const button = document.createElement('button');
button.classList.add('opcion');
button.dataset.respuesta = String.fromCharCode(65 + indice); // A, B, C, D
button.textContent = `${String.fromCharCode(65 + indice)}. ${opcion}`;
button.addEventListener('click', verificarRespuesta);
li.appendChild(button);
opcionesContenedor.appendChild(li);
});
resultadoContenedor.classList.add('oculto');
siguientePreguntaBoton.classList.add('oculto');
resultadoImagen.src = ''; // Limpiar imagen anterior
}
function verificarRespuesta(evento) {
const respuestaSeleccionada = evento.target.dataset.respuesta;
const temaActual = temas[temaActualIndice];
const preguntaActual = preguntas[temaActual][preguntaActualIndice];
const botonesOpciones = document.querySelectorAll('#opciones-contenedor button');
botonesOpciones.forEach(boton => {
if (boton.dataset.respuesta === preguntaActual.respuesta) {
boton.classList.add('correcto');
} else if (boton.dataset.respuesta === respuestaSeleccionada) {
boton.classList.add('incorrecto');
}
boton.disabled = true; // Deshabilitar botones despu�s de la selecci�n
});
if (respuestaSeleccionada === preguntaActual.respuesta) {
puntuacion++;
resultadoTexto.textContent = "�Correcto!";
resultadoImagen.src = imagenesAcierto[Math.floor(Math.random() *
imagenesAcierto.length)];
} else {
resultadoTexto.textContent = `Incorrecto. La respuesta correcta era
${preguntaActual.respuesta}.`;
resultadoImagen.src = imagenesError[Math.floor(Math.random() *
imagenesError.length)];
}
resultadoContenedor.classList.remove('oculto');
siguientePreguntaBoton.classList.remove('oculto');
}
function siguientePregunta() {
const temaActual = temas[temaActualIndice];
preguntaActualIndice++;
if (preguntaActualIndice < preguntas[temaActual].length) {
mostrarPregunta();
} else {
temaActualIndice++;
preguntaActualIndice = 0;
if (temaActualIndice < temas.length) {
mostrarPregunta();
} else {
mostrarResultadoFinal();
}
}
}
function mostrarResultadoFinal() {
preguntaElemento.classList.add('oculto');
opcionesContenedor.classList.add('oculto');
resultadoContenedor.classList.add('oculto');
siguientePreguntaBoton.classList.add('oculto');
puntuacionFinalTexto.textContent = `Tu puntuaci�n final es: ${puntuacion} /
${Object.values(preguntas).flat().length}`;
finalContenedor.classList.remove('oculto');
}
function reiniciarJuego() {
temaActualIndice = 0;
preguntaActualIndice = 0;
puntuacion = 0;
preguntaElemento.classList.remove('oculto');
opcionesContenedor.classList.remove('oculto');
finalContenedor.classList.add('oculto');
mostrarPregunta();
}
// Event listeners
siguientePreguntaBoton.addEventListener('click', siguientePregunta);
reiniciarJuegoBoton.addEventListener('click', reiniciarJuego);
// Iniciar el juego
mostrarPregunta();Uploading script. js.txt…]()

