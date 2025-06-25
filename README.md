<html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>THARAWA</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      background: linear-gradient(120deg, #0f2027, #203a43, #2c5364);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }

    .signage {
      position: relative;
      font-size: 5em;
      font-weight: bold;
      color: #fff;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      animation: pulse 4s ease-in-out infinite;
      z-index: 2;
    }

    @keyframes pulse {
      0%, 100% {
        text-shadow: 0 0 20px rgba(255,255,255,0.3),
                     0 0 40px rgba(255,255,255,0.2);
      }
      50% {
        text-shadow: 0 0 30px rgba(255,255,255,0.6),
                     0 0 60px rgba(255,255,255,0.4);
      }
    }

    .light-rays {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      background: radial-gradient(ellipse at center, rgba(255,255,255,0.05) 0%, transparent 70%);
      z-index: 1;
    }

    .ray {
      position: absolute;
      width: 200%;
      height: 10px;
      background: linear-gradient(to right, transparent, rgba(255,255,255,0.2), transparent);
      animation: moveRay 5s linear infinite;
    }

    @keyframes moveRay {
      0% { transform: translateX(-100%) rotate(25deg); }
      100% { transform: translateX(100%) rotate(25deg); }
    }
  </style>
</head>
<body>
  <div class="light-rays">
    <div class="ray" style="top: 20%; animation-delay: 0s;"></div>
    <div class="ray" style="top: 40%; animation-delay: 1s;"></div>
    <div class="ray" style="top: 60%; animation-delay: 2s;"></div>
    <div class="ray" style="top: 80%; animation-delay: 3s;"></div>
  </div>

  <div class="signage">THARAWA</div>
</body>
</html>
