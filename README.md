# apnacollege
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>I Love You Amma</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    h1 {
      font-size: 3em;
      background: linear-gradient(45deg, #ff416c, #ff4b2b, #f9d423, #e65c00);
      background-size: 400% 400%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: glow 4s ease infinite;
      text-align: center;
    }

    @keyframes glow {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .heart {
      width: 20px;
      height: 20px;
      position: absolute;
      background: red;
      transform: rotate(45deg);
      animation: floatUp 4s infinite ease-in;
    }

    .heart::before,
    .heart::after {
      content: "";
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
      position: absolute;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes floatUp {
      0% {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
      100% {
        opacity: 0;
        transform: translateY(-300px) scale(1.5);
      }
    }
  </style>
</head>
<body>
  <h1>I ❤️ You Amma</h1>

  <script>
    // Generate floating hearts
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 4000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>
