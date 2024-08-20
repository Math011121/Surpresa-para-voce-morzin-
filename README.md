# Surpresa-para-voce-morzin-
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surpresa para Você</title>
    <style>
        body {
            background-color: #800080; /* Roxo */
            color: #FFC0CB; /* Rosa claro */
            font-family: 'Courier New', Courier, monospace;
            text-align: center;
            margin: 0;
            animation: backgroundFade 10s infinite alternate;
        }

        @keyframes backgroundFade {
            0% { background-color: #800080; } /* Roxo */
            100% { background-color: #d36f6f; } /* Rosa mais escuro */
        }

        h1 {
            font-size: 3em;
            margin-top: 20px;
            font-weight: bold;
            letter-spacing: 2px;
            text-shadow: 0 0 10px #ff99cc, 0 0 20px #ff66b2, 0 0 30px #ff3385;
        }

        p {
            font-size: 1.5em;
            margin: 10px;
            line-height: 1.4;
            padding: 0 10px;
        }

        .slideshow-container {
            position: relative;
            max-width: 80%;
            height: 70vh; /* Altura ajustada */
            margin: 20px auto; /* Margens ajustadas */
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 0 20px rgba(255, 102, 178, 0.5);
            animation: slideshowFade 10s infinite alternate;
        }

        @keyframes slideshowFade {
            0% { box-shadow: 0 0 20px rgba(255, 102, 178, 0.5); }
            100% { box-shadow: 0 0 20px rgba(255, 153, 204, 0.6); } /* Rosa mais escuro */
        }

        .slides {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1.5s ease; /* Transição de opacidade mais suave */
        }

        .slides img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .active-slide {
            opacity: 1;
        }

        .dots {
            text-align: center;
            margin-top: 10px;
        }

        .dot {
            height: 12px;
            width: 12px;
            margin: 0 3px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
        }

        .active {
            background-color: #FFC0CB;
        }

        .timer {
            font-size: 2em;
            margin: 10px 0;
            color: #ff99cc;
            text-shadow: 0 0 10px #ff66b2;
        }

        .play-button {
            padding: 10px 20px;
            font-size: 1.5em;
            color: white;
            background-color: #FF69B4;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            margin: 10px;
            box-shadow: 0 0 10px rgba(255, 105, 180, 0.7);
            transition: background-color 0.3s, box-shadow 0.3s;
        }

        .play-button:hover {
            background-color: #FF1493;
            box-shadow: 0 0 20px rgba(255, 105, 180, 1);
        }

        /* Estilos para os corações */
        .heart-fall {
            position: fixed;
            top: -50px;
            font-size: 24px;
            color: #FF69B4;
            animation: fall linear infinite;
            opacity: 0.8;
            z-index: 9999;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh);
                opacity: 0;
            }
        }

        /* Animação de batimento cardíaco */
        @keyframes heartbeat {
            0% { transform: scale(1); }
            20% { transform: scale(1.1); }
            40% { transform: scale(1); }
            60% { transform: scale(1.1); }
            80% { transform: scale(1); }
            100% { transform: scale(1); }
        }

        .heart {
            animation: heartbeat 1.5s infinite;
        }

        /* Brilho nos textos */
        @keyframes glow {
            0% { text-shadow: 0 0 10px #FF69B4; }
            100% { text-shadow: 0 0 20px #FF1493; }
        }

        h1, p, .timer {
            animation: glow 2s infinite alternate;
        }
    </style>
</head>
<body>
    <h1>Para sempre juntos...</h1>

    <!-- Cronômetro -->
    <div id="timer" class="timer"></div>

    <div class="slideshow-container">
        <div class="slides">
            <img src="Foto11.jpg" alt="Foto 1">
        </div>
        <div class="slides">
            <img src="Foto22.jpg" alt="Foto 2">
        </div>
        <div class="slides">
            <img src="Foto33.jpg" alt="Foto 3">
        </div>
        <div class="slides">
            <img src="Foto44.jpg" alt="Foto 4">
        </div>
        <div class="slides">
            <img src="Foto55.jpg" alt="Foto 5">
        </div>
        <div class="slides">
            <img src="Foto66.jpg" alt="Foto 6">
        </div>
    </div>

    <p>Oiii princesinha da minha vidaa 🤗🤍, espero que você goste do nosso presentinho kkkkk, temos o nosso contador de dias para sempre morzinn 😁, cada segundinho vai ser contando e o meu amor por você vai ir aumentando cada vez mais, todos os dias estarei aqui do seu ladinho tá, EU TE AMO MUITOOO MUITOOOO 🤗😘🤍🩵💕💗♾️</p>

    <button class="play-button" onclick="playAudio()">Reproduzir Música</button>
    <audio id="background-audio" loop>
        <source src="musicamg.mp4" type="audio/mpeg">
        Seu navegador não suporta o elemento de áudio.
    </audio>

    <div class="dots">
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
    </div>

    <script>
        // Configuração da data inicial
        const startDate = new Date("March 4, 2024 13:53:00").getTime();

        function updateTimer() {
            const now = new Date().getTime();
            const distance = now - startDate;

            // Cálculos de tempo
            const years = Math.floor(distance / (1000 * 60 * 60 * 24 * 365));
            const months = Math.floor((distance % (1000 * 60 * 60 * 24 * 365)) / (1000 * 60 * 60 * 24 * 30));
            const days = Math.floor((distance % (1000 * 60 * 60 * 24 * 30)) / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            // Exibição do resultado
            document.getElementById("timer").innerHTML = 
                years + " anos, " + 
                months + " meses, " + 
                days + " dias, <br>" + 
                hours + " horas, " + 
                minutes + " minutos, " + 
                seconds + " segundos";

            // Atualiza a cada segundo
            setTimeout(updateTimer, 1000);
        }

        updateTimer();

        // Slideshow com fade-in e fade-out
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let slides = document.getElementsByClassName("slides");
            let dots = document.getElementsByClassName("dot");

            for (let i = 0; i < slides.length; i++) {
                slides[i].classList.remove("active-slide");
            }

            slideIndex++;
            if (slideIndex > slides.length) {slideIndex = 1}

            slides[slideIndex - 1].classList.add("active-slide");

            for (let i = 0; i < dots.length; i++) {
                dots[i].className = dots[i].className.replace(" active", "");
            }
            dots[slideIndex - 1].className += " active";

            setTimeout(showSlides, 3000); // Muda a cada 3 segundos
        }

        // Função para iniciar a música
        function playAudio() {
            const audio = document.getElementById('background-audio');
            audio.play().catch(error => {
                console.log('Erro ao tentar iniciar o áudio: ', error);
            });
        }

        // Função para criar os corações caindo
        function createHearts() {
            const heart = document.createElement('div');
            heart.classList.add('heart-fall');
            heart.innerHTML = '🤍';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 2 + 3 + 's'; // Entre 3s e 5s
            document.body.appendChild(heart);
            setTimeout(() => {
                heart.remove();
            }, 5000); // Remove o coração após 5s
        }

        // Cria os corações a cada intervalo de tempo
        setInterval(createHearts, 300);
    </script>
</body>
</html>