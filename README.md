<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/8e3ab32c-41b3-4b74-b253-f6ea75797604" />
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JMEtechFlow | Welcome</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Great+Vibes&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --gold: #f4d18f;
      --gold-soft: #e4bc72;
      --olive: #667043;
      --olive-deep: #39411f;
      --cream: #f7f0e2;
      --stone: #1b140d;
      --brown: #3d2414;
      --shadow: rgba(0,0,0,0.45);
      --panel: rgba(22, 15, 10, 0.72);
      --line: rgba(244, 209, 143, 0.22);
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      color: var(--cream);
      background:
        linear-gradient(rgba(16, 11, 7, 0.56), rgba(16, 11, 7, 0.8)),
        url('hero-italy.png') center/cover no-repeat fixed;
      min-height: 100vh;
      overflow-x: hidden;
    }

    .glow-orbs::before,
    .glow-orbs::after {
      content: '';
      position: fixed;
      width: 26rem;
      height: 26rem;
      border-radius: 999px;
      filter: blur(90px);
      opacity: 0.18;
      z-index: 0;
      pointer-events: none;
      animation: drift 14s ease-in-out infinite;
    }

    .glow-orbs::before {
      background: #f2bf66;
      top: -6rem;
      right: -4rem;
    }

    .glow-orbs::after {
      background: #647543;
      bottom: -8rem;
      left: -4rem;
      animation-delay: -6s;
    }

    @keyframes drift {
      0%, 100% { transform: translateY(0px) translateX(0px) scale(1); }
      50% { transform: translateY(22px) translateX(-18px) scale(1.06); }
    }

    @keyframes floatWords {
      0%, 100% { transform: translateY(0px); opacity: 0.85; }
      50% { transform: translateY(-10px); opacity: 1; }
    }

    @keyframes pulseGlow {
      0%, 100% {
        text-shadow:
          0 0 14px rgba(244, 209, 143, 0.35),
          0 0 40px rgba(244, 209, 143, 0.18);
      }
      50% {
        text-shadow:
          0 0 20px rgba(244, 209, 143, 0.75),
          0 0 55px rgba(244, 209, 143, 0.35);
      }
    }

    @keyframes shimmerLine {
      0% { background-position: -200% 0; }
      100% { background-position: 200% 0; }
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .page {
      position: relative;
      z-index: 1;
      width: min(1200px, calc(100% - 2rem));
      margin: 0 auto;
      padding: 1.25rem 0 3rem;
    }

    .hero {
      position: relative;
      min-height: 100vh;
      display: grid;
      align-items: center;
      padding: 2rem 0 3rem;
      animation: fadeUp 1s ease;
    }

    .hero::after {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at center, rgba(255,255,255,0.08), transparent 38%);
      pointer-events: none;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 1.5rem;
      align-items: stretch;
    }

    .glass,
    .panel {
      background: var(--panel);
      border: 1px solid var(--line);
      box-shadow: 0 20px 50px var(--shadow);
      backdrop-filter: blur(8px);
    }

    .hero-main {
      border-radius: 30px;
      padding: 2.25rem;
      position: relative;
      overflow: hidden;
    }

    .hero-main::before {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(120deg, rgba(244, 209, 143, 0.09), transparent 28%, transparent 72%, rgba(109, 122, 70, 0.12));
      pointer-events: none;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 0.55rem;
      border: 1px solid rgba(244, 209, 143, 0.25);
      padding: 0.5rem 0.9rem;
      border-radius: 999px;
      font-size: 0.82rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 1rem;
      background: rgba(255,255,255,0.04);
    }

    h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(3.6rem, 8vw, 7rem);
      line-height: 0.95;
      margin: 0;
      color: #fff6e8;
      animation: pulseGlow 4s ease-in-out infinite;
    }

    .script {
      font-family: 'Great Vibes', cursive;
      font-weight: 400;
      color: var(--gold);
      display: inline-block;
      margin-left: 0.4rem;
      font-size: 0.9em;
    }

    .hero-tagline {
      margin: 1rem 0 0;
      font-family: 'Great Vibes', cursive;
      font-size: clamp(1.8rem, 4vw, 3rem);
      color: var(--gold);
      animation: floatWords 4s ease-in-out infinite;
    }

    .hero-copy {
      margin-top: 1.3rem;
      max-width: 60ch;
      line-height: 1.8;
      color: rgba(247, 240, 226, 0.94);
      font-size: 1rem;
    }

    .hero-quote {
      margin-top: 1.35rem;
      padding: 1rem 1.2rem;
      border-left: 3px solid var(--gold-soft);
      background: rgba(255,255,255,0.03);
      border-radius: 0 18px 18px 0;
      color: #f6e7c8;
      font-style: italic;
    }

    .moving-words {
      margin-top: 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .moving-words span {
      padding: 0.7rem 1rem;
      border-radius: 999px;
      border: 1px solid rgba(244, 209, 143, 0.24);
      background: rgba(255,255,255,0.05);
      color: var(--cream);
      font-weight: 500;
      animation: floatWords 3.8s ease-in-out infinite;
    }

    .moving-words span:nth-child(2) { animation-delay: .3s; }
    .moving-words span:nth-child(3) { animation-delay: .6s; }
    .moving-words span:nth-child(4) { animation-delay: .9s; }
    .moving-words span:nth-child(5) { animation-delay: 1.2s; }
    .moving-words span:nth-child(6) { animation-delay: 1.5s; }

    .hero-side {
      display: grid;
      gap: 1rem;
      align-content: start;
    }

    .card {
      border-radius: 24px;
      padding: 1.35rem;
    }

    .card h3 {
      margin: 0 0 0.75rem;
      font-family: 'Cormorant Garamond', serif;
      font-size: 2rem;
      color: #fff4de;
    }

    .card p,
    .card li {
      line-height: 1.75;
      color: rgba(247, 240, 226, 0.92);
    }

    .list {
      display: grid;
      gap: 0.55rem;
      padding: 0;
      margin: 0;
      list-style: none;
    }

    .list li {
      display: flex;
      align-items: center;
      gap: 0.7rem;
    }

    .list li::before {
      content: '✦';
      color: var(--gold);
      font-size: 0.9rem;
    }

    .section {
      margin-top: 1.5rem;
      animation: fadeUp 1s ease;
    }

    .section-title {
      text-align: center;
      margin-bottom: 1rem;
    }

    .section-title h2 {
      margin: 0;
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.3rem, 4vw, 3.6rem);
      color: #fff2db;
    }

    .section-title p {
      margin-top: 0.35rem;
      color: var(--gold);
      font-family: 'Great Vibes', cursive;
      font-size: 1.5rem;
    }

    .build-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 1rem;
    }

    .build-card {
      border-radius: 24px;
      padding: 1.25rem;
      min-height: 210px;
      position: relative;
      overflow: hidden;
    }

    .build-card::before {
      content: '';
      position: absolute;
      inset: auto -30% -65% auto;
      width: 12rem;
      height: 12rem;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(244, 209, 143, 0.18), transparent 68%);
      pointer-events: none;
    }

    .build-card h4 {
      margin: 0 0 0.7rem;
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.65rem;
      color: #fff1d5;
    }

    .build-card p {
      margin: 0;
      line-height: 1.75;
      color: rgba(247, 240, 226, 0.92);
    }

    .footer-line {
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid rgba(244, 209, 143, 0.18);
      text-align: center;
      color: rgba(247, 240, 226, 0.8);
      font-size: 0.95rem;
    }

    .accent-line {
      height: 2px;
      border-radius: 999px;
      margin: 1rem 0 0;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      background-size: 200% 100%;
      animation: shimmerLine 4s linear infinite;
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      margin-top: 1.5rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.55rem;
      padding: 0.85rem 1.2rem;
      border-radius: 999px;
      text-decoration: none;
      font-weight: 600;
      border: 1px solid rgba(244, 209, 143, 0.28);
      transition: transform 0.22s ease, box-shadow 0.22s ease, background 0.22s ease;
    }

    .btn.primary {
      background: linear-gradient(135deg, rgba(244, 209, 143, 0.22), rgba(112, 125, 71, 0.18));
      color: #fff4de;
      box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    }

    .btn.secondary {
      background: rgba(255,255,255,0.03);
      color: var(--cream);
    }

    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 16px 30px rgba(0,0,0,0.25);
    }

    .corner-note {
      position: fixed;
      right: 1rem;
      bottom: 1rem;
      z-index: 5;
      padding: 0.85rem 1rem;
      border-radius: 16px;
      background: rgba(20, 14, 9, 0.8);
      border: 1px solid rgba(244, 209, 143, 0.2);
      color: var(--gold);
      font-size: 0.88rem;
      backdrop-filter: blur(8px);
    }

    @media (max-width: 980px) {
      .hero-grid,
      .build-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 760px) {
      body {
        background-attachment: scroll;
      }

      .page {
        width: min(100% - 1rem, 1200px);
      }

      .hero {
        min-height: auto;
        padding-top: 1rem;
      }

      .hero-grid,
      .build-grid {
        grid-template-columns: 1fr;
      }

      .hero-main,
      .card,
      .build-card {
        border-radius: 22px;
      }

      h1 {
        line-height: 1;
      }

      .corner-note {
        position: static;
        margin: 1rem auto 0;
        width: fit-content;
      }
    }
  </style>
