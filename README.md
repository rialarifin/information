<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rial Arifin Rajagukguk, PhD</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #ffffff;
    --bg-panel: #f7f8fa;
    --bg-panel-2: #eef1f4;
    --sun: #e8912b;
    --sun-soft: #b5680f;
    --sky: #2f6f88;
    --coral: #d15b34;
    --text: #14202e;
    --text-dim: #566579;
    --text-faint: #8a97a8;
    --line: rgba(20,32,46,0.10);
    --line-strong: rgba(20,32,46,0.16);
    --radius: 14px;
  }

  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}

  body{
    background:
      radial-gradient(ellipse 900px 500px at 85% -5%, rgba(232,145,43,0.07), transparent 60%),
      radial-gradient(ellipse 700px 500px at -5% 20%, rgba(47,111,136,0.07), transparent 55%),
      var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  h1,h2,h3, .display{
    font-family: 'Space Grotesk', sans-serif;
    letter-spacing: -0.01em;
  }

  .mono{
    font-family: 'IBM Plex Mono', monospace;
    letter-spacing: 0.02em;
  }

  a{ color: var(--sun-soft); text-decoration: none; }
  a:hover{ text-decoration: underline; text-underline-offset: 3px; }
  a:focus-visible, button:focus-visible{ outline: 2px solid var(--sun); outline-offset: 3px; border-radius: 4px; }

  ::selection{ background: rgba(242,169,59,0.30); }

  /* ---------- layout shell ---------- */
  .wrap{ max-width: 920px; margin: 0 auto; padding: 0 28px; }

  /* ---------- nav ---------- */
  nav{
    position: sticky; top: 0; z-index: 50;
    background: rgba(255,255,255,0.86);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--line);
  }
  .nav-inner{
    max-width: 920px; margin: 0 auto; padding: 14px 28px;
    display:flex; align-items:center; justify-content:space-between;
    gap: 16px;
  }
  .nav-brand{
    display:flex; align-items:center; gap:10px;
    font-family:'Space Grotesk', sans-serif; font-weight:600; font-size:15px;
    color: var(--text); white-space:nowrap;
  }
  .nav-brand svg{ flex-shrink:0; }
  .nav-links{
    display:flex; gap: 22px; overflow-x:auto; scrollbar-width:none;
    font-size: 13px; font-family:'IBM Plex Mono', monospace;
  }
  .nav-links::-webkit-scrollbar{ display:none; }
  .nav-links a{
    color: var(--text-dim); white-space:nowrap; padding: 4px 0;
    border-bottom: 1px solid transparent; transition: color .15s, border-color .15s;
  }
  .nav-links a:hover{ color: var(--sun-soft); text-decoration:none; border-color: var(--sun); }

  /* ---------- sky-cam signature graphic ---------- */
  .skycam-ring{ display:block; }
  .skycam-ring circle.field{ fill:none; stroke: var(--line-strong); }
  .skycam-ring circle.ring{ fill:none; stroke: var(--sky); opacity:0.5; }
  .skycam-ring .sun-dot{ fill: var(--sun); }
  .skycam-ring .tick{ stroke: var(--text-faint); }

  /* ---------- hero ---------- */
  .hero{
    padding: 88px 0 64px;
    position: relative;
    overflow: hidden;
  }
  .hero-grid{
    display:grid; grid-template-columns: 1.15fr 0.85fr; gap: 48px; align-items:center;
  }
  .eyebrow{
    font-family:'IBM Plex Mono', monospace; font-size: 12.5px; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--sun-soft); margin-bottom: 18px;
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{
    content:""; width: 22px; height:1px; background: var(--sun);
  }
  .hero h1{
    font-size: clamp(34px, 5.4vw, 52px); font-weight: 700; line-height: 1.08;
    margin-bottom: 18px;
  }
  .hero h1 .accent{ color: var(--sun); }
  .hero p.lede{
    font-size: 16.5px; color: var(--text-dim); max-width: 54ch; margin-bottom: 26px;
  }
  .hero-links{ display:flex; flex-wrap:wrap; gap: 10px; }
  .pill{
    display:inline-flex; align-items:center; gap:7px;
    font-family:'IBM Plex Mono', monospace; font-size: 12.5px;
    color: var(--text); border: 1px solid var(--line-strong);
    padding: 8px 14px; border-radius: 999px; transition: all .15s;
  }
  .pill:hover{ border-color: var(--sun); color: var(--sun-soft); text-decoration:none; background: rgba(242,169,59,0.06); }

  .hero-portrait{
    position: relative; display:flex; align-items:center; justify-content:center;
  }
  .fisheye{
    width: 100%; max-width: 320px; aspect-ratio: 1/1; border-radius: 50%;
    position: relative; overflow:hidden;
    background:
      radial-gradient(circle at 68% 30%, rgba(232,145,43,0.35), rgba(232,145,43,0) 38%),
      conic-gradient(from 200deg, #e7eef2, #f7f8fa 40%, #f7f8fa 60%, #e2ecf1);
    border: 1px solid var(--line-strong);
    box-shadow: 0 0 0 1px rgba(20,32,46,0.05), 0 30px 60px -25px rgba(20,32,46,0.25), inset 0 0 40px rgba(20,32,46,0.06);
  }
  .fisheye img{
    position:absolute; inset:0; width:100%; height:100%; object-fit:cover;
    opacity: 0.9;
  }
  .fisheye .ring-overlay{ position:absolute; inset:0; width:100%; height:100%; }
  .fisheye-caption{
    position:absolute; bottom: -30px; left:50%; transform:translateX(-50%);
    font-family:'IBM Plex Mono', monospace; font-size: 11px; color: var(--text-faint);
    white-space:nowrap;
  }

  /* ---------- sections ---------- */
  section{ padding: 76px 0; border-top: 1px solid var(--line); }
  section:first-of-type{ border-top:none; }

  .section-head{
    display:flex; align-items:baseline; gap: 16px; margin-bottom: 40px;
  }
  .section-num{ font-family:'IBM Plex Mono', monospace; color: var(--sky); font-size: 13px; }
  .section-head h2{ font-size: 27px; font-weight: 600; }
  .section-sub{ color: var(--text-dim); font-size: 14.5px; margin: -28px 0 36px; max-width: 60ch; }

  /* ---------- about ---------- */
  .about-body{ color: var(--text-dim); font-size: 16px; max-width: 68ch; }
  .about-body strong{ color: var(--text); font-weight: 600; }

  /* ---------- timeline (education / experience) ---------- */
  .timeline{ position:relative; padding-left: 28px; }
  .timeline::before{
    content:""; position:absolute; left: 5px; top: 6px; bottom: 6px; width:1px;
    background: linear-gradient(var(--sun), var(--sky));
    opacity: 0.4;
  }
  .t-item{ position:relative; padding-bottom: 34px; }
  .t-item:last-child{ padding-bottom: 0; }
  .t-item::before{
    content:""; position:absolute; left: -28px; top: 6px;
    width: 11px; height: 11px; border-radius:50%;
    background: var(--bg); border: 2px solid var(--sun);
  }
  .t-date{
    font-family:'IBM Plex Mono', monospace; font-size: 12.5px; color: var(--sky);
    margin-bottom: 6px; display:block;
  }
  .t-item h3{ font-size: 17px; font-weight: 600; margin-bottom: 3px; }
  .t-item .t-org{ color: var(--text-dim); font-size: 14.5px; margin-bottom: 8px; }
  .t-item .t-org a{ color: var(--text-dim); }
  .t-item .t-desc{ font-style: italic; color: var(--text-dim); font-size: 14.5px; }
  .t-item ul{ margin-top: 8px; padding-left: 18px; color: var(--text-dim); font-size: 14.5px; }
  .t-item li{ margin-bottom: 5px; }
  .t-item li::marker{ color: var(--sun); }

  /* ---------- publications ---------- */
  .pub-year-block{ margin-bottom: 40px; }
  .pub-year-block:last-child{ margin-bottom: 0; }
  .pub-year-head{
    display:flex; align-items:center; gap: 14px; margin-bottom: 18px;
  }
  .pub-year-head .yr{
    font-family:'Space Grotesk', sans-serif; font-weight: 700; font-size: 26px; color: var(--sun);
  }
  .pub-year-head .yr-line{ flex:1; height:1px; background: var(--line-strong); }

  .pub-card{
    background: var(--bg-panel);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    padding: 18px 20px;
    margin-bottom: 12px;
    transition: border-color .15s, transform .15s, background .15s;
  }
  .pub-card:hover{ border-color: var(--sky); transform: translateY(-1px); background: var(--bg-panel-2); }
  .pub-card .pub-title{ font-size: 15px; font-weight: 500; color: var(--text); margin-bottom: 6px; }
  .pub-card .pub-title a{ color: var(--text); }
  .pub-card .pub-title a:hover{ color: var(--sun-soft); }
  .pub-card .pub-authors{ font-size: 13px; color: var(--text-dim); margin-bottom: 4px; }
  .pub-card .pub-authors .me{ color: var(--sun-soft); font-weight: 600; }
  .pub-card .pub-venue{ font-family:'IBM Plex Mono', monospace; font-size: 12px; color: var(--sky); }

  /* ---------- projects ---------- */
  .project-card{
    display:flex; justify-content:space-between; align-items:flex-start; gap: 20px;
    padding: 22px 0; border-bottom: 1px solid var(--line);
  }
  .project-card:last-child{ border-bottom:none; }
  .project-card h3{ font-size: 16px; font-weight:600; margin-bottom:4px; }
  .project-card .p-org{ color: var(--sky); font-size:13px; font-family:'IBM Plex Mono', monospace; margin-bottom:10px; }
  .project-card ul{ padding-left: 18px; color: var(--text-dim); font-size: 14px; }
  .project-card li{ margin-bottom: 4px; }
  .project-card li::marker{ color: var(--sun); }
  .p-date{
    font-family:'IBM Plex Mono', monospace; font-size: 12px; color: var(--text-faint);
    white-space:nowrap; padding-top: 3px;
  }

  /* ---------- awards / patent grid ---------- */
  .credential-grid{ display:grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .credential-card{
    background: var(--bg-panel); border:1px solid var(--line); border-radius: var(--radius);
    padding: 20px;
  }
  .credential-card .c-label{
    font-family:'IBM Plex Mono', monospace; font-size: 11px; text-transform:uppercase;
    letter-spacing:0.1em; color: var(--coral); margin-bottom: 10px; display:block;
  }
  .credential-card p{ font-size: 14.5px; color: var(--text); margin-bottom:4px; }
  .credential-card .c-meta{ font-size: 13px; color: var(--text-dim); }

  /* ---------- conferences ---------- */
  .conf-item{ padding: 20px 0; border-bottom: 1px solid var(--line); }
  .conf-item:last-child{ border-bottom: none; }
  .conf-item h3{ font-size: 16px; font-weight:600; margin-bottom: 4px; }
  .conf-meta{ font-family:'IBM Plex Mono', monospace; font-size:12.5px; color: var(--sky); margin-bottom:10px; }
  .conf-item .conf-talk{ font-size: 14px; color: var(--text-dim); margin-bottom: 4px; padding-left: 14px; position:relative; }
  .conf-item .conf-talk::before{ content:"—"; position:absolute; left:0; color: var(--sun); }

  /* ---------- footer ---------- */
  footer{
    padding: 48px 0 60px; text-align:center;
    color: var(--text-faint); font-size: 13px; font-family:'IBM Plex Mono', monospace;
  }
  footer a{ color: var(--text-dim); }

  /* ---------- reveal on scroll ---------- */
  .reveal{ opacity: 0; transform: translateY(14px); transition: opacity .6s ease, transform .6s ease; }
  .reveal.in{ opacity: 1; transform: translateY(0); }

  @media (prefers-reduced-motion: reduce){
    .reveal{ opacity:1; transform:none; transition:none; }
    html{ scroll-behavior:auto; }
  }

  /* ---------- responsive ---------- */
  @media (max-width: 760px){
    .hero-grid{ grid-template-columns: 1fr; }
    .hero-portrait{ order:-1; margin-bottom: 8px; }
    .fisheye{ max-width: 220px; }
    .credential-grid{ grid-template-columns: 1fr; }
    .nav-brand span.full{ display:none; }
    section{ padding: 56px 0; }
    .hero{ padding: 56px 0 40px; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <div class="nav-brand">
      <svg width="20" height="20" viewBox="0 0 40 40">
        <circle cx="20" cy="20" r="18" fill="none" stroke="#4f92ab" stroke-width="1" opacity="0.6"/>
        <circle cx="20" cy="20" r="11" fill="none" stroke="#4f92ab" stroke-width="1" opacity="0.4"/>
        <circle cx="27" cy="13" r="3.2" fill="#f2a93b"/>
      </svg>
      <span class="full">Rajagukguk</span>
    </div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#education">Education</a>
      <a href="#experience">Experience</a>
      <a href="#publications">Publications</a>
      <a href="#projects">Projects</a>
      <a href="#credentials">Awards</a>
      <a href="#conferences">Conferences</a>
    </div>
  </div>
</nav>

<div class="wrap">

  <!-- HERO -->
  <section class="hero" id="about" style="border-top:none;">
    <div class="hero-grid">
      <div>
        <div class="eyebrow">Solar Irradiance &middot; Remote Sensing &middot; Applied ML</div>
        <h1>Rial Arifin<br>Rajagukguk<span class="accent">, PhD</span></h1>
        <p class="lede">I build machine learning models that read the sky — turning sky‑camera and satellite imagery into solar irradiance forecasts for electric vehicles, buildings, and livestock environments.</p>
        <div class="hero-links">
          <a class="pill" href="https://scholar.google.com/citations?user=WdMsyCMAAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
          <a class="pill" href="https://github.com/rialarifin" target="_blank" rel="noopener">GitHub</a>
          <a class="pill" href="https://www.linkedin.com/in/rialarifin/" target="_blank" rel="noopener">LinkedIn</a>
          <a class="pill" href="https://www.researchgate.net/profile/Rial-Rajagukguk-2" target="_blank" rel="noopener">ResearchGate</a>
        </div>
      </div>
      <div class="hero-portrait">
        <div class="fisheye">
          <img src="Rial.jpeg" alt="Portrait of Rial Arifin Rajagukguk" onerror="this.style.display='none'">
          <svg class="ring-overlay" viewBox="0 0 320 320" xmlns="http://www.w3.org/2000/svg">
            <circle cx="160" cy="160" r="150" fill="none" stroke="rgba(20,32,46,0.14)" stroke-width="1"/>
            <circle cx="160" cy="160" r="100" fill="none" stroke="rgba(47,111,136,0.4)" stroke-width="1"/>
            <circle cx="160" cy="160" r="50" fill="none" stroke="rgba(47,111,136,0.28)" stroke-width="1"/>
            <line x1="160" y1="10" x2="160" y2="310" stroke="rgba(20,32,46,0.08)"/>
            <line x1="10" y1="160" x2="310" y2="160" stroke="rgba(20,32,46,0.08)"/>
          </svg>
        </div>
        <div class="fisheye-caption">// sky‑camera view, 08:24 KST</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section>
    <div class="about-body reveal">
      <p style="margin-bottom:16px;">As a researcher, I work across <strong>computer vision</strong>, <strong>machine learning</strong>, <strong>deep learning</strong>, <strong>remote sensing</strong>, <strong>electric vehicles</strong>, <strong>satellite technology</strong>, <strong>sky cameras</strong>, and <strong>solar energy</strong> — disciplines that meet at the point where atmospheric data becomes a usable prediction.</p>
      <p>My flagship project predicts solar irradiance by fusing sky‑camera and satellite imagery, feeding real‑time forecasts to <strong>electric vehicles in motion</strong> so they can optimize energy consumption ahead of the sun. It's a small piece of a larger goal: cutting carbon emissions by making renewable energy easier to plan around.</p>
    </div>
  </section>

  <!-- EDUCATION -->
  <section id="education">
    <div class="section-head reveal"><span class="section-num">01</span><h2>Education</h2></div>
    <div class="timeline">

      <div class="t-item reveal">
        <span class="t-date">2021 — 2024</span>
        <h3>PhD, Kookmin University</h3>
        <div class="t-org">South Korea · <a href="https://english.kookmin.ac.kr" target="_blank" rel="noopener">english.kookmin.ac.kr</a></div>
        <div class="t-desc">"Solar Radiation Prediction Based on the Images of Satellite and Sky Camera for the Energy Management of Electric Vehicles"</div>
      </div>

      <div class="t-item reveal">
        <span class="t-date">2019 — 2021</span>
        <h3>MSc, Kookmin University</h3>
        <div class="t-org">South Korea · <a href="https://english.kookmin.ac.kr" target="_blank" rel="noopener">english.kookmin.ac.kr</a></div>
        <div class="t-desc">"Solar Irradiance Forecasting using Sky Images"</div>
      </div>

      <div class="t-item reveal">
        <span class="t-date">2012 — 2017</span>
        <h3>BSc, Institut Teknologi Bandung</h3>
        <div class="t-org">Indonesia · <a href="https://www.itb.ac.id/" target="_blank" rel="noopener">itb.ac.id</a></div>
        <div class="t-desc">"Parametric Study of Cooling Film and Implementation on One Axial Turbine Blade Stage"</div>
      </div>

    </div>
  </section>

  <!-- EXPERIENCE -->
  <section id="experience">
    <div class="section-head reveal"><span class="section-num">02</span><h2>Work Experience</h2></div>
    <div class="timeline">

      <div class="t-item reveal">
        <span class="t-date">Jul 2025 — now</span>
        <h3>Postdoctoral Researcher</h3>
        <div class="t-org"><a href="https://www.afel-jnu.info/research-projects" target="_blank" rel="noopener">Agricultural Facilities and Environment Lab</a> · Chonnam National University</div>
        <ul><li>Livestock Transport 4.0: eco‑friendly animal welfare transport solutions.</li></ul>
      </div>

      <div class="t-item reveal">
        <span class="t-date">Sep 2024 — Jun 2025</span>
        <h3>Postdoctoral Researcher</h3>
        <div class="t-org"><a href="https://relab.kookmin.ac.kr/home" target="_blank" rel="noopener">Renewable Energy Lab</a> · Kookmin University</div>
        <ul><li>Solar irradiance and cabin air temperature forecasting for moving electric vehicles.</li></ul>
      </div>

      <div class="t-item reveal">
        <span class="t-date">2019</span>
        <h3>Student Researcher — Master's &amp; PhD</h3>
        <div class="t-org"><a href="https://relab.kookmin.ac.kr/home" target="_blank" rel="noopener">Renewable Energy Lab</a> · Kookmin University</div>
        <ul>
          <li>Calculated cloud motion vectors from satellite images using optical flow and computer vision (Python/OpenCV) for solar irradiance forecasting.</li>
          <li>Estimated minute‑level solar radiation time series across South Korea with RNN, LSTM, GRU, and CNN models.</li>
          <li>Separated direct and diffuse irradiance from global horizontal irradiance using deep learning and transfer learning.</li>
          <li>Forecasted cloud fraction at very short‑term horizons using sky‑camera imagery.</li>
          <li>Forecasted solar irradiance, temperature, and humidity for electric‑vehicle energy saving.</li>
        </ul>
      </div>

      <div class="t-item reveal">
        <span class="t-date">2017</span>
        <h3>CFD Engineer</h3>
        <div class="t-org"><a href="https://www.chromaintegrated.com/" target="_blank" rel="noopener">PT. Chroma International</a> · Bandung, Indonesia</div>
        <ul>
          <li>Designed and ran CFD analysis on a small‑scale blow‑down wind tunnel operating at supersonic (Mach 2.0) and subsonic (Mach 0.6) conditions.</li>
          <li>Designed and analyzed a 100 kW axial turbine.</li>
        </ul>
      </div>

    </div>
  </section>

  <!-- PUBLICATIONS -->
  <section id="publications">
    <div class="section-head reveal"><span class="section-num">03</span><h2>Published Papers</h2></div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2026</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://doi.org/10.4081/jae.2026.2096" target="_blank" rel="noopener">Estimating Indoor Heat Stress in Livestock Facilities Using High-Resolution Geo-KOMPSAT-2A Satellite Data</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Jinseon Park, Heejou Kim, Chae-rin Lee, Se-yeon Lee, Ji-yeon Park, Taehwan Ha, Se-woon Hong</div>
        <div class="pub-venue">Journal of Agricultural Engineering</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.espublisher.com/journals/articledetails/2171" target="_blank" rel="noopener">Feature Selection and Interpretability in Satellite-Based Solar Irradiance Estimation: Optimizing GEO-KOMPSAT-2A Multispectral Inputs for Tropical Environments</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Rezi Delfianti, Se-Woon Hong, Indra Ardhanayudha Aditya, Arief Heru Kuncoro, Sudirman Palaloi, Nur Aryanto Aryono, La Ode Muhammad Abdul Wahid, Supratikno, Murbantan Tandirerung, Pranda M.P. Garniwa, Hyunjin Lee</div>
        <div class="pub-venue">Engineered Science</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.korseaj.org/selectArticleInfo.do?article_a_no=HGNHB8_2026_v45_1&ano=HGNHB8_2026_v45_1" target="_blank" rel="noopener">Field Evaluation of Human Exposure to Pesticides and Comparison with Exposure Assessment Models: Drone and Wide-area Sprayer Applications</a></div>
        <div class="pub-authors">Se-yeon Lee, Ji-yeon Park, Jinseon Park, Chae-rin Lee, <span class="me">Rial A. Rajagukguk</span>, Youngho Kang, Hyun Ho Noh, Se-woon Hong</div>
        <div class="pub-venue">Agricultural and Environmental Sciences</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.sciencedirect.com/science/article/pii/S2352484726001095" target="_blank" rel="noopener">Solar Energy Estimation in Tropical Environments: A Novel Framework for Integrating Satellite and Sky Imager Data</a></div>
        <div class="pub-authors">Aditya, I. A., M. Soleh, H. Lee, P. M.P. Garniwa, M. F.B. Suhaimi, S.-W. Hong, <span class="me">Rial A. Rajagukguk</span></div>
        <div class="pub-venue">Energy Reports</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2025</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.nature.com/articles/s41598-025-31719-2" target="_blank" rel="noopener">Dynamic Solar Irradiance Estimation for Vehicle Thermal Management Using a Multi-Modal Machine Learning Framework</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Hoseong Lee, Hyunjin Lee</div>
        <div class="pub-venue">Scientific Reports</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.sciencedirect.com/science/article/pii/S2772375525007701" target="_blank" rel="noopener">Deep Learning for Visual Animal Monitoring (Detection, Tracking, Pose Estimation, and Behavior Classification): A Comprehensive Review</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Se-yeon Lee, Ji-yeon Park, Kehinde FavourDaniel, Chae-rin Lee, ZhengChencDongLiu, TomásNorton, Jinseon Park, Se-woon Hong</div>
        <div class="pub-venue">Smart Agricultural Technology</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.nature.com/articles/s41598-025-91158-x" target="_blank" rel="noopener">Application of Explainable Machine Learning for Estimating Direct and Diffuse Components of Solar Irradiance</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Hyunjin Lee</div>
        <div class="pub-venue">Scientific Reports</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2024</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://doi.org/10.1016/j.buildenv.2024.112429" target="_blank" rel="noopener">Sky-Image-Based Sun-Blocking Index and PredRNN++ for Accurate Short-Term Solar Irradiance Forecasting</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Hyunjin Lee</div>
        <div class="pub-venue">Building and Environment</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://ieeexplore.ieee.org/document/10667941" target="_blank" rel="noopener">Estimating Irradiance through Satellite-Driven Deep Learning Models</a></div>
        <div class="pub-authors">Indra A. Aditya, Pranda M. Putra, <span class="me">Rial A. Rajagukguk</span>, Yessy Asri</div>
        <div class="pub-venue">International Seminar on Intelligent Technology and Its Applications</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2023</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.ksesjournal.co.kr/articles/xml/qVn9/" target="_blank" rel="noopener">Enhancing the Performance of Solar Radiation Decomposition Models Using Deep Learning</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Hyunjin Lee</div>
        <div class="pub-venue">Journal of the Korean Solar Energy Society</div>
      </div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://doi.org/10.1016/j.solener.2023.01.037" target="_blank" rel="noopener">Intra-day Forecast of Global Horizontal Irradiance Using Optical Flow Method and Long Short-Term Memory Model</a></div>
        <div class="pub-authors">Pranda M. Putra, <span class="me">Rial A. Rajagukguk</span>, R. Kamil, Hyunjin Lee</div>
        <div class="pub-venue">Solar Energy</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2022</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://doi.org/10.1016/j.buildenv.2022.109481" target="_blank" rel="noopener">Sun Blocking Index (SBI) from Sky Image to Estimate Solar Irradiance</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Won-Ki Choi, Hyunjin Lee</div>
        <div class="pub-venue">Building and Environment</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2021</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.mdpi.com/2076-3417/11/11/5049" target="_blank" rel="noopener">A Deep Learning Model to Forecast Solar Irradiance Using a Sky Camera</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, R. Kamil, Hyunjin Lee</div>
        <div class="pub-venue">Applied Sciences, 11(11), 5049</div>
      </div>
    </div>

    <div class="pub-year-block reveal">
      <div class="pub-year-head"><span class="yr">2020</span><div class="yr-line"></div></div>

      <div class="pub-card">
        <div class="pub-title"><a href="https://www.mdpi.com/1996-1073/13/24/6623" target="_blank" rel="noopener">A Review on Deep Learning Models for Forecasting Time Series Data of Solar Irradiance and Photovoltaic Power</a></div>
        <div class="pub-authors"><span class="me">Rial A. Rajagukguk</span>, Raden A. A. Ramadhan, Hyunjin Lee</div>
        <div class="pub-venue">Energies, 13(24), 6623</div>
      </div>
    </div>

  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <div class="section-head reveal"><span class="section-num">04</span><h2>Projects</h2></div>

    <div class="project-card reveal">
      <div>
        <h3>Perusahaan Listrik Negara (PT PLN)</h3>
        <div class="p-org">Jakarta, Indonesia</div>
        <ul>
          <li>Solar irradiance estimation using sky camera</li>
          <li>Solar irradiance forecasting using sky camera and satellite image</li>
        </ul>
      </div>
      <div class="p-date">05/2024 — present</div>
    </div>

    <div class="project-card reveal">
      <div>
        <h3>Korea Evaluation Institute of Industrial Technology (KEIT)</h3>
        <div class="p-org">Seoul, Korea</div>
        <ul>
          <li>Thermal management system to reduce energy consumption and optimize the mileage of electric vehicles</li>
        </ul>
      </div>
      <div class="p-date">04/2022 — 12/2025</div>
    </div>

    <div class="project-card reveal">
      <div>
        <h3>National Research Foundation of Korea (NRF)</h3>
        <div class="p-org">Seoul, Korea</div>
        <ul>
          <li>Machine-learning-linked solar radiation model to predict solar irradiance</li>
        </ul>
      </div>
      <div class="p-date">03/2019 — 02/2023</div>
    </div>

    <div class="project-card reveal">
      <div>
        <h3>SONUSYS Co., Ltd</h3>
        <div class="p-org">Seoul, Korea</div>
        <ul>
          <li>Controlling the window based on solar radiation components</li>
        </ul>
      </div>
      <div class="p-date">04/2021 — 10/2021</div>
    </div>
  </section>

  <!-- AWARDS / PATENT -->
  <section id="credentials">
    <div class="section-head reveal"><span class="section-num">05</span><h2>Awards &amp; Patent</h2></div>
    <div class="credential-grid reveal">

      <div class="credential-card">
        <span class="c-label">Award</span>
        <p>Best Poster Presentation</p>
        <div class="c-meta">Korean Society of Animal Environmental Science &amp; Technology (KSAEST) 2026 · Cheongju, South Korea · 12 Jun 2026</div>
      </div>

      <div class="credential-card">
        <span class="c-label">Award</span>
        <p>Best Paper</p>
        <div class="c-meta">The Korean Solar Energy Society (KSES) 2023 · Yeosu, South Korea · 8 Nov 2023</div>
      </div>

      <div class="credential-card" style="grid-column: 1 / -1;">
        <span class="c-label">Patent</span>
        <p>구름 특성 기반 일사량 추정 시스템 및 방법 (Cloud-characteristic-based solar irradiance estimation system and method)</p>
        <div class="c-meta">Korean Intellectual Property Office · 2024</div>
      </div>

    </div>
  </section>

  <!-- CONFERENCES -->
  <section id="conferences">
    <div class="section-head reveal"><span class="section-num">06</span><h2>International Conferences</h2></div>

    <div class="conf-item reveal">
      <h3><a href="https://www.cigr-eurageng-2026.org" target="_blank" rel="noopener">Joint CIGR–EurAgEng World Congress 2026</a></h3>
      <div class="conf-meta">Politecnico di Torino, Italy · 24–26 Jun 2026</div>
      <div class="conf-talk">Satellite-Driven Estimation of Indoor Heat Stress in Livestock Facilities Using Machine Learning and GEO-KOMPSAT-2A Data</div>
      <div class="conf-talk">Developing an Integrated Safety and Welfare Assessment System for Livestock Transport Vehicles in Korea</div>
    </div>

    <div class="conf-item reveal">
      <h3><a href="https://event.asme.org/ES-2023" target="_blank" rel="noopener">ASME Energy Sustainability (ASME ES 2023)</a></h3>
      <div class="conf-meta">The Madison Hotel, Washington, DC · 10–12 Jul 2023</div>
      <div class="conf-talk">Minute-level solar irradiance estimation via sun-blocking index derived from sky images</div>
    </div>

    <div class="conf-item reveal">
      <h3><a href="https://www.ksnre.or.kr/afore/2022/" target="_blank" rel="noopener">11th Asia-Pacific Forum in Renewable Energy (AFORE 2022)</a></h3>
      <div class="conf-meta">Ramada Plaza Jeju, South Korea · 27 Sep – 1 Oct 2022</div>
      <div class="conf-talk">Estimation of minute level of solar irradiance using sun-blocking index (SBI) derived from sky images</div>
    </div>

    <div class="conf-item reveal">
      <h3><a href="https://acts2020jp.org/" target="_blank" rel="noopener">2nd Asian Conference on Thermal Sciences (2nd ACTS)</a></h3>
      <div class="conf-meta">Japan · 3–7 Oct 2021</div>
      <div class="conf-talk">Evaluation of decomposition models to estimate direct normal irradiance using sub-hour data</div>
    </div>
  </section>

  <footer>
    Rial Arifin Rajagukguk, PhD — Renewable Energy · Remote Sensing · Applied ML
  </footer>

</div>

<script>
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } });
  }, { threshold: 0.1 });
  document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>

</body>
</html>
