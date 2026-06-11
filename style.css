let score = 0;
let eco = 50;
let time = 60;
let gameOver = false;

const scoreEl = document.getElementById("score");
const ecoEl = document.getElementById("eco");
const timeEl = document.getElementById("time");
const messageEl = document.getElementById("message");
const restartBtn = document.getElementById("restart");

function atualizarTela() {
    scoreEl.textContent = score;
    ecoEl.textContent = eco;
    timeEl.textContent = time;
}

function plantar() {
    if (gameOver) return;

    score += 10;
    eco += 5;

    messageEl.textContent =
        "Você plantou novas culturas sustentáveis 🌱";

    atualizarTela();
}

function irrigar() {
    if (gameOver) return;

    score += 5;
    eco += 8;

    messageEl.textContent =
        "Irrigação eficiente economiza água 💧";

    atualizarTela();
}

function colher() {
    if (gameOver) return;

    score += 20;
    eco -= 3;

    messageEl.textContent =
        "Boa colheita! Produção aumentada 🚜";

    atualizarTela();
}

function finalizarJogo() {
    gameOver = true;

    document.querySelectorAll(".action")
    .forEach(btn => btn.disabled = true);

    restartBtn.style.display = "inline-block";

    if (eco >= 80) {
        messageEl.textContent =
            `🏆 Parabéns! Você criou um Agro Forte e Sustentável! Pontuação: ${score}`;
    } else {
        messageEl.textContent =
            `⚠️ Sua fazenda produziu bem, mas pode ser mais sustentável. Pontuação: ${score}`;
    }
}

function reiniciar() {
    location.reload();
}

const cronometro = setInterval(() => {

    if (gameOver) {
        clearInterval(cronometro);
        return;
    }

    time--;
    atualizarTela();

    if (time <= 0) {
        clearInterval(cronometro);
        finalizarJogo();
    }

}, 1000);

atualizarTela();