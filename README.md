<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Digital Clock</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #222;
      color: aqua;
      font-family: 'Courier New', monospace;
    }
    .clock {
      height: 100px;
      width: 290px;
      border: 4px solid aqua;
      padding: 20px 40px;
      border-radius: 30px;
      font-size: 4rem;
    }
  </style>
</head>
<body>

  <div class="clock" id="digitalClock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      const hours = String(now.getHours())
      const minutes = String(now.getMinutes())
      const seconds = String(now.getSeconds())
      const timeString = `${hours}:${minutes}:${seconds}`;
      document.getElementById('digitalClock').textContent = timeString;
    }

    setInterval(updateClock, 1000);
    updateClock(); // Initial call to avoid 1-second delay
  </script>

</body>
</html>
# project-JS
