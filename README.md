# g5fwknthhr-blip.github.io

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="apple-mobile-web-app-capable" content="yes">
<title>The Inner Temple — Year 22</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700&family=Cinzel:wght@400;500;600&family=EB+Garamond:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
}

  :root {
    --gold: #c9a84c;
    --gold-light: #e8c96a;
    --gold-pale: #f5e6b8;
    --deep: #0a0a0f;
    --ink: #12121a;
    --parchment: #f7f0e0;
    --crimson: #8b1a2a;
    --azure: #1a3a5c;
    --sage: #3a5c3a;
    --text: #e8dfc8;
    --muted: #8a7f6a;
  }
  
  html { scroll-behavior: smooth; }

  body {
    background: var(--deep);
    color: var(--text);
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 18px;
    line-height: 1.8;
    min-height: 100vh;
    overflow-x: hidden;
  }
  
/* ── STARFIELD ── */
  #stars {
    position: fixed; inset: 0; z-index: 0; pointer-events: none;
    background:
      radial-gradient(ellipse at 20% 30%, rgba(201,168,76,0.06) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 70%, rgba(26,58,92,0.12) 0%, transparent 60%),
      var(--deep);
  }
  #stars::before, #stars::after {
    content: '';
    position: absolute; inset: 0;
    background-image:
      radial-gradient(1px 1px at 10% 15%, rgba(248,236,180,0.8) 0%, transparent 100%),
      radial-gradient(1px 1px at 25% 40%, rgba(248,236,180,0.5) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 40% 10%, rgba(201,168,76,0.9) 0%, transparent 100%),
      radial-gradient(1px 1px at 55% 60%, rgba(248,236,180,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 70% 25%, rgba(248,236,180,0.7) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 85% 50%, rgba(201,168,76,0.8) 0%, transparent 100%),
      radial-gradient(1px 1px at 15% 75%, rgba(248,236,180,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 60% 85%, rgba(248,236,180,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 90% 10%, rgba(248,236,180,0.7) 0%, transparent 100%),
      radial-gradient(1px 1px at 35% 90%, rgba(248,236,180,0.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 75% 80%, rgba(248,236,180,0.5) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 5% 50%, rgba(201,168,76,0.7) 0%, transparent 100%);
  }
  #stars::after {
    background-image:
      radial-gradient(1px 1px at 48% 32%, rgba(248,236,180,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 62% 18%, rgba(248,236,180,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 28% 55%, rgba(248,236,180,0.7) 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 92% 42%, rgba(201,168,76,0.8) 0%, transparent 100%),
      radial-gradient(1px 1px at 18% 88%, rgba(248,236,180,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 80% 95%, rgba(248,236,180,0.4) 0%, transparent 100%);
    animation: twinkle 6s ease-in-out infinite alternate;
  }
  @keyframes twinkle {
    0% { opacity: 0.6; }
    100% { opacity: 1; }
  }

/* ── LAYOUT ── */
  .wrapper {
    position: relative; z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 0 24px 80px;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 80px 0 60px;
    animation: fadeDown 1.4s ease both;
  }
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .sigil {
    width: 110px; height: 110px;
    margin: 0 auto 32px;
    position: relative;
    animation: rotateSlow 40s linear infinite;
  }
  @keyframes rotateSlow { to { transform: rotate(360deg); } }

  .sigil svg { width: 100%; height: 100%; }

  .year-badge {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    letter-spacing: 0.4em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 18px;
    opacity: 0.85;
  }

  h1 {
    font-family: 'Cinzel Decorative', serif;
    font-size: clamp(28px, 6vw, 48px);
    font-weight: 400;
    color: var(--gold-light);
    line-height: 1.2;
    margin-bottom: 16px;
    text-shadow: 0 0 40px rgba(201,168,76,0.3);
  }

  .hero-sub {
    font-style: italic;
    color: var(--muted);
    font-size: 17px;
    max-width: 500px;
    margin: 0 auto;
  }

  /* ── DIVIDER ── */
  .divider {
    display: flex; align-items: center; gap: 16px;
    margin: 40px 0;
    opacity: 0.4;
  }
  .divider::before, .divider::after {
    content: ''; flex: 1;
    height: 1px;
    background: linear-gradient(to right, transparent, var(--gold), transparent);
  }
  .divider span { color: var(--gold); font-size: 14px; }

  /* ── SECTION CARD ── */
  .card {
    background: linear-gradient(135deg, rgba(255,255,255,0.03) 0%, rgba(201,168,76,0.03) 100%);
    border: 1px solid rgba(201,168,76,0.15);
    border-radius: 2px;
    padding: 36px 40px;
    margin-bottom: 28px;
    position: relative;
    animation: fadeUp 0.8s ease both;
  }
  .card::before {
    content: '';
    position: absolute; top: 0; left: 0;
    width: 3px; height: 100%;
    background: linear-gradient(to bottom, var(--gold), transparent);
    border-radius: 2px 0 0 2px;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .card:nth-child(2) { animation-delay: 0.1s; }
  .card:nth-child(3) { animation-delay: 0.2s; }
  .card:nth-child(4) { animation-delay: 0.3s; }
  .card:nth-child(5) { animation-delay: 0.4s; }

  .card-header {
    display: flex; align-items: center; gap: 14px;
    margin-bottom: 20px;
  }
  .card-icon {
    font-size: 22px;
    width: 42px; height: 42px;
    background: rgba(201,168,76,0.08);
    border: 1px solid rgba(201,168,76,0.2);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .card-title {
    font-family: 'Cinzel', serif;
    font-size: 13px;
    letter-spacing: 0.25em;
    color: var(--gold);
    text-transform: uppercase;
  }

  .card p { color: #c8bfa8; margin-bottom: 14px; }
  .card p:last-child { margin-bottom: 0; }

  /* ── PILLARS ── */
  .pillars {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin: 28px 0;
  }
  @media (max-width: 600px) {
    .pillars { grid-template-columns: 1fr; }
  }
  .pillar {
    background: rgba(201,168,76,0.04);
    border: 1px solid rgba(201,168,76,0.12);
    border-radius: 2px;
    padding: 20px 16px;
    text-align: center;
  }
  .pillar-icon { font-size: 24px; margin-bottom: 10px; }
  .pillar-name {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    letter-spacing: 0.2em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 8px;
  }
  .pillar p { font-size: 14px; color: var(--muted); margin: 0; }

  /* ── DAILY PRACTICE ── */
  .practice-list { list-style: none; padding: 0; }
  .practice-list li {
    display: flex; gap: 16px; align-items: flex-start;
    padding: 14px 0;
    border-bottom: 1px solid rgba(201,168,76,0.07);
  }
  .practice-list li:last-child { border-bottom: none; }
  .practice-num {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    color: var(--gold);
    letter-spacing: 0.1em;
    padding-top: 3px;
    min-width: 28px;
  }
  .practice-content strong {
    display: block;
    color: var(--gold-pale);
    font-family: 'Cinzel', serif;
    font-size: 13px;
    letter-spacing: 0.1em;
    font-weight: 500;
    margin-bottom: 4px;
  }
  .practice-content span { font-size: 15px; color: #a09880; }

  /* ── QUOTES ── */
  blockquote {
    border-left: 2px solid var(--gold);
    padding: 12px 20px;
    margin: 20px 0;
    background: rgba(201,168,76,0.04);
  }
  blockquote p {
    font-style: italic;
    font-size: 17px;
    color: var(--gold-pale) !important;
    margin-bottom: 6px !important;
  }
  blockquote cite {
    font-size: 12px;
    letter-spacing: 0.15em;
    color: var(--muted);
    font-style: normal;
    font-family: 'Cinzel', serif;
    text-transform: uppercase;
  }

  /* ── AFFIRMATIONS ── */
  .affirmations { list-style: none; padding: 0; }
  .affirmations li {
    padding: 10px 0;
    border-bottom: 1px solid rgba(201,168,76,0.06);
    color: #c8bfa8;
    font-style: italic;
    font-size: 17px;
    display: flex; gap: 12px; align-items: flex-start;
  }
  .affirmations li::before {
    content: '✦';
    color: var(--gold);
    font-style: normal;
    font-size: 12px;
    padding-top: 4px;
    flex-shrink: 0;
  }
  .affirmations li:last-child { border-bottom: none; }

  /* ── THE SEVEN ── */
  .seven-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin-top: 16px;
  }
  @media (max-width: 500px) { .seven-grid { grid-template-columns: 1fr; } }
  .seven-item {
    background: rgba(201,168,76,0.03);
    border: 1px solid rgba(201,168,76,0.1);
    border-radius: 2px;
    padding: 14px 16px;
  }
  .seven-item-title {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    letter-spacing: 0.2em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 5px;
  }
  .seven-item p { font-size: 14px; color: var(--muted); margin: 0; }

  /* ── FOOTER ── */
  footer {
    text-align: center;
    padding: 48px 0 0;
    border-top: 1px solid rgba(201,168,76,0.1);
    margin-top: 48px;
  }
  footer p {
    font-family: 'Cinzel', serif;
    font-size: 11px;
    letter-spacing: 0.3em;
    color: var(--muted);
    text-transform: uppercase;
  }
  .gold-text { color: var(--gold); }

  /* ── NAV TABS ── */
  .nav-tabs {
    display: flex; gap: 8px; flex-wrap: wrap;
    margin-bottom: 32px;
    justify-content: center;
  }
  .tab-btn {
    background: transparent;
    border: 1px solid rgba(201,168,76,0.2);
    color: var(--muted);
    font-family: 'Cinzel', serif;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    padding: 8px 16px;
    cursor: pointer;
    border-radius: 1px;
    transition: all 0.3s;
  }
  .tab-btn:hover, .tab-btn.active {
    background: rgba(201,168,76,0.1);
    color: var(--gold);
    border-color: rgba(201,168,76,0.4);
  }

  .tab-section { display: none; }
  .tab-section.active { display: block; }
</style>
</head>
<body>
<div id="stars"></div>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="sigil">
      <svg viewBox="0 0 110 110" fill="none" xmlns="http://www.w3.org/2000/svg">
        <!-- Outer circle -->
        <circle cx="55" cy="55" r="52" stroke="#c9a84c" stroke-width="0.8" opacity="0.5"/>
        <!-- Inner circle -->
        <circle cx="55" cy="55" r="38" stroke="#c9a84c" stroke-width="0.5" opacity="0.3"/>
        <!-- Triangle up (fire/spirit) -->
        <polygon points="55,14 88,72 22,72" stroke="#c9a84c" stroke-width="0.9" fill="none" opacity="0.7"/>
        <!-- Triangle down (water/soul) -->
        <polygon points="55,96 22,38 88,38" stroke="#c9a84c" stroke-width="0.9" fill="none" opacity="0.7"/>
        <!-- Center cross -->
        <line x1="55" y1="45" x2="55" y2="65" stroke="#c9a84c" stroke-width="0.8" opacity="0.5"/>
        <line x1="45" y1="55" x2="65" y2="55" stroke="#c9a84c" stroke-width="0.8" opacity="0.5"/>
        <!-- Center dot -->
        <circle cx="55" cy="55" r="3" fill="#c9a84c" opacity="0.9"/>
        <!-- Cardinal points -->
        <circle cx="55" cy="3" r="1.5" fill="#c9a84c" opacity="0.6"/>
        <circle cx="107" cy="55" r="1.5" fill="#c9a84c" opacity="0.6"/>
        <circle cx="55" cy="107" r="1.5" fill="#c9a84c" opacity="0.6"/>
        <circle cx="3" cy="55" r="1.5" fill="#c9a84c" opacity="0.6"/>
      </svg>
    </div>
    <div class="year-badge">✦ &nbsp; The 22nd Year &nbsp; ✦</div>
    <h1>The Inner Temple</h1>
    <p class="hero-sub">A living guide for right thinking, sacred practice, and the great work of becoming</p>
  </div>

  <!-- NAV -->
  <div class="nav-tabs">
    <button class="tab-btn active" onclick="showTab('foundation')">Foundation</button>
    <button class="tab-btn" onclick="showTab('practice')">Daily Practice</button>
    <button class="tab-btn" onclick="showTab('principles')">Principles</button>
    <button class="tab-btn" onclick="showTab('affirmations')">Affirmations</button>
    <button class="tab-btn" onclick="showTab('alchemy')">Alchemy & Mystery</button>
  </div>

  <!-- TAB: FOUNDATION -->
  <div id="tab-foundation" class="tab-section active">

   <div class="card">
      <div class="card-header">
        <div class="card-icon">⚖️</div>
        <div class="card-title">The Three Pillars of Your Year</div>
      </div>
      <div class="pillars">
        <div class="pillar">
          <div class="pillar-icon">🕊️</div>
          <div class="pillar-name">Peace</div>
          <p>Stillness of mind, harmony in every relationship, freedom from inner war</p>
        </div>
        <div class="pillar">
          <div class="pillar-icon">🌿</div>
          <div class="pillar-name">Purity</div>
          <p>Clean thoughts, clean habits, clean energy — released from what no longer serves</p>
        </div>
        <div class="pillar">
          <div class="pillar-icon">✨</div>
          <div class="pillar-name">Prosperity</div>
          <p>Abundance of health, purpose, and provision — the natural fruit of right thinking</p>
        </div>
      </div>
    </div>

  <div class="card">
      <div class="card-header">
        <div class="card-icon">📖</div>
        <div class="card-title">Your Sacred Curriculum</div>
      </div>
      <p>These works form the architecture of your transformation. Each speaks a different dialect of the same truth:</p>
      <blockquote>
        <p>"Mind is the Master power that molds and makes, and Man is Mind, and evermore he takes the Tool of Thought, and, shaping what he wills, brings forth a thousand joys, a thousand ills."</p>
        <cite>— James Allen, As a Man Thinketh</cite>
      </blockquote>
      <ul style="list-style:none; padding:0; margin-top:16px;">
        <li style="padding:10px 0; border-bottom:1px solid rgba(201,168,76,0.07); color:#a09880; font-size:15px;"><span style="color:var(--gold); font-family:'Cinzel',serif; font-size:11px; letter-spacing:.15em; display:block; margin-bottom:3px;">THE MASTER KEY SYSTEM — Charles Haanel</span>Your primary text. 24 weekly lessons. Each lesson is a key that unlocks a deeper chamber of the mind. Read one weekly, sit with the exercise daily.</li>
        <li style="padding:10px 0; border-bottom:1px solid rgba(201,168,76,0.07); color:#a09880; font-size:15px;"><span style="color:var(--gold); font-family:'Cinzel',serif; font-size:11px; letter-spacing:.15em; display:block; margin-bottom:3px;">AS A MAN THINKETH — James Allen</span>The soul of your inner life. Read it as a mirror, not a manual. Return to it whenever your thoughts drift toward shadow.</li>
        <li style="padding:10px 0; border-bottom:1px solid rgba(201,168,76,0.07); color:#a09880; font-size:15px;"><span style="color:var(--gold); font-family:'Cinzel',serif; font-size:11px; letter-spacing:.15em; display:block; margin-bottom:3px;">THE HOLY SCRIPTURES</span>The source of the living water. Proverbs for wisdom. The Psalms for renewal. John for the mystical Christ. Romans 12 as a daily constitution.</li>
        <li style="padding:10px 0; border-bottom:1px solid rgba(201,168,76,0.07); color:#a09880; font-size:15px;"><span style="color:var(--gold); font-family:'Cinzel',serif; font-size:11px; letter-spacing:.15em; display:block; margin-bottom:3px;">THE KYBALION</span>The Hermetic principles that underlie all mystical teaching. "As above, so below." Read it alongside the Master Key System — they illuminate each other.</li>
        <li style="padding:10px 0; color:#a09880; font-size:15px;"><span style="color:var(--gold); font-family:'Cinzel',serif; font-size:11px; letter-spacing:.15em; display:block; margin-bottom:3px;">THE SERMON ON THE MOUNT — Emmet Fox</span>The greatest mystical Christian text of the 20th century. Fox reveals that the Beatitudes are a complete system of mental and spiritual law.</li>
      </ul>
    </div>

   <blockquote>
      <p>"As within, so without. As the mind, so the life. Change the inner, and the outer must follow — it has no choice."</p>
      <cite>— The Hermetic Tradition</cite>
    </blockquote>

  </div>

<!-- TAB: DAILY PRACTICE -->
  <div id="tab-practice" class="tab-section">

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🌅</div>
        <div class="card-title">The Morning Rite — Upon Waking</div>
      </div>
      <ul class="practice-list">
        <li>
          <div class="practice-num">I.</div>
          <div class="practice-content">
            <strong>The First Thought</strong>
            <span>Before your feet touch the floor, speak aloud or in your heart: <em>"I give thanks. This day is given to me. I choose peace, clarity, and right action."</em> Do not let the phone be your first voice.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">II.</div>
          <div class="practice-content">
            <strong>The Still Small Voice — 10 to 20 Minutes</strong>
            <span>This is the Haanel exercise. Sit in silence. The goal is perfect stillness — physical first, then mental. You are not emptying the mind; you are learning to observe it. Watch thoughts arise and pass. Do not grip them. Week by week, this practice will reorganize your inner world.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">III.</div>
          <div class="practice-content">
            <strong>Sacred Reading — 10 Minutes</strong>
            <span>One page of your curriculum. Read slowly. Let a single sentence become a stone you carry all day. Underline it. Write it on a notecard. Let it work on you.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">IV.</div>
          <div class="practice-content">
            <strong>The Declaration</strong>
            <span>Speak your affirmations. See them as true now, not as wishes. The Haanel system teaches that the subconscious mind cannot distinguish between a vividly imagined reality and an actual one — use this wisely.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">V.</div>
          <div class="practice-content">
            <strong>The Body as Temple</strong>
            <span>Water before anything else. Movement — even 10 minutes of deliberate breath and motion — signals to your body that today is different. Alchemy begins in the physical vessel.</span>
          </div>
        </li>
      </ul>
    </div>
 
  <div class="card">
      <div class="card-header">
        <div class="card-icon">☀️</div>
        <div class="card-title">Through the Day — The Walking Practice</div>
      </div>
      <ul class="practice-list">
        <li>
          <div class="practice-num">·</div>
          <div class="practice-content">
            <strong>The Watchman at the Gate</strong>
            <span>Haanel calls the conscious mind "the watchman at the gate." Your one job through the day: notice what you are about to let through the gate of your subconscious. Fear? Resentment? Comparison? Hold the gate. Replace with its opposite.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">·</div>
          <div class="practice-content">
            <strong>The Noon Pause</strong>
            <span>At midday, take 3 minutes. Breathe. Ask: <em>What has my thinking been today? Am I aligned?</em> No judgment — just observation. Recalibrate.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">·</div>
          <div class="practice-content">
            <strong>Harmonious Relationships</strong>
            <span>Before every interaction, set a silent intention: <em>I bring peace into this exchange.</em> The Hermetic tradition teaches that you are always broadcasting a frequency. Choose it consciously. Seek to understand before being understood.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">·</div>
          <div class="practice-content">
            <strong>On What Sets You Back</strong>
            <span>When you notice an old pattern arising — an impulse, a fear, a resentment — name it without shame: <em>There is the old way.</em> Then make a different choice. The alchemical work is in this exact moment of pausing and choosing.</span>
          </div>
        </li>
      </ul>
    </div>

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🌙</div>
        <div class="card-title">The Evening Closing — Before Sleep</div>
      </div>
      <ul class="practice-list">
        <li>
          <div class="practice-num">I.</div>
          <div class="practice-content">
            <strong>The Review Without Judgment</strong>
            <span>Sit with the day for 5 minutes. Where were you aligned? Where did you drift? Do not condemn yourself — James Allen is clear that self-condemnation is as destructive as condemning others. Observe, learn, release.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">II.</div>
          <div class="practice-content">
            <strong>Forgiveness — The Royal Key</strong>
            <span>Every night: release anyone who wronged you today, fully. Not for their sake — for yours. Emmet Fox wrote that resentment is the number one block to answered prayer. The Christ tradition makes forgiveness central for this reason. It is also Hermetic law: what you hold in mind, you hold in life.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">III.</div>
          <div class="practice-content">
            <strong>The Seed Thought</strong>
            <span>The last thought before sleep seeds the night. Plant something worthy: a scripture, an affirmation, a vision of your ideal self — healthy, at peace, purposeful. The subconscious works through the night on whatever you give it.</span>
          </div>
        </li>
      </ul>
    </div>

  </div>

  <!-- TAB: PRINCIPLES -->
  <div id="tab-principles" class="tab-section">

  <div class="card">
      <div class="card-header">
        <div class="card-icon">🔑</div>
        <div class="card-title">The Seven Hermetic Principles</div>
      </div>
      <p>From <em>The Kybalion</em>. These are not beliefs — they are observations about how reality operates. Work with them, not against them.</p>
      <div class="seven-grid">
        <div class="seven-item">
          <div class="seven-item-title">I. Mentalism</div>
          <p>All is mind. The universe is mental. Your outer life is a projection of your inner state — always, without exception.</p>
        </div>
        <div class="seven-item">
          <div class="seven-item-title">II. Correspondence</div>
          <p>As above, so below. As within, so without. Your relationships mirror your inner condition. Change yourself; your world follows.</p>
        </div>
        <div class="seven-item">
          <div class="seven-item-title">III. Vibration</div>
          <p>Nothing rests — everything moves, vibrates. Thought has frequency. Peace is a higher vibration than anxiety. You can choose your vibration.</p>
        </div>
        <div class="seven-item">
          <div class="seven-item-title">IV. Polarity</div>
          <p>Everything has its opposite — and its remedy. Fear and courage are the same thing at different ends of the pole. Transform, don't fight.</p>
        </div>
        <div class="seven-item">
          <div class="seven-item-title">V. Rhythm</div>
          <p>There are seasons to growth. When you feel you are going backward, you may be on the swing that precedes a great advance. Trust the rhythm.</p>
        </div>
        <div class="seven-item">
          <div class="seven-item-title">VI. Cause & Effect</div>
          <p>Nothing happens by chance. Every thought is a cause. Every condition in your life is an effect. You are both the author and the recipient.</p>
        </div>
      </div>
      <div class="seven-item" style="margin-top:12px;">
        <div class="seven-item-title">VII. Gender</div>
        <p>Everything contains masculine and feminine principles — action and receptivity, assertion and surrender. Right thinking requires both: the bold declaration and the quiet trust that it is being answered.</p>
      </div>
    </div>
    
   <div class="card">
      <div class="card-header">
        <div class="card-icon">✝️</div>
        <div class="card-title">The Christ Principles — Key Scriptures</div>
      </div>
      <p>Read these not as religious obligation but as living mental law:</p>
      <blockquote>
        <p>"Be ye transformed by the renewing of your mind."</p>
        <cite>— Romans 12:2</cite>
      </blockquote>
      <blockquote>
        <p>"As a man thinketh in his heart, so is he."</p>
        <cite>— Proverbs 23:7</cite>
      </blockquote>
      <blockquote>
        <p>"The kingdom of God is within you."</p>
        <cite>— Luke 17:21</cite>
      </blockquote>
      <blockquote>
        <p>"Ask, and it shall be given; seek, and ye shall find; knock, and it shall be opened."</p>
        <cite>— Matthew 7:7</cite>
      </blockquote>
      <p>The mystical tradition reads these as instructions in mental law, not metaphors. The "kingdom" is the deeper mind. The "asking" is clear, held intention. The "seeking" is the practice you are beginning.</p>
    </div>

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🧠</div>
        <div class="card-title">Haanel's Core Teaching — Know This</div>
      </div>
      <p>Charles Haanel's entire system rests on one insight: <strong style="color:var(--gold-pale);">the subconscious mind is the connection between the individual and Universal Mind.</strong></p>
      <p>The conscious mind — your thinking, reasoning self — is the gardener. The subconscious is the soil. Whatever you plant repeatedly with feeling and conviction will grow. This is why:</p>
      <ul style="list-style:none; padding:0;">
        <li style="padding:8px 0; color:#a09880; font-size:15px; border-bottom:1px solid rgba(201,168,76,0.07);">Repetition without feeling accomplishes little. <em style="color:#c8bfa8;">Add emotion to your practice.</em></li>
        <li style="padding:8px 0; color:#a09880; font-size:15px; border-bottom:1px solid rgba(201,168,76,0.07);">Negative thinking is not neutral — it plants. <em style="color:#c8bfa8;">Guard your inner speech.</em></li>
        <li style="padding:8px 0; color:#a09880; font-size:15px;">The stillness practice is not optional — it is the method. <em style="color:#c8bfa8;">The silence is where the work happens.</em></li>
      </ul>
    </div>

  </div>

  <!-- TAB: AFFIRMATIONS -->
  <div id="tab-affirmations" class="tab-section">

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🗣️</div>
        <div class="card-title">Morning Declarations — Year 22</div>
      </div>
      <p>Speak these aloud. Slowly. With conviction. They are not wishes — they are statements of identity. Your subconscious responds to what you <em>know</em>, not what you hope.</p>
      <ul class="affirmations">
        <li>I am entering my 22nd year renewed — free from every weight of the past.</li>
        <li>My mind is a sanctuary. Only thoughts of peace, faith, and possibility dwell here.</li>
        <li>I am made in the image of the Most High — whole, complete, and lacking nothing essential.</li>
        <li>Every relationship in my life is harmonious. I bring peace wherever I go.</li>
        <li>My body is strong, healthy, and full of vitality. I honor it as a sacred vessel.</li>
        <li>Prosperity in all its forms flows toward me naturally and abundantly.</li>
        <li>I release, fully and freely, every person and situation that has caused me pain. I am free.</li>
        <li>The universe — God — is working all things together for my good, even what I cannot yet see.</li>
        <li>I am becoming the truest, highest version of myself. The work is already done in spirit.</li>
        <li>I walk in purpose. My presence is a blessing. My life is the evidence of my inner work.</li>
      </ul>
    </div>

  <div class="card">
      <div class="card-header">
        <div class="card-icon">🌙</div>
        <div class="card-title">Evening Seed Thoughts — Choose One Per Night</div>
      </div>
      <ul class="affirmations">
        <li>All is well. I did enough today. Tomorrow is a new canvas.</li>
        <li>While I sleep, my mind works in harmony with infinite intelligence on my behalf.</li>
        <li>I forgive everyone. I forgive myself. The slate is clean.</li>
        <li>I see myself clearly: at peace, in health, walking in my purpose.</li>
        <li>I am grateful. Gratitude is the frequency on which good things travel.</li>
      </ul>
    </div>

  <div class="card">
      <div class="card-header">
        <div class="card-icon">⚡</div>
        <div class="card-title">The Emergency Reset — When You Drift</div>
      </div>
      <p>When you find yourself in fear, anger, comparison, or the old patterns — use this immediately:</p>
      <div style="background:rgba(201,168,76,0.06); border:1px solid rgba(201,168,76,0.15); padding:24px; margin-top:16px; text-align:center; border-radius:2px;">
        <p style="font-family:'Cinzel',serif; font-size:13px; letter-spacing:.2em; color:var(--gold); margin-bottom:16px;">BREATHE — OBSERVE — RETURN</p>
        <p style="font-style:italic; color:var(--gold-pale); font-size:18px; margin-bottom:12px;">"This is not who I am becoming."</p>
        <p style="font-style:italic; color:var(--gold-pale); font-size:18px; margin-bottom:12px;">"I choose again."</p>
        <p style="font-style:italic; color:var(--gold-pale); font-size:18px;">"Peace. Peace. Peace."</p>
      </div>
    </div>

  </div>

  <!-- TAB: ALCHEMY -->
  <div id="tab-alchemy" class="tab-section">

  <div class="card">
      <div class="card-header">
        <div class="card-icon">⚗️</div>
        <div class="card-title">The Great Work — Your Personal Alchemy</div>
      </div>
      <p>The ancient alchemists spoke of transmuting lead into gold. This was never only about metal. It was always about the human soul — transforming the base (fear, ego, reaction, shadow) into the noble (wisdom, love, mastery, light).</p>
      <p>The three stages of classical alchemy map perfectly onto your journey:</p>
      <div class="seven-grid" style="grid-template-columns: repeat(3,1fr);">
        <div class="seven-item" style="text-align:center;">
          <div class="seven-item-title" style="color:#888;">Nigredo</div>
          <div style="font-size:22px; margin:8px 0;">🌑</div>
          <p><em>The Blackening.</em> Facing what must be released. The shadow work. You are here, and it is sacred.</p>
        </div>
        <div class="seven-item" style="text-align:center;">
          <div class="seven-item-title" style="color:#c0c0c0;">Albedo</div>
          <div style="font-size:22px; margin:8px 0;">🌕</div>
          <p><em>The Whitening.</em> Purification. New patterns take hold. The inner life grows quiet and clear.</p>
        </div>
        <div class="seven-item" style="text-align:center;">
          <div class="seven-item-title">Rubedo</div>
          <div style="font-size:22px; margin:8px 0;">🔴</div>
          <p><em>The Reddening.</em> Integration and gold. Spirit, soul, and body unified. The fruit of the Work.</p>
        </div>
      </div>
    </div>

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🌊</div>
        <div class="card-title">The Four Elements as Inner Practice</div>
      </div>
      <ul class="practice-list">
        <li>
          <div class="practice-num">🔥</div>
          <div class="practice-content">
            <strong>Fire — Will & Purification</strong>
            <span>Your intentional acts of discipline. Waking early. Maintaining your practice when feeling resistance. Fire purifies. What in you needs the heat of commitment?</span>
          </div>
        </li>
        <li>
          <div class="practice-num">🌊</div>
          <div class="practice-content">
            <strong>Water — Feeling & Intuition</strong>
            <span>The Haanel system works through feeling. The Master Key teaches to combine clear thought with sincere feeling. Water also purges — let yourself feel what needs to be felt and released.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">🌬️</div>
          <div class="practice-content">
            <strong>Air — Mind & the Word</strong>
            <span>Your declarations, your inner speech, your reading. Air carries the seed. What words are you breathing into your own consciousness daily? Speak only what you wish to become real.</span>
          </div>
        </li>
        <li>
          <div class="practice-num">🌍</div>
          <div class="practice-content">
            <strong>Earth — Body & Action</strong>
            <span>Inner work must ground in physical reality. Rest, nourishment, movement, and purposeful outer action. Ideas that never become action are incomplete alchemy. Ground your vision in steps.</span>
          </div>
        </li>
      </ul>
    </div>

   <div class="card">
      <div class="card-header">
        <div class="card-icon">🌟</div>
        <div class="card-title">The Mystical Christ — The Inner Solar Logos</div>
      </div>
      <p>The deepest mystical traditions — from early Christian Gnosticism to the Rosicrucian stream — understand Christ not only as a historical figure but as a principle: <strong style="color:var(--gold-pale);">the divine light within every human being.</strong></p>
      <blockquote>
        <p>"Christ in you, the hope of glory."</p>
        <cite>— Colossians 1:27</cite>
      </blockquote>
      <p>In this reading, the spiritual path is the awakening of this inner Christ-principle — the higher self, the divine image (imago Dei) — which is also the "Universal Mind" Haanel speaks of. Your practice is the cultivation of this inner light.</p>
      <p>The mystic tradition unites all your sources: Haanel's Universal Mind, the Hermetic All, James Allen's "Thought-Power," and the Christ within are all pointing at the same reality — the divine intelligence available to the stilled and aligned human mind.</p>
    </div>

   <blockquote>
      <p>"The secret of the universe, the very heart of it, is not out there somewhere beyond the stars. It is within — within the consciousness of man. Seek it there."</p>
      <cite>— The Ageless Wisdom</cite>
    </blockquote>

  </div>

  <footer>
    <p><span class="gold-text">✦</span> &nbsp; Year 22 &nbsp; · &nbsp; The Inner Temple &nbsp; · &nbsp; The Work Begins Within &nbsp; <span class="gold-text">✦</span></p>
    <p style="margin-top:12px; font-size:10px;">"Ora et Labora" — Pray and Work</p>
  </footer>

</div>

<script>
  function showTab(id) {
    document.querySelectorAll('.tab-section').forEach(el => el.classList.remove('active'));
    document.querySelectorAll('.tab-btn').forEach(el => el.classList.remove('active'));
    document.getElementById('tab-' + id).classList.add('active');
    event.target.classList.add('active');
  }
</script>
</body>
</html>
