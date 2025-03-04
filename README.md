<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Min webbsida</title>
    <style>
        html, body {
            height: 100%;
            margin: 0;
            padding: 0;
        }

        body {
            background-image: url('https://blog.wasalt.sa/en/wp-content/uploads/2024/11/Ramadan-2025-1.webp');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            color: #fff;
            font-family: Arial, sans-serif;
            padding: 20px;
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        h2 {
            color: #ffcc00;
            font-size: 2em;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }

        a {
            color: #ffcc00;
            text-decoration: none;
            margin: 5px 0;
        }

        a:hover {
            color: #ff6600;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin: 5px 0;
        }

        #countdown {
            font-size: 1.5em;
            margin: 10px 0;
            color: #ffcc00;
        }

        .container {
            max-width: 800px;
            width: 100%;
            padding: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }

        @media (max-width: 600px) {
            h2 {
                font-size: 1.5em;
            }

            #countdown {
                font-size: 1.2em;
            }

            body {
                padding: 10px;
            }

            .container {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <a href="https://www.google.com/maps/dir/?api=1&destination=Klangv%C3%A4gen+2,Stockholm" target="_blank">Vägbeskrivning</a>

        <a href="https://forms.gle/3jYMd922GGoejaFr7" target="_blank">Anmäl dig till iftar här</a>

        <h2>Info om Ramadan Iftar</h2>
        <div id="countdown"></div>

        <ul>
            <li>Ramadan 15/3</li>
            <li>Plats: Klangvägen 2</li>
            <li>Klockan: 17:00</li>
            <li>Det kommer finnas aktiviteter efter iftar, Inshallah</li>
        </ul>

        <a href="https://islam.nu/bonetider/stockholm/2025/03/">Bönetider under ramadan</a>
        <h2>Länkar</h2>
        <a href="https://www.google.com/search?q=Ramadan" target="_blank">Ramadan</a><br>
        <a href="https://islam.nu/e-bocker/rattsbestammelser-fiqh/ramadanboken/" target="_blank">Ladda ner grundläggande förklaring av den fjärde pelaren i islam</a>

        <!-- SoundCloud inbäddning för automatisk uppspelning -->
        <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/29819254&color=%23ff5500&auto_play=true"></iframe>
    </div>

    <script>
        // Nedräkning till iftar
        const iftarDate = new Date('2025-03-16T17:00:00').getTime();

        const countdown = setInterval(() => {
            const now = new Date().getTime();
            const timeLeft = iftarDate - now;

            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

            document.getElementById("countdown").innerHTML = `Nedräkning till Iftar: ${days} dagar, ${hours} timmar, ${minutes} minuter och ${seconds} sekunder.`;

            if (timeLeft < 0) {
                clearInterval(countdown);
                document.getElementById("countdown").innerHTML = "Det är dags för iftar!";
            }
        }, 1000);
    </script>
</body>
</html>
