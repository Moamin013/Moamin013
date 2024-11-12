<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Klik en Verdien Punten Game</title>
    <style>
        /* Basis CSS voor de game */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px;
        }

        #gameArea {
            margin-top: 50px;
        }

        #score {
            font-size: 24px;
            font-weight: bold;
            margin: 20px;
        }

        #clickButton {
            padding: 15px 30px;
            font-size: 20px;
            color: white;
            background-color: #4CAF50;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        #clickButton:hover {
            background-color: #45a049;
        }

    </style>
</head>
<body>

    <!-- Header met de titel van de game -->
    <header>
        <h1>Welkom bij de Klik en Verdien Punten Game!</h1>
    </header>

    <!-- Gamegebied -->
    <div id="gameArea">
        <div id="score">Score: 0</div>
        <button id="clickButton" onclick="clickButton()">Klik hier!</button>
    </div>

    <script>
        // Variabelen voor score en knop
        let score = 0;
        let button = document.getElementById('clickButton');
        let scoreDisplay = document.getElementById('score');

        // Functie voor het klikken op de knop
        function clickButton() {
            // Verhoog de score
            score++;
            scoreDisplay.textContent = "Score: " + score;

            // Verplaats de knop naar een willekeurige plek binnen het scherm
            let maxWidth = window.innerWidth - button.offsetWidth;
            let maxHeight = window.innerHeight - button.offsetHeight;

            let randomX = Math.random() * maxWidth;
            let randomY = Math.random() * maxHeight;

            button.style.position = 'absolute';
            button.style.left = randomX + 'px';
            button.style.top = randomY + 'px';
        }
    </script>

</body>
</html>
