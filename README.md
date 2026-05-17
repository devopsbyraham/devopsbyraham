<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Raham Shaik — DevOps & Cloud-Native Trainer | Kubestronaut | AWS | Terraform</title>
<meta name="description" content="12,000+ students trained. 100+ certified. Students earning 24–30 LPA. Expert DevOps, Kubernetes & Cloud trainer.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,800;0,900;1,700&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080b10;
    --bg2: #0d1117;
    --surface: #141c26;
    --surface2: #1a2535;
    --border: rgba(255,255,255,0.07);
    --border2: rgba(255,255,255,0.12);
    --text: #e8edf5;
    --text2: #8a96a8;
    --text3: #5a6478;
    --accent: #f97316;
    --accent2: #ea580c;
    --accent3: #fb923c;
    --accent-glow: rgba(249,115,22,0.15);
    --green: #22c55e;
    --green-dim: rgba(34,197,94,0.12);
    --green-border: rgba(34,197,94,0.22);
    --font-display: 'Playfair Display', serif;
    --font-body: 'Inter', sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { background: var(--bg); color: var(--text); font-family: var(--font-body); font-size: 16px; line-height: 1.7; overflow-x: hidden; }
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: linear-gradient(rgba(255,255,255,0.015) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.015) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none; z-index: 0;
  }

  /* ── SALARY TICKER BAR ── */
  .salary-ticker-bar {
    background: linear-gradient(90deg, #040d03, #071206, #040d03);
    border-bottom: 1px solid rgba(34,197,94,0.2);
    padding: 0.5rem 0;
    overflow: hidden;
    position: relative;
    z-index: 101;
  }
  .salary-ticker-bar::before, .salary-ticker-bar::after {
    content: ''; position: absolute; top: 0; bottom: 0; width: 100px; z-index: 2; pointer-events: none;
  }
  .salary-ticker-bar::before { left: 0; background: linear-gradient(90deg, #040d03, transparent); }
  .salary-ticker-bar::after  { right: 0; background: linear-gradient(-90deg, #040d03, transparent); }
  .salary-ticker-inner { display: flex; gap: 3.5rem; animation: s-scroll 30s linear infinite; white-space: nowrap; width: max-content; }
  @keyframes s-scroll { from { transform: translateX(0); } to { transform: translateX(-50%); } }
  .s-item { font-family: var(--font-mono); font-size: 0.72rem; color: rgba(34,197,94,0.8); letter-spacing: 0.04em; display: flex; align-items: center; gap: 0.45rem; }
  .s-item strong { color: var(--green); font-weight: 600; }
  .s-item .sep { color: rgba(34,197,94,0.25); }

  /* ── NAV ── */
  nav {
    position: fixed; top: 33px; left: 0; right: 0; z-index: 100;
    padding: 0 5vw; height: 64px;
    display: flex; align-items: center; justify-content: space-between;
    background: rgba(8,11,16,0.9); backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo { font-family: var(--font-display); font-weight: 800; font-size: 1.1rem; letter-spacing: -0.02em; color: var(--text); text-decoration: none; }
  .nav-logo span { color: var(--accent); }
  .nav-links { display: flex; gap: 1.5rem; list-style: none; }
  .nav-links a { font-family: var(--font-mono); font-size: 0.68rem; color: var(--text2); text-decoration: none; letter-spacing: 0.05em; text-transform: uppercase; transition: color 0.2s; }
  .nav-links a:hover { color: var(--accent); }
  .nav-cta { font-family: var(--font-mono); font-size: 0.73rem; font-weight: 500; color: var(--accent); text-decoration: none; border: 1px solid rgba(249,115,22,0.4); padding: 0.4rem 1rem; border-radius: 4px; transition: background 0.2s; letter-spacing: 0.05em; }
  .nav-cta:hover { background: rgba(249,115,22,0.1); }
  .nav-toggle { display: none; flex-direction: column; gap: 5px; cursor: pointer; padding: 4px; background: none; border: none; }
  .nav-toggle span { display: block; width: 22px; height: 2px; background: var(--text2); border-radius: 2px; }

  /* ── HERO ── */
  #hero { min-height: 100vh; display: flex; align-items: center; padding: 160px 5vw 80px; position: relative; overflow: hidden; }
  .hero-orb { position: absolute; border-radius: 50%; filter: blur(80px); pointer-events: none; }
  .hero-orb-1 { width: 600px; height: 600px; background: radial-gradient(circle, rgba(249,115,22,0.12) 0%, transparent 70%); top: -150px; right: -100px; animation: orb-float 8s ease-in-out infinite; }
  .hero-orb-2 { width: 400px; height: 400px; background: radial-gradient(circle, rgba(249,115,22,0.06) 0%, transparent 70%); bottom: 50px; left: -80px; animation: orb-float 10s ease-in-out infinite reverse; }
  @keyframes orb-float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-30px); } }
  .hero-inner { max-width: 1100px; width: 100%; position: relative; z-index: 1; }
  .hero-badge { display: inline-flex; align-items: center; gap: 0.5rem; font-family: var(--font-mono); font-size: 0.72rem; color: var(--accent); letter-spacing: 0.1em; text-transform: uppercase; border: 1px solid rgba(249,115,22,0.3); background: rgba(249,115,22,0.06); padding: 0.35rem 0.85rem; border-radius: 100px; margin-bottom: 2rem; animation: fade-up 0.6s ease both; }
  .hero-badge::before { content: ''; width: 6px; height: 6px; background: var(--accent); border-radius: 50%; animation: pulse-dot 2s ease-in-out infinite; }
  @keyframes pulse-dot { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.4; transform: scale(0.8); } }
  .hero-name { font-family: var(--font-display); font-weight: 800; font-size: clamp(3rem, 7vw, 6rem); line-height: 1.0; letter-spacing: -0.03em; color: var(--text); animation: fade-up 0.6s 0.1s ease both; }
  .hero-title { font-family: var(--font-mono); font-size: clamp(0.8rem, 1.3vw, 0.96rem); color: var(--text2); font-weight: 300; letter-spacing: 0.03em; margin: 1.2rem 0 1.8rem; animation: fade-up 0.6s 0.2s ease both; line-height: 1.9; }
  .hero-title strong { color: var(--text); font-weight: 500; }
  .hero-desc { font-size: 1.05rem; color: var(--text2); max-width: 650px; line-height: 1.9; margin-bottom: 2rem; animation: fade-up 0.6s 0.3s ease both; }
  .hero-cloud-chips { display: flex; gap: 0.5rem; flex-wrap: wrap; margin-bottom: 2.5rem; animation: fade-up 0.6s 0.35s ease both; }
  .cloud-chip { display: inline-flex; align-items: center; gap: 0.4rem; font-family: var(--font-mono); font-size: 0.68rem; font-weight: 500; padding: 0.28rem 0.75rem; border-radius: 100px; border: 1px solid var(--border2); background: var(--surface); color: var(--text2); letter-spacing: 0.04em; transition: border-color 0.2s, color 0.2s; }
  .cloud-chip:hover { border-color: var(--accent); color: var(--accent); }
  .chip-dot { width: 5px; height: 5px; border-radius: 50%; background: var(--accent); opacity: 0.7; flex-shrink: 0; }
  .hero-stats { display: flex; gap: 2.5rem; margin-bottom: 3rem; animation: fade-up 0.6s 0.4s ease both; flex-wrap: wrap; }
  .hero-stat-num { font-family: var(--font-display); font-size: 2.2rem; font-weight: 800; line-height: 1; letter-spacing: -0.03em; color: var(--text); }
  .hero-stat-num span { color: var(--accent); }
  .hero-stat-num.g { color: var(--green); }
  .hero-stat-label { font-family: var(--font-mono); font-size: 0.68rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.08em; margin-top: 0.3rem; }
  .hero-ctas { display: flex; gap: 1rem; align-items: center; flex-wrap: wrap; animation: fade-up 0.6s 0.5s ease both; }
  .btn-primary { font-family: var(--font-mono); font-size: 0.82rem; font-weight: 500; letter-spacing: 0.04em; color: var(--bg); background: var(--accent); padding: 0.85rem 2rem; border-radius: 6px; text-decoration: none; transition: transform 0.2s, box-shadow 0.2s; display: inline-flex; align-items: center; gap: 0.5rem; }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(249,115,22,0.3); }
  .btn-secondary { font-family: var(--font-mono); font-size: 0.82rem; color: var(--text2); background: transparent; padding: 0.85rem 2rem; border-radius: 6px; text-decoration: none; border: 1px solid var(--border2); transition: color 0.2s, border-color 0.2s; display: inline-flex; align-items: center; gap: 0.5rem; }
  .btn-secondary:hover { color: var(--text); border-color: rgba(255,255,255,0.25); }
  .btn-green { font-family: var(--font-mono); font-size: 0.82rem; font-weight: 500; letter-spacing: 0.04em; color: #080b10; background: var(--green); padding: 0.85rem 2rem; border-radius: 6px; text-decoration: none; transition: transform 0.2s, box-shadow 0.2s; display: inline-flex; align-items: center; gap: 0.5rem; }
  .btn-green:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(34,197,94,0.3); }
  .hero-certs { position: absolute; right: 0; top: 50%; transform: translateY(-50%); display: flex; flex-direction: column; gap: 0.75rem; animation: fade-left 0.8s 0.6s ease both; }
  @keyframes fade-left { from { opacity: 0; transform: translateY(-50%) translateX(30px); } to { opacity: 1; transform: translateY(-50%) translateX(0); } }
  @keyframes fade-up { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
  .cert-badge { display: flex; align-items: center; gap: 0.75rem; background: var(--surface); border: 1px solid var(--border2); border-radius: 8px; padding: 0.7rem 1rem; min-width: 190px; transition: border-color 0.2s, transform 0.2s; }
  .cert-badge:hover { border-color: var(--accent); transform: translateX(-4px); }
  .cert-icon { width: 32px; height: 32px; background: var(--accent-glow); border-radius: 6px; display: flex; align-items: center; justify-content: center; font-family: var(--font-display); font-size: 0.55rem; font-weight: 800; color: var(--accent); flex-shrink: 0; }
  .cert-name { font-family: var(--font-mono); font-size: 0.72rem; font-weight: 500; color: var(--text); line-height: 1.2; }
  .cert-org { font-family: var(--font-mono); font-size: 0.63rem; color: var(--text3); margin-top: 0.1rem; }

  /* ── SECTION COMMON ── */
  section { padding: 100px 5vw; position: relative; z-index: 1; }
  .section-inner { max-width: 1100px; margin: 0 auto; }
  .section-tag { font-family: var(--font-mono); font-size: 0.7rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.12em; margin-bottom: 0.75rem; }
  .section-title { font-family: var(--font-display); font-size: clamp(2rem, 4vw, 3rem); font-weight: 800; line-height: 1.1; letter-spacing: -0.03em; color: var(--text); margin-bottom: 1rem; }
  .section-sub { font-size: 1rem; color: var(--text2); max-width: 560px; line-height: 1.8; margin-bottom: 3rem; }

  /* ── IMPACT BAR ── */
  #impact { background: var(--bg2); border-top: 1px solid var(--border); border-bottom: 1px solid var(--border); padding: 60px 5vw; }
  .impact-grid { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: repeat(5, 1fr); gap: 1px; background: var(--border); border: 1px solid var(--border); border-radius: 12px; overflow: hidden; }
  .impact-item { background: var(--bg2); padding: 2.5rem 1.5rem; text-align: center; transition: background 0.2s; }
  .impact-item:hover { background: var(--surface); }
  .impact-num { font-family: var(--font-display); font-size: 2.7rem; font-weight: 800; letter-spacing: -0.04em; color: var(--text); line-height: 1; margin-bottom: 0.5rem; }
  .impact-num span { color: var(--accent); }
  .impact-num.gn { color: var(--green); }
  .impact-label { font-family: var(--font-mono); font-size: 0.66rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.1em; }

  /* ── ABOUT ── */
  #about .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; align-items: center; }
  .about-terminal { background: var(--surface); border: 1px solid var(--border2); border-radius: 12px; overflow: hidden; font-family: var(--font-mono); }
  .terminal-bar { background: var(--surface2); border-bottom: 1px solid var(--border); padding: 0.75rem 1rem; display: flex; align-items: center; gap: 0.4rem; }
  .terminal-dot { width: 10px; height: 10px; border-radius: 50%; }
  .terminal-dot:nth-child(1) { background: #ff5f57; }
  .terminal-dot:nth-child(2) { background: #febc2e; }
  .terminal-dot:nth-child(3) { background: #28c840; }
  .terminal-title { font-size: 0.7rem; color: var(--text3); margin-left: 0.5rem; letter-spacing: 0.05em; }
  .terminal-body { padding: 1.5rem; font-size: 0.78rem; line-height: 2; }
  .t-prompt { color: var(--accent); } .t-cmd { color: var(--text); } .t-key { color: #c678dd; } .t-val { color: #98c379; } .t-string { color: #e5c07b; } .t-number { color: #61afef; }
  .t-cursor { display: inline-block; width: 8px; height: 14px; background: var(--accent); margin-left: 2px; animation: blink 1s step-end infinite; vertical-align: -2px; }
  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
  .about-text p { color: var(--text2); margin-bottom: 1.2rem; font-size: 1rem; line-height: 1.9; }
  .about-text p strong { color: var(--text); font-weight: 500; }
  .about-highlights { display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; margin-top: 2rem; }
  .highlight-item { display: flex; align-items: flex-start; gap: 0.6rem; font-size: 0.88rem; color: var(--text2); }
  .highlight-item::before { content: '▸'; color: var(--accent); font-size: 0.8rem; flex-shrink: 0; margin-top: 0.2rem; }

  /* ── TECHNICAL EXPERTISE ── */
  #expertise { background: var(--bg2); border-top: 1px solid var(--border); }
  .cloud-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; margin-bottom: 1.25rem; }
  .cloud-card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 1.5rem 1.4rem; display: flex; align-items: center; gap: 1.2rem; transition: border-color 0.3s, transform 0.25s; }
  .cloud-card:hover { border-color: rgba(249,115,22,0.4); transform: translateY(-3px); }
  .cloud-logo { width: 46px; height: 46px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1.5rem; flex-shrink: 0; background: var(--surface2); }
  .cloud-name { font-family: var(--font-display); font-size: 1.05rem; font-weight: 700; color: var(--text); letter-spacing: -0.01em; }
  .cloud-desc { font-family: var(--font-mono); font-size: 0.63rem; color: var(--text3); margin-top: 0.2rem; letter-spacing: 0.03em; line-height: 1.6; }
  .expertise-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.25rem; }
  .expertise-card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 1.6rem 1.4rem; transition: border-color 0.3s, transform 0.25s; position: relative; overflow: hidden; }
  .expertise-card:hover { border-color: rgba(249,115,22,0.4); transform: translateY(-4px); }
  .expertise-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--accent), transparent); opacity: 0; transition: opacity 0.3s; }
  .expertise-card:hover::before { opacity: 1; }
  .expertise-card.span2 { grid-column: span 2; background: linear-gradient(135deg, rgba(249,115,22,0.03) 0%, var(--surface) 70%); }
  .ex-icon { font-size: 1.4rem; margin-bottom: 0.9rem; line-height: 1; }
  .ex-label { font-family: var(--font-mono); font-size: 0.62rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.12em; margin-bottom: 0.45rem; }
  .ex-title { font-family: var(--font-display); font-size: 0.95rem; font-weight: 700; color: var(--text); margin-bottom: 0.85rem; letter-spacing: -0.01em; line-height: 1.3; }
  .ex-pills { display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .ex-pill { font-family: var(--font-mono); font-size: 0.63rem; color: var(--text2); background: var(--bg2); border: 1px solid var(--border2); padding: 0.18rem 0.55rem; border-radius: 4px; letter-spacing: 0.03em; transition: color 0.2s, border-color 0.2s; }
  .ex-pill.hi { color: var(--accent); border-color: rgba(249,115,22,0.35); background: rgba(249,115,22,0.05); }
  .expertise-card:hover .ex-pill { border-color: rgba(249,115,22,0.18); }

  /* ── CERTIFICATIONS ── */
  .cert-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
  .cert-card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 2rem; position: relative; overflow: hidden; transition: border-color 0.3s, transform 0.3s; }
  .cert-card:hover { border-color: var(--accent); transform: translateY(-4px); }
  .cert-card::after { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--accent), transparent); opacity: 0; transition: opacity 0.3s; }
  .cert-card:hover::after { opacity: 1; }
  .cert-card-abbr { font-family: var(--font-display); font-size: 1.6rem; font-weight: 800; color: var(--accent); letter-spacing: -0.02em; margin-bottom: 0.5rem; }
  .cert-card-name { font-size: 0.9rem; font-weight: 500; color: var(--text); margin-bottom: 0.5rem; }
  .cert-card-org { font-family: var(--font-mono); font-size: 0.7rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 1rem; }
  .cert-card-desc { font-size: 0.85rem; color: var(--text2); line-height: 1.7; }
  .cert-view-btn { display: inline-flex; align-items: center; gap: 0.4rem; margin-top: 1.2rem; font-family: var(--font-mono); font-size: 0.72rem; font-weight: 500; color: var(--accent); text-decoration: none; border: 1px solid rgba(249,115,22,0.35); background: rgba(249,115,22,0.06); padding: 0.45rem 1rem; border-radius: 5px; letter-spacing: 0.04em; transition: background 0.2s, border-color 0.2s, transform 0.2s; }
  .cert-view-btn:hover { background: rgba(249,115,22,0.14); border-color: var(--accent); transform: translateX(3px); }
  .cert-level { position: absolute; top: 1.2rem; right: 1.2rem; font-family: var(--font-mono); font-size: 0.62rem; color: var(--accent); border: 1px solid rgba(249,115,22,0.3); background: rgba(249,115,22,0.06); padding: 0.2rem 0.6rem; border-radius: 100px; text-transform: uppercase; letter-spacing: 0.06em; }

  /* ── FLAGSHIP TRAINING ── */
  #training { background: var(--bg2); border-top: 1px solid var(--border); }
  .flagship-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .flagship-card { background: var(--surface); border: 1px solid var(--border); border-radius: 14px; padding: 2.2rem; position: relative; overflow: hidden; transition: border-color 0.3s, transform 0.25s; }
  .flagship-card:hover { border-color: rgba(249,115,22,0.4); transform: translateY(-4px); }
  .flagship-card.hero-card { grid-column: span 2; background: linear-gradient(135deg, #110d00 0%, #141c26 60%); border-color: rgba(249,115,22,0.4); }
  .flagship-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, var(--accent), var(--accent3), transparent); opacity: 0; transition: opacity 0.3s; }
  .flagship-card:hover::before, .flagship-card.hero-card::before { opacity: 1; }
  .f-badge { display: inline-block; font-family: var(--font-mono); font-size: 0.6rem; letter-spacing: 0.1em; text-transform: uppercase; color: #080b10; background: var(--accent2); padding: 0.2rem 0.7rem; border-radius: 4px; margin-bottom: 1.2rem; }
  .f-badge.green { background: var(--green); }
  .f-badge.blue { background: #0ea5e9; }
  .f-badge.purple { background: #7c3aed; }
  .f-icon { width: 46px; height: 46px; border-radius: 12px; background: rgba(249,115,22,0.1); border: 1px solid rgba(249,115,22,0.2); display: flex; align-items: center; justify-content: center; font-size: 1.3rem; margin-bottom: 1.2rem; }
  .f-title { font-family: var(--font-display); font-size: 1.2rem; font-weight: 700; color: var(--text); margin-bottom: 0.75rem; letter-spacing: -0.02em; line-height: 1.3; }
  .f-desc { font-size: 0.9rem; color: var(--text2); line-height: 1.85; margin-bottom: 1.3rem; }
  .f-bullets { list-style: none; margin-bottom: 1.4rem; display: flex; flex-direction: column; gap: 0.5rem; }
  .f-bullets li { display: flex; align-items: flex-start; gap: 0.6rem; font-size: 0.85rem; color: var(--text2); line-height: 1.65; }
  .f-bullets li::before { content: '✦'; color: var(--accent); font-size: 0.58rem; flex-shrink: 0; margin-top: 0.3rem; }
  .f-stat-row { display: flex; gap: 1.5rem; border-top: 1px solid var(--border); padding-top: 1.2rem; flex-wrap: wrap; }
  .f-stat-num { font-family: var(--font-display); font-size: 1.4rem; font-weight: 800; color: var(--accent); letter-spacing: -0.02em; line-height: 1; }
  .f-stat-num.g { color: var(--green); }
  .f-stat-label { font-family: var(--font-mono); font-size: 0.62rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.08em; margin-top: 0.2rem; }
  .f-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 1rem; }
  .f-tag { font-family: var(--font-mono); font-size: 0.64rem; color: var(--text3); background: var(--bg); border: 1px solid var(--border); padding: 0.18rem 0.55rem; border-radius: 4px; letter-spacing: 0.03em; }

  /* ── SOCIAL PROOF ── */
  .proof-header { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: start; margin-bottom: 4rem; }
  .big-stat { background: var(--surface); border: 1px solid rgba(249,115,22,0.2); border-radius: 16px; padding: 2.5rem; position: relative; overflow: hidden; }
  .big-stat::before { content: ''; position: absolute; inset: 0; background: radial-gradient(circle at top left, rgba(249,115,22,0.06) 0%, transparent 60%); pointer-events: none; }
  .big-stat-num { font-family: var(--font-display); font-size: 5rem; font-weight: 800; line-height: 1; letter-spacing: -0.04em; color: var(--accent); margin-bottom: 0.5rem; }
  .big-stat-label { font-size: 1.1rem; font-weight: 500; color: var(--text); margin-bottom: 0.5rem; }
  .big-stat-sub { font-size: 0.88rem; color: var(--text2); line-height: 1.7; }
  .proof-breakdown { display: flex; flex-direction: column; gap: 1rem; }
  .proof-bar-top { display: flex; justify-content: space-between; margin-bottom: 0.4rem; }
  .proof-bar-label { font-family: var(--font-mono); font-size: 0.78rem; color: var(--text2); }
  .proof-bar-val { font-family: var(--font-mono); font-size: 0.78rem; color: var(--accent); font-weight: 500; }
  .proof-bar-track { height: 4px; background: var(--border); border-radius: 2px; overflow: hidden; }
  .proof-bar-fill { height: 100%; background: var(--accent); border-radius: 2px; transform-origin: left; animation: bar-grow 1s ease both; }
  @keyframes bar-grow { from { transform: scaleX(0); } to { transform: scaleX(1); } }
  .testimonials-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
  .testimonial-card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 1.75rem; transition: border-color 0.2s; display: flex; flex-direction: column; }
  .testimonial-card:hover { border-color: var(--border2); }
  .testimonial-quote { font-size: 0.9rem; color: var(--text2); line-height: 1.8; margin-bottom: 1.5rem; flex: 1; }
  .testimonial-quote::before { content: '"'; font-family: var(--font-display); font-size: 2rem; color: var(--accent); line-height: 0; vertical-align: -0.5rem; margin-right: 0.2rem; }
  .testimonial-author { display: flex; align-items: center; gap: 0.75rem; border-top: 1px solid var(--border); padding-top: 1rem; }
  .t-avatar { width: 36px; height: 36px; border-radius: 50%; background: var(--surface2); display: flex; align-items: center; justify-content: center; font-family: var(--font-display); font-size: 0.75rem; font-weight: 700; color: var(--accent); flex-shrink: 0; }
  .t-author-name { font-size: 0.85rem; font-weight: 500; color: var(--text); line-height: 1.2; }
  .t-author-role { font-family: var(--font-mono); font-size: 0.68rem; color: var(--text3); margin-top: 0.15rem; }
  .t-cert-badge { margin-left: auto; font-family: var(--font-mono); font-size: 0.62rem; color: var(--accent); border: 1px solid rgba(249,115,22,0.3); background: rgba(249,115,22,0.06); padding: 0.2rem 0.5rem; border-radius: 4px; white-space: nowrap; }
  .batch-ticker { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 1.5rem 2rem; margin-top: 2.5rem; display: flex; align-items: center; gap: 2rem; overflow: hidden; }
  .batch-ticker-label { font-family: var(--font-mono); font-size: 0.68rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.1em; flex-shrink: 0; white-space: nowrap; border-right: 1px solid var(--border2); padding-right: 2rem; }
  .batch-ticker-scroll { display: flex; gap: 3rem; animation: ticker 30s linear infinite; white-space: nowrap; }
  @keyframes ticker { from { transform: translateX(0); } to { transform: translateX(-50%); } }
  .batch-item { font-family: var(--font-mono); font-size: 0.78rem; color: var(--text2); }
  .batch-item strong { color: var(--accent); font-weight: 500; }

  /* ── SALARY TRANSFORMATION ── */
  #salary {
    background: linear-gradient(180deg, #04090303 0%, #080b10 100%);
    border-top: 1px solid var(--green-border);
    border-bottom: 1px solid var(--green-border);
    position: relative; overflow: hidden;
  }
  #salary::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 15% 50%, rgba(34,197,94,0.06) 0%, transparent 55%), radial-gradient(ellipse at 85% 20%, rgba(34,197,94,0.04) 0%, transparent 45%);
    pointer-events: none;
  }
  .salary-header-block { text-align: center; margin-bottom: 4rem; }
  .salary-header-block .section-tag { color: var(--green); display: block; text-align: center; margin-bottom: 0.75rem; }
  .salary-header-block .section-title { margin: 0 auto 1rem; }
  .salary-header-block .section-sub { margin: 0 auto 0; text-align: center; }
  .salary-mega-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-bottom: 3.5rem; }
  .salary-mega-card { background: var(--green-dim); border: 1px solid var(--green-border); border-radius: 16px; padding: 2.5rem 2rem; text-align: center; position: relative; overflow: hidden; transition: border-color 0.3s, transform 0.25s; }
  .salary-mega-card:hover { border-color: rgba(34,197,94,0.45); transform: translateY(-4px); }
  .salary-mega-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, transparent, var(--green), transparent); }
  .salary-mega-num { font-family: var(--font-display); font-size: 3.5rem; font-weight: 900; color: var(--green); letter-spacing: -0.04em; line-height: 1; margin-bottom: 0.5rem; }
  .salary-mega-label { font-size: 0.95rem; font-weight: 500; color: var(--text); margin-bottom: 0.4rem; }
  .salary-mega-sub { font-family: var(--font-mono); font-size: 0.67rem; color: var(--text3); letter-spacing: 0.04em; }
  .success-stories-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; margin-bottom: 2.5rem; }
  .success-card { background: var(--surface); border: 1px solid var(--green-border); border-radius: 14px; padding: 1.75rem; position: relative; overflow: hidden; transition: border-color 0.3s, transform 0.25s; }
  .success-card:hover { border-color: rgba(34,197,94,0.4); transform: translateY(-4px); }
  .success-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--green), transparent); opacity: 0.7; }
  .s-avatar { width: 48px; height: 48px; border-radius: 50%; background: var(--green-dim); border: 2px solid var(--green-border); display: flex; align-items: center; justify-content: center; font-family: var(--font-display); font-size: 1rem; font-weight: 800; color: var(--green); margin-bottom: 1rem; }
  .s-name { font-family: var(--font-display); font-size: 1.1rem; font-weight: 700; color: var(--text); letter-spacing: -0.01em; margin-bottom: 0.2rem; }
  .s-cert { font-family: var(--font-mono); font-size: 0.63rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 1.1rem; }
  .s-salary-row { display: flex; align-items: center; gap: 0.75rem; margin-bottom: 0.8rem; }
  .s-before { font-family: var(--font-mono); font-size: 0.8rem; color: var(--text3); text-decoration: line-through; }
  .s-arrow { color: var(--green); font-size: 1rem; flex-shrink: 0; }
  .s-after { font-family: var(--font-display); font-size: 1.6rem; font-weight: 800; color: var(--green); letter-spacing: -0.03em; line-height: 1; }
  .s-hike-badge { display: inline-flex; align-items: center; gap: 0.3rem; font-family: var(--font-mono); font-size: 0.68rem; font-weight: 600; color: var(--green); background: var(--green-dim); border: 1px solid var(--green-border); padding: 0.22rem 0.65rem; border-radius: 100px; letter-spacing: 0.04em; }
  .s-desc { font-size: 0.82rem; color: var(--text2); line-height: 1.75; margin-top: 0.85rem; }
  .hike-callout { background: linear-gradient(135deg, rgba(34,197,94,0.07) 0%, rgba(34,197,94,0.02) 60%); border: 1px solid rgba(34,197,94,0.28); border-radius: 16px; padding: 2.5rem 3rem; display: flex; align-items: center; gap: 3rem; flex-wrap: wrap; position: relative; overflow: hidden; }
  .hike-callout::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, var(--green), rgba(34,197,94,0.25), transparent); }
  .hike-callout-label { font-family: var(--font-mono); font-size: 0.65rem; color: var(--green); text-transform: uppercase; letter-spacing: 0.12em; margin-bottom: 0.4rem; }
  .hike-callout-num { font-family: var(--font-display); font-size: 5rem; font-weight: 900; color: var(--green); letter-spacing: -0.04em; line-height: 1; }
  .hike-callout-story { font-size: 0.95rem; color: var(--text2); line-height: 1.85; max-width: 500px; }
  .hike-callout-story strong { color: var(--text); }

  /* ── WHY CHOOSE ME ── */
  #why { background: var(--bg2); border-top: 1px solid var(--border); }
  .why-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 1.25rem; }
  .why-card { background: var(--surface); border: 1px solid var(--border); border-radius: 12px; padding: 1.5rem 1.25rem; transition: border-color 0.25s, transform 0.25s; position: relative; overflow: hidden; }
  .why-card:hover { border-color: rgba(249,115,22,0.45); transform: translateY(-4px); }
  .why-card:hover::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: var(--accent); }
  .why-icon { font-size: 1.6rem; margin-bottom: 0.85rem; line-height: 1; }
  .why-title { font-family: var(--font-display); font-size: 0.95rem; font-weight: 700; color: var(--text); margin-bottom: 0.6rem; line-height: 1.3; letter-spacing: -0.01em; }
  .why-desc { font-size: 0.82rem; color: var(--text2); line-height: 1.75; }

  /* ── CONTACT ── */
  .contact-grid { display: grid; grid-template-columns: 1fr 1.2fr; gap: 5rem; align-items: start; }
  .contact-info-title { font-family: var(--font-display); font-size: 2.5rem; font-weight: 800; letter-spacing: -0.03em; color: var(--text); line-height: 1.15; margin-bottom: 1.2rem; }
  .contact-info-title span { color: var(--accent); }
  .contact-info-sub { font-size: 0.95rem; color: var(--text2); line-height: 1.8; margin-bottom: 2.5rem; }
  .contact-channels { display: flex; flex-direction: column; gap: 1rem; }
  .contact-channel { display: flex; align-items: center; gap: 1rem; text-decoration: none; padding: 0.85rem 1.2rem; background: var(--surface); border: 1px solid var(--border); border-radius: 8px; transition: border-color 0.2s, transform 0.2s; }
  .contact-channel:hover { border-color: var(--accent); transform: translateX(4px); }
  .ch-icon { width: 36px; height: 36px; background: var(--accent-glow); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 1rem; flex-shrink: 0; }
  .ch-label { font-family: var(--font-mono); font-size: 0.7rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.08em; }
  .ch-value { font-size: 0.9rem; color: var(--text); font-weight: 500; }
  .ch-arrow { margin-left: auto; color: var(--text3); font-size: 0.8rem; }
  .contact-form-wrapper { background: var(--surface); border: 1px solid var(--border2); border-radius: 16px; padding: 2.5rem; }
  .form-title { font-family: var(--font-display); font-size: 1.3rem; font-weight: 700; color: var(--text); margin-bottom: 0.4rem; letter-spacing: -0.02em; }
  .form-sub { font-size: 0.85rem; color: var(--text3); margin-bottom: 2rem; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .form-group { margin-bottom: 1rem; }
  label { display: block; font-family: var(--font-mono); font-size: 0.7rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.4rem; }
  input[type="text"], input[type="email"], select, textarea { width: 100%; background: var(--bg); border: 1px solid var(--border2); border-radius: 6px; color: var(--text); font-family: var(--font-body); font-size: 0.9rem; padding: 0.7rem 1rem; outline: none; transition: border-color 0.2s; -webkit-appearance: none; }
  input:focus, select:focus, textarea:focus { border-color: var(--accent); }
  input::placeholder, textarea::placeholder { color: var(--text3); }
  select { cursor: pointer; background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' fill='%235a6478' viewBox='0 0 16 16'%3E%3Cpath d='M7.247 11.14L2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z'/%3E%3C/svg%3E"); background-repeat: no-repeat; background-position: right 1rem center; padding-right: 2.5rem; }
  textarea { resize: vertical; min-height: 110px; line-height: 1.7; }
  .form-submit { width: 100%; background: var(--accent); color: var(--bg); border: none; border-radius: 6px; font-family: var(--font-mono); font-size: 0.85rem; font-weight: 500; letter-spacing: 0.04em; padding: 0.9rem; cursor: pointer; margin-top: 0.5rem; transition: transform 0.2s, box-shadow 0.2s; }
  .form-submit:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(249,115,22,0.3); }
  .form-note { font-family: var(--font-mono); font-size: 0.65rem; color: var(--text3); text-align: center; margin-top: 0.75rem; letter-spacing: 0.03em; }
  .form-success { display: none; text-align: center; padding: 3rem 1rem; }
  .form-success-icon { font-size: 3rem; margin-bottom: 1rem; }
  .form-success-title { font-family: var(--font-display); font-size: 1.5rem; font-weight: 700; color: var(--text); margin-bottom: 0.5rem; }
  .form-success-sub { font-size: 0.9rem; color: var(--text2); }

  /* ── FOOTER ── */
  footer { background: var(--bg2); border-top: 1px solid var(--border); padding: 3rem 5vw; position: relative; z-index: 1; }
  .footer-inner { max-width: 1100px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1.5rem; }
  .footer-logo { font-family: var(--font-display); font-weight: 800; font-size: 1.1rem; letter-spacing: -0.02em; color: var(--text); }
  .footer-logo span { color: var(--accent); }
  .footer-links { display: flex; gap: 1.75rem; list-style: none; }
  .footer-links a { font-family: var(--font-mono); font-size: 0.7rem; color: var(--text3); text-decoration: none; letter-spacing: 0.05em; text-transform: uppercase; transition: color 0.2s; }
  .footer-links a:hover { color: var(--text2); }
  .footer-copy { font-family: var(--font-mono); font-size: 0.68rem; color: var(--text3); letter-spacing: 0.04em; }

  /* ── SCROLL ANIMATIONS ── */
  .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }

  /* ── RESPONSIVE ── */
  @media (max-width: 1100px) {
    .why-grid { grid-template-columns: repeat(3, 1fr); }
    .expertise-grid { grid-template-columns: repeat(2, 1fr); }
    .expertise-card.span2 { grid-column: span 1; }
    .cloud-row { grid-template-columns: 1fr; }
    .impact-grid { grid-template-columns: repeat(3, 1fr); }
  }
  @media (max-width: 1024px) {
    .hero-certs { display: none; }
    #about .about-grid { grid-template-columns: 1fr; gap: 3rem; }
    .cert-grid { grid-template-columns: repeat(2, 1fr); }
    .proof-header { grid-template-columns: 1fr; gap: 2rem; }
    .flagship-grid { grid-template-columns: 1fr; }
    .flagship-card.hero-card { grid-column: span 1; }
    .salary-mega-stats { grid-template-columns: 1fr 1fr; }
    .success-stories-grid { grid-template-columns: 1fr 1fr; }
    .contact-grid { grid-template-columns: 1fr; gap: 3rem; }
  }
  @media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .nav-toggle { display: flex; }
    .hero-stats { gap: 1.5rem; }
    .testimonials-grid { grid-template-columns: 1fr; }
    .cert-grid { grid-template-columns: 1fr; }
    .form-row { grid-template-columns: 1fr; }
    .why-grid { grid-template-columns: repeat(2, 1fr); }
    .salary-mega-stats { grid-template-columns: 1fr; }
    .success-stories-grid { grid-template-columns: 1fr; }
    .hike-callout { padding: 2rem; gap: 1.5rem; }
    .hike-callout-num { font-size: 3.5rem; }
    .impact-grid { grid-template-columns: repeat(2, 1fr); }
  }
