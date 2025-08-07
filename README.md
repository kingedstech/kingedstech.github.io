<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Green Clock</title>
  <style>
    body {
      background-color: green;
      color: white;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    #clock {
      font-size: 4rem;
    }
  </style>
</head>
<body>
  <div id="clock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      const hours = String(now.getHours()).padStart(2, '0');
      const minutes = String(now.getMinutes()).padStart(2, '0');
      const seconds = String(now.getSeconds()).padStart(2, '0');
      document.getElementById('clock').textContent = `${hours}:${minutes}:${seconds}`;
    }

    setInterval(updateClock, 1000);
    updateClock(); // Initial call to display clock immediately
  </script>
</body>
</html>
