<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Key Press Display</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        h1 {
            color: #333;
            margin-bottom: 30px;
        }
        .key-display {
            font-size: 48px;
            color: #667eea;
            font-weight: bold;
            min-height: 60px;
            margin: 20px 0;
        }
        .info {
            color: #666;
            margin-top: 20px;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Key Press Detector</h1>
        <p>Press any key on your keyboard</p>
        <div class="key-display" id="keyDisplay">Waiting...</div>
        <div class="info" id="keyInfo"></div>
    </div>

    <script>
        document.addEventListener('keydown', function(event) {
            const display = document.getElementById('keyDisplay');
            const info = document.getElementById('keyInfo');
            
            display.textContent = `Key: ${event.key}`;
            info.innerHTML = `Code: ${event.code}<br>KeyCode: ${event.keyCode}`;
        });
    </script>
</body>
</html>