</head>
<body>
  <div class="glow-orbs"></div>

  <main class="page">
    <section class="hero">
      <div class="hero-grid">
        <div class="hero-main glass">
          <div class="eyebrow">Italy inspired • built with purpose</div>
          <h1>JME<span class="script">techFlow</span></h1>
          <p class="hero-tagline">Built with Intention. Flowing with Purpose.</p>
          <div class="accent-line"></div>

          <p class="hero-copy">
            Like the ancient pathways of Italy, my journey in tech is intentional, structured, and built to last.
            Every step I take is designed to connect people, solve problems, and create systems that stand the test of time.
          </p>

          <div class="hero-quote">
            This is more than a career. This is my pathway.
          </div>

          <div class="moving-words">
            <span>☁️ Cloud Infrastructure</span>
            <span>🗂️ Active Directory</span>
            <span>⚡ PowerShell</span>
            <span>🌐 Networking</span>
            <span>🛠️ System Configuration</span>
            <span>🔐 Security</span>
            <span>🐳 Docker</span>
            <span>💻 Windows Server</span>
            <span>🚀 Azure</span>
            <span>📡 Virtualization</span>
            <span>✨ Built to Last</span>
          </div>

          <div class="cta-row">
            <a class="btn primary" href="#building">Explore the Journey</a>
            <a class="btn secondary" href="#meaning">The Meaning Behind JMEtechFlow</a>
          </div>
        </div>

        <div class="hero-side">
          <article class="card glass">
            <h3>My Journey</h3>
            <p>
              From the classroom to the cloud, my path has been shaped by curiosity, service, and a desire to make a meaningful impact.
            </p>
            <p>
              Education built my foundation. Technology is building my future.
            </p>
          </article>

          <article id="meaning" class="card glass">
            <h3>The Meaning Behind JMEtechFlow</h3>
            <ul class="list">
              <li><strong>JME</strong> — My identity</li>
              <li><strong>Tech</strong> — The systems I build</li>
              <li><strong>Flow</strong> — The intentional pathway that connects it all</li>
            </ul>
            <p style="margin-top: 0.85rem;">
              Where technology, purpose, and growth flow together.
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="building" class="section">
      <div class="section-title">
        <h2>What I’m Building</h2>
        <p>One pathway. Many connections. Lasting impact.</p>
      </div>

      <div class="build-grid">
        <article class="build-card glass">
          <h4>☁️ Cloud Infrastructure & Virtualization</h4>
          <p>I’m developing the skills and experience to build reliable, secure, and efficient systems in the cloud.</p>
        </article>

        <article class="build-card glass">
          <h4>🗂️ Active Directory & Identity Management</h4>
          <p>Strong systems begin with structure. I’m learning how identity, access, and organization work together.</p>
        </article>

        <article class="build-card glass">
          <h4>🌐 Networking & System Configuration</h4>
          <p>Every connection matters. I’m building the technical foundation to support stable, connected environments.</p>
        </article>

        <article class="build-card glass">
          <h4>⚡ PowerShell Automation</h4>
          <p>Intentional work creates efficiency. I’m exploring automation to make systems cleaner, smarter, and more scalable.</p>
        </article>
      </div>
    </section>

    <section class="section">
      <div class="section-title">
        <h2>My Approach</h2>
        <p>Intentional. Structured. People-centered. Built to last.</p>
      </div>

      <div class="build-grid">
        <article class="build-card glass">
          <h4>🎯 Intentional</h4>
          <p>Every step has purpose. I want the work I do to be thoughtful, useful, and grounded in real impact.</p>
        </article>

        <article class="build-card glass">
          <h4>🏛️ Structured</h4>
          <p>Like a strong foundation, growth happens best when built with clarity, consistency, and care.</p>
        </article>

        <article class="build-card glass">
          <h4>🤝 People-Centered</h4>
          <p>Technology should support people. I care about creating systems that serve, solve, and uplift.</p>
        </article>

        <article class="build-card glass">
          <h4>✨ Built to Last</h4>
          <p>I’m committed to continuous learning, real-world problem solving, and building a career that creates lasting value.</p>
        </article>
      </div>
    </section>

    <div class="footer-line">
      “The best roads are not found, they are built — stone by stone, with purpose and passion.”
      <br>
      Inspired by the timeless roads of Italy.
    </div>
  </main>

  <div class="corner-note">Replace <strong>hero-italy.png</strong> with your image file name.</div>
</body>
</html>
