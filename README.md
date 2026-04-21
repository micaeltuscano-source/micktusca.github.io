<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Quanto ti voglio bene</title>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;600&display=swap" rel="stylesheet">

<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  background:radial-gradient(circle,#0f172a,#020617);
  font-family:'Dancing Script', cursive;
  overflow:hidden;
}

.container{
  display:flex;
  align-items:center;
  gap:100px;
}

.text{
  color:#fff;
  max-width:420px;
  opacity:0;
  transform:translateX(-40px);
  animation:showText 2s ease forwards;
  animation-delay:2.5s;
}

.text h1{
  font-size:48px;
  margin-bottom:10px;
}

.text p{
  font-size:28px;
}

@keyframes showText{
  to{
    opacity:1;
    transform:translateX(0);
  }
}

.flower{
  position:relative;
  width:260px;
  height:260px;
}

.petal{
  position:absolute;
  width:100px;
  height:150px;
  background:linear-gradient(to bottom,#ff7ab6,#ff2e6e);
  border-radius:50%;
  top:50%;
  left:50%;
  transform-origin:center bottom;
  opacity:0;
  transform:translate(-50%,-100%) rotate(var(--r)) scale(0);
  animation:grow 1.5s ease forwards;
}

.p1{--r:0deg; animation-delay:0s;}
.p2{--r:72deg; animation-delay:0.15s;}
.p3{--r:144deg; animation-delay:0.3s;}
.p4{--r:216deg; animation-delay:0.45s;}
.p5{--r:288deg; animation-delay:0.6s;}

@keyframes grow{
  from{
    opacity:0;
    transform:translate(-50%,-100%) rotate(var(--r)) scale(0);
  }
  to{
    opacity:1;
    transform:translate(-50%,-100%) rotate(var(--r)) scale(1);
  }
}

.center{
  position:absolute;
  width:60px;
  height:60px;
  background:#ffd000;
  border-radius:50%;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%) scale(0);
  animation:pop 1s ease forwards 1.2s;
  box-shadow:0 0 25px #ffd000;
}

@keyframes pop{
  to{
    transform:translate(-50%,-50%) scale(1);
  }
}

</style>
</head>
<body>

<div class="container">

  <div class="text">
    <h1>Un piccolo messaggio per te</h1>
    <h2>Isaia 54:10</h2>
    <h3>Il mio amore non si allontanerà mai da te 💖</h3>
  </div>

  <div class="flower">
    <div class="petal p1"></div>
    <div class="petal p2"></div>
    <div class="petal p3"></div>
    <div class="petal p4"></div>
    <div class="petal p5"></div>
    <div class="center"></div>
  </div>

</div>

</body>
</html>
