<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Kunal Chandak — GitHub README Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap');

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #21262d;
    --border: #30363d;
    --accent: #58a6ff;
    --accent2: #3fb950;
    --accent3: #e3b341;
    --accent4: #f78166;
    --accent5: #bc8cff;
    --text: #e6edf3;
    --text2: #8b949e;
    --text3: #484f58;
    --glow-blue: rgba(88,166,255,0.15);
    --glow-green: rgba(63,185,80,0.15);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  .readme {
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.5rem 4rem;
    position: relative;
  }

  /* ── CANVAS BACKGROUND ── */
  #bg-canvas {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    opacity: 0.4;
  }

  .readme { position: relative; z-index: 1; }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 3rem 0 2rem;
  }

  .hero-title {
    font-family: 'JetBrains Mono', monospace;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 700;
    letter-spacing: -1px;
    background: linear-gradient(135deg, #58a6ff 0%, #bc8cff 40%, #3fb950 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: gradientShift 6s ease infinite alternate;
    background-size: 200%;
  }

  @keyframes gradientShift {
    0% { background-position: 0% 50%; }
    100% { background-position: 100% 50%; }
  }

  .hero-subtitle {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.95rem;
    color: var(--text2);
    margin-top: 0.5rem;
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .typing-wrap {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    margin: 1.2rem auto 0;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.5rem 1.2rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.9rem;
    color: var(--accent2);
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1em;
    background: var(--accent2);
    animation: blink 1s step-end infinite;
    vertical-align: text-bottom;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }

  /* ── BADGES ── */
  .badges {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.5rem;
    margin: 1.5rem 0 2rem;
  }

  .badge {
    padding: 0.3rem 0.85rem;
    border-radius: 20px;
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.5px;
    border: 1px solid;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }

  .badge:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 20px rgba(255,255,255,0.08);
  }

  .badge-blue  { color: var(--accent);  border-color: rgba(88,166,255,0.4);  background: rgba(88,166,255,0.08); }
  .badge-green { color: var(--accent2); border-color: rgba(63,185,80,0.4);   background: rgba(63,185,80,0.08); }
  .badge-amber { color: var(--accent3); border-color: rgba(227,179,65,0.4);  background: rgba(227,179,65,0.08); }
  .badge-red   { color: var(--accent4); border-color: rgba(247,129,102,0.4); background: rgba(247,129,102,0.08); }
  .badge-purple{ color: var(--accent5); border-color: rgba(188,140,255,0.4); background: rgba(188,140,255,0.08); }

  /* ── SECTION ── */
  .section {
    margin: 2.5rem 0;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 0.7rem;
    margin-bottom: 1.2rem;
    padding-bottom: 0.6rem;
    border-bottom: 1px solid var(--border);
  }

  .section-icon {
    width: 22px;
    height: 22px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 6px;
    font-size: 14px;
  }

  .section-title {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1rem;
    font-weight: 600;
    color: var(--text);
    letter-spacing: -0.3px;
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.7rem;
  }

  .about-item {
    display: flex;
    align-items: flex-start;
    gap: 0.6rem;
    padding: 0.75rem 1rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    font-size: 0.88rem;
    color: var(--text2);
    line-height: 1.4;
    transition: border-color 0.2s, background 0.2s;
  }

  .about-item:hover {
    border-color: rgba(88,166,255,0.3);
    background: rgba(88,166,255,0.04);
    color: var(--text);
  }

  .about-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    margin-top: 6px;
    flex-shrink: 0;
  }

  /* ── TECH GRID ── */
  .tech-category {
    margin-bottom: 1.2rem;
  }

  .tech-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    color: var(--text3);
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 0.5rem;
  }

  .tech-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .pill {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.75rem;
    padding: 0.25rem 0.7rem;
    border-radius: 4px;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--text2);
    transition: all 0.18s;
    cursor: default;
    white-space: nowrap;
  }

  .pill:hover {
    background: var(--surface2);
    color: var(--text);
    border-color: rgba(88,166,255,0.5);
    transform: translateY(-1px);
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.85rem;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.1rem 1.2rem;
    transition: all 0.25s;
    position: relative;
    overflow: hidden;
  }

  .project-card::before {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 10px;
    background: linear-gradient(135deg, transparent 60%, var(--card-glow, transparent));
    opacity: 0;
    transition: opacity 0.3s;
  }

  .project-card:hover::before { opacity: 1; }

  .project-card:hover {
    border-color: var(--card-accent, var(--border));
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(0,0,0,0.4);
  }

  .project-card.agriculture { --card-glow: rgba(63,185,80,0.1); --card-accent: rgba(63,185,80,0.4); }
  .project-card.security    { --card-glow: rgba(88,166,255,0.1); --card-accent: rgba(88,166,255,0.4); }
  .project-card.medical     { --card-glow: rgba(247,129,102,0.1); --card-accent: rgba(247,129,102,0.4); }
  .project-card.pcos        { --card-glow: rgba(188,140,255,0.1); --card-accent: rgba(188,140,255,0.4); }
  .project-card.chess       { --card-glow: rgba(227,179,65,0.1); --card-accent: rgba(227,179,65,0.4); }

  .project-header {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    margin-bottom: 0.5rem;
  }

  .project-icon {
    font-size: 1.1rem;
    width: 32px;
    height: 32px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 8px;
    background: var(--surface2);
    flex-shrink: 0;
  }

  .project-name {
    font-weight: 600;
    font-size: 0.92rem;
    color: var(--text);
    line-height: 1.2;
  }

  .project-desc {
    font-size: 0.8rem;
    color: var(--text2);
    line-height: 1.5;
    margin-bottom: 0.75rem;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
  }

  .tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.68rem;
    padding: 0.15rem 0.5rem;
    border-radius: 4px;
    font-weight: 500;
  }

  .tag-green  { background: rgba(63,185,80,0.12);  color: #3fb950; }
  .tag-blue   { background: rgba(88,166,255,0.12); color: #58a6ff; }
  .tag-red    { background: rgba(247,129,102,0.12);color: #f78166; }
  .tag-purple { background: rgba(188,140,255,0.12);color: #bc8cff; }
  .tag-amber  { background: rgba(227,179,65,0.12); color: #e3b341; }

  /* ── STATS BAR ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.75rem;
    margin-top: 1rem;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1rem;
    text-align: center;
  }

  .stat-num {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--accent);
    display: block;
  }

  .stat-label {
    font-size: 0.75rem;
    color: var(--text2);
    margin-top: 0.2rem;
  }

  /* ── SKILL RADAR ── */
  .radar-wrap {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  .radar-canvas {
    flex-shrink: 0;
  }

  .skill-bars {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
  }

  .bar-row {
    display: flex;
    align-items: center;
    gap: 0.7rem;
  }

  .bar-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.74rem;
    color: var(--text2);
    min-width: 110px;
  }

  .bar-track {
    flex: 1;
    height: 6px;
    background: var(--surface2);
    border-radius: 3px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    border-radius: 3px;
    width: 0;
    transition: width 1.2s cubic-bezier(0.22, 1, 0.36, 1);
  }

  .bar-pct {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem;
    color: var(--text3);
    min-width: 30px;
    text-align: right;
  }

  /* ── TIMELINE ── */
  .timeline {
    position: relative;
    padding-left: 1.5rem;
  }

  .timeline::before {
    content: '';
    position: absolute;
    left: 5px;
    top: 6px;
    bottom: 6px;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), var(--accent5), transparent);
  }

  .timeline-item {
    position: relative;
    padding: 0 0 1.2rem 1rem;
  }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -1.5rem;
    top: 6px;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    border: 2px solid var(--accent);
    background: var(--bg);
  }

  .timeline-date {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .timeline-title {
    font-size: 0.9rem;
    font-weight: 600;
    color: var(--text);
    margin: 0.2rem 0 0.2rem;
  }

  .timeline-body {
    font-size: 0.8rem;
    color: var(--text2);
    line-height: 1.5;
  }

  /* ── FOOTER ── */
  .footer {
    margin-top: 3rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: gap;
    gap: 1rem;
  }

  .footer-quote {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem;
    color: var(--text3);
    font-style: italic;
  }

  .footer-interests {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
  }

  .interest-pill {
    font-size: 0.75rem;
    color: var(--text2);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 0.2rem 0.7rem;
  }

  /* ── CONTRIBUTION GRAPH ── */
  .contrib-row {
    display: flex;
    gap: 3px;
    flex-wrap: wrap;
    margin-top: 0.5rem;
  }

  .contrib-week {
    display: flex;
    flex-direction: column;
    gap: 3px;
  }

  .contrib-day {
    width: 11px;
    height: 11px;
    border-radius: 2px;
    background: var(--surface2);
  }

  .contrib-day.l1 { background: #0e4429; }
  .contrib-day.l2 { background: #006d32; }
  .contrib-day.l3 { background: #26a641; }
  .contrib-day.l4 { background: #39d353; }

  /* ── CONNECTIONS ── */
  .social-row {
    display: flex;
    gap: 0.6rem;
    flex-wrap: wrap;
  }

  .social-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem 1rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    font-size: 0.83rem;
    font-weight: 500;
    color: var(--text2);
    text-decoration: none;
    transition: all 0.2s;
  }

  .social-btn:hover {
    color: var(--text);
    border-color: rgba(88,166,255,0.4);
    background: rgba(88,166,255,0.06);
    transform: translateY(-1px);
  }

  /* ── ANIMATED DOODLE ELEMENTS ── */
  .doodle-float {
    position: absolute;
    opacity: 0.06;
    pointer-events: none;
    animation: floatAround 20s linear infinite;
  }

  @keyframes floatAround {
    0%   { transform: translateY(0) rotate(0deg); }
    33%  { transform: translateY(-12px) rotate(5deg); }
    66%  { transform: translateY(6px) rotate(-3deg); }
    100% { transform: translateY(0) rotate(0deg); }
  }

  /* ── REVEAL ANIMATION ── */
  .reveal {
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }

  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* responsive */
  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .projects-grid { grid-template-columns: 1fr; }
    .stats-row { grid-template-columns: 1fr 1fr; }
    .radar-wrap { flex-direction: column; }
  }
</style>
</head>
<body>

<canvas id="bg-canvas"></canvas>

<div class="readme">

  <!-- HERO -->
  <div class="hero reveal">
    <div class="hero-title">Kunal Chandak</div>
    <div class="hero-subtitle">Mobile · AI/ML · Cybersecurity</div>
    <div class="typing-wrap">
      <span id="typing-text">Building tech that matters</span>
      <span class="cursor"></span>
    </div>

    <div class="badges" style="margin-top:1.2rem">
      <span class="badge badge-blue">📱 Flutter & React Native</span>
      <span class="badge badge-green">🧠 Explainable AI</span>
      <span class="badge badge-red">👁️ Computer Vision</span>
      <span class="badge badge-purple">🔐 Cybersecurity</span>
      <span class="badge badge-amber">🌾 Precision Agriculture</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(88,166,255,0.12)">👤</div>
      <span class="section-title">about_me.md</span>
    </div>
    <div class="about-grid">
      <div class="about-item">
        <div class="about-dot" style="background:#58a6ff"></div>
        Building cross-platform apps with <strong style="color:#e6edf3">Flutter</strong> & <strong style="color:#e6edf3">React Native</strong>
      </div>
      <div class="about-item">
        <div class="about-dot" style="background:#3fb950"></div>
        Researching <strong style="color:#e6edf3">Explainable AI</strong>, XAI pipelines with SHAP, LIME & GradCAM
      </div>
      <div class="about-item">
        <div class="about-dot" style="background:#f78166"></div>
        Building <strong style="color:#e6edf3">Computer Vision</strong> systems for medical diagnosis and agriculture
      </div>
      <div class="about-item">
        <div class="about-dot" style="background:#bc8cff"></div>
        Exploring <strong style="color:#e6edf3">Cybersecurity</strong>, E2E encryption, secure architectures
      </div>
      <div class="about-item">
        <div class="about-dot" style="background:#e3b341"></div>
        Currently: AI-powered <strong style="color:#e6edf3">Precision Irrigation</strong> & Secure QR File Sharing (Spring Boot)
      </div>
      <div class="about-item">
        <div class="about-dot" style="background:#58a6ff"></div>
        Working with <strong style="color:#e6edf3">Raspberry Pi</strong> for edge-deployed ML models in IoT contexts
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(63,185,80,0.12)">⚙️</div>
      <span class="section-title">tech_stack[]</span>
    </div>

    <div class="tech-category">
      <div class="tech-label">// Languages</div>
      <div class="tech-pills">
        <span class="pill">Python</span><span class="pill">Dart</span><span class="pill">Java</span><span class="pill">JavaScript</span><span class="pill">TypeScript</span><span class="pill">C</span><span class="pill">C++</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">// Mobile & Frontend</div>
      <div class="tech-pills">
        <span class="pill">Flutter</span><span class="pill">React Native</span><span class="pill">React.js</span><span class="pill">Node.js</span><span class="pill">Express</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">// AI / ML / CV</div>
      <div class="tech-pills">
        <span class="pill">TensorFlow</span><span class="pill">PyTorch</span><span class="pill">OpenCV</span><span class="pill">Scikit-learn</span>
        <span class="pill">GradCAM</span><span class="pill">EigenCAM</span><span class="pill">SHAP</span><span class="pill">LIME</span>
        <span class="pill">MobileNet</span><span class="pill">ResNet</span><span class="pill">EfficientNet</span><span class="pill">YOLO</span>
        <span class="pill">MC Dropout</span><span class="pill">Tesseract OCR</span><span class="pill">NLP</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">// Backend & Infra</div>
      <div class="tech-pills">
        <span class="pill">Spring Boot</span><span class="pill">FastAPI</span><span class="pill">Firebase</span><span class="pill">PostgreSQL</span>
        <span class="pill">MongoDB</span><span class="pill">Redis</span><span class="pill">Docker</span><span class="pill">AWS</span><span class="pill">GCP</span>
      </div>
    </div>

    <div class="tech-category">
      <div class="tech-label">// Tools & Hardware</div>
      <div class="tech-pills">
        <span class="pill">Raspberry Pi</span><span class="pill">Git</span><span class="pill">Linux</span><span class="pill">Figma</span>
        <span class="pill">Postman</span><span class="pill">VS Code</span><span class="pill">Android Studio</span><span class="pill">Anaconda</span>
      </div>
    </div>
  </div>

  <!-- SKILL PROFICIENCY -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(188,140,255,0.12)">📊</div>
      <span class="section-title">proficiency_radar</span>
    </div>
    <div class="radar-wrap">
      <canvas class="radar-canvas" id="radarChart" width="200" height="200"></canvas>
      <div class="skill-bars" id="skill-bars">
        <div class="bar-row">
          <span class="bar-label">Mobile Dev</span>
          <div class="bar-track"><div class="bar-fill" style="background:#58a6ff" data-pct="90"></div></div>
          <span class="bar-pct">90%</span>
        </div>
        <div class="bar-row">
          <span class="bar-label">Deep Learning</span>
          <div class="bar-track"><div class="bar-fill" style="background:#3fb950" data-pct="85"></div></div>
          <span class="bar-pct">85%</span>
        </div>
        <div class="bar-row">
          <span class="bar-label">Explainable AI</span>
          <div class="bar-track"><div class="bar-fill" style="background:#bc8cff" data-pct="80"></div></div>
          <span class="bar-pct">80%</span>
        </div>
        <div class="bar-row">
          <span class="bar-label">Computer Vision</span>
          <div class="bar-track"><div class="bar-fill" style="background:#f78166" data-pct="82"></div></div>
          <span class="bar-pct">82%</span>
        </div>
        <div class="bar-row">
          <span class="bar-label">Cybersecurity</span>
          <div class="bar-track"><div class="bar-fill" style="background:#e3b341" data-pct="72"></div></div>
          <span class="bar-pct">72%</span>
        </div>
        <div class="bar-row">
          <span class="bar-label">Backend / APIs</span>
          <div class="bar-track"><div class="bar-fill" style="background:#58a6ff" data-pct="78"></div></div>
          <span class="bar-pct">78%</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(227,179,65,0.12)">🚀</div>
      <span class="section-title">featured_projects/</span>
    </div>
    <div class="projects-grid">

      <div class="project-card agriculture">
        <div class="project-header">
          <div class="project-icon">🌾</div>
          <div class="project-name">Precision Irrigation System</div>
        </div>
        <div class="project-desc">AI-powered smart agriculture platform combining weather data, soil sensors, and crop intelligence for predictive irrigation scheduling and plant disease detection.</div>
        <div class="project-tags">
          <span class="tag tag-blue">Flutter</span>
          <span class="tag tag-green">Firebase</span>
          <span class="tag tag-green">ML</span>
          <span class="tag tag-green">YOLO</span>
          <span class="tag tag-amber">Raspberry Pi</span>
        </div>
      </div>

      <div class="project-card security">
        <div class="project-header">
          <div class="project-icon">🔐</div>
          <div class="project-name">Secure Core</div>
        </div>
        <div class="project-desc">Privacy-first Flutter app with room-based end-to-end encrypted file sharing, timed self-destructing drops, and screenshot prevention. Zero data retention.</div>
        <div class="project-tags">
          <span class="tag tag-blue">Flutter</span>
          <span class="tag tag-blue">E2E Encryption</span>
          <span class="tag tag-purple">Spring Boot</span>
          <span class="tag tag-red">QR Auth</span>
        </div>
      </div>

      <div class="project-card medical">
        <div class="project-header">
          <div class="project-icon">🧬</div>
          <div class="project-name">Ovarian Cancer XAI</div>
        </div>
        <div class="project-desc">Multi-model deep learning pipeline (ResNet + EfficientNet) for ovarian cancer detection with LIME explanations and Monte Carlo Dropout uncertainty quantification.</div>
        <div class="project-tags">
          <span class="tag tag-red">ResNet</span>
          <span class="tag tag-red">EfficientNet</span>
          <span class="tag tag-purple">GradCAM</span>
          <span class="tag tag-blue">LIME</span>
          <span class="tag tag-amber">MC Dropout</span>
        </div>
      </div>

      <div class="project-card pcos">
        <div class="project-header">
          <div class="project-icon">🔬</div>
          <div class="project-name">PCOS Detection XAI</div>
        </div>
        <div class="project-desc">5-model ensemble deep learning system for PCOS diagnosis from ultrasound imagery with SHAP-based feature importance and EigenCAM visual explanations.</div>
        <div class="project-tags">
          <span class="tag tag-purple">Ensemble DL</span>
          <span class="tag tag-purple">SHAP</span>
          <span class="tag tag-blue">LIME</span>
          <span class="tag tag-purple">EigenCAM</span>
        </div>
      </div>

      <div class="project-card chess">
        <div class="project-header">
          <div class="project-icon">♟️</div>
          <div class="project-name">Chess AI Engine</div>
        </div>
        <div class="project-desc">Full-featured chess engine in Python with Minimax search and Alpha-Beta pruning, custom evaluation functions, and Pygame GUI.</div>
        <div class="project-tags">
          <span class="tag tag-amber">Python</span>
          <span class="tag tag-amber">Pygame</span>
          <span class="tag tag-amber">Minimax</span>
          <span class="tag tag-amber">Alpha-Beta</span>
        </div>
      </div>

      <div class="project-card" style="--card-glow:rgba(88,166,255,0.08); --card-accent:rgba(88,166,255,0.3); border-style: dashed;">
        <div class="project-header">
          <div class="project-icon" style="background:transparent; font-size:1.4rem">+</div>
          <div class="project-name" style="color:var(--text2)">More in progress...</div>
        </div>
        <div class="project-desc">Always shipping something new. Currently exploring federated learning for privacy-preserving medical AI and adversarial robustness in CV models.</div>
        <div class="project-tags">
          <span class="tag tag-blue">Federated Learning</span>
          <span class="tag tag-red">Adversarial ML</span>
        </div>
      </div>

    </div>
  </div>

  <!-- CONTRIBUTION GRAPH -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(63,185,80,0.12)">📈</div>
      <span class="section-title">contribution_activity</span>
    </div>
    <div id="contrib-container" style="overflow-x:auto"></div>
    <div style="display:flex;gap:0.5rem;align-items:center;margin-top:0.5rem;">
      <span style="font-size:0.72rem;color:var(--text3)">Less</span>
      <div style="width:11px;height:11px;border-radius:2px;background:var(--surface2)"></div>
      <div style="width:11px;height:11px;border-radius:2px;background:#0e4429"></div>
      <div style="width:11px;height:11px;border-radius:2px;background:#006d32"></div>
      <div style="width:11px;height:11px;border-radius:2px;background:#26a641"></div>
      <div style="width:11px;height:11px;border-radius:2px;background:#39d353"></div>
      <span style="font-size:0.72rem;color:var(--text3)">More</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(227,179,65,0.12)">⚡</div>
      <span class="section-title">github_stats</span>
    </div>
    <div class="stats-row">
      <div class="stat-card">
        <span class="stat-num" id="c1">0</span>
        <div class="stat-label">Projects Shipped</div>
      </div>
      <div class="stat-card">
        <span class="stat-num" id="c2">0</span>
        <div class="stat-label">Technologies Used</div>
      </div>
      <div class="stat-card">
        <span class="stat-num" id="c3">0</span>
        <div class="stat-label">XAI Papers Implemented</div>
      </div>
    </div>
    <div style="margin-top:0.75rem;background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:0.7rem 1rem;font-family:'JetBrains Mono',monospace;font-size:0.78rem;color:var(--text2)">
      <span style="color:var(--accent2)">→</span> Most Used: <span style="color:var(--accent)">Python</span> · <span style="color:var(--accent3)">Dart</span> · <span style="color:var(--accent4)">Java</span> · <span style="color:var(--accent5)">JavaScript</span>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section reveal">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(88,166,255,0.12)">🔗</div>
      <span class="section-title">connect_with_me</span>
    </div>
    <div class="social-row">
      <a href="https://www.linkedin.com/in/kunal-chandak-2a532a26b/" class="social-btn" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="#58a6ff"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="https://www.instagram.com/kunalmchandak/" class="social-btn" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="#f78166"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
        Instagram
      </a>
      <a href="https://github.com/kunal-2604" class="social-btn" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="var(--text2)"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        GitHub
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer reveal">
    <div class="footer-quote">"Building tech that actually matters."</div>
    <div class="footer-interests">
      <span class="interest-pill">🚴 Cyclist</span>
      <span class="interest-pill">🏀 Basketball</span>
      <span class="interest-pill">🏸 Badminton</span>
      <span class="interest-pill">📍 Pune, India</span>
    </div>
  </div>

</div>

<script>
// ── BACKGROUND CANVAS (circuit doodle) ──
const bgCanvas = document.getElementById('bg-canvas');
const bgCtx = bgCanvas.getContext('2d');
let W, H;

function resizeBg() {
  W = bgCanvas.width = window.innerWidth;
  H = bgCanvas.height = window.innerHeight;
}
resizeBg();
window.addEventListener('resize', resizeBg);

const nodes = [];
for (let i = 0; i < 40; i++) {
  nodes.push({
    x: Math.random() * 1400,
    y: Math.random() * 1200,
    vx: (Math.random() - 0.5) * 0.3,
    vy: (Math.random() - 0.5) * 0.3
  });
}

function drawBg() {
  bgCtx.clearRect(0, 0, W, H);

  // Draw circuit-like connections
  bgCtx.strokeStyle = '#58a6ff';
  bgCtx.lineWidth = 0.5;

  for (let i = 0; i < nodes.length; i++) {
    for (let j = i + 1; j < nodes.length; j++) {
      const dx = nodes[i].x - nodes[j].x;
      const dy = nodes[i].y - nodes[j].y;
      const d = Math.sqrt(dx*dx + dy*dy);
      if (d < 160) {
        bgCtx.globalAlpha = (1 - d/160) * 0.6;
        bgCtx.beginPath();
        // Circuit-style: go horizontal then vertical
        bgCtx.moveTo(nodes[i].x, nodes[i].y);
        bgCtx.lineTo(nodes[j].x, nodes[i].y);
        bgCtx.lineTo(nodes[j].x, nodes[j].y);
        bgCtx.stroke();
      }
    }
  }

  bgCtx.globalAlpha = 1;
  // Draw nodes as small squares (circuit pads)
  nodes.forEach(n => {
    bgCtx.fillStyle = '#58a6ff';
    bgCtx.globalAlpha = 0.5;
    bgCtx.fillRect(n.x - 2, n.y - 2, 4, 4);
  });
  bgCtx.globalAlpha = 1;

  nodes.forEach(n => {
    n.x += n.vx;
    n.y += n.vy;
    if (n.x < 0 || n.x > 1400) n.vx *= -1;
    if (n.y < 0 || n.y > 1200) n.vy *= -1;
  });

  requestAnimationFrame(drawBg);
}
drawBg();

// ── TYPING ANIMATION ──
const phrases = [
  "Building tech that matters",
  "Explainable AI researcher",
  "Flutter developer",
  "Computer Vision engineer",
  "Cybersecurity explorer",
  "Open to collaboration 🤝"
];
let phraseIdx = 0, charIdx = 0, deleting = false;
const typingEl = document.getElementById('typing-text');

function type() {
  const phrase = phrases[phraseIdx];
  if (!deleting) {
    typingEl.textContent = phrase.slice(0, charIdx++);
    if (charIdx > phrase.length) { deleting = true; setTimeout(type, 1800); return; }
  } else {
    typingEl.textContent = phrase.slice(0, charIdx--);
    if (charIdx < 0) { deleting = false; phraseIdx = (phraseIdx + 1) % phrases.length; charIdx = 0; }
  }
  setTimeout(type, deleting ? 40 : 70);
}
type();

// ── RADAR CHART ──
function drawRadar() {
  const canvas = document.getElementById('radarChart');
  if (!canvas) return;
  const ctx = canvas.getContext('2d');
  const cx = 100, cy = 100, r = 80;
  const skills = [
    { label: 'Mobile', val: 0.90, color: '#58a6ff' },
    { label: 'DL', val: 0.85, color: '#3fb950' },
    { label: 'XAI', val: 0.80, color: '#bc8cff' },
    { label: 'CV', val: 0.82, color: '#f78166' },
    { label: 'Sec', val: 0.72, color: '#e3b341' },
    { label: 'BE', val: 0.78, color: '#58a6ff' }
  ];
  const n = skills.length;
  const angle = (i) => (Math.PI * 2 * i / n) - Math.PI / 2;

  ctx.clearRect(0, 0, 200, 200);

  // Grid circles
  [0.25, 0.5, 0.75, 1].forEach(frac => {
    ctx.beginPath();
    for (let i = 0; i < n; i++) {
      const a = angle(i);
      ctx.lineTo(cx + Math.cos(a) * r * frac, cy + Math.sin(a) * r * frac);
    }
    ctx.closePath();
    ctx.strokeStyle = 'rgba(48,54,61,0.8)';
    ctx.lineWidth = 0.5;
    ctx.stroke();
  });

  // Spokes
  skills.forEach((s, i) => {
    const a = angle(i);
    ctx.beginPath();
    ctx.moveTo(cx, cy);
    ctx.lineTo(cx + Math.cos(a) * r, cy + Math.sin(a) * r);
    ctx.strokeStyle = 'rgba(48,54,61,0.8)';
    ctx.lineWidth = 0.5;
    ctx.stroke();
  });

  // Filled polygon
  ctx.beginPath();
  skills.forEach((s, i) => {
    const a = angle(i);
    ctx.lineTo(cx + Math.cos(a) * r * s.val, cy + Math.sin(a) * r * s.val);
  });
  ctx.closePath();
  ctx.fillStyle = 'rgba(88,166,255,0.12)';
  ctx.fill();
  ctx.strokeStyle = '#58a6ff';
  ctx.lineWidth = 1.5;
  ctx.stroke();

  // Labels
  skills.forEach((s, i) => {
    const a = angle(i);
    const lx = cx + Math.cos(a) * (r + 14);
    const ly = cy + Math.sin(a) * (r + 14);
    ctx.fillStyle = '#8b949e';
    ctx.font = '9px JetBrains Mono, monospace';
    ctx.textAlign = 'center';
    ctx.textBaseline = 'middle';
    ctx.fillText(s.label, lx, ly);
  });

  // Dots
  skills.forEach((s, i) => {
    const a = angle(i);
    ctx.beginPath();
    ctx.arc(cx + Math.cos(a)*r*s.val, cy + Math.sin(a)*r*s.val, 3, 0, Math.PI*2);
    ctx.fillStyle = s.color;
    ctx.fill();
  });
}
drawRadar();

// ── CONTRIBUTION GRAPH ──
function buildContrib() {
  const cont = document.getElementById('contrib-container');
  const weeks = 30;
  const row = document.createElement('div');
  row.className = 'contrib-row';
  const levels = ['', 'l1', 'l2', 'l3', 'l4'];
  for (let w = 0; w < weeks; w++) {
    const col = document.createElement('div');
    col.className = 'contrib-week';
    for (let d = 0; d < 7; d++) {
      const cell = document.createElement('div');
      const rand = Math.random();
      let lvl = '';
      if (rand > 0.6) lvl = levels[Math.floor(Math.random() * 4) + 1];
      cell.className = 'contrib-day ' + lvl;
      col.appendChild(cell);
    }
    row.appendChild(col);
  }
  cont.appendChild(row);
}
buildContrib();

// ── SKILL BAR ANIMATION ──
function animateBars() {
  document.querySelectorAll('.bar-fill').forEach(bar => {
    const pct = bar.dataset.pct;
    bar.style.width = pct + '%';
  });
}

// ── COUNT-UP ──
function countUp(id, target, suffix) {
  const el = document.getElementById(id);
  let val = 0;
  const step = Math.ceil(target / 40);
  const iv = setInterval(() => {
    val = Math.min(val + step, target);
    el.textContent = val + (suffix || '');
    if (val >= target) clearInterval(iv);
  }, 40);
}

// ── REVEAL ON SCROLL ──
const reveals = document.querySelectorAll('.reveal');
let animated = false;

const obs = new IntersectionObserver((entries) => {
  entries.forEach((entry, i) => {
    if (entry.isIntersecting) {
      setTimeout(() => entry.target.classList.add('visible'), i * 80);
      obs.unobserve(entry.target);
    }
  });
}, { threshold: 0.1 });

reveals.forEach(el => obs.observe(el));

// Trigger stats when visible
const statsSection = document.querySelector('.stats-row');
const statsObs = new IntersectionObserver((entries) => {
  if (entries[0].isIntersecting && !animated) {
    animated = true;
    countUp('c1', 10);
    countUp('c2', 35);
    countUp('c3', 4);
    animateBars();
  }
}, { threshold: 0.3 });
if (statsSection) statsObs.observe(statsSection);

// Also trigger bars when skill section visible
const skillSection = document.getElementById('skill-bars');
const skillObs = new IntersectionObserver((entries) => {
  if (entries[0].isIntersecting) {
    setTimeout(animateBars, 300);
    skillObs.unobserve(entries[0].target);
  }
}, { threshold: 0.3 });
if (skillSection) skillObs.observe(skillSection);

// Trigger immediately if in view
setTimeout(() => {
  animateBars();
  countUp('c1', 10);
  countUp('c2', 35);
  countUp('c3', 4);
  reveals.forEach(el => el.classList.add('visible'));
}, 400);
</script>
</body>
</html>