</style>
</head>
<body>

<!-- SALARY TICKER BAR (very top of page) -->
<div class="salary-ticker-bar">
  <div class="salary-ticker-inner">
    <span class="s-item">🚀 Laxman <span class="sep">·</span> <strong>₹30 LPA+</strong> ↑ CKA Certified</span>
    <span class="s-item">🏆 Abdul <span class="sep">·</span> <strong>₹27 LPA</strong> ↑ DevOps Engineer</span>
    <span class="s-item">⭐ Mohanty <span class="sep">·</span> <strong>₹24 LPA</strong> ↑ Cloud-Native Role</span>
    <span class="s-item">🔥 Highest Hike <span class="sep">·</span> <strong>500%</strong> — ₹4 LPA → ₹24 LPA</span>
    <span class="s-item">📈 Average Salary Hike Across All Students <span class="sep">·</span> <strong>100%</strong></span>
    <span class="s-item">✅ 100+ Engineers Certified in 12 Months</span>
    <span class="s-item">☸️ Kubestronaut <span class="sep">·</span> CKA · CKAD · CKS · KCNA · KCSA</span>
    <span class="s-item">🚀 Laxman <span class="sep">·</span> <strong>₹30 LPA+</strong> ↑ CKA Certified</span>
    <span class="s-item">🏆 Abdul <span class="sep">·</span> <strong>₹27 LPA</strong> ↑ DevOps Engineer</span>
    <span class="s-item">⭐ Mohanty <span class="sep">·</span> <strong>₹24 LPA</strong> ↑ Cloud-Native Role</span>
    <span class="s-item">🔥 Highest Hike <span class="sep">·</span> <strong>500%</strong> — ₹4 LPA → ₹24 LPA</span>
    <span class="s-item">📈 Average Salary Hike Across All Students <span class="sep">·</span> <strong>100%</strong></span>
    <span class="s-item">✅ 100+ Engineers Certified in 12 Months</span>
    <span class="s-item">☸️ Kubestronaut <span class="sep">·</span> CKA · CKAD · CKS · KCNA · KCSA</span>
  </div>
