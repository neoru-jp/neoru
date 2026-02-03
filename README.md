<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>住宅トラブル記録作成サービス</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=Inter:wght@400;600;700&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #f8f9fa;
      --card: #ffffff;
      --card-border: #e2e4e8;
      --text-primary: #1a1c24;
      --text-secondary: #6b6e76;
      --accent: #4f8cff;
      --accent-hover: #3a7aee;
      --green: #16a34a;
      --radius: 12px;
      --shadow: 0 2px 8px rgba(0,0,0,0.06);
    }

    * { margin:0; padding:0; box-sizing:border-box; }

    body {
      font-family: 'Noto Sans JP','Inter',sans-serif;
      background: var(--bg);
      color: var(--text-primary);
      min-height: 100vh;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    .wrapper { max-width:560px; margin:0 auto; padding:56px 24px 72px; }

    /* HEADER */
    .header { text-align:center; margin-bottom:40px; }
    .header .badge {
      display:inline-block;
      background: rgba(79,140,255,0.08);
      border: 1px solid rgba(79,140,255,0.2);
      color: var(--accent);
      font-size:13px; font-weight:600; white-space:nowrap;
      
      padding:5px 14px; border-radius:20px;
      margin-bottom:16px;
    }
    .header .badge .en {
      font-size:10px; color:rgba(79,140,255,0.7);
      display:block; margin-top:3px; white-space:nowrap;
    }
    .header h1 {
      font-family:'Noto Sans JP',sans-serif;
      font-size:clamp(26px,5.5vw,34px);
      font-weight:700; color: var(--text-primary);
      line-height:1.25; margin-bottom:12px;
    }
    .header p { font-size:16px; color:var(--text-secondary); max-width:400px; margin:0 auto; }

    /* CARD */
    .card {
      background: var(--card);
      border: 1px solid var(--card-border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding:24px; margin-bottom:14px;
    }
    .card-title {
      font-size:13px; font-weight:700;
      color: var(--text-primary);
      margin-bottom:14px;
    }

    /* CHECKLIST */
    .checklist { list-style:none; }
    .checklist li {
      display:flex; align-items:flex-start; gap:10px;
      padding:9px 0;
      border-bottom:1px solid var(--card-border);
      font-size:15px; color:var(--text-primary);
    }
    .checklist li:last-child { border-bottom:none; }
    .checklist .icon {
      flex-shrink:0; width:20px; height:20px;
      border-radius:50%;
      background:rgba(22,163,74,0.1);
      border:1px solid rgba(22,163,74,0.25);
      display:flex; align-items:center; justify-content:center;
      margin-top:2px;
    }
    .checklist .icon svg {
      width:11px; height:11px;
      stroke:var(--green); fill:none;
      stroke-width:3; stroke-linecap:round; stroke-linejoin:round;
    }

    /* PRICE */
    .price-block {
      text-align:center; padding:28px 24px;
      background:var(--card);
      border:1px solid var(--card-border);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      margin-bottom:14px;
    }
    .price-block .price {
      font-family:'Inter',sans-serif;
      font-size:48px; font-weight:700;
      color:var(--text-primary);
      letter-spacing:-0.03em; line-height:1;
    }
    .price-block .price span { font-size:20px; color:var(--text-secondary); font-weight:400; }
    .price-block .price-note { font-size:13px; color:var(--text-secondary); margin-top:5px; }

    /* CTA */
    .cta-btn {
      display:block; width:100%; padding:16px;
      background:var(--accent); color:#fff;
      border:none; border-radius:var(--radius);
      font-size:17px; font-weight:600;
      font-family:'Noto Sans JP',sans-serif;
      cursor:pointer; text-decoration:none; text-align:center;
      transition:background 0.2s, transform 0.1s;
      margin-bottom:14px;
    }
    .cta-btn .en { font-size:12px; opacity:0.75; font-weight:400; display:block; margin-top:2px; }
    .cta-btn:hover { background:var(--accent-hover); }
    .cta-btn:active { transform:scale(0.985); }

    /* TRUST */
    .trust-row {
      display:flex; justify-content:center;
      gap:20px; flex-wrap:wrap; margin-bottom:28px;
    }
    .trust-item { display:flex; align-items:center; gap:5px; font-size:13px; color:var(--text-secondary); }
    .trust-item svg {
      width:14px; height:14px;
      stroke:var(--green); fill:none;
      stroke-width:2.5; stroke-linecap:round; stroke-linejoin:round;
    }

    /* DISCLAIMER */
    .disclaimer {
      text-align:center; font-size:12px;
      color:var(--text-secondary); line-height:1.9;
      padding-top:20px; border-top:1px solid var(--card-border);
    }
    .disclaimer a { color:var(--accent); text-decoration:none; }
    .disclaimer a:hover { text-decoration:underline; }

    @media(max-width:480px){
      .wrapper { padding:36px 16px 56px; }
      .card,.price-block { padding:18px; }
    }
  </style>
</head>
<body>
<div class="wrapper">

  <header class="header">
    <div class="badge">住宅トラブル記録作成サービス<span class="en">Housing Trouble Record Service</span></div>
    <h1>バラバラの記録を、<br/>相談できる形に整理します</h1>
    <p>時系列PDFと状況整理で、伝えるべき内容が明確になります</p>
  </header>

  <div class="card">
    <div class="card-title">提供内容</div>
    <ul class="checklist">
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>時系列の記録PDF</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>状況の客観的整理</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>対応のヒント集</li>
    </ul>
  </div>

  <div class="card">
    <div class="card-title">できること</div>
    <ul class="checklist">
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>雪で埋もれる前に現場を記録できる</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>時間経過で証拠が消える前に記録できる</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>記憶が曖昧になる前に状況を固定できる</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>資料がないと対応が難しいと言われる前に記録できる</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>バラバラなメモを1つの資料にまとめられる</li>
    </ul>
  </div>

  <div class="card">
    <div class="card-title">こんな方に</div>
    <ul class="checklist">
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>記録があるのに整理できていない</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>相談の準備をしたい</li>
      <li><span class="icon"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></span>状況を可視化したい</li>
    </ul>
  </div>

  <div class="price-block">
    <div class="price">2,980 <span>JPY</span></div>
    <div class="price-note">買い切り（One-time payment）</div>
  </div>

  <!-- ↓ href に Stripe の決済URL を入れる -->
  <a href="#" class="cta-btn">今すぐ記録を作成する<span class="en">Create your record now</span></a>

  <div class="trust-row">
    <div class="trust-item"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>24時間返金対応</div>
    <div class="trust-item"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Stripe決済</div>
    <div class="trust-item"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>即時生成</div>
  </div>

  <div class="disclaimer">
    ＊本サービスは記録整理補助ツールです<br/>
    ＊法的助言・判断・推奨を含みません<br/>
    ＊購入後24時間は理由を問わず返金対応<br/><br/>
    <a href="#">特定商取引法に基づく表記</a>　|　<a href="#">Terms of Service</a>
  </div>

</div>
</body>
</html>
