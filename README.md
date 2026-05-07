<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Welcome to Famly — UK Marketing Lead Onboarding</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@400;500;600;700&family=Mulish:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    /* Famly brand — OKLCH for perceptual uniformity */
    --p50:  oklch(97.5% 0.012 290);
    --p400: oklch(38% 0.18 290);
    --p500: oklch(30% 0.18 290);
    --b400: oklch(55% 0.19 240);
    --n400: oklch(22% 0.015 270);
    --n300: oklch(44% 0.012 270);
    --g400: oklch(36% 0.13 155);
    --g50:  oklch(96% 0.03 155);
    --o400: oklch(68% 0.18 42);
    --y400: oklch(80% 0.16 80);
    --r400: oklch(52% 0.22 18);

    /* Semantic */
    --famly-purple: var(--p400);
    --famly-blue:   var(--b400);
    --famly-dark:   var(--n400);
    --famly-muted:  var(--n300);
    --famly-green:  var(--g400);
    --famly-orange: var(--o400);
    --famly-yellow: var(--y400);
    --famly-red:    var(--r400);
    --famly-bg:     var(--p50);
    --famly-card:   #fff;
    --famly-border: oklch(75% 0.02 290 / 0.3);
    --famly-text:   var(--n400);

    /* Backward compat */
    --famly-mint:   var(--g400);
    --famly-coral:  var(--o400);
    --famly-sky:    var(--b400);
    --famly-navy:   var(--n400);

    /* 4pt spacing scale */
    --space-1: 4px;
    --space-2: 8px;
    --space-3: 12px;
    --space-4: 16px;
    --space-5: 24px;
    --space-6: 32px;
    --space-7: 48px;
    --space-8: 64px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Mulish', system-ui, sans-serif;
    background: var(--famly-bg);
    color: var(--famly-text);
    min-height: 100vh;
    -webkit-font-smoothing: antialiased;
  }

  /* Hero */
  .hero {
    background: var(--p400);
    background-image:
      radial-gradient(ellipse 80% 60% at 10% 120%, oklch(45% 0.22 310 / 0.4) 0%, transparent 60%),
      radial-gradient(ellipse 60% 80% at 90% -20%, oklch(55% 0.14 260 / 0.3) 0%, transparent 50%);
    padding: clamp(36px, 6vw, 56px) clamp(20px, 4vw, 48px) clamp(40px, 6vw, 64px);
    text-align: left;
  }
  .hero-inner {
    max-width: 1060px;
    margin: 0 auto;
  }
  .hero-tag {
    display: inline-block;
    background: oklch(100% 0 0 / 0.12);
    color: oklch(100% 0 0 / 0.8);
    font-family: 'Mulish', sans-serif;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 5px 14px;
    border-radius: 4px;
    margin-bottom: var(--space-5);
  }
  .hero h1 {
    font-family: 'Sora', sans-serif;
    font-size: clamp(30px, 5vw, 52px);
    font-weight: 700;
    color: #fff;
    line-height: 1.1;
    margin-bottom: var(--space-4);
    letter-spacing: -0.02em;
  }
  .hero h1 span { color: #fff; }
  .hero p {
    font-size: 16px;
    color: oklch(100% 0 0 / 0.68);
    max-width: 480px;
    margin: 0 0 var(--space-6);
    line-height: 1.65;
  }
  .progress-bar-wrap {
    background: rgba(255,255,255,0.15);
    border-radius: 20px;
    height: 6px;
    max-width: 400px;
    margin: 0 auto 12px;
  }
  .progress-bar-wrap { overflow: hidden; }
  .progress-bar-fill {
    background: var(--y400);
    height: 100%;
    border-radius: 20px;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1);
  }
  .progress-label {
    font-size: 13px;
    color: rgba(255,255,255,0.55);
  }
  .progress-label span { color: rgba(255,255,255,0.95); font-weight: 500; }

  /* Layout */
  .page-body {
    display: grid;
    grid-template-columns: 220px 1fr;
    max-width: 1060px;
    margin: 0 auto;
    min-height: 100vh;
    align-items: start;
  }

  /* Sidebar */
  .sidebar {
    position: sticky;
    top: 0;
    height: 100vh;
    overflow-y: auto;
    padding: 32px 0 40px;
    border-right: 1px solid var(--famly-border);
    background: #fff;
    scrollbar-width: none;
  }
  .sidebar::-webkit-scrollbar { display: none; }
  .sidebar-label {
    font-family: 'Mulish', sans-serif;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--famly-muted);
    padding: 0 20px 10px;
  }
  .sidebar-group { margin-bottom: 8px; }
  .sidebar-group-title {
    font-family: 'Mulish', sans-serif;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: oklch(70% 0.01 270);
    padding: 16px 20px 6px;
  }
  .tab-btn {
    display: flex;
    align-items: center;
    gap: 10px;
    width: 100%;
    padding: 9px 20px;
    font-family: 'Mulish', sans-serif;
    font-size: 13.5px;
    font-weight: 500;
    color: var(--famly-muted);
    background: transparent;
    border: none;
    cursor: pointer;
    text-align: left;
    transition: color 0.15s, background 0.15s;
    white-space: nowrap;
    position: relative;
  }
  .tab-btn:hover { color: var(--p400); background: var(--p50); }
  .tab-btn.active {
    color: var(--p400);
    background: var(--p50);
    font-weight: 700;
  }
  .tab-btn.active::before {
    content: '';
    position: absolute;
    left: 0; top: 4px; bottom: 4px;
    width: 3px;
    background: var(--p400);
    border-radius: 0 3px 3px 0;
  }
  .tab-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: oklch(85% 0.02 290);
    flex-shrink: 0;
    transition: background 0.2s;
  }
  .tab-btn.active .tab-dot { background: var(--p400); }
  .tab-btn.completed .tab-dot { background: var(--g400); }
  .tab-btn.completed { color: oklch(62% 0.08 155); }

  /* Mobile nav — select dropdown */
  .mobile-nav {
    display: none;
    position: sticky;
    top: 0;
    z-index: 100;
    background: #fff;
    border-bottom: 1px solid var(--famly-border);
    padding: 10px 16px;
  }
  .mobile-nav select {
    width: 100%;
    padding: 10px 14px;
    font-family: 'Mulish', sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: var(--famly-text);
    background: var(--p50);
    border: 1.5px solid var(--famly-border);
    border-radius: 8px;
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%236b6b8a' d='M6 8L1 3h10z'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 14px center;
    cursor: pointer;
  }

  /* Main content */
  .main {
    padding: clamp(28px, 4vw, 48px) clamp(20px, 4vw, 48px) 80px;
    min-width: 0;
  }

  @media (max-width: 720px) {
    .page-body { grid-template-columns: 1fr; }
    .sidebar { display: none; }
    .mobile-nav { display: block; }
    .main { padding: 24px 16px 60px; }
  }

  /* Day panels */
  .day-panel { display: none; }
  .day-panel.active { display: block; }

  .day-header {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    margin-bottom: 32px;
  }
  .day-badge {
    flex: 0 0 auto;
    width: 52px; height: 52px;
    border-radius: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Sora', sans-serif;
    font-size: 20px;
    font-weight: 600;
  }
  .day-badge.d1 { background: hsla(265,75%,94%,1); color: var(--p400); }
  .day-badge.d2 { background: hsla(210,95%,92%,1); color: var(--b400); }
  .day-badge.d3 { background: hsla(43,95%,90%,1);  color: hsla(43,80%,32%,1); }
  .day-badge.d4 { background: hsla(265,75%,94%,1); color: var(--p400); }
  .day-badge.d5 { background: hsla(155,73%,88%,1); color: oklch(32% 0.12 155); }
  .day-badge.overview { background: hsla(240,12%,92%,1); color: var(--n400); }

  .day-header-text h2 {
    font-family: 'Sora', sans-serif;
    font-size: 22px;
    font-weight: 600;
    color: var(--famly-text);
    margin-bottom: 6px;
  }
  .day-header-text p {
    font-size: 14px;
    color: var(--famly-muted);
    line-height: 1.5;
  }

  /* Checklist items */
  .check-section {
    margin-bottom: 28px;
  }
  .section-title {
    font-family: 'Mulish', sans-serif;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 1.6px;
    text-transform: uppercase;
    color: var(--famly-muted);
    margin-bottom: 10px;
    padding-left: 4px;
  }

  .check-item {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    padding: 13px 16px;
    background: var(--famly-card);
    border: 1px solid var(--famly-border);
    border-radius: 10px;
    margin-bottom: 7px;
    cursor: pointer;
    transition: all 0.15s;
    position: relative;
  }
  .check-item:hover { border-color: var(--p400); background: var(--p50); }
  .check-item.done {
    background: hsla(155,73%,97%,1);
    border-color: hsla(155,73%,70%,1);
  }
  .check-item.done .check-label { color: var(--famly-muted); text-decoration: line-through; text-decoration-color: hsla(155,73%,55%,0.6); }

  .check-box {
    flex: 0 0 auto;
    width: 20px; height: 20px;
    border-radius: 5px;
    border: 1.5px solid rgba(90,60,160,0.25);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.15s;
    margin-top: 2px;
  }
  .check-item.done .check-box {
    background: var(--g400);
    border-color: var(--g400);
  }
  .check-box svg { display: none; }
  .check-item.done .check-box svg { display: block; }

  .check-content { flex: 1; }
  .check-label {
    font-size: 14px;
    font-weight: 400;
    color: var(--famly-text);
    line-height: 1.45;
    transition: color 0.15s;
  }
  .check-label strong { font-weight: 500; }
  .check-note {
    font-size: 12.5px;
    color: var(--famly-muted);
    margin-top: 4px;
    line-height: 1.55;
  }
  .check-tag {
    display: inline-block;
    font-size: 10.5px;
    font-weight: 500;
    padding: 2px 7px;
    border-radius: 4px;
    margin-left: 7px;
    vertical-align: middle;
    letter-spacing: 0.2px;
  }
  .tag-tool { background: hsla(210,95%,93%,1); color: hsla(210,75%,32%,1); }
  .tag-read { background: hsla(43,95%,88%,1);  color: hsla(43,80%,32%,1); }
  .tag-meet { background: hsla(265,75%,93%,1); color: var(--p400); }
  .tag-action { background: hsla(25,95%,90%,1); color: hsla(25,80%,35%,1); }

  /* Info cards */
  .info-card {
    background: var(--famly-card);
    border: 1px solid var(--famly-border);
    border-radius: 12px;
    padding: 20px 22px;
    margin-bottom: 18px;
  }
  .info-card.highlight {
    background: hsla(265,75%,97%,1);
    border-color: hsla(265,75%,78%,1);
  }
  .info-card.blue {
    background: hsla(210,95%,96%,1);
    border-color: hsla(210,95%,78%,1);
  }
  .info-card.purple {
    background: hsla(265,75%,97%,1);
    border-color: hsla(265,75%,78%,1);
  }
  .info-card h3 {
    font-family: 'Sora', sans-serif;
    font-size: 14px;
    font-weight: 600;
    margin-bottom: 10px;
    color: var(--famly-text);
  }
  .info-card p {
    font-size: 13.5px;
    color: var(--famly-muted);
    line-height: 1.6;
  }
  .info-card ul { list-style: none; padding: 0; }
  .info-card ul li {
    font-size: 13.5px;
    color: var(--famly-muted);
    padding: 4px 0;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .info-card ul li::before {
    content: '';
    width: 5px; height: 5px;
    border-radius: 50%;
    background: var(--p400);
    flex: 0 0 auto;
  }
  .info-card ul li a { color: inherit; }

  /* People grid */
  .people-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(175px, 1fr));
    gap: 10px;
    margin-top: 4px;
  }
  .person-card {
    background: var(--p50);
    border: 1px solid var(--famly-border);
    border-radius: 10px;
    padding: 12px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .person-avatar {
    width: 34px; height: 34px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Sora', sans-serif;
    font-size: 12px;
    font-weight: 600;
    flex: 0 0 auto;
  }
  .person-info { min-width: 0; }
  .person-name {
    font-size: 13px;
    font-weight: 500;
    color: var(--famly-text);
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .person-role {
    font-size: 12px;
    color: var(--famly-muted);
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  /* Slack channels */
  .channel-group { margin-bottom: 16px; }
  .channel-group-title {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.8px;
    text-transform: none;
    color: var(--famly-muted);
    margin-bottom: 8px;
  }
  .channel-list { display: flex; flex-wrap: wrap; gap: 6px; }
  .channel-pill {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    background: #fff;
    border: 1px solid var(--famly-border);
    border-radius: 6px;
    padding: 5px 10px;
    font-size: 12.5px;
    color: var(--famly-text);
    cursor: pointer;
    transition: all 0.12s;
    user-select: none;
  }
  .channel-pill:hover { background: var(--p50); border-color: var(--p400); color: var(--p400); }
  .channel-pill.joined {
    background: hsla(155,73%,94%,1);
    border-color: hsla(155,73%,60%,1);
    color: oklch(32% 0.12 155);
  }
  .channel-hash { font-size: 12px; opacity: 0.45; }

  /* Complete day button */
  .btn-complete {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    width: 100%;
    padding: 14px;
    background: var(--p400);
    color: #FFF;
    border: none;
    border-radius: 10px;
    font-family: 'Sora', sans-serif;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    margin-top: 28px;
    transition: all 0.15s;
  }
  .btn-complete:hover { background: hsla(265,75%,30%,1); }
  .btn-complete.done-state { background: var(--g400); color: #fff; }

  /* Overview timeline */
  .timeline {
    position: relative;
    padding-left: 32px;
  }
  .timeline::before {
    content: '';
    position: absolute;
    left: 10px; top: 8px; bottom: 8px;
    width: 1.5px;
    background: var(--famly-border);
  }
  .timeline-item { position: relative; margin-bottom: 22px; }
  .timeline-dot {
    position: absolute;
    left: -32px; top: 3px;
    width: 20px; height: 20px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Sora', sans-serif;
    font-size: 9px;
    font-weight: 600;
    background: #fff;
    border: 1.5px solid var(--famly-border);
    color: var(--famly-muted);
    transition: all 0.25s;
  }
  .timeline-dot.active { background: var(--p400); border-color: var(--p400); color: #FFF; }
  .timeline-dot.done   { background: var(--g400); border-color: var(--g400); color: #FFF; }
  .timeline-content h3 {
    font-family: 'Sora', sans-serif;
    font-size: 14px;
    font-weight: 500;
    color: var(--famly-text);
    margin-bottom: 3px;
  }
  .timeline-content p { font-size: 13px; color: var(--famly-muted); line-height: 1.5; }

  /* Links inside check labels */
  .check-label a {
    color: var(--p400);
    text-decoration: none;
    font-weight: 500;
  }
  .check-label a:hover { text-decoration: underline; }

  /* Inline note banner */
  .info-note {
    display: block;
    background: hsla(43,95%,93%,1);
    border: 1px solid hsla(43,80%,70%,1);
    border-radius: 8px;
    padding: 11px 14px;
    font-size: 13px;
    color: hsla(43,80%,28%,1);
    line-height: 1.6;
    margin-top: 8px;
  }
  .info-note-icon { font-size: 14px; margin-right: 6px; }

  /* Responsive */
  @media (max-width: 600px) {
    .hero { padding: 40px 20px 60px; }
    .main { padding: 24px 16px 60px; }
    .tab-btn { padding: 13px 15px; font-size: 12px; }
  }
</style>
</head>
<body>

<div class="hero">
  <div class="hero-inner">
  <div class="hero-tag">UK Marketing Lead · Famly</div>
  <h1>Welcome to<br>your new adventure 👋</h1>
  <p>Two phases: week 19 is about picking Maria's brain before she goes. From 18 May, the real thing starts — five structured days to get you fully operational.</p>
  <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap;">
    <div style="flex:1;min-width:200px;max-width:400px;">
      <div class="progress-bar-wrap" style="margin:0 0 8px;">
        <div class="progress-bar-fill" id="globalProgress"></div>
      </div>
      <div class="progress-label"><span id="progressCount">0</span> of <span id="progressTotal">0</span> tasks completed</div>
    </div>
  </div>
  </div>
</div>

<!-- Mobile dropdown nav -->
<div class="mobile-nav">
  <select onchange="switchTab(this.value)" id="mobileSelect">
    <option value="overview">Overview</option>
    <option value="day1">Day 1 — Setup (18 May)</option>
    <option value="day2">Day 2 — Handover</option>
    <option value="day3">Week 2 — 26 May</option>
    <option value="day3-tools">Day 3 — Tools &amp; product</option>
    <option value="day4">Day 4 — Notion</option>
    <option value="day5">Day 5 — Friday</option>
    <option value="product">Week 2–4 — Product</option>
    <option value="team">Team & Channels</option>
  </select>
</div>

<div class="page-body">
  <!-- Sidebar navigation -->
  <nav class="sidebar">
    <div class="sidebar-label">Navigation</div>
    <div class="sidebar-group">
      <button class="tab-btn active" data-tab="overview" onclick="switchTab('overview')">
        <span class="tab-dot"></span> Overview
      </button>
    </div>
    <div class="sidebar-group">
      <div class="sidebar-group-title">Week 1 — 18 May</div>
      <button class="tab-btn" data-tab="day1" onclick="switchTab('day1')">
        <span class="tab-dot"></span> Day 1 — Setup
      </button>
      <button class="tab-btn" data-tab="day2" onclick="switchTab('day2')">
        <span class="tab-dot"></span> Day 2 — Handover
      </button>
      <button class="tab-btn" data-tab="day3-tools" onclick="switchTab('day3-tools')">
        <span class="tab-dot"></span> Day 3 — Tools & product
      </button>
      <button class="tab-btn" data-tab="day4" onclick="switchTab('day4')">
        <span class="tab-dot"></span> Day 4 — Notion
      </button>
      <button class="tab-btn" data-tab="day5" onclick="switchTab('day5')">
        <span class="tab-dot"></span> Day 5 — Friday
      </button>
    </div>
    <div class="sidebar-group">
      <div class="sidebar-group-title">Beyond week 1</div>
      <button class="tab-btn" data-tab="day3" onclick="switchTab('day3')">
        <span class="tab-dot"></span> 26 May — Your tasks
      </button>
      <button class="tab-btn" data-tab="product" onclick="switchTab('product')">
        <span class="tab-dot"></span> Week 2–4 — Product
      </button>
      <button class="tab-btn" data-tab="team" onclick="switchTab('team')">
        <span class="tab-dot"></span> Team & Channels
      </button>
    </div>
  </nav>

  <!-- Main content -->
  <div class="main">

  <!-- OVERVIEW -->
  <div class="day-panel active" id="tab-overview">
    <div class="day-header">
      <div class="day-badge overview">🗺️</div>
      <div class="day-header-text">
        <h2>Your first month at a glance</h2>
        <p>Five structured days to go from "where do I sit?" to "I run this" — followed by product deep-dives.</p>
      </div>
    </div>

    <div class="timeline" id="overviewTimeline">
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-day1">1</div>
        <div class="timeline-content">
          <h3>Day 1 — Setup & access <span style="font-size:11px;font-weight:500;color:var(--famly-muted);">18 May</span></h3>
          <p>Get your laptop unpacked, accounts created, tools installed.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-day2">2</div>
        <div class="timeline-content">
          <h3>Day 2 — Handover</h3>
          <p>Read Maria's world properly. Then get your intro meetings booked.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-day3">3</div>
        <div class="timeline-content">
          <h3>Week 2 — 26 May</h3>
          <p>Take ownership of Maria's task board. Pick one thing and move it forward today.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-day4">4</div>
        <div class="timeline-content">
          <h3>Day 4 — Go deeper</h3>
          <p>Notion project management and a first look at the product.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-day5">5</div>
        <div class="timeline-content">
          <h3>Day 5 — Wrap-up</h3>
          <p>Tie up loose ends, get final access sorted. You're almost fully operational.</p>
        </div>
      </div>
      <div class="timeline-item">
        <div class="timeline-dot" id="dot-product">📚</div>
        <div class="timeline-content">
          <h3>Week 2–4 — Product Training</h3>
          <p>9 modules with videos. Work through across your first few weeks alongside the day job.</p>
        </div>
      </div>
    </div>

    <div style="margin-top: 40px;">
      <div class="info-card" style="background:hsla(265,75%,35%,1);border-color:hsla(265,75%,35%,1);margin-bottom:16px;">
        <h3 style="color:#fff;">🎯 Your week one goal</h3>
        <p style="color:rgba(255,255,255,0.85);font-size:14px;line-height:1.7;margin:0;">By Friday 23 May, you should own Maria's active tasks and have moved at least one forward. She's on maternity leave — this is the real thing from day one. Your go-to is <strong style="color:#fff;">Matt</strong> for anything you need.</p>
      </div>

      <div class="info-card" style="background:#fff;border:1.5px dashed var(--famly-border);">
        <h3>💡 Nice to know</h3>
        <p>No deadlines, no pressure. A collection of deeper context, Gong demos, all the Slack channels, coffee chat suggestions and good-to-knows for when you have a quiet moment.</p>
        <ul>
          <li><a href="https://www.notion.so/343ff21c494c811098f3f210025e45bd" target="_blank">Open the Nice to know guide →</a></li>
        </ul>
      </div>
    </div>
  </div>

  <!-- DAY 1 -->
  <div class="day-panel" id="tab-day1">
    <div class="day-header">
      <div class="day-badge d1">1</div>
      <div class="day-header-text">
        <h2>Day 1 — Setup & access <span style="font-size:14px;font-weight:500;color:var(--famly-muted);">18 May</span></h2>
        <p>First official day — welcome to the London office. If you get stuck on anything, Matt is your go-to.</p>
      </div>
    </div>

    <div class="check-section">
      <div class="section-title">Morning</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">09:15 — Arrive at the London office <span class="check-tag tag-meet">meet</span></div>
          <div class="check-note">Jakob Hansen will meet you in the foyer. There'll be breakfast with the team to kick things off. 🥐</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">10:30 — Welcome meeting with Signe <span class="check-tag tag-meet">meet</span></div>
        </div>
      </div>
    </div>

    <div class="check-section">
      <div class="section-title">Laptop & accounts</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Unpack and set up your laptop</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/73bbc3ef39534dcd8a2a35300f123c46" target="_blank">Set up Zenegy</a> <span class="check-tag tag-tool">tool</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Set up hiBob & Officevibe (ask Neeta) <span class="check-tag tag-meet">meet</span></div>
        </div>
      </div>
    </div>

    <div class="check-section">
      <div class="section-title">Install apps</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.com/desktop" target="_blank">Install Notion desktop</a> <span class="check-tag tag-tool">tool</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://slack.com/intl/en-gb/downloads/mac" target="_blank">Install Slack desktop</a> <span class="check-tag tag-tool">tool</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://1password.com/downloads/mac" target="_blank">Install 1Password desktop</a> <span class="check-tag tag-tool">tool</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.figma.com/downloads/" target="_blank">Install Figma</a> <span class="check-tag tag-tool">tool</span></div>
          <div class="check-note">You'll use this for design assets and brand work.</div>
        </div>
      </div>
    </div>
    <div class="info-note"><span class="info-note-icon">💡</span> Tech issues? Message @Benjamin Colberg on Slack or join <strong>#it-helpdesk</strong></div>
    <button class="btn-complete" id="complete-day1" onclick="completeDay('day1')">Mark Day 1 complete 🎉</button>
  </div>

  <!-- DAY 2 -->
  <div class="day-panel" id="tab-day2">
    <div class="day-header">
      <div class="day-badge d2">2</div>
      <div class="day-header-text">
        <h2>Day 2 — Hit the ground running</h2>
        <p>The handover with Maria happened in week 19. Today is about getting your intro meetings booked and starting to understand the role from the inside.</p>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Your reference doc</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/Welcome-to-Maria-s-world-33eff21c494c8002ba52c928fd3184f7" target="_blank">👸 Maria's world</a> <span class="check-tag tag-read">read</span></div>
          <div class="check-note">You've been through this with Maria already. Keep it open as your go-to reference when questions come up.</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Today's meetings — already in your calendar</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Intro with Matt Arnerich & Julia Rose — Brand, positioning and the sector <span class="check-tag tag-meet">meet</span></div>
          <div class="check-note">Already booked in your calendar.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Intro with Gaspard Strauss <span class="check-tag tag-meet">meet</span></div>
          <div class="check-note">Already booked in your calendar.</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Book your intro meetings</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Neeta <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Matt Halsey <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Mads Naumann <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Kim Ingeman <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Kat Morris <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Alan Gibson <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Jakob B. Hanssen <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Book intro with Josie &amp; Monica <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Subject: "Intro to new UK marketing maternity cover and your area"</div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-day2" onclick="completeDay('day2')">Mark Day 2 complete 🎉</button>
  </div>

  <!-- DAY 3 -->
  <div class="day-panel" id="tab-day3">
    <div class="day-header">
      <div class="day-badge d3" style="font-size:12px;">W2</div>
      <div class="day-header-text">
        <h2>Week 2 — 26 May <span style="font-size:14px;font-weight:500;color:var(--famly-muted);">26 May</span></h2>
        <p>Matt walks you through the task board and everything that's in flight. After this session you own it.</p>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">26 May — already in your calendar</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Work and ways of working — with Matt <span class="check-tag tag-meet">meet</span></div>
          <div class="check-note">Matt walks you through how the team works, current priorities, and your tasks. Come with questions.</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">After the session</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/e9554009217441ed85cf58ceea3499f2" target="_blank">Open the UK Task Board</a> and filter by your name <span class="check-tag tag-action">action</span></div>
          <div class="check-note">You should now see everything tagged to you. This is your list — own it.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Check the <a href="https://www.notion.so/326ff21c494c80d59c3ae4c8b387e83a" target="_blank">Comms Calendar</a> — anything coming up that needs your attention? <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Add yourself to the filters so you see what's in the pipeline.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Pick one task and move it forward today <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Reply to a brief, update a status, send a draft — anything that moves it forward.</div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-day3" onclick="completeDay('day3')">Mark Day 3 complete 🎉</button>
  </div>

  <!-- DAY 3 -->
  <div class="day-panel" id="tab-day3-tools">
    <div class="day-header">
      <div class="day-badge" style="background:hsla(25,95%,92%,1);color:hsla(25,95%,35%,1);">3</div>
      <div class="day-header-text">
        <h2>Day 3 — Tools & product</h2>
        <p>Get your tools set up and take a first look at the product.</p>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Tools</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/Providing-employees-access-to-Customer-Data-Systems-f89c90001a7a4243bdf626fba075b4a7" target="_blank">Get set up on Intercom</a> — full outbound seat needed <span class="check-tag tag-tool">tool</span></div>
          <div class="check-note">Access is provisioned from your official start date. Ask Matt if it's not ready.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/Hubspot-1e3ff21c494c804196d1cf02cd3e784b" target="_blank">Get set up on HubSpot</a> — read the guide first <span class="check-tag tag-tool">tool</span></div>
          <div class="check-note">Then follow the <a href="https://www.notion.so/famly/Hubspot-first-time-setup-2cbff21c494c80da8faafca1da712b30" target="_blank">first-time setup guide</a> to get your account configured correctly.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Get added to Village as an admin <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Village is our customer community on Circle.io, 4,000+ members. You'll be responsible for moderation and content.</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">First look at the product</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.famly.co/about/video-tour" target="_blank">Watch the 3-minute Famly product tour</a> <span class="check-tag tag-action">action</span></div>
          <div class="check-note">See the product through a customer's eyes. Start here.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Log in to the Famly UK test account — search "Famly UK test account" in 1Password <span class="check-tag tag-tool">tool</span></div>
          <div class="check-note">Have a click around. The full product training is in Week 2–4.</div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-day3-tools" onclick="completeDay('day3-tools')">Mark Day 3 complete 🎉</button>
  </div>

  <!-- DAY 4 -->
  <div class="day-panel" id="tab-day4">
    <div class="day-header">
      <div class="day-badge d4">4</div>
      <div class="day-header-text">
        <h2>Day 4 — Notion</h2>
        <p>Get comfortable in Notion — it's how the whole team works.</p>
      </div>
    </div>
    <div class="info-note" style="margin-bottom:16px;">
      <span class="info-note-icon">💡</span> Questions about Notion? Reach out to <strong>Mads Naumann</strong> — he's your go-to.
    </div>
    <div class="check-section">
      <div class="section-title">Notion project management</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/How-to-use-your-new-Notion-project-management-databases-d7092153ce34445680725ec669e57ad7" target="_blank">Read: How to use our Notion project management databases</a> <span class="check-tag tag-read">read</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/Notion-tutorial-5eb4186f8e6045df89999536f7f86220" target="_blank">Complete the Notion Tutorial</a> <span class="check-tag tag-action">action</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Browse Notion broadly — get comfortable navigating it <span class="check-tag tag-action">action</span></div>
          <div class="check-note">It's the main information hub. Clicking around is not wasted time.</div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-day4" onclick="completeDay('day4')">Mark Day 4 complete 🎉</button>
  </div>

  <!-- WEEK 2-4: PRODUCT TRAINING -->
  <div class="day-panel" id="tab-week24">
    <div class="day-header">
      <div class="day-badge d4">📚</div>
      <div class="day-header-text">
        <h2>Week 2–4 — Product Training</h2>
        <p>No rush on this one — work through it across your first few weeks alongside the day job.</p>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Notion project management</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/How-to-use-your-new-Notion-project-management-databases-d7092153ce34445680725ec669e57ad7" target="_blank">Read: How to use our Notion project management databases</a> <span class="check-tag tag-read">read</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/famly/Notion-tutorial-5eb4186f8e6045df89999536f7f86220" target="_blank">Complete the Notion Tutorial</a> <span class="check-tag tag-action">action</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Browse Notion broadly — get comfortable navigating it <span class="check-tag tag-action">action</span></div>
          <div class="check-note">It's the main information hub. Clicking around is not wasted time.</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Product knowledge</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.famly.co/about/video-tour" target="_blank">Watch the 3-minute Famly product tour</a> <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Quick way to see the product through a customer's eyes. Start here.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Do the Product Training — work through all 9 modules <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Use the Product Training tab above. Find the Famly UK test account in 1Password to follow along in the actual product.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://www.notion.so/98d5f77dbd7f48b0b1e95e5ddb2f7f92" target="_blank">Explore the Product Game in Notion</a> <span class="check-tag tag-action">action</span></div>
          <div class="check-note">A fun way to learn what the product actually does feature by feature.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://app-eu1.hubspot.com/calls/25284517/review/485244118250" target="_blank">Watch sales call 1</a> <span class="check-tag tag-action">watch</span></div>
          <div class="check-note">Watch at least 2–3 sales calls. See how Famly is sold and talked about with real customers.</div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://app-eu1.hubspot.com/calls/25284517/review/485481548011" target="_blank">Watch sales call 2</a> <span class="check-tag tag-action">watch</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://app-eu1.hubspot.com/calls/25284517/review/482250229983" target="_blank">Watch sales call 3</a> <span class="check-tag tag-action">watch</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label"><a href="https://app-eu1.hubspot.com/calls/25284517/review/483525710034" target="_blank">Watch sales call 4</a> <span class="check-tag tag-action">watch</span></div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-week24" onclick="completeDay('week24')">Mark complete 🎉</button>
  </div>

  <!-- DAY 5 -->
  <div class="day-panel" id="tab-day5">
    <div class="day-header">
      <div class="day-badge d5">5</div>
      <div class="day-header-text">
        <h2>Day 5 — First week wrap-up <span style="font-size:14px;font-weight:500;color:var(--famly-muted);">Friday 22 May</span></h2>
        <p>Tie up loose ends and check in with Signe.</p>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Already in your calendar</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">12:00 — 1-1 with Signe <span class="check-tag tag-meet">meet</span></div>
          <div class="check-note">End of week check-in. How's it going? What do you need? What's still unclear?</div>
        </div>
      </div>
    </div>
    <div class="check-section">
      <div class="section-title">Wrap-up</div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Catch up on any unfinished reads or tasks from Days 1–4 <span class="check-tag tag-action">action</span></div>
        </div>
      </div>
      <div class="check-item" onclick="toggle(this)">
        <div class="check-box"><svg width="12" height="9" viewBox="0 0 12 9" fill="none"><path d="M1 4L4.5 7.5L11 1" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="check-content">
          <div class="check-label">Task transfer — coordinate with the team to get Maria's tasks reassigned to you <span class="check-tag tag-action">action</span></div>
          <div class="check-note">Ask Mads to help you find the recurring task templates and update assignments.</div>
        </div>
      </div>
    </div>
    <button class="btn-complete" id="complete-day5" onclick="completeDay('day5')">Mark Day 5 complete — you did it! 🎉</button>
  </div>

  <!-- TEAM & CHANNELS -->
  <div class="day-panel" id="tab-team">
    <div class="day-header">
      <div class="day-badge overview">👥</div>
      <div class="day-header-text">
        <h2>Team & Slack channels</h2>
        <p>People to meet and channels to join. Tap a channel pill to mark it joined.</p>
      </div>
    </div>

    <div class="info-card" style="margin-bottom: 28px;">
      <h3>People to meet</h3>
      <div class="people-grid" style="margin-top: 12px;">
        <div class="person-card"><div class="person-avatar" style="background:rgba(255,107,74,0.12);color:var(--famly-coral)">SI</div><div class="person-info"><div class="person-name">Signe</div><div class="person-role">CMO (your manager)</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(76,201,240,0.12);color:#0A7AA8">NE</div><div class="person-info"><div class="person-name">Neeta</div><div class="person-role">People Partner</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(123,94,167,0.12);color:var(--famly-purple)">MH</div><div class="person-info"><div class="person-name">Matt Halsey</div><div class="person-role">GM UK</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(255,209,102,0.2);color:#8A6400">MA</div><div class="person-info"><div class="person-name">Matt Arnerich</div><div class="person-role">Sr Dir Brand & Comms</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(6,214,160,0.12);color:#036b4f">GS</div><div class="person-info"><div class="person-name">Gaspard Strauss</div><div class="person-role">Dir Revenue Marketing</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(11,29,58,0.08);color:var(--famly-navy)">MN</div><div class="person-info"><div class="person-name">Mads Naumann</div><div class="person-role">Creative Ops Lead</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(255,107,74,0.12);color:var(--famly-coral)">JR</div><div class="person-info"><div class="person-name">Julia Rose</div><div class="person-role">Senior Content Manager</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(76,201,240,0.12);color:#0A7AA8">KI</div><div class="person-info"><div class="person-name">Kim Ingeman</div><div class="person-role">Head of Sales UK</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(123,94,167,0.12);color:var(--famly-purple)">KM</div><div class="person-info"><div class="person-name">Kat Morris</div><div class="person-role">Head of Key Accounts</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(255,209,102,0.2);color:#8A6400">AG</div><div class="person-info"><div class="person-name">Alan Gibson</div><div class="person-role">NMT events lead</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(6,214,160,0.12);color:#036b4f">JB</div><div class="person-info"><div class="person-name">Jakob B. Hanssen</div><div class="person-role">Head of CS UK</div></div></div>
        <div class="person-card"><div class="person-avatar" style="background:rgba(255,107,74,0.12);color:var(--famly-coral)">JM</div><div class="person-info"><div class="person-name">Josie & Monica</div><div class="person-role">Customer Advisory (Village)</div></div></div>
      </div>
    </div>

    <div class="info-card">
      <h3>Slack channels to join</h3>
      <p style="margin-bottom: 16px; font-size: 13px;">Tap a channel to mark it joined.</p>

      <div class="channel-group">
        <div class="channel-group-title">Marketing</div>
        <div class="channel-list">
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>marketing</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-marketing</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>marketing-budget</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>marketing-metrics</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>marketing-prio</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>summer-campaign-uk-2026</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-commercial-marketing</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>wg-village</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>beamer-activity</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>app-reviews-wg</span>
        </div>
      </div>

      <div class="channel-group">
        <div class="channel-group-title">UK</div>
        <div class="channel-list">
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>nmt-owners-clubs-events-2026</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>nursery-worlds-big-day-out-2026</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-ae</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-commercial</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-market-leadership</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-pricing-update-2026</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>uk-sales</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>wg-win-ooscs</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>win-leyf</span>
        </div>
      </div>

      <div class="channel-group">
        <div class="channel-group-title">Product</div>
        <div class="channel-list">
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>whatsnew</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>upcoming-releases</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>wg-public-roadmap</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>wg-new-invoicing-experience</span>
        </div>
      </div>

      <div class="channel-group">
        <div class="channel-group-title">Company</div>
        <div class="channel-list">
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>general</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>famlylove</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>expenses</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>wg-ai</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>it-helpdesk</span>
        </div>
      </div>

      <div class="channel-group">
        <div class="channel-group-title">Fun stuff</div>
        <div class="channel-list">
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>random</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>social-instasnap</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>social-books-podcasts</span>
          <span class="channel-pill" onclick="toggleChannel(this)"><span class="channel-hash">#</span>social-netflix-and-drama</span>
        </div>
      </div>
    </div>
  </div>



  <!-- PRODUCT TRAINING STYLES -->
  <style>
    .module-grid { display:grid; grid-template-columns:1fr; gap:12px; }
    .module-card { background:var(--famly-card); border:1px solid var(--famly-border); border-radius:12px; overflow:hidden; transition:border-color 0.15s; }
    .module-card:hover { border-color:var(--p400); }
    .module-card.done { border-color:hsla(155,73%,60%,1); background:hsla(155,73%,97%,1); }
    .module-header { display:flex; align-items:center; gap:14px; padding:16px 18px; cursor:pointer; user-select:none; }
    .module-icon { width:40px; height:40px; border-radius:10px; display:flex; align-items:center; justify-content:center; font-size:18px; flex:0 0 auto; }
    .module-icon.purple { background:hsla(265,75%,93%,1); }
    .module-icon.blue   { background:hsla(210,95%,92%,1); }
    .module-icon.green  { background:hsla(155,73%,88%,1); }
    .module-icon.orange { background:hsla(25,95%,90%,1); }
    .module-icon.yellow { background:hsla(43,95%,88%,1); }
    .module-title-wrap { flex:1; min-width:0; }
    .module-title { font-family:"Sora",sans-serif; font-size:14px; font-weight:600; color:var(--famly-text); margin-bottom:2px; }
    .module-meta { font-size:12px; color:var(--famly-muted); display:flex; gap:6px; flex-wrap:wrap; }
    .module-tag { display:inline-flex; align-items:center; gap:4px; font-size:12px; font-weight:500; padding:2px 7px; border-radius:4px; }
    .module-tag.video { background:hsla(360,80%,94%,1); color:hsla(360,70%,38%,1); }
    .module-tag.read  { background:hsla(43,95%,88%,1); color:hsla(43,80%,32%,1); }
    .module-tag.quiz  { background:hsla(265,75%,93%,1); color:var(--p400); }
    .module-toggle { font-size:20px; color:var(--famly-muted); transition:transform 0.2s; flex:0 0 auto; line-height:1; }
    .module-card.open .module-toggle { transform:rotate(90deg); }
    .module-body { display:none; border-top:1px solid var(--famly-border); padding:16px 18px; }
    .module-card.open .module-body { display:block; }
    .module-check { width:20px; height:20px; border-radius:50%; border:1.5px solid var(--famly-border); display:flex; align-items:center; justify-content:center; flex:0 0 auto; transition:all 0.2s; }
    .module-card.done .module-check { background:var(--g400); border-color:var(--g400); }
    .resource-row { display:flex; align-items:center; gap:12px; padding:10px 12px; border-radius:8px; margin-bottom:6px; background:var(--p50); border:1px solid transparent; text-decoration:none; color:var(--famly-text); transition:all 0.12s; cursor:pointer; }
    .resource-row:hover { border-color:var(--p400); background:#fff; }
    .resource-icon { width:32px; height:32px; border-radius:7px; display:flex; align-items:center; justify-content:center; font-size:14px; flex:0 0 auto; }
    .resource-icon.vid { background:hsla(360,80%,94%,1); }
    .resource-icon.doc { background:hsla(210,95%,92%,1); }
    .resource-label { flex:1; font-size:13px; font-weight:500; color:var(--famly-text); line-height:1.3; }
    .resource-sub { font-size:11.5px; color:var(--famly-muted); margin-top:1px; }
    .resource-arrow { font-size:12px; color:var(--famly-muted); flex:0 0 auto; }
    .module-done-btn { display:flex; align-items:center; justify-content:center; gap:8px; width:100%; padding:11px; background:var(--p400); color:#fff; border:none; border-radius:8px; font-family:'Mulish',sans-serif; font-size:13px; font-weight:700; cursor:pointer; margin-top:12px; transition:background 0.15s; }
    .module-done-btn:hover { background:hsla(265,75%,30%,1); }
    .module-done-btn.done { background:var(--g400); cursor:default; }
    .module-section-label { font-family:"Mulish",sans-serif; font-size:12px; font-weight:800; letter-spacing:0.3px; text-transform:none; color:var(--famly-muted); margin:16px 0 8px; }
    .module-desc { font-size:13px; color:var(--famly-muted); line-height:1.6; margin-bottom:14px; }
    .quiz-q { margin-bottom:14px; }
    .quiz-q-num { font-size:12px; font-weight:700; letter-spacing:0.2px; text-transform:none; color:var(--famly-muted); margin-bottom:5px; }
    .quiz-q-text { font-size:13.5px; font-weight:500; color:var(--famly-text); margin-bottom:8px; line-height:1.45; }
    .quiz-opts { display:flex; flex-direction:column; gap:6px; }
    .quiz-opt { display:flex; align-items:center; gap:9px; padding:9px 12px; border:1.5px solid var(--famly-border); border-radius:7px; cursor:pointer; font-size:13px; color:var(--famly-text); background:var(--p50); transition:all 0.1s; user-select:none; }
    .quiz-opt:hover { border-color:var(--p400); background:#fff; }
    .quiz-opt.correct { background:oklch(95% 0.03 155); border-color:oklch(60% 0.14 155); color:oklch(25% 0.1 155); pointer-events:none; }
    .quiz-opt.wrong   { background:hsla(360,80%,96%,1); border-color:hsla(360,80%,70%,1); color:hsla(360,60%,35%,1); pointer-events:none; }
    .quiz-opt.faded   { opacity:0.4; pointer-events:none; }
    .quiz-opt-letter { width:22px; height:22px; border-radius:5px; background:rgba(90,60,160,0.1); display:flex; align-items:center; justify-content:center; font-size:10px; font-weight:600; flex:0 0 auto; color:var(--p400); }
    .quiz-opt.correct .quiz-opt-letter { background:var(--g400); color:#fff; }
    .quiz-opt.wrong   .quiz-opt-letter { background:var(--r400); color:#fff; }
    .quiz-expl { display:none; font-size:12.5px; color:var(--famly-text); background:hsla(265,75%,97%,1); border:1px solid hsla(265,75%,78%,1); border-radius:7px; padding:10px 12px; margin-top:8px; line-height:1.6; }
    .quiz-expl.show { display:block; }
    .stat-grid { display:grid; grid-template-columns:1fr 1fr; gap:6px; margin-bottom:16px; }
    .stat-box { background:var(--p50); border:1px solid var(--famly-border); border-radius:8px; padding:10px 12px; text-align:center; }
    .stat-num { font-size:22px; font-weight:600; color:var(--p400); font-family:"Sora",sans-serif; }
    .stat-label { font-size:12px; color:var(--famly-muted); margin-top:2px; }
    .seg-box { background:var(--p50); border:1px solid var(--famly-border); border-radius:8px; padding:12px 14px; margin-bottom:6px; }
    .seg-title { font-size:12px; font-weight:600; color:var(--p400); margin-bottom:4px; }
    .seg-desc { font-size:13px; color:var(--famly-muted); line-height:1.5; }
  </style>

  <!-- PRODUCT TRAINING PANEL -->
  <div class="day-panel" id="tab-product">
    <div class="day-header">
      <div class="day-badge d4">📚</div>
      <div class="day-header-text">
        <h2>Product Training</h2>
        <p>Work through each module at your own pace. Watch the videos, read the context, then mark it done.</p>
      </div>
    </div>

    <div class="info-note" style="margin-bottom:12px;"><span class="info-note-icon">💡</span> Videos open in a new tab. Watch, then come back here to complete each module.</div>
    <div class="info-note" style="margin-bottom:24px;background:hsla(265,75%,97%,1);border-color:hsla(265,75%,78%,1);color:var(--famly-text);"><span class="info-note-icon">🔑</span> <strong>Use the Famly UK test account</strong> while working through these modules — having the product open alongside the videos makes everything click much faster. Find the login details in <strong>1Password</strong> by searching for <em>"Famly UK test account"</em>.</div>

    <div class="module-grid">

      <!-- MODULE 0: What is Famly -->
      <div class="module-card" id="mod-0">
        <div class="module-header" onclick="toggleModule('mod-0')">
          <div class="module-icon purple">🌍</div>
          <div class="module-title-wrap">
            <div class="module-title">What is Famly (UK)?</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <p class="module-desc"><strong>Famly is the early years assistant that gives childcare professionals their time back.</strong> It handles the admin that eats up the day — invoicing, rota management, observations, parent communication, compliance — so nursery owners, managers, and educators can spend less time on a screen and more time with children.</p>

          <div class="module-section-label">Brand &amp; product promise</div>
          <div style="background:var(--p50);border:1px solid var(--famly-border);border-radius:8px;padding:12px 14px;margin-bottom:12px;font-size:13px;line-height:1.7;">
            <div><strong>Tagline:</strong> Play matters, software doesn't.</div>
            <div><strong>Brand promise:</strong> Early education matters</div>
            <div><strong>Product promise:</strong> Early years professionals get more time</div>
          </div>

          <div class="module-section-label">Key proof points</div>
          <div class="stat-grid">
            <div class="stat-box"><div class="stat-num">10h</div><div class="stat-label">saved per week on admin</div></div>
            <div class="stat-box"><div class="stat-num">84%</div><div class="stat-label">of staff say Famly saves time</div></div>
            <div class="stat-box"><div class="stat-num">94%</div><div class="stat-label">say it improved family connection</div></div>
            <div class="stat-box"><div class="stat-num">1M+</div><div class="stat-label">users across ~10,000 settings</div></div>
          </div>

          <div class="module-section-label">UK segments</div>
          <div class="seg-box"><div class="seg-title">🏠 SMB — 1–5 sites</div><div class="seg-desc">Owner-led, no IT team. Time is everything. Message: <em>"Your extra pair of hands. The software that runs quietly in the background so you can get back to the children."</em></div></div>
          <div class="seg-box"><div class="seg-title">🏢 Midmarket — 6–19 sites</div><div class="seg-desc">Growing group, head office relying on Excel, stretched managers. Message: <em>"One platform, consistent processes — and reliable data from nursery floor to head office without the chasing."</em></div></div>
          <div class="seg-box"><div class="seg-title">🏙️ Enterprise — 20+ sites</div><div class="seg-desc">Busy Bees, Kids Planet, Old Station. Dedicated HR, finance, compliance. Message: <em>"Head office confidence. Nursery floor simplicity. Trusted by the UK's largest providers."</em></div></div>

          <div class="module-section-label">Watch first</div>
          <a class="resource-row" href="https://www.famly.co/about/video-tour" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">3-minute Famly product tour</div><div class="resource-sub">See the full platform through a customer's eyes</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <button class="module-done-btn" onclick="markModuleDone('mod-0', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 1: Home -->
      <div class="module-card" id="mod-1">
        <div class="module-header" onclick="toggleModule('mod-1')">
          <div class="module-icon purple">🏠</div>
          <div class="module-title-wrap">
            <div class="module-title">Home — Overview &amp; Staff</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it is</div>
          <p class="module-desc">The first thing users see when they log in — a live daily command centre. Also covers Newsfeed (parent communication) and Documents for Parents.</p>
          <div class="module-section-label">Home — what it does</div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:12px;">
            <li>Real-time overview of who's signed in (children and staff)</li>
            <li>"To-dos" widget: overdue invoices, failed payments, missing PINs</li>
            <li>Smart widget ordering — most important actions at the top</li>
            <li>Managers can see staff leave in the site overview widget</li>
          </ul>
          <div class="module-section-label">Newsfeed &amp; Documents</div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:6px;">
            <li>Post photos, videos, polls to individuals or whole groups</li>
            <li>Direct messaging — search by child name, mark all as read</li>
            <li>Live Translation — 130+ languages (Google Translate &amp; DeepL)</li>
          </ul>
          <div style="background:hsla(265,75%,97%,1);border:1px solid hsla(265,75%,78%,1);border-radius:8px;padding:11px 14px;font-size:13px;color:var(--famly-text);margin-bottom:14px;line-height:1.6;">
            <strong>🔴 Documents for Parents (Feb 2025, UK Professional &amp; Premium)</strong> — send documents that require acknowledgement, with automatic reminders and a full audit log.<br>Marketing angle: <strong>"Send it once. Know who's read it. Done."</strong>
          </div>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/5a0205487ae649b99e505c585f3d97ab" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Recording daily activities</div><div class="resource-sub">Home overview — sign in/out, daily logs, newsfeed</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/643ca8ae0af24a3dbab86c63b64d007e" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Create a news feed post</div><div class="resource-sub">Newsfeed posts, messaging, documents and forms</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/c71eb629bcdc4e46b33686571ec82f7f" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Parents view of Famly 😍</div><div class="resource-sub">What parents see in the app — newsfeed, messages, documents</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">What does Famly Home replace for a nursery manager's morning routine?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Their email inbox only</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Whiteboard + inbox + rota + spreadsheet — all in one live view</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> The staff rota only</div>
            </div>
            <div class="quiz-expl">Famly Home consolidates everything managers used to check separately. Smart widget ordering surfaces the most urgent actions first.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">What is the official marketing angle for Documents for Parents?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> "Digital documents made easy"</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> "Send it once. Know who's read it. Done."</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> "No more paper. No more chasing."</div>
            </div>
            <div class="quiz-expl">Available on UK Professional and Premium. Key features: documents require acknowledgement, automatic reminders, full audit log.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-1', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 2: Children -->
      <div class="module-card" id="mod-2">
        <div class="module-header" onclick="toggleModule('mod-2')">
          <div class="module-icon blue">👶</div>
          <div class="module-title-wrap">
            <div class="module-title">Children — Profiles, Safeguarding &amp; Health</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it covers</div>
          <p class="module-desc">Everything child-related — profiles, contacts, daily logs, and the Safeguarding section (accident forms, medication, headcount). Critical for Ofsted compliance.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li>Child profiles — personal details, allergies, contacts, medical notes</li>
            <li><strong>Collection password</strong> — parents set a code for safe child pickup (Sept 2024)</li>
            <li>Daily diary: nappies, meals, sleep, mood — done in seconds on a phone</li>
            <li>Accident &amp; incident forms — logged digitally, sent to parents instantly</li>
            <li><strong>Accident form review workflow</strong> — managers formally sign off in-app (Aug 2025)</li>
            <li>Medication forms with dosage tracking</li>
            <li>Headcount — real-time attendance visibility (under Safeguarding)</li>
            <li>Dentist field for Ofsted oral health requirements (UK-specific, Sept 2024)</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/9a6ab73c841a4f1281b27f6322666327" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Add Children</div><div class="resource-sub">Child profiles, contacts, and basic setup</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/707eae2ab5434e22946131bc480ed4a1" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Where to find important information</div><div class="resource-sub">Child profile: contacts, allergies, medical notes, collection password</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/8003347eadff4060b2fd32154dd1558c" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Head counts</div><div class="resource-sub">Real-time attendance visibility — found under Children &gt; Safeguarding</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/9d408c38fdad44c8a0dbfdd74b08a7a6" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Log an accident or incident</div><div class="resource-sub">Digital accident forms, parent notification, manager sign-off</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/0a5ec352217f43d9826e013f337a9ee2" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Creating medication forms and registering administration 🩹</div><div class="resource-sub">Medication requests, dosage records, parent consent</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">Where in the Famly app would you find Headcount?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Home &gt; Overview</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Children &gt; Safeguarding</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Attendance &gt; Reports</div>
            </div>
            <div class="quiz-expl">Headcount is under Children &gt; Safeguarding — giving staff and managers a real-time view of who is on-site at any moment.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">Which UK-specific field was added to child health profiles for Ofsted compliance?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Optician field</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Dentist field — for Ofsted oral health requirements</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> GP surgery field</div>
            </div>
            <div class="quiz-expl">The dentist field (Sept 2024) is UK-specific — a good example of Famly building for the UK market's regulatory needs.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-2', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 3: Home → Newsfeed & Documents -->
      <div class="module-card" id="mod-3">
        <div class="module-header" onclick="toggleModule('mod-3')">
          <div class="module-icon blue">💬</div>
          <div class="module-title-wrap">
            <div class="module-title">Home — Newsfeed, Messaging &amp; Documents</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it is</div>
          <p class="module-desc">A secure, professional communication channel between settings and families — replacing WhatsApp groups, emails, and paper notes.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:6px;">
            <li>Newsfeed posts with photos, videos, polls — to individuals or whole groups</li>
            <li>Direct messaging with full history and search by child name</li>
            <li>Live Translation — 130+ languages in real time (Google Translate &amp; DeepL)</li>
            <li>Comments on posts now also translated (Sept 2024)</li>
          </ul>
          <div class="module-section-label">🔴 Key feature: Documents for Parents (Feb 2025)</div>
          <div style="background:hsla(265,75%,97%,1);border:1px solid hsla(265,75%,78%,1);border-radius:8px;padding:11px 14px;font-size:13px;color:var(--famly-text);margin-bottom:14px;line-height:1.6;">
            Send documents to parents that require acknowledgement. Parents get reminders until they've read it. Full audit log — who acknowledged, when. Marketing angle: <strong>"Send it once. Know who's read it. Done."</strong><br>Available: UK Professional &amp; Premium.
          </div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li>Custom Forms (May 2025) — fully customisable fields, bulk send to whole rooms</li>
            <li>Limited Parent Access Role (May 2025) — protects separated families' privacy</li>
            <li>GDPR: parent names now shown as first name + initial to other parents (Jul 2025)</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/643ca8ae0af24a3dbab86c63b64d007e" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Create a news feed post</div><div class="resource-sub">Newsfeed posts, messaging, documents and forms</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/c71eb629bcdc4e46b33686571ec82f7f" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Parents view of Famly 😍</div><div class="resource-sub">What parents see in the app — newsfeed, messages, documents</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">Famly Live Translation supports real-time translation. How many languages?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> 60+ languages</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> 130+ languages</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> 30+ languages</div>
            </div>
            <div class="quiz-expl">130+ languages via Google Translate and DeepL. Highly relevant for the UK's multicultural nurseries. From Sept 2024, comments on posts are also translated.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">What is the official marketing angle for Documents for Parents?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> "Digital documents made easy"</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> "Send it once. Know who's read it. Done."</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> "No more paper. No more chasing."</div>
            </div>
            <div class="quiz-expl">Available on UK Professional and Premium. Key features: documents require acknowledgement, automatic reminders, full audit log.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q3</div>
            <div class="quiz-q-text">Limited Parent Access Role (May 2025) — what is the primary use case?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Parents who never log in</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Separated families — one parent shouldn't see the other's contact details</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Parents with outstanding invoices</div>
            </div>
            <div class="quiz-expl">Marketing angle: "Protect families. Handle separation sensitively." Available on all UK packages.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q4</div>
            <div class="quiz-q-text">What changed about how parent names are displayed to other parents in July 2025?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Full names are now hidden entirely</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Parents now see first name + last initial only (GDPR data minimisation)</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Parent names are replaced with usernames</div>
            </div>
            <div class="quiz-expl">A GDPR data minimisation update — parents now see "Jane S." rather than full names of other parents. Configurable per site.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-3', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 3b: Attendance -->
      <div class="module-card" id="mod-3b">
        <div class="module-header" onclick="toggleModule('mod-3b')">
          <div class="module-icon orange">📋</div>
          <div class="module-title-wrap">
            <div class="module-title">Attendance — Room Planner &amp; Registers</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it covers</div>
          <p class="module-desc">Everything in the Attendance section of the app — Room planner, child attendance, staffing view, and registration. This is where managers plan the day and track who is where.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li><strong>Room planner</strong> — drag-and-drop daily room view, ratios, who's in each room</li>
            <li><strong>Child attendance</strong> — register, sign-in/out tracking, attendance reports</li>
            <li><strong>Staffing</strong> — staff schedule view within attendance context</li>
            <li><strong>Registration</strong> — enquiries and enrolment pipeline</li>
            <li><strong>Reports</strong> — attendance, occupancy, FTE</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/b8fc39328eaf4ca2a503ee5c8ca77229" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Room planner (You register in Famly)</div><div class="resource-sub">Room setup, ratios, registers — Attendance &gt; Room planner</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">Where in the Famly app would you find Room planner?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Home &gt; Overview</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Attendance &gt; Room planner</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Children &gt; Overview</div>
            </div>
            <div class="quiz-expl">Room planner is the first item under Attendance — it gives managers a drag-and-drop view of which children and staff are in each room, with live ratio checking.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-3b', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 4: Child Development -->
      <div class="module-card" id="mod-4">
        <div class="module-header" onclick="toggleModule('mod-4')">
          <div class="module-icon green">📚</div>
          <div class="module-title-wrap">
            <div class="module-title">Learning — Child Development &amp; EYFS</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it covers</div>
          <p class="module-desc">A full EYFS-aligned suite for tracking, documenting and sharing children's developmental progress — from on-the-go observations to formal assessments and learning journeys.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li>Observations — capture on the go with photos, videos, and notes tagged to EYFS areas</li>
            <li>Statutory 2-year check and EYFS progress assessments</li>
            <li>Cohort-level view: on track, emerging, or needs support</li>
            <li>Learning Journeys — shareable digital portfolio per child</li>
            <li>Parents can now print/download their child's learning journey themselves (Sept 2024)</li>
            <li>Curriculum Builder with org-level activity library (Jul 2025) — major for enterprise</li>
            <li>SEND observations and EAL support</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/0d548d6f40664c6a8cd0ec81544d817c" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Child development overview and progress report</div><div class="resource-sub">EYFS framework, assessments, and learning journeys</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/085398b6de054ce496c5675b59622526" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Write an observation</div><div class="resource-sub">Step-by-step: capturing, tagging, and sharing with parents</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/8bf530e4555b471d8335ad132bce9d3c" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Write an assessment</div><div class="resource-sub">Progress assessments and the statutory 2-year check</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/a12f222fc3dc4618a272946e8a5c2be1" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Activity Library and Planner 🎉</div><div class="resource-sub">Curriculum builder, activity suggestions, planning tools</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">What does EYFS stand for?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Early Years Funding Scheme</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Early Years Foundation Stage</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Early Years Feature Set</div>
            </div>
            <div class="quiz-expl">Early Years Foundation Stage — the statutory curriculum framework in England. Famly is EYFS-aligned, and Ofsted checks that settings document children's development correctly.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">What changed for enterprise customers with the Org-level activity library (Jul 2025)?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Activities are now auto-generated by AI for each child</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Activities can be added to multiple sites by area selection — one action, all sites</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> The curriculum is now pre-built and cannot be customised</div>
            </div>
            <div class="quiz-expl">The org-level activity library is a significant time-saver for large groups like Busy Bees — add curriculum activities to all sites in one go rather than site by site.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q3</div>
            <div class="quiz-q-text">Since September 2024, who can print or download a child's learning journey?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Only nursery managers</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Parents can now do it themselves</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Only the child's key worker</div>
            </div>
            <div class="quiz-expl">Parents can now print/download their child's learning journey themselves — a significant time-saver for staff who used to have to do this on request.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-4', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 5: Sidekick AI -->
      <div class="module-card" id="mod-5">
        <div class="module-header" onclick="toggleModule('mod-5')">
          <div class="module-icon yellow">🤖</div>
          <div class="module-title-wrap">
            <div class="module-title">Learning — Sidekick AI</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">Why this matters — a lot</div>
          <p class="module-desc">Sidekick is Famly's built-in AI assistant, living in the right-hand side panel. It's one of Famly's strongest differentiators and the most talked-about feature in UK marketing. Understand it deeply.</p>

          <div class="module-section-label">Writing Assistant</div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:6px;">
            <li>Helps write observations, assessments, two-year checks, newsfeed posts</li>
            <li>Staff draft rough note → Sidekick produces polished, professional entry</li>
            <li>Critical for diverse teams and staff with lower written English proficiency</li>
            <li>Marketing angle: <strong>"Write better observations, faster — even on a phone."</strong></li>
          </ul>
          <div style="background:hsla(43,95%,93%,1);border:1px solid hsla(43,80%,70%,1);border-radius:8px;padding:11px 14px;font-size:13px;margin-bottom:14px;line-height:1.6;">
            <strong>🆕 Sidekick WA 2.0 (Early Access, Nov 2025)</strong> — the biggest Sidekick upgrade yet.<br>
            Voice input: speak highlights and Sidekick writes the full observation. Custom tone settings per nursery. Quick reply suggestions in conversations.<br>
            <em>Not yet for broad marketing — but know it well.</em> Marketing angle: <strong>"Speak it. Sidekick writes it."</strong>
          </div>

          <div class="module-section-label">Live Translation</div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li>130+ languages in real time</li>
            <li>Comments on posts now also translated (Sept 2024)</li>
            <li>GDPR compliant — Google EMEA processes in EU region</li>
          </ul>

          <div class="module-section-label">Coming next</div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li><strong>Sidekick Learning</strong> — AI activity suggestions tailored to each child's interests (Beta, ~20 UK settings). Not yet for broad marketing.</li>
            <li><strong>Ask Sidekick</strong> (in development) — conversational AI over your Famly data. e.g. "Which children haven't had an observation this week?"</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/d9ad7ab733184320ac50ad2b664ec3cd" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">How to Use Live In-App Translation Feature 🌎</div><div class="resource-sub">130+ languages, real-time, GDPR compliant</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">What is the marketing angle for Sidekick Writing Assistant 2.0?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> "AI observations in seconds"</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> "Speak it. Sidekick writes it."</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> "Your extra set of eyes"</div>
            </div>
            <div class="quiz-expl">WA 2.0 introduced voice input — staff speak their highlights and Sidekick writes the full observation. Still Early Access (Nov 2025) — not yet for broad marketing, but know it well.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">Why is Sidekick Writing Assistant especially valuable for UK nurseries?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> It saves the nursery money on paper</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> It's critical for diverse teams and staff with lower written English proficiency</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> It translates observations into other languages</div>
            </div>
            <div class="quiz-expl">UK nurseries often have diverse teams where written English proficiency varies. Sidekick levels the playing field — any staff member can produce polished, professional observations.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q3</div>
            <div class="quiz-q-text">What is "Ask Sidekick" — and what's its status?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> A chatbot for parents — live for all customers</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Conversational AI over Famly data (e.g. "Which children haven't had an observation this week?") — in development, not yet live</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> A help bot for staff questions about EYFS</div>
            </div>
            <div class="quiz-expl">Ask Sidekick will let users ask natural language questions about their own Famly data. In development — good to know for future content angles but not for current marketing.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-5', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 6: Finance -->
      <div class="module-card" id="mod-6">
        <div class="module-header" onclick="toggleModule('mod-6')">
          <div class="module-icon yellow">💰</div>
          <div class="module-title-wrap">
            <div class="module-title">Finances — Invoicing &amp; TFC</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it is</div>
          <p class="module-desc">A complete billing system built for the complexity of UK childcare — funded hours, top-up fees, Tax-Free Childcare, HMRC compliance, and more.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:6px;">
            <li>Auto-generated invoices from each child's plan — preview, then send in one click</li>
            <li>Annualised or actuals billing</li>
            <li>Compliant invoices with "Other charges" listing for LA audit (Aug 2025)</li>
            <li>Famly Pay — parents pay by card directly in the app</li>
            <li>Automated payment reminders and debt collection report</li>
          </ul>
          <div style="background:hsla(265,75%,97%,1);border:1px solid hsla(265,75%,78%,1);border-radius:8px;padding:11px 14px;font-size:13px;color:var(--famly-text);margin-bottom:14px;line-height:1.6;">
            <strong>🔴 Tax-Free Childcare (Mar 2025, all UK packages)</strong> — parents link their TFC account directly in Famly. Payments reconcile automatically. No manual matching, no chasing parents about government payments. Marketing angle: <strong>"TFC now just works — inside Famly."</strong>
          </div>
          <div style="background:hsla(43,95%,93%,1);border:1px solid hsla(43,80%,70%,1);border-radius:8px;padding:11px 14px;font-size:13px;margin-bottom:14px;line-height:1.6;">
            <strong>Current UK focus area: New Invoicing Experience</strong> — v1 invoicing profiles are being phased out. This is the campaign you're running. Keep regular alignment with Commercial and Product on timing.
          </div>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/170db95a3e3a4f8a9d15b996d7104dbe" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Add a plan</div><div class="resource-sub">Sessions, booking plans, and funding setup</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/860eb410e3f74d4592d9fdfea757f254" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Finance walkthrough</div><div class="resource-sub">Invoicing, billing plans, and payment management</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">TFC went live for all UK packages in March 2025. What does TFC stand for and why does it matter?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Total Finance Control — a Famly reporting feature</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Tax-Free Childcare — an HMRC scheme where the government tops up parent payments. Now integrated directly in Famly.</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Timed Fee Collection — automatic invoice scheduling</div>
            </div>
            <div class="quiz-expl">For every £8 parents pay in, the government adds £2. Famly integrated TFC so parents link their account in-app and payments reconcile automatically. Marketing angle: "TFC now just works — inside Famly."</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">What is "funding" in UK childcare — and what does Famly do to handle it?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> Venture capital for nurseries</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Free hours paid by local authorities (LA) — Famly generates LA-compliant invoices with an audit trail</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> Government support for staff salaries</div>
            </div>
            <div class="quiz-expl">Local authorities fund 15–30 free hours per week depending on age and family income. Famly handles funding allocation and generates compliant invoices with "Other charges" for LA audit.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-6', this)">Mark as done &#10003;</button>
        </div>
      </div>

      <!-- MODULE 7: Staffing -->
      <div class="module-card" id="mod-7">
        <div class="module-header" onclick="toggleModule('mod-7')">
          <div class="module-icon orange">👩‍💼</div>
          <div class="module-title-wrap">
            <div class="module-title">Staff Management &amp; Rotas</div>
            <div class="module-meta"><span class="module-tag video">&#9654; Video</span><span class="module-tag read">Context</span><span class="module-tag quiz">Quiz</span></div>
          </div>
          <div class="module-check"><svg width="10" height="8" viewBox="0 0 10 8" fill="none"><path d="M1 4L3.5 6.5L9 1" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
          <div class="module-toggle">&#x203A;</div>
        </div>
        <div class="module-body">
          <div class="module-section-label">What it is</div>
          <p class="module-desc">A complete staff management system — scheduling, absence, qualifications, and time tracking. Built to replace the spreadsheets and disconnected tools most nurseries are stuck with.</p>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:6px;">
            <li>Drag-and-drop weekly rota builder with real-time who's-in view</li>
            <li>Manager Notes in shifts (Oct 2024)</li>
            <li>Closure days now visible on Staff Schedule (Mar 2026)</li>
            <li>Staff qualifications — certificates stored with expiry alerts</li>
          </ul>
          <div style="background:hsla(265,75%,97%,1);border:1px solid hsla(265,75%,78%,1);border-radius:8px;padding:11px 14px;font-size:13px;color:var(--famly-text);margin-bottom:6px;line-height:1.6;">
            <strong>🔴 Absence Management (Jun 2025 — default for all UK)</strong> — holiday entitlement, overlap visibility, auto-unassigning of shifts when absence is recorded. Replaces Excel-based leave tracking. Marketing angle: <strong>"Your rota and your absence management — finally in one place."</strong>
          </div>
          <ul style="font-size:13px;color:var(--famly-muted);line-height:1.8;padding-left:18px;margin-bottom:14px;">
            <li><strong>Staff Hours Approval</strong> (Jun 2025, Early Access) — managers lock hours per pay period. Marketing angle: "Know your payroll before it hits accounting."</li>
            <li><strong>Role-Based Login Security</strong> (Nov 2025) — assign MFA/SSO per role, not org-wide. Launched after UK nursery sector data breach. Marketing angle: "Security that fits your team structure."</li>
          </ul>

          <div class="module-section-label">Watch</div>
          <a class="resource-row" href="https://www.loom.com/share/ef3f404e093846ec8517a30dc76efc7a" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Update your setting's information</div><div class="resource-sub">Site details, opening hours, and account setup</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/0b1d5916da1841c4848d6f2d9f3e22c5" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Add Staff</div><div class="resource-sub">Staff accounts, roles and permissions</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>
          <a class="resource-row" href="https://www.loom.com/share/857f424f1b5d4644b21ff9e01b73d774" target="_blank">
            <div class="resource-icon vid">&#9654;</div>
            <div><div class="resource-label">Staff profile overview</div><div class="resource-sub">Staff profile, notifications, and account settings</div></div>
            <div class="resource-arrow">&#x2197;</div>
          </a>

          <div class="module-section-label">Quick quiz</div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q1</div>
            <div class="quiz-q-text">Absence Management became the default for all UK customers in June 2025. What's the marketing angle?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> "HR in your pocket"</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> "Your rota and your absence management — finally in one place."</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> "Always know your ratios"</div>
            </div>
            <div class="quiz-expl">It replaces Excel-based absence tracking. Key features: holiday entitlement, overlap visibility, auto-removal of shifts when absence is recorded.</div>
          </div>
          <div class="quiz-q" data-answered="false">
            <div class="quiz-q-num">Q2</div>
            <div class="quiz-q-text">Role-Based Login Security (Nov 2025) — what is the context behind its launch?</div>
            <div class="quiz-opts">
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">A</span> A routine security update requested by enterprise clients</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'correct')"><span class="quiz-opt-letter">B</span> Launched after a data breach in the UK nursery sector — lets you assign MFA to managers without requiring it for all staff</div>
              <div class="quiz-opt" onclick="quizAnswer(this,'wrong')"><span class="quiz-opt-letter">C</span> A GDPR requirement from the ICO</div>
            </div>
            <div class="quiz-expl">Marketing angle: "Security that fits your team structure." Managers on MFA, educators on standard login. The flexibility enterprise groups needed without forcing all 200 staff onto MFA.</div>
          </div>
          <button class="module-done-btn" onclick="markModuleDone('mod-7', this)">Mark as done &#10003;</button>
        </div>
      </div>

    </div>

    <div id="product-complete-banner" style="margin-top:20px;"></div>
  </div>
</div><!-- /.main -->
</div><!-- /.page-body -->

<script>
  const dayOrder = ['day1','day2','day3-tools','day4','day5','week24','product'];
  const completedDays = new Set();
  const doneModules = new Set();

  function toggleModule(id) {
    document.getElementById(id).classList.toggle('open');
  }

  function quizAnswer(optEl, result) {
    const q = optEl.closest('.quiz-q');
    if (q.dataset.answered === 'true') return;
    q.dataset.answered = 'true';
    q.querySelectorAll('.quiz-opt').forEach(o => o.classList.add('faded'));
    optEl.classList.remove('faded');
    optEl.classList.add(result);
    const expl = q.querySelector('.quiz-expl');
    if (expl) expl.classList.add('show');
  }

  function markModuleDone(id, btn) {
    const card = document.getElementById(id);
    card.classList.add('done');
    btn.classList.add('done');
    btn.textContent = '\u2713 Done';
    doneModules.add(id);
    updateProgress();
    if (doneModules.size === 9) {
      completedDays.add('product');
      updateTabDots();
      document.getElementById('product-complete-banner').innerHTML = '<div class="info-note" style="background:oklch(95% 0.03 155);border-color:oklch(60% 0.14 155);color:oklch(25% 0.1 155);"><span class="info-note-icon">&#127881;</span> <strong>Product training complete!</strong> You know the platform. Go make great marketing.</div>';
    }
  }

  function switchTab(id) {
    document.querySelectorAll('.day-panel').forEach(p => p.classList.remove('active'));
    document.getElementById('tab-' + id).classList.add('active');
    document.querySelectorAll('.tab-btn').forEach(b => {
      b.classList.remove('active');
      if (b.dataset.tab === id) b.classList.add('active');
    });
    const sel = document.getElementById('mobileSelect');
    if (sel) sel.value = id;
  }

  function toggle(el) {
    el.classList.toggle('done');
    updateProgress();
  }

  function toggleChannel(el) {
    el.classList.toggle('joined');
  }

  function completeDay(day) {
    const panel = document.getElementById('tab-' + day);
    const items = panel.querySelectorAll('.check-item');
    items.forEach(i => i.classList.add('done'));
    completedDays.add(day);
    const btn = document.getElementById('complete-' + day);
    if (btn) { btn.classList.add('done-state'); btn.textContent = '\u2713 Done!'; }
    updateProgress();
    updateTimeline();
    updateTabDots();
    const nextIndex = dayOrder.indexOf(day) + 1;
    if (nextIndex < dayOrder.length) {
      setTimeout(() => switchTab(dayOrder[nextIndex]), 600);
    }
  }

  function updateProgress() {
    const all = document.querySelectorAll('.check-item');
    const done = document.querySelectorAll('.check-item.done');
    const pct = all.length ? Math.round((done.length / all.length) * 100) : 0;
    document.getElementById('globalProgress').style.transform = 'scaleX(' + (pct/100) + ')';
    document.getElementById('progressCount').textContent = done.length;
    document.getElementById('progressTotal').textContent = all.length;
  }

  function updateTimeline() {
    dayOrder.forEach((day, i) => {
      const dot = document.getElementById('dot-' + day);
      if (!dot) return;
      if (completedDays.has(day)) {
        dot.classList.add('done');
        dot.classList.remove('active');
        dot.textContent = '\u2713';
      } else if (i === 0 || completedDays.has(dayOrder[i - 1])) {
        dot.classList.add('active');
      }
    });
  }

  function updateTabDots() {
    dayOrder.forEach(day => {
      const btn = document.querySelector('[data-tab="' + day + '"]');
      if (btn && completedDays.has(day)) btn.classList.add('completed');
    });
  }

  updateProgress();
  updateTimeline();
</script>
</body>
</html>
