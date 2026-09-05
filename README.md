<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pavithra D — Mechanical Engineering, Robotics &amp; Automation</title>
<meta name="description" content="Portfolio of Pavithra D — Mechanical Engineering student specializing in robotics, automation, and manufacturing.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=IBM+Plex+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --dark-bg:#12161d;
    --dark-panel:#181e27;
    --line-dark:#2b3648;
    --line-dark-soft:#1f2733;
    --cream:#efe9d8;
    --cream-2:#e7e0cb;
    --line-cream:#c9beA0;
    --ink:#1c1a14;
    --ink-dim:#54503f;
    --accent:#d9793f;
    --accent-dim:#b4602c;
    --steel:#6f9bd1;
    --text:#eee9de;
    --text-dim:#9aa1ac;
    --text-faint:#5a6376;
    --radius:2px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--dark-bg);
    color:var(--text);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  a{color:inherit;}
  img{max-width:100%;display:block;}
  .mono{font-family:'IBM Plex Mono', monospace;}
  .headline{font-family:'Anton', sans-serif; font-weight:400; letter-spacing:0.01em;}
  h2,h3,h4{font-family:'IBM Plex Sans',sans-serif;font-weight:600;margin:0;}
  .wrap{max-width:1080px;margin:0 auto;padding:0 40px;position:relative;z-index:1;}
  @media (max-width:640px){ .wrap{padding:0 22px;} }

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:20;
    background:#141a26;
    border-bottom:1px solid var(--line-dark);
  }
  nav .wrap{display:flex;justify-content:space-between;align-items:center;padding:18px 40px;max-width:1200px;}
  .nav-mark{font-family:'IBM Plex Mono',monospace;font-weight:700;font-size:14px;letter-spacing:0.03em;color:var(--text);}
  .nav-mark span{color:var(--text-dim);font-weight:400;}
  .nav-links{display:flex;gap:26px;font-family:'IBM Plex Mono',monospace;font-size:12.5px;letter-spacing:0.03em;color:var(--text-dim);}
  .nav-links a{text-decoration:none;transition:color .15s;}
  .nav-links a:hover{color:var(--accent);}
  .nav-toggle{display:none;background:none;border:1px solid var(--line-dark);color:var(--text);padding:6px 12px;font-family:'IBM Plex Mono',monospace;font-size:12px;cursor:pointer;}
  @media (max-width:820px){
    .nav-links{display:none;}
    .nav-links.open{
      display:flex;flex-direction:column;gap:0;
      position:absolute;top:100%;left:0;right:0;
      background:#141a26;border-bottom:1px solid var(--line-dark);
    }
    .nav-links.open a{padding:14px 40px;border-top:1px solid var(--line-dark-soft);}
    .nav-toggle{display:block;}
  }

  /* ---------- HERO ---------- */
  header.hero{
    background:var(--dark-bg);
    background-image:
      linear-gradient(var(--line-dark-soft) 1px, transparent 1px),
      linear-gradient(90deg, var(--line-dark-soft) 1px, transparent 1px);
    background-size:60px 60px;
    padding:90px 0 0;
    position:relative;
  }
  .hero-inner{max-width:1200px;margin:0 auto;padding:0 40px;}
  @media (max-width:640px){ .hero-inner{padding:0 22px;} }
  .kicker{
    font-family:'IBM Plex Mono',monospace;
    font-size:12.5px; letter-spacing:0.04em;
    color:var(--accent);
    margin-bottom:22px;
  }
  h1.name{
    font-size:clamp(52px, 9vw, 108px);
    line-height:0.94;
    color:var(--text);
    text-transform:uppercase;
    margin:0;
  }
  .role{
    font-size:clamp(18px,2.3vw,23px);
    color:var(--text);
    font-family:'IBM Plex Sans',sans-serif;
    font-weight:400;
    margin-top:26px;
    max-width:32ch;
  }
  .lede{
    color:var(--text-dim);
    font-size:16px;
    max-width:58ch;
    margin-top:20px;
  }
  .hero-btns{display:flex;gap:14px;flex-wrap:wrap;margin-top:36px;}
  .btn{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px; letter-spacing:0.03em;
    padding:14px 26px;
    border:1px solid var(--line-dark);
    text-decoration:none;
    color:var(--text);
    transition:opacity .15s;
  }
  .btn.solid{background:var(--accent);border-color:var(--accent);color:#1a0f06;font-weight:500;}
  .btn:hover{opacity:0.85;}

  .title-block{
    margin-top:64px;
    border:1px solid var(--line-dark);
    border-bottom:none;
    display:grid;
    grid-template-columns:repeat(6,1fr);
  }
  .title-block div{
    padding:16px 20px;
    border-right:1px solid var(--line-dark);
  }
  .title-block div:last-child{border-right:none;}
  .title-block .k{font-family:'IBM Plex Mono',monospace;font-size:10.5px;letter-spacing:0.05em;color:var(--text-faint);margin-bottom:6px;}
  .title-block .v{font-family:'IBM Plex Mono',monospace;font-size:13.5px;color:var(--text);}
  @media (max-width:820px){
    .title-block{grid-template-columns:repeat(3,1fr);}
    .title-block div:nth-child(3){border-right:none;}
  }
  @media (max-width:480px){
    .title-block{grid-template-columns:repeat(2,1fr);}
    .title-block div:nth-child(2){border-right:none;}
  }

  /* ---------- SECTION SHELLS ---------- */
  section{padding:88px 0;}
  section.cream{background:var(--cream); color:var(--ink);}
  section.dark{background:var(--dark-bg); color:var(--text);}
  .sheet-label{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px; letter-spacing:0.04em;
    margin-bottom:46px;
  }
  section.cream .sheet-label{color:var(--ink-dim); border-bottom:1px solid var(--line-cream); padding-bottom:14px;}
  section.dark .sheet-label{color:var(--text-faint); border-bottom:1px solid var(--line-dark); padding-bottom:14px;}
  .eyebrow{font-family:'IBM Plex Mono',monospace;font-size:12.5px;letter-spacing:0.04em;color:var(--accent);margin-bottom:16px;}
  h2.sec-title{font-size:clamp(30px,4vw,44px);font-weight:700;line-height:1.08;max-width:16ch;margin-bottom:44px;}

  /* ---------- ABOUT ---------- */
  .about-grid{display:grid;grid-template-columns:260px 1fr;gap:56px;align-items:start;}
  @media (max-width:760px){ .about-grid{grid-template-columns:1fr;} }
  .photo-frame{border:1px solid var(--line-cream);padding:10px;}
  .photo-frame img{width:100%;filter:grayscale(15%);}
  .photo-cap{font-family:'IBM Plex Mono',monospace;font-size:11.5px;letter-spacing:0.03em;color:var(--ink-dim);margin-top:12px;}
  .about-body p{color:var(--ink-dim);font-size:16px;max-width:64ch;}
  .about-body p + p{margin-top:16px;}
  .stat-strip{
    margin-top:40px;
    border:1px solid var(--line-cream);
    display:grid;
    grid-template-columns:repeat(4,1fr);
  }
  .stat-strip div{padding:20px 22px;border-right:1px solid var(--line-cream);}
  .stat-strip div:last-child{border-right:none;}
  .stat-strip .k{font-family:'IBM Plex Mono',monospace;font-size:10.5px;letter-spacing:0.04em;color:var(--ink-dim);margin-bottom:8px;}
  .stat-strip .v{font-family:'IBM Plex Sans',sans-serif;font-size:19px;font-weight:600;color:var(--ink);}
  @media (max-width:640px){ .stat-strip{grid-template-columns:repeat(2,1fr);} .stat-strip div:nth-child(2){border-right:none;} }

  /* ---------- SKILLS ---------- */
  .skills-grid{display:grid;grid-template-columns:1fr 1fr;column-gap:64px;row-gap:44px;}
  @media (max-width:760px){ .skills-grid{grid-template-columns:1fr;} }
  .skill-cat h4{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px; letter-spacing:0.04em; font-weight:500;
    color:var(--accent);
    margin-bottom:18px;
  }
  .pill-grid{display:flex;flex-wrap:wrap;gap:10px;}
  .pill{
    font-family:'IBM Plex Sans',sans-serif;
    font-size:14px;
    padding:11px 16px;
    border:1px solid var(--line-dark);
    color:var(--text);
  }

  /* ---------- PROJECTS ---------- */
  .project{border:1px solid var(--line-cream);margin-bottom:28px;background:var(--cream-2);}
  .project-head{display:flex;justify-content:space-between;align-items:flex-start;gap:16px;padding:24px 28px;border-bottom:1px solid var(--line-cream);flex-wrap:wrap;}
  .project-head h3{font-size:21px;max-width:40ch;color:var(--ink);}
  .project-tag{font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--ink-dim);white-space:nowrap;padding-top:4px;}
  .project-body{padding:24px 28px 8px;}
  .project-body ul{list-style:none;margin:0;padding:0;}
  .project-body li{
    position:relative;
    padding-left:22px;
    color:var(--ink-dim);
    font-size:15.5px;
    margin-bottom:16px;
  }
  .project-body li::before{content:"—";position:absolute;left:0;color:var(--accent);}
  .project-tools{padding:0 28px 24px;font-size:14px;color:var(--ink-dim);}
  .project-tools b{color:var(--ink);font-weight:600;}
  .project-tools .t{color:var(--accent-dim);}

  /* ---------- CAD GALLERY ---------- */
  .gallery-grid{display:grid;grid-template-columns:1fr 1fr;gap:28px;}
  @media (max-width:760px){ .gallery-grid{grid-template-columns:1fr;} }
  .gallery-item{border:1px solid var(--line-dark);}
  .gallery-item img{width:100%;display:block;}
  .gallery-cap{padding:16px 18px;border-top:1px solid var(--line-dark);}
  .gallery-cap .fig{font-family:'IBM Plex Mono',monospace;font-size:11px;color:var(--text-faint);margin-bottom:6px;}
  .gallery-cap .name{font-size:14.5px;color:var(--text);font-weight:500;}
  .gallery-item.wide{grid-column:1 / -1;}

  /* ---------- LEADERSHIP ---------- */
  .leadership-grid{display:grid;grid-template-columns:1.3fr 1fr;gap:56px;}
  @media (max-width:760px){ .leadership-grid{grid-template-columns:1fr;gap:44px;} }
  .dtl{border-left:1px solid var(--line-cream);}
  .dtl-item{position:relative;padding:0 0 30px 28px;}
  .dtl-item:last-child{padding-bottom:0;}
  .dtl-item::before{
    content:"";position:absolute;left:-5px;top:4px;
    width:9px;height:9px;background:var(--accent);
    transform:rotate(45deg);
  }
  .dtl-date{font-size:12.5px;color:var(--ink-dim);margin-bottom:6px;}
  .dtl-item h5{font-size:16px;font-weight:600;margin:0 0 8px;color:var(--ink);}
  .dtl-item p{margin:0;color:var(--ink-dim);font-size:15px;}
  .badge-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
  @media (max-width:480px){ .badge-grid{grid-template-columns:1fr;} }
  .badge-card{border:1px solid var(--line-cream);padding:22px;background:var(--cream-2);}
  .badge-icon{font-size:22px;margin-bottom:14px;}
  .badge-card h5{font-size:15.5px;font-weight:600;margin:0 0 6px;color:var(--ink);}
  .badge-org{font-size:10.5px;letter-spacing:0.04em;color:var(--ink-dim);margin-bottom:14px;padding-bottom:14px;border-bottom:1px solid var(--line-cream);}
  .badge-card p{margin:0;font-size:13.5px;color:var(--ink-dim);}

  /* ---------- EDU + CERTS ---------- */
  .two-col{display:grid;grid-template-columns:1fr 1fr;gap:56px;}
  @media (max-width:760px){ .two-col{grid-template-columns:1fr;gap:44px;} }
  h4.sub{font-family:'IBM Plex Mono',monospace;font-size:13px;letter-spacing:0.04em;color:var(--accent);margin-bottom:22px;}
  .edu-item{padding:18px 0;border-top:1px solid var(--line-dark);}
  .edu-item:first-child{border-top:none;padding-top:0;}
  .edu-item h5{font-size:16px;font-weight:600;margin:0 0 5px;color:var(--text);}
  .edu-item .meta{font-size:14px;color:var(--text-dim);}
  .edu-item .score{font-family:'IBM Plex Mono',monospace;font-size:12.5px;color:var(--steel);margin-top:6px;}
  .cert-list{list-style:none;margin:0;padding:0;}
  .cert-list li{display:flex;gap:14px;padding:13px 0;border-top:1px solid var(--line-dark);font-size:15px;color:var(--text-dim);}
  .cert-list li:first-child{border-top:none;padding-top:0;}
  .cert-list .idx{font-family:'IBM Plex Mono',monospace;color:var(--text-faint);flex-shrink:0;}
  .lang-line{margin-top:30px;padding-top:22px;border-top:1px solid var(--line-dark);font-size:14.5px;color:var(--text-dim);}
  .lang-line b{color:var(--text);font-weight:500;}

  /* ---------- CONTACT ---------- */
  .contact-links{display:flex;flex-wrap:wrap;gap:14px;margin-top:8px;margin-bottom:56px;}

  footer{padding:28px 0 40px;color:var(--text-faint);font-size:13px;background:var(--dark-bg);border-top:1px solid var(--line-dark);}
  footer .wrap{display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px;max-width:1200px;padding-top:28px;}

  a:focus-visible, button:focus-visible{outline:2px solid var(--accent);outline-offset:2px;}
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="nav-mark">PAVITHRA D <span>// MECH.ENG</span></div>
    <div class="nav-links" id="navLinks">
      <a href="#about">ABOUT</a>
      <a href="#skills">SKILLS</a>
      <a href="#projects">PROJECTS</a>
      <a href="#gallery">CAD GALLERY</a>
      <a href="#leadership">LEADERSHIP</a>
      <a href="#contact">CONTACT</a>
    </div>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu">MENU</button>
  </div>
