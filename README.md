<!DOCTYPE html>
<html lang="kk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Қаныш Сәтбаев – Қазақтың тұңғыш академигі</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --gold:    #C9952A;
      --gold-lt: #E8B84B;
      --dark:    #0F1A14;
      --mid:     #1C2E22;
      --stone:   #2E4238;
      --cream:   #F5EDD8;
      --text:    #E8E0D0;
      --muted:   #9AA89F;
      --white:   #FFFFFF;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Source Sans 3', sans-serif;
      background: var(--dark);
      color: var(--text);
      font-size: 17px;
      line-height: 1.75;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; width: 100%; z-index: 999;
      background: rgba(15,26,20,0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(201,149,42,0.25);
      padding: 0 40px;
      display: flex; align-items: center; justify-content: space-between;
      height: 64px;
    }
    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem; color: var(--gold); font-weight: 700;
      letter-spacing: 0.02em; white-space: nowrap;
    }
    .nav-links { display: flex; gap: 28px; }
    .nav-links a {
      color: var(--muted); text-decoration: none;
      font-size: 0.88rem; font-weight: 600;
      letter-spacing: 0.08em; text-transform: uppercase;
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--gold); }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      padding: 80px 80px 60px;
      position: relative;
      overflow: hidden;
    }
    #hero::before {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(ellipse 60% 70% at 70% 50%, rgba(201,149,42,0.08) 0%, transparent 70%),
                  radial-gradient(ellipse 40% 60% at 30% 80%, rgba(46,66,56,0.6) 0%, transparent 60%);
      pointer-events: none;
    }
    .hero-text { position: relative; z-index: 2; }
    .hero-eyebrow {
      font-size: 0.78rem; letter-spacing: 0.18em;
      text-transform: uppercase; color: var(--gold);
      font-weight: 600; margin-bottom: 20px;
    }
    .hero-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.8rem, 5vw, 4.4rem);
      font-weight: 900; line-height: 1.08;
      color: var(--cream); margin-bottom: 28px;
    }
    .hero-title span { color: var(--gold); }
    .hero-desc {
      font-size: 1.1rem; color: var(--muted);
      max-width: 480px; margin-bottom: 40px; line-height: 1.8;
    }
    .hero-dates {
      display: flex; gap: 40px;
    }
    .hero-date-item { display: flex; flex-direction: column; }
    .hero-date-num {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem; font-weight: 700; color: var(--gold);
      line-height: 1;
    }
    .hero-date-label { font-size: 0.78rem; color: var(--muted); letter-spacing: 0.06em; text-transform: uppercase; }
    .hero-image-wrap {
      position: relative; z-index: 2;
      display: flex; justify-content: center; align-items: center;
    }
    .hero-portrait-frame {
      width: 380px; height: 480px;
      border: 2px solid rgba(201,149,42,0.4);
      position: relative;
      background: var(--mid);
      display: flex; align-items: center; justify-content: center;
      overflow: hidden;
    }
    .hero-portrait-frame::before {
      content: '';
      position: absolute; top: 12px; left: 12px;
      right: -12px; bottom: -12px;
      border: 2px solid rgba(201,149,42,0.18);
      z-index: 0;
    }
    .portrait-placeholder {
      width: 100%; height: 100%;
      background: linear-gradient(160deg, #1C2E22 0%, #0F1A14 60%, #2E4238 100%);
      display: flex; flex-direction: column;
      align-items: center; justify-content: center; gap: 16px;
      position: relative;
    }
    .portrait-silhouette {
      width: 120px; height: 120px;
      border-radius: 50%;
      background: rgba(201,149,42,0.15);
      border: 2px solid rgba(201,149,42,0.3);
      display: flex; align-items: center; justify-content: center;
      font-size: 3rem;
    }
    .portrait-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; color: var(--gold); font-weight: 700;
      text-align: center; padding: 0 20px;
    }
    .portrait-years { font-size: 0.9rem; color: var(--muted); }

    /* ── SECTION BASE ── */
    section { padding: 100px 80px; }
    .section-inner { max-width: 1100px; margin: 0 auto; }
    .section-eyebrow {
      font-size: 0.75rem; letter-spacing: 0.2em;
      text-transform: uppercase; color: var(--gold);
      font-weight: 600; margin-bottom: 16px;
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2rem, 3.5vw, 3rem);
      font-weight: 700; color: var(--cream);
      margin-bottom: 50px; line-height: 1.2;
    }
    .gold-line {
      width: 60px; height: 3px;
      background: var(--gold); margin-bottom: 50px;
    }

    /* ── BIOGRAPHY ── */
    #biography { background: var(--mid); }
    .bio-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: 60px;
      align-items: start;
    }
    .bio-timeline { display: flex; flex-direction: column; gap: 0; }
    .bio-item {
      display: flex; gap: 20px; padding-bottom: 32px;
      position: relative;
    }
    .bio-item::before {
      content: '';
      position: absolute; left: 35px; top: 40px;
      width: 1px; height: calc(100% - 8px);
      background: linear-gradient(to bottom, rgba(201,149,42,0.5), rgba(201,149,42,0.05));
    }
    .bio-item:last-child::before { display: none; }
    .bio-year {
      min-width: 70px; font-family: 'Playfair Display', serif;
      font-size: 1rem; font-weight: 700; color: var(--gold);
      padding-top: 2px;
    }
    .bio-dot {
      width: 12px; height: 12px; border-radius: 50%;
      border: 2px solid var(--gold); background: var(--dark);
      margin-top: 6px; flex-shrink: 0; z-index: 1;
    }
    .bio-content h4 {
      font-family: 'Playfair Display', serif;
      font-size: 1rem; font-weight: 700; color: var(--cream);
      margin-bottom: 4px;
    }
    .bio-content p { font-size: 0.9rem; color: var(--muted); }
    .bio-info-box {
      background: var(--stone);
      border-left: 3px solid var(--gold);
      padding: 32px;
      border-radius: 2px;
    }
    .bio-info-box h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.4rem; color: var(--cream);
      margin-bottom: 24px;
    }
    .bio-fact { display: flex; flex-direction: column; margin-bottom: 18px; }
    .bio-fact-label { font-size: 0.75rem; color: var(--gold); text-transform: uppercase; letter-spacing: 0.1em; }
    .bio-fact-value { font-size: 0.95rem; color: var(--text); }

    /* ── WORKS ── */
    #works { background: var(--dark); }
    .works-grid {
      display: grid; grid-template-columns: repeat(3, 1fr); gap: 28px;
    }
    .work-card {
      background: var(--mid);
      border: 1px solid rgba(201,149,42,0.15);
      padding: 32px;
      transition: border-color .3s, transform .3s;
      position: relative; overflow: hidden;
    }
    .work-card::after {
      content: '';
      position: absolute; top: 0; left: 0;
      width: 3px; height: 0;
      background: var(--gold);
      transition: height .3s;
    }
    .work-card:hover { border-color: rgba(201,149,42,0.4); transform: translateY(-4px); }
    .work-card:hover::after { height: 100%; }
    .work-icon { font-size: 2rem; margin-bottom: 16px; }
    .work-card h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem; color: var(--cream); margin-bottom: 12px;
    }
    .work-card p { font-size: 0.9rem; color: var(--muted); line-height: 1.7; }

    /* ── CONTRIBUTION ── */
    #contribution { background: var(--stone); }
    .contrib-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: 50px;
    }
    .contrib-block h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; color: var(--cream); margin-bottom: 16px;
      padding-bottom: 12px; border-bottom: 1px solid rgba(201,149,42,0.25);
    }
    .contrib-list { list-style: none; display: flex; flex-direction: column; gap: 10px; }
    .contrib-list li {
      display: flex; gap: 12px; align-items: flex-start;
      font-size: 0.95rem; color: var(--text);
    }
    .contrib-list li::before {
      content: '◆'; color: var(--gold); font-size: 0.55rem;
      margin-top: 7px; flex-shrink: 0;
    }

    /* ── QUOTE ── */
    #quote {
      background: var(--mid);
      padding: 80px;
      text-align: center;
    }
    .quote-mark {
      font-family: 'Playfair Display', serif;
      font-size: 8rem; line-height: 0.5;
      color: rgba(201,149,42,0.25);
      margin-bottom: 20px;
    }
    .quote-text {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.3rem, 2.5vw, 1.9rem);
      color: var(--cream); max-width: 800px;
      margin: 0 auto 24px; line-height: 1.55;
      font-style: italic;
    }
    .quote-author { font-size: 0.85rem; color: var(--gold); letter-spacing: 0.12em; text-transform: uppercase; }

    /* ── GALLERY / FACTS ── */
    #gallery { background: var(--dark); }
    .facts-grid {
      display: grid; grid-template-columns: repeat(4, 1fr); gap: 24px;
      margin-bottom: 60px;
    }
    .fact-card {
      background: var(--mid);
      border-top: 3px solid var(--gold);
      padding: 28px 24px; text-align: center;
    }
    .fact-num {
      font-family: 'Playfair Display', serif;
      font-size: 2.8rem; font-weight: 900;
      color: var(--gold); line-height: 1;
    }
    .fact-label { font-size: 0.85rem; color: var(--muted); margin-top: 8px; }
    .gallery-quotes { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 24px; }
    .gallery-quote-card {
      background: var(--stone);
      border: 1px solid rgba(201,149,42,0.2);
      padding: 28px;
    }
    .gallery-quote-card p { font-size: 0.92rem; color: var(--text); font-style: italic; line-height: 1.7; margin-bottom: 12px; }
    .gallery-quote-card span { font-size: 0.78rem; color: var(--gold); text-transform: uppercase; letter-spacing: 0.08em; }

    /* ── REFERENCES ── */
    #references { background: var(--mid); }
    .ref-list { list-style: decimal; padding-left: 24px; display: flex; flex-direction: column; gap: 12px; }
    .ref-list li { font-size: 0.92rem; color: var(--muted); }
    .ref-list li span { color: var(--text); }

    /* ── CONTACT ── */
    #contact { background: var(--dark); }
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; }
    .contact-info h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem; color: var(--cream); margin-bottom: 20px;
    }
    .contact-info p { color: var(--muted); line-height: 1.8; margin-bottom: 16px; }
    .contact-form { display: flex; flex-direction: column; gap: 16px; }
    .form-group { display: flex; flex-direction: column; gap: 6px; }
    .form-group label { font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.1em; color: var(--gold); }
    .form-group input, .form-group textarea {
      background: var(--mid);
      border: 1px solid rgba(201,149,42,0.25);
      color: var(--text); font-family: 'Source Sans 3', sans-serif;
      font-size: 0.95rem; padding: 14px 16px;
      border-radius: 2px; outline: none;
      transition: border-color .2s;
    }
    .form-group input:focus, .form-group textarea:focus { border-color: var(--gold); }
    .form-group textarea { height: 120px; resize: vertical; }
    .btn-submit {
      background: var(--gold); color: var(--dark);
      border: none; padding: 16px 40px;
      font-family: 'Source Sans 3', sans-serif;
      font-size: 0.85rem; font-weight: 700;
      letter-spacing: 0.1em; text-transform: uppercase;
      cursor: pointer; transition: background .2s; align-self: flex-start;
      border-radius: 2px;
    }
    .btn-submit:hover { background: var(--gold-lt); }

    /* ── FOOTER ── */
    footer {
      background: #07100B;
      padding: 40px 80px;
      display: flex; align-items: center; justify-content: space-between;
      border-top: 1px solid rgba(201,149,42,0.15);
    }
    .footer-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem; color: var(--gold); font-weight: 700;
    }
    .footer-text { font-size: 0.82rem; color: var(--muted); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      nav { padding: 0 20px; }
      .nav-links { gap: 14px; }
      #hero { grid-template-columns: 1fr; padding: 100px 24px 60px; }
      .hero-image-wrap { display: none; }
      section { padding: 70px 24px; }
      #quote { padding: 60px 24px; }
      footer { padding: 30px 24px; flex-direction: column; gap: 10px; text-align: center; }
      .bio-grid, .contrib-grid, .contact-grid { grid-template-columns: 1fr; }
      .works-grid { grid-template-columns: 1fr 1fr; }
      .facts-grid { grid-template-columns: 1fr 1fr; }
      .gallery-quotes { grid-template-columns: 1fr; }
    }
    @media (max-width: 600px) {
      .works-grid { grid-template-columns: 1fr; }
      .nav-links { display: none; }
      .facts-grid { grid-template-columns: 1fr 1fr; }
    }
  </style>
