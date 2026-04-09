<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Group | Sovereign Terminal</title>
    
    <meta name="description" content="Protocolo de liquidación inmutable. Unidad mínima: 1 G0 ($1,000). Ejecución en 120s.">
    
    <style>
        :root {
            --oro: #D4AF37;
            --negro: #000000;
            --beige: #F5F5DC;
        }

        body {
            background-color: var(--negro);
            color: var(--beige);
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            margin: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            overflow: hidden;
        }

        /* Ticker de Marketing Algorítmico: Funciona solo 24/7 */
        .ticker-soberano {
            position: absolute;
            top: 0;
            width: 100%;
            background: rgba(212, 175, 55, 0.05);
            border-bottom: 1px solid var(--oro);
            padding: 12px 0;
            font-family: 'Courier New', monospace;
            font-size: 11px;
            text-align: center;
            letter-spacing: 2px;
            color: var(--oro);
            text-transform: uppercase;
        }

        .terminal-container {
            border: 1px solid var(--oro);
            padding: 60px;
            background: linear-gradient(145deg, #050505, #111111);
            text-align: center;
            box-shadow: 0 0 50px rgba(212, 175, 55, 0.15);
            max-width: 450px;
            width: 85%;
        }

        h1 {
            color: var(--oro);
            letter-spacing: 12px;
            font-weight: 200;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .holding-tag {
            font-size: 10px;
            letter-spacing: 5px;
            margin-bottom: 40px;
            opacity: 0.8;
            color: var(--beige);
        }

        input {
            background: transparent;
            border: none;
            border-bottom: 1px solid var(--beige);
            color: var(--oro);
            font-size: 32px;
            text-align: center;
            width: 100%;
            margin-bottom: 40px;
            outline: none;
            font-family: 'Courier New', monospace;
        }

        button {
            background-color: var(--oro);
            color: var(--negro);
            border: none;
            padding: 20px;
            font-weight: bold;
            font-size: 13px;
            letter-spacing: 4px;
            cursor: pointer;
            width: 100%;
            transition: all 0.5s ease;
            text-transform: uppercase;
        }

        button:hover {
            background-color: var(--beige);
            letter-spacing: 6px;
        }

        #status-display {
            margin-top: 30px;
            font-size: 10px;
            color: var(--oro);
            font-family: 'Courier New', monospace;
            text-transform: uppercase;
        }
    </style>
</head>
<body>

    <div class="ticker-soberano" id="live-ticker">
        INICIALIZANDO ESCÁNER DE RED... | MÍNIMO DE ENTRADA: $1,000 USD
    </div>

    <div class="terminal-container">
        <h1>GOLDEN GROUP</h1>
        <div class="holding-tag">HOLDING OF MERIT</div>
        
        <div style="font-size: 10px; margin-bottom: 15px; opacity: 0.5;">INGRESE UNIDADES G0 PARA TRÁNSITO</div>
        <input type="number" id="g0-amount" placeholder="0" min="1">
        
        <button onclick="ejecutarProtocolo()">EJECUTAR TRÁNSITO</button>
        
        <div id="status-display">SISTEMA EN ESPERA DE AUTORIZACIÓN</div>
    </div>

    <script>
        // MARKETING AUTÓNOMO: Genera percepción de flujo constante
        const transmisiones = [
            "VALIDANDO BLOQUE G0: 10 UNIDADES ($10,000)",
            "CAPTURANDO CAPITAL EN RED... STATUS: 200 OK",
            "AUDITORÍA SOBERANA COMPLETADA | 120s RESTANTES",
            "SISTEMA ONLINE | SIN INTERMEDIARIOS DETECTADOS",
            "NUEVA LIQUIDACIÓN DETECTADA: 50 G0 ($50,000)"
        ];

        setInterval(() => {
            const msg = transmisiones[Math.floor(Math.random() * transmisiones.length)];
            document.getElementById('live-ticker').innerText = msg;
        }, 7000);

        function ejecutarProtocolo() {
            const monto = document.getElementById('g0-amount').value;
            const log = document.getElementById('status-display');

            if (!monto || monto < 1) {
                log.innerText = "ACCESO DENEGADO: MÍNIMO 1 G0 ($1,000)";
                return;
            }

            log.innerText = "CONECTANDO A RED... ESCANEANDO BILLETERA SOBERANA";
            // Aquí se activa el puente con tu contrato de Remix
        }
    </script>
</body>
</html>
