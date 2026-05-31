<!DOCTYPE html>
<html lang="ru">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Прайс-лист: Покос травы</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Unbounded:wght@400;700;900&family=Raleway:wght@300;400;500&display=swap');

  :root {
    --green-dark: #1a3a1a;
    --green-mid: #2d6a2d;
    --green-light: #4caf50;
    --green-pale: #a8d5a2;
    --yellow: #f5e642;
    --red: #e05252;
    --cream: #f7f4ec;
    --white: #ffffff;
    --shadow: rgba(10, 40, 10, 0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Raleway', sans-serif;
    background: var(--cream);
    color: var(--green-dark);
    min-height: 100vh;
    padding: 32px 16px 48px;
    position: relative;
    overflow-x: hidden;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 10% 20%, rgba(76,175,80,0.10) 0%, transparent 55%),
      radial-gradient(ellipse at 90% 80%, rgba(45,106,45,0.10) 0%, transparent 55%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 760px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  .header {
    text-align: center;
    margin-bottom: 40px;
    animation: fadeDown 0.7s ease both;
  }
  .header-emoji { font-size: 48px; display: block; margin-bottom: 10px; filter: drop-shadow(0 4px 12px rgba(76,175,80,0.3)); }
  .header h1 { font-family: 'Unbounded', sans-serif; font-size: clamp(22px, 5vw, 36px); font-weight: 900; color: var(--green-dark); line-height: 1.1; letter-spacing: -0.5px; text-transform: uppercase; }
  .header h1 span { color: var(--green-mid); }
  .header p { font-size: 14px; color: #5a7a5a; margin-top: 10px; font-weight: 400; }

  .section-title {
    font-family: 'Unbounded', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--green-mid);
    margin-bottom: 14px;
    padding-left: 4px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-title::after { content: ''; flex: 1; height: 1px; background: linear-gradient(to right, var(--green-pale), transparent); }

  .price-block {
    background: var(--white);
    border-radius: 18px;
    border: 1.5px solid #dcefd8;
    box-shadow: 0 6px 32px var(--shadow);
    overflow: hidden;
    margin-bottom: 26px;
    animation: fadeUp 0.6s ease both;
  }

  table { width: 100%; border-collapse: collapse; }
  thead tr { background: var(--green-dark); }
  thead th { font-family: 'Unbounded', sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--green-pale); padding: 13px 18px; text-align: left; }
  thead th:last-child { text-align: right; }
  tbody tr { border-bottom: 1px solid #edf5eb; transition: background 0.18s; }
  tbody tr:last-child { border-bottom: none; }
  tbody tr:hover { background: #f0faf0; }
  tbody td { padding: 13px 18px; font-size: 14px; color: var(--green-dark); font-weight: 400; }
  .td-name { font-weight: 500; }
  .td-price { font-family: 'Unbounded', sans-serif; font-size: 15px; font-weight: 700; color: var(--green-mid); white-space: nowrap; }
  .td-price .unit { font-size: 10px; font-weight: 400; color: #8aaa88; margin-left: 2px; }

  .mult-block {
    background: var(--white);
    border-radius: 18px;
    border: 1.5px solid #dcefd8;
    box-shadow: 0 6px 32px var(--shadow);
    padding: 22px 22px 18px;
    margin-bottom: 26px;
    animation: fadeUp 0.7s ease both;
  }
  .mult-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 4px; }
  .mult-card { border-radius: 12px; padding: 14px 16px; border: 1.5px solid transparent; }
  .mult-card.green { background: #f0faf0; border-color: #b2dfb2; }
  .mult-card.yellow { background: #fffde7; border-color: #ffe58a; }
  .mult-card.red { background: #fdecea; border-color: #f5c0bc; }
  .mult-label { font-size: 12px; font-weight: 500; color: #5a7a5a; margin-bottom: 5px; }
  .mult-value { font-family: 'Unbounded', sans-serif; font-size: 18px; font-weight: 900; line-height: 1; }
  .mult-card.green .mult-value { color: var(--green-mid); }
  .mult-card.yellow .mult-value { color: #a07800; }
  .mult-card.red .mult-value { color: #c62828; }
  .mult-sub { font-size: 11px; color: #8a9a8a; margin-top: 3px; font-weight: 400; }

  .collect-banner {
    background: linear-gradient(135deg, #1a3a1a 0%, #2d6a2d 100%);
    border-radius: 16px 16px 0 0;
    padding: 20px 22px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 14px;
  }
  .collect-table-wrap { padding: 14px 22px; background: #f9fdf9; border-top: 1px solid #dcefd8; }
  .collect-th { font-family: 'Unbounded', sans-serif; font-size: 9px; letter-spacing: 2px; color: #5a7a5a; text-transform: uppercase; padding: 6px 0; font-weight: 700; }

  .calc-block {
    background: var(--green-dark);
    border-radius: 18px;
    padding: 24px 24px 20px;
    color: var(--white);
    margin-bottom: 26px;
    animation: fadeUp 0.8s ease both;
  }
  .calc-block .section-title { color: var(--green-pale); margin-bottom: 16px; }
  .calc-block .section-title::after { background: linear-gradient(to right, rgba(168,213,162,0.3), transparent); }
  .calc-example { background: rgba(255,255,255,0.07); border-radius: 10px; padding: 16px; margin-bottom: 10px; }
  .calc-example:last-child { margin-bottom: 0; }
  .calc-title { font-family: 'Unbounded', sans-serif; font-size: 11px; font-weight: 700; color: var(--green-pale); margin-bottom: 10px; letter-spacing: 0.5px; }
  .calc-row { display: flex; justify-content: space-between; font-size: 13px; color: rgba(255,255,255,0.75); margin-bottom: 5px; align-items: center; }
  .calc-row span:last-child { font-weight: 600; color: #fff; }
  .calc-total { border-top: 1px solid rgba(255,255,255,0.15); margin-top: 8px; padding-top: 8px; display: flex; justify-content: space-between; align-items: center; }
  .calc-total-label { font-family: 'Unbounded', sans-serif; font-size: 11px; color: var(--green-pale); letter-spacing: 1px; text-transform: uppercase; }
  .calc-total-price { font-family: 'Unbounded', sans-serif; font-size: 22px; font-weight: 900; color: var(--yellow); }

  .notes-block { background: #fffde7; border: 1.5px solid #ffe58a; border-radius: 14px; padding: 18px 20px; animation: fadeUp 0.9s ease both; margin-bottom: 26px; }
  .notes-block ul { list-style: none; margin-top: 8px; }
  .notes-block ul li { font-size: 13px; color: #5a5020; padding: 5px 0 5px 18px; position: relative; border-bottom: 1px solid rgba(255,220,0,0.2); }
  .notes-block ul li:last-child { border-bottom: none; }
  .notes-block ul li::before { content: '→'; position: absolute; left: 0; color: #c0900a; font-weight: 700; }

  .footer { text-align: center; margin-top: 32px; font-size: 12px; color: #8aaa88; animation: fadeUp 1s ease both; }

  @keyframes fadeDown { from { opacity: 0; transform: translateY(-20px); } to { opacity: 1; transform: translateY(0); } }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

  @media (max-width: 500px) {
    .mult-grid { grid-template-columns: 1fr; }
    thead th, tbody td { padding: 11px 12px; }
    .collect-banner { flex-direction: column; align-items: flex-start; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HEADER -->
  <div class="header">
    <span class="header-emoji">🌿</span>
    <h1>Покос <span>травы</span><br>на участке</h1>
    <p>Прайс-лист · Сезон 2025</p>
  </div>

  <!-- BASE PRICES -->
  <div class="section-title">Базовые цены по площади</div>
  <div class="price-block">
    <table>
      <thead>
        <tr>
          <th>Площадь</th>
          <th>Обычная цена</th>
          <th style="text-align:right;">По-соседски 🤝</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="td-name">6 соток<br><span style="font-size:11px;color:#8aaa88;font-weight:400;">~600 м²</span></td>
          <td class="td-price">
            <span style="text-decoration:line-through; color:#c0392b; font-size:15px; opacity:0.75;">6 000 ₽</span>
          </td>
          <td style="text-align:right;">
            <span style="font-family:'Unbounded',sans-serif; font-size:18px; font-weight:900; color:#2d6a2d;">5 000 <span style="font-size:11px;font-weight:400;color:#8aaa88;">₽</span></span><br>
            <span style="font-size:10px; color:#4caf50; font-weight:600;">— 1 000 ₽</span>
          </td>
        </tr>
        <tr>
          <td class="td-name">12 соток<br><span style="font-size:11px;color:#8aaa88;font-weight:400;">~1 200 м²</span></td>
          <td class="td-price">
            <span style="text-decoration:line-through; color:#c0392b; font-size:15px; opacity:0.75;">12 000 ₽</span>
          </td>
          <td style="text-align:right;">
            <span style="font-family:'Unbounded',sans-serif; font-size:18px; font-weight:900; color:#2d6a2d;">10 000 <span style="font-size:11px;font-weight:400;color:#8aaa88;">₽</span></span><br>
            <span style="font-size:10px; color:#4caf50; font-weight:600;">— 2 000 ₽</span>
          </td>
        </tr>
        <tr>
          <td class="td-name">15 соток<br><span style="font-size:11px;color:#8aaa88;font-weight:400;">~1 500 м²</span></td>
          <td class="td-price">
            <span style="text-decoration:line-through; color:#c0392b; font-size:15px; opacity:0.75;">15 000 ₽</span>
          </td>
          <td style="text-align:right;">
            <span style="font-family:'Unbounded',sans-serif; font-size:18px; font-weight:900; color:#2d6a2d;">12 500 <span style="font-size:11px;font-weight:400;color:#8aaa88;">₽</span></span><br>
            <span style="font-size:10px; color:#4caf50; font-weight:600;">— 2 500 ₽</span>
          </td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- GRASS COLLECTION -->
  <div class="section-title">Сбор и вывоз скошенной травы</div>
  <div class="price-block">
    <div class="collect-banner">
      <div>
        <div style="font-family:'Unbounded',sans-serif; font-size:11px; letter-spacing:2px; color:#a8d5a2; text-transform:uppercase; margin-bottom:6px;">🌾 Опция — сбор травы</div>
        <div style="font-size:13px; color:rgba(255,255,255,0.78); max-width:340px; line-height:1.6;">
          Сбор, упаковка и вывоз скошенной травы с участка рассчитывается отдельно сверх стоимости покоса
        </div>
      </div>
      <div style="text-align:right; flex-shrink:0;">
        <div style="font-family:'Unbounded',sans-serif; font-size:36px; font-weight:900; color:#f5e642; line-height:1;">+100%</div>
        <div style="font-size:11px; color:#a8d5a2; margin-top:4px;">от стоимости покоса</div>
      </div>
    </div>
    <div class="collect-table-wrap">
      <table>
        <thead>
          <tr style="background: #f0faf0;">
            <th class="collect-th" style="text-align:left;">Площадь</th>
            <th class="collect-th" style="text-align:right;">Только покос</th>
            <th class="collect-th" style="text-align:right;">+ Сбор травы</th>
            <th class="collect-th" style="text-align:right; color:#1a3a1a;">Итого</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td style="padding:10px 0; font-size:13px; font-weight:500;">6 соток</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#2d6a2d; font-weight:600;">5 000 ₽</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#a07800; font-weight:600;">+ 5 000 ₽</td>
            <td style="padding:10px 0; text-align:right; font-family:'Unbounded',sans-serif; font-size:14px; font-weight:900; color:#1a3a1a;">10 000 ₽</td>
          </tr>
          <tr>
            <td style="padding:10px 0; font-size:13px; font-weight:500;">12 соток</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#2d6a2d; font-weight:600;">10 000 ₽</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#a07800; font-weight:600;">+ 10 000 ₽</td>
            <td style="padding:10px 0; text-align:right; font-family:'Unbounded',sans-serif; font-size:14px; font-weight:900; color:#1a3a1a;">20 000 ₽</td>
          </tr>
          <tr>
            <td style="padding:10px 0; font-size:13px; font-weight:500;">15 соток</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#2d6a2d; font-weight:600;">12 500 ₽</td>
            <td style="padding:10px 0; text-align:right; font-size:13px; color:#a07800; font-weight:600;">+ 12 500 ₽</td>
            <td style="padding:10px 0; text-align:right; font-family:'Unbounded',sans-serif; font-size:14px; font-weight:900; color:#1a3a1a;">25 000 ₽</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- MODIFIERS -->
  <div class="section-title">Коэффициенты и надбавки</div>
  <div class="mult-block">
    <div class="mult-grid">
      <div class="mult-card green">
        <div class="mult-label">✅ Ровный участок</div>
        <div class="mult-value">× 1.0</div>
        <div class="mult-sub">Базовая цена без надбавок</div>
      </div>
      <div class="mult-card yellow">
        <div class="mult-label">⛰️ Неровный участок</div>
        <div class="mult-value">× 1.3</div>
        <div class="mult-sub">+30% к базовой стоимости</div>
      </div>
      <div class="mult-card green">
        <div class="mult-label">✅ Без борщевика</div>
        <div class="mult-value">× 1.0</div>
        <div class="mult-sub">Стандартная стоимость</div>
      </div>
      <div class="mult-card red">
        <div class="mult-label">☣️ Есть борщевик</div>
        <div class="mult-value">× 1.5</div>
        <div class="mult-sub">+50% · спецзащита и СИЗ</div>
      </div>
      <div class="mult-card green">
        <div class="mult-label">✅ Уже косили ранее</div>
        <div class="mult-value">× 1.0</div>
        <div class="mult-sub">Обычная высота травы</div>
      </div>
      <div class="mult-card yellow">
        <div class="mult-label">🌾 Никогда не косили</div>
        <div class="mult-value">× 1.4</div>
        <div class="mult-sub">+40% · запущенный участок</div>
      </div>
    </div>
  </div>

  <!-- EXAMPLES -->
  <div class="section-title">Примеры расчёта</div>
  <div class="calc-block">
    <div class="section-title" style="margin-bottom:16px;">Примеры итоговой стоимости</div>

    <div class="calc-example">
      <div class="calc-title">📍 6 соток · ровный · без борщевика · ранее косили</div>
      <div class="calc-row"><span>Базовая цена (6 соток)</span><span>5 000 ₽</span></div>
      <div class="calc-row"><span>Ровный · без борщевика · ранее косили</span><span>× 1.0</span></div>
      <div class="calc-total">
        <span class="calc-total-label">Итого</span>
        <span class="calc-total-price">5 000 ₽</span>
      </div>
    </div>

    <div class="calc-example">
      <div class="calc-title">📍 12 соток · неровный · без борщевика · никогда не косили</div>
      <div class="calc-row"><span>Базовая цена (12 соток)</span><span>10 000 ₽</span></div>
      <div class="calc-row"><span>Неровный участок</span><span>× 1.3</span></div>
      <div class="calc-row"><span>Никогда не косили</span><span>× 1.4</span></div>
      <div class="calc-total">
        <span class="calc-total-label">Итого</span>
        <span class="calc-total-price">18 200 ₽</span>
      </div>
    </div>

    <div class="calc-example">
      <div class="calc-title">📍 15 соток · неровный · борщевик · никогда не косили + сбор травы</div>
      <div class="calc-row"><span>Базовая цена (15 соток)</span><span>12 500 ₽</span></div>
      <div class="calc-row"><span>Неровный участок</span><span>× 1.3</span></div>
      <div class="calc-row"><span>Есть борщевик</span><span>× 1.5</span></div>
      <div class="calc-row"><span>Никогда не косили</span><span>× 1.4</span></div>
      <div class="calc-row"><span>Сбор и вывоз травы</span><span>× 2.0</span></div>
      <div class="calc-total">
        <span class="calc-total-label">Итого</span>
        <span class="calc-total-price">68 250 ₽</span>
      </div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="section-title">Условия и примечания</div>
  <div class="notes-block">
    <ul>
      <li>Минимальная стоимость выезда — 5 000 ₽</li>
      <li>Сбор и вывоз травы — отдельная услуга, +100% от стоимости покоса</li>
      <li>При наличии борщевика обязательно сообщите заранее — работа в СИЗ</li>
      <li>Запущенный участок (никогда не косился) требует осмотра или фото</li>
      <li>Выезд за пределы 50 км от города оплачивается отдельно</li>
      <li>Возможна скидка 10% при регулярном обслуживании (раз в 2–3 недели)</li>
    </ul>
  </div>

  <div class="footer">
    Для записи и расчёта стоимости — обращайтесь по контактам ниже
  </div>

</div>
</body>
</html>
