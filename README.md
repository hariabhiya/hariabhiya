<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Journey</title>
    <style>
        body {
            text-align: center;
            background-color: #FFC0CB; /* Light pink background */
            font-family: Arial, sans-serif;
        }
        h1 {
            color: red;
            font-size: 50px;
        }
        .heart {
            font-size: 50px;
            color: red;
        }
        .container {
            padding: 50px;
        }
        button {
            background-color: red;
            color: white;
            font-size: 20px;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            margin: 10px;
            transition: 0.3s;
        }
        button:hover {
            background-color: darkred;
        }
        /* Styling for the "No" button that moves */
        .no-button {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            transition: 0.3s;
        }
    </style>
    <script>
        function moveNoButton() {
            let button = document.getElementById("noButton");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = x + "px";
            button.style.top = y + "px";
        }
    </script>
</head>
<body>

<div class="container" id="page1">
    <h1>Do you love me? ❤️</h1>
    <button onclick="goToPage(2)">Yes</button>
    <button onclick="goToPage(2)">No</button>
</div>

<div class="container" id="page2" style="display:none;">
    <h1>Are you my Vavaa or not? 💕</h1>
    <button onclick="goToPage(3)">Yes</button>
    <button onclick="goToPage(3)">No</button>
</div>

<div class="container" id="page3" style="display:none;">
    <h1>This is me waiting to be your official Valentine 😍</h1>
    <p class="heart">💖💘💞</p>
    <button onclick="goToPage(4)">I dare you press NO 😈😁</button>
    <button id="noButton" class="no-button" onmouseover="moveNoButton()">No</button>
</div>

<div class="container" id="page4" style="display:none;">
    <h1>Hehehe 😁 You failed, now you're only mine 😈😈</h1>
    <button onclick="goToPage(5)">Yes</button>
</div>

<div class="container" id="page5" style="display:none;">
    <h1>Finally, I want to ask you something... 🥰</h1>
    <button onclick="goToPage(6)">Ask</button>
    <button onclick="goToPage(6)">Don't Ask</button>
</div>

<div class="container" id="page6" style="display:none;">
    <h1>Will you be my Valentine? 🥹💍💕🌍</h1>
    <button onclick="goToPage(7)">Yes</button>
</div>

<div class="container" id="page7" style="display:none;">
    <h1>Hehehehe ummmmmmmmaaaaaaaaahhhhhh 😚😚😚😚</h1>
    <p class="heart">💖💘💞</p>
</div>

<script>
    function goToPage(pageNumber) {
        // Hide all pages
        for (let i = 1; i <= 7; i++) {
            document.getElementById("page" + i).style.display = "none";
        }
        // Show the selected page
        document.getElementById("page" + pageNumber).style.display = "block";
    }
</script>

</body>
</html>
