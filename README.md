# pardofederico13-byte.github.io
pardofederico13-byte.github.io
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OG-Tushin | Streamer Oficial</title>
    <link rel="icon" type="image/png" href="/mnt/kimi/upload/Gaming%20YouTube%20Channel%20Logo%20in%20Blue%20Pink%20Typelectric%20Style(1).png">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --neon-blue: #00d4ff;
            --neon-pink: #ff00ff;
            --dark-bg: #0a0a0f;
            --panel-bg: rgba(20, 20, 30, 0.95);
            --text-primary: #ffffff;
            --text-secondary: #b0b0b0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--dark-bg);
            color: var(--text-primary);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Fondo animado mejorado */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 212, 255, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 50%, rgba(255, 0, 255, 0.15) 0%, transparent 50%),
                var(--dark-bg);
        }

        .grid-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 212, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 0, 255, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -1;
            pointer-events: none;
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: rgba(10, 10, 15, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0, 212, 255, 0.2);
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-small {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid transparent;
            background: linear-gradient(var(--dark-bg), var(--dark-bg)) padding-box,
                        linear-gradient(45deg, var(--neon-blue), var(--neon-pink)) border-box;
            box-shadow: 0 0 15px rgba(0, 212, 255, 0.5);
            animation: pulse-small 2s infinite;
        }

        @keyframes pulse-small {
            0%, 100% { box-shadow: 0 0 15px rgba(0, 212, 255, 0.5); }
            50% { box-shadow: 0 0 25px rgba(255, 0, 255, 0.8); }
        }

        .streamer-name {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Botón de configuración */
        .config-btn {
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            color: white;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
            box-shadow: 0 0 15px rgba(0, 212, 255, 0.4);
        }

        .config-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 0 25px rgba(255, 0, 255, 0.6);
        }

        /* Panel de configuración desplegable */
        .config-panel {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background: var(--panel-bg);
            backdrop-filter: blur(20px);
            border-left: 2px solid var(--neon-blue);
            z-index: 2000;
            transition: right 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            overflow-y: auto;
            padding: 30px;
            box-shadow: -10px 0 30px rgba(0, 0, 0, 0.5);
        }

        .config-panel.active {
            right: 0;
        }

        .panel-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(0, 212, 255, 0.3);
        }

        .panel-title {
            font-size: 1.5rem;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .close-panel {
            background: none;
            border: none;
            color: var(--text-primary);
            font-size: 1.5rem;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .close-panel:hover {
            transform: rotate(90deg);
            color: var(--neon-pink);
        }

        .config-section {
            margin-bottom: 30px;
        }

        .config-section h3 {
            color: var(--neon-blue);
            margin-bottom: 15px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .input-group {
            margin-bottom: 20px;
        }

        .input-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .input-group input,
        .input-group textarea,
        .input-group select {
            width: 100%;
            padding: 12px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(0, 212, 255, 0.3);
            border-radius: 8px;
            color: var(--text-primary);
            font-size: 1rem;
            transition: all 0.3s;
        }

        .input-group input:focus,
        .input-group textarea:focus,
        .input-group select:focus {
            outline: none;
            border-color: var(--neon-pink);
            box-shadow: 0 0 10px rgba(255, 0, 255, 0.3);
        }

        .input-group textarea {
            resize: vertical;
            min-height: 80px;
        }

        .color-picker-wrapper {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        input[type="color"] {
            width: 50px;
            height: 40px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }

        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }

        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(255, 255, 255, 0.1);
            transition: .4s;
            border-radius: 24px;
        }

        .slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }

        input:checked + .slider {
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
        }

        input:checked + .slider:before {
            transform: translateX(26px);
        }

        .save-btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            border: none;
            border-radius: 10px;
            color: white;
            font-weight: bold;
            cursor: pointer;
            font-size: 1.1rem;
            transition: transform 0.3s;
            margin-top: 20px;
        }

        .save-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(0, 212, 255, 0.3);
        }

        /* Contenido principal */
        main {
            margin-top: 90px;
            padding: 20px;
            max-width: 1400px;
            margin-left: auto;
            margin-right: auto;
        }

        /* HERO SECTION CON LOGO PRINCIPAL */
        .hero-section {
            text-align: center;
            padding: 40px 20px 60px;
            margin-bottom: 40px;
            position: relative;
        }

        /* Contenedor del logo principal */
        .main-logo-container {
            position: relative;
            display: inline-block;
            margin-bottom: 40px;
        }

        /* Anillo de luz alrededor del logo */
        .logo-ring {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 420px;
            height: 420px;
            border-radius: 50%;
            background: conic-gradient(from 0deg, var(--neon-blue), var(--neon-pink), var(--neon-blue));
            animation: rotate 10s linear infinite;
            filter: blur(20px);
            opacity: 0.6;
            z-index: -1;
        }

        .logo-ring-inner {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 400px;
            height: 400px;
            border-radius: 50%;
            border: 3px solid transparent;
            background: linear-gradient(var(--dark-bg), var(--dark-bg)) padding-box,
                        linear-gradient(45deg, var(--neon-blue), var(--neon-pink)) border-box;
            box-shadow: 
                0 0 60px rgba(0, 212, 255, 0.4),
                inset 0 0 60px rgba(255, 0, 255, 0.1);
            animation: pulse-ring 3s ease-in-out infinite;
        }

        @keyframes rotate {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(360deg); }
        }

        @keyframes pulse-ring {
            0%, 100% { 
                box-shadow: 0 0 60px rgba(0, 212, 255, 0.4), inset 0 0 60px rgba(255, 0, 255, 0.1);
                transform: translate(-50%, -50%) scale(1);
            }
            50% { 
                box-shadow: 0 0 100px rgba(255, 0, 255, 0.6), inset 0 0 80px rgba(0, 212, 255, 0.2);
                transform: translate(-50%, -50%) scale(1.02);
            }
        }

        /* Logo principal */
        .main-logo {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            position: relative;
            z-index: 10;
            border: 4px solid transparent;
            background: linear-gradient(var(--dark-bg), var(--dark-bg)) padding-box,
                        linear-gradient(45deg, var(--neon-blue), var(--neon-pink)) border-box;
            box-shadow: 
                0 0 80px rgba(0, 212, 255, 0.6),
                0 0 120px rgba(255, 0, 255, 0.4);
            animation: float-logo 4s ease-in-out infinite;
            transition: transform 0.3s;
        }

        .main-logo:hover {
            transform: scale(1.05);
            filter: brightness(1.1);
        }

        @keyframes float-logo {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            25% { transform: translateY(-15px) rotate(1deg); }
            50% { transform: translateY(-5px) rotate(0deg); }
            75% { transform: translateY(-20px) rotate(-1deg); }
        }

        /* Partículas alrededor del logo */
        .particles {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 500px;
            height: 500px;
            pointer-events: none;
            z-index: 5;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: var(--neon-blue);
            border-radius: 50%;
            box-shadow: 0 0 10px var(--neon-blue);
            animation: particle-float 6s infinite;
        }

        .particle:nth-child(odd) {
            background: var(--neon-pink);
            box-shadow: 0 0 10px var(--neon-pink);
        }

        @keyframes particle-float {
            0%, 100% { 
                transform: translate(0, 0) scale(0);
                opacity: 0;
            }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { 
                transform: translate(var(--tx), var(--ty)) scale(0);
                opacity: 0;
            }
        }

        .hero-title {
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink), var(--neon-blue));
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-transform: uppercase;
            letter-spacing: 5px;
            font-weight: 900;
            animation: shine 3s linear infinite;
            text-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
        }

        @keyframes shine {
            to { background-position: 200% center; }
        }

        .hero-subtitle {
            font-size: 1.4rem;
            color: var(--text-secondary);
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.6;
        }

        /* Botones de acción rápida */
        .hero-actions {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .hero-btn {
            padding: 15px 40px;
            border-radius: 30px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            font-size: 1rem;
        }

        .hero-btn.primary {
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            color: white;
            border: none;
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.4);
        }

        .hero-btn.secondary {
            background: transparent;
            color: var(--neon-blue);
            border: 2px solid var(--neon-blue);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        .hero-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.5);
        }

        .hero-btn.secondary:hover {
            background: rgba(0, 212, 255, 0.1);
            border-color: var(--neon-pink);
            color: var(--neon-pink);
        }

        /* Botones de redes sociales */
        .social-connections {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-bottom: 50px;
        }

        .social-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(0, 212, 255, 0.2);
            border-radius: 20px;
            padding: 30px;
            width: 280px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .social-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .social-card:hover::before {
            left: 100%;
        }

        .social-card:hover {
            transform: translateY(-10px);
            border-color: var(--neon-pink);
            box-shadow: 0 20px 40px rgba(255, 0, 255, 0.2);
        }

        .social-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .facebook { color: #1877f2; }
        .tiktok { 
            background: linear-gradient(45deg, #ff0050, #00f2ea);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .kick { color: #53fc18; }

        .social-name {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .social-status {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            background: rgba(0, 212, 255, 0.1);
            color: var(--neon-blue);
        }

        .social-status.connected {
            background: rgba(83, 252, 24, 0.1);
            color: #53fc18;
        }

        /* Sección de Videos/Streams */
        .content-section {
            margin-bottom: 60px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 20px;
        }

        .section-title {
            font-size: 2rem;
            color: var(--text-primary);
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .live-indicator {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 20px;
            background: rgba(255, 0, 0, 0.2);
            border: 1px solid #ff0000;
            border-radius: 25px;
            color: #ff4444;
            font-weight: bold;
            animation: blink 1.5s infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.6; }
        }

        .live-dot {
            width: 10px;
            height: 10px;
            background: #ff0000;
            border-radius: 50%;
            box-shadow: 0 0 10px #ff0000;
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
        }

        .video-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid rgba(0, 212, 255, 0.1);
            transition: all 0.3s;
            cursor: pointer;
        }

        .video-card:hover {
            transform: scale(1.02);
            border-color: var(--neon-blue);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.2);
        }

        .video-thumbnail {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(255, 0, 255, 0.1));
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .play-btn {
            width: 60px;
            height: 60px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--neon-blue);
            font-size: 1.5rem;
            transition: all 0.3s;
            border: 2px solid var(--neon-blue);
        }

        .video-card:hover .play-btn {
            background: var(--neon-blue);
            color: white;
            transform: scale(1.1);
        }

        .video-info {
            padding: 20px;
        }

        .video-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--text-primary);
        }

        .video-meta {
            display: flex;
            gap: 20px;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .video-meta span {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .platform-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            padding: 5px 10px;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 5px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Estadísticas */
        .stats-bar {
            display: flex;
            justify-content: center;
            gap: 60px;
            margin: 50px 0;
            flex-wrap: wrap;
            padding: 30px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            border: 1px solid rgba(0, 212, 255, 0.1);
        }

        .stat-item {
            text-align: center;
            position: relative;
        }

        .stat-item::after {
            content: '';
            position: absolute;
            right: -30px;
            top: 50%;
            transform: translateY(-50%);
            width: 1px;
            height: 40px;
            background: linear-gradient(to bottom, transparent, var(--neon-blue), transparent);
        }

        .stat-item:last-child::after {
            display: none;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1;
        }

        .stat-label {
            color: var(--text-secondary);
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-top: 10px;
        }

        /* Overlay para móvil */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1500;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
        }

        .overlay.active {
            opacity: 1;
            visibility: visible;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header {
                padding: 15px 20px;
            }

            .main-logo {
                width: 250px;
                height: 250px;
            }

            .logo-ring, .logo-ring-inner {
                width: 300px;
                height: 300px;
            }

            .hero-title {
                font-size: 2.5rem;
            }

            .config-panel {
                width: 100%;
                right: -100%;
            }

            .video-grid {
                grid-template-columns: 1fr;
            }

            .social-connections {
                flex-direction: column;
                align-items: center;
            }

            .stats-bar {
                gap: 30px;
            }

            .stat-item::after {
                display: none;
            }

            .stat-number {
                font-size: 2rem;
            }
        }

        /* Animaciones adicionales */
        .glow-text {
            text-shadow: 0 0 10px currentColor;
        }
    </style>
</head>
<body>
    <div class="bg-animation"></div>
    <div class="grid-overlay"></div>
    <div class="overlay" id="overlay"></div>

    <!-- Header -->
    <header>
        <div class="logo-container">
            <img src="/mnt/kimi/upload/Gaming%20YouTube%20Channel%20Logo%20in%20Blue%20Pink%20Typelectric%20Style(1).png" alt="OG-Tushin Logo" class="logo-small">
            <span class="streamer-name" id="headerName">OG-Tushin</span>
        </div>
        <button class="config-btn" onclick="toggleConfig()">
            <i class="fas fa-cog"></i>
            Configuración
        </button>
    </header>

    <!-- Panel de Configuración -->
    <div class="config-panel" id="configPanel">
        <div class="panel-header">
            <h2 class="panel-title"><i class="fas fa-sliders-h"></i> Configuración</h2>
            <button class="close-panel" onclick="toggleConfig()">
                <i class="fas fa-times"></i>
            </button>
        </div>

        <div class="config-section">
            <h3><i class="fas fa-user"></i> Perfil</h3>
            <div class="input-group">
                <label>Nombre del Canal</label>
                <input type="text" id="configChannelName" value="OG-Tushin" oninput="updateContent()">
            </div>
            <div class="input-group">
                <label>Descripción</label>
                <textarea id="configDescription" oninput="updateContent()">Streamer profesional de gaming. ¡Únete a mis streams diarios!</textarea>
            </div>
        </div>

        <div class="config-section">
            <h3><i class="fas fa-palette"></i> Apariencia</h3>
            <div class="input-group">
                <label>Color Principal</label>
                <div class="color-picker-wrapper">
                    <input type="color" id="primaryColor" value="#00d4ff" onchange="updateColors()">
                    <span>Azul Neón</span>
                </div>
            </div>
            <div class="input-group">
                <label>Color Secundario</label>
                <div class="color-picker-wrapper">
                    <input type="color" id="secondaryColor" value="#ff00ff" onchange="updateColors()">
                    <span>Rosa Neón</span>
                </div>
            </div>
        </div>

        <div class="config-section">
            <h3><i class="fas fa-share-alt"></i> Redes Sociales</h3>
            <div class="input-group">
                <label>Usuario de Facebook</label>
                <input type="text" id="configFacebook" value="@OGTushin" oninput="updateSocial()">
            </div>
            <div class="input-group">
                <label>Usuario de TikTok</label>
                <input type="text" id="configTiktok" value="@og.tushin" oninput="updateSocial()">
            </div>
            <div class="input-group">
                <label>Usuario de Kick</label>
                <input type="text" id="configKick" value="og-tushin" oninput="updateSocial()">
            </div>
        </div>

        <div class="config-section">
            <h3><i class="fas fa-video"></i> Stream</h3>
            <div class="input-group">
                <label>Título del Stream Actual</label>
                <input type="text" id="configStreamTitle" value="🔴 EN VIVO: Compitiendo en Rankeds" oninput="updateStream()">
            </div>
            <div class="input-group">
                <label style="display: flex; justify-content: space-between; align-items: center;">
                    Mostrar indicador LIVE
                    <label class="toggle-switch">
                        <input type="checkbox" id="showLive" checked onchange="toggleLive()">
                        <span class="slider"></span>
                    </label>
                </label>
            </div>
        </div>

        <div class="config-section">
            <h3><i class="fas fa-chart-line"></i> Estadísticas</h3>
            <div class="input-group">
                <label>Seguidores</label>
                <input type="number" id="configFollowers" value="12500" oninput="updateStats()">
            </div>
            <div class="input-group">
                <label>Streams Completados</label>
                <input type="number" id="configStreams" value="342" oninput="updateStats()">
            </div>
            <div class="input-group">
                <label>Horas Streameadas</label>
                <input type="number" id="configHours" value="1250" oninput="updateStats()">
            </div>
        </div>

        <button class="save-btn" onclick="saveConfig()">
            <i class="fas fa-save"></i> Guardar Cambios
        </button>
    </div>

    <!-- Contenido Principal -->
    <main>
        <!-- Hero Section con Logo Principal -->
        <section class="hero-section">
            <div class="main-logo-container">
                <!-- Anillos de luz animados -->
                <div class="logo-ring"></div>
                <div class="logo-ring-inner"></div>
                
                <!-- Partículas decorativas -->
                <div class="particles" id="particles"></div>
                
                <!-- Logo Principal -->
                <img src="/mnt/kimi/upload/Gaming%20YouTube%20Channel%20Logo%20in%20Blue%20Pink%20Typelectric%20Style(1).png" 
                     alt="OG-Tushin Logo Principal" 
                     class="main-logo"
                     id="mainLogo">
            </div>

            <h1 class="hero-title" id="heroTitle">OG-Tushin</h1>
            <p class="hero-subtitle" id="heroDescription">
                Streamer profesional de gaming. ¡Únete a mis streams diarios!
            </p>

            <!-- Botones de acción -->
            <div class="hero-actions">
                <a href="#" class="hero-btn primary" onclick="startStream()">
                    <i class="fas fa-play"></i> Ver Stream
                </a>
                <a href="#" class="hero-btn secondary" onclick="document.getElementById('socialSection').scrollIntoView({behavior: 'smooth'})">
                    <i class="fas fa-share-alt"></i> Seguir
                </a>
            </div>

            <!-- Estadísticas -->
            <div class="stats-bar">
                <div class="stat-item">
                    <div class="stat-number" id="statFollowers">12.5K</div>
                    <div class="stat-label">Seguidores</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="statStreams">342</div>
                    <div class="stat-label">Streams</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="statHours">1.2K</div>
                    <div class="stat-label">Horas</div>
                </div>
            </div>
        </section>

        <!-- Conexiones Sociales -->
        <section class="content-section" id="socialSection">
            <div class="section-header">
                <h2 class="section-title">
                    <i class="fas fa-plug" style="color: var(--neon-blue);"></i>
                    Conectar Cuentas
                </h2>
            </div>
            
            <div class="social-connections">
                <div class="social-card" onclick="connectSocial('facebook')">
                    <div class="social-icon facebook">
                        <i class="fab fa-facebook"></i>
                    </div>
                    <div class="social-name">Facebook</div>
                    <div class="social-status" id="facebookStatus">
                        <i class="fas fa-plus"></i> Conectar
                    </div>
                </div>

                <div class="social-card" onclick="connectSocial('tiktok')">
                    <div class="social-icon tiktok">
                        <i class="fab fa-tiktok"></i>
                    </div>
                    <div class="social-name">TikTok</div>
                    <div class="social-status" id="tiktokStatus">
                        <i class="fas fa-plus"></i> Conectar
                    </div>
                </div>

                <div class="social-card" onclick="connectSocial('kick')">
                    <div class="social-icon kick">
                        <i class="fas fa-broadcast-tower"></i>
                    </div>
                    <div class="social-name">Kick</div>
                    <div class="social-status" id="kickStatus">
                        <i class="fas fa-plus"></i> Conectar
                    </div>
                </div>
            </div>
        </section>

        <!-- Videos/Streams -->
        <section class="content-section">
            <div class="section-header">
                <h2 class="section-title">
                    <i class="fas fa-play-circle" style="color: var(--neon-pink);"></i>
                    Contenido Reciente
                </h2>
                <div class="live-indicator" id="liveIndicator">
                    <div class="live-dot"></div>
                    <span>LIVE</span>
                </div>
            </div>

            <div class="video-grid">
                <div class="video-card">
                    <div class="video-thumbnail">
                        <span class="platform-badge" style="color: #53fc18;">KICK</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title" id="streamTitle1">🔴 EN VIVO: Compitiendo en Rankeds</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 1.2K viendo</span>
                            <span><i class="fas fa-clock"></i> Ahora</span>
                        </div>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-thumbnail" style="background: linear-gradient(135deg, rgba(255,0,80,0.1), rgba(0,242,234,0.1));">
                        <span class="platform-badge" style="color: #ff0050;">TIKTOK</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title">Mejores momentos del torneo</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 45K views</span>
                            <span><i class="fas fa-clock"></i> Hace 2 días</span>
                        </div>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-thumbnail" style="background: linear-gradient(135deg, rgba(24,119,242,0.1), rgba(0,212,255,0.1));">
                        <span class="platform-badge" style="color: #1877f2;">FB</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title">Guía completa para principiantes</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 12K views</span>
                            <span><i class="fas fa-clock"></i> Hace 5 días</span>
                        </div>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-thumbnail" style="background: linear-gradient(135deg, rgba(83,252,24,0.1), rgba(0,212,255,0.1));">
                        <span class="platform-badge" style="color: #53fc18;">KICK</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title">Stream de práctica - Nuevas estrategias</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 8.5K views</span>
                            <span><i class="fas fa-clock"></i> Hace 1 semana</span>
                        </div>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-thumbnail" style="background: linear-gradient(135deg, rgba(255,0,255,0.1), rgba(0,212,255,0.1));">
                        <span class="platform-badge" style="color: #ff00ff;">YT</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title">Reacting a los mejores clips</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 32K views</span>
                            <span><i class="fas fa-clock"></i> Hace 2 semanas</span>
                        </div>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-thumbnail" style="background: linear-gradient(135deg, rgba(0,212,255,0.1), rgba(255,0,80,0.1));">
                        <span class="platform-badge" style="color: #00d4ff;">TWITCH</span>
                        <div class="play-btn">
                            <i class="fas fa-play"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h3 class="video-title">Colaboración especial con el squad</h3>
                        <div class="video-meta">
                            <span><i class="fas fa-eye"></i> 28K views</span>
                            <span><i class="fas fa-clock"></i> Hace 3 semanas</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <script>
        // Estado de conexiones
        const connections = {
            facebook: false,
            tiktok: false,
            kick: false
        };

        // Toggle del panel de configuración
        function toggleConfig() {
            const panel = document.getElementById('configPanel');
            const overlay = document.getElementById('overlay');
            panel.classList.toggle('active');
            overlay.classList.toggle('active');
        }

        // Cerrar panel al hacer clic en overlay
        document.getElementById('overlay').addEventListener('click', toggleConfig);

        // Crear partículas alrededor del logo
        function createParticles() {
            const container = document.getElementById('particles');
            const particleCount = 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Posición aleatoria en círculo
                const angle = (Math.random() * 360) * (Math.PI / 180);
                const radius = 180 + Math.random() * 50;
                const x = Math.cos(angle) * radius;
                const y = Math.sin(angle) * radius;
                
                particle.style.left = `calc(50% + ${x}px)`;
                particle.style.top = `calc(50% + ${y}px)`;
                particle.style.setProperty('--tx', `${x * 0.5}px`);
                particle.style.setProperty('--ty', `${y * 0.5}px`);
                particle.style.animationDelay = `${Math.random() * 6}s`;
                particle.style.animationDuration = `${4 + Math.random() * 4}s`;
                
                container.appendChild(particle);
            }
        }

        // Actualizar contenido en tiempo real
        function updateContent() {
            const name = document.getElementById('configChannelName').value;
            const desc = document.getElementById('configDescription').value;
            
            document.getElementById('headerName').textContent = name || 'OG-Tushin';
            document.getElementById('heroTitle').textContent = name || 'OG-Tushin';
            document.getElementById('heroDescription').textContent = desc;
        }

        // Actualizar colores
        function updateColors() {
            const primary = document.getElementById('primaryColor').value;
            const secondary = document.getElementById('secondaryColor').value;
            
            document.documentElement.style.setProperty('--neon-blue', primary);
            document.documentElement.style.setProperty('--neon-pink', secondary);
        }

        // Actualizar redes sociales
        function updateSocial() {
            // Aquí se actualizarían los usuarios en la UI
            console.log('Actualizando redes sociales...');
        }

        // Actualizar stream
        function updateStream() {
            const title = document.getElementById('configStreamTitle').value;
            document.getElementById('streamTitle1').textContent = title;
        }

        // Toggle LIVE
        function toggleLive() {
            const show = document.getElementById('showLive').checked;
            const indicator = document.getElementById('liveIndicator');
            indicator.style.display = show ? 'flex' : 'none';
        }

        // Actualizar estadísticas
        function updateStats() {
            const followers = document.getElementById('configFollowers').value;
            const streams = document.getElementById('configStreams').value;
            const hours = document.getElementById('configHours').value;
            
            document.getElementById('statFollowers').textContent = formatNumber(followers);
            document.getElementById('statStreams').textContent = streams;
            document.getElementById('statHours').textContent = formatNumber(hours);
        }

        // Formatear números
        function formatNumber(num) {
            if (num >= 1000000) return (num / 1000000).toFixed(1) + 'M';
            if (num >= 1000) return (num / 1000).toFixed(1) + 'K';
            return num;
        }

        // Conectar redes sociales
        function connectSocial(platform) {
            connections[platform] = !connections[platform];
            const statusEl = document.getElementById(platform + 'Status');
            
            if (connections[platform]) {
                statusEl.innerHTML = '<i class="fas fa-check"></i> Conectado';
                statusEl.classList.add('connected');
                
                // Simular autenticación
                setTimeout(() => {
                    alert(`¡Cuenta de ${platform.charAt(0).toUpperCase() + platform.slice(1)} conectada exitosamente!`);
                }, 500);
            } else {
                statusEl.innerHTML = '<i class="fas fa-plus"></i> Conectar';
                statusEl.classList.remove('connected');
            }
        }

        // Iniciar stream
        function startStream() {
            alert('¡Iniciando transmisión en vivo! 🎮🔴');
        }

        // Guardar configuración
        function saveConfig() {
            const config = {
                channelName: document.getElementById('configChannelName').value,
                description: document.getElementById('configDescription').value,
                primaryColor: document.getElementById('primaryColor').value,
                secondaryColor: document.getElementById('secondaryColor').value,
                facebook: document.getElementById('configFacebook').value,
                tiktok: document.getElementById('configTiktok').value,
                kick: document.getElementById('configKick').value,
                streamTitle: document.getElementById('configStreamTitle').value,
                showLive: document.getElementById('showLive').checked,
                followers: document.getElementById('configFollowers').value,
                streams: document.getElementById('configStreams').value,
                hours: document.getElementById('configHours').value
            };
            
            localStorage.setItem('ogTushinConfig', JSON.stringify(config));
            
            // Animación de guardado
            const btn = document.querySelector('.save-btn');
            const originalText = btn.innerHTML;
            btn.innerHTML = '<i class="fas fa-check"></i> ¡Guardado!';
            btn.style.background = 'linear-gradient(45deg, #00ff88, #00d4ff)';
            
            setTimeout(() => {
                btn.innerHTML = originalText;
                btn.style.background = '';
                toggleConfig();
            }, 1500);
        }

        // Cargar configuración guardada
        function loadConfig() {
            const saved = localStorage.getItem('ogTushinConfig');
            if (saved) {
                const config = JSON.parse(saved);
                document.getElementById('configChannelName').value = config.channelName || 'OG-Tushin';
                document.getElementById('configDescription').value = config.description || 'Streamer profesional de gaming. ¡Únete a mis streams diarios!';
                document.getElementById('primaryColor').value = config.primaryColor || '#00d4ff';
                document.getElementById('secondaryColor').value = config.secondaryColor || '#ff00ff';
                document.getElementById('configFacebook').value = config.facebook || '@OGTushin';
                document.getElementById('configTiktok').value = config.tiktok || '@og.tushin';
                document.getElementById('configKick').value = config.kick || 'og-tushin';
                document.getElementById('configStreamTitle').value = config.streamTitle || '🔴 EN VIVO: Compitiendo en Rankeds';
                document.getElementById('showLive').checked = config.showLive !== false;
                document.getElementById('configFollowers').value = config.followers || '12500';
                document.getElementById('configStreams').value = config.streams || '342';
                document.getElementById('configHours').value = config.hours || '1250';
                
                // Aplicar cambios
                updateContent();
                updateColors();
                updateStream();
                toggleLive();
                updateStats();
            }
        }

        // Inicializar
        window.addEventListener('load', () => {
            loadConfig();
            createParticles();
            
            // Animación de entrada
            document.querySelectorAll('.video-card, .social-card').forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(30px)';
                setTimeout(() => {
                    el.style.transition = 'all 0.6s ease';
                    el.style.opacity = '1';
                    el.style.transform = 'translateY(0)';
                }, index * 100);
            });
        });

        // Efecto parallax suave en el logo
        document.addEventListener('mousemove', (e) => {
            const logo = document.getElementById('mainLogo');
            const x = (window.innerWidth / 2 - e.pageX) / 50;
            const y = (window.innerHeight / 2 - e.pageY) / 50;
            
            logo.style.transform = `translate(${x}px, ${y}px) scale(1.02)`;
        });
    </script>
</body>
</html>
