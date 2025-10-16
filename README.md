# Webpage
## Nazmul.Bhuiyan Web Exercise

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>World Environment</title>
  <meta name="description" content="World Environment — awareness, actions, and projects to protect our planet." />

  <!-- Simple Open Graph -->
  <meta property="og:title" content="World Environment" />
  <meta property="og:description" content="Awareness, actions, and projects to protect our planet." />
  <meta property="og:type" content="website" />
  <meta property="og:image" content="https://images.unsplash.com/photo-1501785888041-af3ef285b470?q=80&w=1200&auto=format&fit=crop&crop=entropy" />

  <style>
    :root{
      --bg: #f7fbf7;
      --card: #ffffff;
      --muted: #55606a;
      --accent: #2b8a6b;
      --accent-2: #2b6b8a;
      --glass: rgba(255,255,255,0.6);
      --radius: 14px;
      --shadow: 0 6px 24px rgba(16,24,40,0.06);
      color-scheme: light;
      --transition: 250ms ease;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    [data-theme="dark"]{
      --bg: #071018;
      --card: #071b1f;
      --muted: #9fb6b0;
      --accent: #49c39a;
      --accent-2: #4fb6d1;
      --glass: rgba(255,255,255,0.04);
      color-scheme: dark;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background: linear-gradient(180deg,var(--bg), #eaf6f0 60%);
      font-size:16px;
      line-height:1.5;
      color:var(--muted);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      transition:background var(--transition), color var(--transition);
      padding:24px;
      display:flex;
      justify-content:center;
      font-family:inherit;
    }

    .container{
      width:100%;
      max-width:1100px;
      margin:0 auto;
    }

    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      margin-bottom:18px;
    }

    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      text-decoration:none;
      color:inherit;
    }

    .logo{
      width:56px;
      height:56px;
      border-radius:12px;
      background: linear-gradient(135deg,var(--accent),var(--accent-2));
      display:grid;
      place-items:center;
      color:white;
      font-weight:700;
      box-shadow: var(--shadow);
      flex:0 0 56px;
    }

    nav{
      display:flex;
      gap:12px;
      align-items:center;
      flex-wrap:wrap;
    }

    a.btn{
      background:var(--card);
      padding:8px 14px;
      border-radius:10px;
      text-decoration:none;
      color:var(--muted);
      box-shadow: var(--shadow);
      transition:transform var(--transition), box-shadow var(--transition);
      font-weight:600;
    }
    a.btn:hover{ transform:translateY(-4px) }

    .hero{
      background: linear-gradient(90deg, rgba(43,138,107,0.08), rgba(43,107,138,0.06));
      border-radius: var(--radius);
      padding:28px;
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:18px;
      align-items:center;
      box-shadow: var(--shadow);
      margin-bottom:22px;
    }

    .hero h1{
      margin:0 0 8px 0;
      font-size: clamp(22px, 3.6vw, 36px);
      color: #0d2b28;
    }
    [data-theme="dark"] .hero h1{ color: #d9fff0 }

    .lead{
      margin:0 0 16px 0;
      color:var(--muted);
      font-size:1rem;
    }

    .cta-row{ display:flex; gap:10px; align-items:center; flex-wrap:wrap }
    .primary{
      background: linear-gradient(90deg,var(--accent),var(--accent-2));
      color:white;
      padding:10px 16px;
      border-radius:10px;
      text-decoration:none;
      font-weight:700;
      box-shadow: 0 6px 20px rgba(43,138,107,0.18);
    }

    .secondary{
      background:transparent;
      border:1px solid rgba(0,0,0,0.06);
      padding:9px 14px;
      border-radius:10px;
      text-decoration:none;
      color:var(--muted);
      font-weight:600;
    }

    .hero-visual{
      border-radius:12px;
      overflow:hidden;
      box-shadow: 0 12px 34px rgba(10,20,30,0.08);
      min-height:190px;
      background-image: url('https://images.unsplash.com/photo-1501785888041-af3ef285b470?q=80&w=1200&auto=format&fit=crop&crop=entropy');
      background-size:cover;
      background-position:center;
      position:relative;
      display:flex;
      align-items:flex-end;
    }
    .hero-visual .caption{
      background: linear-gradient(0deg, rgba(0,0,0,0.38), transparent);
      padding:12px;
      color:white;
      width:100%;
      box-sizing:border-box;
      font-weight:600;
    }

    main{
      display:grid;
      grid-template-columns: 1fr 320px;
      gap:18px;
      align-items:start;
    }

    .card{
      background:var(--card);
      border-radius:12px;
      padding:18px;
      box-shadow: var(--shadow);
    }

    .grid-2{
      display:grid;
      grid-template-columns: repeat(2, 1fr);
      gap:12px;
    }

    h2{ margin:0 0 10px 0; color: #0a2b27 }
    [data-theme="dark"] h2{ color:#c9fff0 }
    p.small{ margin:0; font-size:0.95rem; color:var(--muted) }

    .issue{
      display:flex;
      gap:12px;
      align-items:flex-start;
    }
    .issue .icon{
      width:54px;
      height:54px;
      border-radius:10px;
      background:var(--glass);
      display:grid;
      place-items:center;
      font-weight:700;
      color:var(--accent);
      flex:0 0 54px;
    }

    .stats{
      display:flex;
      gap:10px;
      margin-top:10px;
    }
    .stat{
      flex:1;
      padding:10px;
      border-radius:10px;
      text-align:center;
      background:linear-gradient(180deg, rgba(255,255,255,0.6), rgba(255,255,255,0.3));
      box-shadow: 0 6px 18px rgba(8,12,20,0.04);
    }
    .stat strong{display:block; font-size:1.2rem; color:#0b362f}
    [data-theme="dark"] .stat strong{ color: #bff7df }

    .help-list{ list-style:none; padding:0; margin:0; display:grid; gap:8px }
    .help-list li{
      padding:10px;
      border-radius:10px;
      display:flex;
      gap:10px;
      align-items:center;
      background:var(--glass);
    }

    form input, form textarea{
      width:100%;
      padding:10px 12px;
      border-radius:10px;
      border:1px solid rgba(0,0,0,0.08);
      outline:none;
      font-size:1rem;
      background:transparent;
      color:inherit;
    }
    form label{ font-size:0.9rem; margin-bottom:6px; display:block; color:var(--muted) }

    footer{
      margin-top:20px;
      display:flex;
      justify-content:space-between;
      gap:12px;
      align-items:center;
      flex-wrap:wrap;
    }

    .small-muted{ font-size:0.88rem; color:var(--muted) }

    /* responsive */
    @media (max-width:980px){
      .hero{ grid-template-columns:1fr; }
      main{ grid-template-columns:1fr; }
      .hero-visual{ min-height:180px }
    }

    @media (max-width:480px){
      body{ padding:14px }
      .logo{ width:48px; height:48px }
    }
  </style>
</head>
<body data-theme="light">
  <div class="container" role="main">
    <header>
      <a href="#" class="brand" aria-label="World Environment homepage">
        <div class="logo" aria-hidden="true">WE</div>
        <div>
          <div style="font-weight:800; font-size:18px; line-height:1;">World Environment</div>
          <div style="font-size:12px; color:var(--muted)">Protect. Restore. Sustain.</div>
        </div>
      </a>

      <nav aria-label="Main navigation">
        <a class="btn" href="#about">About</a>
        <a class="btn" href="#actions">Take Action</a>
        <a class="btn" href="#projects">Projects</a>
        <button id="themeToggle" class="btn" aria-pressed="false" title="Toggle light/dark">Toggle theme</button>
      </nav>
    </header>

    <section class="hero" aria-labelledby="hero-title">
      <div>
        <h1 id="hero-title">Protecting the planet, one action at a time</h1>
        <p class="lead">World Environment is a community hub for awareness, small actions that add up, and scalable local projects focused on biodiversity, clean air, and climate resilience.</p>

        <div class="cta-row" role="group" aria-label="Call to action">
          <a class="primary" href="#actions">How to help</a>
          <a class="secondary" href="#projects">See our projects</a>
          <a class="secondary" href="#contact">Contact</a>
        </div>

        <div style="margin-top:16px" class="card" aria-hidden="false">
          <div style="display:flex; gap:12px; align-items:center; justify-content:space-between; flex-wrap:wrap">
            <div>
              <div style="font-size:13px; color:var(--muted)">Join our monthly micro-action</div>
              <div style="font-weight:700; font-size:16px">Plant native seeds — October challenge</div>
            </div>
            <div>
              <a class="primary" href="#join">Join challenge</a>
            </div>
          </div>
        </div>
      </div>

      <div class="hero-visual" role="img" aria-label="Lush forest and hands holding soil with a sprout">
        <div class="caption">Small seeds. Big future.</div>
      </div>
    </section>

    <main>
      <section>
        <article id="about" class="card" aria-labelledby="about-title">
          <h2 id="about-title">About the issue</h2>
          <p class="small">Ecosystems around the world are under pressure from climate change, habitat loss, pollution, and unsustainable resource use. Many solutions are known and low-cost — what’s missing is collective action and local implementation at scale.</p>

          <div style="margin-top:14px" class="grid-2">
            <div class="card" style="padding:12px;">
              <h3 style="margin-top:0;margin-bottom:8px">Why it matters</h3>
              <p class="small">Healthy environments provide food, clean water, stable climate, and livelihoods. Protecting biodiversity also reduces pandemic risk and supports resilient communities.</p>
            </div>

            <div class="card" style="padding:12px;">
              <h3 style="margin-top:0;margin-bottom:8px">Our focus areas</h3>
              <ul style="margin:0 0 0 18px; color:var(--muted)">
                <li>Restoration & native planting</li>
                <li>Plastic reduction & circularity</li>
                <li>Clean energy advocacy</li>
                <li>Community education & youth programs</li>
              </ul>
            </div>
          </div>

          <div style="margin-top:16px" class="stats" aria-hidden="false">
            <div class="stat">
              <strong>120K+</strong>
              <div class="small-muted">People reached</div>
            </div>
            <div class="stat">
              <strong>2,400+</strong>
              <div class="small-muted">Trees & native plants planted</div>
            </div>
            <div class="stat">
              <strong>48</strong>
              <div class="small-muted">Local projects active</div>
            </div>
          </div>
        </article>

        <article id="actions" class="card" style="margin-top:18px" aria-labelledby="actions-title">
          <h2 id="actions-title">Simple actions you can take today</h2>

          <ul class="help-list" aria-label="List of actions">
            <li><strong style="width:110px;display:inline-block">Reduce waste</strong> — Bring a reusable bottle and shopping bag; choose products with less packaging.</li>
            <li><strong style="width:110px;display:inline-block">Plant native</strong> — Even a small pot of native plants helps pollinators.</li>
            <li><strong style="width:110px;display:inline-block">Conserve water</strong> — Shorter showers and fixing leaks make a difference.</li>
            <li><strong style="width:110px;display:inline-block">Learn & share</strong> — Talk to friends and vote for green policies.</li>
          </ul>
        </article>

        <article id="projects" class="card" style="margin-top:18px" aria-labelledby="projects-title">
          <h2 id="projects-title">Featured local projects</h2>

          <div style="display:grid; gap:12px; margin-top:8px;">
            <div class="issue">
              <div class="icon" aria-hidden="true">🌱</div>
              <div>
                <div style="font-weight:700">Riverbank Restoration — Sundarbans buffer</div>
                <div class="small-muted">Protecting wetlands by planting native mangroves and building local stewardship programs.</div>
              </div>
            </div>

            <div class="issue">
              <div class="icon" aria-hidden="true">♻️</div>
              <div>
                <div style="font-weight:700">Plastics to Products — Dhaka pilot</div>
                <div class="small-muted">Turning collected waste into building blocks and community assets.</div>
              </div>
            </div>
          </div>
        </article>
      </section>

      <aside>
        <div class="card" id="join" aria-labelledby="join-title">
          <h2 id="join-title">Get involved</h2>
          <p class="small">Sign up for monthly micro-actions and local event alerts.</p>

          <form id="signup" style="margin-top:10px" onsubmit="event.preventDefault(); alert('Thanks — this is a demo signup.');">
            <label for="name">Name</label>
            <input id="name" name="name" type="text" placeholder="Your name" required />

            <label for="email" style="margin-top:8px">Email</label>
            <input id="email" name="email" type="email" placeholder="you@example.com" required />

            <div style="margin-top:10px; display:flex; gap:8px;">
              <button type="submit" class="primary" style="flex:1">Sign up</button>
              <a href="#projects" class="secondary" style="display:inline-block; padding:10px 12px; align-self:center">See projects</a>
            </div>
          </form>
        </div>

        <div class="card" id="contact" style="margin-top:12px;">
          <h2 style="margin-top:0">Contact</h2>
          <p class="small">Questions, collaboration proposals, or media enquiries? Send a message.</p>

          <form style="margin-top:8px" onsubmit="event.preventDefault(); alert('Message sent (demo).');">
            <label for="msg-name">Name</label>
            <input id="msg-name" type="text" placeholder="Name" required />

            <label for="msg-email" style="margin-top:8px">Email</label>
            <input id="msg-email" type="email" placeholder="Email" required />

            <label for="message" style="margin-top:8px">Message</label>
            <textarea id="message" rows="4" placeholder="How can we help?" required></textarea>

            <div style="margin-top:10px;">
              <button class="primary" type="submit">Send</button>
            </div>
          </form>
        </div>

        <div class="card" style="margin-top:12px;">
          <h3 style="margin:0 0 8px 0">Quick tips</h3>
          <ol style="margin:0 0 0 16px; color:var(--muted)">
            <li>Buy local & seasonal produce.</li>
            <li>Fix & repair before replacing.</li>
            <li>Support protected areas and community projects.</li>
          </ol>
        </div>
      </aside>
    </main>

    <footer>
      <div class="small-muted">© <span id="year"></span> World Environment · Built with care</div>
      <div style="display:flex; gap:12px; align-items:center;">
        <a class="btn" href="#" title="Privacy">Privacy</a>
        <a class="btn" href="#" title="Terms">Terms</a>
        <a class="primary" href="#" style="padding:8px 12px">Donate</a>
      </div>
    </footer>
  </div>

  <script>
    // Small interactive helpers (theme toggle and year)
    (function(){
      const body = document.body;
      const toggle = document.getElementById('themeToggle');
      const year = document.getElementById('year');
      year.textContent = new Date().getFullYear();

      function setTheme(name){
        body.setAttribute('data-theme', name);
        const pressed = (name === 'dark');
        toggle.setAttribute('aria-pressed', String(pressed));
      }

      // initialize from localStorage if available
      const saved = localStorage.getItem('we-theme');
      if(saved) setTheme(saved);

      toggle.addEventListener('click', () => {
        const current = body.getAttribute('data-theme') || 'light';
        const next = current === 'light' ? 'dark' : 'light';
        setTheme(next);
        localStorage.setItem('we-theme', next);
      });

      // small progressive enhancement: reduce motion respect
      const prefersReduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
      if(prefersReduced){
        document.documentElement.style.scrollBehavior = 'auto';
      }
    })();
  </script>
</body>
</html>
