<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@esei</title>
    
    <!-- Favicon link (add your logo file path) -->
    <link rel="icon" href="assets/logo.ico" type="image/x-icon"> <!-- Replace 'assets/logo.ico' with your actual logo file path -->
    
    <!-- Google Fonts Link -->
    <link href="https://fonts.google.com/noto/specimen/Noto+Sans+Display?preview.text=misery302&amp;query=ancient" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000000;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #ffffff;
            font-family: 'Roboto', sans-serif;
            overflow: hidden;
            position: relative;
            cursor: url('assets/cursor.cur'), auto; /* Custom cursor */
        }

        /* Video Background Styling */
        #backgroundVideo {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            z-index: 0;
            display: none; /* Hidden initially */
            background-color: #000000;
            opacity: 0; /* Initially hidden */
            pointer-events: none; /* Prevent interaction with video */
            transition: opacity 2s ease-in-out; /* Fade-in animation */
        }

        .profile-container {
            position: relative;
            text-align: center;
            background-color: rgba(255, 255, 255, 0);
            padding: 20px;
            border-radius: 10px;
            z-index: 2;
        }

        .profile-pic {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            background: url('assets/invisible.png') center center no-repeat;
            background-size: cover;
            position: absolute;
            top: -210px;
            left: 50%;
            transform: translateX(-50%);
            border: 0px solid #000000;
        }

        .username {
            font-size: 40px;
            font-weight: normal;
            margin-top: -90px;
            position: relative;
            text-shadow: 1px 1px 20px rgba(0, 0, 0, 1); /* Shadow added here */
            background-image: url(assets/black_particle.gif);
            filter: drop-shadow(#000000 1px 0 7px);
        }

        .icon-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 60px;   
        }

        .icon {
            width: 40px;
            height: 40px;
            cursor: url('assets/cursor.cur'), auto; /* Custom cursor for icons */
            transition: transform 0.3s ease-in-out; /* Transition for scaling */
            filter: drop-shadow(#000000 1px 0 7px);
        }

        .icon:hover {
            transform: scale(1.2); /* Scale the icon by 20% */
        }

        /* Black Overlay */
        .black-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(8px);
            z-index: 4;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: url('assets/cursor.cur'), auto; /* Custom cursor for overlay */
            opacity: 1;
            transition: opacity 2s ease; /* Slow fade-out */
        }

        .rain {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 1;
            pointer-events: none;
        }

        .raindrop {
            position: absolute;
            top: -10%;
            width: 3px;
            height: 3px;
            background: white;
            opacity: 0.5;
            animation: fall linear infinite; /* Make it infinite */
        }

        @keyframes fall {
            0% {
                transform: translateY(0) translateX(0); /* Start at the top */
                opacity: 0.5; /* Start with full opacity */
            }
            100% {
                transform: translateY(120vh) translateX(calc(-10px + 20px * var(--direction))); /* Fall to the bottom */
                opacity: 0; /* Fade out as it falls */
            }
        }

    </style>
</head>
<body>

<!-- Background Video -->
<video id="backgroundVideo" muted="" loop="" autoplay="" playsinline="" style="display: block; opacity: 1;">
    <source src="assets/background.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

<!-- Black Blur Overlay -->
<div class="black-overlay" id="blackOverlay" style="opacity: 0; display: none;"></div>

<!-- Profile Container -->
<div class="profile-container">
    <div class="profile-pic"></div>
    <div class="username" id="username">eseire</div>
    <div class="icon-container">
        <a href="https://discord.com/users/640547461751898122" target="_blank">
            <img src="assets/discord_logo.svg" class="icon" alt="Discord">
        </a>
        <a href="https://tiktok.com/@eseire" target="_blank">
            <img src="assets/tiktok_logo.svg" class="icon" alt="TikTok">
        </a>
        <a href="https://instagram.com/anklechopper" target="_blank">
            <img src="assets/instagram_logo.svg" class="icon" alt="Instagram">
        </a>
    </div>
