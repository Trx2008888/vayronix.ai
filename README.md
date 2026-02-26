<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vayronix (VRNX) | Decentralized AI</title>
    <style>
        :root {
            --neon-blue: #00f3ff;
            --deep-space: #050505;
            --text-gray: #a0a0a0;
        }

        body {
            background-color: var(--deep-space);
            color: white;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            margin: 0;
            overflow-x: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }

        /* Animated Background */
        .grid-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: linear-gradient(to right, #111 1px, transparent 1px),
                              linear-gradient(to bottom, #111 1px, transparent 1px);
            background-size: 40px 40px;
            z-index: -1;
            mask-image: radial-gradient(circle, black, transparent 80%);
        }

        .container {
            text-align: center;
            padding: 20px;
            max-width: 800px;
        }

        .logo-area h1 {
            font-size: 3.5rem;
            letter-spacing: 10px;
            margin-bottom: 0;
            background: linear-gradient(to right, #fff, var(--neon-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(0, 243, 255, 0.3);
        }

        .tagline {
            color: var(--neon-blue);
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 5px;
            margin-bottom: 40px;
        }

        .terminal {
            background: rgba(0, 0, 0, 0.7);
            border: 1px solid #222;
            padding: 20px;
            border-radius: 10px;
            text-align: left;
            font-family: 'Courier New', Courier, monospace;
            margin-bottom: 30px;
            box-shadow: 0 0 30px rgba(0,0,0,0.5);
        }

        .status-line { color: #0f0; margin: 5px 0; }
        .loading-bar { color: var(--neon-blue); }

        .btn-group {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .main-btn {
            background: transparent;
            border: 1px solid var(--neon-blue);
            color: var(--neon-blue);
            padding: 15px 30px;
            font-size: 1rem;
            cursor: pointer;
            transition: 0.3s;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
            overflow: hidden;
        }

        .main-btn:hover {
            background: var(--neon-blue);
            color: black;
            box-shadow: 0 0 20px var(--neon-blue);
        }

        footer {
            margin-top: 50px;
            font-size: 0.8rem;
            color: var(--text-gray);
        }

        /* Interactive Response Styling */
        #status-msg {
            margin-top: 20px;
            height: 20px;
            font-weight: bold;
            color: var(--neon-blue);
        }
    </style>
</head>
<body>

    <div class="grid-bg"></div>

    <div class="container">
        <div class="logo-area">
            <h1>VAYRONIX</h1>
            <p class="tagline">Neural AI Network • Solana Ecosystem</p>
        </div>

        <div class="terminal" id="terminal">
            <div class="status-line">> Initializing VRNX Core...</div>
            <div class="status-line">> Created by Babul Kaur ji</div>
            <div class="status-line">> System: Decentralized Intelligence Active</div>
            <div class="loading-bar" id="loading">]████████████████████] 100%</div>
        </div>

        <div class="btn-group">
            <button class="main-btn" onclick="runAction('DEPLOY')">Deploy VRNX</button>
            <button class="main-btn" onclick="runAction('AUTH')">Initiate Auth</button>
            <button class="main-btn" onclick="runAction('NETWORK')">Network Status</button>
        </div>

        <div id="status-msg"></div>

        <footer>
            &copy; 2026 Vayronix.ai | Powered by Solana
        </footer>
    </div>

    <script>
        function runAction(type) {
            const msg = document.getElementById('status-msg');
            const term = document.getElementById('terminal');
            
            if(type === 'DEPLOY') {
                msg.innerText = "Connecting to Solana Mainnet... Please wait.";
                term.innerHTML += '<div class="status-line" style="color:yellow">> Attaching Neural Nodes...</div>';
            } else if(type === 'AUTH') {
                msg.innerText = "Requesting Authorization Signature...";
                alert("Babul Kaur ji's System: Security Layer Active. Authentication in progress.");
            } else if(type === 'NETWORK') {
                msg.innerText = "Latency: 14ms | Nodes: 1,024 Active";
            }
            
            // Clear message after 3 seconds
            setTimeout(() => { msg.innerText = ""; }, 3000);
        }
    </script>
</body>
</html>
