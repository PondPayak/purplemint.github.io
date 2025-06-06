<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      font-family: 'Comic Sans MS', cursive, sans-serif;
      color: #fff;
      text-align: center;
      overflow: hidden;
    }
    h1 {
      margin-top: 50px;
      font-size: 4em;
      animation: pop 1s ease-in-out infinite alternate;
    }
    p {
      font-size: 1.5em;
    }
    .balloon {
      width: 50px;
      height: 70px;
      background-color: red;
      border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      position: absolute;
      animation: float 6s ease-in-out infinite;
    }
    @keyframes float {
      0% { transform: translateY(100vh); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh); opacity: 0; }
    }
    @keyframes pop {
      0% { transform: scale(1); }
      100% { transform: scale(1.1); }
    }
  </style>
</head>
<body>
  <h1>🎉 Happy Birthday! 🎂</h1>
  <p>Wishing you joy, laughter, and cake!</p>

  <script>
    // Create multiple balloons
    for (let i = 0; i < 20; i++) {
      const balloon = document.createElement("div");
      balloon.className = "balloon";
      balloon.style.left = Math.random() * 100 + "vw";
      balloon.style.backgroundColor = `hsl(${Math.random() * 360}, 70%, 60%)`;
      balloon.style.animationDuration = 4 + Math.random() * 3 + "s";
      document.body.appendChild(balloon);
    }
  </script>
</body>
</html>