</div>

<!-- Rain Effect -->
<div class="rain" id="rainEffect"><div class="raindrop" style="left: 56.1686vw; animation-duration: 4.34765s; animation-delay: -0.511679s; --direction: 0.5768811960621898;"></div><div class="raindrop" style="left: 66.5253vw; animation-duration: 4.5222s; animation-delay: -0.69284s; --direction: -0.1401813977370785;"></div><div class="raindrop" style="left: 94.3382vw; animation-duration: 4.01023s; animation-delay: -4.34931s; --direction: -0.6422292357951256;"></div><div class="raindrop" style="left: 62.4054vw; animation-duration: 4.12479s; animation-delay: -0.000760058s; --direction: -0.8475049372136954;"></div><div class="raindrop" style="left: 77.1229vw; animation-duration: 4.18405s; animation-delay: -4.43185s; --direction: -0.15810532545912626;"></div><div class="raindrop" style="left: 69.8857vw; animation-duration: 4.82065s; animation-delay: -1.47904s; --direction: -0.3466158130528014;"></div><div class="raindrop" style="left: 65.345vw; animation-duration: 3.40169s; animation-delay: -3.80654s; --direction: 0.7512362797920145;"></div><div class="raindrop" style="left: 49.3728vw; animation-duration: 4.06921s; animation-delay: -0.310225s; --direction: 0.6958690643158407;"></div><div class="raindrop" style="left: 54.7838vw; animation-duration: 4.73334s; animation-delay: -0.546597s; --direction: -0.9816954279473173;"></div><div class="raindrop" style="left: 47.9814vw; animation-duration: 3.77988s; animation-delay: -1.08395s; --direction: -0.7519436484523041;"></div><div class="raindrop" style="left: 40.7259vw; animation-duration: 4.15279s; animation-delay: -4.40333s; --direction: 0.7257927750534305;"></div><div class="raindrop" style="left: 41.4733vw; animation-duration: 3.79043s; animation-delay: -4.01069s; --direction: -0.7503437303059246;"></div><div class="raindrop" style="left: 28.0481vw; animation-duration: 4.46554s; animation-delay: -1.73407s; --direction: -0.6435886256405396;"></div><div class="raindrop" style="left: 26.3788vw; animation-duration: 3.44399s; animation-delay: -4.24634s; --direction: -0.6224931310726145;"></div><div class="raindrop" style="left: 45.3876vw; animation-duration: 3.4808s; animation-delay: -0.341407s; --direction: 0.8687082529926791;"></div><div class="raindrop" style="left: 49.1674vw; animation-duration: 3.83868s; animation-delay: -4.79749s; --direction: 0.10157820980966337;"></div><div class="raindrop" style="left: 41.0086vw; animation-duration: 4.69827s; animation-delay: -2.55076s; --direction: 0.07636116177243268;"></div><div class="raindrop" style="left: 77.3864vw; animation-duration: 4.3433s; animation-delay: -4.9089s; --direction: 0.2311071466793182;"></div><div class="raindrop" style="left: 2.97484vw; animation-duration: 4.83566s; animation-delay: -4.94112s; --direction: 0.030441894093106825;"></div><div class="raindrop" style="left: 54.8964vw; animation-duration: 4.90183s; animation-delay: -2.83697s; --direction: -0.30671590717119956;"></div><div class="raindrop" style="left: 13.1907vw; animation-duration: 4.9555s; animation-delay: -0.00702373s; --direction: -0.9369466411967196;"></div><div class="raindrop" style="left: 46.8531vw; animation-duration: 2.37359s; animation-delay: -4.95871s; --direction: -0.7247338879667593;"></div><div class="raindrop" style="left: 9.98046vw; animation-duration: 3.54953s; animation-delay: -1.11437s; --direction: -0.33840944469154355;"></div><div class="raindrop" style="left: 26.3941vw; animation-duration: 4.36166s; animation-delay: -0.773526s; --direction: -0.5348749555821501;"></div><div class="raindrop" style="left: 15.4251vw; animation-duration: 3.3777s; animation-delay: -3.45217s; --direction: 0.2515390863485778;"></div><div class="raindrop" style="left: 38.4897vw; animation-duration: 4.01119s; animation-delay: -1.74878s; --direction: -0.003496991835363339;"></div><div class="raindrop" style="left: 16.5111vw; animation-duration: 4.67629s; animation-delay: -0.852181s; --direction: -0.22799094294685496;"></div><div class="raindrop" style="left: 80.5352vw; animation-duration: 2.57825s; animation-delay: -0.210809s; --direction: 0.36960639512244864;"></div><div class="raindrop" style="left: 80.3891vw; animation-duration: 4.41409s; animation-delay: -0.527186s; --direction: 0.8330505475040781;"></div><div class="raindrop" style="left: 26.7624vw; animation-duration: 3.03923s; animation-delay: -4.06411s; --direction: -0.28406052002937043;"></div><div class="raindrop" style="left: 42.8324vw; animation-duration: 2.5962s; animation-delay: -2.67115s; --direction: 0.4510002169746281;"></div><div class="raindrop" style="left: 37.1252vw; animation-duration: 3.47488s; animation-delay: -4.45442s; --direction: -0.5055216192231575;"></div><div class="raindrop" style="left: 19.4777vw; animation-duration: 3.90462s; animation-delay: -1.5924s; --direction: 0.4972089050722248;"></div><div class="raindrop" style="left: 12.0119vw; animation-duration: 4.22638s; animation-delay: -1.55025s; --direction: -0.6029344197012154;"></div><div class="raindrop" style="left: 51.7131vw; animation-duration: 2.6384s; animation-delay: -0.523379s; --direction: -0.28879297548424354;"></div><div class="raindrop" style="left: 43.2338vw; animation-duration: 3.98445s; animation-delay: -0.708445s; --direction: 0.21035554259989775;"></div><div class="raindrop" style="left: 12.5748vw; animation-duration: 4.06655s; animation-delay: -4.20472s; --direction: 0.884904763035884;"></div><div class="raindrop" style="left: 9.09964vw; animation-duration: 4.4743s; animation-delay: -1.45331s; --direction: -0.7531119521539611;"></div><div class="raindrop" style="left: 15.183vw; animation-duration: 4.04806s; animation-delay: -0.346113s; --direction: -0.6700058977534402;"></div><div class="raindrop" style="left: 38.6804vw; animation-duration: 4.88727s; animation-delay: -0.257247s; --direction: 0.4125314499509818;"></div><div class="raindrop" style="left: 98.2049vw; animation-duration: 4.27925s; animation-delay: -0.128625s; --direction: -0.9619727728804923;"></div><div class="raindrop" style="left: 83.79vw; animation-duration: 4.96456s; animation-delay: -0.612665s; --direction: 0.5032098626794164;"></div><div class="raindrop" style="left: 48.1308vw; animation-duration: 3.14916s; animation-delay: -1.49223s; --direction: 0.7667939181522403;"></div><div class="raindrop" style="left: 50.1397vw; animation-duration: 2.12741s; animation-delay: -0.297208s; --direction: 0.4105014068902091;"></div><div class="raindrop" style="left: 61.5239vw; animation-duration: 4.021s; animation-delay: -2.56703s; --direction: 0.7445020529563084;"></div><div class="raindrop" style="left: 46.2097vw; animation-duration: 4.64488s; animation-delay: -2.73791s; --direction: -0.8037921297315416;"></div><div class="raindrop" style="left: 85.2094vw; animation-duration: 4.52338s; animation-delay: -1.86867s; --direction: -0.8294492688219712;"></div><div class="raindrop" style="left: 31.1348vw; animation-duration: 2.03474s; animation-delay: -0.191322s; --direction: -0.3310269428266239;"></div><div class="raindrop" style="left: 52.8353vw; animation-duration: 4.68099s; animation-delay: -0.831532s; --direction: -0.3334928499374299;"></div><div class="raindrop" style="left: 32.0563vw; animation-duration: 3.72947s; animation-delay: -1.57615s; --direction: -0.38986073690657097;"></div><div class="raindrop" style="left: 96.9449vw; animation-duration: 2.27006s; animation-delay: -0.241785s; --direction: -0.8588123233345311;"></div><div class="raindrop" style="left: 73.8958vw; animation-duration: 3.2305s; animation-delay: -1.05039s; --direction: 0.3482889983121389;"></div><div class="raindrop" style="left: 16.3509vw; animation-duration: 4.73695s; animation-delay: -4.86291s; --direction: -0.2207111243291595;"></div><div class="raindrop" style="left: 50.3375vw; animation-duration: 4.86418s; animation-delay: -0.233145s; --direction: 0.4020245791868935;"></div><div class="raindrop" style="left: 22.2853vw; animation-duration: 3.33752s; animation-delay: -1.86774s; --direction: 0.984420258097368;"></div><div class="raindrop" style="left: 93.7752vw; animation-duration: 3.25894s; animation-delay: -0.813361s; --direction: -0.5637327533959762;"></div><div class="raindrop" style="left: 11.2006vw; animation-duration: 4.99707s; animation-delay: -3.32401s; --direction: -0.2306935265986021;"></div><div class="raindrop" style="left: 36.8594vw; animation-duration: 2.52658s; animation-delay: -1.14275s; --direction: 0.8913266402520694;"></div><div class="raindrop" style="left: 22.0785vw; animation-duration: 3.74662s; animation-delay: -4.82641s; --direction: 0.885208028694167;"></div><div class="raindrop" style="left: 92.0075vw; animation-duration: 4.02791s; animation-delay: -4.31353s; --direction: -0.8364032756988666;"></div><div class="raindrop" style="left: 46.2592vw; animation-duration: 2.90616s; animation-delay: -4.52292s; --direction: -0.9902067971371209;"></div><div class="raindrop" style="left: 79.1911vw; animation-duration: 3.79829s; animation-delay: -3.83429s; --direction: 0.0963213010142927;"></div><div class="raindrop" style="left: 85.2839vw; animation-duration: 2.32472s; animation-delay: -3.73403s; --direction: 0.667751656742082;"></div><div class="raindrop" style="left: 42.12vw; animation-duration: 2.13814s; animation-delay: -3.20559s; --direction: -0.10996321028141409;"></div><div class="raindrop" style="left: 69.964vw; animation-duration: 3.79649s; animation-delay: -2.32781s; --direction: -0.9379723280902432;"></div><div class="raindrop" style="left: 23.237vw; animation-duration: 2.90989s; animation-delay: -0.2023s; --direction: -0.7866648764393553;"></div><div class="raindrop" style="left: 67.4556vw; animation-duration: 4.35046s; animation-delay: -3.45751s; --direction: -0.04042362861244886;"></div><div class="raindrop" style="left: 27.3733vw; animation-duration: 4.08885s; animation-delay: -2.32058s; --direction: 0.7932946992988574;"></div><div class="raindrop" style="left: 98.3066vw; animation-duration: 2.81829s; animation-delay: -1.39733s; --direction: 0.6109001156049185;"></div><div class="raindrop" style="left: 26.5357vw; animation-duration: 3.78895s; animation-delay: -1.52537s; --direction: -0.1261156262681422;"></div><div class="raindrop" style="left: 13.7148vw; animation-duration: 4.80241s; animation-delay: -1.23639s; --direction: -0.8183877996001021;"></div><div class="raindrop" style="left: 28.3783vw; animation-duration: 3.6596s; animation-delay: -1.16517s; --direction: 0.48936177099451106;"></div><div class="raindrop" style="left: 86.8411vw; animation-duration: 4.62219s; animation-delay: -0.324625s; --direction: 0.7263593856672346;"></div><div class="raindrop" style="left: 61.2853vw; animation-duration: 2.78459s; animation-delay: -0.205475s; --direction: -0.44619463515972013;"></div><div class="raindrop" style="left: 12.4011vw; animation-duration: 2.10488s; animation-delay: -4.20906s; --direction: 0.45171055816169847;"></div><div class="raindrop" style="left: 35.3039vw; animation-duration: 3.76154s; animation-delay: -2.96306s; --direction: 0.6104754952252316;"></div><div class="raindrop" style="left: 69.9521vw; animation-duration: 3.14594s; animation-delay: -1.26497s; --direction: -0.4380785460809129;"></div><div class="raindrop" style="left: 45.4026vw; animation-duration: 3.96929s; animation-delay: -3.46469s; --direction: -0.1053050943500633;"></div><div class="raindrop" style="left: 61.1987vw; animation-duration: 4.56824s; animation-delay: -0.559654s; --direction: -0.1479097207834701;"></div><div class="raindrop" style="left: 86.5452vw; animation-duration: 3.76825s; animation-delay: -4.62828s; --direction: 0.11633800432838148;"></div><div class="raindrop" style="left: 46.0074vw; animation-duration: 4.55438s; animation-delay: -3.29937s; --direction: 0.5352365277585713;"></div><div class="raindrop" style="left: 95.5101vw; animation-duration: 3.0128s; animation-delay: -3.49451s; --direction: -0.5540919624470289;"></div><div class="raindrop" style="left: 39.8193vw; animation-duration: 3.56269s; animation-delay: -2.49284s; --direction: -0.689500364222488;"></div><div class="raindrop" style="left: 44.2675vw; animation-duration: 4.35643s; animation-delay: -1.21791s; --direction: -0.3012994098212296;"></div><div class="raindrop" style="left: 2.56166vw; animation-duration: 3.92205s; animation-delay: -3.472s; --direction: 0.4342097363685915;"></div><div class="raindrop" style="left: 18.2679vw; animation-duration: 2.19088s; animation-delay: -1.15676s; --direction: 0.7176105833297481;"></div><div class="raindrop" style="left: 62.7211vw; animation-duration: 2.77195s; animation-delay: -1.78809s; --direction: -0.7975392306929874;"></div><div class="raindrop" style="left: 85.7105vw; animation-duration: 3.01111s; animation-delay: -1.4811s; --direction: -0.46480790422309637;"></div><div class="raindrop" style="left: 96.215vw; animation-duration: 4.03574s; animation-delay: -3.31584s; --direction: -0.8828022373403734;"></div><div class="raindrop" style="left: 48.5174vw; animation-duration: 3.16181s; animation-delay: -4.44631s; --direction: -0.40779428620684266;"></div><div class="raindrop" style="left: 59.3628vw; animation-duration: 2.71454s; animation-delay: -1.2128s; --direction: 0.8298492216027604;"></div><div class="raindrop" style="left: 78.5629vw; animation-duration: 3.24534s; animation-delay: -4.98277s; --direction: -0.1911277893681338;"></div><div class="raindrop" style="left: 45.1274vw; animation-duration: 4.3648s; animation-delay: -1.58739s; --direction: -0.6993635306462629;"></div><div class="raindrop" style="left: 56.4461vw; animation-duration: 4.72339s; animation-delay: -3.90669s; --direction: 0.8281082600585461;"></div><div class="raindrop" style="left: 86.9288vw; animation-duration: 2.3049s; animation-delay: -1.09386s; --direction: 0.7904686398540988;"></div><div class="raindrop" style="left: 51.7989vw; animation-duration: 3.8597s; animation-delay: -1.23012s; --direction: 0.3052475520846878;"></div><div class="raindrop" style="left: 91.4138vw; animation-duration: 2.89503s; animation-delay: -3.70757s; --direction: 0.05716263399151211;"></div><div class="raindrop" style="left: 89.6672vw; animation-duration: 2.55403s; animation-delay: -3.88362s; --direction: -0.7047946934132785;"></div><div class="raindrop" style="left: 48.0879vw; animation-duration: 4.24056s; animation-delay: -3.07693s; --direction: -0.48509588529016723;"></div><div class="raindrop" style="left: 5.21564vw; animation-duration: 3.14015s; animation-delay: -0.694387s; --direction: -0.9163083355460455;"></div></div>