</div>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">Raham<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#certifications">Credentials</a></li>
    <li><a href="#training">Training</a></li>
    <li><a href="#proof">Results</a></li>
    <li><a href="#salary">Success</a></li>
    <li><a href="#why">Why Me</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Hire Me →</a>
  <button class="nav-toggle" aria-label="Menu" onclick="toggleMobileMenu()">
    <span></span><span></span><span></span>
  </button>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>
  <div class="hero-inner">
    <div class="hero-badge">Available for Corporate &amp; Individual Training</div>
    <h1 class="hero-name">Raham Shaik</h1>
    <p class="hero-title">
      <strong>DevOps R&amp;D Engineer</strong> &amp; Freelance Trainer &nbsp;·&nbsp; Kubestronaut · CKA · CKAD · CKS · KCNA · KCSA · Terraform<br>
      <strong>Cloud Expert</strong> &nbsp;·&nbsp; AWS · Azure · GCP &nbsp;·&nbsp; Students landing <strong>24–30 LPA roles</strong>
    </p>
    <p class="hero-desc">
      Helping engineers and enterprise teams master Kubernetes, AWS, Azure, GCP, Terraform, and DevSecOps — with a track record of 12,000+ students trained, 100+ certifications in one year, and graduates earning <strong style="color:var(--text)">up to ₹30 LPA</strong>.
    </p>
    <div class="hero-cloud-chips">
      <span class="cloud-chip"><span class="chip-dot"></span>AWS</span>
      <span class="cloud-chip"><span class="chip-dot"></span>Azure</span>
      <span class="cloud-chip"><span class="chip-dot"></span>GCP</span>
      <span class="cloud-chip"><span class="chip-dot"></span>Kubernetes</span>
      <span class="cloud-chip"><span class="chip-dot"></span>Terraform</span>
      <span class="cloud-chip"><span class="chip-dot"></span>EKS · AKS · GKE</span>
      <span class="cloud-chip"><span class="chip-dot"></span>ArgoCD · Jenkins</span>
      <span class="cloud-chip"><span class="chip-dot"></span>DevSecOps</span>
    </div>
    <div class="hero-stats">
      <div>
        <div class="hero-stat-num">12k<span>+</span></div>
        <div class="hero-stat-label">Students Trained</div>
      </div>
      <div>
        <div class="hero-stat-num">90<span>+</span></div>
        <div class="hero-stat-label">Batches Delivered</div>
      </div>
      <div>
        <div class="hero-stat-num">100<span>+</span></div>
        <div class="hero-stat-label">Certified Last Year</div>
      </div>
      <div>
        <div class="hero-stat-num g">500<span>%</span></div>
        <div class="hero-stat-label">Highest Salary Hike</div>
      </div>
      <div>
        <div class="hero-stat-num g">₹30L<span>+</span></div>
        <div class="hero-stat-label">Top Student Package</div>
      </div>
    </div>
    <div class="hero-ctas">
      <a href="#contact" class="btn-primary">Get a Training Quote →</a>
      <a href="#salary" class="btn-green">See Student Salaries ↑</a>
      <a href="#proof" class="btn-secondary">View Results</a>
    </div>
  </div>
  <div class="hero-certs">
    <div class="cert-badge"><div class="cert-icon">CKA</div><div><div class="cert-name">Certified Kubernetes<br>Administrator</div><div class="cert-org">CNCF / Linux Foundation</div></div></div>
    <div class="cert-badge"><div class="cert-icon">CKAD</div><div><div class="cert-name">Certified Kubernetes<br>App Developer</div><div class="cert-org">CNCF / Linux Foundation</div></div></div>
    <div class="cert-badge"><div class="cert-icon">CKS</div><div><div class="cert-name">Certified Kubernetes<br>Security Specialist</div><div class="cert-org">CNCF / Linux Foundation</div></div></div>
    <div class="cert-badge"><div class="cert-icon" style="font-size:0.44rem;">TF</div><div><div class="cert-name">Terraform Associate<br>Certified</div><div class="cert-org">HashiCorp</div></div></div>
    <div class="cert-badge"><div class="cert-icon">KCNA</div><div><div class="cert-name">Kubernetes &amp; Cloud<br>Native Associate</div><div class="cert-org">CNCF</div></div></div>
    <div class="cert-badge" style="border-color:rgba(249,115,22,0.5);background:rgba(249,115,22,0.04)"><div class="cert-icon" style="font-size:0.9rem;background:rgba(249,115,22,0.12)">🏆</div><div><div class="cert-name">Kubestronaut</div><div class="cert-org">CNCF Elite Status</div></div></div>
  </div>