</nav>

<header class="hero">
  <div class="hero-inner">
    <div class="kicker">FINAL-YEAR B.E. MECHANICAL ENGINEERING — VEMANA INSTITUTE OF TECHNOLOGY</div>
    <h1 class="name headline">Pavithra D.</h1>
    <p class="role">Industrial Robotics &amp; Automation — Manufacturing &amp; Production</p>
    <p class="lede">I take mechanical designs from CAD sketch to machined, working parts — CNC toolpaths, generative structural studies, and embedded control systems that actually run. Looking for a hands-on robotics, automation, or manufacturing internship.</p>
    <div class="hero-btns">
      <a class="btn solid" href="#projects">VIEW PROJECTS</a>
      <a class="btn" href="#contact">GET IN TOUCH</a>
    </div>
    <div class="title-block">
      <div><div class="k">NAME</div><div class="v">Pavithra D</div></div>
      <div><div class="k">SHEET</div><div class="v">01 OF 08</div></div>
      <div><div class="k">SCALE</div><div class="v">N.T.S.</div></div>
      <div><div class="k">REV</div><div class="v">A</div></div>
      <div><div class="k">DATE</div><div class="v">2026</div></div>
      <div><div class="k">LOCATION</div><div class="v">Bangalore, IN</div></div>
    </div>
  </div>
