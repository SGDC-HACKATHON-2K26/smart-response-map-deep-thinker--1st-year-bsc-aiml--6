# smart-response-map-deep-thinker--1st-year-bsc-aiml--6
SGDC-6=deep thinker
Smart Response Map — An intelligent emergency response and mapping platform designed to visualize incidents, map critical locations, and support faster, data-driven emergency coordination. Developed by Team Deep Thinker, 1st Year B.Sc. AI & ML, for SGDC HACKATHON 2K26.



<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080c1c">
<meta name="description" content="Meet Team Deep Thinker, creators of Smart Response Map at SGDC HACKATHON 2K26.">
<title>Team Deep Thinker | SGDC HACKATHON 2K26</title>

<style>
:root {
  --bg: #080c1c;
  --panel: rgba(18, 27, 53, .78);
  --cyan: #55f4e8;
  --purple: #a78bfa;
  --text: #f2f5ff;
  --muted: #9daac8;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: Inter, "Segoe UI", Arial, sans-serif;
  overflow-x: hidden;
  line-height: 1.6;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: -1;
  background:
    radial-gradient(ellipse at 15% 20%, #163f6370, transparent 40%),
    radial-gradient(ellipse at 85% 65%, #572d8260, transparent 42%);
}

a { color: inherit; text-decoration: none; }

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  padding: 22px 7%;
  border-bottom: 1px solid #ffffff12;
}

.brand {
  font-weight: 900;
  letter-spacing: 2px;
  font-size: 15px;
}

.brand span { color: var(--cyan); }

nav a:last-child {
  color: var(--cyan);
  border: 1px solid #55f4e855;
  border-radius: 30px;
  padding: 9px 17px;
  font-size: 13px;
}

.hero {
  min-height: 76vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 95px 22px 80px;
  position: relative;
}

.eyebrow {
  border: 1px solid #55f4e84a;
  color: var(--cyan);
  background: #55f4e80b;
  border-radius: 30px;
  padding: 8px 17px;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
}

.hero h1 {
  font-size: clamp(48px, 10vw, 104px);
  line-height: 1.04;
  letter-spacing: -4px;
  margin: 28px 0 20px;
}

.hero h1 span {
  display: block;
  background: linear-gradient(100deg, var(--cyan), #a5b4fc, var(--purple));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.hero p {
  max-width: 650px;
  color: var(--muted);
  font-size: 17px;
}

.actions {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 32px;
}

.btn {
  display: inline-block;
  padding: 13px 23px;
  border-radius: 12px;
  font-weight: 800;
  font-size: 13px;
  transition: transform .2s, box-shadow .2s;
}

.btn:hover { transform: translateY(-3px); }

.primary {
  color: #08131c;
  background: var(--cyan);
  box-shadow: 0 0 28px #55f4e82b;
}

.secondary {
  border: 1px solid #ffffff25;
  background: #ffffff08;
}

.orbit {
  width: 150px;
  height: 150px;
  border: 1px solid #55f4e850;
  border-radius: 50%;
  display: grid;
  place-items: center;
  margin-bottom: 35px;
  position: relative;
  box-shadow: 0 0 50px #55f4e815, inset 0 0 40px #a78bfa10;
}

.orbit::before, .orbit::after {
  content: "";
  position: absolute;
  border: 1px dashed #a78bfa65;
  border-radius: 50%;
  inset: 13px;
  animation: spin 18s linear infinite;
}

.orbit::after {
  inset: -10px;
  border-color: #55f4e830;
  animation-direction: reverse;
  animation-duration: 26s;
}

.orbit span { font-size: 54px; }

@keyframes spin { to { transform: rotate(360deg); } }

.section {
  max-width: 1120px;
  padding: 75px 24px;
  margin: auto;
}

.section-label {
  color: var(--cyan);
  text-transform: uppercase;
  font-size: 11px;
  font-weight: 900;
  letter-spacing: 3px;
}

.section h2 {
  font-size: clamp(29px, 5vw, 46px);
  margin: 8px 0 14px;
  letter-spacing: -1px;
}

.intro {
  max-width: 680px;
  color: var(--muted);
  margin-bottom: 32px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 20px;
}

.card {
  border: 1px solid #ffffff14;
  background: var(--panel);
  border-radius: 20px;
  padding: 27px;
  backdrop-filter: blur(12px);
  transition: transform .25s, border-color .25s;
}

.card:hover {
  transform: translateY(-5px);
  border-color: #55f4e877;
}

.icon {
  width: 52px;
  height: 52px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, #55f4e821, #a78bfa22);
  border-radius: 15px;
  font-size: 25px;
  margin-bottom: 22px;
}

.card h3 { font-size: 19px; margin-bottom: 10px; }
.card p { color: var(--muted); font-size: 14px; }

.team-panel {
  border: 1px solid #55f4e82b;
  background: linear-gradient(120deg, #55f4e80b, #a78bfa12);
  border-radius: 24px;
  padding: clamp(25px, 5vw, 48px);
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
  align-items: center;
}

.team-mark {
  width: 120px;
  height: 120px;
  border-radius: 30px;
  display: grid;
  place-items: center;
  font-size: 52px;
  margin-bottom: 24px;
  background: linear-gradient(135deg, #55f4e82a, #a78bfa30);
  border: 1px solid #ffffff20;
}

.team-panel p { color: var(--muted); }

.team-details {
  display: grid;
  gap: 12px;
}

.detail {
  padding: 15px 17px;
  border: 1px solid #ffffff12;
  background: #080c1c75;
  border-radius: 12px;
}

.detail small {
  display: block;
  color: var(--muted);
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
}

.detail strong { font-size: 14px; overflow-wrap: anywhere; }

.manifesto {
  text-align: center;
  border-top: 1px solid #ffffff10;
  border-bottom: 1px solid #ffffff10;
  background: #ffffff03;
  padding: 75px 20px;
}

.manifesto blockquote {
  font-size: clamp(24px, 5vw, 44px);
  font-weight: 800;
  line-height: 1.35;
  max-width: 850px;
  margin: 18px auto;
}

.manifesto blockquote span { color: var(--cyan); }

footer {
  text-align: center;
  padding: 30px 20px;
  color: var(--muted);
  font-size: 12px;
}

footer strong { color: var(--cyan); }

@media (max-width: 760px) {
  .grid { grid-template-columns: 1fr; }
  .team-panel { grid-template-columns: 1fr; }
  .hero h1 { letter-spacing: -2px; }
  nav { padding: 18px 5%; }
  .section { padding-top: 55px; padding-bottom: 55px; }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: .01ms !important;
    scroll-behavior: auto !important;
    transition-duration: .01ms !important;
  }
}
</style>
</head>

<body>

<nav>
  <a href="#" class="brand">DEEP<span>THINKER</span></a>
  <a href="#team">MEET THE TEAM ↗</a>
</nav>

<header class="hero">
  <div class="orbit" aria-hidden="true"><span>⌖</span></div>

  <div class="eyebrow">SGDC HACKATHON 2K26 · TEAM SHOWCASE</div>

  <h1>Think Deep.<span>Build Smart.</span></h1>

  <p>
    We are Team Deep Thinker, a first-year B.Sc. AI &amp; ML team
    turning intelligent ideas into meaningful technology.
    Meet our vision: Smart Response Map.
  </p>

  <div class="actions">
    <a class="btn primary" href="#project">EXPLORE OUR PROJECT ↗</a>
    <a class="btn secondary" href="#team">OUR TEAM ↓</a>
  </div>
</header>

<main>
  <section class="section" id="project">
    <div class="section-label">01 / The Mission</div>
    <h2>Intelligence with a purpose.</h2>
    <p class="intro">
      Smart Response Map is our hackathon project concept focused on
      location-based incident visualization and smarter emergency
      coordination. Our goal is to explore how mapping and technology
      can help people understand situations and coordinate responses.
    </p>

    <div class="grid">
      <article class="card">
        <div class="icon">⌖</div>
        <h3>Map the Situation</h3>
        <p>Present relevant locations and incident information in a clear, map-oriented interface.</p>
      </article>

      <article class="card">
        <div class="icon">◈</div>
        <h3>Connect the Data</h3>
        <p>Bring available information together to make location-based insights easier to understand.</p>
      </article>

      <article class="card">
        <div class="icon">⚡</div>
        <h3>Support Response</h3>
        <p>Explore ways to help people coordinate, prioritize information, and make informed decisions.</p>
      </article>
    </div>
  </section>

  <section class="section" id="team">
    <div class="section-label">02 / The People</div>
    <h2>Meet the minds behind the map.</h2>
    <p class="intro">
      A team built around curiosity, collaboration, experimentation,
      and the courage to turn an idea into a prototype.
    </p>

    <div class="team-panel">
      <div>
        <div class="team-mark" aria-hidden="true">🧠</div>
        <div class="section-label">TEAM IDENTITY</div>
        <h2>Deep Thinker</h2>
        <p>
          First Year · B.Sc. Artificial Intelligence &amp; Machine Learning.
          Learning, building, testing, and improving together.
        </p>
      </div>

      <div class="team-details">
        <div class="detail">
          <small>Project</small>
          <strong>Smart Response Map</strong>
        </div>
        <div class="detail">
          <small>Event</small>
          <strong>SGDC HACKATHON 2K26</strong>
        </div>
        <div class="detail">
          <small>Institution</small>
          <strong>Shri Gnanambica Degree College (Autonomous)</strong>
        </div>
        <div class="detail">
          <small>Team Members</small>
          <strong>Meet our contributors in the project repository</strong>
        </div>
      </div>
    </div>
  </section>

  <section class="manifesto">
    <div class="section-label">03 / Our Philosophy</div>
    <blockquote>
      “Great ideas begin with questions.<br>
      <span>Great solutions begin with teamwork.</span>”
    </blockquote>
    <p style="color: var(--muted)">
      THINK · DESIGN · BUILD · TEST · IMPROVE
    </p>
  </section>

  <section class="section">
    <div class="section-label">04 / Explore</div>
    <h2>Follow the journey.</h2>
    <p class="intro">
      Explore our code, review our implementation, and follow our progress.
    </p>

    <a
      class="btn primary"
      href="https://github.com/SGDC-HACKATHON-2K26/smart-response-map-deep-thinker--1st-year-bsc-aiml--6"
      target="_blank"
      rel="noopener noreferrer"
    >
      VIEW PROJECT ON GITHUB ↗
    </a>
  </section>
</main>

<footer>
  <p><strong>DEEP THINKER</strong> · SGDC HACKATHON 2K26</p>
  <p>Built with curiosity. Driven by ideas. United by innovation.</p>
  <p>© 2026 Team Deep Thinker</p>
</footer>

</body>
</html>