</section>

<!-- IMPACT BAR -->
<div id="impact">
  <div class="impact-grid reveal">
    <div class="impact-item"><div class="impact-num">12<span>k+</span></div><div class="impact-label">Students Trained</div></div>
    <div class="impact-item"><div class="impact-num">90<span>+</span></div><div class="impact-label">Batches Completed</div></div>
    <div class="impact-item"><div class="impact-num">100<span>+</span></div><div class="impact-label">Certified in 12 Months</div></div>
    <div class="impact-item"><div class="impact-num gn">500<span>%</span></div><div class="impact-label">Highest Salary Hike</div></div>
    <div class="impact-item"><div class="impact-num gn">₹30<span>LPA+</span></div><div class="impact-label">Top Student Package</div></div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <div class="about-grid">
      <div class="about-visual reveal">
        <div class="about-terminal">
          <div class="terminal-bar">
            <div class="terminal-dot"></div><div class="terminal-dot"></div><div class="terminal-dot"></div>
            <span class="terminal-title">raham-profile.json</span>
          </div>
          <div class="terminal-body">
            <div><span class="t-prompt">$</span> <span class="t-cmd">cat profile.json</span></div>
            <div>&nbsp;</div>
            <div>{</div>
            <div>&nbsp; <span class="t-key">"name"</span>: <span class="t-string">"Raham Shaik"</span>,</div>
            <div>&nbsp; <span class="t-key">"role"</span>: <span class="t-string">"DevOps R&amp;D Engineer &amp; Trainer"</span>,</div>
            <div>&nbsp; <span class="t-key">"clouds"</span>: [<span class="t-string">"AWS"</span>, <span class="t-string">"Azure"</span>, <span class="t-string">"GCP"</span>],</div>
            <div>&nbsp; <span class="t-key">"specialization"</span>: [</div>
            <div>&nbsp;&nbsp;&nbsp; <span class="t-string">"Kubernetes / Kubestronaut"</span>,</div>
            <div>&nbsp;&nbsp;&nbsp; <span class="t-string">"Terraform IaC"</span>,</div>
            <div>&nbsp;&nbsp;&nbsp; <span class="t-string">"DevSecOps"</span>,</div>
            <div>&nbsp;&nbsp;&nbsp; <span class="t-string">"CI/CD · ArgoCD · GitOps"</span></div>
            <div>&nbsp; ],</div>
            <div>&nbsp; <span class="t-key">"students_trained"</span>: <span class="t-number">12000</span>,</div>
            <div>&nbsp; <span class="t-key">"top_package"</span>: <span class="t-string">"₹30 LPA+"</span>,</div>
            <div>&nbsp; <span class="t-key">"highest_hike"</span>: <span class="t-string">"500%"</span>,</div>
            <div>&nbsp; <span class="t-key">"avg_hike"</span>: <span class="t-string">"100%"</span>,</div>
            <div>&nbsp; <span class="t-key">"status"</span>: <span class="t-val">"available_for_hire"</span></div>
            <div>}</div>
            <div>&nbsp;</div>
            <div><span class="t-prompt">$</span> <span class="t-cursor"></span></div>
          </div>
        </div>
      </div>
      <div class="about-text reveal reveal-delay-1">
        <div class="section-tag">About Me</div>
        <h2 class="section-title">Engineer who teaches.<br>Trainer who ships.</h2>
        <p>I'm a DevOps R&D Engineer and freelance trainer with deep expertise across Kubernetes, AWS, Azure, GCP, Terraform, and DevSecOps. I bridge the gap between real-world engineering and practical, job-ready education.</p>
        <p>Over 12,000+ students and 90+ training batches, I've refined a methodology that gets results: <strong>100+ certifications in one year, students landing 24–30 LPA roles, and the highest hike I've seen is 500% — from ₹4 LPA to ₹24 LPA.</strong></p>
        <p>Whether you're preparing for CKA/CKAD/CKS, AWS Solutions Architect, or Terraform — or a company upskilling a cloud-native team — I bring both <strong>practitioner depth and educator clarity</strong> to every engagement.</p>
        <div class="about-highlights">
          <div class="highlight-item">Kubernetes &amp; Kubestronaut track</div>
          <div class="highlight-item">AWS, Azure &amp; GCP bootcamps</div>
          <div class="highlight-item">Terraform IaC &amp; DevSecOps</div>
          <div class="highlight-item">CI/CD · Jenkins · ArgoCD · GitOps</div>
          <div class="highlight-item">Corporate batch training</div>
          <div class="highlight-item">1-on-1 certification coaching</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TECHNICAL EXPERTISE -->
