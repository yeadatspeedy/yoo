<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Day</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f8f0f0;
            color: #6a4f4d;
            text-align: center;
            margin-top: 10%;
            padding: 0;
            box-sizing: border-box;
        }

        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 48px;
            color: #d94f4f;
            margin-bottom: 30px;
        }

        button {
            font-family: 'Roboto', sans-serif;
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        #yes {
            background-color: #ff6699;
            color: white;
        }

        #no {
            background-color: #ffcc00;
            color: white;
        }

        button:hover {
            opacity: 0.8;
            transform: scale(1.05);
        }

        #heart {
            display: none;
            font-size: 150px;
            color: red;
            margin-top: 50px;
        }

        #gif {
            display: none;
            margin-top: 30px;
        }

        #message {
            position: relative;
            z-index: 10;
        }
    </style>
</head>
<body>

    <div id="message">
        <h1>Bailey, will you be my Valentine?</h1>
        <button id="yes" onclick="yesClicked()">Yes</button>
        <button id="no" onclick="noClicked()">No</button>
    </div>
    
    <div id="heart">❤️</div>
    <div id="gif">
        <img src="https://media.giphy.com/media/Idv6CCs0F1dc4/giphy.gif" alt="Valentine's Day Gif" width="300" height="300">
    </div>

    <script>
        function yesClicked() {
            // Hide the message and buttons
            document.getElementById('message').style.display = 'none';
            document.getElementById('heart').style.display = 'block';  // Show the heart
            document.getElementById('gif').style.display = 'block';    // Show the gif
        }

        function noClicked() {
            const buttonNo = document.getElementById('no');
            // Randomly move the "No" button to a new position on the screen
            const x = Math.random() * (window.innerWidth - buttonNo.offsetWidth);
            const y = Math.random() * (window.innerHeight - buttonNo.offsetHeight);

            buttonNo.style.position = 'absolute';
            buttonNo.style.left = `${x}px`;
            buttonNo.style.top = `${y}px`;
        }
    </script>

</body>
</html>

