# codealpha_backgroundgenrator
<!DOCTYPE html>
<html>
<head>
  <title>Background Generator</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(to right, #00ff00, #0000ff);
    }
    
    .container {
      display: flex;
      align-items: center;
    }
    
    h1 {
      font-family: Arial, sans-serif;
      color: #ffffff;
    }
    
    input[type="color"] {
      margin: 0 10px;
    }
    
    button {
      padding: 10px 20px;
      background-color: #ffffff;
      border: none;
      border-radius: 5px;
      font-family: Arial, sans-serif;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Background Generator</h1>
  <div class="container">
    <input type="color" id="color1" value="#00ff00">
    <input type="color" id="color2" value="#0000ff">
    <button id="gradientBtn">Generate</button>
  </div>

  <script>
    const color1 = document.getElementById("color1");
    const color2 = document.getElementById("color2");
    const gradientBtn = document.getElementById("gradientBtn");

    function setGradient() {
      document.body.style.background = `linear-gradient(to right, ${color1.value}, ${color2.value})`;
    }

    gradientBtn.addEventListener("click", setGradient);
  </script>
</body>
</html>