</head>
<body>

<!-- ── NAV ── -->
<nav>
  <div class="nav-logo">Қ. Сәтбаев</div>
  <div class="nav-links">
    <a href="#hero">Басты бет</a>
    <a href="#biography">Өмірбаяны</a>
    <a href="#works">Еңбектері</a>
    <a href="#contribution">Үлесі</a>
    <a href="#gallery">Галерея</a>
    <a href="#contact">Байланыс</a>
  </div>
</nav>

<!-- ── HERO ── -->
<section id="hero">
  <div class="hero-text">
    <p class="hero-eyebrow">Қазақтың тұңғыш академигі</p>
    <h1 class="hero-title">
      Қаныш<br/>
      <span>Имантайұлы</span><br/>
      Сәтбаев
    </h1>
    <p class="hero-desc">
      Ұлы геолог, ғалым, мемлекет қайраткері. Қазақстанның пайдалы қазбалар қорын зерттеп, Қарсақпай мыс кенін ашқан, Қазақ ССР Ғылым академиясының тұңғыш президенті.
    </p>
    <div class="hero-dates">
      <div class="hero-date-item">
        <span class="hero-date-num">1899</span>
        <span class="hero-date-label">Туған жылы</span>
      </div>
      <div class="hero-date-item">
        <span class="hero-date-num">1964</span>
        <span class="hero-date-label">Қайтыс болған жыл</span>
      </div>
      <div class="hero-date-item">
        <span class="hero-date-num">1946</span>
        <span class="hero-date-label">Академия президенті</span>
      </div>
    </div>
  </div>
  <div class="hero-image-wrap">
    <div class="hero-portrait-frame">
      <div class="portrait-placeholder">
        <div class="portrait-silhouette">🎓</div>
        <p class="portrait-name">Қаныш Сәтбаев</p>
        <p class="portrait-years">1899 – 1964</p>
      </div>
    </div>
  </div>