<section id="expertise">
  <div class="section-inner">
    <div class="section-tag reveal">Technical Expertise</div>
    <h2 class="section-title reveal">The full cloud-native<br>engineering stack.</h2>
    <p class="section-sub reveal">Everything I teach, I run in production. This is the complete technology landscape I cover across individual training, corporate bootcamps, and advisory engagements.</p>

    <div class="cloud-row reveal">
      <div class="cloud-card">
        <div class="cloud-logo">☁️</div>
        <div>
          <div class="cloud-name">Amazon Web Services</div>
          <div class="cloud-desc">EC2 · EKS · ECS · ECR · Lambda · S3 · IAM · VPC · CloudWatch<br>Control Tower · Organizations · Well-Architected Framework</div>
        </div>
      </div>
      <div class="cloud-card">
        <div class="cloud-logo">🔷</div>
        <div>
          <div class="cloud-name">Microsoft Azure</div>
          <div class="cloud-desc">AKS · Azure DevOps · Container Registry<br>Virtual Networks · Azure Monitor · RBAC · Azure Pipelines</div>
        </div>
      </div>
      <div class="cloud-card">
        <div class="cloud-logo">🌐</div>
        <div>
          <div class="cloud-name">Google Cloud Platform</div>
          <div class="cloud-desc">GKE · Cloud Run · Artifact Registry<br>IAM · Cloud Build · GCP Networking · Workload Identity</div>
        </div>
      </div>
    </div>

    <div class="expertise-grid reveal reveal-delay-1">
      <div class="expertise-card">
        <div class="ex-icon">☸️</div>
        <div class="ex-label">Containers &amp; Kubernetes</div>
        <div class="ex-title">Container Orchestration</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Kubernetes</span>
          <span class="ex-pill">Docker</span>
          <span class="ex-pill hi">EKS</span>
          <span class="ex-pill hi">AKS</span>
          <span class="ex-pill hi">GKE</span>
          <span class="ex-pill">ECS · ECR</span>
          <span class="ex-pill">Helm</span>
          <span class="ex-pill">Kustomize</span>
        </div>
      </div>
      <div class="expertise-card">
        <div class="ex-icon">🔄</div>
        <div class="ex-label">CI/CD &amp; GitOps</div>
        <div class="ex-title">Automation Pipelines</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Jenkins</span>
          <span class="ex-pill hi">GitHub Actions</span>
          <span class="ex-pill hi">ArgoCD</span>
          <span class="ex-pill">Maven</span>
          <span class="ex-pill">Nexus</span>
          <span class="ex-pill">SonarQube</span>
          <span class="ex-pill">GitOps</span>
        </div>
      </div>
      <div class="expertise-card">
        <div class="ex-icon">🏗️</div>
        <div class="ex-label">IaC &amp; Config Mgmt</div>
        <div class="ex-title">Infrastructure as Code</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Terraform</span>
          <span class="ex-pill hi">Ansible</span>
          <span class="ex-pill">Terragrunt</span>
          <span class="ex-pill">Sentinel</span>
          <span class="ex-pill">Remote State</span>
          <span class="ex-pill">Modules</span>
        </div>
      </div>
      <div class="expertise-card">
        <div class="ex-icon">📊</div>
        <div class="ex-label">Monitoring &amp; Observability</div>
        <div class="ex-title">Observability Stack</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Prometheus</span>
          <span class="ex-pill hi">Grafana</span>
          <span class="ex-pill">AWS CloudWatch</span>
          <span class="ex-pill">Alertmanager</span>
          <span class="ex-pill">Dashboards</span>
        </div>
      </div>
      <div class="expertise-card">
        <div class="ex-icon">🛡️</div>
        <div class="ex-label">DevSecOps</div>
        <div class="ex-title">Security Engineering</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Trivy</span>
          <span class="ex-pill">OWASP</span>
          <span class="ex-pill hi">Terrascan</span>
          <span class="ex-pill">SonarQube</span>
          <span class="ex-pill hi">HashiCorp Sentinel</span>
          <span class="ex-pill">OPA/Gatekeeper</span>
          <span class="ex-pill">Vault</span>
          <span class="ex-pill">Falco</span>
        </div>
      </div>
      <div class="expertise-card">
        <div class="ex-icon">💻</div>
        <div class="ex-label">Scripting &amp; OS</div>
        <div class="ex-title">Automation &amp; Linux</div>
        <div class="ex-pills">
          <span class="ex-pill hi">Linux</span>
          <span class="ex-pill hi">Bash / Shell</span>
          <span class="ex-pill">kubectl</span>
          <span class="ex-pill">etcdctl</span>
          <span class="ex-pill">kubeadm</span>
          <span class="ex-pill">crictl</span>
        </div>
      </div>
      <div class="expertise-card span2">
        <div class="ex-icon">🤖</div>
        <div class="ex-label">AI Cloud Tools — Emerging Stack</div>
        <div class="ex-title">AI-Powered Cloud Engineering</div>
        <div class="ex-pills">
          <span class="ex-pill hi">K8sGPT</span>
          <span class="ex-pill hi">CAST AI</span>
          <span class="ex-pill hi">Terraformer</span>
          <span class="ex-pill">AI-driven cluster diagnostics</span>
          <span class="ex-pill">Cost optimisation automation</span>
          <span class="ex-pill">IaC reverse-generation</span>
          <span class="ex-pill">Intelligent anomaly detection</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="section-inner">
    <div class="section-tag reveal">Credentials</div>
    <h2 class="section-title reveal">I hold what I teach.</h2>
    <p class="section-sub reveal">Every certification I train others for, I've earned myself — which means you get instruction from someone who has passed the exact exams your team is preparing for.</p>
    <div class="cert-grid">
      <div class="cert-card reveal" style="grid-column:span 3;background:linear-gradient(135deg,#1a1200 0%,#141c26 60%);border-color:rgba(249,115,22,0.5);">
        <span class="cert-level" style="background:rgba(249,115,22,0.2);border-color:rgba(249,115,22,0.6);">🏆 Elite Status</span>
        <div style="display:flex;align-items:center;gap:1.5rem;flex-wrap:wrap;">
          <div>
            <div class="cert-card-abbr" style="font-size:2.2rem;">Kubestronaut</div>
            <div class="cert-card-name" style="font-size:1rem;">CNCF Kubestronaut — All 5 Kubernetes Certifications Achieved</div>
            <div class="cert-card-org">CNCF · Cloud Native Computing Foundation</div>
            <div class="cert-card-desc" style="max-width:600px;">Kubestronaut is an elite CNCF recognition awarded only to engineers who hold all five Kubernetes certifications simultaneously: CKA, CKAD, CKS, KCNA, and KCSA. Fewer than 1,000 engineers worldwide carry this title — Raham is one of them.</div>
          </div>
          <a href="https://www.credly.com/badges/61985acf-5d90-407b-9707-207be8f2c1f8/linked_in_profile" target="_blank" class="cert-view-btn" style="margin-left:auto;flex-shrink:0;">View Badge →</a>
        </div>
      </div>
      <div class="cert-card reveal"><span class="cert-level">Expert</span><div class="cert-card-abbr">CKA</div><div class="cert-card-name">Certified Kubernetes Administrator</div><div class="cert-card-org">CNCF · Linux Foundation</div><div class="cert-card-desc">Core Kubernetes administration, cluster setup, networking, storage, troubleshooting.</div><a href="https://ti-user-certificates.s3.amazonaws.com/e0df7fbf-a057-42af-8a1f-590912be5460/ed35cfd3-842b-429b-8fd0-6267e10058ec-rahamthulla-shaik-1c60f48e-9772-41be-bfb6-bfea18875f28-certificate.pdf" target="_blank" class="cert-view-btn">View Certificate →</a></div>
      <div class="cert-card reveal reveal-delay-1"><span class="cert-level">Expert</span><div class="cert-card-abbr">CKAD</div><div class="cert-card-name">Certified Kubernetes Application Developer</div><div class="cert-card-org">CNCF · Linux Foundation</div><div class="cert-card-desc">Application design, deployment, and configuration on Kubernetes for cloud-native developers.</div><a href="https://ti-user-certificates.s3.amazonaws.com/e0df7fbf-a057-42af-8a1f-590912be5460/ed35cfd3-842b-429b-8fd0-6267e10058ec-rahamthulla-shaik-b5dee7f7-594c-4972-b52b-a774ed477386-certificate.pdf" target="_blank" class="cert-view-btn">View Certificate →</a></div>
      <div class="cert-card reveal reveal-delay-2"><span class="cert-level">Expert</span><div class="cert-card-abbr">CKS</div><div class="cert-card-name">Certified Kubernetes Security Specialist</div><div class="cert-card-org">CNCF · Linux Foundation</div><div class="cert-card-desc">Cluster hardening, supply chain security, runtime protection — the most advanced Kubernetes certification.</div><a href="https://ti-user-certificates.s3.amazonaws.com/e0df7fbf-a057-42af-8a1f-590912be5460/ed35cfd3-842b-429b-8fd0-6267e10058ec-rahamthulla-shaik-e28e3a0a-653e-468a-89f7-0b070aa4793d-certificate.pdf" target="_blank" class="cert-view-btn">View Certificate →</a></div>
      <div class="cert-card reveal"><span class="cert-level">Associate</span><div class="cert-card-abbr">KCNA</div><div class="cert-card-name">Kubernetes &amp; Cloud Native Associate</div><div class="cert-card-org">CNCF</div><div class="cert-card-desc">Foundation-level cloud-native knowledge covering the full CNCF landscape, GitOps, and observability.</div><a href="https://ti-user-certificates.s3.amazonaws.com/e0df7fbf-a057-42af-8a1f-590912be5460/ed35cfd3-842b-429b-8fd0-6267e10058ec-shaik-raham-thulla-3ecb9097-e82f-4e1b-aad1-a80353a21b8c-certificate.pdf" target="_blank" class="cert-view-btn">View Certificate →</a></div>
      <div class="cert-card reveal reveal-delay-1"><span class="cert-level">Associate</span><div class="cert-card-abbr">KCSA</div><div class="cert-card-name">Kubernetes &amp; Cloud Native Security Associate</div><div class="cert-card-org">CNCF</div><div class="cert-card-desc">Security fundamentals across the cloud-native stack, bridging KCNA and the CKS expert track.</div><a href="https://ti-user-certificates.s3.amazonaws.com/e0df7fbf-a057-42af-8a1f-590912be5460/ed35cfd3-842b-429b-8fd0-6267e10058ec-rahamthulla-shaik-5df472c4-1b9e-43a6-87c8-c3caf7c3fb02-certificate.pdf" target="_blank" class="cert-view-btn">View Certificate →</a></div>
      <div class="cert-card reveal reveal-delay-2"><span class="cert-level">Associate</span><div class="cert-card-abbr">Terraform</div><div class="cert-card-name">Terraform Associate Certified</div><div class="cert-card-org">HashiCorp</div><div class="cert-card-desc">Infrastructure as Code — modules, state management, workspaces, and cloud provider integration at scale.</div><a href="https://www.credly.com/badges/453f4896-cdf4-4736-84ac-236bd0a49650/linked_in_profile" target="_blank" class="cert-view-btn">View Badge →</a></div>
    </div>
  </div>
