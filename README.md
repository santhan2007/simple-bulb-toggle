# simple-bulb-toggle
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bulb Toggle</title>
  <style>
    body {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f0f0f0;
      font-family: Arial, sans-serif;
    }

    .bulb {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      background-color: #555;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
      margin-bottom: 20px;
      transition: background-color 0.3s, box-shadow 0.3s;
    }

    .bulb.on {
      background-color: #4caf50;
      box-shadow: 0 0 40px #4caf50;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: #007bff;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <div class="bulb" id="bulb"></div>
  <button id="toggleButton" onclick="toggleBulb()">Start</button>

  <script>
    function toggleBulb() {
      const bulb = document.getElementById('bulb');
      const button = document.getElementById('toggleButton');
      bulb.classList.toggle('on');
      if (bulb.classList.contains('on')) {
        button.textContent = 'Stop';
      } else {
        button.textContent = 'Start';
      }
    }
  </script>
</body>
</html>
