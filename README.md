# FREE-FIRE-ACADEMY
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Free Fire Academy - Guides & Education</title>
    <meta name="description" content="Improve your Free Fire skills with sensitivity calculators, guides, and daily quest tips.">
    <style>
        body { font-family: Arial, sans-serif; background-color: #1a1a1a; color: #fff; margin: 0; padding: 0; }
        header { background-color: #ff4500; padding: 20px; text-align: center; }
        nav { display: flex; justify-content: center; gap: 20px; margin: 10px 0; }
        nav a { color: #fff; text-decoration: none; font-weight: bold; }
        section { padding: 20px; max-width: 1200px; margin: 0 auto; }
        .calculator { background-color: #333; padding: 20px; border-radius: 10px; }
        .guides { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .guide-card { background-color: #444; padding: 15px; border-radius: 10px; }
        .cheat-sheet table { width: 100%; border-collapse: collapse; }
        .cheat-sheet th, .cheat-sheet td { border: 1px solid #fff; padding: 10px; text-align: left; }
        footer { text-align: center; padding: 10px; background-color: #222; }
        @media (max-width: 768px) { nav { flex-direction: column; } .guides { grid-template-columns: 1fr; } }
    </style>
</head>
<body>
    <header>
        <h1>The Free Fire Academy</h1>
        <p>Master Free Fire with tools, guides, and tips.</p>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#calculator">Sensitivity Calculator</a>
        <a href="#guides">Guides</a>
        <a href="#cheat-sheet">Daily Cheat Sheet</a>
    </nav>

    <section id="home">
        <h2>Welcome to the Academy</h2>
        <p>Level up your game with our free resources. From beginners to pros, we've got you covered.</p>
        <p>Featured: Check out our new Pro Guide on Drag Headshots!</p>
    </section>

    <section id="calculator" class="calculator">
        <h2>Headshot/Sensitivity Calculator</h2>
        <p>Enter your device and DPI to get optimal settings.</p>
        <form id="sens-form">
            <label>Device Model: <input type="text" id="device" placeholder="e.g., iPhone 13"></label><br>
            <label>DPI (for emulator): <input type="number" id="dpi" placeholder="400"></label><br>
            <button type="button" onclick="calculateSensitivity()">Calculate</button>
        </form>
        <div id="results"></div>
        <script>
            function calculateSensitivity() {
                const device = document.getElementById('device').value;
                const dpi = parseInt(document.getElementById('dpi').value);
                let general = 120, redDot = 80, twoX = 60, fourX = 40;
                if (dpi > 400) { general += 10; redDot += 5; } // Adjust based on DPI
                document.getElementById('results').innerHTML = `
                    <h3>Recommended Settings for ${device}:</h3>
                    <ul>
                        <li>General Sensitivity: ${general}%</li>
                        <li>Red Dot: ${redDot}%</li>
                        <li>2x Scope: ${twoX}%</li>
                        <li>4x Scope: ${fourX}%</li>
                    </ul>
                    <p>Tip: Test in training mode and tweak by 5-10%.</p>
                `;
            }
        </script>
    </section>

    <section id="guides">
        <h2>Beginner to Pro Guides</h2>
        <div class="guides">
            <div class="guide-card">
                <h3>Beginner: Loot Priority</h3>
                <p>Start with shotguns and armor. Prioritize health in the first 30 seconds.</p>
                <iframe width="100%" height="200" src="https://www.youtube.com/embed/sample-video-id" frameborder="0" allowfullscreen></iframe>
            </div>
            <div class="guide-card">
                <h3>Intermediate: Gloo Wall Placement Drills</h3>
                <p>Practice 45-degree angles. Drill: 5 walls in 10 seconds.</p>
                <iframe width="100%" height="200" src="https://www.youtube.com/embed/sample-video-id" frameborder="0" allowfullscreen></iframe>
            </div>
            <div class="guide-card">
                <h3>Pro: Master the Drag Headshot</h3>
                <p>Use 4x scope, lead shots. Combine with flashbangs.</p>
                <iframe width="100%" height="200" src="https://www.youtube.com/embed/sample-video-id" frameborder="0" allowfullscreen></iframe>
            </div>
        </div>
    </section>

    <section id="cheat-sheet">
        <h2>Daily Quests/Mission Cheat Sheet</h2>
        <p>Updated daily. Sample for today:</p>
        <div class="cheat-sheet">
            <table>
                <tr><th>Mission</th><th>Reward</th><th>Fastest Tip</th><th>Est. Time</th></tr>
                <tr><td>Win 2 Matches</td><td>500 Gold</td><td>Play Duo; early rotations.</td><td>10-15 mins</td></tr>
                <tr><td>Deal 10,000 Damage</td><td>Elite Points</td><td>Use AK; farm safe zones.</td><td>5-10 mins</td></tr>
                <tr><td>Revive 5 Teammates</td><td>Skin Fragment</td><td>Squad mode; prioritize revives.</td><td>15-20 mins</td></tr>
            </table>
        </div>
        <p>Note: Update manually or automate with a script.</p>
    </section>

    <footer>
        <p>&copy; 2023 The Free Fire Academy. Not affiliated with Garena. Follow us on [Social Links].</p>
        <p>Made by 3.tuux__</p>
    </footer>
</body>
</html>
