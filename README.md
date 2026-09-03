# Ventana-de-Prueba
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Ganancias</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0b0f19;
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .calculator-container {
            background-color: #111827;
            border: 1px solid #1f2937;
            border-radius: 16px;
            width: 100%;
            max-width: 550px;
            padding: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }

        .badge {
            background-color: #2563eb;
            color: white;
            font-size: 11px;
            font-weight: bold;
            text-transform: uppercase;
            padding: 6px 14px;
            border-radius: 20px;
            display: inline-block;
            margin-bottom: 15px;
            letter-spacing: 0.5px;
        }

        .header-center {
            text-align: center;
            margin-bottom: 25px;
        }

        .header-center h1 {
            font-size: 22px;
            font-weight: 700;
            margin-bottom: 5px;
        }

        .header-center p {
            font-size: 13px;
            color: #9ca3af;
        }

        .total-box {
            background: linear-gradient(135deg, #2563eb, #1d4ed8);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            margin-bottom: 25px;
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }

        .total-box span {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 600;
            color: #dbeafe;
        }

        .total-box h2 {
            font-size: 36px;
            font-weight: 800;
            margin-top: 5px;
        }

        .item-card {
            background-color: #1f2937;
            border-radius: 10px;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 12px;
        }

        .item-info h3 {
            font-size: 14px;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: 4px;
        }

        .item-info p {
            font-size: 12px;
            color: #9ca3af;
        }

        .item-controls {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .controls-group {
            display: flex;
            align-items: center;
            background-color: #111827;
            border-radius: 8px;
            padding: 4px;
            border: 1px solid #374151;
        }

        .btn-ctrl {
            background-color: #374151;
            color: white;
            border: none;
            width: 28px;
            height: 28px;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: background 0.2s;
        }

        .btn-ctrl:hover {
            background-color: #4b5563;
        }

        .quantity {
            width: 30px;
            text-align: center;
            font-size: 14px;
            font-weight: 600;
        }

        .item-total {
            font-size: 14px;
            font-weight: 700;
            color: #ffffff;
            min-width: 60px;
            text-align: right;
        }

        .footer-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #1f2937;
            font-size: 13px;
            color: #9ca3af;
        }

        .footer-row span b {
            color: #ffffff;
        }

        .btn-reset {
            background-color: transparent;
            color: #ef4444;
            border: 1px solid #ef4444;
            padding: 6px 14px;
            border-radius: 6px;
            font-size: 12px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }

        .btn-reset:hover {
            background-color: #ef4444;
            color: white;
        }
    </style>
</head>
<body>

    <div class="calculator-container">
        <div class="header-center">
            <div class="badge">Ventana de Prueba</div>
            <h1>Calculadora de Ganancias</h1>
            <p>Toca los botones para sumar o restar tus ventas</p>
        </div>

        <div class="total-box">
            <span>Tu ganancia total estimada</span>
            <h2 id="totalGain">$53.00</h2>
        </div>

        <!-- Producto 1 -->
        <div class="item-card" data-commission="2" data-price="10">
            <div class="item-info">
                <h3>Panaxtreaming - Pantalla</h3>
                <p>Cliente: $4.00 | Comisión: <span style="color: #60a5fa;">$2.00</span></p>
            </div>
            <div class="item-controls">
                <div class="controls-group">
                    <button class="btn-ctrl btn-minus">-</button>
                    <span class="quantity">5</span>
                    <button class="btn-ctrl btn-plus">+</button>
                </div>
                <div class="item-total">$10.00</div>
            </div>
        </div>

        <!-- Producto 2 -->
        <div class="item-card" data-commission="3" data-price="15">
            <div class="item-info">
                <h3>Panaxtreaming - Cuenta Completa</h3>
                <p>Cliente: $8.00 | Comisión: <span style="color: #60a5fa;">$3.00</span></p>
            </div>
            <div class="item-controls">
                <div class="controls-group">
                    <button class="btn-ctrl btn-minus">-</button>
                    <span class="quantity">5</span>
                    <button class="btn-ctrl btn-plus">+</button>
                </div>
                <div class="item-total">$15.00</div>
            </div>
        </div>

        <!-- Producto 3 -->
        <div class="item-card" data-commission="2" data-price="10">
            <div class="item-info">
                <h3>Stella TV - Pantalla / Acceso</h3>
                <p>Cliente: $6.00 | Comisión: <span style="color: #60a5fa;">$2.00</span></p>
            </div>
            <div class="item-controls">
                <div class="controls-group">
                    <button class="btn-ctrl btn-minus">-</button>
                    <span class="quantity">5</span>
                    <button class="btn-ctrl btn-plus">+</button>
                </div>
                <div class="item-total">$10.00</div>
            </div>
        </div>

        <!-- Producto 4 -->
        <div class="item-card" data-commission="3" data-price="18">
            <div class="item-info">
                <h3>Stella TV - Cuenta Completa</h3>
                <p>Cliente: $9.00 | Comisión: <span style="color: #60a5fa;">$3.00</span></p>
            </div>
            <div class="item-controls">
                <div class="controls-group">
                    <button class="btn-ctrl btn-minus">-</button>
                    <span class="quantity">6</span>
                    <button class="btn-ctrl btn-plus">+</button>
                </div>
                <div class="item-total">$18.00</div>
            </div>
        </div>

        <div class="footer-row">
            <span>Total de ventas: <b id="totalUnits">21</b> unidades</span>
            <button class="btn-reset" id="btnReset">Reiniciar</button>
        </div>
    </div>

    <script>
        const items = document.querySelectorAll('.item-card');
        const totalGainElement = document.getElementById('totalGain');
        const totalUnitsElement = document.getElementById('totalUnits');
        const btnReset = document.getElementById('btnReset');

        function updateCalculator() {
            let totalGain = 0;
            let totalUnits = 0;

            items.forEach(item => {
                const commission = parseFloat(item.getAttribute('data-commission'));
                const quantityElement = item.querySelector('.quantity');
                const itemTotalElement = item.querySelector('.item-total');
                
                let qty = parseInt(quantityElement.textContent);
                
                let subtotal = qty * commission;
                itemTotalElement.textContent = `$${subtotal.toFixed(2)}`;

                totalGain += subtotal;
                totalUnits += qty;
            });

            totalGainElement.textContent = `$${totalGain.toFixed(2)}`;
            totalUnitsElement.textContent = totalUnits;
        }

        items.item(0).querySelectorAll('.quantity')[0] // solo referencia
        items.forEach(item => {
            const btnPlus = item.querySelector('.btn-plus');
            const btnMinus = item.querySelector('.btn-minus');
            const quantityElement = item.querySelector('.quantity');

            btnPlus.addEventListener('click', () => {
                let qty = parseInt(quantityElement.textContent);
                quantityElement.textContent = qty + 1;
                updateCalculator();
            });

            btnMinus.addEventListener('click', () => {
                let qty = parseInt(quantityElement.textContent);
                if (qty > 0) {
                    quantityElement.textContent = qty - 1;
                    updateCalculator();
                }
            });
        });

        btnReset.addEventListener('click', () => {
            items.forEach(item => {
                item.querySelector('.quantity').textContent = '0';
            });
            updateCalculator();
        });

        // Inicializar con los valores por defecto de la imagen (5, 5, 5, 6)
        updateCalculator();
    </script>
</body>
</html>
