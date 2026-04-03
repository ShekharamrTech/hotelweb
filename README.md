<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mandya Nati Style Hotel — Authentic Karnataka Flavours</title>
<link href="https://fonts.googleapis.com/css2?family=Tiro+Kannada&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@300;400;700&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --gold: #C8860A;
    --gold-light: #F0B94A;
    --gold-pale: #FDF3DC;
    --dark: #1A0E00;
    --dark2: #2E1A00;
    --brown: #5C3010;
    --cream: #FDF6E3;
    --green: #2D5A1B;
    --green2: #3E7A25;
    --red: #8B1C1C;
    --text: #2E1A00;
    --text-light: #6B4226;
    --border: rgba(200,134,10,0.25);
  }

  html { scroll-behavior: smooth; }
  body {
    font-family: 'Lato', sans-serif;
    background: var(--cream);
    color: var(--text);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(26,14,0,0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--gold);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 4vw;
    height: 64px;
  }
  .nav-logo {
    font-family: 'Tiro Kannada', serif;
    color: var(--gold-light);
    font-size: 1.35rem;
    letter-spacing: 0.02em;
    text-decoration: none;
    line-height: 1.2;
  }
  .nav-logo span { display: block; font-family: 'Lato', sans-serif; font-size: 0.6rem; color: var(--gold); letter-spacing: 0.18em; text-transform: uppercase; }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a { color: #D4B483; text-decoration: none; font-size: 0.82rem; letter-spacing: 0.12em; text-transform: uppercase; transition: color 0.2s; }
  .nav-links a:hover { color: var(--gold-light); }
  .nav-cta {
    background: var(--gold);
    color: var(--dark);
    border: none; cursor: pointer;
    padding: 0.5rem 1.2rem;
    font-family: 'Lato', sans-serif;
    font-size: 0.78rem; font-weight: 700;
    letter-spacing: 0.1em; text-transform: uppercase;
    transition: background 0.2s;
    text-decoration: none;
  }
  .nav-cta:hover { background: var(--gold-light); }
  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
  .hamburger span { width: 24px; height: 2px; background: var(--gold); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background:
      linear-gradient(to bottom, rgba(26,14,0,0.72) 0%, rgba(26,14,0,0.45) 40%, rgba(26,14,0,0.85) 100%),
      url('https://images.unsplash.com/photo-1600891964092-4316c288032e?w=1600&auto=format&fit=crop&q=80') center/cover no-repeat;
    display: flex; align-items: center; justify-content: center;
    text-align: center;
    position: relative; padding: 64px 1rem 0;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at center, transparent 30%, rgba(26,14,0,0.5) 100%);
    pointer-events: none;
  }
  .hero-content { position: relative; z-index: 1; max-width: 780px; }
  .hero-badge {
    display: inline-block;
    border: 1px solid var(--gold);
    color: var(--gold-light);
    font-size: 0.7rem; letter-spacing: 0.22em; text-transform: uppercase;
    padding: 0.4rem 1.2rem; margin-bottom: 1.8rem;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 7vw, 5.5rem);
    color: #FDF6E3;
    line-height: 1.1;
    margin-bottom: 0.5rem;
  }
  .hero h1 em { color: var(--gold-light); font-style: italic; }
  .hero-kannada {
    font-family: 'Tiro Kannada', serif;
    font-size: clamp(1.1rem, 3vw, 1.8rem);
    color: var(--gold);
    margin-bottom: 1.5rem;
    opacity: 0.9;
  }
  .hero p {
    color: #D4C4A8; font-size: 1.05rem; line-height: 1.7;
    max-width: 520px; margin: 0 auto 2.5rem;
  }
  .hero-btns { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
  .btn-primary {
    background: var(--gold);
    color: var(--dark);
    padding: 0.9rem 2.2rem;
    font-weight: 700; font-size: 0.85rem;
    letter-spacing: 0.1em; text-transform: uppercase;
    text-decoration: none; border: none; cursor: pointer;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }
  .btn-outline {
    border: 1.5px solid var(--gold);
    color: var(--gold-light);
    padding: 0.9rem 2.2rem;
    font-weight: 700; font-size: 0.85rem;
    letter-spacing: 0.1em; text-transform: uppercase;
    text-decoration: none; background: transparent; cursor: pointer;
    transition: background 0.2s, color 0.2s;
  }
  .btn-outline:hover { background: var(--gold); color: var(--dark); }
  .hero-scroll {
    position: absolute; bottom: 2.5rem; left: 50%; transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
    color: rgba(253,246,227,0.5); font-size: 0.65rem; letter-spacing: 0.2em; text-transform: uppercase;
  }
  .scroll-line { width: 1px; height: 48px; background: linear-gradient(to bottom, transparent, var(--gold)); animation: scrollDown 2s ease-in-out infinite; }
  @keyframes scrollDown { 0%,100%{transform:scaleY(0);transform-origin:top} 50%{transform:scaleY(1);transform-origin:top} }

  /* ── SECTION WRAPPER ── */
  section { padding: 6rem 4vw; }
  .section-label {
    font-size: 0.65rem; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.8rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    color: var(--dark); line-height: 1.15;
    margin-bottom: 1.2rem;
  }
  .section-title em { color: var(--gold); font-style: italic; }
  .divider {
    width: 60px; height: 2px;
    background: linear-gradient(to right, var(--gold), transparent);
    margin-bottom: 1.5rem;
  }
  .divider.center { margin: 0 auto 1.5rem; }

  /* ── ABOUT ── */
  .about {
    background: var(--dark);
    position: relative;
  }
  .about::before {
    content: '';
    position: absolute; top: 0; right: 0; bottom: 0; width: 40%;
    background: url('https://images.unsplash.com/photo-1567188040759-fb8a883dc6d8?w=800&auto=format&fit=crop&q=80') center/cover;
    opacity: 0.18;
  }
  .about-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; align-items: center; max-width: 1100px; margin: 0 auto; position: relative; z-index: 1; }
  .about .section-label { color: var(--gold); }
  .about .section-title { color: #FDF6E3; }
  .about p { color: #B8A07A; line-height: 1.85; font-size: 1rem; margin-bottom: 1.2rem; }
  .about-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-top: 2.5rem; }
  .stat-box {
    border: 1px solid rgba(200,134,10,0.25);
    padding: 1.2rem;
    position: relative;
  }
  .stat-box::before {
    content: '';
    position: absolute; top: -1px; left: 0; width: 40%; height: 2px;
    background: var(--gold);
  }
  .stat-num { font-family: 'Playfair Display', serif; font-size: 2.2rem; color: var(--gold-light); line-height: 1; }
  .stat-label { font-size: 0.7rem; letter-spacing: 0.12em; text-transform: uppercase; color: #7A5E3A; margin-top: 0.3rem; }
  .about-img { position: relative; }
  .about-img img { width: 100%; object-fit: cover; display: block; }
  .about-img-frame {
    position: absolute; top: -16px; left: -16px; right: 16px; bottom: 16px;
    border: 1.5px solid rgba(200,134,10,0.35);
    pointer-events: none;
  }

  /* ── MENU ── */
  .menu { background: var(--cream); }
  .menu-header { text-align: center; max-width: 600px; margin: 0 auto 3.5rem; }
  .menu-tabs { display: flex; justify-content: center; gap: 0; margin-bottom: 3rem; flex-wrap: wrap; }
  .tab-btn {
    padding: 0.75rem 1.8rem;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--text-light);
    font-family: 'Lato', sans-serif;
    font-size: 0.78rem; letter-spacing: 0.14em; text-transform: uppercase;
    cursor: pointer; transition: all 0.2s;
  }
  .tab-btn:hover { background: var(--gold-pale); color: var(--brown); }
  .tab-btn.active { background: var(--gold); color: var(--dark); border-color: var(--gold); }
  .menu-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 1.5rem; max-width: 1200px; margin: 0 auto; }
  .menu-card {
    background: #fff;
    border: 1px solid var(--border);
    padding: 1.5rem;
    position: relative;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .menu-card:hover { transform: translateY(-3px); box-shadow: 0 12px 40px rgba(200,134,10,0.1); }
  .menu-card-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 0.6rem; }
  .menu-card h3 { font-family: 'Playfair Display', serif; font-size: 1.1rem; color: var(--dark); }
  .price { font-size: 1rem; font-weight: 700; color: var(--gold); white-space: nowrap; margin-left: 1rem; }
  .menu-card p { font-size: 0.85rem; color: var(--text-light); line-height: 1.6; }
  .veg-dot { display: inline-block; width: 10px; height: 10px; border-radius: 50%; margin-right: 6px; vertical-align: middle; }
  .veg { background: var(--green); }
  .nonveg { background: var(--red); }
  .menu-badge {
    display: inline-block; font-size: 0.58rem; letter-spacing: 0.12em; text-transform: uppercase;
    padding: 0.2rem 0.5rem; margin-bottom: 0.5rem;
    background: var(--gold-pale); color: var(--gold); border: 1px solid var(--gold-light);
  }
  .tab-panel { display: none; }
  .tab-panel.active { display: block; }

  /* ── SPECIALS ── */
  .specials {
    background:
      linear-gradient(135deg, rgba(26,14,0,0.94) 60%, rgba(92,48,16,0.9) 100%),
      url('https://images.unsplash.com/photo-1617692855027-33b14f061079?w=1400&auto=format&fit=crop&q=80') center/cover;
    text-align: center;
  }
  .specials .section-label { color: var(--gold); }
  .specials .section-title { color: #FDF6E3; }
  .specials .section-title em { color: var(--gold-light); }
  .specials-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 2rem; max-width: 1100px; margin: 3rem auto 0; }
  .special-item {
    border: 1px solid rgba(200,134,10,0.2);
    padding: 2rem 1.5rem;
    position: relative; overflow: hidden;
    transition: border-color 0.3s;
  }
  .special-item:hover { border-color: var(--gold); }
  .special-icon { font-size: 2.8rem; margin-bottom: 1rem; }
  .special-item h3 { font-family: 'Playfair Display', serif; font-size: 1.15rem; color: var(--gold-light); margin-bottom: 0.6rem; }
  .special-item p { font-size: 0.85rem; color: #8A7055; line-height: 1.7; }

  /* ── GALLERY ── */
  .gallery { background: #FEF9EE; }
  .gallery-header { text-align: center; margin-bottom: 3rem; }
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 220px 220px;
    gap: 12px;
    max-width: 1200px; margin: 0 auto;
  }
  .g-item { overflow: hidden; position: relative; }
  .g-item img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform 0.5s; }
  .g-item:hover img { transform: scale(1.07); }
  .g-item:nth-child(1) { grid-column: span 5; grid-row: span 2; }
  .g-item:nth-child(2) { grid-column: span 4; }
  .g-item:nth-child(3) { grid-column: span 3; }
  .g-item:nth-child(4) { grid-column: span 3; }
  .g-item:nth-child(5) { grid-column: span 4; }
  .g-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(26,14,0,0.5), transparent);
    opacity: 0; transition: opacity 0.3s;
  }
  .g-item:hover .g-overlay { opacity: 1; }

  /* ── RESERVATIONS ── */
  .reservations { background: var(--dark2); }
  .res-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; max-width: 1100px; margin: 0 auto; align-items: start; }
  .res-info .section-label { color: var(--gold); }
  .res-info .section-title { color: #FDF6E3; }
  .res-info p { color: #8A7055; line-height: 1.8; margin-bottom: 1.5rem; }
  .contact-list { list-style: none; display: flex; flex-direction: column; gap: 1rem; }
  .contact-list li { display: flex; align-items: flex-start; gap: 0.9rem; }
  .contact-icon { width: 36px; height: 36px; border: 1px solid rgba(200,134,10,0.3); display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .contact-list span { font-size: 0.88rem; color: #B8A07A; line-height: 1.5; }
  .contact-list strong { display: block; font-size: 0.7rem; text-transform: uppercase; letter-spacing: 0.12em; color: var(--gold); margin-bottom: 0.2rem; }
  .res-form { background: rgba(255,255,255,0.04); border: 1px solid rgba(200,134,10,0.18); padding: 2.5rem; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.4rem; margin-bottom: 1rem; }
  .form-group label { font-size: 0.68rem; letter-spacing: 0.18em; text-transform: uppercase; color: var(--gold); }
  .form-group input, .form-group select, .form-group textarea {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(200,134,10,0.22);
    color: #D4B483;
    padding: 0.75rem 1rem;
    font-family: 'Lato', sans-serif;
    font-size: 0.88rem;
    outline: none;
    transition: border-color 0.2s;
  }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus { border-color: var(--gold); }
  .form-group select option { background: var(--dark2); color: #D4B483; }
  .form-group textarea { resize: vertical; min-height: 90px; }
  .form-group input::placeholder, .form-group textarea::placeholder { color: rgba(180,140,80,0.4); }
  .form-msg { display: none; padding: 0.8rem 1rem; margin-bottom: 1rem; font-size: 0.85rem; }
  .form-msg.success { background: rgba(45,90,27,0.2); border: 1px solid var(--green2); color: #7EC85A; }
  .form-msg.error { background: rgba(139,28,28,0.2); border: 1px solid var(--red); color: #E86B6B; }

  /* ── TIMINGS ── */
  .timings { background: var(--cream); }
  .timings-inner { max-width: 900px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
  .timing-table { width: 100%; border-collapse: collapse; margin-top: 1.5rem; }
  .timing-table tr { border-bottom: 1px solid var(--border); }
  .timing-table td { padding: 0.85rem 0; font-size: 0.9rem; color: var(--text-light); }
  .timing-table td:last-child { text-align: right; font-weight: 700; color: var(--dark); }
  .timing-table tr:last-child td { border-bottom: none; }
  .highlight-row td { color: var(--gold) !important; }

  /* ── TESTIMONIALS ── */
  .testimonials { background: var(--dark); text-align: center; }
  .test-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; max-width: 1100px; margin: 3rem auto 0; }
  .test-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(200,134,10,0.15);
    padding: 2rem 1.8rem;
    text-align: left;
    position: relative;
  }
  .test-card::before {
    content: '"';
    font-family: 'Playfair Display', serif;
    font-size: 5rem; line-height: 1;
    color: rgba(200,134,10,0.15);
    position: absolute; top: 0.5rem; left: 1rem;
  }
  .test-card p { font-size: 0.92rem; color: #9A8060; line-height: 1.75; margin-bottom: 1.5rem; font-style: italic; }
  .test-author { display: flex; align-items: center; gap: 0.8rem; }
  .test-avatar { width: 40px; height: 40px; border-radius: 50%; background: var(--gold); display: flex; align-items: center; justify-content: center; font-weight: 700; color: var(--dark); font-size: 0.9rem; flex-shrink: 0; }
  .test-name { font-size: 0.85rem; font-weight: 700; color: var(--gold-light); }
  .test-loc { font-size: 0.72rem; color: #5C4228; text-transform: uppercase; letter-spacing: 0.1em; }
  .stars { color: var(--gold); font-size: 0.9rem; margin-bottom: 0.8rem; }

  /* ── FOOTER ── */
  footer {
    background: #0E0800;
    padding: 4rem 4vw 2rem;
    border-top: 1px solid rgba(200,134,10,0.2);
  }
  .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 3rem; max-width: 1200px; margin: 0 auto 3rem; }
  .footer-brand .nav-logo { font-size: 1.5rem; display: block; margin-bottom: 1rem; }
  .footer-brand p { font-size: 0.85rem; color: #5C4228; line-height: 1.7; max-width: 280px; }
  .footer-col h4 { font-size: 0.68rem; letter-spacing: 0.22em; text-transform: uppercase; color: var(--gold); margin-bottom: 1.2rem; }
  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 0.7rem; }
  .footer-col ul a { font-size: 0.84rem; color: #5C4228; text-decoration: none; transition: color 0.2s; }
  .footer-col ul a:hover { color: var(--gold); }
  .footer-bottom { border-top: 1px solid rgba(200,134,10,0.1); padding-top: 1.5rem; display: flex; justify-content: space-between; align-items: center; max-width: 1200px; margin: 0 auto; flex-wrap: wrap; gap: 1rem; }
  .footer-bottom p { font-size: 0.75rem; color: #3A2510; }
  .social-links { display: flex; gap: 0.8rem; }
  .social-links a {
    width: 34px; height: 34px; border: 1px solid rgba(200,134,10,0.2);
    display: flex; align-items: center; justify-content: center;
    color: #5C4228; text-decoration: none; font-size: 0.8rem;
    transition: all 0.2s;
  }
  .social-links a:hover { border-color: var(--gold); color: var(--gold); }

  /* ── MOBILE NAV ── */
  #mob-menu {
    display: none; position: fixed; top: 64px; left: 0; right: 0; bottom: 0;
    background: rgba(14,8,0,0.98); z-index: 99;
    flex-direction: column; align-items: center; justify-content: center; gap: 2rem;
  }
  #mob-menu.open { display: flex; }
  #mob-menu a { color: var(--gold-light); text-decoration: none; font-size: 1.2rem; letter-spacing: 0.15em; text-transform: uppercase; }

  /* ── FLOATING ORDER ── */
  .float-btn {
    position: fixed; bottom: 2rem; right: 2rem; z-index: 90;
    background: var(--gold); color: var(--dark);
    border: none; cursor: pointer;
    padding: 0.9rem 1.6rem;
    font-family: 'Lato', sans-serif; font-size: 0.78rem; font-weight: 700;
    letter-spacing: 0.1em; text-transform: uppercase;
    box-shadow: 0 4px 20px rgba(200,134,10,0.4);
    text-decoration: none; display: flex; align-items: center; gap: 0.5rem;
    transition: background 0.2s, transform 0.15s;
  }
  .float-btn:hover { background: var(--gold-light); transform: translateY(-2px); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .nav-links, .nav-cta { display: none; }
    .hamburger { display: flex; }
    .about-inner, .res-inner, .timings-inner, .footer-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .about-img { display: none; }
    .about::before { display: none; }
    .gallery-grid { grid-template-columns: 1fr 1fr; grid-template-rows: auto; }
    .g-item { grid-column: span 1 !important; grid-row: span 1 !important; height: 180px; }
    .form-row { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 580px) {
    section { padding: 4rem 5vw; }
    .footer-grid { grid-template-columns: 1fr; }
    .about-stats { grid-template-columns: 1fr 1fr; }
    .gallery-grid { grid-template-columns: 1fr; }
    .g-item { height: 200px; }
  }

  /* ── ANIMATIONS ── */
  .fade-in { opacity: 0; transform: translateY(28px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .fade-in.visible { opacity: 1; transform: none; }
</style>
</head>
<body>

<!-- NAV -->
<nav id="navbar">
  <a href="#" class="nav-logo">ಮಂಡ್ಯ ನಾಟಿ<span>Mandya Nati Style Hotel</span></a>
  <ul class="nav-links">
    <li><a href="#about">Our Story</a></li>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#specials">Specials</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#timings">Timings</a></li>
  </ul>
  <a href="#reservations" class="nav-cta">Book a Table</a>
  <div class="hamburger" id="ham" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- MOBILE MENU -->
<div id="mob-menu">
  <a href="#about" onclick="closeMenu()">Our Story</a>
  <a href="#menu" onclick="closeMenu()">Menu</a>
  <a href="#specials" onclick="closeMenu()">Specials</a>
  <a href="#gallery" onclick="closeMenu()">Gallery</a>
  <a href="#reservations" onclick="closeMenu()">Book a Table</a>
  <a href="#timings" onclick="closeMenu()">Timings</a>
</div>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-content">
    <span class="hero-badge">Est. 1998 · Mandya, Karnataka</span>
    <h1>Taste the <em>True Soul</em><br>of Karnataka</h1>
    <p class="hero-kannada">ನಿಜವಾದ ನಾಟಿ ರುಚಿ, ಹಳ್ಳಿಯ ಶೈಲಿ</p>
    <p>Wood-fired cooking, farm-fresh ingredients, and recipes passed down through generations — authentic nati-style dining at the heart of Mandya.</p>
    <div class="hero-btns">
      <a href="#menu" class="btn-primary">Explore Menu</a>
      <a href="#reservations" class="btn-outline">Reserve a Table</a>
    </div>
  </div>
  <div class="hero-scroll"><div class="scroll-line"></div>Scroll</div>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-inner">
    <div class="fade-in">
      <p class="section-label">Our Story</p>
      <h2 class="section-title">Rooted in <em>Tradition</em>,<br>Cooked with Soul</h2>
      <div class="divider"></div>
      <p>Founded in 1998 by Smt. Kavitha & Sri. Ramu Gowda, Mandya Nati Style Hotel began as a humble roadside eatery serving the Ragi Mudde and Nati Koli Saaru that labourers and farmers swore by. Today, we remain fiercely committed to that legacy.</p>
      <p>Every dish is prepared in our traditional clay pots over firewood, using locally sourced country chicken, fresh greens from Mandya's renowned farms, and cold-pressed coconut oil. No shortcuts. No compromise.</p>
      <div class="about-stats">
        <div class="stat-box"><div class="stat-num">25+</div><div class="stat-label">Years Serving</div></div>
        <div class="stat-box"><div class="stat-num">12</div><div class="stat-label">Family Recipes</div></div>
        <div class="stat-box"><div class="stat-num">500+</div><div class="stat-label">Daily Guests</div></div>
        <div class="stat-box"><div class="stat-num">4.8★</div><div class="stat-label">Google Rating</div></div>
      </div>
    </div>
    <div class="about-img fade-in">
      <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=600&auto=format&fit=crop&q=80" alt="Traditional Karnataka food"/>
      <div class="about-img-frame"></div>
    </div>
  </div>
</section>

<!-- MENU -->
<section class="menu" id="menu">
  <div class="menu-header fade-in">
    <p class="section-label">What We Serve</p>
    <h2 class="section-title">Our <em>Nati</em> Menu</h2>
    <div class="divider center"></div>
    <p style="color:var(--text-light);line-height:1.7;">All dishes prepared fresh, the traditional way. Served on banana leaves on request.</p>
  </div>
  <div class="menu-tabs" id="tabs">
    <button class="tab-btn active" data-tab="meals">Meals & Thali</button>
    <button class="tab-btn" data-tab="starters">Starters</button>
    <button class="tab-btn" data-tab="mains">Mains</button>
    <button class="tab-btn" data-tab="drinks">Drinks & Sweets</button>
  </div>

  <div class="tab-panel active" id="tab-meals">
    <div class="menu-grid">
      <div class="menu-card fade-in">
        <span class="menu-badge">Most Popular</span>
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Full Meals (Oota)</h3><span class="price">₹180</span></div>
        <p>Ragi Mudde, Soppu Saaru, Palya, Rice, Papad, Pickle — unlimited rice & sambar. Served on banana leaf.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Nati Koli Thali</h3><span class="price">₹280</span></div>
        <p>Country chicken curry, Ragi Mudde, 2 palyas, rice, rasam, curd, pickle. Full traditional spread.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Mutton Thali</h3><span class="price">₹320</span></div>
        <p>Slow-cooked nati style mutton saaru, bone-in pieces, served with rice, mudde & fresh rasam.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Akki Roti Set</h3><span class="price">₹120</span></div>
        <p>Three rice flour rotis with coconut chutney, green chili chutney & onion raita.</p>
      </div>
      <div class="menu-card fade-in">
        <span class="menu-badge">Weekend Special</span>
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Fish Thali</h3><span class="price">₹260</span></div>
        <p>Freshwater fish curry (Mandya style), rice, mudde, rasam, papad. Saturdays & Sundays only.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Veg Special Thali</h3><span class="price">₹160</span></div>
        <p>Bisibelebath, Vangi Bath, 2 palyas, rice, rasam, curd, papad. Festive comfort on a plate.</p>
      </div>
    </div>
  </div>

  <div class="tab-panel" id="tab-starters">
    <div class="menu-grid">
      <div class="menu-card fade-in">
        <span class="menu-badge">Chef's Pick</span>
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Nati Koli Sukka</h3><span class="price">₹220</span></div>
        <p>Dry-fried country chicken with freshly ground spices, curry leaves & shallots. Crispy exterior, juicy inside.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Mutton Chops</h3><span class="price">₹260</span></div>
        <p>Marinated with nati masala, slow-roasted over coal. Tender, smoky, finger-licking good.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Kadle Usli</h3><span class="price">₹80</span></div>
        <p>Sprouted chickpeas tossed with grated coconut, green chili, mustard & lime. A wholesome village snack.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Mandakki Puri</h3><span class="price">₹60</span></div>
        <p>Puffed rice chaat with tomato, onion, coriander and our special tamarind-jaggery sauce. Perfectly crunchy.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Egg Bhurji</h3><span class="price">₹90</span></div>
        <p>Country eggs scrambled with onion, tomato, ginger-garlic paste and fresh coriander. Serve with akki roti.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Ragi Mudde (2 pcs)</h3><span class="price">₹40</span></div>
        <p>Traditional finger-millet balls, the heart of any nati meal. Served with soppu saaru or sambar.</p>
      </div>
    </div>
  </div>

  <div class="tab-panel" id="tab-mains">
    <div class="menu-grid">
      <div class="menu-card fade-in">
        <span class="menu-badge">Signature</span>
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Nati Koli Saaru</h3><span class="price">₹200</span></div>
        <p>Country chicken curry slow-cooked with hand-ground masala, coconut milk and village spices. The dish that built our reputation.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Mutton Halu Curry</h3><span class="price">₹280</span></div>
        <p>Mutton in a rich milk-coconut gravy, light yet flavourful. A rare delicacy from Mandya's culinary tradition.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Bisibelebath</h3><span class="price">₹130</span></div>
        <p>Hot lentil rice with 27 spices, topped with ghee and served with papad and raita. Pure Karnataka soul food.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Soppu Saaru</h3><span class="price">₹70</span></div>
        <p>Thin green-leaves curry made with fresh dill, garlic and tamarind. Light and therapeutic.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot nonveg"></span>Prawns Masala</h3><span class="price">₹300</span></div>
        <p>River prawns cooked in a fiery Mandya-style red masala with coconut and curry leaves. Weekend only.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Eerulli Saaru</h3><span class="price">₹80</span></div>
        <p>Traditional shallot curry — thin, tangy, aromatic. A beautiful accompaniment to Ragi Mudde or rice.</p>
      </div>
    </div>
  </div>

  <div class="tab-panel" id="tab-drinks">
    <div class="menu-grid">
      <div class="menu-card fade-in">
        <span class="menu-badge">Bestseller</span>
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Sugarcane Juice</h3><span class="price">₹40</span></div>
        <p>Fresh-pressed Mandya sugarcane with ginger and lime. Chilled and refreshing, straight from the press.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Majjige (Buttermilk)</h3><span class="price">₹30</span></div>
        <p>Hand-churned village-style salted buttermilk with roasted cumin, curry leaves and green chili. Cooling and digestive.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Filter Coffee</h3><span class="price">₹25</span></div>
        <p>Traditional south Indian drip-filtered coffee with full-cream dairy milk. Strong, frothy, and aromatic.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Payasam</h3><span class="price">₹60</span></div>
        <p>Moong dal or rice payasam slow-cooked with jaggery, coconut milk, cardamom and cashews. Festive sweetness.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Panchakajjaya</h3><span class="price">₹50</span></div>
        <p>Traditional offering sweet — roasted Bengal gram, coconut, jaggery, cardamom, and sesame. Auspicious and delicious.</p>
      </div>
      <div class="menu-card fade-in">
        <div class="menu-card-top"><h3><span class="veg-dot veg"></span>Tender Coconut</h3><span class="price">₹45</span></div>
        <p>Freshly cut tender coconut from local farms. Natural hydration at its finest.</p>
      </div>
    </div>
  </div>
</section>

<!-- SPECIALS -->
<section class="specials" id="specials">
  <p class="section-label">Why Choose Us</p>
  <h2 class="section-title">The <em>Nati</em> Difference</h2>
  <div class="divider center" style="background:linear-gradient(to right,transparent,var(--gold),transparent);width:80px;"></div>
  <div class="specials-grid">
    <div class="special-item fade-in">
      <div class="special-icon">🪵</div>
      <h3>Wood-Fired Cooking</h3>
      <p>All our curries simmer over firewood in traditional clay pots. No gas, no pressure cookers — just slow, patient heat.</p>
    </div>
    <div class="special-item fade-in">
      <div class="special-icon">🐔</div>
      <h3>Country Chicken Only</h3>
      <p>We source exclusively nati (country) chicken from local farms. The difference in flavour is unmistakable.</p>
    </div>
    <div class="special-item fade-in">
      <div class="special-icon">🌿</div>
      <h3>Farm-Fresh Greens</h3>
      <p>Vegetables and greens arrive daily from Mandya's agricultural belt — seasonal, pesticide-free, peak flavour.</p>
    </div>
    <div class="special-item fade-in">
      <div class="special-icon">🍃</div>
      <h3>Banana Leaf Service</h3>
      <p>Traditional banana leaf meals available every day. An authentic experience that enhances the taste of food.</p>
    </div>
    <div class="special-item fade-in">
      <div class="special-icon">🏺</div>
      <h3>Clay Pot Recipes</h3>
      <p>Ancient earthenware vessels impart a unique mineral taste to our dishes — a technique lost in most modern restaurants.</p>
    </div>
    <div class="special-item fade-in">
      <div class="special-icon">🤲</div>
      <h3>Generational Recipes</h3>
      <p>Our masalas are hand-ground daily using recipes that have been in the Gowda family for over four generations.</p>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section class="gallery" id="gallery">
  <div class="gallery-header fade-in">
    <p class="section-label">From Our Kitchen</p>
    <h2 class="section-title">A Visual <em>Feast</em></h2>
    <div class="divider center"></div>
  </div>
  <div class="gallery-grid">
    <div class="g-item"><img src="https://images.unsplash.com/photo-1565557623262-b51c2513a641?w=800&auto=format&fit=crop&q=80" alt="Feast spread"/><div class="g-overlay"></div></div>
    <div class="g-item"><img src="https://images.unsplash.com/photo-1567188040759-fb8a883dc6d8?w=500&auto=format&fit=crop&q=80" alt="Curry pot"/><div class="g-overlay"></div></div>
    <div class="g-item"><img src="https://images.unsplash.com/photo-1596797038530-2c107229654b?w=400&auto=format&fit=crop&q=80" alt="Spices"/><div class="g-overlay"></div></div>
    <div class="g-item"><img src="https://images.unsplash.com/photo-1589301760014-d929f3979dbc?w=400&auto=format&fit=crop&q=80" alt="Dal rice"/><div class="g-overlay"></div></div>
    <div class="g-item"><img src="https://images.unsplash.com/photo-1574653853027-5382a3d23a15?w=500&auto=format&fit=crop&q=80" alt="South Indian food"/><div class="g-overlay"></div></div>
  </div>
</section>

<!-- TIMINGS -->
<section class="timings" id="timings">
  <div class="timings-inner">
    <div class="fade-in">
      <p class="section-label">Visit Us</p>
      <h2 class="section-title">Opening <em>Hours</em></h2>
      <div class="divider"></div>
      <p style="color:var(--text-light);line-height:1.75;margin-bottom:0.5rem;">We open early for breakfast and serve continuously through the day. Last orders 30 minutes before closing.</p>
      <table class="timing-table">
        <tr><td>Monday – Friday</td><td>7:00 AM – 10:30 PM</td></tr>
        <tr class="highlight-row"><td>Saturday</td><td>6:30 AM – 11:00 PM</td></tr>
        <tr class="highlight-row"><td>Sunday</td><td>6:30 AM – 11:00 PM</td></tr>
        <tr><td>Public Holidays</td><td>Special hours — call ahead</td></tr>
      </table>
    </div>
    <div class="fade-in" style="border:1px solid var(--border);padding:2.5rem;">
      <p class="section-label">Location</p>
      <h3 style="font-family:'Playfair Display',serif;font-size:1.3rem;margin-bottom:1rem;color:var(--dark);">Find Us in Mandya</h3>
      <p style="font-size:0.9rem;color:var(--text-light);line-height:1.75;margin-bottom:1.5rem;">
        No. 14, KRS Road, Near Bus Stand<br>Mandya — 571 401<br>Karnataka, India
      </p>
      <p style="font-size:0.9rem;color:var(--text-light);line-height:1.75;margin-bottom:0.5rem;">📞 <strong>+91 98450 12345</strong></p>
      <p style="font-size:0.9rem;color:var(--text-light);line-height:1.75;margin-bottom:1.5rem;">📧 <strong>hello@mandyanatihotel.in</strong></p>
      <a href="https://maps.google.com" target="_blank" class="btn-primary" style="display:inline-block;font-size:0.78rem;">Get Directions →</a>
    </div>
  </div>
</section>

<!-- RESERVATIONS -->
<section class="reservations" id="reservations">
  <div class="res-inner">
    <div class="res-info fade-in">
      <p class="section-label">Reserve Your Seat</p>
      <h2 class="section-title">Book a <em>Table</em></h2>
      <div class="divider"></div>
      <p>We welcome walk-ins, but for guaranteed seating — especially on weekends and festivals — we recommend booking ahead. Groups of 10+ can pre-order banana leaf meals.</p>
      <ul class="contact-list">
        <li>
          <div class="contact-icon">📞</div>
          <div><strong>Phone</strong><span>+91 98450 12345<br>+91 97310 67890</span></div>
        </li>
        <li>
          <div class="contact-icon">📍</div>
          <div><strong>Address</strong><span>No. 14, KRS Road, Near Bus Stand<br>Mandya — 571 401, Karnataka</span></div>
        </li>
        <li>
          <div class="contact-icon">⏰</div>
          <div><strong>Best Time to Book</strong><span>Call us before noon for same-day bookings. Weekend group bookings 48 hrs in advance.</span></div>
        </li>
      </ul>
    </div>
    <div class="res-form fade-in">
      <div id="form-msg" class="form-msg"></div>
      <div class="form-row">
        <div class="form-group">
          <label>Full Name</label>
          <input type="text" id="fname" placeholder="Your name"/>
        </div>
        <div class="form-group">
          <label>Phone Number</label>
          <input type="tel" id="fphone" placeholder="+91 XXXXX XXXXX"/>
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Date</label>
          <input type="date" id="fdate"/>
        </div>
        <div class="form-group">
          <label>Time</label>
          <select id="ftime">
            <option value="">Select Time</option>
            <option>7:00 AM</option><option>8:00 AM</option><option>9:00 AM</option>
            <option>12:00 PM</option><option>1:00 PM</option><option>2:00 PM</option>
            <option>6:00 PM</option><option>7:00 PM</option><option>8:00 PM</option><option>9:00 PM</option>
          </select>
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Guests</label>
          <select id="fguests">
            <option>1–2 Guests</option><option>3–4 Guests</option><option>5–8 Guests</option>
            <option>9–15 Guests</option><option>16–30 Guests</option><option>30+ Guests</option>
          </select>
        </div>
        <div class="form-group">
          <label>Meal Preference</label>
          <select id="fmeal">
            <option value="">Select</option>
            <option>Veg Banana Leaf Meals</option>
            <option>Non-Veg Banana Leaf Meals</option>
            <option>Nati Koli Thali</option>
            <option>Mix / Regular Menu</option>
            <option>No Preference</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label>Special Requests</label>
        <textarea id="fnote" placeholder="Any dietary requirements, special occasions, or notes..."></textarea>
      </div>
      <button class="btn-primary" style="width:100%;padding:1rem;" onclick="submitForm()">Confirm Reservation</button>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="testimonials" id="testimonials">
  <p class="section-label">Guest Reviews</p>
  <h2 class="section-title" style="color:#FDF6E3;">What Our <em>Guests</em> Say</h2>
  <div class="divider center" style="background:linear-gradient(to right,transparent,var(--gold),transparent);width:80px;"></div>
  <div class="test-grid">
    <div class="test-card fade-in">
      <div class="stars">★★★★★</div>
      <p>The Nati Koli Saaru here is unlike anything I've had anywhere else. The clay pot aroma, the hand-ground masala — it took me straight back to my grandmother's kitchen. I drive 80 km from Mysuru just for this.</p>
      <div class="test-author"><div class="test-avatar">RK</div><div><div class="test-name">Ramesh Kumar</div><div class="test-loc">Mysuru</div></div></div>
    </div>
    <div class="test-card fade-in">
      <div class="stars">★★★★★</div>
      <p>We brought 40 colleagues for a company lunch — the banana leaf spread was spectacular. The service was warm and genuine, everything arrived hot and fresh. Highly recommend for group bookings.</p>
      <div class="test-author"><div class="test-avatar">SN</div><div><div class="test-name">Savitha Nagaraj</div><div class="test-loc">Bengaluru</div></div></div>
    </div>
    <div class="test-card fade-in">
      <div class="stars">★★★★★</div>
      <p>I've been coming here since 2005. The taste has never changed, and that is the highest compliment I can give. The Ragi Mudde with Soppu Saaru is soul-satisfying food at its simplest and most honest.</p>
      <div class="test-author"><div class="test-avatar">MG</div><div><div class="test-name">Manjunath Gowda</div><div class="test-loc">Mandya</div></div></div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <a href="#" class="nav-logo">ಮಂಡ್ಯ ನಾಟಿ<span>Mandya Nati Style Hotel</span></a>
      <p>Serving authentic Karnataka village-style cuisine since 1998. Wood-fired, clay-pot, banana-leaf — the way it should be.</p>
    </div>
    <div class="footer-col">
      <h4>Navigate</h4>
      <ul>
        <li><a href="#about">Our Story</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#specials">Why Us</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#reservations">Book a Table</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Menu</h4>
      <ul>
        <li><a href="#menu">Meals & Thali</a></li>
        <li><a href="#menu">Starters</a></li>
        <li><a href="#menu">Main Course</a></li>
        <li><a href="#menu">Drinks & Sweets</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contact</h4>
      <ul>
        <li><a href="tel:+919845012345">+91 98450 12345</a></li>
        <li><a href="mailto:hello@mandyanatihotel.in">hello@mandyanatihotel.in</a></li>
        <li><a href="#">KRS Road, Mandya</a></li>
        <li><a href="#">Karnataka — 571 401</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 Mandya Nati Style Hotel. All rights reserved. | Crafted with ♥ in Karnataka</p>
    <div class="social-links">
      <a href="#" title="Facebook">f</a>
      <a href="#" title="Instagram">in</a>
      <a href="#" title="WhatsApp">wa</a>
      <a href="#" title="YouTube">yt</a>
    </div>
  </div>
</footer>

<!-- FLOATING CTA -->
<a href="tel:+919845012345" class="float-btn">📞 Call & Order</a>

<script>
  // Tab switching
  document.querySelectorAll('.tab-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
      document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById('tab-' + btn.dataset.tab).classList.add('active');
    });
  });

  // Scroll animations
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));

  // Mobile menu
  function toggleMenu() {
    document.getElementById('mob-menu').classList.toggle('open');
  }
  function closeMenu() {
    document.getElementById('mob-menu').classList.remove('open');
  }

  // Form submission
  function submitForm() {
    const name = document.getElementById('fname').value.trim();
    const phone = document.getElementById('fphone').value.trim();
    const date = document.getElementById('fdate').value;
    const time = document.getElementById('ftime').value;
    const msg = document.getElementById('form-msg');

    if (!name || !phone || !date || !time) {
      msg.textContent = 'Please fill in your name, phone, date and time to continue.';
      msg.className = 'form-msg error';
      msg.style.display = 'block';
      return;
    }
    msg.textContent = `🎉 Thank you, ${name}! Your table is reserved for ${date} at ${time}. We'll confirm via WhatsApp shortly.`;
    msg.className = 'form-msg success';
    msg.style.display = 'block';
    document.getElementById('fname').value = '';
    document.getElementById('fphone').value = '';
    document.getElementById('fdate').value = '';
    document.getElementById('ftime').value = '';
    document.getElementById('fnote').value = '';
    setTimeout(() => { msg.style.display = 'none'; }, 7000);
  }

  // Nav background on scroll
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('navbar');
    nav.style.boxShadow = window.scrollY > 50 ? '0 2px 24px rgba(0,0,0,0.5)' : 'none';
  });

  // Set min date to today for reservations
  const today = new Date().toISOString().split('T')[0];
  document.getElementById('fdate').min = today;
</script>
</body>
</html>