</header>

<section id="about" class="cream">
  <div class="wrap">
    <div class="sheet-label">SHEET 02 / 08 — ABOUT</div>
    <div class="about-grid">
      <div>
        <div class="photo-frame">
          <img src="images/photo.jpg" alt="Pavithra D">
        </div>
        <div class="photo-cap">PAVITHRA D — BANGALORE, INDIA</div>
      </div>
      <div>
        <div class="eyebrow">ABOUT</div>
        <h2 class="sec-title" style="color:var(--ink);">Building the parts, not just modeling them.</h2>
        <div class="about-body">
          <p>I'm a final-year Mechanical Engineering student at Vemana Institute of Technology (VTU), working across CAD, CNC manufacturing, and embedded robotics. I've taken two prototypes end-to-end — an IoT-enabled filament extrusion system and an ESP32-based adaptive EV braking system — from SolidWorks and Fusion 360 models to machined, functioning hardware.</p>
          <p>As Vice Chair of the IEEE Robotics and Automation Society student chapter, I co-organize industrial robotics workshops and technical events, coordinating with faculty and industry professionals. Before that, I managed chapter finances as Treasurer for two years.</p>
          <p>Right now I'm looking for an internship in robotics, automation, or manufacturing &amp; production — where I can bring the same build-fast, iterate-faster approach to a real production floor.</p>
        </div>
        <div class="stat-strip">
          <div><div class="k">CGPA</div><div class="v">7.9 / 10</div></div>
          <div><div class="k">GRADUATING</div><div class="v">2027</div></div>
          <div><div class="k">CHAPTER ROLE</div><div class="v">IEEE RAS Vice Chair</div></div>
          <div><div class="k">BASED IN</div><div class="v">Bangalore, IN</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="skills" class="dark">
  <div class="wrap">
    <div class="sheet-label">SHEET 03 / 08 — SKILLS</div>
    <div class="eyebrow">CAPABILITIES</div>
    <h2 class="sec-title headline" style="text-transform:none;font-family:'IBM Plex Sans',sans-serif;">Tools &amp; technical range</h2>
    <div class="skills-grid">
      <div class="skill-cat">
        <h4>ROBOTICS &amp; AUTOMATION</h4>
        <div class="pill-grid">
          <span class="pill">Industrial Robot Programming</span>
          <span class="pill">PLC Basics</span>
          <span class="pill">G-code / M-code</span>
          <span class="pill">ESP32 / Arduino</span>
          <span class="pill">PWM Control</span>
          <span class="pill">Sensor &amp; Actuator Integration</span>
        </div>
      </div>
      <div class="skill-cat">
        <h4>CAD / CAM / ANALYSIS</h4>
        <div class="pill-grid">
          <span class="pill">SolidWorks</span>
          <span class="pill">AutoCAD</span>
          <span class="pill">Fusion 360</span>
          <span class="pill">Ansys / FEA</span>
          <span class="pill">CNC Programming</span>
          <span class="pill">GD&amp;T</span>
          <span class="pill">DFM / DFMA</span>
        </div>
      </div>
      <div class="skill-cat">
        <h4>MANUFACTURING &amp; PRODUCTION</h4>
        <div class="pill-grid">
          <span class="pill">CNC Machining</span>
          <span class="pill">3D Printing / Additive Mfg</span>
          <span class="pill">Lean &amp; 5S Fundamentals</span>
          <span class="pill">BOM Preparation</span>
          <span class="pill">Total Quality Management</span>
        </div>
      </div>
      <div class="skill-cat">
        <h4>PROGRAMMING &amp; TOOLS</h4>
        <div class="pill-grid">
          <span class="pill">MATLAB / Simulink</span>
          <span class="pill">Python</span>
          <span class="pill">Embedded C</span>
          <span class="pill">Arduino IDE</span>
          <span class="pill">LaTeX</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects" class="cream">
  <div class="wrap">
    <div class="sheet-label">SHEET 04 / 08 — PROJECTS</div>
    <div class="eyebrow">FEATURED PROJECTS</div>
    <h2 class="sec-title" style="color:var(--ink);">Two prototypes, shipped end to end</h2>

    <div class="project">
      <div class="project-head">
        <h3>IoT-Based Automated 3D Printer Filament Extrusion System Using Solid Waste</h3>
        <span class="project-tag">PRJ.01</span>
      </div>
      <div class="project-body">
        <ul>
          <li>Engineered an automated plastic-to-filament recycling system, designing the IoT-enabled extrusion pipeline in SolidWorks and integrating ESP32-based automated process control — cutting raw material and manufacturing cost.</li>
          <li>Implemented real-time control logic across extrusion, cooling, and spooling stages using Arduino/ESP32 and CNC-machined components, reducing manual monitoring and material waste.</li>
          <li>Applied DFM principles and GD&amp;T tolerancing while maintaining an accurate BOM across design iterations — cutting fixture lead time as measured by fewer rework cycles against a manual extrusion baseline.</li>
        </ul>
      </div>
      <div class="project-tools"><b>Tools —</b> <span class="t">Fusion 360</span> · <span class="t">SolidWorks</span> · <span class="t">Arduino / ESP32</span> · <span class="t">CNC Machining</span> · <span class="t">3D Printing</span></div>
    </div>

    <div class="project">
      <div class="project-head">
        <h3>Adaptive Regenerative Braking System</h3>
        <span class="project-tag">PRJ.02</span>
      </div>
      <div class="project-body">
        <ul>
          <li>Designed a gradient-adaptive braking system for EV applications using an ESP32 microcontroller and ADXL335 accelerometer to dynamically adjust braking intensity via PWM-controlled BLDC motor output.</li>
          <li>Improved braking efficiency, energy recovery, and vehicle stability during incline/decline braking against a fixed-braking baseline, validated through iterative testing.</li>
          <li>Resolved intermittent braking lag by conducting root-cause analysis on a sensor calibration error, then recalibrating the accelerometer input pipeline to fix it.</li>
        </ul>
      </div>
      <div class="project-tools"><b>Tools —</b> <span class="t">ESP32</span> · <span class="t">ADXL335</span> · <span class="t">Embedded C</span> · <span class="t">PWM Control</span> · <span class="t">BLDC Motor</span></div>
    </div>
  </div>
