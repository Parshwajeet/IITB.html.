# IITB.html.
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="AstraPaw — AI pet care for adventurous owners. Trusted, scheduled, and stellar care for your pet while you explore the stars." />
  <title>AstraPaw — AI Pet Sitter for the Modern Explorer</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg: #071226;
      --card: #0f1724;
      --muted: #a6b0c3;
      --accent1: #7afcff;
      --accent2: #8a7bff;
      --glass: rgba(255,255,255,0.04);
      --radius: 14px;
      --max-width: 1100px;
      --container-gap: 1.25rem;
      --ff: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--ff);
      background: linear-gradient(180deg, #050611 0%, var(--bg) 50%);
      color:#e8eefb;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      font-size:16px;
    }
    .reduced-motion * { animation: none !important; transition: none !important; }
    .container{
      width: calc(100% - 2rem);
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 2rem 1rem;
    }
    .header-inner, .footer-inner { display:flex; align-items:center; justify-content:space-between; gap:1rem; }
    .site-header{
      position:sticky;
      top:0;
      z-index:30;
      background: linear-gradient(180deg, rgba(7,10,22,0.6), rgba(7,10,22,0.2));
      backdrop-filter: blur(6px);
      border-bottom:1px solid rgba(255,255,255,0.03);
    }
    .brand{
      display:flex;
      align-items:center;
      gap:.6rem;
      color:var(--accent1);
      text-decoration:none;
      font-weight:700;
    }
    .brand svg{ color:var(--accent1) }
    .brand-name{ font-size:1.05rem; letter-spacing:0.2px; }
    .main-nav .nav-list{ list-style:none; margin:0; padding:0; display:flex; gap:1rem; }
    .nav-link { color:var(--muted); text-decoration:none; font-weight:600; font-size:.95rem; }
    .nav-link:hover, .nav-link:focus { color: white; outline: none; text-decoration:underline; }
    .hero{
      min-height: calc(100vh - 72px);
      display:flex;
      align-items:center;
      padding-top: 2.5rem;
      padding-bottom: 3rem;
    }
    .hero-grid{
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:2rem;
      align-items:center;
    }
    .eyebrow{ color:var(--accent1); font-weight:700; letter-spacing:1px; font-size:.82rem; margin:0 0 .5rem 0; }
    .hero-title{
      font-size: clamp(2rem, 4.6vw, 3.1rem);
      margin:0 0 1rem 0;
      line-height:1.03;
      font-weight:800;
      color: #fff;
    }
    .animated-text{
      display:inline-block;
      background: linear-gradient(90deg, var(--accent1), #5ee7ff 20%, var(--accent2) 60%, #ffb7ff 100%);
      background-size: 300% 100%;
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientShift 6s linear infinite, floatUp 6s ease-in-out infinite;
      will-change: background-position, transform;
    }
    @keyframes gradientShift {
      0% { background-position: 0% 50%; filter: hue-rotate(0deg); }
      50% { background-position: 100% 50%; filter: hue-rotate(20deg); }
      100% { background-position: 0% 50%; filter: hue-rotate(0deg); }
    }
    @keyframes floatUp {
      0% { transform: translateY(0); }
      25% { transform: translateY(-6px); }
      50% { transform: translateY(0); }
      75% { transform: translateY(-3px); }
      100% { transform: translateY(0); }
    }
    .lead{ color:var(--muted); font-size:1.02rem; margin:0 0 1.2rem 0; max-width:54ch; }
    .btn{ display:inline-block; text-decoration:none; padding:0.75rem 1.2rem; border-radius:10px; font-weight:700; font-size:.95rem; margin-right:.6rem; }
    .btn.primary{ background: linear-gradient(90deg, var(--accent1), var(--accent2)); color:#071226; box-shadow: 0 8px 30px rgba(106,90,255,0.12); }
    .btn.ghost{ background:transparent; color:var(--muted); border:1px solid rgba(255,255,255,0.06); }
    .trust-list{ list-style:none; padding:0; margin:1.25rem 0 0 0; display:flex; gap:1.25rem; color:var(--muted); font-size:.92rem; }
    .trust-list strong{ color:#fff; margin-right:.25rem; }
    .hero-visual{ border-radius:var(--radius); overflow:hidden; background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); padding:1rem; box-shadow: 0 12px 40px rgba(2,6,23,0.6); }
    .hero-footer{ margin-top:2.5rem; padding-top:1.25rem; border-top:1px solid rgba(255,255,255,0.03); color:var(--muted); }
    .hero-footer .small{ padding:0; }
    .site-footer{ border-top:1px solid rgba(255,255,255,0.03); padding:1rem 0; color:var(--muted); background:linear-gradient(180deg, transparent, rgba(0,0,0,0.15)); }
    .site-footer a{ color:var(--muted); text-decoration:none; margin-left:.6rem }
    .site-footer a:hover{ color: white }
    @media (max-width: 980px){
      .hero-grid{ grid-template-columns: 1fr; }
      .hero-visual{ order:-1; margin-bottom: 1rem; height: 280px; }
      .header-inner{ padding:0.6rem 0; }
      .main-nav { display:none; }
    }
    @media (max-width:480px){
      .lead{ font-size:.95rem }
      .trust-list{ flex-direction:column; gap:.5rem; }
      .brand-name{ display:none }
    }
    a:focus, button:focus { outline: 3px solid rgba(122,123,255,0.16); outline-offset:3px; border-radius:6px; }
  </style>
</head>
<body>
  <header class="site-header" role="banner">
    <div class="container header-inner">
      <a class="brand" href="#" aria-label="AstraPaw home">
        <svg width="36" height="36" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <path fill="currentColor" d="M12 2c1.1 0 2 .9 2 2v3h3c1.1 0 2 .9 2 2v6c0 1.1-.9 2-2 2h-3v3c0 1.1-.9 2-2 2s-2-.9-2-2v-3H7c-1.1 0-2-.9-2-2V9c0-1.1.9-2 2-2h3V4c0-1.1.9-2 2-2z"/>
        </svg>
        <span class="brand-name">AstraPaw</span>
      </a>
      <nav class="main-nav" role="navigation" aria-label="Main">
        <ul class="nav-list">
          <li><a href="#how" class="nav-link">How it works</a></li>
          <li><a href="#features" class="nav-link">Features</a></li>
          <li><a href="#cta" class="nav-link">Get started</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main id="main" class="site-main" role="main">
    <section class="hero" aria-labelledby="hero-title" id="hero">
      <div class="container hero-grid">
        <div class="hero-content">
          <p class="eyebrow">AI · Remote · Trusted</p>
          <h1 id="hero-title" class="hero-title">
            Your pet's care, <span class="animated-text">out of this world</span>
          </h1>
          <p class="lead">
            AstraPaw uses onboard-like telemetry and AI routines to schedule walks, feedings, vet alerts and playtime — whether you're on a launchpad or late at work.
            Real-time camera checks, adaptive routines, and human-verified visits.
          </p>
          <div class="hero-ctas" id="cta">
            <a class="btn primary" href="#" role="button">Start free trial</a>
            <a class="btn ghost" href="#how">See how it works</a>
          </div>
          <ul class="trust-list" aria-hidden="false">
            <li><strong>99.9%</strong> uptime on cameras</li>
            <li><strong>24/7</strong> human support</li>
            <li><strong>Trusted</strong> by 12,000+ explorers</li>
          </ul>
        </div>
        <figure class="hero-visual" aria-hidden="true">
          <svg viewBox="0 0 400 300" width="100%" height="100%" role="img" aria-label="Illustration of a pet wearing a tiny space helmet">
            <defs>
              <linearGradient id="g1" x1="0" x2="1">
                <stop offset="0" stop-color="#8be9fd"/>
                <stop offset="1" stop-color="#6c6cff"/>
              </linearGradient>
            </defs>
            <rect width="100%" height="100%" rx="18" fill="#0b1020"></rect>
            <g transform="translate(40,20)">
              <circle cx="220" cy="120" r="80" fill="url(#g1)" opacity="0.15"/>
              <g fill="#fff">
                <ellipse cx="180" cy="150" rx="40" ry="30" fill="#fff" opacity="0.95"/>
                <circle cx="170" cy="140" r="6" />
                <circle cx="190" cy="140" r="6" />
                <path d="M155 160 q25 18 50 0" stroke="#222" stroke-width="3" fill="none" stroke-linecap="round"/>
                <circle cx="180" cy="105" r="36" fill="rgba(255,255,255,0.06)" stroke="#fff" stroke-opacity="0.12"/>
                <rect x="150" y="75" width="60" height="6" rx="3" fill="#fff" opacity="0.12"/>
              </g>
            </g>
          </svg>
        </figure>
      </div>
      <div class="hero-footer" id="how">
        <div class="container small">
          <h3>How it works</h3>
          <p class="muted">Schedule: AI plans → Human-approved visits → Live-checks → Reports to your phone.</p>
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer" role="contentinfo">
    <div class="container footer-inner">
      <p>© <span id="year"></span> AstraPaw — All rights reserved.</p>
      <nav aria-label="footer">
        <a href="#">Privacy</a> · <a href="#">Terms</a> · <a href="#">Contact</a>
      </nav>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
    if (window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
      document.documentElement.classList.add('reduced-motion');
    }
  </script>
</body>
</html>