<audio id="backgroundMusic" loop="">
    <source src="assets/music.mp3" type="audio/mpeg">
    Your browser does not support the audio tag.
</audio>

<script>
    // Generate raindrops with random positions and speeds
    const rainContainer = document.getElementById('rainEffect');
    const raindropCount = 100;
    const maxRaindropDuration = 3;

    function createRaindrop() {
        const raindrop = document.createElement('div');
        raindrop.classList.add('raindrop');
        
        // Set random horizontal position
        raindrop.style.left = Math.random() * 100 + 'vw';
        
        // Set random animation duration (speed of fall)
        const duration = 2 + Math.random() * maxRaindropDuration; // Random duration for falling
        raindrop.style.animationDuration = `${duration}s`;
        
        // Set random animation delay (so that raindrops start at different times)
        raindrop.style.animationDelay = Math.random() * -5 + 's';
        
        // Random direction to make rain look more natural
        raindrop.style.setProperty('--direction', Math.random() * 2 - 1);

        // Append to rain container
        rainContainer.appendChild(raindrop);

        // Remove the raindrop after its animation ends, to keep the DOM clean
        raindrop.addEventListener('animationiteration', () => {
            raindrop.remove();
            createRaindrop();  // Create a new raindrop when one finishes falling
        });
    }

    // Create initial raindrops and continuously generate more
    for (let i = 0; i < raindropCount; i++) {
        createRaindrop();
    }

    // Play the background music and start video after overlay fade-out
    const blackOverlay = document.getElementById('blackOverlay');
    const music = document.getElementById('backgroundMusic');
    const video = document.getElementById('backgroundVideo');

    blackOverlay.addEventListener('click', () => {
        music.volume = 0;
        music.play();

        // Gradually increase music volume
        let volumeIncreaseInterval = setInterval(() => {
            if (music.volume < 1) {
                music.volume = Math.min(music.volume + 0.1, 1);
            } else {
                clearInterval(volumeIncreaseInterval);
            }
        }, 200);

        // Start fading out the overlay and fading in the video at the same time
        blackOverlay.style.opacity = '0';  // Fade out overlay
        video.style.display = 'block';  // Show video
        video.style.opacity = '1';  // Start fading in video

        // Play the video after the fade-in starts
        video.play();

        setTimeout(() => {
            blackOverlay.style.display = 'none'; // Hide the overlay completely after fade
        }, 2000); // Ensure the overlay fades out before it's hidden
    });

    // Typing and Deleting Effect for browser title
    const originalTitle = "@unkan";
    const deleteSpeed = 300; // Speed for deleting text in milliseconds
    const typingSpeed = 300; // Speed for typing text in milliseconds

    let titleIndex = 0;
    let titleDeleteIndex = originalTitle.length;

    // Typing effect function
    function typeTitle() {
        if (titleIndex < originalTitle.length) {
            document.title += originalTitle.charAt(titleIndex);
            titleIndex++;
            setTimeout(typeTitle, typingSpeed);
        } else {
            setTimeout(deleteTitle, 0); // Start deleting after typing
        }
    }

    // Deleting effect function
    function deleteTitle() {
        if (titleDeleteIndex >= 1) {
            document.title = document.title.slice(0, titleDeleteIndex);
            titleDeleteIndex--;
            setTimeout(deleteTitle, deleteSpeed);
        } else {
            titleIndex = 1;
            titleDeleteIndex = originalTitle.length;
            setTimeout(typeTitle, 0); // Start typing again after deleting
        }
    }

    // Start the typing effect when the page loads
    window.onload = () => {
        typeTitle();
        video.style.display = 'none';  // Hide video initially
    };

</script>



</body></html>
