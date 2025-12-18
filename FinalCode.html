<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Mind Reader: AI Edition</title>

<style>
    /* Base Styles */
    body {
        font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        background-color: #f0f2f5;
        color: #1a1a1a;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
        overflow: hidden;
        transition: all 0.5s ease;
    }

    /* Dynamic Glitch Backgrounds */
    .level-1 { background-color: #e1e8ed; }
    .level-2 { background-color: #d1d8e0; border: 5px solid #3498db; }
    .level-3 { background-color: #2c3e50; color: white; }
    .level-max { 
        background-color: #000; 
        color: #ff0000; 
        text-shadow: 2px 2px #550000;
        animation: shake 0.2s infinite;
    }

    @keyframes shake {
        0% { transform: translate(1px, 1px) rotate(0deg); }
        20% { transform: translate(-1px, -2px) rotate(-1deg); }
        50% { transform: translate(-3px, 1px) rotate(1deg); }
        100% { transform: translate(1px, -1px) rotate(0deg); }
    }

    .game-card {
        background: rgba(255, 255, 255, 0.95);
        padding: 40px;
        width: 100%;
        max-width: 400px;
        border-radius: 20px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        text-align: center;
        transition: transform 0.3s ease;
    }

    .level-max .game-card {
        background: rgba(20, 20, 20, 0.9);
        border: 2px solid #ff0000;
        color: white;
    }

    h1 { margin-bottom: 10px; }
    
    /* Progress Bar */
    .progress-container {
        background: #eee;
        border-radius: 10px;
        height: 10px;
        margin: 20px 0;
        overflow: hidden;
    }
    #progress-bar {
        background: #3498db;
        height: 100%;
        width: 0%;
        transition: width 0.4s ease, background 0.4s;
    }

    input[type="number"] {
        width: 80%;
        padding: 12px;
        border: 2px solid #ddd;
        border-radius: 8px;
        font-size: 1.2rem;
        text-align: center;
        outline: none;
    }

    .btn-group { margin-top: 20px; }
    
    button {
        padding: 12px 25px;
        border: none;
        border-radius: 8px;
        font-weight: bold;
        cursor: pointer;
        transition: 0.2s;
        margin: 5px;
    }

    .btn-guess { background: #3498db; color: white; }
    .btn-guess:hover { background: #2980b9; transform: scale(1.05); }
    .btn-reset { background: #95a5a6; color: white; }

    #feedback { font-size: 1.1rem; margin-top: 20px; min-height: 1.5em; }
</style>
</head>

<body>

<div class="game-card">
    <h1 id="title">🤖 Mind Reader</h1>
    <p>The AI has chosen a number. Can you extract it?</p>

    <select id="difficulty" style="margin-bottom: 15px; padding: 5px;">
        <option value="10">Easy (1-10)</option>
        <option value="50">Medium (1-50)</option>
        <option value="100" selected>Hard (1-100)</option>
    </select>

    <div class="progress-container">
        <div id="progress-bar"></div>
    </div>

    <input type="number" id="guessInput" placeholder="Enter Guess" autofocus>

    <div class="btn-group">
        <button class="btn-guess" onclick="makeGuess()">Analyze</button>
        <button class="btn-reset" onclick="resetGame()">Reset System</button>
    </div>

    <p id="feedback">System Ready.</p>
    <p id="attempts-text" style="font-size: 0.8rem; color: #7f8c8d;">Attempts Used: 0 / 10</p>
    
    <a href="scratch.html" style="display:block; margin-top:20px; color:#3498db; text-decoration:none; font-size:0.9rem;">← Back to Scratch Page</a>
</div>

<script>
    let maxNumber = 100;
    let secretNumber = Math.floor(Math.random() * maxNumber) + 1;
    let attempts = 0;
    const maxAttempts = 10;

    const input = document.getElementById("guessInput");
    
    // Allow "Enter" key to submit guess
    input.addEventListener("keypress", (e) => {
        if (e.key === "Enter") makeGuess();
    });

    document.getElementById("difficulty").addEventListener("change", function() {
        maxNumber = parseInt(this.value);
        resetGame();
    });

    function makeGuess() {
        const guess = parseInt(input.value);
        const feedback = document.getElementById("feedback");
        const bar = document.getElementById("progress-bar");

        if (isNaN(guess) || guess < 1 || guess > maxNumber) {
            feedback.textContent = "Error: Input out of bounds.";
            feedback.style.color = "#e67e22";
            return;
        }

        attempts++;
        updateUI(guess);

        if (guess === secretNumber) {
            feedback.textContent = "SUCCESS: Mind match found!";
            feedback.style.color = "#27ae60";
            endGame(true);
        } else if (attempts >= maxAttempts) {
            feedback.textContent = `CRITICAL FAILURE: Number was ${secretNumber}`;
            feedback.style.color = "#c0392b";
            endGame(false);
        } else {
            feedback.textContent = guess < secretNumber ? "STATUS: Too Low" : "STATUS: Too High";
            feedback.style.color = "#34495e";
        }
        
        input.value = "";
        input.focus();
    }

    function updateUI() {
        const percentage = (attempts / maxAttempts) * 100;
        const bar = document.getElementById("progress-bar");
        bar.style.width = percentage + "%";
        
        document.getElementById("attempts-text").textContent = `Attempts Used: ${attempts} / ${maxAttempts}`;

        // Dynamic Styling based on attempts
        if (attempts >= 9) {
            document.body.className = "level-max";
            bar.style.background = "#ff0000";
        } else if (attempts >= 7) {
            document.body.className = "level-3";
            bar.style.background = "#e67e22";
        } else if (attempts >= 4) {
            document.body.className = "level-2";
            bar.style.background = "#f1c40f";
        } else {
            document.body.className = "level-1";
        }
    }

    function endGame(win) {
        input.disabled = true;
        document.querySelector(".btn-guess").disabled = true;
        if(win) {
            document.getElementById("title").textContent = "🔓 Access Granted";
        } else {
            document.getElementById("title").textContent = "🔒 System Locked";
        }
    }

    function resetGame() {
        secretNumber = Math.floor(Math.random() * maxNumber) + 1;
        attempts = 0;
        document.body.className = "";
        input.disabled = false;
        input.value = "";
        document.querySelector(".btn-guess").disabled = false;
        document.getElementById("progress-bar").style.width = "0%";
        document.getElementById("feedback").textContent = "System Ready.";
        document.getElementById("feedback").style.color = "#333";
        document.getElementById("title").textContent = "🤖 Mind Reader";
        document.getElementById("attempts-text").textContent = "Attempts Used: 0 / 10";
    }
</script>

</body>
</html>
