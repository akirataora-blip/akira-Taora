<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <title>Portfolio VAKIMA – Étudiante M1 & Freelance</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- SEO de base -->
  <meta name="description" content="Portfolio de VAKIMA : étudiante en M1 à Burgundy School of Business et freelance, créatrice de cadeaux personnalisés et prestataire de services événementiels, restauration et logistique." />
  <meta name="keywords" content="VAKIMA, portfolio, freelance, cadeaux personnalisés, événementiel, restauration, logistique, Burgundy School of Business" />
  <meta name="author" content="VAKIMA" />

  <!-- Typographies Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;600;700&family=Lato:wght@300;400;500;700&display=swap" rel="stylesheet" />

  <style>
    /* ========= VARIABLES & RESET ========= */
    :root {
      --color-primary: #1E3A5F;   /* bleu profond */
      --color-bg: #F5F0E6;        /* beige/crème */
      --color-accent: #7A2E3A;    /* bordeaux */
      --color-text-main: #1E3A5F;
      --color-text-secondary: #6C757D;
      --color-white: #ffffff;
      --shadow-soft: 0 10px 30px rgba(0,0,0,0.08);
      --radius-large: 18px;
      --radius-medium: 12px;
      --radius-small: 8px;
      --transition-fast: 0.2s ease;
      --max-width: 1100px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Lato', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background-color: var(--color-bg);
      color: var(--color-text-main);
      line-height: 1.6;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    ul {
      list-style: none;
    }

    /* ========= LAYOUT GLOBAL ========= */
    .wrapper {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem 3rem;
    }

    section {
      padding: 5rem 0 3rem;
    }

    section:nth-of-type(odd) .section-card {
      background-color: var(--color-white);
    }

    .section-card {
      background-color: #FBF8F2;
      border-radius: var(--radius-large);
      padding: 3rem 2rem;
      box-shadow: var(--shadow-soft);
    }

    .section-header {
      margin-bottom: 2rem;
    }

    .section-kicker {
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-size: 0.8rem;
      color: var(--color-accent);
      font-weight: 600;
    }

    .section-title {
      font-family: 'Montserrat', system-ui, sans-serif;
      font-size: 1.9rem;
      margin-top: 0.4rem;
      margin-bottom: 0.6rem;
    }

    .section-subtitle {
      color: var(--color-text-secondary);
      font-size: 0.97rem;
      max-width: 600px;
    }

    /* ========= NAVIGATION ========= */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(16px);
      background-color: rgba(245,240,230,0.92);
      box-shadow: 0 1px 0 rgba(0,0,0,0.04);
    }

    .nav {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0.6rem 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
    }

    .nav-brand {
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .nav-logo-circle {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--color-white);
      font-weight: 700;
      font-size: 0.9rem;
    }

    .nav-brand-text {
      font-family: 'Montserrat', system-ui, sans-serif;
      font-weight: 600;
      font-size: 1rem;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.6rem;
      font-size: 0.93rem;
    }

    .nav-links a {
      position: relative;
      padding-bottom: 0.2rem;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 0;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(90deg, var(--color-primary), var(--color-accent));
      transition: width var(--transition-fast);
    }

    .nav-links a:hover::after,
    .nav-links a.active::after {
      width: 100%;
    }

    .nav-cta {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      padding: 0.45rem 1.1rem;
      font-size: 0.9rem;
      border: none;
      cursor: pointer;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), background-color var(--transition-fast), color var(--transition-fast);
      font-weight: 500;
      font-family: inherit;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
      color: var(--color-white);
      box-shadow: 0 10px 25px rgba(30,58,95,0.25);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 14px 30px rgba(30,58,95,0.28);
    }

    .btn-secondary {
      background-color: var(--color-white);
      color: var(--color-primary);
      border: 1px solid rgba(0,0,0,0.06);
    }

    .btn-secondary:hover {
      background-color: #fdfaf4;
    }

    /* Burger */
    .nav-burger {
      display: none;
      width: 32px;
      height: 32px;
      border-radius: 999px;
      border: 1px solid rgba(0,0,0,0.06);
      background-color: var(--color-white);
      align-items: center;
      justify-content: center;
      cursor: pointer;
    }

    .nav-burger-lines {
      width: 18px;
      height: 2px;
      background-color: var(--color-primary);
      position: relative;
      transition: transform 0.25s ease, background-color 0.25s ease;
    }

    .nav-burger-lines::before,
    .nav-burger-lines::after {
      content: "";
      position: absolute;
      left: 0;
      width: 18px;
      height: 2px;
      background-color: var(--color-primary);
      transition: transform 0.25s ease, opacity 0.2s ease;
    }

    .nav-burger-lines::before {
      top: -6px;
    }

    .nav-burger-lines::after {
      top: 6px;
    }

    .nav-burger.active .nav-burger-lines {
      transform: rotate(45deg);
    }

    .nav-burger.active .nav-burger-lines::before {
      transform: rotate(-90deg) translateX(-6px);
    }

    .nav-burger.active .nav-burger-lines::after {
      opacity: 0;
    }

    .nav-links-mobile {
      display: none;
    }

    /* ========= HERO / ACCUEIL ========= */
    #accueil {
      padding-top: 5rem;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1.1fr);
      gap: 2.5rem;
      align-items: center;
    }

    .hero-text-kicker {
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-size: 0.78rem;
      color: var(--color-accent);
      font-weight: 600;
      margin-bottom: 0.7rem;
    }

    .hero-title {
      font-family: 'Montserrat', system-ui, sans-serif;
      font-size: clamp(1.9rem, 3vw, 2.4rem);
      margin-bottom: 0.6rem;
    }

    .hero-tagline {
      font-size: 1.05rem;
      color: var(--color-text-secondary);
      margin-bottom: 1.5rem;
    }

    .hero-intro {
      font-size: 0.98rem;
      margin-bottom: 1.8rem;
      color: var(--color-text-secondary);
    }

    .hero-cta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      align-items: center;
      margin-bottom: 1.4rem;
    }

    .hero-meta {
      font-size: 0.9rem;
      color: var(--color-text-secondary);
    }

    .hero-photo-wrapper {
      position: relative;
      justify-self: center;
    }

    .hero-photo {
      width: min(270px, 70vw);
      border-radius: 26px;
      object-fit: cover;
      box-shadow: 0 18px 45px rgba(0,0,0,0.18);
      border: 4px solid var(--color-white);
      background-color: #d7dde8;
    }

    .hero-pill {
      position: absolute;
      left: -16px;
      top: 14%;
      background-color: var(--color-white);
      padding: 0.55rem 0.9rem;
      font-size: 0.8rem;
      border-radius: 999px;
      box-shadow: var(--shadow-soft);
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .hero-pill-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
    }

    .hero-pill-bottom {
      position: absolute;
      right: -18px;
      bottom: 12%;
      background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
      color: var(--color-white);
      padding: 0.5rem 1rem;
      border-radius: 16px;
      font-size: 0.8rem;
      box-shadow: var(--shadow-soft);
    }

    /* ========= À PROPOS ========= */
    .about-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1.1fr);
      gap: 2rem;
    }

    .about-values {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin: 1rem 0 1.7rem;
    }

    .chip {
      font-size: 0.8rem;
      padding: 0.35rem 0.8rem;
      border-radius: 999px;
      background-color: #f1e5dd;
      color: var(--color-accent);
      font-weight: 500;
    }

    .about-timeline {
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
      margin-top: 1rem;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: auto minmax(0, 1fr);
      column-gap: 1rem;
      align-items: flex-start;
    }

    .timeline-marker {
      width: 16px;
      height: 16px;
      border-radius: 999px;
      border: 3px solid var(--color-primary);
      margin-top: 2px;
      position: relative;
    }

    .timeline-marker::after {
      content: "";
      position: absolute;
      left: 50%;
      top: 16px;
      transform: translateX(-50%);
      width: 2px;
      height: 28px;
      background: linear-gradient(to bottom, var(--color-primary), transparent);
    }

    .timeline-item:last-child .timeline-marker::after {
      display: none;
    }

    .timeline-title-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      align-items: baseline;
    }

    .timeline-role {
      font-weight: 600;
      font-size: 0.98rem;
    }

    .timeline-org {
      font-size: 0.92rem;
      color: var(--color-text-secondary);
    }

    .timeline-desc {
      font-size: 0.88rem;
      color: var(--color-text-secondary);
      margin-top: 0.25rem;
    }

    .about-skills {
      margin-top: 1.8rem;
    }

    .about-skills-list {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .skill-tag {
      font-size: 0.8rem;
      padding: 0.35rem 0.8rem;
      border-radius: 999px;
      background-color: #e3ebf7;
      color: var(--color-primary);
      font-weight: 500;
    }

    /* ========= PROJETS ========= */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.6rem;
    }

    .project-card {
      background-color: var(--color-white);
      border-radius: var(--radius-medium);
      padding: 1.4rem 1.3rem;
      box-shadow: var(--shadow-soft);
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
    }

    .project-label {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--color-accent);
      font-weight: 600;
    }

    .project-title {
      font-family: 'Montserrat', system-ui, sans-serif;
      font-size: 1.05rem;
    }

    .project-meta {
      font-size: 0.85rem;
      color: var(--color-text-secondary);
    }

    .project-role {
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--color-primary);
    }

    .project-desc {
      font-size: 0.9rem;
      color: var(--color-text-secondary);
    }

    .project-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-top: 0.2rem;
    }

    .project-badge {
      font-size: 0.78rem;
      padding: 0.23rem 0.6rem;
      border-radius: 999px;
      background-color: #f1e5dd;
      color: var(--color-accent);
    }

    .project-media-placeholder {
      margin-top: 0.6rem;
      font-size: 0.8rem;
      color: var(--color-text-secondary);
      padding: 0.6rem 0.75rem;
      border-radius: var(--radius-small);
      border: 1px dashed rgba(0,0,0,0.12);
      background-color: #fdfaf6;
    }

    /* ========= VAKIMA ========= */
    .vakima-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1.1fr);
      gap: 2rem;
      align-items: flex-start;
    }

    .vakima-pill {
      font-size: 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.35rem 0.8rem;
      border-radius: 999px;
      background-color: #e3ebf7;
      color: var(--color-primary);
      margin-bottom: 0.8rem;
    }

    .vakima-columns {
      display: grid;
      grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
      gap: 1.3rem;
      margin-top: 1.4rem;
    }

    .vakima-column-card {
      background-color: #fdfaf4;
      border-radius: var(--radius-medium);
      padding: 1.1rem 1rem;
      border: 1px solid rgba(0,0,0,0.03);
    }

    .vakima-column-title {
      font-size: 0.98rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .vakima-list {
      font-size: 0.88rem;
      color: var(--color-text-secondary);
      padding-left: 1.1rem;
      margin-top: 0.3rem;
    }

    .vakima-list li {
      margin-bottom: 0.18rem;
      list-style: disc;
    }

    .vakima-advantages {
      margin-top: 1.4rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .vakima-adv-chip {
      font-size: 0.8rem;
      padding: 0.35rem 0.8rem;
      border-radius: 999px;
      background-color: #e8f3ff;
      color: var(--color-primary);
      font-weight: 500;
    }

    .vakima-gallery {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.7rem;
      margin-top: 0.8rem;
    }

    .vakima-photo {
      border-radius: 14px;
      background-color: #d7dde8;
      height: 120px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8rem;
      color: var(--color-text-secondary);
    }

    .vakima-cta {
      margin-top: 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
    }

    /* ========= CONTACT ========= */
    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 2rem;
    }

    .contact-info-list {
      display: flex;
      flex-direction: column;
      gap: 0.9rem;
      font-size: 0.9rem;
      color: var(--color-text-secondary);
    }

    .contact-info-item span {
      font-weight: 600;
      color: var(--color-primary);
    }

    .contact-socials {
      margin-top: 1.2rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      font-size: 0.86rem;
    }

    .contact-social-pill {
      padding: 0.35rem 0.8rem;
      border-radius: 999px;
      background-color: #f1e5dd;
      color: var(--color-accent);
      cursor: pointer;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 0.8rem;
    }

    label {
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--color-primary);
      margin-bottom: 0.15rem;
    }

    input[type="text"],
    input[type="email"],
    textarea {
      width: 100%;
      border-radius: 10px;
      border: 1px solid rgba(0,0,0,0.12);
      padding: 0.6rem 0.7rem;
      font-size: 0.9rem;
      font-family: inherit;
      outline: none;
      background-color: #fdfaf4;
      transition: border-color var(--transition-fast), box-shadow var(--transition-fast), background-color var(--transition-fast);
      resize: vertical;
      min-height: 38px;
    }

    input[type="text"]:focus,
    input[type="email"]:focus,
    textarea:focus {
      border-color: var(--color-primary);
      box-shadow: 0 0 0 1px rgba(30,58,95,0.09);
      background-color: #ffffff;
    }

    textarea {
      min-height: 120px;
    }

    .contact-small {
      font-size: 0.8rem;
      color: var(--color-text-secondary);
    }

    .form-status {
      font-size: 0.83rem;
      margin-top: 0.4rem;
    }

    .form-status.success {
      color: #1b7f3b;
    }

    .form-status.error {
      color: var(--color-accent);
    }

    /* ========= FOOTER ========= */
    footer {
      padding: 1.5rem 0 0.8rem;
      font-size: 0.78rem;
      color: var(--color-text-secondary);
    }

    .footer-inner {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      justify-content: space-between;
      align-items: center;
    }

    /* ========= ANIMATIONS LÉGÈRES ========= */
    .fade-in {
      opacity: 0;
      transform: translateY(12px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ========= RESPONSIVE ========= */
    @media (max-width: 900px) {
      .hero,
      .about-grid,
      .vakima-grid,
      .contact-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-photo-wrapper {
        order: -1;
      }

      .vakima-columns {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    @media (max-width: 768px) {
      .nav-links,
      .nav-cta {
        display: none;
      }

      .nav-burger {
        display: inline-flex;
      }

      .nav-links-mobile {
        display: none;
        flex-direction: column;
        gap: 0.6rem;
        padding: 0.8rem 1.5rem 1.1rem;
        border-top: 1px solid rgba(0,0,0,0.04);
        background-color: rgba(245,240,230,0.97);
      }

      .nav-links-mobile a {
        font-size: 0.92rem;
      }

      .nav-links-mobile .nav-mobile-cta {
        display: flex;
        gap: 0.5rem;
        margin-top: 0.6rem;
      }

      section {
        padding-top: 4rem;
      }

      .section-card {
        padding: 2.2rem 1.5rem;
      }
    }

    @media (max-width: 480px) {
      .hero-title {
        font-size: 1.7rem;
      }

      .hero-photo {
        width: min(230px, 80vw);
      }
    }
  </style>
</head>

<body>
  <!-- ========= NAV ========= -->
  <header>
    <nav class="nav" aria-label="Navigation principale">
      <div class="nav-brand">
        <div class="nav-logo-circle" aria-hidden="true">V</div>
        <div class="nav-brand-text">VAKIMA</div>
      </div>

      <div class="nav-links" role="menubar">
        <a href="#accueil" class="nav-link active" role="menuitem">Accueil</a>
        <a href="#a-propos" class="nav-link" role="menuitem">À propos</a>
        <a href="#projets" class="nav-link" role="menuitem">Projets</a>
        <a href="#vakima" class="nav-link" role="menuitem">VAKIMA</a>
        <a href="#contact" class="nav-link" role="menuitem">Contact</a>
      </div>

      <div class="nav-cta">
        <a href="#projets" class="btn btn-secondary">Découvrir mes projets</a>
        <a href="#contact" class="btn btn-primary">Me contacter</a>
      </div>

      <button class="nav-burger" aria-label="Ouvrir le menu" aria-expanded="false">
        <div class="nav-burger-lines"></div>
      </button>
    </nav>
    <div class="nav-links-mobile" id="nav-mobile">
      <a href="#accueil">Accueil</a>
      <a href="#a-propos">À propos</a>
      <a href="#projets">Projets</a>
      <a href="#vakima">VAKIMA</a>
      <a href="#contact">Contact</a>
      <div class="nav-mobile-cta">
        <a href="#projets" class="btn btn-secondary">Projets</a>
        <a href="#contact" class="btn btn-primary">Contact</a>
      </div>
    </div>
  </header>

  <main class="wrapper">
    <!-- ========= ACCUEIL ========= -->
    <section id="accueil" aria-labelledby="hero-title">
      <div class="section-card hero fade-in">
        <div class="hero">
          <div>
            <div class="hero-text-kicker">Étudiante M1 & Freelance</div>
            <h1 class="hero-title" id="hero-title">Créatrice de moments uniques</h1>
            <p class="hero-tagline">Allier créativité, relation humaine et rigueur professionnelle.</p>
            <p class="hero-intro">
              Je suis étudiante en Master 1 à Burgundy School of Business et fondatrice de <strong>VAKIMA</strong>, une micro‑entreprise dédiée aux cadeaux personnalisés et aux prestations de service sur mesure.
            </p>
            <div class="hero-cta">
              <a href="#projets" class="btn btn-primary">Découvrir mes projets</a>
              <a href="#contact" class="btn btn-secondary">Me contacter</a>
            </div>
            <p class="hero-meta">
              Basée entre Lyon et la Bourgogne, je construis des expériences authentiques qui combinent ancrage local, sens du détail et bienveillance.
            </p>
          </div>

          <div class="hero-photo-wrapper" aria-hidden="true">
            <!-- Remplace src par ta vraie photo -->
            <img src="https://via.placeholder.com/400x500.png?text=Ta+photo+ici" alt="Portrait professionnel de VAKIMA" class="hero-photo" />
            <div class="hero-pill">
              <span class="hero-pill-dot"></span>
              <span>+7 ans d’animation & terrain</span>
            </div>
            <div class="hero-pill-bottom">
              VAKIMA · cadeaux & services
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ========= À PROPOS ========= -->
    <section id="a-propos" aria-labelledby="about-title">
      <div class="section-card fade-in">
        <header class="section-header">
          <p class="section-kicker">À propos</p>
          <h2 class="section-title" id="about-title">De la Polynésie à la Bourgogne</h2>
          <p class="section-subtitle">
            Un parcours entre îles et continent, de la classe préparatoire à Burgundy School of Business, qui nourrit ma polyvalence, mon sens du collectif et ma capacité d’adaptation.
          </p>
        </header>

        <div class="about-grid">
          <div>
            <p>
              Originaire de Polynésie française, j’ai grandi avec une culture du partage, de la convivialité et de l’engagement communautaire.
              Après un parcours en classe préparatoire, je poursuis aujourd’hui mon Master 1 à BSB, tout en développant mon activité freelance.
            </p>
            <p style="margin-top:0.8rem;">
              Mon quotidien se situe à la croisée de plusieurs univers : animation, restauration, logistique, relation client et développement commercial, que je mets au service de projets concrets.
            </p>

            <div class="about-values" aria-label="Valeurs principales">
              <span class="chip">Partage</span>
              <span class="chip">Créativité</span>
              <span class="chip">Engagement</span>
              <span class="chip">Polyvalence</span>
            </div>

            <div class="about-skills">
              <h3 style="font-size:0.98rem; margin-bottom:0.4rem;">Compétences clés</h3>
              <div class="about-skills-list">
                <span class="skill-tag">Gestion de projet</span>
                <span class="skill-tag">Relation client</span>
                <span class="skill-tag">Animation d’équipe</span>
                <span class="skill-tag">Organisation d’événements</span>
                <span class="skill-tag">Communication interpersonnelle</span>
                <span class="skill-tag">Gestion logistique</span>
              </div>
            </div>
          </div>

          <div>
            <h3 style="font-size:0.98rem; margin-bottom:0.6rem;">Expériences marquantes</h3>
            <div class="about-timeline" aria-label="Timeline des expériences">
              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Fondatrice – VAKIMA</span>
                    <span class="timeline-org">· Artisanat & prestations de service</span>
                  </div>
                  <p class="timeline-desc">
                    Création de cadeaux personnalisés, accompagnement client de A à Z, gestion de projet, prestations ponctuelles en événementiel, restauration et logistique.
                  </p>
                </div>
              </div>

              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Ambassadrice étudiante</span>
                    <span class="timeline-org">· Burgundy School of Business</span>
                  </div>
                  <p class="timeline-desc">
                    Promotion de l’école, accueil et accompagnement des candidats, participation aux événements de recrutement et de découverte.
                  </p>
                </div>
              </div>

              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Responsable d’exploitation</span>
                    <span class="timeline-org">· Les Petites Cantines</span>
                  </div>
                  <p class="timeline-desc">
                    Gestion d’équipe, logistique quotidienne, approvisionnement et animation d’un lieu convivial autour de la cuisine participative.
                  </p>
                </div>
              </div>

              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Développeuse commerciale internationale</span>
                    <span class="timeline-org">· Pentaskill</span>
                  </div>
                  <p class="timeline-desc">
                    Prospection, suivi de portefeuille clients et contribution au développement de l’activité à l’international.
                  </p>
                </div>
              </div>

              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Animatrice</span>
                    <span class="timeline-org">· 7 ans d’expérience</span>
                  </div>
                  <p class="timeline-desc">
                    Encadrement d’enfants, conception et animation d’activités ludiques et pédagogiques, gestion de groupes et de temps forts.
                  </p>
                </div>
              </div>

              <div class="timeline-item">
                <div class="timeline-marker"></div>
                <div>
                  <div class="timeline-title-row">
                    <span class="timeline-role">Restauration & relation client</span>
                    <span class="timeline-org">· Divers établissements & TCL</span>
                  </div>
                  <p class="timeline-desc">
                    Service en salle, accueil client, gestion des flux, enquêtes de satisfaction pour les transports en commun lyonnais (TCL).
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ========= PROJETS ========= -->
    <section id="projets" aria-labelledby="projects-title">
      <div class="section-card fade-in">
        <header class="section-header">
          <p class="section-kicker">Projets & réalisations</p>
          <h2 class="section-title" id="projects-title">Donner vie aux idées</h2>
          <p class="section-subtitle">
            Des projets personnels, associatifs et professionnels qui mêlent organisation d’événements, sensibilisation, collecte de fonds et créations sur mesure.
          </p>
        </header>

        <h3 style="font-size:0.98rem; margin-bottom:0.8rem;">Projets personnels & associatifs</h3>
        <div class="projects-grid">
          <!-- Soirée Polynésienne -->
          <article class="project-card">
            <div class="project-label">Événement</div>
            <h4 class="project-title">Soirée Polynésienne</h4>
            <p class="project-meta">Organisation d’un événement intergénérationnel autour de la culture polynésienne.</p>
            <p class="project-role">Mon rôle</p>
            <p class="project-desc">
              Conception du concept de la soirée, coordination des animations, gestion des intervenants, communication et accueil du public pour créer une expérience chaleureuse et immersive.
            </p>
            <div class="project-badges">
              <span class="project-badge">Organisation d’événement</span>
              <span class="project-badge">Animation</span>
              <span class="project-badge">Gestion logistique</span>
            </div>
            <div class="project-media-placeholder">
              Ajoute ici des photos de la soirée, des ateliers ou des moments de partage.
            </div>
          </article>

          <!-- Boussole Intime -->
          <article class="project-card">
            <div class="project-label">Sensibilisation</div>
            <h4 class="project-title">“Boussole Intime”</h4>
            <p class="project-meta">Projet de sensibilisation à la sexualité auprès des jeunes, en partenariat avec des associations.</p>
            <p class="project-role">Mon rôle</p>
            <p class="project-desc">
              Co‑construction du programme, animation de temps d’échange, coordination avec les partenaires associatifs et adaptation des contenus à différents publics.
            </p>
            <div class="project-badges">
              <span class="project-badge">Pédagogie</span>
              <span class="project-badge">Co‑animation</span>
              <span class="project-badge">Partenariats</span>
            </div>
            <div class="project-media-placeholder">
              Intègre ici visuels, affiches ou supports créés pour le projet.
            </div>
          </article>

          <!-- Collecte de fonds -->
          <article class="project-card">
            <div class="project-label">Collecte de fonds</div>
            <h4 class="project-title">Tour de France des préparationnaires</h4>
            <p class="project-meta">Organisation d’une campagne pour financer le Tour de France des préparationnaires.</p>
            <p class="project-role">Mon rôle</p>
            <p class="project-desc">
              Mise en place de la stratégie de collecte, organisation d’actions locales, communication, suivi des donateurs et reporting pour garantir transparence et efficacité.
            </p>
            <div class="project-badges">
              <span class="project-badge">Gestion de projet</span>
              <span class="project-badge">Communication</span>
              <span class="project-badge">Collecte de fonds</span>
            </div>
            <div class="project-media-placeholder">
              Ajoute ici visuels de campagne, chiffres clés ou témoignages.
            </div>
          </article>
        </div>

        <h3 style="font-size:0.98rem; margin:2.4rem 0 0.8rem;">Projets VAKIMA</h3>
        <div class="projects-grid">
          <!-- Créations personnalisées -->
          <article class="project-card">
            <div class="project-label">VAKIMA · Cadeaux</div>
            <h4 class="project-title">Créations personnalisées</h4>
            <p class="project-meta">Cadeaux sur mesure pour particuliers et événements (anniversaires, mariages, soirées d’entreprise, etc.).</p>
            <p class="project-role">Mon rôle</p>
            <p class="project-desc">
              Écoute du besoin, proposition d’idées, création des objets, personnalisation et livraison en temps voulu, avec un suivi attentif du client.
            </p>
            <div class="project-badges">
              <span class="project-badge">Créativité</span>
              <span class="project-badge">Accompagnement client</span>
              <span class="project-badge">Gestion de délais</span>
            </div>
            <div class="project-media-placeholder">
              Ajoute ici une galerie de photos de tes produits (coffrets, cadres, goodies, etc.).
            </div>
          </article>

          <!-- Prestations de service -->
          <article class="project-card">
            <div class="project-label">VAKIMA · Services</div>
            <h4 class="project-title">Prestations de service terrain</h4>
            <p class="project-meta">Missions ponctuelles en restauration, logistique et événementiel dans la région lyonnaise.</p>
            <p class="project-role">Mon rôle</p>
            <p class="project-desc">
              Renfort sur le terrain lors de services, événements ou opérations logistiques, avec une attention particulière à la qualité d’accueil et à l’efficacité.
            </p>
            <div class="project-badges">
              <span class="project-badge">Polyvalence</span>
              <span class="project-badge">Opérations terrain</span>
              <span class="project-badge">Esprit d’équipe</span>
            </div>
            <div class="project-media-placeholder">
              Ajoute ici des photos de missions, coulisses d’événements ou moments de travail.
            </div>
          </article>

          <!-- Témoignages clients -->
          <article class="project-card">
            <div class="project-label">VAKIMA · Témoignages</div>
            <h4 class="project-title">Ce que disent mes clients</h4>
            <p class="project-meta">Extraits de retours clients sur les créations VAKIMA et les prestations de service.</p>
            <p class="project-desc">
              « Une écoute attentive, des idées originales et une livraison impeccable. »  
              « Professionnelle, souriante et fiable, même en période de rush. »
            </p>
            <div class="project-badges">
              <span class="project-badge">Satisfaction client</span>
              <span class="project-badge">Qualité de service</span>
            </div>
            <div class="project-media-placeholder">
              Intègre ici de vrais témoignages avec prénoms, type d’événement et photos si possible.
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- ========= VAKIMA ========= -->
    <section id="vakima" aria-labelledby="vakima-title">
      <div class="section-card fade-in">
        <header class="section-header">
          <p class="section-kicker">Mon activité freelance</p>
          <h2 class="section-title" id="vakima-title">VAKIMA – Créations & services</h2>
          <p class="section-subtitle">
            VAKIMA, c’est à la fois un atelier de cadeaux personnalisés et un soutien terrain pour les acteurs de la restauration, de la logistique et de l’événementiel, principalement à Lyon et dans la région.
          </p>
        </header>

        <div class="vakima-grid">
          <div>
            <div class="vakima-pill">
              <span style="width:8px; height:8px; border-radius:999px; background:linear-gradient(135deg, var(--color-primary), var(--color-accent));"></span>
              Micro‑entreprise déclarée · VAKIMA
            </div>
            <p>
              VAKIMA est née d’un constat simple : les personnes et les organisations ont besoin d’un accompagnement humain, souple et créatif, qu’il s’agisse de faire plaisir avec un cadeau personnalisé ou de renforcer une équipe le temps d’un événement.
            </p>

            <div class="vakima-columns">
              <div class="vakima-column-card">
                <h3 class="vakima-column-title">1. Création de cadeaux personnalisés</h3>
                <p style="font-size:0.88rem; color:var(--color-text-secondary);">
                  Des cadeaux pensés sur mesure, pour marquer un moment important et refléter la personnalité de la personne ou de l’événement.
                </p>
                <ul class="vakima-list">
                  <li>Idéation et conseils personnalisés.</li>
                  <li>Création et personnalisation (noms, dates, messages).</li>
                  <li>Préparation des commandes et emballage.</li>
                  <li>Remise en main propre ou livraison selon le projet.</li>
                </ul>
              </div>

              <div class="vakima-column-card">
                <h3 class="vakima-column-title">2. Prestations de service</h3>
                <p style="font-size:0.88rem; color:var(--color-text-secondary);">
                  Renfort opérationnel sur des missions ponctuelles, avec une approche professionnelle et souriante.
                </p>
                <ul class="vakima-list">
                  <li>Restauration : service, mise en place, plonge légère.</li>
                  <li>Logistique : montage/démontage, préparation de commandes.</li>
                  <li>Événementiel : accueil, vestiaire, animation, gestion de flux.</li>
                  <li>Autres missions de courte durée selon les besoins.</li>
                </ul>
              </div>
            </div>

            <div class="vakima-advantages" aria-label="Avantages VAKIMA">
              <span class="vakima-adv-chip">Accompagnement personnalisé</span>
              <span class="vakima-adv-chip">Rigueur & fiabilité</span>
              <span class="vakima-adv-chip">Créativité</span>
              <span class="vakima-adv-chip">Ancrage local · Lyon & région</span>
            </div>

            <div class="vakima-cta">
              <a href="#contact" class="btn btn-primary">Demander un devis</a>
              <a href="#contact" class="btn btn-secondary">Discuter de votre projet</a>
            </div>
          </div>

          <div>
            <h3 style="font-size:0.98rem; margin-bottom:0.6rem;">Galerie VAKIMA</h3>
            <p style="font-size:0.88rem; color:var(--color-text-secondary); margin-bottom:0.7rem;">
              Un aperçu de mes créations et de mes missions terrain. Remplace ces zones par tes propres photos pour rendre la galerie encore plus vivante.
            </p>
            <div class="vakima-gallery">
              <div class="vakima-photo">Photo cadeau personnalis&eacute;</div>
              <div class="vakima-photo">Coulisses atelier</div>
              <div class="vakima-photo">Mission &eacute;v&eacute;nementielle</div>
              <div class="vakima-photo">Moment client</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ========= CONTACT ========= -->
    <section id="contact" aria-labelledby="contact-title">
      <div class="section-card fade-in">
        <header class="section-header">
          <p class="section-kicker">Contact</p>
          <h2 class="section-title" id="contact-title">Parlons de votre projet</h2>
          <p class="section-subtitle">
            Une idée de cadeau, un besoin de renfort sur un événement ou une opportunité professionnelle ?
            Écrivez‑moi, et nous verrons ensemble comment y répondre concrètement.
          </p>
        </header>

        <div class="contact-grid">
          <div>
            <div class="contact-info-list">
              <p class="contact-info-item">
                <span>Localisation :</span> Lyon & région (Rhône‑Alpes), déplacements possibles selon projet.
              </p>
              <p class="contact-info-item">
                <span>Email :</span> <a href="mailto:prenom.nom@vakima.fr">prenom.nom@vakima.fr</a>
              </p>
              <p class="contact-info-item">
                <span>LinkedIn :</span> <a href="https://www.linkedin.com/in/ton-profil" target="_blank" rel="noreferrer">Mon profil LinkedIn</a>
              </p>
            </div>

            <div class="contact-socials">
              <div class="contact-social-pill">Instagram (VAKIMA)</div>
              <div class="contact-social-pill">Facebook (optionnel)</div>
              <div class="contact-social-pill">Autres réseaux selon besoins</div>
            </div>
          </div>

          <div>
            <form id="contact-form" novalidate>
              <div>
                <label for="name">Nom & prénom</label>
                <input type="text" id="name" name="name" placeholder="Votre nom complet" required />
              </div>
              <div>
                <label for="email">Adresse email</label>
                <input type="email" id="email" name="email" placeholder="vous@exemple.com" required />
              </div>
              <div>
                <label for="subject">Objet</label>
                <input type="text" id="subject" name="subject" placeholder="Cadeau personnalisé, mission événementielle..." required />
              </div>
              <div>
                <label for="message">Message</label>
                <textarea id="message" name="message" placeholder="Parlez-moi de votre besoin, de la date, du contexte..." required></textarea>
              </div>
              <p class="contact-small">
                Ce formulaire est une première prise de contact. Je reviendrai vers vous par email pour préciser votre besoin et vous transmettre une proposition.
              </p>
              <button type="submit" class="btn btn-primary" style="margin-top:0.4rem;">Envoyer le message</button>
              <div class="form-status" id="form-status" aria-live="polite"></div>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- ========= FOOTER ========= -->
  <footer>
    <div class="footer-inner">
      <p>© <span id="year"></span> VAKIMA – Portfolio. Tous droits réservés.</p>
      <p>Site créé par VAKIMA pour mettre en lumière un parcours entre études, terrain et entrepreneuriat.</p>
    </div>
  </footer>

  <!-- ========= JS ========= -->
  <script>
    // Année dynamique
    document.getElementById('year').textContent = new Date().getFullYear();

    // Burger menu
    const burger = document.querySelector('.nav-burger');
    const mobileNav = document.getElementById('nav-mobile');
    burger.addEventListener('click', () => {
      const isActive = burger.classList.toggle('active');
      mobileNav.style.display = isActive ? 'flex' : 'none';
      burger.setAttribute('aria-expanded', isActive ? 'true' : 'false');
    });

    // Scroll doux pour les liens internes
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        const targetId = this.getAttribute('href').substring(1);
        const target = document.getElementById(targetId);
        if (target) {
          e.preventDefault();
          const offset = 80; // hauteur approximative de la nav
          const targetPosition = target.getBoundingClientRect().top + window.pageYOffset - offset;
          window.scrollTo({ top: targetPosition, behavior: 'smooth' });
          mobileNav.style.display = 'none';
          burger.classList.remove('active');
          burger.setAttribute('aria-expanded', 'false');
        }
      });
    });

    // Activation du lien de navigation selon la section visible
    const sections = document.querySelectorAll('main section[id]');
    const navLinks = document.querySelectorAll('.nav-links a');

    const observerSections = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const id = entry.target.id;
          navLinks.forEach(link => {
            link.classList.toggle('active', link.getAttribute('href') === '#' + id);
          });
        }
      });
    }, { rootMargin: '-55% 0px -40% 0px' });

    sections.forEach(section => observerSections.observe(section));

    // Animation légère au scroll (fade‑in)
    const fadeIns = document.querySelectorAll('.fade-in');
    const observerFade = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          observerFade.unobserve(entry.target);
        }
      });
    }, { threshold: 0.18 });

    fadeIns.forEach(el => observerFade.observe(el));

    // Validation simple du formulaire (front uniquement)
    const form = document.getElementById('contact-form');
    const formStatus = document.getElementById('form-status');

    form.addEventListener('submit', (e) => {
      e.preventDefault();
      formStatus.textContent = '';
      formStatus.className = 'form-status';

      const name = form.name.value.trim();
      const email = form.email.value.trim();
      const subject = form.subject.value.trim();
      const message = form.message.value.trim();

      if (!name || !email || !subject || !message) {
        formStatus.textContent = 'Merci de remplir tous les champs obligatoires.';
        formStatus.classList.add('error');
        return;
      }

      // Ici, tu peux brancher un service (Formspree, Netlify Forms, backend perso, etc.)
      formStatus.textContent = 'Merci pour votre message ! Je vous répondrai dans les plus brefs délais.';
      formStatus.classList.add('success');
      form.reset();
    });
  </script>
</body>
</html>
