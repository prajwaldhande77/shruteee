# shruteee
annivarsary
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Anniversary ❤️</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fad0c4);
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      text-align: center;
      color: white;
      padding: 30px;
      border-radius: 20px;
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
      animation: fadeIn 2s ease-in-out;
      max-width: 700px;
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 15px;
      animation: pulse 2s infinite;
    }

    p {
      font-size: 1.3rem;
      margin-bottom: 20px;
      line-height: 1.6;
    }

    .heart {
      font-size: 3rem;
      color: red;
      animation: beat 1s infinite;
    }

    .falling-hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      top: 0;
      left: 0;
      z-index: -1;
    }

    .falling-hearts span {
      position: absolute;
      top: -10%;
      color: rgba(255, 255, 255, 0.8);
      font-size: 20px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh);
      }
    }

    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .btn {
      display: inline-block;
      margin-top: 10px;
      padding: 12px 24px;
      border: none;
      border-radius: 30px;
      background: white;
      color: #ff4b6e;
      font-size: 1rem;
      font-weight: bold;
      cursor: pointer;
      transition: transform 0.2s ease, background 0.2s ease;
    }

    .btn:hover {
      transform: scale(1.08);
      background: #ffe6eb;
    }

    #message {
      margin-top: 20px;
      font-size: 1.2rem;
      display: none;
      color: #fff;
    }
  </style>
</head>
<body>
  <div class="falling-hearts" id="hearts"></div>

  <div class="container">
    <h1>Happy Anniversary ❤️</h1>
    <p>
      Every moment with you is special.<br />
      Thank you for filling life with love, joy, and beautiful memories.
    </p>
    <div class="heart">❤️</div>
    <button class="btn" onclick="showMessage()">Click for a Surprise</button>
    <div id="message">You are my today, my tomorrow, and my forever 💖</div>
  </div>

  <script>
    function showMessage() {
      document.getElementById("message").style.display = "block";
    }

    const heartsContainer = document.getElementById("hearts");

    for (let i = 0; i < 30; i++) {
      const heart = document.createElement("span");
      heart.innerHTML = "❤";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
      heart.style.fontSize = (Math.random() * 20 + 15) + "px";
      heart.style.opacity = Math.random();
      heartsContainer.appendChild(heart);
    }
  </script>
</body>
</html>
