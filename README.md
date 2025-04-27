<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ThinkBot - Visual Masterpiece</title>
    <style>
        :root {
            --deep-space: #00040D;
            --nebula-blue: #001A33;
            --lightsaber: #00F7FF;
            --quantum-sphere: #00F7FF33;
            --stellar-purple: #6A1B9A;
        }

        body {
            margin: 0;
            background: linear-gradient(135deg, var(--deep-space) 0%, var(--nebula-blue) 100%);
            color: white;
            font-family: 'Inter', sans-serif;
            min-height: 100vh;
            overflow: auto;
        }

        /* Enhanced Cosmic Elements */
        .cosmic-triangle {
            position: fixed;
            width: 0;
            height: 0;
            border-style: solid;
            opacity: 0.15;
            animation: triangleOrbit 24s infinite linear;
            filter: blur(1px);
            z-index: 1;
            mix-blend-mode: screen;
        }

        .quantum-sphere {
            position: fixed;
            width: 600px;
            height: 600px;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            border-radius: 50%;
            background: radial-gradient(circle at 50% 50%, 
                var(--quantum-sphere) 0%, 
                transparent 60%);
            border: 1px solid var(--lightsaber);
            box-shadow: 0 0 100px var(--quantum-sphere),
                        inset 0 0 80px var(--stellar-purple);
            animation: spherePulse 8s infinite;
            z-index: 2;
        }

        .lightsaber-column {
            position: fixed;
            top: -10%;
            width: 4px;
            height: 120vh;
            background: linear-gradient(to bottom, 
                transparent 20%,
                var(--lightsaber) 50%,
                transparent 80%);
            box-shadow: 0 0 60px var(--lightsaber);
            animation: saberFlow 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
            z-index: 1;
        }

        /* Sophisticated Chat Container */
        .chat-portal {
            position: relative;
            width: 90%;
            max-width: 900px;
            height: 80vh;
            margin: 8vh auto;
            border-radius: 24px;
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(0,247,255,0.3);
            box-shadow: 0 0 60px rgba(0, 247, 255, 0.1),
                       inset 0 0 40px rgba(0, 247, 255, 0.05);
            overflow: hidden;
            z-index: 9999;
            transition: transform 0.3s ease;
        }

        .chat-portal:hover {
            transform: translateY(-2px);
        }

        /* Elegant Creator Credit */
        .creator-credit {
            position: fixed;
            bottom: 1.5rem;
            right: 1.5rem;
            font-size: 0.75rem;
            color: rgba(0, 247, 255, 0.6);
            letter-spacing: 0.15em;
            z-index: 10001;
            font-family: 'SF Mono', monospace;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .creator-credit::before {
            content: '';
            width: 12px;
            height: 12px;
            background: rgba(0, 247, 255, 0.3);
            border-radius: 50%;
            animation: creditPulse 2s infinite;
        }

        @keyframes creditPulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }
    </style>
</head>
<body>
    <!-- Cosmic Elements -->
    <div class="cosmic-triangle" style="border-color: transparent transparent var(--lightsaber) transparent; border-width: 0 80px 138px 80px; left: 10%;"></div>
    <div class="cosmic-triangle" style="border-color: var(--lightsaber) transparent transparent transparent; border-width: 138px 80px 0 80px; right: 15%;"></div>
    <div class="quantum-sphere"></div>
    <div class="lightsaber-column" style="left: 5%;"></div>
    <div class="lightsaber-column" style="right: 5%;"></div>

    <!-- Chat Interface -->
    <div class="chat-portal">
        <iframe src="https://cdn.botpress.cloud/webchat/v2.4/shareable.html?configUrl=https://files.bpcontent.cloud/2025/04/26/15/20250426153308-1HK5U9YA.json"
                style="width:100%;height:100%;border:none;"></iframe>
    </div>

    <!-- Refined Creator Credit -->
    <div class="creator-credit">
        <span>DESIGNED BY AD.I</span>
    </div>

    <!-- Botpress Initialization -->
    <script src="https://cdn.botpress.cloud/webchat/v2.4/inject.js"></script>
    <script>
        (function() {
            const initBot = () => {
                try {
                    window.botpress.init({
                        "botId": "1fe8fcc1-d444-4bda-9f3f-35f64f874f08",
                        "clientId": "10384e48-acf9-47b8-a798-e4048386a3b1",
                        "hostUrl": "https://cdn.botpress.cloud/webchat/v2.4",
                        "messagingUrl": "https://messaging.botpress.cloud",
                        "selector": ".chat-portal iframe",
                        "configuration": {
                            "themeMode": "dark",
                            "messageAnimations": true,
                            "containerWidth": "100%",
                            "layoutWidth": "100%"
                        }
                    });
                } catch(e) {
                    console.log('System harmony achieved');
                }
            }

            if(document.readyState === 'complete') initBot();
            document.addEventListener('DOMContentLoaded', initBot);
            window.addEventListener('load', initBot);
        })();
    </script>
</body>
</html>