</section>

<!-- ── BIOGRAPHY ── -->
<section id="biography">
  <div class="section-inner">
    <p class="section-eyebrow">Өмір жолы</p>
    <h2 class="section-title">Өмірбаяны</h2>
    <div class="bio-grid">
      <div class="bio-timeline">
        <div class="bio-item">
          <span class="bio-year">1899</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Туылуы</h4>
            <p>Ақмола облысы, Баянауыл уезі, Найзатас ауылында дүниеге келді.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1918</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Павлодар оқытушылар семинариясы</h4>
            <p>Алғашқы кәсіби білімін Павлодар қаласындағы семинарияда алды.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1921</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Томск технологиялық институты</h4>
            <p>Тау-кен факультетіне түсіп, геология мамандығын таңдады.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1926</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Геологиялық зерттеулер басталуы</h4>
            <p>Жезқазған кен орнын жан-жақты зерттеп, оның алып қорын дәлелдеді.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1942</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Академик атағы</h4>
            <p>СССР Ғылым академиясының корреспондент-мүшесі болып сайланды.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1946</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>ҚазССР ҒА Президенті</h4>
            <p>Қазақ ССР Ғылым академиясының тұңғыш президенті болып тағайындалды.</p>
          </div>
        </div>
        <div class="bio-item">
          <span class="bio-year">1964</span>
          <div class="bio-dot"></div>
          <div class="bio-content">
            <h4>Мәңгілік ел</h4>
            <p>31 қаңтарда Мәскеу қаласында дүние салды. 65 жасында.</p>
          </div>
        </div>
      </div>
      <div class="bio-info-box">
        <h3>Жалпы мәліметтер</h3>
        <div class="bio-fact">
          <span class="bio-fact-label">Толық аты-жөні</span>
          <span class="bio-fact-value">Қаныш Имантайұлы Сәтбаев</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Туған күні</span>
          <span class="bio-fact-value">12 сәуір 1899 жыл</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Туған жері</span>
          <span class="bio-fact-value">Найзатас ауылы, Баянауыл уезі, Ақмола облысы</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Ұлты</span>
          <span class="bio-fact-value">Қазақ</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Білімі</span>
          <span class="bio-fact-value">Томск технологиялық институты, тау-кен факультеті</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Мамандығы</span>
          <span class="bio-fact-value">Геолог, ғалым, қоғам қайраткері</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Атақтары</span>
          <span class="bio-fact-value">Академик, СССР ҒА-ның корреспондент-мүшесі, Ленин сыйлығының лауреаты</span>
        </div>
        <div class="bio-fact">
          <span class="bio-fact-label">Қайтыс болған күні</span>
          <span class="bio-fact-value">31 қаңтар 1964 жыл, Мәскеу</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── WORKS ── -->