</section>

<!-- FLAGSHIP TRAINING PROGRAMMES -->
<section id="training">
  <div class="section-inner">
    <div class="section-tag reveal">Flagship Programmes</div>
    <h2 class="section-title reveal">Training built for<br>outcomes, not hours.</h2>
    <p class="section-sub reveal">Each programme is scoped around a clear result — a certification pass, a production-ready team, or a career-defining salary jump. No filler modules. No generic curriculum.</p>
    <div class="flagship-grid">

      <!-- Hero card: Kubestronaut -->
      <div class="flagship-card hero-card reveal">
        <div class="f-badge">🏆 Flagship · Most Popular</div>
        <div style="display:flex;gap:2.5rem;flex-wrap:wrap;align-items:flex-start;">
          <div style="flex:1;min-width:270px;">
            <div class="f-icon">☸️</div>
            <div class="f-title">Kubernetes Kubestronaut Bootcamp<br><span style="color:var(--accent3);font-size:0.85rem;font-family:var(--font-mono);font-weight:400;">CKA · CKAD · CKS · KCNA · KCSA</span></div>
            <div class="f-desc">The only programme in India that takes you from Kubernetes novice to Kubestronaut — all 5 CNCF certifications in a single structured track. Built by a Kubestronaut, taught with real clusters, not slides.</div>
            <ul class="f-bullets">
              <li>Comprehensive 5-in-1 CNCF track: cluster administration, application development, security hardening, networking architecture, and the full cloud-native ecosystem</li>
              <li>Hands-on labs simulating real-world cluster troubleshooting, RBAC, NetworkPolicy, OPA/Gatekeeper, Falco runtime security, and supply chain security</li>
              <li>Mock exams replicating the exact exam environment — time-pressured, terminal-only, scenario-based, no theory shortcuts</li>
              <li>1-on-1 doubt clearing, exam strategy sessions, career guidance, resume building, and mock interviews included</li>
            </ul>
            <div class="f-tags">
              <span class="f-tag">Live Sessions</span>
              <span class="f-tag">Cluster Labs</span>
              <span class="f-tag">Mock Exams</span>
              <span class="f-tag">Individual &amp; Corporate</span>
              <span class="f-tag">RBAC · Falco · OPA</span>
              <span class="f-tag">Supply Chain Security</span>
            </div>
          </div>
          <div style="flex-shrink:0;display:flex;flex-direction:column;gap:1.2rem;">
            <div>
              <div class="f-stat-num">3,000+</div>
              <div class="f-stat-label">Engineers Trained</div>
            </div>
            <div>
              <div class="f-stat-num g">95%</div>
              <div class="f-stat-label">CKA Pass Rate</div>
            </div>
            <div>
              <div class="f-stat-num g">100%</div>
              <div class="f-stat-label">CKAD Pass Rate</div>
            </div>
            <a href="#contact" class="cert-view-btn" style="margin-top:0.25rem;width:fit-content;">Enquire Now →</a>
          </div>
        </div>
      </div>

      <!-- AWS -->
      <div class="flagship-card reveal">
        <div class="f-badge green">☁️ AWS · High Demand</div>
        <div class="f-icon">☁️</div>
        <div class="f-title">AWS Solutions Architect &amp; DevOps Engineer Bootcamp</div>
        <div class="f-desc">End-to-end AWS training for engineers who want to architect, automate, and secure cloud infrastructure at enterprise scale — and pass the SAA-C03 exam.</div>
        <ul class="f-bullets">
          <li>Core infrastructure, serverless, containers (EKS/ECS), CI/CD automation, and multi-account governance with Control Tower &amp; AWS Organizations</li>
          <li>Covers all 5 Well-Architected Framework pillars: Reliability, Security, Cost Optimisation, Performance, Sustainability</li>
          <li>Real-world projects: build production-grade VPC, EKS cluster, and full CI/CD pipeline end-to-end</li>
        </ul>
        <div class="f-stat-row">
          <div><div class="f-stat-num">SAA-C03</div><div class="f-stat-label">Target Certification</div></div>
          <div><div class="f-stat-num g">✓</div><div class="f-stat-label">Hands-on Labs</div></div>
        </div>
      </div>

      <!-- Terraform -->
      <div class="flagship-card reveal reveal-delay-1">
        <div class="f-badge" style="background:#7c3aed;">🏗️ HashiCorp · IaC</div>
        <div class="f-icon">🏗️</div>
        <div class="f-title">Terraform Associate Certification Programme</div>
        <div class="f-desc">From IaC fundamentals to advanced production patterns — everything you need for the exam and for real infrastructure work. Trained 2,000+ engineers with a 90%+ first-attempt pass rate.</div>
        <ul class="f-bullets">
          <li>IaC fundamentals → advanced patterns: modules, remote state, workspaces, Terragrunt, CDK for Terraform, and Terraform Cloud / Enterprise</li>
          <li>Sentinel policy-as-code and compliance automation across cloud environments at scale</li>
          <li>2,000+ engineers trained; industry-leading first-attempt certification pass rate above 90%</li>
        </ul>
        <div class="f-stat-row">
          <div><div class="f-stat-num">2,000+</div><div class="f-stat-label">Engineers Trained</div></div>
          <div><div class="f-stat-num g">90%+</div><div class="f-stat-label">First-Attempt Pass</div></div>
        </div>
      </div>

      <!-- DevSecOps -->
      <div class="flagship-card reveal">
        <div class="f-badge blue">🛡️ DevSecOps · Advanced</div>
        <div class="f-icon">🛡️</div>
        <div class="f-title">DevSecOps &amp; Platform Engineering Masterclass</div>
        <div class="f-desc">Security embedded at every stage of the SDLC — built for DevOps leads, Security champions, and Platform Engineering teams ready to shift left for real.</div>
        <ul class="f-bullets">
          <li>SAST/DAST, container scanning (Trivy), IaC security (Terrascan), secrets management (Vault), and policy enforcement (OPA/Sentinel)</li>
          <li>Integrating Falco for runtime threat detection and SonarQube for continuous code quality gates across pipelines</li>
          <li>Designed for Security champions, DevOps leads, and Platform Engineering teams who need more than checkbox compliance</li>
        </ul>
        <div class="f-tags">
          <span class="f-tag">Trivy</span><span class="f-tag">OWASP</span><span class="f-tag">Vault</span><span class="f-tag">OPA</span><span class="f-tag">Falco</span><span class="f-tag">Terrascan</span>
        </div>
      </div>

      <!-- Corporate -->
      <div class="flagship-card reveal reveal-delay-1">
        <div class="f-badge" style="background:#0ea5e9;">🏢 Corporate</div>
        <div class="f-icon">🏢</div>
        <div class="f-title">Corporate DevOps Upskilling</div>
        <div class="f-desc">Custom-scoped training for engineering teams. Kubernetes, CI/CD, Terraform, cloud-native architecture — tailored to your stack, your team's level, and your timeline.</div>
        <ul class="f-bullets">
          <li>Fully custom curriculum scoped to your team's current level, target outcomes, and internal tooling — not a generic syllabus</li>
          <li>Delivered as multi-day intensives or ongoing weekly batch sessions — remote or on-site, weekday or weekend</li>
          <li>Reference: 12 of 14 Tech Mahindra engineers cleared CKA or CKAD within 3 months of the engagement</li>
        </ul>
        <div class="f-tags">
          <span class="f-tag">Custom Scope</span><span class="f-tag">On-Site / Remote</span><span class="f-tag">All Team Sizes</span><span class="f-tag">Outcome-Driven</span>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- SOCIAL PROOF -->
