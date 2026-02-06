<html lang="en">
<head>
  <meta charset="UTF-8">
  <title> Anjali, Be My Valentine 💖</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff5f6d, #ffc371);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .box {
      background: rgba(255,255,255,0.2);
      backdrop-filter: blur(10px);
      padding: 40px 30px;
      border-radius: 25px;
      text-align: center;
      color: white;
      width: 90%;
      max-width: 380px;
      box-shadow: 0 25px 50px rgba(0,0,0,0.25);
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 10px;
    }

    p {
      font-size: 1.1rem;
      margin-bottom: 25px;
    }

    button {
      padding: 14px 30px;
      font-size: 1.1rem;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      font-weight: bold;
      margin: 10px;
      transition: transform 0.2s;
    }

    #yes {
      background: white;
      color: #ff3f6c;
    }

    #no {
      background: #ff3f6c;
      color: white;
      position: absolute;
    }

    button:hover {
      transform: scale(1.08);
    }

    .hidden {
      display: none;
    }

    .celebrate {
      font-size: 2rem;
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
  </audio>

  <div class="box">
    <h1 id="title">Will you be my Valentine? 💘</h1>
    <p id="text">Think carefully… your heart already knows 💕</p>

    <button id="yes" onclick="yesClicked()">YES 💖</button>
    <button id="no" onmouseover="moveNo()">NO 😜</button>

    <div id="celebration" class="celebrate hidden">
      🎉😍💞💖💘🥰🎉
    </div>
  </div>

  <script>
    function moveNo() {
      const btn = document.getElementById("no");
      const x = Math.random() * (window.innerWidth - btn.offsetWidth);
      const y = Math.random() * (window.innerHeight - btn.offsetHeight);
      btn.style.left = x + "px";
      btn.style.top = y + "px";
    }

    function yesClicked() {
      document.getElementById("title").innerText = "YAYYYY!!! 💍💖";
      document.getElementById("text").innerText =
        "Officially my Valentine 😍 Let’s make it memorable ❤️";
      document.getElementById("celebration").classList.remove("hidden");
      document.getElementById("yes").style.display = "none";
      document.getElementById("no").style.display = "none";
    }
  </script>

</body>
</html>