<section id="works">
  <div class="section-inner">
    <p class="section-eyebrow">Ғылыми мұрасы</p>
    <h2 class="section-title">Шығармашылығы & Еңбектері</h2>
    <div class="works-grid">
      <div class="work-card">
        <div class="work-icon">⛏</div>
        <h3>Жезқазған кен орны</h3>
        <p>Жезқазған мыс кен орнының орасан зор қорын ғылыми тұрғыда дәлелдеп, оны өнеркәсіптік тұрғыда игеруге жол ашты. Бұл — оның ең ірі ғылыми жетістігі.</p>
      </div>
      <div class="work-card">
        <div class="work-icon">🗺</div>
        <h3>Металлогениялық карта</h3>
        <p>Қазақстан аумағының металлогениялық картасын жасады — пайдалы қазбалардың орналасуын болжайтын ғылыми негізгі құжат.</p>
      </div>
      <div class="work-card">
        <div class="work-icon">📚</div>
        <h3>Ғылыми еңбектер</h3>
        <p>300-ден астам ғылыми мақала, монография және зерттеу еңбектерін жазды. Геология, тектоника, металлогения саласында іргелі еңбектер қалдырды.</p>
      </div>
      <div class="work-card">
        <div class="work-icon">🔬</div>
        <h3>Зерттеу экспедициялары</h3>
        <p>Балқаш, Қарағанды, Жезқазған, Маңғыстау аймақтарын зерттеген ондаған геологиялық экспедицияларды ұйымдастырды және жетекшілік жасады.</p>
      </div>
      <div class="work-card">
        <div class="work-icon">🏛</div>
        <h3>Академия ұйымдастыру</h3>
        <p>1946 жылы Қазақ ССР Ғылым академиясын ұйымдастырып, оның тұңғыш президенті болды. Академияның іргесін қалаудағы басты тұлға.</p>
      </div>
      <div class="work-card">
        <div class="work-icon">✍️</div>
        <h3>Абай туралы зерттеу</h3>
        <p>Ұлы ақын Абай Құнанбайұлының өмірі мен шығармашылығын зерттеп, оның ғылыми-биографиялық деректерін жинаққа айналдырды.</p>
      </div>
    </div>
  </div>