<section id="proof">
  <div class="section-inner">
    <div class="section-tag reveal">Results &amp; Social Proof</div>
    <div class="proof-header">
      <div class="big-stat reveal">
        <div class="big-stat-num">100+</div>
        <div class="big-stat-label">Students Certified in 12 Months</div>
        <div class="big-stat-sub">Not enrolled — <em>certified</em>. These engineers passed their CKA, CKAD, CKS, or Terraform exams after training with me. This is the only number that matters.</div>
      </div>
      <div class="proof-breakdown reveal reveal-delay-1">
        <h3 style="font-family:var(--font-display);font-size:1.15rem;font-weight:700;color:var(--text);margin-bottom:1.5rem;letter-spacing:-0.02em;">Certification Pass Rates</h3>
        <div><div class="proof-bar-top"><span class="proof-bar-label">CKA Batch Pass Rate</span><span class="proof-bar-val">95%</span></div><div class="proof-bar-track"><div class="proof-bar-fill" style="width:95%"></div></div></div><br>
        <div><div class="proof-bar-top"><span class="proof-bar-label">CKAD Batch Pass Rate</span><span class="proof-bar-val">100%</span></div><div class="proof-bar-track"><div class="proof-bar-fill" style="width:100%;animation-delay:0.1s"></div></div></div><br>
        <div><div class="proof-bar-top"><span class="proof-bar-label">CKS Batch Pass Rate</span><span class="proof-bar-val">82%</span></div><div class="proof-bar-track"><div class="proof-bar-fill" style="width:82%;animation-delay:0.2s"></div></div></div><br>
        <div><div class="proof-bar-top"><span class="proof-bar-label">Terraform Batch Pass Rate</span><span class="proof-bar-val">100%</span></div><div class="proof-bar-track"><div class="proof-bar-fill" style="width:100%;animation-delay:0.3s"></div></div></div><br>
        <div style="margin-top:1.5rem;font-family:var(--font-mono);font-size:0.68rem;color:var(--text3);letter-spacing:0.04em;">Based on student-reported outcomes across 90+ batches</div>
      </div>
    </div>
    <div class="testimonials-grid">
      <div class="testimonial-card reveal">
        <div class="testimonial-quote">I had attempted the CKA once before joining Raham's batch and failed because I was studying from documentation alone. His approach is completely different — every concept is taught through live cluster scenarios, not theory slides. The troubleshooting sessions gave me the confidence to debug under exam pressure. I cleared the CKA on my second attempt with a score I am genuinely proud of.</div>
        <div class="testimonial-author"><div class="t-avatar">AK</div><div><div class="t-author-name">Arjun K.</div><div class="t-author-role">Senior DevOps Engineer, TCS</div></div><div class="t-cert-badge">✓ CKA Certified</div></div>
      </div>
      <div class="testimonial-card reveal reveal-delay-1">
        <div class="testimonial-quote">Coming from a pure development background, I was intimidated by Kubernetes before I found Raham. The way he breaks down complex topics using real-world scenarios made everything feel approachable. I cleared CKAD on my first attempt and transitioned into a cloud role within two months of certification. This training genuinely changed my career direction.</div>
        <div class="testimonial-author"><div class="t-avatar">SW</div><div><div class="t-author-name">Swetha</div><div class="t-author-role">Developer → Cloud Engineer, Wipro</div></div><div class="t-cert-badge">✓ CKAD Certified</div></div>
      </div>
      <div class="testimonial-card reveal reveal-delay-2">
        <div class="testimonial-quote">We engaged Raham for a corporate Kubernetes upskilling at Tech Mahindra for fourteen engineers. What stood out was how he customised content to our internal tooling and workflows. Within three months, twelve of our engineers cleared either CKA or CKAD. The team's confidence with Kubernetes has completely transformed.</div>
        <div class="testimonial-author"><div class="t-avatar">RT</div><div><div class="t-author-name">Rohit T.</div><div class="t-author-role">Engineering Manager, Tech Mahindra</div></div><div class="t-cert-badge">✓ Corporate Training</div></div>
      </div>
    </div>
    <div class="batch-ticker reveal">
      <div class="batch-ticker-label">Recent Batches</div>
      <div class="batch-ticker-scroll">
        <span class="batch-item">Batch #91 — <strong>CKA · 18 students</strong></span>
        <span class="batch-item">Batch #90 — <strong>CKAD · 22 students</strong></span>
        <span class="batch-item">Batch #89 — <strong>CKS + CKA Combo · 14 students</strong></span>
        <span class="batch-item">Batch #88 — <strong>Corporate DevOps · TechCorp India</strong></span>
        <span class="batch-item">Batch #87 — <strong>Terraform Associate · 20 students</strong></span>
        <span class="batch-item">Batch #86 — <strong>KCNA + KCSA · 16 students</strong></span>
        <span class="batch-item">Batch #85 — <strong>AWS Bootcamp · 18 students</strong></span>
        <span class="batch-item">Batch #91 — <strong>CKA · 18 students</strong></span>
        <span class="batch-item">Batch #90 — <strong>CKAD · 22 students</strong></span>
        <span class="batch-item">Batch #89 — <strong>CKS + CKA Combo · 14 students</strong></span>
        <span class="batch-item">Batch #88 — <strong>Corporate DevOps · TechCorp India</strong></span>
        <span class="batch-item">Batch #87 — <strong>Terraform Associate · 20 students</strong></span>
        <span class="batch-item">Batch #86 — <strong>KCNA + KCSA · 16 students</strong></span>
        <span class="batch-item">Batch #85 — <strong>AWS Bootcamp · 18 students</strong></span>
      </div>
    </div>
  </div>
</section>

