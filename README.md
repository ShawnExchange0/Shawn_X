<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shawn Exchange - Invest & Grow</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            background: white;
            padding: 2rem 1rem;
            border-radius: 15px;
            margin-bottom: 1rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .header h1 {
            color: #2c3e50;
            margin-bottom: 0.5rem;
        }

        .header p {
            color: #7f8c8d;
        }

        .card {
            background: white;
            padding: 1.5rem;
            border-radius: 15px;
            margin-bottom: 1rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .plan {
            border-left: 4px solid #e74c3c;
            padding-left: 1rem;
            margin: 1rem 0;
        }

        .investment {
            font-size: 1.2rem;
            font-weight: bold;
            color: #2c3e50;
        }

        .profit {
            font-size: 1.4rem;
            font-weight: bold;
            color: #27ae60;
        }

        .btn {
            display: block;
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: bold;
            text-align: center;
            text-decoration: none;
            margin: 10px 0;
            cursor: pointer;
        }

        .btn-primary {
            background: #e74c3c;
            color: white;
        }

        .btn-success {
            background: #27ae60;
            color: white;
        }

        .btn-whatsapp {
            background: #25D366;
            color: white;
        }

        .payment-section {
            background: #e8f5e8;
            border: 2px dashed #27ae60;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            margin: 1rem 0;
        }

        .account-details {
            font-size: 1.3rem;
            font-weight: bold;
            background: white;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
            border-left: 4px solid #3498db;
        }

        .instructions {
            background: #f8f9fa;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
        }

        .instructions ol {
            margin-left: 1.5rem;
        }

        .instructions li {
            margin-bottom: 0.5rem;
        }

        .feature {
            display: flex;
            align-items: center;
            margin: 0.5rem 0;
        }

        .feature::before {
            content: "✅";
            margin-right: 0.5rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>Shawn Exchange</h1>
            <p>Smart Investments • Guaranteed Returns</p>
        </div>

        <!-- Features -->
        <div class="card">
            <h3>Why Choose Shawn Exchange?</h3>
            <div class="feature">Proven Investment Strategies</div>
            <div class="feature">Consistent Profitable Returns</div>
            <div class="feature">Secure & Reliable Platform</div>
            <div class="feature">24/7 Customer Support</div>
        </div>

        <!-- Investment Plans -->
        <div class="card">
            <h3>💰 Investment Plans</h3>
            
            <div class="plan">
                <div class="investment">Invest: 10,000 XAF</div>
                <div class="profit">Earn: 50,000 XAF</div>
                <small>400% Return on Investment</small>
            </div>

            <div class="plan">
                <div class="investment">Invest: 20,000 XAF</div>
                <div class="profit">Earn: 100,000 XAF</div>
                <small>400% Return on Investment</small>
            </div>

            <div class="plan">
                <div class="investment">Invest: 30,000 XAF</div>
                <div class="profit">Earn: 150,000 XAF</div>
                <small>400% Return on Investment</small>
            </div>

            <button class="btn btn-success" onclick="showPaymentSection()">
                Start Investing Now
            </button>
        </div>

        <!-- Payment Section -->
        <div id="paymentSection" class="card" style="display: none;">
            <h3>📱 Make Payment</h3>
            
            <div class="payment-section">
                <p>Send payment to this MoMo account:</p>
                <div class="account-details" id="accountDetails">
                    678160575<br>
                    <small>Javis Emeh</small>
                </div>
                <button class="btn btn-primary" onclick="copyAccountNumber()">
                    📋 Copy Account Number
                </button>
            </div>

            <div class="instructions">
                <h4>Payment Instructions:</h4>
                <ol>
                    <li>Open your MoMo app</li>
                    <li>Send money to: <strong>678160575</strong></li>
                    <li>Enter your chosen amount</li>
                    <li>Use your name as reference</li>
                    <li>Take screenshot of confirmation</li>
                    <li>Send screenshot via WhatsApp</li>
                </ol>
            </div>

            <button class="btn btn-whatsapp" onclick="contactAdmin()">
                💬 Contact Admin on WhatsApp
            </button>
        </div>

        <!-- How It Works -->
        <div class="card">
            <h3>🚀 How It Works</h3>
            <div class="feature">1. Register & Choose Plan</div>
            <div class="feature">2. Make MoMo Payment</div>
            <div class="feature">3. Send Payment Proof</div>
            <div class="feature">4. Start Earning Profits</div>
        </div>

        <!-- Contact -->
        <div class="card">
            <h3>📞 Contact Support</h3>
            <p>24/7 customer support available</p>
            <button class="btn btn-whatsapp" onclick="contactAdmin()">
                💬 WhatsApp Support
            </button>
        </div>
    </div>

    <script>
        function showPaymentSection() {
            document.getElementById('paymentSection').style.display = 'block';
            document.getElementById('paymentSection').scrollIntoView({
                behavior: 'smooth'
            });
        }

        function copyAccountNumber() {
            const accountNumber = '678160575';
            
            // Try modern clipboard API first
            if (navigator.clipboard) {
                navigator.clipboard.writeText(accountNumber).then(function() {
                    alert('✅ Account number copied: 678160575');
                }).catch(function() {
                    fallbackCopy(accountNumber);
                });
            } else {
                fallbackCopy(accountNumber);
            }
            
            function fallbackCopy(text) {
                const input = document.createElement('input');
                input.value = text;
                document.body.appendChild(input);
                input.select();
                document.execCommand('copy');
                document.body.removeChild(input);
                alert('✅ Account number copied: 678160575');
            }
        }

        function contactAdmin() {
            const phoneNumber = '678160575';
            const message = 'Hello Shawn Exchange! I want to invest in your plans.';
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }

        // Show payment section if URL has parameter
        if (window.location.hash === '#invest') {
            showPaymentSection();
        }
    </script>
</body>
</html>