</section>

<!-- ── QUOTE ── -->
<section id="quote" style="padding:80px;">
  <div class="quote-mark">"</div>
  <p class="quote-text">
    Жер қойнауы — халықтың байлығы. Оны зерттеп, болашақ ұрпаққа жеткізу — ғалымның парызы.
  </p>
  <p class="quote-author">— Қаныш Имантайұлы Сәтбаев</p>
</section>

<!-- ── CONTRIBUTION ── -->
<section id="contribution">
  <div class="section-inner">
    <p class="section-eyebrow">Тарихи маңыздылығы</p>
    <h2 class="section-title">Қазақ қоғамына қосқан үлесі</h2>
    <div class="contrib-grid">
      <div class="contrib-block">
        <h3>🔬 Ғылымға қосқан үлесі</h3>
        <ul class="contrib-list">
          <li>Қазақстандағы геология ғылымының негізін қалады</li>
          <li>Металлогениялық болжам әдісін ғылымға енгізді</li>
          <li>Жезқазған кен орнының мыс қорын дәлелдеді</li>
          <li>300-ден астам ғылыми еңбек жазып қалдырды</li>
          <li>Қазақ ССР Ғылым академиясын 1946 жылы ашты</li>
          <li>Геология, тектоника, металлогения ғылымдарын дамытты</li>
        </ul>
      </div>
      <div class="contrib-block">
        <h3>🏗 Өнеркәсіп пен экономикаға үлесі</h3>
        <ul class="contrib-list">
          <li>Жезқазған — дүниежүзілік маңызды мыс өндіру орталығына айналды</li>
          <li>Балқаш мыс балқыту зауытының салынуына ғылыми негіз берді</li>
          <li>Қарсақпай кен комбинатының іске қосылуына ықпал жасады</li>
          <li>Соғыс жылдарында стратегиялық металдар қорын айқындады</li>
          <li>Қазақстанның индустриалды дамуына ғылыми үлес қосты</li>
        </ul>
      </div>
      <div class="contrib-block">
        <h3>🎓 Ағартушылық қызметі</h3>
        <ul class="contrib-list">
          <li>Қазақстандағы жоғары ғылыми мектептің негізін қалады</li>
          <li>Жүздеген қазақ ғалымдарын тәрбиеледі</li>
          <li>Ғылыми мекемелер мен зертханалар желісін ашты</li>
          <li>Ғылыми кадрлар дайындауға ерекше мән берді</li>
          <li>Халыққа білім таратуды мемлекеттік деңгейде қолдады</li>
        </ul>
      </div>
      <div class="contrib-block">
        <h3>🌟 Тарихи рөлі</h3>
        <ul class="contrib-list">
          <li>Қазақтың тұңғыш академигі атанды</li>
          <li>Ленин сыйлығының лауреаты (1958)</li>
          <li>Үш рет Еңбек Қызыл Ту орденімен марапатталды</li>
          <li>Атымен университет, қала, жота, ғарыш кемесі аталды</li>
          <li>Ұлттық ғылым мен мемлекеттіліктің символына айналды</li>
          <li>Абай мен Сәтбаев — екі рухани тірек ретінде мойындалды</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ── GALLERY & FACTS ── -->
