<!DOCTYPE html>
<html lang="bg">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Как работи Lev2EUR - Ръководство</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: #f5f7fa;
            color: #1a1a2e;
            line-height: 1.7;
            padding: 20px;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: #fff;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        h1 {
            color: #007a63;
            margin-bottom: 10px;
            font-size: 32px;
            text-align: center;
        }
        .subtitle {
            text-align: center;
            color: #666;
            font-size: 18px;
            margin-bottom: 40px;
        }
        h2 {
            color: #007a63;
            margin-top: 40px;
            margin-bottom: 20px;
            font-size: 22px;
            border-bottom: 2px solid #e0e0e0;
            padding-bottom: 10px;
        }
        h3 {
            color: #1a1a2e;
            margin-top: 25px;
            margin-bottom: 15px;
            font-size: 18px;
        }
        p { margin-bottom: 15px; }
        ul, ol { margin-left: 25px; margin-bottom: 20px; }
        li { margin-bottom: 10px; }
        .highlight-box {
            background: linear-gradient(135deg, rgba(0, 122, 99, 0.1) 0%, rgba(0, 102, 170, 0.1) 100%);
            border-left: 4px solid #007a63;
            padding: 20px;
            border-radius: 0 12px 12px 0;
            margin: 25px 0;
        }
        .rate-box {
            background: #007a63;
            color: #fff;
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            margin: 30px 0;
        }
        .rate-box .rate {
            font-size: 36px;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }
        .rate-box .label {
            font-size: 14px;
            opacity: 0.9;
            margin-top: 5px;
        }
        .example {
            background: #f8f9fb;
            border: 1px solid #e0e0e0;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
        }
        .example-title {
            font-weight: bold;
            color: #007a63;
            margin-bottom: 15px;
            font-size: 16px;
        }
        .calc-step {
            display: flex;
            align-items: center;
            margin: 10px 0;
            padding: 10px 15px;
            background: #fff;
            border-radius: 8px;
            border: 1px solid #e0e0e0;
        }
        .calc-step .icon {
            font-size: 24px;
            margin-right: 15px;
        }
        .calc-step .text {
            flex: 1;
        }
        .calc-step .value {
            font-family: 'Courier New', monospace;
            font-weight: bold;
            color: #007a63;
            font-size: 18px;
        }
        .result-positive { color: #007a63; }
        .result-negative { color: #c62828; }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }
        th {
            background: #f5f7fa;
            font-weight: 600;
            color: #1a1a2e;
        }
        tr:hover { background: #f8f9fb; }
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }
        .feature-card {
            background: #f8f9fb;
            padding: 20px;
            border-radius: 12px;
            border: 1px solid #e0e0e0;
        }
        .feature-card .icon {
            font-size: 32px;
            margin-bottom: 10px;
        }
        .feature-card h4 {
            color: #1a1a2e;
            margin-bottom: 8px;
        }
        .feature-card p {
            color: #666;
            font-size: 14px;
            margin: 0;
        }
        .lang-tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 30px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .lang-tab {
            padding: 10px 20px;
            background: #f0f2f5;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 500;
            transition: all 0.2s;
        }
        .lang-tab:hover { background: #e0e0e0; }
        .lang-tab.active {
            background: #007a63;
            color: #fff;
        }
        .lang-content { display: none; }
        .lang-content.active { display: block; }
        .back-link {
            display: inline-block;
            margin-top: 30px;
            padding: 14px 28px;
            background: #007a63;
            color: #fff;
            text-decoration: none;
            border-radius: 10px;
            font-weight: 500;
        }
        .back-link:hover { background: #005a4a; }
        .cta-box {
            text-align: center;
            padding: 30px;
            background: linear-gradient(135deg, #007a63 0%, #0066aa 100%);
            border-radius: 16px;
            margin-top: 40px;
        }
        .cta-box h3 {
            color: #fff;
            margin-bottom: 15px;
        }
        .cta-box p {
            color: rgba(255,255,255,0.9);
            margin-bottom: 20px;
        }
        .cta-box .back-link {
            background: #fff;
            color: #007a63;
        }
        @media (max-width: 600px) {
            .container { padding: 20px; }
            h1 { font-size: 26px; }
            .rate-box .rate { font-size: 28px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>💱 Lev2EUR</h1>
        <p class="subtitle">Калкулатор за ресто и превалутиране</p>

        <div class="lang-tabs">
            <button class="lang-tab active" onclick="showLang('bg')">🇧🇬 Български</button>
            <button class="lang-tab" onclick="showLang('en')">🇬🇧 English</button>
        </div>

        <!-- BULGARIAN CONTENT -->
        <div id="content-bg" class="lang-content active">
            
            <div class="rate-box">
                <div class="label">Официален фиксиран курс</div>
                <div class="rate">1 EUR = 1.95583 BGN</div>
                <div class="label">Валиден за България при влизане в еврозоната</div>
            </div>

            <h2>🎯 За какво служи?</h2>
            <p>Lev2EUR е безплатен калкулатор, създаден да помогне на <strong>касиери, търговци и работници</strong> при прехода от лева към евро в България.</p>
            
            <div class="highlight-box">
                <strong>Основна функция:</strong> Изчисляване на ресто, когато клиентът плаща със смесени валути (евро и лева едновременно).
            </div>

            <h2>✨ Основни функции</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="icon">🧮</div>
                    <h4>Бързо изчисление</h4>
                    <p>Въведете сумата и веднага вижте рестото в евро и лева</p>
                </div>
                <div class="feature-card">
                    <div class="icon">💱</div>
                    <h4>Смесено плащане</h4>
                    <p>Клиентът плаща част в евро, част в лева - без проблем</p>
                </div>
                <div class="feature-card">
                    <div class="icon">✂️</div>
                    <h4>Раздели рестото</h4>
                    <p>Изчислете колко да върнете в евро и колко в лева</p>
                </div>
                <div class="feature-card">
                    <div class="icon">🌍</div>
                    <h4>4 езика</h4>
                    <p>Български, английски, украински и руски</p>
                </div>
            </div>

            <h2>📖 Как да използвам калкулатора?</h2>

            <h3>Стъпка 1: Сума за плащане</h3>
            <p>Въведете общата сума, която клиентът трябва да плати <strong>в евро (EUR)</strong>.</p>
            <p>Калкулаторът автоматично показва еквивалента в лева.</p>

            <h3>Стъпка 2: Клиентът плаща</h3>
            <p>Въведете колко пари ви дава клиентът:</p>
            <ul>
                <li><strong>BGN / лв.</strong> - сумата в български лева</li>
                <li><strong>EUR</strong> - сумата в евро</li>
            </ul>
            <p>Можете да попълните и двете полета, ако клиентът плаща със смесени валути.</p>

            <h3>Стъпка 3: Ресто / Дължимо</h3>
            <p>Калкулаторът показва:</p>
            <ul>
                <li><span class="result-positive">Зелено число</span> = Ресто за връщане</li>
                <li><span class="result-negative">Червено число</span> = Клиентът още дължи</li>
            </ul>

            <h3>Стъпка 4: Раздели рестото (по избор)</h3>
            <p>Ако искате да върнете част от рестото в евро:</p>
            <ol>
                <li>Въведете колко евро ще дадете в полето "Давам в EUR"</li>
                <li>Калкулаторът показва остатъка, който трябва да дадете в лева</li>
            </ol>

            <h2>📝 Примери</h2>

            <div class="example">
                <div class="example-title">Пример 1: Просто плащане</div>
                <div class="calc-step">
                    <span class="icon">🧾</span>
                    <span class="text">Сметка:</span>
                    <span class="value">10.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💳</span>
                    <span class="text">Клиентът дава:</span>
                    <span class="value">20.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Ресто:</span>
                    <span class="value result-positive">10.00 EUR (= 19.56 лв.)</span>
                </div>
            </div>

            <div class="example">
                <div class="example-title">Пример 2: Смесено плащане</div>
                <div class="calc-step">
                    <span class="icon">🧾</span>
                    <span class="text">Сметка:</span>
                    <span class="value">15.00 EUR (= 29.34 лв.)</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💳</span>
                    <span class="text">Клиентът дава:</span>
                    <span class="value">10.00 EUR + 20.00 лв.</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Ресто:</span>
                    <span class="value result-positive">5.23 EUR (= 10.22 лв.)</span>
                </div>
            </div>

            <div class="example">
                <div class="example-title">Пример 3: Раздели рестото</div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Общо ресто:</span>
                    <span class="value">5.23 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">✂️</span>
                    <span class="text">Давам в евро:</span>
                    <span class="value">5.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">🪙</span>
                    <span class="text">Остатък в лева:</span>
                    <span class="value">0.45 лв.</span>
                </div>
            </div>

            <h2>❓ Често задавани въпроси</h2>

            <h3>Защо курсът е точно 1.95583?</h3>
            <p>Това е официалният фиксиран курс, определен от Европейската централна банка за България при влизане в еврозоната. Той няма да се променя.</p>

            <h3>Мога ли да използвам калкулатора офлайн?</h3>
            <p>Да! Веднъж заредена, страницата работи и без интернет. Препоръчваме да запазите приложението за Android за най-добро офлайн изживяване.</p>

            <h3>Калкулаторът безплатен ли е?</h3>
            <p>Да, напълно безплатен. Поддържа се от реклами.</p>

            <h3>Данните ми защитени ли са?</h3>
            <p>Да. Никакви данни не се записват или изпращат. Всички изчисления се извършват локално на вашето устройство.</p>

        </div>

        <!-- ENGLISH CONTENT -->
        <div id="content-en" class="lang-content">
            
            <div class="rate-box">
                <div class="label">Official Fixed Exchange Rate</div>
                <div class="rate">1 EUR = 1.95583 BGN</div>
                <div class="label">Valid for Bulgaria's Eurozone entry</div>
            </div>

            <h2>🎯 What is it for?</h2>
            <p>Lev2EUR is a free calculator designed to help <strong>cashiers, merchants, and workers</strong> during Bulgaria's transition from lev to euro.</p>
            
            <div class="highlight-box">
                <strong>Main function:</strong> Calculate change when customers pay with mixed currencies (euro and lev simultaneously).
            </div>

            <h2>✨ Key Features</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="icon">🧮</div>
                    <h4>Quick Calculation</h4>
                    <p>Enter the amount and instantly see the change in euro and lev</p>
                </div>
                <div class="feature-card">
                    <div class="icon">💱</div>
                    <h4>Mixed Payment</h4>
                    <p>Customer pays part in euro, part in lev - no problem</p>
                </div>
                <div class="feature-card">
                    <div class="icon">✂️</div>
                    <h4>Split Change</h4>
                    <p>Calculate how much to return in euro and how much in lev</p>
                </div>
                <div class="feature-card">
                    <div class="icon">🌍</div>
                    <h4>4 Languages</h4>
                    <p>Bulgarian, English, Ukrainian, and Russian</p>
                </div>
            </div>

            <h2>📖 How to use the calculator?</h2>

            <h3>Step 1: Total to Pay</h3>
            <p>Enter the total amount the customer needs to pay <strong>in euro (EUR)</strong>.</p>
            <p>The calculator automatically shows the equivalent in lev.</p>

            <h3>Step 2: Customer Pays</h3>
            <p>Enter how much money the customer gives you:</p>
            <ul>
                <li><strong>BGN / лв.</strong> - amount in Bulgarian lev</li>
                <li><strong>EUR</strong> - amount in euro</li>
            </ul>
            <p>You can fill both fields if the customer pays with mixed currencies.</p>

            <h3>Step 3: Change / Due</h3>
            <p>The calculator shows:</p>
            <ul>
                <li><span class="result-positive">Green number</span> = Change to return</li>
                <li><span class="result-negative">Red number</span> = Customer still owes</li>
            </ul>

            <h3>Step 4: Split Change (optional)</h3>
            <p>If you want to return part of the change in euro:</p>
            <ol>
                <li>Enter how many euros you'll give in the "Give in EUR" field</li>
                <li>The calculator shows the remainder to give in lev</li>
            </ol>

            <h2>📝 Examples</h2>

            <div class="example">
                <div class="example-title">Example 1: Simple Payment</div>
                <div class="calc-step">
                    <span class="icon">🧾</span>
                    <span class="text">Bill:</span>
                    <span class="value">10.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💳</span>
                    <span class="text">Customer gives:</span>
                    <span class="value">20.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Change:</span>
                    <span class="value result-positive">10.00 EUR (= 19.56 лв.)</span>
                </div>
            </div>

            <div class="example">
                <div class="example-title">Example 2: Mixed Payment</div>
                <div class="calc-step">
                    <span class="icon">🧾</span>
                    <span class="text">Bill:</span>
                    <span class="value">15.00 EUR (= 29.34 лв.)</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💳</span>
                    <span class="text">Customer gives:</span>
                    <span class="value">10.00 EUR + 20.00 лв.</span>
                </div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Change:</span>
                    <span class="value result-positive">5.23 EUR (= 10.22 лв.)</span>
                </div>
            </div>

            <div class="example">
                <div class="example-title">Example 3: Split Change</div>
                <div class="calc-step">
                    <span class="icon">💰</span>
                    <span class="text">Total change:</span>
                    <span class="value">5.23 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">✂️</span>
                    <span class="text">Give in euro:</span>
                    <span class="value">5.00 EUR</span>
                </div>
                <div class="calc-step">
                    <span class="icon">🪙</span>
                    <span class="text">Remaining in lev:</span>
                    <span class="value">0.45 лв.</span>
                </div>
            </div>

            <h2>❓ Frequently Asked Questions</h2>

            <h3>Why is the rate exactly 1.95583?</h3>
            <p>This is the official fixed rate set by the European Central Bank for Bulgaria's eurozone entry. It will not change.</p>

            <h3>Can I use the calculator offline?</h3>
            <p>Yes! Once loaded, the page works without internet. We recommend saving the Android app for the best offline experience.</p>

            <h3>Is the calculator free?</h3>
            <p>Yes, completely free. It's supported by ads.</p>

            <h3>Is my data protected?</h3>
            <p>Yes. No data is recorded or sent. All calculations are performed locally on your device.</p>

        </div>

        <div class="cta-box">
            <h3>Готови сте! / You're ready!</h3>
            <p>Започнете да използвате калкулатора сега</p>
            <a href="https://lev2eur.xyz" class="back-link">← Към калкулатора / Go to Calculator</a>
        </div>

    </div>

    <script>
        function showLang(lang) {
            // Hide all content
            document.querySelectorAll('.lang-content').forEach(el => {
                el.classList.remove('active');
            });
            // Remove active from all tabs
            document.querySelectorAll('.lang-tab').forEach(el => {
                el.classList.remove('active');
            });
            // Show selected content
            document.getElementById('content-' + lang).classList.add('active');
            // Activate selected tab
            event.target.classList.add('active');
        }
    </script>
</body>
</html>
