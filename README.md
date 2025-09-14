[index.html.html](https://github.com/user-attachments/files/22324954/index.html.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For My Cutiee 💕</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 25px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 400px;
      animation: fadeIn 2s ease-in-out;
    }
    h1 {
      font-size: 2em;
      color: #ff4f81;
    }
    p {
      font-size: 1.2em;
      color: #444;
    }
    .hearts {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }
    .heart {
      position: absolute;
      color: #ff4f81;
      font-size: 20px;
      animation: float 6s linear infinite;
    }
    @keyframes float {
      0% {transform: translateY(100vh) scale(0.5); opacity: 0;}
      50% {opacity: 1;}
      100% {transform: translateY(-10vh) scale(1); opacity: 0;}
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: scale(0.8);}
      to {opacity: 1; transform: scale(1);}
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      border-radius: 15px;
      background: #ff4f81;
      color: white;
      font-size: 1em;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #ff6fa1;
    }
  </style>
</head>
<body>
  <div class="hearts"></div>
  <div class="card">
    <h1>💖 Hello Cutiee 💖</h1>
    <p>You mean the world to me 🌍💕<br>
       This site is just for you ✨</p>
    <button onclick="showLove()">Click me 💌</button>
    <p id="msg" style="display:none; margin-top:15px; font-size:1.3em; color:#ff4f81;">I love you forever ❤️</p>
  </div>
  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerText = '❤';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = Math.random() * 20 + 15 + 'px';
      heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
      document.querySelector('.hearts').appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 500);

    function showLove(){
      document.getElementById('msg').style.display = 'block';
    }
  </script>
</body>
</html>
