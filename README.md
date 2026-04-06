# Mine-stats-2.0
Enter nickname to stats player
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <title>Minecraft Statystyki</title>
    <style>
        body { font-family: sans-serif; background: #2c3e50; color: white; text-align: center; padding: 50px; }
        input { padding: 10px; border-radius: 5px; border: none; width: 200px; }
        button { padding: 10px 20px; border-radius: 5px; border: none; background: #27ae60; color: white; cursor: pointer; }
        #wynik { margin-top: 30px; }
        img { width: 150px; border: 5px solid #bdc3c7; border-radius: 10px; }
    </style>
</head>
<body>

    <h1>🔍 Minecraft Player Checker</h1>
    <p>Wpisz nick gracza, aby zobaczyć jego skina:</p>
    
    <input type="text" id="nickGracza" placeholder="Np. Notch">
    <button onclick="sprawdzGracza()">Sprawdź</button>

    <div id="wynik">
        <h2 id="wyswietlonyNick"></h2>
        <img id="avatarGracza" src="" style="display:none;">
    </div>

    <script>
        function sprawdzGracza() {
            const nick = document.getElementById('nickGracza').value;
            const imgElement = document.getElementById('avatarGracza');
            const tekstElement = document.getElementById('wyswietlonyNick');

            if(nick) {
                // Używamy darmowego API mc-heads.net
                imgElement.src = `https://mc-heads.net/body/${nick}`;
                imgElement.style.display = 'inline-block';
                tekstElement.innerText = `Gracz: ${nick}`;
            } else {
                alert("Wpisz najpierw nick!");
            }
        }
    </script>

</body>
</html>

