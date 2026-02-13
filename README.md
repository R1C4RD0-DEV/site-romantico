<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mayra ❤️ Ricardo</title>

<style>
body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff4e8b, #8a2be2);
    font-family: 'Segoe UI', sans-serif;
    color: white;
    text-align: center;
    overflow-x: hidden;
}

.container {
    padding: 40px 20px;
}

h1 {
    font-size: 2.5em;
    animation: fadeIn 2s ease-in-out;
}

p {
    font-size: 1.2em;
}

button {
    background: white;
    color: #ff4e8b;
    border: none;
    padding: 12px 25px;
    border-radius: 25px;
    font-size: 1em;
    cursor: pointer;
    margin-top: 20px;
    transition: 0.3s;
}

button:hover {
    background: #ffe6f0;
}

#carta {
    display: none;
    margin-top: 20px;
    background: rgba(255,255,255,0.2);
    padding: 20px;
    border-radius: 15px;
}

.heart {
    position: fixed;
    bottom: -10px;
    color: #fff;
    font-size: 20px;
    animation: subir 5s linear infinite;
}

@keyframes subir {
    0% {transform: translateY(0); opacity: 1;}
    100% {transform: translateY(-100vh); opacity: 0;}
}

@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}
</style>
</head>

<body>

<div class="container">
    <h1>Mayra Luiza ❤️ Ricardo</h1>
    <p>Desde o dia <strong>01/12/2025</strong> construindo a nossa história...</p>

    <h2 id="contador"></h2>

    <button onclick="mostrarCarta()">Abrir Carta 💌</button>

    <div id="carta">
        <p>
        Mayra, você é a melhor parte dos meus dias.  
        Seu sorriso muda meu humor, sua voz acalma meu mundo  
        e estar ao seu lado é o meu lugar favorito.  
        Eu escolheria você mil vezes, em qualquer vida. ❤️
        </p>
    </div>
</div>

<audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
function mostrarCarta() {
    document.getElementById("carta").style.display = "block";
}

function atualizarContador() {
    const inicio = new Date("2025-12-06T00:00:00");
    const agora = new Date();
    const diff = agora - inicio;

    const dias = Math.floor(diff / (1000 * 60 * 60 * 24));
    const horas = Math.floor((diff / (1000 * 60 * 60)) % 24);

    document.getElementById("contador").innerHTML =
        dias + " dias e " + horas + " horas juntos ❤️";
}

setInterval(atualizarContador, 1000);

function criarCoracao() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (3 + Math.random() * 2) + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(criarCoracao, 500);
</script>

</body>
</html>