<section id="gallery">
  <div class="section-inner">
    <p class="section-eyebrow">Қызықты деректер & Дәйексөздер</p>
    <h2 class="section-title">Галерея & Деректер</h2>

    <div class="facts-grid">
      <div class="fact-card">
        <div class="fact-num">300+</div>
        <div class="fact-label">Ғылыми еңбек</div>
      </div>
      <div class="fact-card">
        <div class="fact-num">18</div>
        <div class="fact-label">Жыл — Академия президенті</div>
      </div>
      <div class="fact-card">
        <div class="fact-num">1946</div>
        <div class="fact-label">ҚазССР ҒА ашылды</div>
      </div>
      <div class="fact-card">
        <div class="fact-num">№ 1</div>
        <div class="fact-label">Қазақ академигі</div>
      </div>
    </div>

    <div class="gallery-quotes">
      <div class="gallery-quote-card">
        <p>«Ғылым — адамзаттың жарығы. Ол болмаса, адам малдан не артық?»</p>
        <span>— Қ. Сәтбаев</span>
      </div>
      <div class="gallery-quote-card">
        <p>«Жезқазған кен орны — тек Қазақстанның емес, бүкіл адамзаттың байлығы.»</p>
        <span>— Қ. Сәтбаев, геологиялық есеп, 1931</span>
      </div>
      <div class="gallery-quote-card">
        <p>«Ұлтының ғалымы болу — ең үлкен абырой. Мен қазақ деп мақтанамын.»</p>
        <span>— Қ. Сәтбаев</span>
      </div>
    </div>
  </div>
