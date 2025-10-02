<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Boyfriend's Day 💙</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 50%, #90caf9 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 10px; /* Minimal padding for edges */
        }

        .container {
            max-width: 100%;
            width: 100%;
            text-align: center;
            padding: 20px;
        }

        .envelope {
            position: relative;
            width: 80vw; /* Larger: 80% of viewport width */
            max-width: 800px; /* Cap for large screens */
            height: 50vh; /* Larger: 50% of viewport height */
            min-height: 300px; /* Minimum size */
            margin: 0 auto 30px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .envelope:hover {
            transform: scale(1.02);
        }

        .envelope-back {
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, #1976d2 0%, #42a5f5 100%); /* Blue shades */
            border-radius: 12px;
            box-shadow: 0 15px 40px rgba(25, 118, 210, 0.3); /* Blue-tinted shadow */
            z-index: 1;
        }

        .envelope-flap {
            position: absolute;
            width: 100%;
            height: 35%; /* Adjusted for larger envelope */
            background: linear-gradient(45deg, #1976d2 0%, #42a5f5 100%); /* Blue shades */
            border-radius: 12px 12px 0 0;
            transform-origin: top;
            transition: transform 1s ease; /* Slower for dramatic effect */
            z-index: 2;
            box-shadow: 0 8px 25px rgba(25, 118, 210, 0.2);
        }

        .envelope.open .envelope-flap {
            transform: rotateX(180deg);
        }

        .letter {
            position: absolute;
            width: 88%;
            height: 85%; /* Fits larger envelope */
            background: white;
            border: 2px solid #bbdefb; /* Subtle blue border */
            border-radius: 8px;
            padding: 25px;
            top: 7.5%;
            left: 6%;
            z-index: 3;
            opacity: 0;
            transform: translateY(30px);
            transition: all 1s ease;
            box-shadow: 0 10px 25px rgba(25, 118, 210, 0.15); /* Blue shadow */
            overflow-y: auto; /* Scroll for long letter */
            font-size: 16px; /* Slightly larger text for big envelope */
        }

        .envelope.open .letter {
            opacity: 1;
            transform: translateY(0);
        }

        .letter-content {
            font-size: 16px;
            line-height: 1.7;
            color: #1e3a8a; /* Dark blue text */
            text-align: left;
        }

        .letter-header {
            text-align: center;
            font-size: 20px;
            font-weight: bold;
            color: #1976d2; /* Blue header */
            margin-bottom: 15px;
            font-family: 'Dancing Script', cursive;
        }

        .heart-seal {
            position: absolute;
            top: -20px;
            right: -20px;
            width: 40px; /* Larger seal for big envelope */
            height: 40px;
            background: #1976d2; /* Blue heart */
            transform: rotate(45deg);
            border-radius: 6px;
            box-shadow: 0 4px 15px rgba(25, 118, 210, 0.4);
        }

        .heart-seal::before,
        .heart-seal::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 40px;
            background: #1976d2;
            border-radius: 50%;
        }

        .heart-seal::before {
            top: -20px;
            left: 0;
        }

        .heart-seal::after {
            top: 0;
            left: -20px;
        }

        .instructions {
            margin-top: 20px;
            color: #1565c0; /* Blue instructions */
            font-style: italic;
            font-size: 18px;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 5px;
            }
            
            .envelope {
                width: 95vw;
                height: 45vh;
                min-height: 250px;
            }
            
            .letter {
                width: 85%;
                height: 80%;
                padding: 20px;
                font-size: 14px;
            }
            
            .letter-content {
                font-size: 14px;
            }
            
            .letter-header {
                font-size: 18px;
            }
            
            .instructions {
                font-size: 16px;
            }
        }

        @media (max-width: 480px) {
            .letter {
                padding: 15px;
                font-size: 13px;
            }
            
            .letter-content {
                font-size: 13px;
            }
        }

        /* Import Google Font for header */
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&display=swap');
    </style>
</head>
<body>
    <div class="container">
        <div class="envelope" id="envelope">
            <div class="envelope-back"></div>
            <div class="envelope-flap"></div>
            <div class="letter">
                <div class="heart-seal"></div>
                <div class="letter-content">
                    <div class="letter-header">Happy Boyfriend's Day! 💙</div>
                    Hi love happy boyfriend's day i know your not aware with this kind of thing 🫶 but it's okay i got you 😉<br><br>
                    i want to tell you that i love you so much even if sometimes your a headache but i still love you 🫶 ILOVEYOUSOMUCH MYLOVE 🫶<br><br>
                    dont get tired loving me even if sometimes I'm giving you all the trantrums WHAHAHA but always remember that i love you very much ❤️<br><br>
                    even if sometimes i even questions your love on me but i will always love you 🫶 MUAH MUAH MUAH
                </div>
            </div>
        </div>
        <div class="instructions">Click the envelope to open your special message 💙</div>
    </div>

    <script>
        document.getElementById('envelope').addEventListener('click', function() {
            this.classList.toggle('open');
            
            // Update instructions based on state
            const instructions = document.querySelector('.instructions');
            if (this.classList.contains('open')) {
                instructions.innerHTML = 'Click the envelope to close your special message 💙';
            } else {
                instructions.innerHTML = 'Click the envelope to open your special message 💙';
            }
        });
    </script>
</body>
</html>