<!-- SALARY TRANSFORMATION -->
<section id="salary">
  <div class="section-inner">
    <div class="salary-header-block reveal">
      <div class="section-tag">🚀 Student Success Stories</div>
      <h2 class="section-title">Training that pays for itself —<br><span style="color:var(--green);">many times over.</span></h2>
      <p class="section-sub">These aren't just certifications. These are career transformations. Real engineers, real offers, real packages — earned after training with Raham.</p>
    </div>

    <div class="salary-mega-stats">
      <div class="salary-mega-card reveal">
        <div class="salary-mega-num">500%</div>
        <div class="salary-mega-label">Highest Salary Hike</div>
        <div class="salary-mega-sub">₹4 LPA → ₹24 LPA · Single Student</div>
      </div>
      <div class="salary-mega-card reveal reveal-delay-1">
        <div class="salary-mega-num">100%</div>
        <div class="salary-mega-label">Average Salary Hike</div>
        <div class="salary-mega-sub">Across all students who completed training</div>
      </div>
      <div class="salary-mega-card reveal reveal-delay-2">
        <div class="salary-mega-num">₹30L+</div>
        <div class="salary-mega-label">Highest Package Achieved</div>
        <div class="salary-mega-sub">Top student earning post-certification</div>
      </div>
    </div>

    <div class="success-stories-grid">
      <div class="success-card reveal">
        <div class="s-avatar">LK</div>
        <div class="s-name">Laxman</div>
        <div class="s-cert">CKA Certified · Senior DevOps Engineer</div>
        <div class="s-salary-row">
          <span class="s-before">Before</span>
          <span class="s-arrow">→</span>
          <span class="s-after">₹30 LPA+</span>
        </div>
        <span class="s-hike-badge">↑ Top Earner in Programme</span>
        <div class="s-desc">Secured a senior DevOps Engineer role at a product-based company after completing the Kubernetes bootcamp. Among the highest packages achieved by any student in the programme — a result of deep skills, not just a certificate.</div>
      </div>
      <div class="success-card reveal reveal-delay-1">
        <div class="s-avatar">AB</div>
        <div class="s-name">Abdul</div>
        <div class="s-cert">Cloud-Native Engineer · Certified</div>
        <div class="s-salary-row">
          <span class="s-before">Before</span>
          <span class="s-arrow">→</span>
          <span class="s-after">₹27 LPA</span>
        </div>
        <span class="s-hike-badge">↑ Major Career Jump</span>
        <div class="s-desc">Leveraged Kubernetes certification and cloud-native skills to transition into a premium engineering role — combining technical depth from training with career positioning support through resume building and mock interviews.</div>
      </div>
      <div class="success-card reveal reveal-delay-2">
        <div class="s-avatar">MH</div>
        <div class="s-name">Mohanty</div>
        <div class="s-cert">CKAD Certified · Cloud Engineer</div>
        <div class="s-salary-row">
          <span class="s-before">Before</span>
          <span class="s-arrow">→</span>
          <span class="s-after">₹24 LPA</span>
        </div>
        <span class="s-hike-badge">↑ Career-Defining Move</span>
        <div class="s-desc">Transitioned from a traditional IT role to a cloud-native engineering position after completing the Kubernetes track — achieving a salary milestone that would have taken years through any other path.</div>
      </div>
    </div>

    <div class="hike-callout reveal">
      <div>
        <div class="hike-callout-label">🔥 Record — Single Student</div>
        <div class="hike-callout-num">500%</div>
        <div style="font-family:var(--font-mono);font-size:0.72rem;color:var(--green);margin-top:0.5rem;letter-spacing:0.05em;">₹4 LPA → ₹24 LPA</div>
      </div>
      <div class="hike-callout-story">
        One of Raham's students joined the Kubernetes bootcamp earning <strong>₹4 LPA</strong>. Through hands-on cluster training, troubleshooting mastery, and end-to-end career support — resume building, mock interviews, and job positioning — they landed a role at <strong>₹24 LPA</strong>.<br><br>
        That is a <strong>500% salary increase</strong>. Not an outlier — a result of the right training methodology, the right skills, and the right positioning in the job market.<br><br>
        <strong>Average hike across all students: 100%.</strong> The programme does not just get you certified. It gets you hired — at the right number.
      </div>
      <a href="#contact" class="btn-green" style="flex-shrink:0;white-space:nowrap;">Start Your Journey →</a>
    </div>
  </div>
</section>

<!-- WHY CHOOSE ME -->
<section id="why">
  <div class="section-inner">
    <div class="section-tag reveal">Why Choose Me</div>
    <h2 class="section-title reveal">Not just a trainer.<br>A practitioner who teaches.</h2>
    <p class="section-sub reveal">Every programme I run is built around one principle — if you cannot do it in production, the training has failed. Here is what makes this engagement genuinely different.</p>
    <div class="why-grid reveal">
      <div class="why-card"><div class="why-icon">🎯</div><div class="why-title">Interactive Teaching</div><div class="why-desc">Every session is a two-way conversation. Students work alongside me on live clusters, ask questions in real time, and debug problems as they arise. Learning by doing, not watching.</div></div>
      <div class="why-card"><div class="why-icon">🧩</div><div class="why-title">100% Scenario-Based</div><div class="why-desc">No isolated theory. Every concept — RBAC to NetworkPolicy to pod disruption budgets — is taught through a realistic scenario you'd encounter in production or the exam environment.</div></div>
      <div class="why-card"><div class="why-icon">🔍</div><div class="why-title">Troubleshooting Mastery</div><div class="why-desc">Entire sessions dedicated to diagnosing broken clusters, misconfigured resources, and developing the systematic debugging mindset that both exams and production demand.</div></div>
      <div class="why-card"><div class="why-icon">⚙️</div><div class="why-title">Automated Scripts</div><div class="why-desc">A curated library of production-grade shell scripts, kubectl aliases, and automation snippets — built and refined across 90+ batches to accelerate your exam and daily work.</div></div>
      <div class="why-card"><div class="why-icon">📋</div><div class="why-title">Day-to-Day Simulations</div><div class="why-desc">Rolling updates, scaling, ingress configuration, secret management, monitoring setup. Real DevOps work, every session — not textbook exercises disconnected from production reality.</div></div>
      <div class="why-card"><div class="why-icon">🏗️</div><div class="why-title">Real Production Clusters</div><div class="why-desc">We build and break real infrastructure together. Students leave having configured actual Kubernetes clusters end-to-end — not just having understood how it theoretically works.</div></div>
      <div class="why-card"><div class="why-icon">🧭</div><div class="why-title">Career Guidance</div><div class="why-desc">Where Kubernetes, AWS, and cloud-native skills fit in the broader market, which roles to target, and how to position yourself for the right opportunities after certification.</div></div>
      <div class="why-card"><div class="why-icon">📄</div><div class="why-title">Resume Building</div><div class="why-desc">A certification without a strong resume rarely opens doors. I help craft your DevOps resume the way senior hiring managers and FAANG recruiters actually look for candidates.</div></div>
      <div class="why-card"><div class="why-icon">📝</div><div class="why-title">Tool-by-Tool Exam Drills</div><div class="why-desc">Structured drills on kubectl, etcdctl, kubeadm, crictl — so you're fast, accurate, and confident in the terminal-only exam environment under time pressure.</div></div>
      <div class="why-card"><div class="why-icon">🎤</div><div class="why-title">Mock Interviews</div><div class="why-desc">Realistic mock interviews covering system design, Kubernetes architecture, troubleshooting scenarios, and behavioral questions — so you walk into your next interview fully prepared.</div></div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="contact-grid">
      <div>
        <div class="section-tag reveal">Get In Touch</div>
        <h2 class="contact-info-title reveal">Ready to upskill your team<br>or <span>get certified?</span></h2>
        <p class="contact-info-sub reveal">Whether you're an individual engineer targeting CKA/CKAD/CKS/AWS, or a company building a cloud-native team — let's talk. I respond within 24 hours.</p>
        <div class="contact-channels reveal">
          <a href="mailto:rahamthetrainer@gmail.com" class="contact-channel">
            <div class="ch-icon">✉️</div>
            <div><div class="ch-label">Email</div><div class="ch-value">rahamthetrainer@gmail.com</div></div>
            <div class="ch-arrow">→</div>
          </a>
          <a href="https://www.linkedin.com/in/raham-shaik-813317201/" target="_blank" class="contact-channel">
            <div class="ch-icon">💼</div>
            <div><div class="ch-label">LinkedIn</div><div class="ch-value">linkedin.com/in/raham-shaik-813317201</div></div>
            <div class="ch-arrow">→</div>
          </a>
        </div>
      </div>
      <div class="contact-form-wrapper reveal reveal-delay-1">
        <div id="contact-form-inner">
          <div class="form-title">Send a Training Inquiry</div>
          <div class="form-sub">Free consultation · No commitment required</div>
          <div class="form-row">
            <div class="form-group"><label for="f-name">Your Name</label><input type="text" id="f-name" placeholder="Arjun Kumar"></div>
            <div class="form-group"><label for="f-email">Email Address</label><input type="email" id="f-email" placeholder="you@company.com"></div>
          </div>
          <div class="form-group">
            <label for="f-type">Programme Interest</label>
            <select id="f-type">
              <option value="" disabled selected>Select one…</option>
              <option>Kubernetes Kubestronaut Bootcamp (CKA/CKAD/CKS/KCNA/KCSA)</option>
              <option>AWS Solutions Architect / DevOps Bootcamp</option>
              <option>Terraform Associate Certification</option>
              <option>DevSecOps &amp; Platform Engineering Masterclass</option>
              <option>Corporate Batch Training</option>
              <option>Other / Just Exploring</option>
            </select>
          </div>
          <div class="form-group">
            <label for="f-team">Team Size (if corporate)</label>
            <select id="f-team">
              <option value="" disabled selected>Select range…</option>
              <option>Just me</option>
              <option>2–5 engineers</option>
              <option>6–15 engineers</option>
              <option>16–50 engineers</option>
              <option>50+ engineers</option>
            </select>
          </div>
          <div class="form-group"><label for="f-msg">What are you trying to achieve?</label><textarea id="f-msg" placeholder="e.g. I want to pass CKA in 3 months. Currently a DevOps engineer with 2 years experience looking for hands-on cluster training…"></textarea></div>
          <button class="form-submit" onclick="submitForm()">Send Inquiry →</button>
          <div class="form-note">I typically respond within 24 hours · No spam, ever</div>
        </div>
        <div class="form-success" id="form-success">
          <div class="form-success-icon">✅</div>
          <div class="form-success-title">Inquiry received!</div>
          <div class="form-success-sub">Thanks for reaching out. I'll be in touch within 24 hours to discuss your training needs.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">Raham<span>.</span></div>
    <ul class="footer-links">
      <li><a href="#about">About</a></li>
      <li><a href="#expertise">Expertise</a></li>
      <li><a href="#certifications">Credentials</a></li>
      <li><a href="#training">Training</a></li>
      <li><a href="#proof">Results</a></li>
      <li><a href="#salary">Success</a></li>
      <li><a href="#why">Why Me</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="footer-copy">© 2025 Raham Shaik · DevOps &amp; Cloud Trainer · Kubestronaut · All rights reserved</div>
  </div>
</footer>

<script>
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.08, rootMargin: '0px 0px -30px 0px' });
reveals.forEach(el => observer.observe(el));

function submitForm() {
  const name = document.getElementById('f-name').value.trim();
  const email = document.getElementById('f-email').value.trim();
  if (!name || !email) { alert('Please enter your name and email to continue.'); return; }
  document.getElementById('contact-form-inner').style.display = 'none';
  document.getElementById('form-success').style.display = 'block';
}

function toggleMobileMenu() {
  const links = document.querySelector('.nav-links');
  const cta = document.querySelector('.nav-cta');
  if (links) {
    const isVisible = links.style.display === 'flex';
    links.style.cssText = isVisible ? '' : 'display:flex;flex-direction:column;position:fixed;top:97px;left:0;right:0;background:var(--bg);padding:2rem;gap:1.5rem;border-bottom:1px solid var(--border);z-index:99;';
    if (cta) cta.style.display = isVisible ? '' : 'none';
  }
}

document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    const target = document.querySelector(a.getAttribute('href'));
    if (target) {
      e.preventDefault();
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      const links = document.querySelector('.nav-links');
      if (links && links.style.flexDirection === 'column') toggleMobileMenu();
    }
  });
});
</script>
</body>
</html>
