<html>
<head>
    <title> First Page </title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
    <style>
        #hello_image {
            position: absolute;
            top: 52%;
            left: 50%;
            transform: translate(-50%, -50%);
            -webkit-filter: drop-shadow(5px 5px 5px #4682B4);
            filter: drop-shadow(5px 5px 5px #4682B4);
        }

        body {
            
	    background-color: lightpink;
        }

        .container {
            text-align: center;
            color: palevioletred;
            text-shadow: 0 0 5px #FF0000, 0 0 5px #0000FF;
        }

        .centered {
            position: absolute;
            top: 63%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        #demo {
            position: absolute;
            top: 10%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-family: "Sofia", sans-serif;
            font-size: 55px;
            color: palevioletred;
        }

                   
        .zoom-text {
            transition: transform 0.3s ease;
        }

        .zoom-text:hover {
            transform: scale(1.2);
        }
    </style>
    <script>
        var flag = false;
        function playAudio(url) {
            if (!flag) {
                var audio = new Audio(url);
                audio.loop = true;
                audio.play();
                flag = true;
            }
        }
    </script>
</head>
<body>
<div class="container">
    <div id="hello_image">
        <img src="https://camo.githubusercontent.com/a065311cbb5a658371e69b972a9eb03be4cbe882ab6ecbac38f714c775ff649d/68747470733a2f2f6d61737465727069656365722d696d616765732e73332e79616e6465782e6e65742f34643265653236373734636631316565616561643536393639313062313133373a75707363616c6564" width="60%" height="auto">
    </div>
    <div id="hello_world">
        <div class="centered">
            <h1 class="zoom-text" onclick="playAudio('')">(( Hello, World ! ))</h1>
        </div>
    </div>
</div>
<p id="demo"></p>
<script>
    document.getElementById("hello_image").addEventListener("click", function() {
        document.getElementById("demo").innerHTML = "Happy New Year! Love and peace!";
    });
</script>
</body>
</html>
