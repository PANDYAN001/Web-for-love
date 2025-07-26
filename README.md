# Web-for-love
To propose my her
    git add .
    git commit -m "Initial website commit"
    git push origin main
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday Page</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      text-align: center;
      overflow: hidden;
    }

    h1 {
      margin-top: 50px;
      font-size: 3em;
      color: #fff;
      text-shadow: 2px 2px 5px #000;
    }

    p {
      font-size: 1.2em;
      margin: 20px auto;
      max-width: 600px;
      color: #fff;
      text-shadow: 1px 1px 3px #000;
    }

    /* Balloons */
    .balloon {
      position: absolute;
      bottom: -150px;
      width: 80px;
      height: 100px;
      background: red;
      border-radius: 50% 50% 50% 50%;
      animation: floatUp 6s linear infinite;
    }

    .balloon::after {
      content: "";
      position: absolute;
      bottom: -20px;
      left: 50%;
      width: 2px;
      height: 40px;
      background: #fff;
      transform: translateX(-50%);
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-120vh); opacity: 0; }
    }

    /* Confetti */
    .confetti {
      position: fixed;
      top: -10px;
      width: 8px;
      height: 14px;
      background-color: yellow;
      animation: fall 5s linear infinite;
    }

    @keyframes fall {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(100vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1 id="title">🎂 Happy Birthday 🎂</h1>
  <p id="message">
    This is your own special passage. Write your wishes here! 🎉<br>
    Example: Wishing you joy, love, and success always!
  </p>

  <!-- Balloons -->
  <div class="balloon" style="left:10%; background:#ff6f61;"></div>
  <div class="balloon" style="left:30%; background:#6ec6ff; animation-delay:1s;"></div>
  <div class="balloon" style="left:50%; background:#ffd54f; animation-delay:2s;"></div>
  <div class="balloon" style="left:70%; background:#81c784; animation-delay:3s;"></div>
  <div class="balloon" style="left:90%; background:#ba68c8; animation-delay:1.5s;"></div>

  <!-- Confetti (multiple pieces with different positions/colors) -->
  <script>
    for (let i = 0; i < 50; i++) {
      let confetti = document.createElement('div');
      confetti.className = 'confetti';
      confetti.style.left = Math.random() * 100 + 'vw';
      confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 80%, 60%)`;
      confetti.style.animationDelay = Math.random() * 5 + 's';
      confetti.style.animationDuration = (3 + Math.random() * 2) + 's';
      document.body.appendChild(confetti);
    }
  </script>
</body>
</html>
