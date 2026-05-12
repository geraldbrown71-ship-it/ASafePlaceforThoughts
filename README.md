
<html lang="en">
l[image alt](CB6F6C12-5A2F-4CCD-BD81-280C82AFB74F.PNG)
  <meta charset="UTF-8" />
  <title>ASafePlaceForThoughts – Men’s Mental Health</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #050810;
      --bg-alt: #0c1220;
      --card: #151b2c;
      --accent: #4fd1c5;
      --accent-soft: rgba(79, 209, 197, 0.15);
      --text: #f7fafc;
      --muted: #a0aec0;
      --danger: #f56565;
      --success: #48bb78;
      --border: #2d3748;
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.55);
      --radius-lg: 18px;
      --radius-pill: 999px;
      --transition: 0.25s ease;
      --font-main: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: var(--font-main);
      background: radial-gradient(circle at top, #1a365d 0, #050810 45%, #020309 100%);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font-family: inherit;
      cursor: pointer;
    }

    /* Layout */

    header {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(18px);
      background: linear-gradient(to right, rgba(5, 8, 16, 0.96), rgba(5, 8, 16, 0.85));
      border-bottom: 1px solid rgba(79, 209, 197, 0.15);
    }

    .nav {
      max-width: 1120px;
      margin: 0 auto;
      padding: 14px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-size: 0.9rem;
    }

    .logo-mark {
      width: 32px;
      height: 32px;
      border-radius: 12px;
      background: radial-gradient(circle at 30% 20%, #81e6d9, #2c5282 55%, #171923 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 0 1px rgba(79, 209, 197, 0.4);
      font-size: 0.8rem;
    }

    .nav-links {
      display: flex;
      gap: 18px;
      font-size: 0.9rem;
    }

    .nav-links button {
      background: transparent;
      border: none;
      color: var(--muted);
      padding: 6px 10px;
      border-radius: 999px;
      transition: color var(--transition), background var(--transition), transform var(--transition);
    }

    .nav-links button:hover {
      color: var(--text);
      background: rgba(79, 209, 197, 0.12);
      transform: translateY(-1px);
    }

    .nav-links button.active {
      color: var(--text);
      background: var(--accent-soft);
      box-shadow: 0 0 0 1px rgba(79, 209, 197, 0.4);
    }

    main {
      flex: 1;
      max-width: 1120px;
      margin: 0 auto;
      padding: 24px 20px 40px;
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2fr);
      gap: 26px;
    }

    @media (max-width: 880px) {
      main {
        grid-template-columns: minmax(0, 1fr);
      }
      header {
        position: static;
      }
      .nav {
        flex-wrap: wrap;
      }
    }

    /* Hero / Intro */

    .hero {
      background: radial-gradient(circle at top left, rgba(79, 209, 197, 0.12), transparent 55%),
                  linear-gradient(145deg, #0b1120, #050810);
      border-radius: 26px;
      padding: 26px 24px 22px;
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(148, 163, 184, 0.35);
      position: relative;
      overflow: hidden;
    }

    .hero-tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.6);
      font-size: 0.75rem;
      color: var(--muted);
      margin-bottom: 12px;
    }

    .hero-tag-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: var(--accent);
      box-shadow: 0 0 0 4px rgba(79, 209, 197, 0.25);
    }

    .hero h1 {
      font-size: 2.1rem;
      line-height: 1.2;
      margin-bottom: 10px;
    }

    .hero h1 span {
      background: linear-gradient(to right, #81e6d9, #63b3ed);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero-sub {
      font-size: 0.95rem;
      color: var(--muted);
      max-width: 32rem;
      margin-bottom: 18px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 18px;
    }

    .btn-primary {
      border-radius: var(--radius-pill);
      border: none;
      padding: 9px 18px;
      font-size: 0.9rem;
      font-weight: 600;
      background: linear-gradient(135deg, #4fd1c5, #63b3ed);
      color: #0b1120;
      box-shadow: 0 14px 30px rgba(66, 153, 225, 0.45);
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: transform var(--transition), box-shadow var(--transition), filter var(--transition);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      filter: brightness(1.05);
      box-shadow: 0 18px 40px rgba(66, 153, 225, 0.6);
    }

    .btn-ghost {
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.7);
      padding: 8px 16px;
      font-size: 0.9rem;
      background: rgba(15, 23, 42, 0.9);
      color: var(--muted);
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: background var(--transition), color var(--transition), border-color var(--transition), transform var(--transition);
    }

    .btn-ghost:hover {
      background: rgba(15, 23, 42, 1);
      color: var(--text);
      border-color: rgba(148, 163, 184, 1);
      transform: translateY(-1px);
    }

    .hero-metrics {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      font-size: 0.8rem;
      color: var(--muted);
      margin-top: 4px;
    }

    .hero-metric {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 6px 10px;
      border-radius: var(--radius-pill);
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.4);
    }

    .hero-metric strong {
      color: var(--text);
      font-size: 0.9rem;
    }

    /* Right column */

    .side-panel {
      display: flex;
      flex-direction: column;
      gap: 18px;
    }

    .card {
      background: radial-gradient(circle at top, rgba(79, 209, 197, 0.12), transparent 60%),
                  linear-gradient(145deg, #050816, #020309);
      border-radius: 22px;
      padding: 18px 16px 16px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      box-shadow: var(--shadow-soft);
    }

    .card-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 10px;
    }

    .card-title {
      font-size: 0.95rem;
      font-weight: 600;
    }

    .card-sub {
      font-size: 0.8rem;
      color: var(--muted);
      margin-bottom: 10px;
    }

    .chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 10px;
    }

    .chip {
      font-size: 0.75rem;
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.5);
      color: var(--muted);
      background: rgba(15, 23, 42, 0.9);
    }

    /* Mood check-in */

    .mood-scale {
      display: flex;
      justify-content: space-between;
      gap: 6px;
      margin: 10px 0 8px;
    }

    .mood-btn {
      flex: 1;
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.5);
      background: rgba(15, 23, 42, 0.9);
      padding: 8px 4px;
      font-size: 0.75rem;
      color: var(--muted);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 4px;
      transition: background var(--transition), border-color var(--transition), transform var(--transition), color var(--transition), box-shadow var(--transition);
    }

    .mood-btn span {
      font-size: 1.1rem;
    }

    .mood-btn:hover {
      transform: translateY(-1px);
      border-color: var(--accent);
      box-shadow: 0 10px 25px rgba(79, 209, 197, 0.35);
    }

    .mood-btn.selected {
      background: radial-gradient(circle at top, rgba(79, 209, 197, 0.25), rgba(15, 23, 42, 0.95));
      border-color: var(--accent);
      color: var(--text);
      box-shadow: 0 12px 30px rgba(79, 209, 197, 0.45);
    }

    .mood-note {
      width: 100%;
      margin-top: 6px;
      border-radius: 12px;
      border: 1px solid rgba(148, 163, 184, 0.5);
      background: rgba(15, 23, 42, 0.9);
      color: var(--text);
      padding: 8px 9px;
      font-size: 0.8rem;
      resize: vertical;
      min-height: 60px;
    }

    .mood-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 8px;
      gap: 8px;
    }

    .mood-status {
      font-size: 0.75rem;
      color: var(--muted);
    }

    .mood-status strong {
      color: var(--accent);
    }

    .btn-small {
      border-radius: var(--radius-pill);
      border: none;
      padding: 6px 12px;
      font-size: 0.8rem;
      font-weight: 500;
      background: rgba(79, 209, 197, 0.12);
      color: var(--accent);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: background var(--transition), transform var(--transition), box-shadow var(--transition);
    }

    .btn-small:hover {
      background: rgba(79, 209, 197, 0.2);
      transform: translateY(-1px);
      box-shadow: 0 10px 25px rgba(79, 209, 197, 0.35);
    }

    /* Tabs / sections */

    .section-tabs {
      margin-top: 18px;
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }

    .section-tab {
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.5);
      padding: 6px 12px;
      font-size: 0.8rem;
      background: rgba(15, 23, 42, 0.9);
      color: var(--muted);
      cursor: pointer;
      transition: background var(--transition), color var(--transition), border-color var(--transition), transform var(--transition);
    }

    .section-tab.active {
      background: var(--accent-soft);
      color: var(--text);
      border-color: var(--accent);
      transform: translateY(-1px);
    }

    .section-content {
      margin-top: 16px;
      display: none;
      animation: fadeIn 0.25s ease-out;
    }

    .section-content.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(4px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Stories */

    .story-list {
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-height: 260px;
      overflow-y: auto;
      padding-right: 4px;
    }

    .story {
      border-radius: 14px;
      padding: 10px 11px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 0.8rem;
    }

    .story-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 4px;
    }

    .story-name {
      font-weight: 600;
      font-size: 0.8rem;
    }

    .story-tagline {
      color: var(--muted);
      font-size: 0.75rem;
      margin-bottom: 4px;
    }

    .story-meta {
      display: flex;
      gap: 8px;
      font-size: 0.7rem;
      color: var(--muted);
      margin-top: 4px;
    }

    .badge {
      border-radius: var(--radius-pill);
      padding: 2px 8px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      font-size: 0.7rem;
      color: var(--muted);
    }

    /* Exercises */

    .exercise-list {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .exercise {
      border-radius: 14px;
      padding: 10px 11px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 0.8rem;
    }

    .exercise-title {
      font-weight: 600;
      margin-bottom: 4px;
    }

    .exercise-steps {
      margin-left: 16px;
      margin-top: 4px;
    }

    .exercise-steps li {
      margin-bottom: 2px;
    }

    /* Journal */

    .journal-form {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .journal-input,
    .journal-textarea {
      width: 100%;
      border-radius: 12px;
      border: 1px solid rgba(148, 163, 184, 0.5);
      background: rgba(15, 23, 42, 0.9);
      color: var(--text);
      padding: 8px 9px;
      font-size: 0.8rem;
      resize: vertical;
    }

    .journal-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.75rem;
      color: var(--muted);
    }

    .journal-list {
      margin-top: 10px;
      max-height: 180px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .journal-entry {
      border-radius: 12px;
      padding: 8px 9px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 0.8rem;
    }

    .journal-entry-header {
      display: flex;
      justify-content: space-between;
      font-size: 0.7rem;
      color: var(--muted);
      margin-bottom: 4px;
    }

    /* Resources */

    .resource-list {
      display: flex;
      flex-direction: column;
      gap: 8px;
      font-size: 0.8rem;
    }

    .resource-item {
      border-radius: 12px;
      padding: 8px 9px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.4);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
    }

    .resource-text {
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .resource-text span:first-child {
      font-weight: 600;
    }

    .resource-text span:last-child {
      color: var(--muted);
      font-size: 0.75rem;
    }

    .resource-tag {
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      padding: 3px 8px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      color: var(--muted);
    }

    /* Toast / feedback */

    .toast {
      position: fixed;
      bottom: 18px;
      right: 18px;
      background: #0f172a;
      border-radius: 14px;
      padding: 10px 12px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      font-size: 0.8rem;
      color: var(--text);
      display: flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.7);
      opacity: 0;
      pointer-events: none;
      transform: translateY(8px);
      transition: opacity 0.2s ease, transform 0.2s ease;
      z-index: 50;
    }

    .toast.show {
      opacity: 1;
      pointer-events: auto;
      transform: translateY(0);
    }

    .toast-icon {
      font-size: 1rem;
    }

    .toast-success .toast-icon {
      color: var(--success);
    }

    .toast-error .toast-icon {
      color: var(--danger);
    }

    footer {
      max-width: 1120px;
      margin: 0 auto;
      padding: 0 20px 20px;
      font-size: 0.75rem;
      color: var(--muted);
      display: flex;
      justify-content: space-between;
      gap: 10px;
      flex-wrap: wrap;
    }

    footer a {
      text-decoration: underline;
      text-decoration-style: dotted;
    }
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="logo">
        <div class="logo-mark">ASPFT</div>
        <span>ASafePlaceForThoughts</span>
      </div>
      <div class="nav-links">
        <button data-nav="home" class="active">Home</button>
        <button data-nav="stories">Stories</button>
        <button data-nav="exercises">Tools</button>
        <button data-nav="journal">Journal</button>
        <button data-nav="resources">Support</button>
      </div>
    </div>
  </header>

  <main>
    <!-- Left: main content -->
    <section>
      <div class="hero">
        <div class="hero-tag">
          <div class="hero-tag-dot"></div>
          <span>Iam strong enough to be vulnerable and brave enough to feel.</span>
        </div>
        <h1>
          You’re not “too much”&mdash;<span>you’ve just carried too many storms alone.</span>
        </h1>
        <p class="hero-sub">
          You pushed through.You didnt complain.You buried what hurts and kept moving. That weight doesnt disappear-it builds.This is where you deal with it, without judgemwnt.
        </p>
        <div class="hero-actions">
          <button class="btn-primary" id="startCheckIn">
            Start a 60‑second check‑in
            <span>⏱️</span>
          </button>
          <button class="btn-ghost" id="openStoryTab">
            Read real stories
            <span>📖</span>
          </button>
        </div>
        <div class="hero-metrics">
          <div class="hero-metric">
            <strong>3,200+</strong>
            men logged a check‑in
          </div>
          <div class="hero-metric">
            <strong>72%</strong>
            say naming feelings made them feel lighter
          </div>
          <div class="hero-metric">
            <strong>1 rule</strong>
            you don’t have to be “the strong one” here
          </div>
        </div>

        <div class="section-tabs">
          <button class="section-tab active" data-section="stories">Stories</button>
          <button class="section-tab" data-section="exercises">Exercises</button>
          <button class="section-tab" data-section="journal">Journal</button>
          <button class="section-tab" data-section="resources">Resources</button>
        </div>

        <!-- Stories section -->
        <div class="section-content active" id="section-stories">
          <div class="story-list" id="storyList">
            <!-- Stories will be injected by JS -->
          </div>
        </div>

        <!-- Exercises section -->
        <div class="section-content" id="section-exercises">
          <div class="exercise-list" id="exerciseList">
            <!-- Exercises injected by JS -->
          </div>
        </div>

        <!-- Journal section -->
        <div class="section-content" id="section-journal">
          <form class="journal-form" id="journalForm">
            <input
              type="text"
              class="journal-input"
              id="journalTitle"
              placeholder="Title (e.g. 'What I needed as a kid')"
            />
            <textarea
              class="journal-textarea"
              id="journalBody"
              rows="4"
              placeholder="Write like no one is judging you. What’s sitting heavy on your chest today?"
            ></textarea>
            <div class="journal-meta">
              <span id="journalCharCount">0 / 600</span>
              <button type="submit" class="btn-small">
                Save entry
              </button>
            </div>
          </form>
          <div class="journal-list" id="journalList"></div>
        </div>

        <!-- Resources section -->
        <div class="section-content" id="section-resources">
          <div class="resource-list" id="resourceList">
            <!-- Resources injected by JS -->
          </div>
        </div>
      </div>
    </section>

    <!-- Right: mood check-in + quick tools -->
    <aside class="side-panel">
      <div class="card">
        <div class="card-header">
          <div>
            <div class="card-title">Quick mood check‑in</div>
            <div class="card-sub">No scores, no judgment. Just a quick “how am I really?”</div>
          </div>
        </div>

        <div class="chip-row">
          <span class="chip">Grew up in chaos</span>
          <span class="chip">Old wounds</span>
          <span class="chip">Breaking patterns</span>
        </div>

        <div class="mood-scale" id="moodScale">
          <button class="mood-btn" data-mood="overwhelmed">
            <span>🌧️</span>
            <small>Overwhelmed</small>
          </button>
          <button class="mood-btn" data-mood="numb">
            <span>🧊</span>
            <small>Numb</small>
          </button>
          <button class="mood-btn" data-mood="tired">
            <span>😮‍💨</span>
            <small>Just tired</small>
          </button>
          <button class="mood-btn" data-mood="okay">
            <span>🌤️</span>
            <small>Okay</small>
          </button>
          <button class="mood-btn" data-mood="hopeful">
            <span>🌅</span>
            <small>Hopeful</small>
          </button>
        </div>

        <textarea
          class="mood-note"
          id="moodNote"
          placeholder="If you want, add a sentence: What’s making today heavy or lighter than usual?"
        ></textarea>

        <div class="mood-footer">
          <div class="mood-status" id="moodStatus">
            Today’s check‑in: <strong>not saved yet</strong>
          </div>
          <button class="btn-small" id="saveMood">
            Save check‑in
          </button>
        </div>
      </div>

      <div class="card">
        <div class="card-header">
          <div>
            <div class="card-title">Grounding in 30 seconds</div>
            <div class="card-sub">When your chest is tight and your thoughts are loud.</div>
          </div>
        </div>
        <div class="exercise">
          <div class="exercise-title">5–4–3–2–1 reset</div>
          <ul class="exercise-steps">
            <li>5 things you can see</li>
            <li>4 things you can touch</li>
            <li>3 things you can hear</li>
            <li>2 things you can smell</li>
            <li>1 thing you’re grateful you survived</li>
          </ul>
        </div>
        <button class="btn-small" id="startGrounding">
          Walk me through it
        </button>
      </div>
    </aside>
  </main>

  <footer>
    <span>Not therapy, not a diagnosis—just a place to not carry it alone.</span>
    <span>
      If you’re in immediate danger or thinking about self‑harm, contact your local emergency number or a crisis line.
    </span>
  </footer>

  <!-- Toast -->
  <div class="toast" id="toast">
    <span class="toast-icon">✅</span>
    <span id="toastMessage">Saved</span>
  </div>

  <script>
    // --- Data ---

    const stories = [
      {
        name: "Marcus, 34",
        tagline: "“I thought anger was my only language.”",
        text:
          "I grew up in a house where yelling was how you knew people cared. When I had my own son, I caught myself using the same tone on him that used to make me shrink. Therapy helped, but honestly, the first step was just admitting I was scared, not just angry.",
        tags: ["Anger", "Fatherhood", "Breaking cycles"],
        time: "Shared 2 weeks ago"
      },
      {
        name: "Luis, 28",
        tagline: "“Being the ‘man of the house’ at 10 messed me up.”",
        text:
          "My dad left and suddenly every adult in my family called me ‘the man of the house.’ I didn’t know how to be a kid and I still don’t know how to ask for help without feeling weak. I’m learning that needing support doesn’t cancel out everything I survived.",
        tags: ["Parentification", "Responsibility", "Asking for help"],
        time: "Shared 5 days ago"
      },
      {
        name: "Jay, 41",
        tagline: "“I used to think crying meant I lost.”",
        text:
          "Where I’m from, crying was something you did once, at a funeral, and even then you wiped your face fast. The first time I cried in front of a friend and he didn’t flinch, something in me softened. I realized I’d been fighting myself for decades.",
        tags: ["Crying", "Friendship", "Softening"],
        time: "Shared yesterday"
      }
    ];

    const exercises = [
      {
        title: "Name it to tame it",
        steps: [
          "Pause and notice: what’s happening in your body right now?",
          "Pick 1–2 words for the feeling (e.g. ‘resentful’, ‘lonely’, ‘on edge’).",
          "Say it out loud or write it: “Right now I feel ____ and it makes sense because ____.”",
          "Remind yourself: feelings are information, not a verdict on your worth."
        ]
      },
      {
        title: "Rewriting the script",
        steps: [
          "Think of a sentence you heard growing up (e.g. “Stop crying or I’ll give you something to cry about”).",
          "Write it down, then underneath write what you wish you’d heard instead.",
          "Read the new sentence slowly, like you’re saying it to your younger self.",
          "Keep the new version somewhere you can see it this week."
        ]
      }
    ];

    const resources = [
      {
        name: "National Suicide & Crisis Lifeline (US)",
        desc: "Call or text 988 – free, confidential support 24/7.",
        tag: "Crisis"
      },
      {
        name: "Therapy directories",
        desc: "Search for therapists who specialize in men’s issues and childhood trauma.",
        tag: "Therapy"
      },
      {
        name: "Men’s support groups",
        desc: "Look for local or online groups focused on men’s mental health and recovery.",
        tag: "Community"
      }
    ];

    // --- Helpers ---

    const $ = (selector) => document.querySelector(selector);
    const $$ = (selector) => document.querySelectorAll(selector);

    function showToast(message, type = "success") {
      const toast = $("#toast");
      const msg = $("#toastMessage");
      const icon = toast.querySelector(".toast-icon");

      msg.textContent = message;
      toast.classList.remove("toast-success", "toast-error");
      if (type === "success") {
        toast.classList.add("toast-success");
        icon.textContent = "✅";
      } else {
        toast.classList.add("toast-error");
        icon.textContent = "⚠️";
      }

      toast.classList.add("show");
      setTimeout(() => {
        toast.classList.remove("show");
      }, 2600);
    }

    // --- Navigation (top nav + internal tabs) ---

    const navButtons = $$(".nav-links button");
    const sectionTabs = $$(".section-tab");

    navButtons.forEach((btn) => {
      btn.addEventListener("click", () => {
        navButtons.forEach((b) => b.classList.remove("active"));
        btn.classList.add("active");

        const target = btn.dataset.nav;
        if (target === "stories") {
          activateSection("stories");
        } else if (target === "exercises") {
          activateSection("exercises");
        } else if (target === "journal") {
          activateSection("journal");
        } else if (target === "resources") {
          activateSection("resources");
        } else {
          activateSection("stories");
        }

        window.scrollTo({ top: 0, behavior: "smooth" });
      });
    });

    function activateSection(sectionId) {
      sectionTabs.forEach((tab) => {
        tab.classList.toggle("active", tab.dataset.section === sectionId);
      });
      [ "stories", "exercises", "journal", "resources" ].forEach((id) => {
        const el = $("#section-" + id);
        if (!el) return;
        el.classList.toggle("active", id === sectionId);
      });
    }

    sectionTabs.forEach((tab) => {
      tab.addEventListener("click", () => {
        activateSection(tab.dataset.section);
      });
    });

    $("#openStoryTab").addEventListener("click", () => {
      activateSection("stories");
      navButtons.forEach((b) => b.classList.remove("active"));
      navButtons.forEach((b) => {
        if (b.dataset.nav === "stories") b.classList.add("active");
      });
      window.scrollTo({ top: 0, behavior: "smooth" });
    });

    // --- Render stories ---

    function renderStories() {
      const container = $("#storyList");
      container.innerHTML = "";
      stories.forEach((story) => {
        const div = document.createElement("article");
        div.className = "story";
        div.innerHTML = `
          <div class="story-header">
            <span class="story-name">${story.name}</span>
            <span class="badge">${story.time}</span>
          </div>
          <div class="story-tagline">${story.tagline}</div>
          <p>${story.text}</p>
          <div class="story-meta">
            ${story.tags.map((t) => `<span>#${t}</span>`).join("")}
          </div>
        `;
        container.appendChild(div);
      });
    }

    // --- Render exercises ---

    function renderExercises() {
      const container = $("#exerciseList");
      container.innerHTML = "";
      exercises.forEach((ex) => {
        const div = document.createElement("article");
        div.className = "exercise";
        div.innerHTML = `
          <div class="exercise-title">${ex.title}</div>
          <ul class="exercise-steps">
            ${ex.steps.map((s) => `<li>${s}</li>`).join("")}
          </ul>
        `;
        container.appendChild(div);
      });
    }

    // --- Render resources ---

    function renderResources() {
      const container = $("#resourceList");
      container.innerHTML = "";
      resources.forEach((r) => {
        const div = document.createElement("div");
        div.className = "resource-item";
        div.innerHTML = `
          <div class="resource-text">
            <span>${r.name}</span>
            <span>${r.desc}</span>
          </div>
          <span class="resource-tag">${r.tag}</span>
        `;
        container.appendChild(div);
      });
    }

    // --- Mood check-in ---

    let selectedMood = null;

    $$("#moodScale .mood-btn").forEach((btn) => {
      btn.addEventListener("click", () => {
        $$("#moodScale .mood-btn").forEach((b) => b.classList.remove("selected"));
        btn.classList.add("selected");
        selectedMood = btn.dataset.mood;
        updateMoodStatus();
      });
    });

    function updateMoodStatus(saved = false) {
      const status = $("#moodStatus");
      if (!selectedMood) {
        status.innerHTML = "Today’s check‑in: <strong>not saved yet</strong>";
        return;
      }
      const moodLabel = selectedMood.charAt(0).toUpperCase() + selectedMood.slice(1);
      status.innerHTML = saved
        ? `Saved as: <strong>${moodLabel}</strong>`
        : `Selected: <strong>${moodLabel}</strong> (not saved yet)`;
    }

    $("#saveMood").addEventListener("click", () => {
      if (!selectedMood && !$("#moodNote").value.trim()) {
        showToast("Pick a mood or write a note first.", "error");
        return;
      }
      updateMoodStatus(true);
      showToast("Today’s check‑in saved.");
    });

    $("#startCheckIn").addEventListener("click", () => {
      window.scrollTo({ top: document.body.scrollHeight, behavior: "smooth" });
      showToast("Start with picking a mood that feels closest to right now.");
    });

    // --- Grounding walkthrough ---

    $("#startGrounding").addEventListener("click", () => {
      const steps = [
        "Look around and name 5 things you can see.",
        "Now 4 things you can touch from where you are.",
        "3 things you can hear, even if they’re faint.",
        "2 things you can smell, or remember a smell you like.",
        "1 thing you’re grateful you survived."
      ];
      let i = 0;
      function nextStep() {
        if (i >= steps.length) {
          showToast("Nice job. One small reset at a time.");
          return;
        }
        const proceed = confirm(steps[i] + "\n\nClick OK when you’re ready for the next step.");
        if (proceed) {
          i++;
          nextStep();
        }
      }
      nextStep();
    });

    // --- Journal ---

    const journalForm = $("#journalForm");
    const journalTitle = $("#journalTitle");
    const journalBody = $("#journalBody");
    const journalList = $("#journalList");
    const journalCharCount = $("#journalCharCount");
    const JOURNAL_LIMIT = 600;

    function loadJournalEntries() {
      try {
        const raw = localStorage.getItem("stb_journal");
        if (!raw) return [];
        return JSON.parse(raw);
      } catch {
        return [];
      }
    }

    function saveJournalEntries(entries) {
      localStorage.setItem("stb_journal", JSON.stringify(entries));
    }

    function renderJournalEntries() {
      const entries = loadJournalEntries();
      journalList.innerHTML = "";
      if (!entries.length) {
        const empty = document.createElement("div");
        empty.className = "journal-entry";
        empty.textContent = "Your entries will show up here. You don’t have to write something deep—just honest.";
        journalList.appendChild(empty);
        return;
      }
      entries
        .slice()
        .reverse()
        .forEach((entry) => {
          const div = document.createElement("article");
          div.className = "journal-entry";
          div.innerHTML = `
            <div class="journal-entry-header">
              <span>${entry.title || "Untitled"}</span>
              <span>${entry.date}</span>
            </div>
            <p>${entry.body}</p>
          `;
          journalList.appendChild(div);
        });
    }

    journalBody.addEventListener("input", () => {
      const len = journalBody.value.length;
      if (len > JOURNAL_LIMIT) {
        journalBody.value = journalBody.value.slice(0, JOURNAL_LIMIT);
      }
      journalCharCount.textContent = `${journalBody.value.length} / ${JOURNAL_LIMIT}`;
    });

    journalForm.addEventListener("submit", (e) => {
      e.preventDefault();
      const title = journalTitle.value.trim();
      const body = journalBody.value.trim();
      if (!title && !body) {
        showToast("Write something first, even one sentence.", "error");
        return;
      }
      const entries = loadJournalEntries();
      entries.push({
        title,
        body,
        date: new Date().toLocaleString()
      });
      saveJournalEntries(entries);
      renderJournalEntries();
      journalTitle.value = "";
      journalBody.value = "";
      journalCharCount.textContent = `0 / ${JOURNAL_LIMIT}`;
      showToast("Journal entry saved.");
    });

    // --- Init ---

    renderStories();
    renderExercises();
    renderResources();
    renderJournalEntries();
  </script>
</body>
</html>