</section>

<section id="gallery" class="dark">
  <div class="wrap">
    <div class="sheet-label">SHEET 05 / 08 — CAD GALLERY</div>
    <div class="eyebrow">MODELED &amp; MACHINED</div>
    <h2 class="sec-title" style="text-transform:none;">A look inside the CAD work</h2>
    <h4 class="sub" style="margin-bottom:24px;">FROM PRJ.01 — FILAMENT EXTRUSION SYSTEM</h4>
    <div class="gallery-grid" style="margin-bottom:56px;">
      <div class="gallery-item">
        <img src="images/cad-shedder.jpg" alt="PET bottle cutter and shredder assembly">
        <div class="gallery-cap">
          <div class="fig">FIG.01</div>
          <div class="name">PET Bottle Shredder — gear-driven cutter that reduces bottles to feedstock</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-strip-spooler.jpg" alt="PET strip spooler component assembly">
        <div class="gallery-cap">
          <div class="fig">FIG.02</div>
          <div class="name">Strip Spooler — winds shredded PET strips ahead of extrusion</div>
        </div>
      </div>
      <div class="gallery-item wide">
        <img src="images/cad-spooler-gears.jpg" alt="Full spooler gear train assembly">
        <div class="gallery-cap">
          <div class="fig">FIG.03</div>
          <div class="name">Spooler Gear Train — helical gear assembly driving the filament take-up spool</div>
        </div>
      </div>
    </div>

    <h4 class="sub" style="margin-bottom:24px;">OTHER CAD &amp; GENERATIVE DESIGN WORK</h4>
    <div class="gallery-grid">
      <div class="gallery-item wide">
        <img src="images/cad-engine-assembly.jpg" alt="Inline-4 engine assembly modeled in Fusion 360">
        <div class="gallery-cap">
          <div class="fig">FIG.04</div>
          <div class="name">I4 Engine Assembly — piston, connecting rod, and crankshaft assembly</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-piston-crank.jpg" alt="Piston and crankshaft hybrid model">
        <div class="gallery-cap">
          <div class="fig">FIG.05</div>
          <div class="name">Piston-Crank Hybrid Model — surface and solid modeling combined</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-generative-bracket.jpg" alt="Generative design study of a structural bracket">
        <div class="gallery-cap">
          <div class="fig">FIG.06</div>
          <div class="name">GE Bracket — generative design study exploring load-optimized geometry</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-generative-load.jpg" alt="Generative design load case study with support posts">
        <div class="gallery-cap">
          <div class="fig">FIG.07</div>
          <div class="name">Generative Load Case — structural study on a four-post support plate</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-front-loader-linkage.jpg" alt="Generative design study of a front loader linkage">
        <div class="gallery-cap">
          <div class="fig">FIG.08</div>
          <div class="name">Front Loader Linkage — generative design study on a mechanical linkage arm</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-cross-bracket.jpg" alt="Cross-shaped sheet metal mounting bracket">
        <div class="gallery-cap">
          <div class="fig">FIG.09</div>
          <div class="name">Cross Mounting Bracket — sheet metal component with formed flanges</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-cam-facing.jpg" alt="CAM toolpath setup for facing and drilling operations">
        <div class="gallery-cap">
          <div class="fig">FIG.10</div>
          <div class="name">CAM Setup — facing and drilling toolpaths for a machined base plate</div>
        </div>
      </div>
      <div class="gallery-item">
        <img src="images/cad-cam-corner.jpg" alt="CAM toolpath setup for an angled corner bracket">
        <div class="gallery-cap">
          <div class="fig">FIG.11</div>
          <div class="name">CAM Setup — adaptive clearing and drilling for an angled corner bracket</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="leadership" class="cream">
  <div class="wrap">
    <div class="sheet-label">SHEET 06 / 08 — LEADERSHIP &amp; INVOLVEMENT</div>
    <div class="eyebrow">LEADERSHIP</div>
    <h2 class="sec-title" style="color:var(--ink);">Beyond the workbench</h2>
    <div class="leadership-grid">
      <div>
        <h4 class="sub" style="color:var(--accent-dim);">ORGANIZING &amp; LEADERSHIP</h4>
        <div class="dtl">
          <div class="dtl-item">
            <div class="dtl-date mono">2025 – 2026</div>
            <h5>Vice Chair, IEEE Robotics and Automation Society (RAS)</h5>
            <p>Co-organized 3+ industrial robotics workshops and technical events; coordinated with faculty and industry professionals.</p>
          </div>
          <div class="dtl-item">
            <div class="dtl-date mono">2023 – 2024</div>
            <h5>Treasurer, IEEE RAS Student Chapter</h5>
            <p>Managed chapter budget, finances, and event expenditures for technical workshops and competitions.</p>
          </div>
        </div>
      </div>
      <div>
        <h4 class="sub" style="color:var(--accent-dim);">BADGES &amp; AWARDS</h4>
        <div class="badge-grid">
          <div class="badge-card">
            <div class="badge-icon">🏆</div>
            <h5>2nd Prize — Robotics</h5>
            <div class="badge-org mono">ROBOMANTHAN PVT. LTD.</div>
            <p>Competitive design-build robotics event, 2025.</p>
          </div>
          <div class="badge-card">
            <div class="badge-icon">🔧</div>
            <h5>CNC Machining</h5>
            <div class="badge-org mono">PRACTICAL SKILL</div>
            <p>CNC-machined components across both prototype builds.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="education" class="dark">
  <div class="wrap">
    <div class="sheet-label">SHEET 07 / 08 — EDUCATION &amp; CERTIFICATIONS</div>
    <div class="two-col">
      <div>
        <h4 class="sub">EDUCATION</h4>
        <div class="edu-item">
          <h5>B.E. Mechanical Engineering</h5>
          <div class="meta">Vemana Institute of Technology, VTU · 2023 – 2027 (Expected)</div>
          <div class="score">CGPA 7.9 / 10</div>
        </div>
        <div class="edu-item">
          <h5>Pre-University (KSEAB)</h5>
          <div class="meta">Krupanidhi Group of Institutions · 2021 – 2023</div>
          <div class="score">68.8%</div>
        </div>
        <div class="edu-item">
          <h5>ICSE, KSEEB</h5>
          <div class="meta">Patel Public School · 2021</div>
          <div class="score">71.2%</div>
        </div>
        <div class="lang-line"><b>Languages —</b> English (Professional) · Hindi (Conversational) · Kannada (Conversational) · Telugu (Native)</div>
      </div>
      <div>
        <h4 class="sub">CERTIFICATIONS</h4>
        <ul class="cert-list">
          <li><span class="idx mono">01</span>SolidWorks Certified</li>
          <li><span class="idx mono">02</span>Autodesk Certificate of Completion</li>
          <li><span class="idx mono">03</span>MATLAB Onramp</li>
          <li><span class="idx mono">04</span>Python 3.4.3 Course Completion</li>
          <li><span class="idx mono">05</span>Data Visualisation — Tata x Forage (2026)</li>
          <li><span class="idx mono">06</span>Industrial Robotics Skill Development Workshop (3-Day)</li>
          <li><span class="idx mono">07</span>Fundamentals of Robotics Workshop (2-Day)</li>
          <li><span class="idx mono">08</span>EV Saksham Electric Vehicle Workshop (5-Day)</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="contact" class="dark" style="padding-bottom:0;">
  <div class="wrap">
    <div class="sheet-label">SHEET 08 / 08 — CONTACT</div>
    <h2 class="sec-title headline" style="text-transform:none;font-family:'Anton',sans-serif;font-size:clamp(34px,5vw,52px);">Get in touch</h2>
    <p style="color:var(--text-dim);font-size:16px;max-width:56ch;margin-top:-16px;margin-bottom:32px;">I'm available for internships in robotics, automation and manufacturing. Reach out to discuss projects, placements or collaborations.</p>
    <div class="contact-links">
      <a class="btn" href="mailto:reddydpavithra@gmail.com">Email</a>
      <a class="btn" href="https://linkedin.com/in/pavithra-reddy-d-7589b8383" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <span>© Pavithra D — Mechanical Engineering Portfolio</span>
    <span>Designed &amp; built — Fusion 360 · SolidWorks</span>
  </div>
</footer>

<script>
  document.getElementById('navToggle').addEventListener('click', function(){
    document.getElementById('navLinks').classList.toggle('open');
  });
  document.querySelectorAll('.nav-links a').forEach(function(a){
    a.addEventListener('click', function(){
      document.getElementById('navLinks').classList.remove('open');
    });
  });
</script>

</body>
</html>
