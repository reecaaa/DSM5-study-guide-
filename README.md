<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DSM-5-TR | RPM Board Exam Mastery Guide</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@400;500&family=Lora:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0c10;
    --surface: #111318;
    --surface2: #181c24;
    --border: #252a35;
    --accent: #4af0a8;
    --accent2: #f0a84a;
    --accent3: #a84af0;
    --accent4: #f04a4a;
    --text: #e8eaf0;
    --muted: #7a8099;
    --highlight: #1a2a1e;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Lora', Georgia, serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* HEADER */
  header {
    background: linear-gradient(135deg, #0a0c10 0%, #0d1a14 50%, #0a0c10 100%);
    border-bottom: 1px solid var(--border);
    padding: 2rem 2rem 1.5rem;
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(12px);
  }
  .header-inner {
    max-width: 1400px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    gap: 1.5rem;
    flex-wrap: wrap;
  }
  .logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1.1rem;
    color: var(--accent);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    white-space: nowrap;
  }
  .logo span { color: var(--muted); font-weight: 400; }
  .search-bar {
    flex: 1;
    min-width: 200px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.5rem 1rem;
    color: var(--text);
    font-family: 'DM Mono', monospace;
    font-size: 0.85rem;
    outline: none;
    transition: border-color 0.2s;
  }
  .search-bar:focus { border-color: var(--accent); }
  .search-bar::placeholder { color: var(--muted); }
  .tab-bar {
    display: flex;
    gap: 0.4rem;
    flex-wrap: wrap;
  }
  .tab {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 0.35rem 0.75rem;
    border-radius: 6px;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--muted);
    cursor: pointer;
    transition: all 0.2s;
    white-space: nowrap;
  }
  .tab:hover, .tab.active {
    background: var(--accent);
    color: #000;
    border-color: var(--accent);
  }

  /* LAYOUT */
  .app-body {
    max-width: 1400px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 260px 1fr;
    gap: 0;
    min-height: calc(100vh - 80px);
  }

  /* SIDEBAR */
  .sidebar {
    border-right: 1px solid var(--border);
    padding: 1.5rem 0;
    position: sticky;
    top: 80px;
    height: calc(100vh - 80px);
    overflow-y: auto;
  }
  .sidebar::-webkit-scrollbar { width: 4px; }
  .sidebar::-webkit-scrollbar-track { background: transparent; }
  .sidebar::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }
  .sidebar-section {
    padding: 0 1rem 1rem;
  }
  .sidebar-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.65rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    padding: 0.5rem 0.5rem 0.25rem;
    margin-bottom: 0.25rem;
  }
  .nav-item {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.4rem 0.6rem;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.15s;
    font-family: 'Syne', sans-serif;
    font-size: 0.78rem;
    font-weight: 500;
    color: var(--muted);
    border: none;
    background: none;
    width: 100%;
    text-align: left;
  }
  .nav-item:hover { background: var(--surface); color: var(--text); }
  .nav-item.active { background: var(--highlight); color: var(--accent); }
  .nav-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--border);
    flex-shrink: 0;
  }
  .nav-item.active .nav-dot { background: var(--accent); }

  /* MAIN CONTENT */
  .main-content {
    padding: 2rem;
    overflow-y: auto;
  }
  .view { display: none; }
  .view.active { display: block; }

  /* CARDS */
  .section-header {
    margin-bottom: 2rem;
  }
  .section-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 2rem;
    line-height: 1.1;
    margin-bottom: 0.5rem;
  }
  .section-subtitle {
    color: var(--muted);
    font-size: 0.9rem;
    font-style: italic;
  }

  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 1.25rem;
  }
  .card-title {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 1rem;
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .badge {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    padding: 0.15rem 0.5rem;
    border-radius: 4px;
    font-weight: 500;
    letter-spacing: 0.05em;
  }
  .badge-green { background: #1a3020; color: var(--accent); }
  .badge-orange { background: #2a1e0a; color: var(--accent2); }
  .badge-purple { background: #1e0a2a; color: var(--accent3); }
  .badge-red { background: #2a0a0a; color: var(--accent4); }

  /* TABLES */
  .tbl-wrap { overflow-x: auto; margin: 0.75rem 0; }
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.82rem;
  }
  th {
    background: var(--surface2);
    font-family: 'Syne', sans-serif;
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    padding: 0.6rem 0.8rem;
    text-align: left;
    border-bottom: 1px solid var(--border);
    white-space: nowrap;
  }
  td {
    padding: 0.55rem 0.8rem;
    border-bottom: 1px solid var(--border);
    vertical-align: top;
    line-height: 1.5;
  }
  tr:last-child td { border-bottom: none; }
  tr:hover td { background: var(--surface2); }

  /* MNEMONICS */
  .mnemonic {
    background: linear-gradient(135deg, #0d1a14, #101424);
    border: 1px solid #2a3530;
    border-left: 3px solid var(--accent);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    margin: 0.75rem 0;
    font-family: 'DM Mono', monospace;
    font-size: 0.82rem;
  }
  .mnemonic-label {
    font-size: 0.65rem;
    color: var(--accent);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.4rem;
    font-weight: 500;
  }
  .pearl {
    background: linear-gradient(135deg, #1a1500, #241a00);
    border: 1px solid #3a2e00;
    border-left: 3px solid var(--accent2);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    margin: 0.75rem 0;
    font-size: 0.85rem;
  }
  .pearl-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.65rem;
    color: var(--accent2);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.4rem;
    font-weight: 700;
  }
  .trap {
    background: linear-gradient(135deg, #1a0a0a, #240d0d);
    border: 1px solid #3a1515;
    border-left: 3px solid var(--accent4);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    margin: 0.75rem 0;
    font-size: 0.85rem;
  }
  .trap-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.65rem;
    color: var(--accent4);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.4rem;
    font-weight: 700;
  }

  /* CRITERIA BOXES */
  .criteria-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 0.75rem;
    margin: 0.75rem 0;
  }
  .criteria-box {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.75rem;
    text-align: center;
  }
  .criteria-val {
    font-family: 'Syne', sans-serif;
    font-size: 1.6rem;
    font-weight: 800;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 0.2rem;
  }
  .criteria-lbl {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }

  /* GRID LAYOUTS */
  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .three-col { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1rem; }
  @media(max-width: 900px) {
    .app-body { grid-template-columns: 1fr; }
    .sidebar { position: static; height: auto; }
    .two-col, .three-col { grid-template-columns: 1fr; }
  }

  b, strong { color: var(--accent2); font-weight: 600; }
  em { color: var(--accent3); font-style: italic; }
  ul { padding-left: 1.2rem; }
  li { margin-bottom: 0.25rem; line-height: 1.6; }

  /* QUIZ SECTION */
  .quiz-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 1rem;
  }
  .quiz-question {
    font-size: 0.95rem;
    margin-bottom: 1rem;
    line-height: 1.6;
  }
  .quiz-options { display: flex; flex-direction: column; gap: 0.4rem; }
  .quiz-opt {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.6rem 1rem;
    cursor: pointer;
    font-size: 0.85rem;
    transition: all 0.2s;
    text-align: left;
    color: var(--text);
    font-family: 'Lora', serif;
  }
  .quiz-opt:hover { border-color: var(--accent); background: var(--highlight); }
  .quiz-opt.correct { background: var(--highlight); border-color: var(--accent); color: var(--accent); }
  .quiz-opt.wrong { background: #1a0a0a; border-color: var(--accent4); color: var(--accent4); }
  .quiz-explanation {
    display: none;
    margin-top: 1rem;
    padding: 0.75rem 1rem;
    background: var(--surface2);
    border-radius: 8px;
    font-size: 0.82rem;
    color: var(--muted);
    line-height: 1.6;
  }
  .quiz-explanation.show { display: block; }

  /* AI CHAT */
  .ai-input-area {
    display: flex;
    gap: 0.75rem;
    margin-top: 1rem;
  }
  .ai-input {
    flex: 1;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.75rem 1rem;
    color: var(--text);
    font-family: 'Lora', serif;
    font-size: 0.875rem;
    outline: none;
    resize: vertical;
    min-height: 60px;
    transition: border-color 0.2s;
  }
  .ai-input:focus { border-color: var(--accent); }
  .ai-input::placeholder { color: var(--muted); }
  .btn {
    font-family: 'Syne', sans-serif;
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    padding: 0.6rem 1.2rem;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    white-space: nowrap;
  }
  .btn-primary { background: var(--accent); color: #000; }
  .btn-primary:hover { background: #2ad888; }
  .btn-primary:disabled { opacity: 0.5; cursor: not-allowed; }
  .ai-response {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.25rem;
    margin-top: 1rem;
    font-size: 0.875rem;
    line-height: 1.7;
    min-height: 60px;
    display: none;
  }
  .ai-response.show { display: block; }
  .ai-response.loading { color: var(--muted); }
  .typing-indicator { display: inline-flex; gap: 4px; align-items: center; }
  .typing-indicator span {
    width: 6px; height: 6px; border-radius: 50%;
    background: var(--accent);
    animation: bounce 1.2s infinite;
  }
  .typing-indicator span:nth-child(2) { animation-delay: 0.2s; }
  .typing-indicator span:nth-child(3) { animation-delay: 0.4s; }
  @keyframes bounce {
    0%, 60%, 100% { transform: translateY(0); }
    30% { transform: translateY(-6px); }
  }

  /* OVERVIEW GRID */
  .overview-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 0.75rem;
    margin-bottom: 2rem;
  }
  .overview-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1rem;
    cursor: pointer;
    transition: all 0.2s;
  }
  .overview-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .ov-num {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1.8rem;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 0.25rem;
  }
  .ov-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.75rem;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 0.15rem;
  }
  .ov-sub {
    font-size: 0.7rem;
    color: var(--muted);
  }

  /* highlight searched terms */
  .highlight { background: rgba(74,240,168,0.2); border-radius: 3px; padding: 0 2px; }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <div class="logo">DSM-5-TR <span>/ RPM Mastery</span></div>
    <input class="search-bar" id="globalSearch" placeholder="Search any disorder, symptom, or concept..." oninput="handleSearch(this.value)">
    <div class="tab-bar">
      <button class="tab active" onclick="switchTab('overview', this)">Overview</button>
      <button class="tab" onclick="switchTab('neurodevelopmental', this)">Neurodev</button>
      <button class="tab" onclick="switchTab('psychotic', this)">Psychotic</button>
      <button class="tab" onclick="switchTab('bipolar', this)">Bipolar</button>
      <button class="tab" onclick="switchTab('depressive', this)">Depressive</button>
      <button class="tab" onclick="switchTab('anxiety', this)">Anxiety</button>
      <button class="tab" onclick="switchTab('ocd', this)">OCD</button>
      <button class="tab" onclick="switchTab('trauma', this)">Trauma</button>
      <button class="tab" onclick="switchTab('dissociative', this)">Dissociative</button>
      <button class="tab" onclick="switchTab('somatic', this)">Somatic</button>
      <button class="tab" onclick="switchTab('eating', this)">Eating</button>
      <button class="tab" onclick="switchTab('personality', this)">Personality</button>
      <button class="tab" onclick="switchTab('neurocognitive', this)">NeuroCog</button>
      <button class="tab" onclick="switchTab('substance', this)">Substance</button>
      <button class="tab" onclick="switchTab('treatments', this)">Treatments</button>
      <button class="tab" onclick="switchTab('quiz', this)">Quiz</button>
      <button class="tab" onclick="switchTab('ai', this)">AI Tutor</button>
    </div>
  </div>
</header>

<div class="app-body">
  <aside class="sidebar">
    <div class="sidebar-section">
      <div class="sidebar-label">Categories</div>
      <button class="nav-item active" onclick="switchView('overview', this)"><span class="nav-dot"></span>Overview & Intro</button>
      <button class="nav-item" onclick="switchView('neurodevelopmental', this)"><span class="nav-dot"></span>Neurodevelopmental</button>
      <button class="nav-item" onclick="switchView('psychotic', this)"><span class="nav-dot"></span>Psychotic Disorders</button>
      <button class="nav-item" onclick="switchView('bipolar', this)"><span class="nav-dot"></span>Bipolar & Related</button>
      <button class="nav-item" onclick="switchView('depressive', this)"><span class="nav-dot"></span>Depressive Disorders</button>
      <button class="nav-item" onclick="switchView('anxiety', this)"><span class="nav-dot"></span>Anxiety Disorders</button>
      <button class="nav-item" onclick="switchView('ocd', this)"><span class="nav-dot"></span>OCD & Related</button>
      <button class="nav-item" onclick="switchView('trauma', this)"><span class="nav-dot"></span>Trauma & Stressor</button>
      <button class="nav-item" onclick="switchView('dissociative', this)"><span class="nav-dot"></span>Dissociative</button>
      <button class="nav-item" onclick="switchView('somatic', this)"><span class="nav-dot"></span>Somatic & Related</button>
      <button class="nav-item" onclick="switchView('eating', this)"><span class="nav-dot"></span>Eating Disorders</button>
      <button class="nav-item" onclick="switchView('personality', this)"><span class="nav-dot"></span>Personality Disorders</button>
      <button class="nav-item" onclick="switchView('neurocognitive', this)"><span class="nav-dot"></span>Neurocognitive</button>
      <button class="nav-item" onclick="switchView('substance', this)"><span class="nav-dot"></span>Substance-Related</button>
      <button class="nav-item" onclick="switchView('sexual', this)"><span class="nav-dot"></span>Sexual & Gender</button>
      <button class="nav-item" onclick="switchView('sleep', this)"><span class="nav-dot"></span>Sleep-Wake</button>
      <button class="nav-item" onclick="switchView('disruptive', this)"><span class="nav-dot"></span>Disruptive/Conduct</button>
    </div>
    <div class="sidebar-section">
      <div class="sidebar-label">Tools</div>
      <button class="nav-item" onclick="switchView('treatments', this)"><span class="nav-dot"></span>Treatment Cheat Sheet</button>
      <button class="nav-item" onclick="switchView('quiz', this)"><span class="nav-dot"></span>Board Exam Quiz</button>
      <button class="nav-item" onclick="switchView('ai', this)"><span class="nav-dot"></span>AI Study Tutor</button>
      <button class="nav-item" onclick="switchView('master', this)"><span class="nav-dot"></span>Master Review</button>
    </div>
  </aside>

  <main class="main-content">

    <!-- ===== OVERVIEW ===== -->
    <div class="view active" id="view-overview">
      <div class="section-header">
        <div class="section-tag">RPM / BLEPP Board Exam</div>
        <div class="section-title">DSM-5-TR Mastery Guide</div>
        <div class="section-subtitle">The 20% that generates 80% of board exam questions — with board pearls, mnemonics, and differentials</div>
      </div>

      <div class="overview-grid">
        <div class="overview-card" onclick="switchView('neurodevelopmental')">
          <div class="ov-num">6</div>
          <div class="ov-label">Neurodevelopmental</div>
          <div class="ov-sub">ADHD, ASD, ID, SLD, Tic</div>
        </div>
        <div class="overview-card" onclick="switchView('psychotic')">
          <div class="ov-num">5</div>
          <div class="ov-label">Psychotic Disorders</div>
          <div class="ov-sub">Schizophrenia, Brief, Delusional</div>
        </div>
        <div class="overview-card" onclick="switchView('bipolar')">
          <div class="ov-num">4</div>
          <div class="ov-label">Bipolar & Related</div>
          <div class="ov-sub">Bipolar I, II, Cyclothymia</div>
        </div>
        <div class="overview-card" onclick="switchView('depressive')">
          <div class="ov-num">5</div>
          <div class="ov-label">Depressive Disorders</div>
          <div class="ov-sub">MDD, PDD, PMDD, DMDD</div>
        </div>
        <div class="overview-card" onclick="switchView('anxiety')">
          <div class="ov-num">6</div>
          <div class="ov-label">Anxiety Disorders</div>
          <div class="ov-sub">GAD, Panic, Phobias, Social</div>
        </div>
        <div class="overview-card" onclick="switchView('ocd')">
          <div class="ov-num">5</div>
          <div class="ov-label">OCD & Related</div>
          <div class="ov-sub">OCD, BDD, Hoarding, Trichotillo</div>
        </div>
        <div class="overview-card" onclick="switchView('trauma')">
          <div class="ov-num">4</div>
          <div class="ov-label">Trauma & Stressor</div>
          <div class="ov-sub">PTSD, ASD, Adjustment, RAD</div>
        </div>
        <div class="overview-card" onclick="switchView('dissociative')">
          <div class="ov-num">3</div>
          <div class="ov-label">Dissociative</div>
          <div class="ov-sub">DID, Amnesia, Deper/Drereal</div>
        </div>
        <div class="overview-card" onclick="switchView('eating')">
          <div class="ov-num">5</div>
          <div class="ov-label">Eating Disorders</div>
          <div class="ov-sub">AN, BN, BED, ARFID, Pica</div>
        </div>
        <div class="overview-card" onclick="switchView('personality')">
          <div class="ov-num">10</div>
          <div class="ov-label">Personality Disorders</div>
          <div class="ov-sub">Cluster A, B, C</div>
        </div>
        <div class="overview-card" onclick="switchView('neurocognitive')">
          <div class="ov-num">4</div>
          <div class="ov-label">Neurocognitive</div>
          <div class="ov-sub">Delirium, Major/Mild NCD, Alz</div>
        </div>
        <div class="overview-card" onclick="switchView('substance')">
          <div class="ov-num">11</div>
          <div class="ov-label">Substance-Related</div>
          <div class="ov-sub">Use disorders, intoxication, WD</div>
        </div>
      </div>

      <div class="card">
        <div class="card-title">🎯 How Board Exams Are Structured <span class="badge badge-orange">Strategy</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Question Type</th><th>Frequency</th><th>What to Master</th></tr>
            <tr><td>Differential Diagnosis</td><td><b>~35%</b></td><td>Key distinguishing features between similar disorders</td></tr>
            <tr><td>Diagnostic Criteria</td><td><b>~25%</b></td><td>Symptom counts, duration requirements, specifiers</td></tr>
            <tr><td>Treatment/Intervention</td><td><b>~20%</b></td><td>Gold-standard pairings (ERP → OCD, DBT → BPD)</td></tr>
            <tr><td>Case Vignettes</td><td><b>~15%</b></td><td>Identify disorder from symptoms described in a story</td></tr>
            <tr><td>Assessment Tools</td><td><b>~5%</b></td><td>Which scale goes with which disorder</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Master Formula</div>
          <strong>D-D-T-V-A</strong> = Differentials, Duration, Treatment, Vignette, Assessment<br>
          Focus 80% of study time here → 80% of board points.
        </div>
      </div>

      <div class="card">
        <div class="card-title">⚡ Top 20 Most Tested DSM Facts (Quick Fire) <span class="badge badge-red">Must Know</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>#</th><th>Fact</th><th>Category</th></tr>
            <tr><td>1</td><td>Schizophrenia duration: <b>≥6 months</b> (with ≥1 month active phase)</td><td>Psychotic</td></tr>
            <tr><td>2</td><td>MDD: <b>≥5</b> symptoms, <b>2-week</b> minimum, must include depressed mood OR anhedonia</td><td>Depressive</td></tr>
            <tr><td>3</td><td>PTSD: symptoms last <b>>1 month</b>; Acute Stress Disorder: <b>3 days–1 month</b></td><td>Trauma</td></tr>
            <tr><td>4</td><td>Mania: <b>≥7 days</b> (any duration if hospitalized); Hypomania: <b>≥4 days</b></td><td>Bipolar</td></tr>
            <tr><td>5</td><td>GAD: <b>≥6 months</b>, <b>≥3</b> worry symptoms (adults); <b>≥1</b> in children</td><td>Anxiety</td></tr>
            <tr><td>6</td><td>Gold-standard for OCD = <b>ERP (Exposure & Response Prevention)</b></td><td>Treatment</td></tr>
            <tr><td>7</td><td>Gold-standard for BPD = <b>DBT (Dialectical Behavior Therapy)</b></td><td>Treatment</td></tr>
            <tr><td>8</td><td>ADHD: symptoms present before <b>age 12</b> in ≥2 settings</td><td>Neurodevelopmental</td></tr>
            <tr><td>9</td><td>Anorexia AN: refusal to maintain <b>≥85%</b> expected body weight (BMI <b><17.5</b>)</td><td>Eating</td></tr>
            <tr><td>10</td><td>Intellectual Disability: IQ <b>≤70</b> (approximately) + adaptive deficits + onset <b>before 18</b></td><td>Neurodevelopmental</td></tr>
            <tr><td>11</td><td>Brief Psychotic Disorder: <b>1 day–1 month</b></td><td>Psychotic</td></tr>
            <tr><td>12</td><td>Schizophreniform: <b>1–6 months</b></td><td>Psychotic</td></tr>
            <tr><td>13</td><td>Persistent Depressive Disorder (Dysthymia): <b>≥2 years</b> adults, <b>≥1 year</b> children</td><td>Depressive</td></tr>
            <tr><td>14</td><td>Cyclothymia: <b>≥2 years</b>, numerous hypomanic + depressive symptoms (not full episodes)</td><td>Bipolar</td></tr>
            <tr><td>15</td><td>DID formerly called <b>Multiple Personality Disorder</b></td><td>Dissociative</td></tr>
            <tr><td>16</td><td>Conversion Disorder = <b>Functional Neurological Symptom Disorder</b></td><td>Somatic</td></tr>
            <tr><td>17</td><td>Malingering: <b>intentional</b>, for external gain; Factitious: intentional, <b>no external gain</b></td><td>Somatic</td></tr>
            <tr><td>18</td><td>Antisocial PD: requires conduct disorder before <b>age 15</b>, diagnosed ≥<b>age 18</b></td><td>Personality</td></tr>
            <tr><td>19</td><td>Delirium: <b>acute, fluctuating</b>; Dementia: chronic, <b>progressive</b></td><td>Neurocognitive</td></tr>
            <tr><td>20</td><td>ABA (Applied Behavior Analysis) = gold standard for <b>ASD</b></td><td>Treatment</td></tr>
          </table>
        </div>
      </div>
    </div>

    <!-- ===== NEURODEVELOPMENTAL ===== -->
    <div class="view" id="view-neurodevelopmental">
      <div class="section-header">
        <div class="section-tag">Category 1</div>
        <div class="section-title">Neurodevelopmental Disorders</div>
        <div class="section-subtitle">ADHD, ASD, Intellectual Disability, Specific Learning Disorder, Tic Disorders</div>
      </div>

      <!-- ADHD -->
      <div class="card">
        <div class="card-title">ADHD — Attention-Deficit/Hyperactivity Disorder <span class="badge badge-orange">High Yield</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≥6</div><div class="criteria-lbl">Symptoms (children)</div></div>
          <div class="criteria-box"><div class="criteria-val">≥5</div><div class="criteria-lbl">Symptoms (≥17 yrs)</div></div>
          <div class="criteria-box"><div class="criteria-val">6 mo</div><div class="criteria-lbl">Duration minimum</div></div>
          <div class="criteria-box"><div class="criteria-val"><12</div><div class="criteria-lbl">Age of onset (symptoms)</div></div>
          <div class="criteria-box"><div class="criteria-val">≥2</div><div class="criteria-lbl">Settings required</div></div>
        </div>
        <div class="two-col">
          <div>
            <strong>Inattentive Symptoms (≥6/9):</strong>
            <ul style="margin-top:0.5rem">
              <li>Fails to give close attention to details / careless mistakes</li>
              <li>Difficulty sustaining attention in tasks</li>
              <li>Does not seem to listen when spoken to directly</li>
              <li>Does not follow through on instructions</li>
              <li>Difficulty organizing tasks and activities</li>
              <li>Avoids tasks requiring sustained mental effort</li>
              <li>Loses things necessary for tasks</li>
              <li>Easily distracted by extraneous stimuli</li>
              <li>Forgetful in daily activities</li>
            </ul>
          </div>
          <div>
            <strong>Hyperactive-Impulsive Symptoms (≥6/9):</strong>
            <ul style="margin-top:0.5rem">
              <li>Fidgets with hands/feet or squirms</li>
              <li>Leaves seat when expected to remain seated</li>
              <li>Runs about/climbs inappropriately</li>
              <li>Unable to play quietly</li>
              <li>"On the go" / driven by a motor</li>
              <li>Talks excessively</li>
              <li>Blurts out answers</li>
              <li>Difficulty waiting turn</li>
              <li>Interrupts or intrudes on others</li>
            </ul>
          </div>
        </div>
        <div class="tbl-wrap" style="margin-top:1rem">
          <table>
            <tr><th>Presentation</th><th>Criteria</th><th>Board Clue</th></tr>
            <tr><td>Predominantly Inattentive</td><td>≥6 inattentive only</td><td>"Daydreamer," loses things, disorganized</td></tr>
            <tr><td>Predominantly H-I</td><td>≥6 hyperactive-impulsive only</td><td>Can't sit still, impulsive, talks too much</td></tr>
            <tr><td>Combined</td><td>≥6 of BOTH</td><td>Most common clinical presentation</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Board Pearl</div>
          ADHD in adults needs only <b>≥5 symptoms</b> (not 6). Symptoms must be present <b>before age 12</b>, in <b>≥2 settings</b>. NEVER diagnosed if only at home or only at school.
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Mnemonic — Inattentive: "CLAMS DOF"</div>
          <b>C</b>areless errors · <b>L</b>istening problems · <b>A</b>void sustained tasks · <b>M</b>isses details · <b>S</b>ustain attention trouble · <b>D</b>isorganized · <b>O</b>ften loses things · <b>F</b>orgetful/distracted
        </div>
        <div class="tbl-wrap" style="margin-top:1rem">
          <table>
            <tr><th>ADHD vs</th><th>Key Difference</th></tr>
            <tr><td>ASD</td><td>ASD: social communication deficits + restricted behaviors; ADHD: primarily attention/impulse; can be COMORBID</td></tr>
            <tr><td>ODD</td><td>ODD: defiant behavior toward authority, not attention deficit</td></tr>
            <tr><td>Anxiety</td><td>Anxiety: worries cause inattention; ADHD: inattention is primary; ADHD doesn't worry as much</td></tr>
            <tr><td>Intellectual Disability</td><td>ID: global cognitive impairment; ADHD: normal IQ but attention dysregulation</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>First-line:</b> Stimulants (methylphenidate, amphetamines) + Behavioral Therapy<br>
          <b>Non-stimulant:</b> Atomoxetine (Strattera), Guanfacine, Clonidine<br>
          <b>Psychotherapy:</b> Behavioral management, Parent training, CBT (older children/adults)
        </div>
      </div>

      <!-- ASD -->
      <div class="card">
        <div class="card-title">Autism Spectrum Disorder (ASD) <span class="badge badge-red">Must Know</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">3/3</div><div class="criteria-lbl">Social-Comm Criteria</div></div>
          <div class="criteria-box"><div class="criteria-val">2/4</div><div class="criteria-lbl">Restricted Behavior</div></div>
          <div class="criteria-box"><div class="criteria-val">Early</div><div class="criteria-lbl">Onset (early dev period)</div></div>
        </div>
        <div class="two-col">
          <div>
            <strong>Criterion A — Social Communication (ALL 3):</strong>
            <ul style="margin-top:0.5rem">
              <li>Deficits in social-emotional reciprocity</li>
              <li>Deficits in nonverbal communicative behaviors</li>
              <li>Deficits in developing/maintaining relationships</li>
            </ul>
          </div>
          <div>
            <strong>Criterion B — Restricted/Repetitive (≥2 of 4 — "SIRS"):</strong>
            <ul style="margin-top:0.5rem">
              <li><b>S</b>tereotyped/repetitive motor movements or speech</li>
              <li><b>I</b>nsistence on sameness / routines</li>
              <li><b>R</b>estricted, fixated interests</li>
              <li><b>S</b>ensory hyper/hyposensitivity</li>
            </ul>
          </div>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Mnemonic — Restricted Behaviors: "SIRS"</div>
          <b>S</b>tereotyped movements · <b>I</b>nsistence on sameness · <b>R</b>estricted interests · <b>S</b>ensory issues
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Specifier</th><th>Description</th></tr>
            <tr><td>With/without intellectual impairment</td><td>Comorbid ID</td></tr>
            <tr><td>With/without language impairment</td><td>Functional speech level</td></tr>
            <tr><td>Level 1</td><td>Requiring support</td></tr>
            <tr><td>Level 2</td><td>Requiring substantial support</td></tr>
            <tr><td>Level 3</td><td>Requiring very substantial support</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Board Pearls</div>
          • DSM-5 merged Asperger's, Autistic Disorder, PDD-NOS → single <b>ASD spectrum</b><br>
          • Asperger's = ASD <b>without</b> language/intellectual impairment (no longer a separate diagnosis)<br>
          • <b>ABA</b> = Gold standard treatment for ASD<br>
          • ASD vs Intellectual Disability: ASD has specific social-communication deficits + restricted behaviors; ID has global cognitive deficits
        </div>
      </div>

      <!-- Intellectual Disability -->
      <div class="card">
        <div class="card-title">Intellectual Disability (Intellectual Developmental Disorder) <span class="badge badge-green">Core</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≤70</div><div class="criteria-lbl">IQ (approx)</div></div>
          <div class="criteria-box"><div class="criteria-val"><18</div><div class="criteria-lbl">Age of onset</div></div>
          <div class="criteria-box"><div class="criteria-val">3</div><div class="criteria-lbl">Domains: Conceptual, Social, Practical</div></div>
        </div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Severity</th><th>IQ Range</th><th>Adaptive Function</th><th>Board Clue</th></tr>
            <tr><td>Mild</td><td><b>50–70</b></td><td>Academic 6th grade max; can live independently</td><td>Most common (~85%)</td></tr>
            <tr><td>Moderate</td><td><b>35–49</b></td><td>2nd grade academic; needs support for daily living</td><td>Can do simple work</td></tr>
            <tr><td>Severe</td><td><b>20–34</b></td><td>Limited communication; needs supervision</td><td>May communicate in phrases</td></tr>
            <tr><td>Profound</td><td><b><20</b></td><td>Minimal self-care; needs total care</td><td>Rare (~1-2%); often neurological cause</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Board Pearl</div>
          ID is diagnosed by <b>adaptive functioning</b>, not IQ alone. IQ testing has standard error of measurement (~5 pts). <b>Global Developmental Delay</b> = same concept but used for children <b>under 5</b> when formal IQ testing not reliable.
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Exam Trap</div>
          <b>ID ≠ just low IQ.</b> Must have BOTH: low IQ <em>AND</em> deficits in adaptive functioning in ≥2 domains (conceptual, social, practical). Onset must be in developmental period (before age 18).
        </div>
      </div>

      <!-- Specific Learning Disorder -->
      <div class="card">
        <div class="card-title">Specific Learning Disorder (SLD) <span class="badge badge-green">Core</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Type</th><th>Old Name</th><th>Core Feature</th></tr>
            <tr><td>With impairment in reading</td><td>Dyslexia</td><td>Word reading accuracy, fluency, comprehension</td></tr>
            <tr><td>With impairment in written expression</td><td>Dysgraphia</td><td>Spelling accuracy, grammar, organization</td></tr>
            <tr><td>With impairment in mathematics</td><td>Dyscalculia</td><td>Number sense, math facts, calculation</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Board Pearl</div>
          SLD: Academic skills <b>substantially below</b> chronological age, normal IQ. Must persist despite <b>≥6 months</b> targeted intervention. Onset in school-age years. NOT due to ID, sensory deficits, or inadequate instruction.
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ SLD vs ID Trap</div>
          SLD: <b>Normal IQ</b>, deficit in specific academic area. ID: <b>Low IQ + adaptive deficits</b>, global impairment across all areas.
        </div>
      </div>

      <!-- Tic Disorders -->
      <div class="card">
        <div class="card-title">Tic Disorders — Comparison <span class="badge badge-purple">Compare</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Tic Type</th><th>Duration</th><th>Onset</th><th>Board Clue</th></tr>
            <tr><td>Tourette's Disorder</td><td><b>Multiple motor + ≥1 vocal</b></td><td><b>>1 year</b></td><td><b><18</b></td><td>Coprolalia (involuntary profanity) — rare but tested</td></tr>
            <tr><td>Persistent Motor or Vocal</td><td>Motor OR vocal (not both)</td><td>>1 year</td><td><18</td><td>Only one type</td></tr>
            <tr><td>Provisional Tic Disorder</td><td>Motor and/or vocal</td><td><b><1 year</b></td><td><18</td><td>Short duration</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Tourette's Memory Hook</div>
          <b>"Tour de France"</b> = Tourette's = <b>T</b>wo types of tics (Motor + Vocal) for <b>T</b>welve months minimum before <b>T</b>eenage years end.
        </div>
      </div>

      <!-- Neurodevelopmental Summary -->
      <div class="card">
        <div class="card-title">⚡ Neurodevelopmental Quick Differentials <span class="badge badge-red">Exam Traps</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Pair</th><th>Key Distinguisher</th><th>Board Clue</th></tr>
            <tr><td>ASD vs ADHD</td><td>ASD: social deficits + restricted behaviors; ADHD: attention/impulse</td><td>They CAN be comorbid; look for which is primary</td></tr>
            <tr><td>ASD vs ID</td><td>ASD: specific social-comm deficit; ID: global cognitive + adaptive impairment</td><td>ASD IQ can be normal; ID IQ always ≤70</td></tr>
            <tr><td>ADHD vs ODD</td><td>ADHD: can't control attention; ODD: won't follow rules (defiant)</td><td>ODD = angry/defiant; ADHD = distracted/impulsive</td></tr>
            <tr><td>SLD vs ID</td><td>SLD: normal IQ, specific domain; ID: low IQ + global adaptive deficits</td><td>IQ test is the differentiator</td></tr>
            <tr><td>ID vs GDD</td><td>GDD: under age 5, can't formally test; ID: ≥5 years, formally diagnosed</td><td>Age of assessment is the clue</td></tr>
            <tr><td>Tourette's vs Persistent</td><td>Tourette's needs BOTH motor AND vocal tics; Persistent = only one type</td><td>Count the tic types</td></tr>
          </table>
        </div>
      </div>
    </div>

    <!-- ===== PSYCHOTIC ===== -->
    <div class="view" id="view-psychotic">
      <div class="section-header">
        <div class="section-tag">Category 2</div>
        <div class="section-title">Schizophrenia Spectrum & Psychotic Disorders</div>
        <div class="section-subtitle">Duration is the master key — memorize the timeline</div>
      </div>

      <div class="card">
        <div class="card-title">🕐 Duration Comparison — The Psychotic Spectrum <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Duration</th><th>Key Feature</th><th>Mnemonic</th></tr>
            <tr><td>Brief Psychotic Disorder</td><td><b>1 day – 1 month</b></td><td>Sudden onset; full remission; often stress-triggered</td><td><b>B</b>rief = <b>B</b>ump (short bump)</td></tr>
            <tr><td>Schizophreniform Disorder</td><td><b>1 – 6 months</b></td><td>Like schizophrenia but shorter; may or may not have impaired functioning</td><td><b>Form</b>ing = in between</td></tr>
            <tr><td>Schizophrenia</td><td><b>≥6 months</b></td><td>≥1 month active phase; significant functional decline</td><td><b>S</b>chizophrenia = <b>S</b>tays long</td></tr>
            <tr><td>Schizoaffective Disorder</td><td>≥6 months total; ≥2 weeks psychosis WITHOUT mood episode</td><td>Psychosis + major mood episode; ≥2 weeks psychosis alone</td><td><b>Schizo</b> + <b>Affective</b> = both</td></tr>
            <tr><td>Delusional Disorder</td><td><b>≥1 month</b></td><td>Only non-bizarre delusions; NO hallucinations/disorganized behavior</td><td>"Just believes it" = only delusions</td></tr>
          </table>
        </div>
      </div>

      <!-- Schizophrenia -->
      <div class="card">
        <div class="card-title">Schizophrenia — Core Criteria <span class="badge badge-red">Must Know</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≥2</div><div class="criteria-lbl">Criterion A symptoms</div></div>
          <div class="criteria-box"><div class="criteria-val">1 mo</div><div class="criteria-lbl">Active phase minimum</div></div>
          <div class="criteria-box"><div class="criteria-val">6 mo</div><div class="criteria-lbl">Total duration</div></div>
        </div>
        <div class="two-col">
          <div>
            <strong>Criterion A — ≥2 (must include ≥1 from first 3):</strong>
            <ul style="margin-top:0.5rem">
              <li><b>1. Delusions</b> (most common positive symptom)</li>
              <li><b>2. Hallucinations</b> (auditory most common)</li>
              <li><b>3. Disorganized speech</b></li>
              <li>4. Grossly disorganized/catatonic behavior</li>
              <li>5. Negative symptoms</li>
            </ul>
          </div>
          <div>
            <strong>Positive vs Negative Symptoms:</strong>
            <ul style="margin-top:0.5rem">
              <li><b>Positive</b> (add): Delusions, Hallucinations, Disorganized speech/behavior</li>
              <li><b>Negative</b> (remove — "5 A's"):</li>
              <li style="margin-left:1rem"><b>A</b>ffect flat</li>
              <li style="margin-left:1rem"><b>A</b>logia (poverty of speech)</li>
              <li style="margin-left:1rem"><b>A</b>volition (lack of motivation)</li>
              <li style="margin-left:1rem"><b>A</b>nhedonia</li>
              <li style="margin-left:1rem"><b>A</b>ssocial behavior</li>
            </ul>
          </div>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Negative Symptoms: "5 A's"</div>
          <b>A</b>ffect flat · <b>A</b>logia · <b>A</b>volition · <b>A</b>nhedonia · <b>A</b>ssocial
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Type of Delusion</th><th>Description</th><th>Freq. Tested</th></tr>
            <tr><td>Persecutory</td><td>Belief of being harmed/conspired against</td><td>Most common overall</td></tr>
            <tr><td>Grandiose</td><td>Exaggerated belief in own power/importance</td><td>Common in mania too</td></tr>
            <tr><td>Referential</td><td>Neutral events have personal meaning</td><td>High yield</td></tr>
            <tr><td>Somatic</td><td>Body is diseased/malfunctioning</td><td>Differentiate from Illness Anxiety</td></tr>
            <tr><td>Erotomanic</td><td>Someone (usually famous) is in love with you</td><td>Delusional Disorder type</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>First-line:</b> Atypical antipsychotics (olanzapine, risperidone, quetiapine, clozapine for treatment-resistant)<br>
          <b>Psychosocial:</b> Social skills training, supported employment, family psychoeducation, CBT for psychosis<br>
          <b>Clozapine:</b> Only for treatment-resistant; requires WBC monitoring (risk of agranulocytosis)
        </div>
      </div>

      <!-- Schizophrenia Differentials -->
      <div class="card">
        <div class="card-title">Psychotic Disorders — Key Differentials <span class="badge badge-orange">Differentials</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Compare</th><th>Schizophrenia</th><th>Schizoaffective</th><th>Mood Disorder + Psychosis</th></tr>
            <tr><td>Psychosis without mood episode</td><td>Yes, always</td><td><b>Yes, ≥2 weeks</b></td><td>No — psychosis only WITH mood</td></tr>
            <tr><td>Mood episode</td><td>Can occur, not required</td><td>Required (major mood)</td><td>Required</td></tr>
            <tr><td>Board Clue</td><td>Psychosis is the main story</td><td>Both stories; psychosis outlasts mood</td><td>Mood is the main story</td></tr>
          </table>
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Compare</th><th>Schizophrenia</th><th>Delusional Disorder</th></tr>
            <tr><td>Hallucinations</td><td>Common</td><td>Absent (or minimal/non-prominent)</td></tr>
            <tr><td>Delusion type</td><td>Can be bizarre</td><td><b>Non-bizarre only</b> (plausible situations)</td></tr>
            <tr><td>Functioning</td><td>Markedly impaired</td><td>Relatively preserved</td></tr>
            <tr><td>Board Clue</td><td>"Hearing voices telling me to hurt someone"</td><td>"Convinced my neighbor is poisoning my food"</td></tr>
          </table>
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Classic Exam Trap</div>
          <b>Schizophrenia vs Schizophreniform:</b> Schizophreniform has SAME symptoms but duration <b>1–6 months</b>. If the patient recovers completely in 4 months → Schizophreniform. If still symptomatic at 7 months → Schizophrenia. The <b>only difference is duration</b>.
        </div>
      </div>
    </div>

    <!-- ===== BIPOLAR ===== -->
    <div class="view" id="view-bipolar">
      <div class="section-header">
        <div class="section-tag">Category 3</div>
        <div class="section-title">Bipolar & Related Disorders</div>
        <div class="section-subtitle">Master the mania vs hypomania distinction — it's the entire exam</div>
      </div>

      <div class="card">
        <div class="card-title">Mania vs Hypomania vs Cyclothymia <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Feature</th><th>Mania (Bipolar I)</th><th>Hypomania (Bipolar II)</th><th>Cyclothymia</th></tr>
            <tr><td>Duration</td><td><b>≥7 days</b> (any if hospitalized)</td><td><b>≥4 days</b></td><td><b>≥2 years</b></td></tr>
            <tr><td>Severity</td><td>Severe; hospitalizable</td><td>Not severe enough for hospitalization</td><td>Sub-threshold (never full episodes)</td></tr>
            <tr><td>Hospitalization</td><td>May require</td><td>Does NOT require</td><td>N/A</td></tr>
            <tr><td>Psychosis</td><td>May have psychotic features</td><td>NO psychotic features</td><td>No</td></tr>
            <tr><td>Functioning</td><td>Marked impairment</td><td>No marked impairment</td><td>Chronic fluctuation</td></tr>
            <tr><td>Observable change</td><td>Yes, definite change noted by others</td><td>Yes, observable</td><td>Numerous periods</td></tr>
          </table>
        </div>
      </div>

      <div class="card">
        <div class="card-title">Manic Episode Criteria — "DIG FAST" <span class="badge badge-orange">Mnemonic</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≥3</div><div class="criteria-lbl">Symptoms needed (4 if irritable mood)</div></div>
          <div class="criteria-box"><div class="criteria-val">7</div><div class="criteria-lbl">Days minimum</div></div>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Mnemonic: "DIG FAST"</div>
          <b>D</b>istractibility · <b>I</b>mpulsivity (reckless behavior) · <b>G</b>randiosity · <b>F</b>light of ideas · <b>A</b>ctivity increase (goal-directed) · <b>S</b>leep decreased (no need) · <b>T</b>alkative (pressured speech)
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Disorder</th><th>Required Episodes</th><th>Board Clue</th></tr>
            <tr><td>Bipolar I</td><td>≥1 <b>Manic</b> episode (depressive not required)</td><td>One manic episode = Bipolar I, period.</td></tr>
            <tr><td>Bipolar II</td><td>≥1 <b>Hypomanic</b> + ≥1 <b>Major Depressive</b></td><td>NEVER has a full manic episode</td></tr>
            <tr><td>Cyclothymia</td><td>≥2 years of hypo symptoms + depressive symptoms (never full episodes)</td><td>Sub-threshold, chronic, no full episodes</td></tr>
          </table>
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Exam Trap — Bipolar I vs II</div>
          If a Bipolar II patient EVER has a full manic episode → <b>diagnosis changes to Bipolar I</b>. Bipolar II is not "less severe" Bipolar I — it's a <em>separate diagnosis requiring</em> both hypomania AND depression.
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment Pearls</div>
          <b>Bipolar I (acute mania):</b> Lithium, Valproate, Atypical antipsychotics (olanzapine, quetiapine)<br>
          <b>Bipolar II:</b> Lithium, Lamotrigine (especially for depression phase)<br>
          <b>Cyclothymia:</b> Mood stabilizers; psychoeducation<br>
          <b>⚠️ Antidepressants alone can trigger mania in Bipolar patients — always use with mood stabilizer</b>
        </div>
      </div>
    </div>

    <!-- ===== DEPRESSIVE ===== -->
    <div class="view" id="view-depressive">
      <div class="section-header">
        <div class="section-tag">Category 4</div>
        <div class="section-title">Depressive Disorders</div>
        <div class="section-subtitle">MDD, PDD (Dysthymia), PMDD, DMDD — master duration differences</div>
      </div>

      <div class="card">
        <div class="card-title">Major Depressive Disorder (MDD) <span class="badge badge-red">Must Know</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≥5</div><div class="criteria-lbl">Symptoms required</div></div>
          <div class="criteria-box"><div class="criteria-val">2 wk</div><div class="criteria-lbl">Duration minimum</div></div>
          <div class="criteria-box"><div class="criteria-val">1 of 2</div><div class="criteria-lbl">Must include: depressed mood OR anhedonia</div></div>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 MDD Symptoms: "SIG E CAPS"</div>
          <b>S</b>leep disturbance · <b>I</b>nterest loss (anhedonia) · <b>G</b>uilt (worthlessness) · <b>E</b>nergy loss · <b>C</b>oncentration problems · <b>A</b>ppetite/weight change · <b>P</b>sychomotor changes · <b>S</b>uicidal ideation
          <br><em>+ Depressed mood = 9 total symptoms; need ≥5 including depressed mood or anhedonia</em>
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>MDD Specifier</th><th>What it means</th></tr>
            <tr><td>With anxious distress</td><td>Prominent anxiety symptoms</td></tr>
            <tr><td>With melancholic features</td><td>Anhedonia + early morning awakening + psychomotor changes + guilt</td></tr>
            <tr><td>With psychotic features</td><td>Mood-congruent or incongruent delusions/hallucinations</td></tr>
            <tr><td>With atypical features</td><td>Mood reactivity + ≥2: hypersomnia, hyperphagia, leaden paralysis, rejection sensitivity</td></tr>
            <tr><td>With peripartum onset</td><td>During pregnancy or within 4 weeks postpartum</td></tr>
            <tr><td>With seasonal pattern</td><td>Episodes tied to season (winter depression)</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>Mild-Moderate:</b> Psychotherapy alone (CBT, IPT) or SSRIs<br>
          <b>Moderate-Severe:</b> SSRIs + CBT or IPT; first-line SSRIs = fluoxetine, sertraline, escitalopram<br>
          <b>Psychotic depression:</b> Antidepressant + antipsychotic<br>
          <b>Treatment-resistant:</b> ECT (electroconvulsive therapy) — most effective for severe MDD
        </div>
      </div>

      <div class="card">
        <div class="card-title">Depressive Disorders — Duration Comparison <span class="badge badge-orange">Differentials</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Duration</th><th>Key Feature</th><th>Board Clue</th></tr>
            <tr><td>MDD</td><td><b>≥2 weeks</b></td><td>≥5 symptoms including depressed mood or anhedonia</td><td>Episodic; can have remission</td></tr>
            <tr><td>Persistent Depressive Disorder (Dysthymia)</td><td><b>≥2 years</b> adults / <b>≥1 year</b> children</td><td>Depressed mood + ≥2 symptoms; chronic, low-grade</td><td>"I've always been this way"</td></tr>
            <tr><td>PMDD</td><td>Last week of luteal phase, remit ~7 days after menses</td><td>Mood lability + depressive symptoms tied to cycle</td><td>Confirmed over 2 cycles</td></tr>
            <tr><td>DMDD</td><td>Temper outbursts ≥3x/week for ≥1 year</td><td>Onset <10, severe irritability in children</td><td>Replaces "pediatric bipolar" diagnosis</td></tr>
            <tr><td>Adjustment Disorder with Depressed Mood</td><td><3 months after stressor</td><td>Below threshold for MDD; clear stressor</td><td>Reaction to stressor, not full MDD</td></tr>
          </table>
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ PDD vs MDD Trap (Double Depression)</div>
          "Double Depression" = MDD episode superimposed on PDD. After MDD episode resolves, patient returns to dysthymic baseline. PDD is <b>chronic</b>; MDD is <b>episodic</b>. PDD requires <b>depressed mood most of the day, more days than not</b>.
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Bereavement vs MDD</div>
          DSM-5-TR REMOVED the bereavement exclusion. Grief can be diagnosed as MDD if full criteria are met. Key: <b>grief features</b> (waves of sadness, thoughts of deceased) vs <b>MDD features</b> (persistent, pervasive hopelessness, SI, functional impairment).
        </div>
      </div>
    </div>

    <!-- ===== ANXIETY ===== -->
    <div class="view" id="view-anxiety">
      <div class="section-header">
        <div class="section-tag">Category 5</div>
        <div class="section-title">Anxiety Disorders</div>
        <div class="section-subtitle">GAD, Panic Disorder, Social Anxiety, Specific Phobia, Agoraphobia, Separation Anxiety</div>
      </div>

      <div class="card">
        <div class="card-title">Anxiety Disorders — Duration & Symptom Comparison <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Fear</th><th>Duration</th><th>Symptom #</th><th>Board Clue</th></tr>
            <tr><td>GAD</td><td>Uncontrollable worry about multiple areas</td><td><b>≥6 months</b></td><td>≥3 symptoms (adults); ≥1 (children)</td><td>Chronic, pervasive, hard to control worry</td></tr>
            <tr><td>Panic Disorder</td><td>Unexpected panic attacks + anticipatory anxiety</td><td>≥1 month concern/change</td><td>≥4 panic symptoms per attack</td><td>Unexpected attacks + "fear of fear"</td></tr>
            <tr><td>Social Anxiety Disorder</td><td>Fear of negative evaluation in social situations</td><td><b>≥6 months</b></td><td>N/A</td><td>Fear of embarrassment, judgment</td></tr>
            <tr><td>Specific Phobia</td><td>Specific object or situation</td><td><b>≥6 months</b></td><td>N/A</td><td>Animal, natural environment, blood, situational</td></tr>
            <tr><td>Agoraphobia</td><td>≥2 of 5 situations (crowds, open/enclosed, transport, outside alone)</td><td><b>≥6 months</b></td><td>≥2 of 5 situations</td><td>Fear of escape difficulty; can be without panic</td></tr>
            <tr><td>Separation Anxiety</td><td>Fear of separation from attachment figures</td><td>≥4 weeks (children); <b>≥6 months</b> (adults)</td><td>≥3 symptoms</td><td>NOT limited to children in DSM-5</td></tr>
          </table>
        </div>
      </div>

      <div class="card">
        <div class="card-title">Panic Attack — Criteria <span class="badge badge-orange">High Yield</span></div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">≥4</div><div class="criteria-lbl">Symptoms required</div></div>
          <div class="criteria-box"><div class="criteria-val">Peak</div><div class="criteria-lbl">within 10 minutes</div></div>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Panic Attack Symptoms: "3 Chests DUMB"</div>
          <b>C</b>hest pain · <b>C</b>hills/hot flashes · <b>C</b>hoking sensation · <b>D</b>erealization/depersonalization · <b>U</b>nsteady/dizzy/faint · <b>M</b>outh dry (nausea) · <b>B</b>odygoing numb/tingling
          <br><em>Plus: palpitations, sweating, trembling, shortness of breath, fear of dying, fear of losing control</em>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Panic Attack vs Panic Disorder</div>
          <b>Panic Attack</b> = a symptom, not a diagnosis. Can occur in any disorder.<br>
          <b>Panic Disorder</b> = recurrent <em>unexpected</em> panic attacks + ≥1 month of persistent concern OR behavioral change.<br>
          Key: attacks must be <b>unexpected</b> for Panic Disorder.
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>GAD:</b> CBT + SSRIs/SNRIs; Buspirone (non-addictive anxiolytic)<br>
          <b>Panic Disorder:</b> CBT (interoceptive exposure) + SSRIs; Benzodiazepines SHORT-TERM only<br>
          <b>Social Anxiety:</b> CBT + SSRIs; Group therapy; beta-blockers (performance anxiety)<br>
          <b>Specific Phobia:</b> <b>Exposure therapy</b> = gold standard; no meds generally needed
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Anxiety Differential</th><th>Key Distinguisher</th><th>Board Clue</th></tr>
            <tr><td>GAD vs OCD</td><td>GAD: worries about real life events; OCD: obsessions are ego-dystonic, intrusive, irrational</td><td>OCD patient knows thoughts are abnormal</td></tr>
            <tr><td>GAD vs Panic Disorder</td><td>GAD: chronic, sustained worry; PD: episodic intense panic attacks</td><td>GAD is a "slow burn"; PD is "sudden explosion"</td></tr>
            <tr><td>Social Anxiety vs AVPD</td><td>Social Anxiety: limited to social situations; Avoidant PD: pervasive pattern of avoidance + inadequacy</td><td>If it's pervasive, lifelong, affects ALL relationships → PD</td></tr>
            <tr><td>Agoraphobia vs Specific Phobia</td><td>Agoraphobia: ≥2 situations + fear of escape; SP: one specific trigger</td><td>Count the situations feared</td></tr>
          </table>
        </div>
      </div>
    </div>

    <!-- ===== OCD ===== -->
    <div class="view" id="view-ocd">
      <div class="section-header">
        <div class="section-tag">Category 6</div>
        <div class="section-title">Obsessive-Compulsive & Related Disorders</div>
        <div class="section-subtitle">OCD, BDD, Hoarding, Trichotillomania, Excoriation</div>
      </div>

      <div class="card">
        <div class="card-title">OCD — Diagnostic Criteria <span class="badge badge-red">Most Tested</span></div>
        <div class="two-col">
          <div>
            <strong>Obsessions (must have A & B):</strong>
            <ul style="margin-top:0.5rem">
              <li>Recurrent, persistent, intrusive thoughts/urges/images</li>
              <li>Person attempts to suppress or neutralize them</li>
            </ul>
            <strong style="display:block;margin-top:0.75rem">Compulsions (must have A & B):</strong>
            <ul style="margin-top:0.5rem">
              <li>Repetitive behaviors or mental acts driven by obsessions or rigid rules</li>
              <li>Aimed at preventing/reducing distress (not realistically connected)</li>
            </ul>
          </div>
          <div>
            <strong>Key Specifiers:</strong>
            <ul style="margin-top:0.5rem">
              <li><b>Good or fair insight:</b> Knows beliefs are probably/definitely not true</li>
              <li><b>Poor insight:</b> Thinks beliefs are probably true</li>
              <li><b>Absent insight/delusional beliefs:</b> Completely convinced</li>
              <li><b>Tic-related:</b> Current or past tic disorder</li>
            </ul>
            <strong style="display:block;margin-top:0.75rem">Time criterion:</strong>
            <ul><li>Obsessions/compulsions are time-consuming (<b>>1 hour/day</b>) OR cause significant distress</li></ul>
          </div>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Gold Standard Treatment</div>
          <b>ERP (Exposure and Response Prevention)</b> = #1 treatment for OCD<br>
          Medications: SSRIs (higher doses than for depression); Clomipramine (TCA — effective but more side effects)<br>
          <b>Combined ERP + SSRI</b> = most effective
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>OCD vs</th><th>Key Difference</th><th>Board Clue</th></tr>
            <tr><td>GAD</td><td>OCD: obsessions are ego-dystonic, unrealistic; GAD: worries are about real-life problems</td><td>"I know it's irrational but I can't stop" = OCD</td></tr>
            <tr><td>OCPD</td><td>OCD: ego-dystonic obsessions + compulsions; OCPD: ego-syntonic perfectionism, NO obsessions/compulsions</td><td>OCPD patient doesn't see a problem; OCD patient is distressed</td></tr>
            <tr><td>BDD</td><td>OCD-related; obsessions about physical appearance; checking/camouflaging behaviors</td><td>BDD is in the OCD family but specifically about looks</td></tr>
            <tr><td>Hoarding</td><td>Difficulty discarding; NOT fear of contamination or harm; persistent difficulty parting with possessions</td><td>Hoarding is its own disorder (NOT just OCD with hoarding)</td></tr>
          </table>
        </div>
      </div>

      <div class="card">
        <div class="card-title">OCD-Related Disorders — Quick Compare <span class="badge badge-purple">Compare</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Behavior</th><th>Gold Standard Tx</th><th>Board Clue</th></tr>
            <tr><td>OCD</td><td>Obsessions + compulsions</td><td>ERP + SSRI</td><td>Ego-dystonic; >1 hr/day</td></tr>
            <tr><td>Body Dysmorphic Disorder</td><td>Preoccupation with perceived appearance flaw</td><td>ERP + SSRI</td><td>Insight specifier; not eating disorder</td></tr>
            <tr><td>Hoarding Disorder</td><td>Difficulty discarding; cluttered living spaces</td><td>CBT (adapted for hoarding)</td><td>Emotional attachment to possessions</td></tr>
            <tr><td>Trichotillomania</td><td>Recurrent hair pulling causing hair loss</td><td>HRT (Habit Reversal Training)</td><td>Hair pulling = TTM</td></tr>
            <tr><td>Excoriation Disorder</td><td>Recurrent skin picking causing lesions</td><td>HRT</td><td>Skin picking = excoriation</td></tr>
          </table>
        </div>
      </div>
    </div>

    <!-- ===== TRAUMA ===== -->
    <div class="view" id="view-trauma">
      <div class="section-header">
        <div class="section-tag">Category 7</div>
        <div class="section-title">Trauma- and Stressor-Related Disorders</div>
        <div class="section-subtitle">PTSD, Acute Stress Disorder, Adjustment Disorder — duration is everything</div>
      </div>

      <div class="card">
        <div class="card-title">Trauma Disorders — Duration Timeline <span class="badge badge-red">Must Know</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Duration After Trauma</th><th>Key Feature</th></tr>
            <tr><td>Acute Stress Disorder</td><td><b>3 days – 1 month</b></td><td>Dissociative symptoms prominent; immediate post-trauma</td></tr>
            <tr><td>PTSD</td><td><b>>1 month</b></td><td>4 symptom clusters; functional impairment</td></tr>
            <tr><td>Adjustment Disorder</td><td><b>Within 3 months</b> of stressor; resolves <b>within 6 months</b></td><td>Below PTSD threshold; reaction to any stressor (not just trauma)</td></tr>
          </table>
        </div>
      </div>

      <div class="card">
        <div class="card-title">PTSD — 4 Symptom Clusters <span class="badge badge-red">Must Know</span></div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 PTSD Clusters: "RAIN"</div>
          <b>R</b>e-experiencing · <b>A</b>voidance · <b>I</b>mpact on cognition/mood (negative) · <b>N</b>egative alterations in arousal/reactivity
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Cluster</th><th>Symptoms</th><th>Required</th></tr>
            <tr><td>B — Re-experiencing</td><td>Flashbacks, nightmares, intrusive memories, distress at cues</td><td><b>≥1</b></td></tr>
            <tr><td>C — Avoidance</td><td>Avoid trauma-related thoughts, places, people, activities</td><td><b>≥1</b></td></tr>
            <tr><td>D — Negative Cognition/Mood</td><td>Distorted blame, negative beliefs, diminished interest, feeling detached, persistent negative emotions</td><td><b>≥2</b></td></tr>
            <tr><td>E — Arousal/Reactivity</td><td>Hypervigilance, startle, irritability, reckless behavior, sleep problems, concentration</td><td><b>≥2</b></td></tr>
          </table>
        </div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">>1</div><div class="criteria-lbl">Month duration</div></div>
          <div class="criteria-box"><div class="criteria-val">≥18</div><div class="criteria-lbl">Adult criteria (separate <6 yrs)</div></div>
          <div class="criteria-box"><div class="criteria-val">B+C+D+E</div><div class="criteria-lbl">All 4 clusters required</div></div>
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>Gold Standard:</b> Trauma-Focused CBT (TF-CBT)<br>
          Also effective: EMDR (Eye Movement Desensitization and Reprocessing), Prolonged Exposure (PE), CPT<br>
          <b>Medications:</b> SSRIs (sertraline, paroxetine — FDA approved); Prazosin for nightmares
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ ASD vs PTSD Trap</div>
          ASD lasts <b>3 days to 1 month</b>; PTSD lasts <b>>1 month</b>. ASD has prominent <b>dissociative symptoms</b> not required in PTSD. ASD predicts PTSD in 50% of cases. Also: <b>ASD</b> in trauma = Acute Stress Disorder (NOT Autism Spectrum Disorder — know context!).
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ PTSD vs Adjustment Disorder</div>
          Adjustment Disorder: stressor doesn't have to be life-threatening; symptoms below PTSD threshold; resolves within 6 months. PTSD: traumatic stressor specifically, full cluster criteria, no time limit for resolution.
        </div>
      </div>
    </div>

    <!-- ===== DISSOCIATIVE ===== -->
    <div class="view" id="view-dissociative">
      <div class="section-header">
        <div class="section-tag">Category 8</div>
        <div class="section-title">Dissociative Disorders</div>
        <div class="section-subtitle">DID, Dissociative Amnesia, Depersonalization/Derealization</div>
      </div>

      <div class="card">
        <div class="card-title">Dissociative Disorders — Quick Comparison <span class="badge badge-orange">High Yield</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Feature</th><th>Board Clue</th></tr>
            <tr><td>Dissociative Identity Disorder (DID)</td><td>≥2 distinct personality states (alters); amnesia between states</td><td>Formerly MPD (Multiple Personality Disorder)</td></tr>
            <tr><td>Dissociative Amnesia</td><td>Inability to recall autobiographical info (usually trauma-related)</td><td>Can include dissociative fugue (purposeful travel, new identity)</td></tr>
            <tr><td>Depersonalization/Derealization Disorder</td><td>Detachment from self (depersonalization) or surroundings (derealization)</td><td>Reality testing INTACT (knows it's not real)</td></tr>
          </table>
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ DID vs Schizophrenia</div>
          <b>DID:</b> Multiple identities, amnesia between states, no true hallucinations (voices are the alters)<br>
          <b>Schizophrenia:</b> One identity with disorganized thinking, true hallucinations, delusions<br>
          Board clue: DID patient hears "voices" that are distinct personalities, not external voices commenting
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Depersonalization vs Panic Disorder</div>
          Depersonalization/derealization can OCCUR in panic attacks but is transient. Depersonalization Disorder = <b>persistent</b>, not episodic; reality testing INTACT (they know they're not actually detached).
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Dissociative Amnesia vs NCD</div>
          Dissociative Amnesia: usually after psychological trauma, retrograde, no neurological cause<br>
          Neurocognitive Disorder: progressive, new learning impaired, neurological cause
        </div>
      </div>
    </div>

    <!-- ===== SOMATIC ===== -->
    <div class="view" id="view-somatic">
      <div class="section-header">
        <div class="section-tag">Category 9</div>
        <div class="section-title">Somatic Symptom & Related Disorders</div>
        <div class="section-subtitle">SSD, Illness Anxiety, Conversion, Factitious, Malingering</div>
      </div>

      <div class="card">
        <div class="card-title">Somatic Disorders — Critical Distinctions <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Symptoms Real?</th><th>Intentional?</th><th>External Gain?</th><th>Board Clue</th></tr>
            <tr><td>Somatic Symptom Disorder</td><td>Yes (may/may not have medical cause)</td><td>No</td><td>No</td><td>Excessive thoughts/feelings/behaviors about symptoms</td></tr>
            <tr><td>Illness Anxiety Disorder</td><td>Minimal or none</td><td>No</td><td>No</td><td>Fear of HAVING a disease, not actual symptoms</td></tr>
            <tr><td>Conversion Disorder (FND)</td><td>Neurological symptoms (no medical cause)</td><td>No</td><td>No</td><td>Incompatibility with known neurological disease</td></tr>
            <tr><td>Factitious Disorder</td><td>Falsified/induced</td><td><b>Yes</b></td><td><b>No</b> (sick role only)</td><td>Imposed on self or another (Munchausen)</td></tr>
            <tr><td>Malingering</td><td>Falsified</td><td><b>Yes</b></td><td><b>Yes</b> (money, avoid jail, etc.)</td><td>NOT a mental disorder; intentional deception</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Factitious vs Malingering</div>
          <b>Factitious</b> = Faking for <b>F</b>eel-like-a-patient (sick role, no tangible gain)<br>
          <b>Malingering</b> = <b>M</b>oney (external incentive — avoiding work, legal responsibility, getting drugs)
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Feature</th><th>SSD</th><th>Illness Anxiety Disorder</th></tr>
            <tr><td>Somatic symptoms</td><td>YES, prominent</td><td>Minimal or absent</td></tr>
            <tr><td>Preoccupation</td><td>About the symptoms</td><td>About having a disease</td></tr>
            <tr><td>Duration</td><td><b>≥6 months</b></td><td><b>≥6 months</b></td></tr>
            <tr><td>Former term</td><td>Somatization Disorder</td><td>Hypochondriasis</td></tr>
            <tr><td>Care-seeking</td><td>Excessive</td><td>Can be care-seeking OR care-avoidant</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Conversion Disorder Pearl</div>
          Formerly "Hysteria." Key feature: neurological symptoms (paralysis, blindness, seizures) that are <b>incompatible</b> with recognized neurological disease. "La belle indifférence" (lack of concern about symptoms) is sometimes seen but NOT required. <b>Treat with PT + psychotherapy</b>.
        </div>
      </div>
    </div>

    <!-- ===== EATING ===== -->
    <div class="view" id="view-eating">
      <div class="section-header">
        <div class="section-tag">Category 10</div>
        <div class="section-title">Feeding and Eating Disorders</div>
        <div class="section-subtitle">Anorexia, Bulimia, BED, ARFID, Pica</div>
      </div>

      <div class="card">
        <div class="card-title">Eating Disorders — Core Comparison <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Feature</th><th>Anorexia Nervosa (AN)</th><th>Bulimia Nervosa (BN)</th><th>Binge-Eating Disorder (BED)</th></tr>
            <tr><td>Weight</td><td><b>Significantly low</b> (BMI <17.5)</td><td>Normal or above</td><td>Often overweight/obese</td></tr>
            <tr><td>Body image disturbance</td><td>YES (intense fear of weight gain)</td><td>YES (self-worth tied to shape/weight)</td><td>Distress but not same distortion</td></tr>
            <tr><td>Binge eating</td><td>No (restriction) — except Binge/Purge type</td><td>YES (recurrent)</td><td>YES (recurrent, no purging)</td></tr>
            <tr><td>Purging/Compensatory</td><td>Only in B/P subtype</td><td>YES (key feature)</td><td>NO</td></tr>
            <tr><td>Duration criteria</td><td>N/A (persistent pattern)</td><td><b>≥1x/week for 3 months</b></td><td><b>≥1x/week for 3 months</b></td></tr>
            <tr><td>Insight</td><td>Poor (denies illness)</td><td>Ego-dystonic (knows it's wrong)</td><td>Distressed by bingeing</td></tr>
            <tr><td>Medical risks</td><td>Lanugo, amenorrhea, osteoporosis, cardiac</td><td>Dental erosion, electrolyte imbalance, parotid enlargement</td><td>Metabolic syndrome</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 AN Types</div>
          <b>R</b>estrictive type: No bingeing/purging, only restricts<br>
          <b>B</b>inge/Purge type: Does binge and purge
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>AN Severity (by BMI)</th><th>BMI</th></tr>
            <tr><td>Mild</td><td><b>≥17</b></td></tr>
            <tr><td>Moderate</td><td><b>16–16.99</b></td></tr>
            <tr><td>Severe</td><td><b>15–15.99</b></td></tr>
            <tr><td>Extreme</td><td><b><15</b></td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Russell's Sign</div>
          Calluses on knuckles from self-induced vomiting = <b>Russell's Sign</b> → associated with Bulimia Nervosa
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>AN:</b> Nutritional rehabilitation FIRST (weight restoration), then psychotherapy (FBT for adolescents, CBT for adults). No FDA-approved meds.<br>
          <b>BN:</b> CBT = gold standard + SSRIs (fluoxetine — only FDA-approved med for BN)<br>
          <b>BED:</b> CBT + SSRIs; Lisdexamfetamine (Vyvanse) — FDA approved for BED
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>ARFID vs AN</th><th>ARFID</th><th>Anorexia</th></tr>
            <tr><td>Body image concern</td><td>NO</td><td>YES (intense fear of weight gain)</td></tr>
            <tr><td>Motivation for restriction</td><td>Sensory, texture, fear of choking, or lack of interest</td><td>Fear of weight gain</td></tr>
            <tr><td>Onset</td><td>Often younger (childhood)</td><td>Often adolescence</td></tr>
          </table>
        </div>
      </div>
    </div>

    <!-- ===== PERSONALITY ===== -->
    <div class="view" id="view-personality">
      <div class="section-header">
        <div class="section-tag">Category 11</div>
        <div class="section-title">Personality Disorders</div>
        <div class="section-subtitle">Cluster A (Odd/Eccentric), B (Dramatic/Emotional), C (Anxious/Fearful)</div>
      </div>

      <div class="card">
        <div class="card-title">Cluster Overview — "ABC" <span class="badge badge-red">Most Tested</span></div>
        <div class="three-col">
          <div class="card" style="margin:0; border-color:#2a3530">
            <div style="color:var(--accent); font-family:'Syne',sans-serif; font-weight:700; margin-bottom:0.5rem">Cluster A — Odd/Eccentric</div>
            <ul>
              <li><b>Paranoid PD:</b> Distrust, suspicion</li>
              <li><b>Schizoid PD:</b> Detachment, no interest in social relationships</li>
              <li><b>Schizotypal PD:</b> Odd beliefs, magical thinking, perceptual distortions</li>
            </ul>
            <div class="mnemonic" style="margin-top:0.75rem; padding:0.6rem"><div class="mnemonic-label">Mnemonic</div><b>"Weird"</b></div>
          </div>
          <div class="card" style="margin:0; border-color:#3a1515">
            <div style="color:var(--accent4); font-family:'Syne',sans-serif; font-weight:700; margin-bottom:0.5rem">Cluster B — Dramatic/Emotional</div>
            <ul>
              <li><b>Antisocial PD:</b> Disregard for rights of others</li>
              <li><b>Borderline PD:</b> Instability in relationships, mood, identity, impulsivity</li>
              <li><b>Histrionic PD:</b> Attention-seeking, dramatic</li>
              <li><b>Narcissistic PD:</b> Grandiosity, lack of empathy</li>
            </ul>
            <div class="mnemonic" style="margin-top:0.75rem; padding:0.6rem"><div class="mnemonic-label">Mnemonic</div><b>"Wild"</b></div>
          </div>
          <div class="card" style="margin:0; border-color:#1e0a2a">
            <div style="color:var(--accent3); font-family:'Syne',sans-serif; font-weight:700; margin-bottom:0.5rem">Cluster C — Anxious/Fearful</div>
            <ul>
              <li><b>Avoidant PD:</b> Social inhibition, inadequacy, hypersensitivity</li>
              <li><b>Dependent PD:</b> Submissiveness, clinging, separation fear</li>
              <li><b>OCPD:</b> Perfectionism, control, orderliness (ego-syntonic)</li>
            </ul>
            <div class="mnemonic" style="margin-top:0.75rem; padding:0.6rem"><div class="mnemonic-label">Mnemonic</div><b>"Worried"</b></div>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-title">High-Yield PD Differentials <span class="badge badge-orange">Differentials</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Pair</th><th>Key Difference</th><th>Board Clue</th></tr>
            <tr><td>BPD vs Bipolar</td><td>BPD: mood shifts last hours; Bipolar: episodes last days-weeks; BPD has identity disturbance, FBT</td><td>BPD mood reactive to interpersonal events; Bipolar is episodic</td></tr>
            <tr><td>BPD vs Histrionic</td><td>BPD: self-destructive, identity chaos, parasuicidal; Histrionic: attention-seeking, seductive, no self-harm</td><td>Self-harm → BPD; seductive drama → Histrionic</td></tr>
            <tr><td>Antisocial vs Narcissistic</td><td>ASPD: violates laws/rules, exploits for personal gain; NPD: exploits for admiration, grandiose</td><td>Criminal behavior → ASPD; superiority complex → NPD</td></tr>
            <tr><td>Schizoid vs Avoidant</td><td>Schizoid: doesn't WANT relationships (content alone); Avoidant: WANTS relationships but fears rejection</td><td>Happy alone = Schizoid; Lonely and scared = Avoidant</td></tr>
            <tr><td>OCD vs OCPD</td><td>OCD: ego-dystonic (unwanted obsessions/compulsions); OCPD: ego-syntonic (sees perfectionism as correct)</td><td>Distressed by it → OCD; proud of it → OCPD</td></tr>
            <tr><td>Paranoid PD vs Schizotypal</td><td>Paranoid: suspicious/distrustful only; Schizotypal: odd beliefs, magical thinking, perceptual disturbances</td><td>Magical thinking + odd speech = Schizotypal</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Borderline PD — 9 Criteria (need ≥5): "I DESPAIR"</div>
          <div class="mnemonic" style="margin:0">
            <b>I</b>dentity disturbance · <b>D</b>issociation/paranoia (transient, stress-related) · <b>E</b>mptiness (chronic) · <b>S</b>uicidal/self-mutilating behavior · <b>P</b>aranoia/dissociation · <b>A</b>ffective instability · <b>I</b>mpulsivity (≥2 areas) · <b>R</b>age (inappropriate, intense) · <b>A</b>bandonment (frantic efforts to avoid)
          </div>
          <br><b>Gold Standard Treatment:</b> DBT (Dialectical Behavior Therapy)
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ ASPD Requirements</div>
          ASPD requires: Conduct Disorder before <b>age 15</b> + currently ≥ <b>age 18</b>. Cannot diagnose ASPD before 18 — use Conduct Disorder. Psychopathy ≠ ASPD (psychopathy is not in DSM).
        </div>
      </div>
    </div>

    <!-- ===== NEUROCOGNITIVE ===== -->
    <div class="view" id="view-neurocognitive">
      <div class="section-header">
        <div class="section-tag">Category 12</div>
        <div class="section-title">Neurocognitive Disorders</div>
        <div class="section-subtitle">Delirium, Major NCD (Dementia), Mild NCD — onset & course are key</div>
      </div>

      <div class="card">
        <div class="card-title">Delirium vs Major NCD (Dementia) <span class="badge badge-red">Most Tested</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Feature</th><th>Delirium</th><th>Major Neurocognitive Disorder (Dementia)</th></tr>
            <tr><td>Onset</td><td><b>Acute</b> (hours-days)</td><td><b>Gradual/insidious</b> (months-years)</td></tr>
            <tr><td>Course</td><td><b>Fluctuating</b> (worse at night)</td><td><b>Progressive</b></td></tr>
            <tr><td>Consciousness</td><td><b>Impaired</b> (clouding of consciousness)</td><td>Usually clear (early stages)</td></tr>
            <tr><td>Attention</td><td>Severely impaired</td><td>Relatively preserved early</td></tr>
            <tr><td>Reversibility</td><td>Often <b>reversible</b></td><td>Usually <b>irreversible</b></td></tr>
            <tr><td>Common cause</td><td>Medical illness, drugs, withdrawal, post-surgery</td><td>Alzheimer's, vascular, Lewy body, frontotemporal</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Delirium vs Dementia</div>
          <b>D</b>elirium = <b>D</b>ramatic onset, <b>D</b>usk worsening (sundowning), <b>D</b>rugs/medical cause<br>
          <b>D</b>ementia = <b>D</b>ownhill gradually, <b>D</b>egenerative, <b>D</b>oesn't fluctuate (early)
        </div>
      </div>

      <div class="card">
        <div class="card-title">NCD Subtypes — Distinguishing Features <span class="badge badge-orange">High Yield</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Subtype</th><th>Hallmark Feature</th><th>Board Clue</th></tr>
            <tr><td>Alzheimer's Disease</td><td>Gradual memory loss, language, executive function; amyloid plaques + tau tangles</td><td>Most common cause of dementia</td></tr>
            <tr><td>Frontotemporal NCD (Pick's)</td><td>Early personality change + language difficulty; relatively preserved memory early</td><td>"He's a different person" before memory loss</td></tr>
            <tr><td>Lewy Body NCD</td><td>Visual hallucinations + Parkinsonism + fluctuating cognition</td><td>Hallucinations + motor symptoms</td></tr>
            <tr><td>Vascular NCD</td><td>Stepwise decline; focal neurological signs; after stroke</td><td>Stepwise = vascular</td></tr>
          </table>
        </div>
        <div class="tbl-wrap" style="margin-top:0.75rem">
          <table>
            <tr><th>Feature</th><th>Major NCD</th><th>Mild NCD</th></tr>
            <tr><td>Cognitive decline</td><td>Significant decline; interferes with independence</td><td>Modest decline; does NOT interfere with independence</td></tr>
            <tr><td>ADL function</td><td>Impaired</td><td>Preserved (may need aids/strategies)</td></tr>
            <tr><td>Old term</td><td>Dementia</td><td>Mild Cognitive Impairment (MCI)</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Treatment</div>
          <b>Alzheimer's:</b> Cholinesterase inhibitors (donepezil, rivastigmine, galantamine) for mild-moderate; Memantine (NMDA antagonist) for moderate-severe<br>
          <b>Delirium:</b> Treat underlying cause; environmental modifications; low-dose haloperidol if needed<br>
          <b>No cure</b> for most NCDs — treatment is symptomatic management
        </div>
      </div>
    </div>

    <!-- ===== SUBSTANCE ===== -->
    <div class="view" id="view-substance">
      <div class="section-header">
        <div class="section-tag">Category 13</div>
        <div class="section-title">Substance-Related & Addictive Disorders</div>
        <div class="section-subtitle">Use disorder criteria, intoxication, withdrawal — and gambling disorder</div>
      </div>

      <div class="card">
        <div class="card-title">Substance Use Disorder — 11 Criteria <span class="badge badge-red">Must Know</span></div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 11 Criteria: "WTTL CHUTS RC"</div>
          <b>W</b>ithdrawal · <b>T</b>olerance · <b>T</b>ime spent (obtaining/using/recovering) · <b>L</b>arger amounts than intended<br>
          <b>C</b>raving · <b>H</b>azardous use · <b>U</b>nable to cut down · <b>T</b>rouble fulfilling obligations · <b>S</b>ocial/interpersonal problems<br>
          <b>R</b>ecurrent use causing failure at major role obligations · <b>C</b>ontinued use despite psychological/physical problems
        </div>
        <div class="criteria-grid">
          <div class="criteria-box"><div class="criteria-val">2-3</div><div class="criteria-lbl">Mild (of 11)</div></div>
          <div class="criteria-box"><div class="criteria-val">4-5</div><div class="criteria-lbl">Moderate (of 11)</div></div>
          <div class="criteria-box"><div class="criteria-val">≥6</div><div class="criteria-lbl">Severe (of 11)</div></div>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Board Pearl</div>
          <b>Tolerance and Withdrawal alone do NOT qualify</b> for SUD if occurring solely from prescribed medications used as directed. These are physiological adaptations, not disorder.
        </div>
      </div>

      <div class="card">
        <div class="card-title">Withdrawal Syndromes — High Yield <span class="badge badge-orange">High Yield</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Substance</th><th>Withdrawal Features</th><th>Danger Level</th><th>Treatment</th></tr>
            <tr><td>Alcohol</td><td>Tremor, sweating, seizures, <b>delirium tremens</b> (72 hrs), tachycardia</td><td><b>LIFE-THREATENING</b></td><td>Benzodiazepines (lorazepam, diazepam)</td></tr>
            <tr><td>Benzodiazepines</td><td>Same as alcohol withdrawal</td><td><b>LIFE-THREATENING</b></td><td>Slow taper with long-acting benzo</td></tr>
            <tr><td>Opioids</td><td>"Flu-like" — yawning, lacrimation, rhinorrhea, muscle aches, diarrhea, anxiety</td><td>Not life-threatening</td><td>Methadone, buprenorphine, clonidine</td></tr>
            <tr><td>Stimulants (cocaine, amphetamine)</td><td>"Crash" — depression, fatigue, hypersomnia, increased appetite</td><td>Not life-threatening</td><td>Supportive</td></tr>
            <tr><td>Cannabis</td><td>Irritability, anxiety, sleep problems, decreased appetite</td><td>Not life-threatening</td><td>Supportive</td></tr>
            <tr><td>Nicotine</td><td>Irritability, anxiety, difficulty concentrating, weight gain</td><td>Not life-threatening</td><td>NRT, bupropion, varenicline</td></tr>
          </table>
        </div>
        <div class="trap">
          <div class="trap-label">⚠️ Most Dangerous Withdrawal</div>
          <b>Alcohol and Benzodiazepine withdrawal can be FATAL.</b> Opioid withdrawal is PAINFUL but rarely fatal. This is a classic board question — know the danger hierarchy.
        </div>
        <div class="pearl">
          <div class="pearl-label">💊 Substance Treatment</div>
          <b>Alcohol Use Disorder:</b> Naltrexone, Acamprosate, Disulfiram (Antabuse)<br>
          <b>Opioid Use Disorder:</b> Methadone (opioid agonist), Buprenorphine/Naloxone (Suboxone), Naltrexone<br>
          <b>Psychotherapy:</b> Motivational Interviewing (MI) + CBT = gold standard for all SUD<br>
          <b>12-Step programs:</b> AA, NA (adjunctive, not gold standard alone)
        </div>
      </div>
    </div>

    <!-- ===== SEXUAL & GENDER ===== -->
    <div class="view" id="view-sexual">
      <div class="section-header">
        <div class="section-tag">Category 14-15</div>
        <div class="section-title">Sexual Dysfunctions & Gender Dysphoria</div>
      </div>
      <div class="card">
        <div class="card-title">Sexual Dysfunctions — Quick Overview <span class="badge badge-green">Core</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Feature</th><th>Duration</th><th>Board Clue</th></tr>
            <tr><td>Male Hypoactive Sexual Desire</td><td>Deficient sexual thoughts/desire</td><td><b>≥6 months</b></td><td>Must cause distress</td></tr>
            <tr><td>Female Sexual Interest/Arousal Disorder</td><td>Lack of interest or arousal</td><td>≥6 months</td><td>≥3 of 6 indicators</td></tr>
            <tr><td>Erectile Disorder</td><td>Marked difficulty achieving/maintaining erection</td><td>≥6 months</td><td>75-100% of occasions</td></tr>
            <tr><td>Female Orgasmic Disorder</td><td>Marked delay/absence of orgasm or reduced intensity</td><td>≥6 months</td><td>75-100% of occasions</td></tr>
            <tr><td>Premature Ejaculation</td><td>Ejaculation within ~1 minute, before desired</td><td>≥6 months</td><td>>75-100% of occasions</td></tr>
            <tr><td>Genito-Pelvic Pain/Penetration Disorder</td><td>Pain during intercourse; tightening of vaginal muscles</td><td>≥6 months</td><td>Merged vaginismus + dyspareunia</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 Gender Dysphoria Pearl</div>
          Gender Dysphoria = marked incongruence between experienced/expressed gender and assigned gender; must cause <b>clinically significant distress</b>. DSM-5-TR uses "Gender Dysphoria" (not Gender Identity Disorder). Being transgender alone is NOT a mental disorder — only the distress caused by incongruence qualifies.
        </div>
      </div>
    </div>

    <!-- ===== SLEEP ===== -->
    <div class="view" id="view-sleep">
      <div class="section-header">
        <div class="section-tag">Category 16</div>
        <div class="section-title">Sleep-Wake Disorders</div>
      </div>
      <div class="card">
        <div class="card-title">Sleep Disorders — Quick Reference <span class="badge badge-green">Core</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Feature</th><th>Board Clue</th></tr>
            <tr><td>Insomnia Disorder</td><td>Difficulty initiating/maintaining sleep; ≥3 nights/week, ≥3 months</td><td>Despite adequate opportunity</td></tr>
            <tr><td>Hypersomnolence Disorder</td><td>Excessive sleepiness ≥3x/week despite ≥7 hrs sleep</td><td>Distinct from narcolepsy</td></tr>
            <tr><td>Narcolepsy</td><td>Irresistible sleep attacks + cataplexy + sleep paralysis + hypnagogic hallucinations</td><td>Cataplexy (sudden muscle weakness with strong emotion)</td></tr>
            <tr><td>Obstructive Sleep Apnea</td><td>Apneas during sleep, snoring, daytime sleepiness</td><td>Diagnosed by polysomnography</td></tr>
            <tr><td>REM Sleep Behavior Disorder</td><td>Acting out dreams (no REM atonia)</td><td>Older men; associated with Parkinson's/Lewy body</td></tr>
            <tr><td>Restless Legs Syndrome</td><td>Urge to move legs, worse at rest/night, relieved by movement</td><td>Circadian pattern</td></tr>
            <tr><td>NREM Sleep Arousal Disorder</td><td>Sleepwalking or sleep terrors (NREM stage 3)</td><td>No memory of episode; can't be awakened easily</td></tr>
            <tr><td>Nightmare Disorder</td><td>Frightening dreams from REM sleep; full recall</td><td>Unlike sleep terrors — remember the dream</td></tr>
          </table>
        </div>
        <div class="mnemonic">
          <div class="mnemonic-label">🧠 Narcolepsy Tetrad: "CASH"</div>
          <b>C</b>ataplexy · <b>A</b>utomatic behavior · <b>S</b>leep paralysis · <b>H</b>ypnagogic hallucinations
        </div>
      </div>
    </div>

    <!-- ===== DISRUPTIVE ===== -->
    <div class="view" id="view-disruptive">
      <div class="section-header">
        <div class="section-tag">Category 17</div>
        <div class="section-title">Disruptive, Impulse-Control & Conduct Disorders</div>
      </div>
      <div class="card">
        <div class="card-title">Disruptive Disorders — Quick Compare <span class="badge badge-orange">High Yield</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Core Feature</th><th>Age Onset</th><th>Board Clue</th></tr>
            <tr><td>ODD (Oppositional Defiant)</td><td>Angry/irritable mood + argumentative/defiant + vindictiveness toward authority</td><td>Before <b>8 years</b></td><td>Defiant WITHOUT violating others' rights</td></tr>
            <tr><td>Conduct Disorder</td><td>Violates rules/rights of others: aggression, destruction, deceitfulness, rule violations</td><td>Childhood or adolescent onset</td><td>Violates rights; precursor to ASPD</td></tr>
            <tr><td>Intermittent Explosive Disorder</td><td>Recurrent explosive outbursts; impulsive/reactive aggression</td><td>Adolescence/early adulthood</td><td>Rage disproportionate to trigger</td></tr>
            <tr><td>Pyromania</td><td>Deliberate fire-setting; tension/excitement before; NO external motive</td><td>Any</td><td>Fire-setting + excitement/tension + not for gain</td></tr>
            <tr><td>Kleptomania</td><td>Recurrent impulsive theft; not for need/value; tension before, relief after</td><td>Any</td><td>Steals things they don't need; not for money</td></tr>
          </table>
        </div>
        <div class="pearl">
          <div class="pearl-label">💎 ODD vs Conduct Disorder vs ASPD Timeline</div>
          <b>ODD → Conduct Disorder → ASPD</b> (developmental progression)<br>
          ODD: Defiant (no rights violations) → CD: Violates rights of others (<18) → ASPD: Same pattern (≥18)<br>
          ASPD requires CD history before age 15.
        </div>
      </div>
    </div>

    <!-- ===== TREATMENTS ===== -->
    <div class="view" id="view-treatments">
      <div class="section-header">
        <div class="section-tag">Master Reference</div>
        <div class="section-title">Treatment Cheat Sheet</div>
        <div class="section-subtitle">Gold-standard pairings, medication classes, and therapy associations</div>
      </div>

      <div class="card">
        <div class="card-title">🏆 Gold-Standard Treatment Pairings <span class="badge badge-red">Must Memorize</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Disorder</th><th>Gold Standard Treatment</th><th>Board Clue</th></tr>
            <tr><td>OCD</td><td><b>ERP (Exposure & Response Prevention)</b></td><td>Most tested OCD treatment</td></tr>
            <tr><td>Borderline Personality Disorder</td><td><b>DBT (Dialectical Behavior Therapy)</b></td><td>Classic association — always DBT for BPD</td></tr>
            <tr><td>Specific Phobia</td><td><b>Systematic Desensitization / Exposure Therapy</b></td><td>In vivo exposure = most effective</td></tr>
            <tr><td>PTSD</td><td><b>Trauma-Focused CBT (TF-CBT) / PE / CPT / EMDR</b></td><td>Trauma-focused is key</td></tr>
            <tr><td>ADHD</td><td><b>Stimulants + Behavioral Therapy</b></td><td>Combined treatment; behavior first for preschoolers</td></tr>
            <tr><td>Autism Spectrum Disorder</td><td><b>ABA (Applied Behavior Analysis)</b></td><td>Always ABA for ASD</td></tr>
            <tr><td>Schizophrenia</td><td><b>Atypical Antipsychotics + Psychosocial Interventions</b></td><td>Never antipsychotics alone</td></tr>
            <tr><td>Bipolar I (acute mania)</td><td><b>Mood Stabilizers (Lithium, Valproate)</b></td><td>Never antidepressants alone</td></tr>
            <tr><td>Major Depressive Disorder</td><td><b>CBT or IPT + SSRIs</b></td><td>Combined is most effective</td></tr>
            <tr><td>Bulimia Nervosa</td><td><b>CBT + Fluoxetine (SSRI)</b></td><td>Only FDA-approved med for BN</td></tr>
            <tr><td>Anorexia Nervosa</td><td><b>Nutritional Rehabilitation FIRST</b></td><td>Weight restoration before therapy</td></tr>
            <tr><td>Binge-Eating Disorder</td><td><b>CBT + Lisdexamfetamine (Vyvanse)</b></td><td>Only FDA-approved med for BED</td></tr>
            <tr><td>Alcohol Use Disorder</td><td><b>MI + CBT + Naltrexone/Acamprosate</b></td><td>MI is always first step</td></tr>
            <tr><td>Opioid Use Disorder</td><td><b>Methadone or Buprenorphine (MAT)</b></td><td>Medication-Assisted Treatment</td></tr>
            <tr><td>Social Anxiety Disorder</td><td><b>CBT + SSRIs</b></td><td>CBT addresses cognitions + exposure</td></tr>
            <tr><td>Panic Disorder</td><td><b>CBT (interoceptive exposure) + SSRIs</b></td><td>Interoceptive = body sensation exposure</td></tr>
            <tr><td>Trichotillomania / Excoriation</td><td><b>HRT (Habit Reversal Training)</b></td><td>Not SSRIs first-line</td></tr>
            <tr><td>Insomnia Disorder</td><td><b>CBT-I (CBT for Insomnia)</b></td><td>NOT sleep meds first-line</td></tr>
            <tr><td>Treatment-Resistant MDD</td><td><b>ECT (Electroconvulsive Therapy)</b></td><td>Most effective for severe/TRD</td></tr>
            <tr><td>Conduct Disorder / ODD</td><td><b>Parent Management Training + CBT</b></td><td>Family involvement is key</td></tr>
          </table>
        </div>
      </div>

      <div class="card">
        <div class="card-title">💊 Medication Classes — Board Cheat Sheet <span class="badge badge-orange">High Yield</span></div>
        <div class="tbl-wrap">
          <table>
            <tr><th>Class</th><th>Used For</th><th>Examples</th><th>Key Side Effect</th><th>Board Pearl</th></tr>
            <tr><td>SSRIs</td><td>MDD, Anxiety, OCD, BN, PTSD, Panic</td><td>Fluoxetine, Sertraline, Escitalopram, Paroxetine</td><td>Sexual dysfunction, GI, serotonin syndrome</td><td>First-line for most mood/anxiety disorders</td></tr>
            <tr><td>SNRIs</td><td>MDD, GAD, Fibromyalgia</td><td>Venlafaxine, Duloxetine</td><td>Hypertension, sweating</td><td>Venlafaxine = best for GAD</td></tr>
            <tr><td>TCAs</td><td>MDD, OCD (clomipramine), pain, enuresis</td><td>Amitriptyline, Imipramine, Clomipramine</td><td>Anticholinergic (dry mouth, constipation), cardiac, lethal in OD</td><td>Clomipramine = most effective for OCD of all meds</td></tr>
            <tr><td>MAOIs</td><td>Atypical depression, refractory cases</td><td>Phenelzine, Tranylcypromi
