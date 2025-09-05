<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Spider-Man Runner Emoji 🕷️</title>
<style>
  body {
    margin: 0;
    background: #87ceeb;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
  }
  canvas {
    border: 4px solid #000;
  }
</style>
</head>
<body>
<canvas id="gameCanvas" width="600" height="200"></canvas>
<script>
const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");

// Joueur Spider-Man emoji
const player = { x: 50, y: 150, width: 30, height: 30, dy: 0, jumping: false, swing: 0 };
const gravity = 0.7;
const jumpPower = -14;
let obstacles = [];
let frame = 0;
let score = 0;
let gameOver = false;
let speed = 3;

// Liste des vilains Marvel emojis
const villains = ["💀","🦹","🐍","🦑","👹"];

// Créer un obstacle avec hauteur et taille aléatoire
function createObstacle() {
  const sizeType = Math.random();
  let height;
  if(sizeType < 0.4) height = 20;      // petit
  else if(sizeType < 0.8) height = 35; // moyen
  else height = 50;                     // grand
  const emoji = villains[Math.floor(Math.random() * villains.length)];
  obstacles.push({ x: canvas.width, y: 200 - height, width: 30, height: height, emoji });
}

// Collision
function collision(p, o) {
  return p.x < o.x + o.width && p.x + p.width > o.x &&
         p.y < o.y + o.height && p.y + p.height > o.y;
}

// Saut
function jump() {
  if(!player.jumping){
    player.dy = jumpPower;
    player.jumping = true;
    player.swing = -20; 
    spawnStars();
  }
}

// Étoiles du saut
let stars = [];
function spawnStars() {
  for(let i=0;i<5;i++){
    stars.push({x:player.x+player.width/2,y:player.y+player.height/2,dy:Math.random()*-2-1,life:30});
  }
}

// Dessiner étoiles
function drawStars(){
  ctx.fillStyle="yellow";
  for(let i=stars.length-1;i>=0;i--){
    const s=stars[i];
    ctx.fillRect(s.x,s.y,3,3);
    s.y += s.dy;
    s.life--;
    if(s.life<=0) stars.splice(i,1);
  }
}

// Onomatopée
function drawComicText(text,x,y,color="red"){
  ctx.font="30px Comic Sans MS";
  ctx.fillStyle=color;
  ctx.strokeStyle="black";
  ctx.lineWidth=2;
  ctx.strokeText(text,x,y);
  ctx.fillText(text,x,y);
}

// Événements
document.addEventListener("keydown", e=>{ if(e.code==="Space"||e.key===" ") jump(); });
canvas.addEventListener("click", jump);
canvas.addEventListener("touchstart", jump);

// Boucle de jeu
function update(){
  if(gameOver) return;

  ctx.clearRect(0,0,canvas.width,canvas.height);

  // Gravité
  player.dy += gravity;
  player.y += player.dy;
  if(player.y + player.height >= 200){
    player.y = 200 - player.height;
    player.dy = 0;
    player.jumping = false;
  }

  // Balancement Spider-Man
  if(player.swing < 20) player.swing += 1;

  // Dessiner Spider-Man emoji avec balancement
  ctx.save();
  ctx.translate(player.x + player.width/2, player.y + player.height/2);
  ctx.rotate(player.swing * Math.PI/180);
  ctx.font = "30px Arial";
  ctx.fillText("🕷️", -player.width/2, player.height/2 -5);
  ctx.restore();

  // Créer obstacles
  if(frame % 90 === 0) createObstacle(); // un peu plus fréquent

  // Score et vitesse progressive
  score = Math.floor(frame/10);
  speed = 3 + Math.floor(score/50);

  // Déplacer et dessiner obstacles
  ctx.font = "30px Arial";
  for(let i=0;i<obstacles.length;i++){
    const o = obstacles[i];
    o.x -= speed;
    ctx.fillText(o.emoji, o.x, o.y + o.height);

    if(collision(player,o)){
      gameOver = true;
      drawComicText("BAM!", player.x, player.y - 10);
    }
  }

  drawStars();

  // Afficher score
  ctx.fillStyle="black";
  ctx.font="20px Comic Sans MS";
  ctx.fillText("Score: "+score,10,30);

  frame++;
  if(!gameOver) requestAnimationFrame(update);
  else drawComicText("POW! GAME OVER",150,100);
}

update();
</script>
</body>
</html>