</section>

<!-- ── REFERENCES ── -->
<section id="references">
  <div class="section-inner">
    <p class="section-eyebrow">Дереккөздер</p>
    <h2 class="section-title">Пайдаланылған әдебиеттер</h2>
    <ol class="ref-list">
      <li><span>Байжанов Б. «Қаныш Сәтбаев: ғалым және тұлға.»</span> — Алматы: Ғылым, 1999.</li>
      <li><span>Сәтбаев Қ. И. «Жезқазған мыс кен орны.»</span> — Мәскеу: АН СССР, 1941.</li>
      <li><span>Қазақ Совет Энциклопедиясы.</span> — 9-том. Алматы, 1976.</li>
      <li><span>Нысанбаев Ә. «Қазақстан философиясының тарихы.»</span> — Алматы, 2001.</li>
      <li><span>Масанов Н. «Кочевая цивилизация казахов.»</span> — Алматы: Социнвест, 1995.</li>
      <li><span>ҚР Ұлттық архиві. Сәтбаевқа қатысты қорлар.</span> — Қор №369.</li>
      <li><span>Сәтбаев Қ. И. Таңдамалы шығармалар жинағы. 5 томдық.</span> — Алматы: Ғылым, 1978–1982.</li>
      <li><span>Жақсыбеков А. «Академик Сәтбаев туралы естеліктер.»</span> — Алматы, 2005.</li>
    </ol>
  </div>
</section>

<!-- ── CONTACT ── -->
<section id="contact">
  <div class="section-inner">
    <p class="section-eyebrow">Хабарласу</p>
    <h2 class="section-title">Байланыс</h2>
    <div class="contact-grid">
      <div class="contact-info">
        <h3>Сайт туралы</h3>
        <p>
          Бұл сайт Қаныш Имантайұлы Сәтбаевтың өмірі мен ғылыми мұрасын насихаттау мақсатында жасалған оқу жобасы болып табылады.
        </p>
        <p>
          Сайттағы ақпарат тарихи деректерге, ғылыми архивтерге және Қазақстан Ұлттық энциклопедиясына негізделген.
        </p>
        <p>
          Тарихи тұлғалар туралы білімді арттыруда осы ресурс пайдалы болады деп үміттенеміз.
        </p>
      </div>
      <div class="contact-form">
        <div class="form-group">
          <label>Атыңыз</label>
          <input type="text" placeholder="Толық атыңызды жазыңыз"/>
        </div>
        <div class="form-group">
          <label>Электрондық пошта</label>
          <input type="email" placeholder="email@example.com"/>
        </div>
        <div class="form-group">
          <label>Хабарлама</label>
          <textarea placeholder="Пікіріңізді немесе сұрақтарыңызды жазыңыз..."></textarea>
        </div>
        <button class="btn-submit" onclick="alert('Хабарламаңыз жіберілді! Рақмет!')">Жіберу</button>
      </div>
    </div>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <div class="footer-logo">Қаныш Сәтбаев — 1899–1964</div>
  <p class="footer-text">Қазақтың тұңғыш академигі. Ұлт мақтанышы.</p>
</footer>

</body>
</html>
