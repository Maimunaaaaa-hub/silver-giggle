<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Promposal: Chammak Challo</title>
  <style>
    @keyframes float {
      0% { transform: translateX(-200px) translateY(0); }
      50% { transform: translateX(50vw) translateY(-20px); }
      100% { transform: translateX(100vw) translateY(0); }
    }

    body {
      margin: 0;
      font-family: 'Comic Sans MS', 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #b3d9ff, #e6f2ff);
      overflow: hidden;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .cloud-text {
      position: absolute;
      top: 5%;
      width: 100%;
      text-align: center;
      font-size: 2.5rem;
      color: white;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    }

    .floating-cloud {
      position: absolute;
      top: 10%;
      width: 200px;
      height: 100px;
      background: white;
      border-radius: 50%;
      box-shadow: 60px 0 white, 120px 0 white;
      animation: float 60s linear infinite;
      opacity: 0.7;
    }

    .floating-text {
      position: absolute;
      white-space: nowrap;
      color: #666;
      font-size: 1rem;
      animation: float 60s linear infinite;
    }

    .window {
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: absolute;
      width: 70%;
      max-width: 600px;
      background: white;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
      padding: 30px;
      text-align: center;
    }

    .window.active {
      display: flex;
    }

    .button-group button {
      margin: 10px;
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background-color: #66b3ff;
      color: white;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s;
    }

    .button-group button:hover {
      background-color: #3399ff;
    }

    ul {
      list-style: none;
      padding: 0;
      text-align: left;
    }

    li {
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <div class="cloud-text">Will you be my Chammak Challo?</div>

  <!-- Floating Clouds with Writings -->
  <div class="floating-cloud" style="top: 20%; left: -250px;"></div>
  <div class="floating-text" style="top: 22%; left: -250px;">cutest cloud for the cutest you</div>

  <div class="floating-cloud" style="top: 40%; left: -300px;"></div>
  <div class="floating-text" style="top: 42%; left: -300px;">your smile is sunshine</div>

  <div class="floating-cloud" style="top: 60%; left: -200px;"></div>
  <div class="floating-text" style="top: 62%; left: -200px;">say yes please only</div>

  <!-- Windows -->
  <div class="window active" id="window1">
    <h2>Are you cutie?</h2>
    <div class="button-group">
      <button onclick="nextWindow()">Yes</button>
      <button onclick="nextWindow()">Yes</button>
    </div>
  </div>

  <div class="window" id="window2">
    <h2>10 Reasons Why You Should Go To Prom With Me:</h2>
    <ul>
      <li>1) I love your smile</li>
      <li>2) I love your nose</li>
      <li>3) I love your smell</li>
      <li>4) I love your bhai</li>
      <li>5) I am cool</li>
      <li>6) I know you want to come with me too</li>
      <li>7) I think you're cool</li>
      <li>8) I think your mom would find me cool</li>
      <li>9) I find your mom cool</li>
      <li>10) I love you</li>
    </ul>
    <button onclick="nextWindow()">Next</button>
  </div>

  <div class="window" id="window3">
    <h2>Will you please go out with me for our junior prom?</h2>
    <div class="button-group">
      <button>Yes Please Only</button>
    </div>
  </div>

  <script>
    let current = 1;
    function nextWindow() {
      document.getElementById(`window${current}`).classList.remove('active');
      current++;
      document.getElementById(`window${current}`).classList.add('active');
    }
  </script>
</body>
</html>
