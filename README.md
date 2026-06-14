# elccon-website-
environmental life change community organisation net 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ELCCON – Environmental Life Change Community Organization Net</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --forest:   #1B4332;
    --leaf:     #2D6A4F;
    --lime:     #74C69D;
    --gold:     #E9B84A;
    --brown:    #8B5E3C;
    --soil:     #5C3D1E;
    --mist:     #F7F5F0;
    --white:    #FFFFFF;
    --charcoal: #2D2D2D;
    --gray:     #6B7280;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--mist);
    color: var(--charcoal);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(27,67,50,0.97);
    backdrop-filter: blur(8px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%;
    height: 68px;
    border-bottom: 1px solid rgba(233,184,74,0.25);
  }
  .nav-logo {
    display: flex; align-items: center; gap: 12px;
  }
  .nav-emblem {
    width: 42px; height: 42px;
    background: var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 20px;
    flex-shrink: 0;
  }
  .nav-name {
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 1rem;
    color: var(--white);
    line-height: 1.2;
  }
  .nav-name span { color: var(--gold); display: block; font-size: 0.7rem; font-style: italic; font-weight: 400; }
  .nav-links {
    display: flex; gap: 32px; list-style: none;
  }
  .nav-links a {
    color: rgba(255,255,255,0.8);
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── HERO ── */
  .hero {
    position: relative;
    min-height: 100vh;
    background: var(--forest);
    display: flex; align-items: center;
    overflow: hidden;
  }

  /* Organic texture layer */
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 60% 80% at 70% 50%, rgba(45,106,79,0.6) 0%, transparent 70%),
      radial-gradient(ellipse 40% 60% at 20% 80%, rgba(92,61,30,0.4) 0%, transparent 60%);
  }

  /* Floating fruit/leaf decorations */
  .hero-deco {
    position: absolute; right: 0; top: 0; bottom: 0;
    width: 55%;
    display: flex; align-items: center; justify-content: center;
    pointer-events: none;
  }

  .fruit-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    opacity: 0.18;
    transform: rotate(-8deg) scale(1.1);
  }

  .fruit-item {
    width: 80px; height: 80px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 2.5rem;
    animation: floatFruit 6s ease-in-out infinite;
  }
  .fruit-item:nth-child(2n) { animation-delay: -2s; }
  .fruit-item:nth-child(3n) { animation-delay: -4s; }

  @keyframes floatFruit {
    0%, 100% { transform: translateY(0); }
    50%       { transform: translateY(-12px); }
  }

  .hero-content {
    position: relative; z-index: 2;
    padding: 120px 5% 80px;
    max-width: 700px;
  }

  .hero-eyebrow {
    display: inline-block;
    background: var(--gold);
    color: var(--soil);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 24px;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5.5vw, 5rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.08;
    margin-bottom: 28px;
  }
  .hero-title em {
    font-style: italic;
    color: var(--gold);
  }

  .hero-sub {
    font-size: 1.05rem;
    color: rgba(255,255,255,0.72);
    line-height: 1.7;
    max-width: 520px;
    margin-bottom: 44px;
  }

  .hero-cta-group { display: flex; gap: 16px; flex-wrap: wrap; }

  .btn-primary {
    background: var(--gold);
    color: var(--soil);
    padding: 14px 32px;
    border-radius: 3px;
    font-weight: 700;
    font-size: 0.9rem;
    text-decoration: none;
    letter-spacing: 0.04em;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-primary:hover { background: #f5ca6a; transform: translateY(-2px); }

  .btn-ghost {
    border: 1.5px solid rgba(255,255,255,0.4);
    color: var(--white);
    padding: 14px 32px;
    border-radius: 3px;
    font-weight: 500;
    font-size: 0.9rem;
    text-decoration: none;
    transition: border-color 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-ghost:hover { border-color: var(--gold); color: var(--gold); transform: translateY(-2px); }

  .hero-stats {
    position: absolute;
    bottom: 48px; left: 5%;
    display: flex; gap: 48px; z-index: 2;
  }
  .stat-item { }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 900;
    color: var(--gold);
    line-height: 1;
  }
  .stat-label {
    font-size: 0.72rem;
    color: rgba(255,255,255,0.55);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-top: 4px;
  }

  /* ── WAVE DIVIDER ── */
  .wave {
    display: block;
    width: 100%;
    overflow: hidden;
    line-height: 0;
  }
  .wave svg { display: block; width: 100%; }

  /* ── MISSION ── */
  .section { padding: 96px 5%; }
  .section-inner { max-width: 1100px; margin: 0 auto; }

  .section-label {
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--leaf);
    margin-bottom: 16px;
  }

  .section-heading {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    font-weight: 700;
    color: var(--forest);
    line-height: 1.2;
    margin-bottom: 20px;
  }

  .divider-leaf {
    width: 60px; height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--lime));
    border-radius: 2px;
    margin-bottom: 32px;
  }

  .mission-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
  }

  .mission-text p {
    font-size: 1rem;
    line-height: 1.8;
    color: #4B5563;
    margin-bottom: 20px;
  }

  .mission-cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .mission-card {
    background: var(--white);
    border-radius: 8px;
    padding: 24px 20px;
    border-left: 4px solid var(--gold);
    box-shadow: 0 2px 12px rgba(27,67,50,0.07);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .mission-card:hover { transform: translateY(-4px); box-shadow: 0 8px 24px rgba(27,67,50,0.12); }
  .mission-card .icon { font-size: 2rem; margin-bottom: 10px; }
  .mission-card h4 {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    color: var(--forest);
    margin-bottom: 8px;
  }
  .mission-card p { font-size: 0.85rem; color: var(--gray); line-height: 1.5; margin: 0; }

  /* ── FRUIT TREES ── */
  .trees-section {
    background: var(--forest);
    padding: 96px 5%;
  }
  .trees-section .section-heading { color: var(--white); }
  .trees-section .section-label { color: var(--lime); }

  .trees-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
    margin-top: 56px;
  }

  .tree-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(233,184,74,0.2);
    border-radius: 12px;
    overflow: hidden;
    transition: transform 0.25s, border-color 0.25s;
  }
  .tree-card:hover { transform: translateY(-6px); border-color: var(--gold); }

  .tree-banner {
    height: 180px;
    display: flex; align-items: center; justify-content: center;
    font-size: 5rem;
    position: relative;
    overflow: hidden;
  }
  .tree-banner.citrus   { background: linear-gradient(135deg, #1B4332, #2D6A4F); }
  .tree-banner.avocado  { background: linear-gradient(135deg, #1a3a1a, #2D5016); }
  .tree-banner.macadamia{ background: linear-gradient(135deg, #3b2a1a, #5C3D1E); }

  .tree-info { padding: 28px; }
  .tree-info h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--white);
    margin-bottom: 8px;
  }
  .tree-info .latin {
    font-style: italic;
    font-size: 0.8rem;
    color: var(--lime);
    margin-bottom: 16px;
    display: block;
  }
  .tree-info p {
    font-size: 0.88rem;
    color: rgba(255,255,255,0.65);
    line-height: 1.7;
    margin-bottom: 20px;
  }

  .tree-tags { display: flex; gap: 8px; flex-wrap: wrap; }
  .tag {
    background: rgba(233,184,74,0.15);
    color: var(--gold);
    font-size: 0.72rem;
    padding: 4px 10px;
    border-radius: 20px;
    font-weight: 500;
    border: 1px solid rgba(233,184,74,0.3);
  }

  /* ── OPERATIONS ── */
  .ops-section { background: var(--mist); }

  .ops-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 56px;
  }

  .ops-card {
    background: var(--white);
    border-radius: 10px;
    padding: 36px 28px;
    text-align: center;
    box-shadow: 0 2px 16px rgba(27,67,50,0.06);
    border-top: 3px solid transparent;
    transition: border-color 0.2s, transform 0.2s;
  }
  .ops-card:hover { border-top-color: var(--gold); transform: translateY(-4px); }
  .ops-card .big-icon { font-size: 3rem; margin-bottom: 20px; }
  .ops-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    color: var(--forest);
    margin-bottom: 12px;
  }
  .ops-card p { font-size: 0.87rem; color: var(--gray); line-height: 1.7; }

  /* ── LOCATION BANNER ── */
  .location-banner {
    background: linear-gradient(135deg, var(--brown) 0%, var(--soil) 100%);
    padding: 72px 5%;
    text-align: center;
  }
  .location-banner h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    color: var(--white);
    margin-bottom: 16px;
  }
  .location-banner p {
    color: rgba(255,255,255,0.75);
    font-size: 1rem;
    margin-bottom: 32px;
  }
  .location-pills {
    display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;
  }
  .pill {
    background: rgba(255,255,255,0.12);
    border: 1px solid rgba(255,255,255,0.25);
    color: var(--white);
    padding: 10px 22px;
    border-radius: 30px;
    font-size: 0.85rem;
    font-weight: 500;
  }

  /* ── CONTACT ── */
  .contact-section {
    background: var(--white);
    padding: 96px 5%;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
    max-width: 1100px;
    margin: 0 auto;
  }

  .contact-info h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.4rem);
    color: var(--forest);
    margin-bottom: 16px;
  }

  .contact-info p {
    color: var(--gray);
    font-size: 0.95rem;
    line-height: 1.7;
    margin-bottom: 40px;
  }

  .contact-list { list-style: none; display: flex; flex-direction: column; gap: 24px; }
  .contact-list li {
    display: flex; align-items: flex-start; gap: 16px;
  }
  .c-icon {
    width: 44px; height: 44px; border-radius: 50%;
    background: linear-gradient(135deg, var(--leaf), var(--forest));
    display: flex; align-items: center; justify-content: center;
    font-size: 1.2rem; flex-shrink: 0;
  }
  .c-text strong {
    display: block;
    font-size: 0.78rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--leaf);
    margin-bottom: 2px;
  }
  .c-text span, .c-text a {
    font-size: 0.95rem;
    color: var(--charcoal);
    text-decoration: none;
  }
  .c-text a:hover { color: var(--leaf); }

  /* Contact form panel */
  .contact-form-panel {
    background: var(--mist);
    border-radius: 12px;
    padding: 40px 36px;
  }
  .contact-form-panel h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--forest);
    margin-bottom: 28px;
  }
  .form-group { margin-bottom: 20px; }
  .form-group label {
    display: block;
    font-size: 0.78rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--forest);
    margin-bottom: 8px;
  }
  .form-group input,
  .form-group textarea,
  .form-group select {
    width: 100%;
    padding: 12px 16px;
    border: 1.5px solid #D1D5DB;
    border-radius: 6px;
    font-family: 'Inter', sans-serif;
    font-size: 0.92rem;
    background: var(--white);
    color: var(--charcoal);
    transition: border-color 0.2s;
    outline: none;
  }
  .form-group input:focus,
  .form-group textarea:focus,
  .form-group select:focus { border-color: var(--leaf); }
  .form-group textarea { resize: vertical; min-height: 110px; }

  .btn-submit {
    width: 100%;
    background: var(--forest);
    color: var(--white);
    border: none;
    padding: 14px;
    border-radius: 6px;
    font-family: 'Inter', sans-serif;
    font-size: 0.95rem;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s, transform 0.15s;
    letter-spacing: 0.04em;
  }
  .btn-submit:hover { background: var(--leaf); transform: translateY(-2px); }

  /* ── FOOTER ── */
  footer {
    background: #111;
    color: rgba(255,255,255,0.5);
    padding: 48px 5% 32px;
  }
  .footer-inner {
    max-width: 1100px; margin: 0 auto;
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 24px;
  }
  .footer-brand {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    color: var(--white);
  }
  .footer-brand span { color: var(--gold); }
  .footer-note { font-size: 0.8rem; margin-top: 8px; }
  footer .footer-links { display: flex; gap: 24px; list-style: none; }
  footer .footer-links a { color: rgba(255,255,255,0.4); text-decoration: none; font-size: 0.82rem; transition: color 0.2s; }
  footer .footer-links a:hover { color: var(--gold); }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .mission-grid, .trees-grid, .ops-grid, .contact-grid {
      grid-template-columns: 1fr;
      gap: 32px;
    }
    .mission-cards { grid-template-columns: 1fr; }
    .hero-stats { flex-direction: column; gap: 20px; }
    .nav-links { display: none; }
    .hero-deco { display: none; }
  }

  @media (prefers-reduced-motion: reduce) {
    .fruit-item { animation: none; }
    * { transition: none !important; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <div class="nav-emblem">🌿</div>
    <div class="nav-name">
      ELCCON
      <span>Environmental Life Change Community Org. Net</span>
    </div>
  </div>
  <ul class="nav-links">
    <li><a href="#mission">Mission</a></li>
    <li><a href="#trees">Our Crops</a></li>
    <li><a href="#operations">Operations</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-deco" aria-hidden="true">
    <div class="fruit-grid">
      <div class="fruit-item">🍋</div>
      <div class="fruit-item">🥑</div>
      <div class="fruit-item">🌿</div>
      <div class="fruit-item">🍊</div>
      <div class="fruit-item">🌱</div>
      <div class="fruit-item">🥑</div>
      <div class="fruit-item">🍋</div>
      <div class="fruit-item">🌳</div>
      <div class="fruit-item">🍋</div>
    </div>
  </div>

  <div class="hero-content">
    <span class="hero-eyebrow">Est. 2020 · Wundanyi, Kenya</span>
    <h1 class="hero-title">
      Growing Lives Through<br><em>Nature's Harvest</em>
    </h1>
    <p class="hero-sub">
      ELCCON empowers communities across Eastern and Central Africa by establishing sustainable fruit-tree farms — citrus, avocado, and macadamia — transforming land into lasting livelihood.
    </p>
    <div class="hero-cta-group">
      <a href="#trees" class="btn-primary">Explore Our Farms</a>
      <a href="#contact" class="btn-ghost">Partner With Us</a>
    </div>
  </div>

  <div class="hero-stats">
    <div class="stat-item">
      <div class="stat-num">3+</div>
      <div class="stat-label">Fruit Crop Programmes</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">2</div>
      <div class="stat-label">Regions Active</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">2020</div>
      <div class="stat-label">Year Founded</div>
    </div>
  </div>
</section>

<!-- WAVE -->
<div class="wave">
  <svg viewBox="0 0 1440 60" fill="none" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
    <path d="M0,40 C360,80 1080,0 1440,40 L1440,60 L0,60 Z" fill="#F7F5F0"/>
  </svg>
</div>

<!-- MISSION -->
<section class="section" id="mission">
  <div class="section-inner">
    <div class="mission-grid">
      <div class="mission-text">
        <div class="section-label">Who We Are</div>
        <h2 class="section-heading">Rooted in Community,<br>Grown for Change</h2>
        <div class="divider-leaf"></div>
        <p>
          The Environmental Life Change Community Organization Net (ELCCON) is a grassroots network headquartered in Wundanyi, Taita Taveta County, Kenya. We believe that planting the right tree in the right hands can redefine a community's future.
        </p>
        <p>
          Our work spans Eastern and Central Africa, where we guide smallholder farmers, cooperatives, and youth groups through every stage of orchard development — from soil preparation and seedling selection to harvest and market linkage.
        </p>
        <p>
          We are driven by one conviction: that environmental stewardship and economic empowerment are not competing goals — they are the same goal, grown from the same soil.
        </p>
      </div>
      <div class="mission-cards">
        <div class="mission-card">
          <div class="icon">🌍</div>
          <h4>Environmental Care</h4>
          <p>Restoring green cover and soil health through perennial tree crops.</p>
        </div>
        <div class="mission-card">
          <div class="icon">👩‍🌾</div>
          <h4>Community Uplift</h4>
          <p>Training farmers for sustainable, profitable orchard management.</p>
        </div>
        <div class="mission-card">
          <div class="icon">📈</div>
          <h4>Economic Growth</h4>
          <p>Linking producers to regional and international markets.</p>
        </div>
        <div class="mission-card">
          <div class="icon">🤝</div>
          <h4>Partnerships</h4>
          <p>Collaborating with NGOs, governments, and agribusinesses.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FRUIT TREES -->
<section class="trees-section" id="trees">
  <div class="section-inner">
    <div class="section-label">Our Crop Focus</div>
    <h2 class="section-heading">Three Trees.<br>Infinite Possibilities.</h2>
    <div class="divider-leaf"></div>

    <div class="trees-grid">

      <!-- CITRUS -->
      <div class="tree-card">
        <div class="tree-banner citrus">🍋</div>
        <div class="tree-info">
          <h3>Citrus</h3>
          <span class="latin">Citrus sinensis · Citrus limon · Citrus reticulata</span>
          <p>
            Oranges, lemons, limes, and tangerines thrive in Taita Taveta's warm highland climate. Fast-yielding and high-demand, citrus trees provide early income for farming families while enriching the soil with organic matter.
          </p>
          <div class="tree-tags">
            <span class="tag">High Yield</span>
            <span class="tag">3–5 Year Maturity</span>
            <span class="tag">Export Ready</span>
            <span class="tag">Vitamin C Rich</span>
          </div>
        </div>
      </div>

      <!-- AVOCADO -->
      <div class="tree-card">
        <div class="tree-banner avocado">🥑</div>
        <div class="tree-info">
          <h3>Avocado</h3>
          <span class="latin">Persea americana – Hass & Fuerte varieties</span>
          <p>
            Kenya's avocado is among the most sought-after in European markets. ELCCON promotes Hass and Fuerte varieties, supporting farmers from certified planting material through Good Agricultural Practice (GAP) certification and export linkage.
          </p>
          <div class="tree-tags">
            <span class="tag">EU Export</span>
            <span class="tag">High-Value</span>
            <span class="tag">GAP Certified</span>
            <span class="tag">Drought Hardy</span>
          </div>
        </div>
      </div>

      <!-- MACADAMIA -->
      <div class="tree-card">
        <div class="tree-banner macadamia">🌰</div>
        <div class="tree-info">
          <h3>Macadamia</h3>
          <span class="latin">Macadamia integrifolia · M. tetraphylla</span>
          <p>
            A long-term wealth crop, macadamia trees produce for over 40 years once established. ELCCON supports farmer groups to plant, manage, and collectively process macadamia nuts for premium domestic and international markets.
          </p>
          <div class="tree-tags">
            <span class="tag">40+ Year Lifespan</span>
            <span class="tag">Premium Nuts</span>
            <span class="tag">Carbon Sequestration</span>
            <span class="tag">Group Farming</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- OPERATIONS -->
<section class="section ops-section" id="operations">
  <div class="section-inner">
    <div class="section-label">What We Do</div>
    <h2 class="section-heading">From Seedling to Market</h2>
    <div class="divider-leaf"></div>

    <div class="ops-grid">
      <div class="ops-card">
        <div class="big-icon">🗺️</div>
        <h3>Farm Planning & Design</h3>
        <p>We conduct soil analysis, climate assessments, and layout planning to match the right fruit crop to every unique parcel of land.</p>
      </div>
      <div class="ops-card">
        <div class="big-icon">🌱</div>
        <h3>Seedling Supply</h3>
        <p>Providing certified, disease-free planting material sourced from accredited nurseries to ensure every orchard starts strong.</p>
      </div>
      <div class="ops-card">
        <div class="big-icon">🎓</div>
        <h3>Farmer Training</h3>
        <p>Hands-on workshops covering pruning, fertilisation, pest control, irrigation, and post-harvest handling for maximum quality.</p>
      </div>
      <div class="ops-card">
        <div class="big-icon">💧</div>
        <h3>Irrigation Support</h3>
        <p>Advising on water-efficient drip systems that keep orchards productive through Kenya's dry seasons without wasteful use.</p>
      </div>
      <div class="ops-card">
        <div class="big-icon">🔗</div>
        <h3>Market Linkage</h3>
        <p>Connecting farmers to buyers, cooperatives, processors, and exporters — ensuring that effort at the farm translates to income in the pocket.</p>
      </div>
      <div class="ops-card">
        <div class="big-icon">📊</div>
        <h3>Monitoring & Evaluation</h3>
        <p>Regular on-farm visits and data collection to track growth, yields, and community impact across all our programme sites.</p>
      </div>
    </div>
  </div>
</section>

<!-- LOCATION BANNER -->
<div class="location-banner">
  <h2>Operating Across Eastern &amp; Central Africa</h2>
  <p>Headquartered in Wundanyi, Taita Taveta County, Kenya — expanding our reach across the region.</p>
  <div class="location-pills">
    <span class="pill">📍 Wundanyi HQ, Taita Taveta</span>
    <span class="pill">🌍 Eastern Africa Operations</span>
    <span class="pill">🌍 Central Africa Operations</span>
    <span class="pill">🤝 Open to New Partnerships</span>
  </div>
</div>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="contact-grid">
    <div class="contact-info">
      <div class="section-label">Reach Us</div>
      <h2>Let's Grow Together</h2>
      <div class="divider-leaf"></div>
      <p>
        Whether you are a farmer looking to start an orchard, an NGO seeking a local partner, or an investor interested in sustainable agriculture across Eastern and Central Africa — we want to hear from you.
      </p>
      <ul class="contact-list">
        <li>
          <div class="c-icon">📍</div>
          <div class="c-text">
            <strong>Headquarters</strong>
            <span>Wundanyi, Taita Taveta County, Kenya</span>
          </div>
        </li>
        <li>
          <div class="c-icon">📞</div>
          <div class="c-text">
            <strong>Phone</strong>
            <a href="tel:+254701930794">0701 930 794</a><br>
            <a href="tel:+254715883589">0715 883 589</a>
          </div>
        </li>
        <li>
          <div class="c-icon">✉️</div>
          <div class="c-text">
            <strong>Email</strong>
            <a href="mailto:elccon2020@gmail.com">elccon2020@gmail.com</a>
          </div>
        </li>
        <li>
          <div class="c-icon">🌍</div>
          <div class="c-text">
            <strong>Working Region</strong>
            <span>Eastern &amp; Central Africa</span>
          </div>
        </li>
      </ul>
    </div>

    <div class="contact-form-panel">
      <h3>Send Us a Message</h3>
      <div class="form-group">
        <label for="name">Full Name</label>
        <input type="text" id="name" placeholder="Your full name">
      </div>
      <div class="form-group">
        <label for="email">Email Address</label>
        <input type="email" id="email" placeholder="you@example.com">
      </div>
      <div class="form-group">
        <label for="subject">Area of Interest</label>
        <select id="subject">
          <option value="">Select one…</option>
          <option>Citrus Farm Establishment</option>
          <option>Avocado Farm Establishment</option>
          <option>Macadamia Farm Establishment</option>
          <option>Partnership / Collaboration</option>
          <option>Training & Capacity Building</option>
          <option>Market Linkage</option>
          <option>General Inquiry</option>
        </select>
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" placeholder="Tell us how we can help…"></textarea>
      </div>
      <button class="btn-submit" onclick="handleSubmit()">Send Message →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div>
      <div class="footer-brand">ELC<span>CON</span></div>
      <div class="footer-note">Environmental Life Change Community Organization Net</div>
      <div class="footer-note" style="margin-top:6px;">Wundanyi, Taita Taveta County, Kenya · Est. 2020</div>
    </div>
    <ul class="footer-links">
      <li><a href="#mission">Mission</a></li>
      <li><a href="#trees">Our Crops</a></li>
      <li><a href="#operations">Operations</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</footer>

<script>
  function handleSubmit() {
    const name    = document.getElementById('name').value.trim();
    const email   = document.getElementById('email').value.trim();
    const message = document.getElementById('message').value.trim();

    if (!name || !email || !message) {
      alert('Please fill in your name, email, and message before sending.');
      return;
    }
    alert('Thank you, ' + name + '! Your message has been received. We will get back to you at ' + email + ' shortly.\n\nYou can also reach us directly at elccon2020@gmail.com or call 0701 930 794 / 0715 883 589.');
  }

  // Smooth reveal on scroll
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.style.opacity = '1';
        e.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.mission-card, .tree-card, .ops-card').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(24px)';
    el.style.transition = 'opacity 0.55s ease, transform 0.55s ease';
    observer.observe(el);
  });
</script>

</body>
</html>
