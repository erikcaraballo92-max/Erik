# Erik
Para mí princesita 
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para mi princesita hermosa 💖</title>
<style>
body {
  margin: 0;
  overflow: hidden;
  background: black;
  font-family: Arial, sans-serif;
  color: white;
}

canvas {
  position: absolute;
  top: 0;
  left: 0;
}

.message {
  position: absolute;
  padding: 10px 15px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 15px;
  backdrop-filter: blur(5px);
  cursor: pointer;
  transition: transform 0.3s;
}

.message:hover {
  transform: scale(1.2);
}
</style>
</head>
<body>

<canvas id="stars"></canvas>

<div class="message" style="top:20%; left:30%;">💫 Te amo más de lo que las palabras pueden explicar</div>
<div class="message" style="top:50%; left:70%;">🌙 Estoy orgulloso de la mujer increíble que sos</div>
<div class="message" style="top:70%; left:20%;">✨ Me das una paz que nadie más puede darme</div>
<div class="message" style="top:40%; left:50%;">💖 Sos mi felicidad, mi calma y mi todo</div>
<div class="message" style="top:80%; left:60%;">🌌 Siempre voy a desearte lo mejor en la vida</div>

<h1 style="position:absolute; top:5%; width:100%; text-align:center;">
Para mi princesita hermosa, mi Kiara 💕
</h1>

<script>
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let stars = [];

for (let i = 0; i < 200; i++) {
  stars.push({
    x: Math.random() * canvas.width,
    y: Math.random() * canvas.height,
    radius: Math.random() * 2,
    speed: Math.random() * 0.5
  });
}

function drawStars() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);

  ctx.fillStyle = "white";

  stars.forEach(star => {
    ctx.beginPath();
    ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
    ctx.fill();

    star.y += star.speed;
    if (star.y > canvas.height) star.y = 0;
  });

  requestAnimationFrame(drawStars);
}

drawStars();
</script>

</body>
</html>