<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Porra Mundialista 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow+Condensed:wght@400;600;700&family=Barlow:wght@400;500&display=swap" rel="stylesheet">
<style>
  /* ─── RESET & BASE ─── */
  html { scroll-behavior: smooth; }
  * { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --blue: #0057B7;
    --blue-light: #4A90FF;
    --red: #E8002D;
    --red-dark: #A5001F;
    --green: #007A35;
    --green-light: #00B84C;
    --dark: #030810;
    --dark2: #060E1A;
    --dark3: #0D1826;
    --white: #F0F6FF;
    --gray: #7A90B0;
  }

  body {
    background: var(--dark);
    color: var(--white);
    font-family: 'Barlow', sans-serif;
    overflow-x: hidden;
    min-width: 320px;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
    padding: 2rem 1.5rem;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 0%, rgba(0,87,183,0.55) 0%, transparent 70%),
      radial-gradient(ellipse 60% 50% at 20% 100%, rgba(232,0,45,0.3) 0%, transparent 70%),
      radial-gradient(ellipse 50% 40% at 80% 90%, rgba(0,122,53,0.25) 0%, transparent 70%),
      var(--dark2);
  }
  .hero-bg::before {
    content: '';
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
    background-size: 60px 60px, 60px 60px;
    pointer-events: none;
  }
  .ball {
    position: absolute;
    border-radius: 50%;
    background: radial-gradient(circle at 35% 35%, #fff 0%, #ccc 50%, #999 100%);
    box-shadow: inset -8px -8px 20px rgba(0,0,0,0.5);
    opacity: 0.1;
    animation: floatBall linear infinite;
  }
  .b1 { width:120px;height:120px; top:8%; left:5%; animation-duration:18s; }
  .b2 { width:60px;height:60px; top:20%; right:8%; animation-duration:14s; animation-delay:-4s; }
  .b3 { width:90px;height:90px; bottom:15%; left:12%; animation-duration:22s; animation-delay:-8s; }
  .b4 { width:50px;height:50px; bottom:25%; right:6%; animation-duration:16s; animation-delay:-2s; }
  @keyframes floatBall {
    0%   { transform: translateY(0) rotate(0deg); }
    50%  { transform: translateY(-30px) rotate(180deg); }
    100% { transform: translateY(0) rotate(360deg); }
  }
  .hero-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 0.85rem; font-weight: 600;
    letter-spacing: 0.35em; text-transform: uppercase;
    color: var(--blue-light);
    background: rgba(0,87,183,0.15);
    border: 1px solid rgba(0,87,183,0.4);
    padding: 0.35rem 1.2rem; border-radius: 2px;
    margin-bottom: 1.5rem;
    animation: fadeUp 0.8s ease both;
  }
  .hero-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(3.5rem, 10vw, 8rem);
    line-height: 0.9; letter-spacing: 0.02em;
    text-shadow: 0 0 40px rgba(0,87,183,0.35);
    animation: fadeUp 0.8s 0.15s ease both;
  }
  .hero-title span.blue { color: var(--blue-light); }
  .hero-title span.red  { color: var(--red); }
  .hero-subtitle {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: clamp(1.1rem, 3vw, 1.6rem); font-weight: 600;
    letter-spacing: 0.15em; text-transform: uppercase;
    color: rgba(240,246,255,0.6); margin-top: 0.8rem;
    animation: fadeUp 0.8s 0.3s ease both;
  }
  .hero-tagline {
    font-size: clamp(0.95rem, 2vw, 1.15rem);
    color: rgba(240,246,255,0.75);
    max-width: 560px; margin: 1.8rem auto 0; line-height: 1.65;
    animation: fadeUp 0.8s 0.45s ease both;
  }
  .hero-cta {
    margin-top: 2.5rem;
    display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;
    animation: fadeUp 0.8s 0.6s ease both;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ─── BUTTONS ─── */
  .btn {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 1rem; font-weight: 700;
    letter-spacing: 0.12em; text-transform: uppercase;
    padding: 0.85rem 2.2rem;
    border: none; border-radius: 999px;
    cursor: pointer; text-decoration: none;
    display: inline-block;
    transition: transform 0.15s, box-shadow 0.15s;
  }
  .btn-primary {
    background: var(--blue); color: var(--white);
    box-shadow: 0 4px 24px rgba(0,87,183,0.5), inset 0 1px 0 rgba(255,255,255,0.15);
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 32px rgba(0,87,183,0.7); }
  .btn-outline {
    background: transparent; color: var(--white);
    border: 1.5px solid rgba(240,246,255,0.35);
  }
  .btn-outline:hover { border-color: var(--white); transform: translateY(-2px); }
  .btn-info {
    background: linear-gradient(135deg, rgba(245,166,35,0.18), rgba(232,0,45,0.1));
    color: var(--white); border: 1.5px solid rgba(245,166,35,0.5);
  }
  .btn-info:hover {
    background: linear-gradient(135deg, rgba(245,166,35,0.32), rgba(232,0,45,0.18));
    border-color: #F5A623; transform: translateY(-2px);
    box-shadow: 0 8px 28px rgba(245,166,35,0.28);
  }
  .btn-phases {
    background: linear-gradient(135deg, rgba(0,122,53,0.18), rgba(0,87,183,0.12));
    color: var(--white); border: 1.5px solid rgba(0,184,76,0.45);
  }
  .btn-phases:hover {
    background: linear-gradient(135deg, rgba(0,122,53,0.3), rgba(0,87,183,0.2));
    border-color: var(--green-light); transform: translateY(-2px);
    box-shadow: 0 8px 28px rgba(0,122,53,0.3);
  }
  .btn-scoring {
    background: linear-gradient(135deg, rgba(0,87,183,0.15), rgba(0,122,53,0.1));
    color: var(--white); border: 1.5px solid rgba(0,87,183,0.45);
  }
  .btn-scoring:hover {
    background: linear-gradient(135deg, rgba(0,87,183,0.28), rgba(0,122,53,0.2));
    border-color: var(--blue-light); transform: translateY(-2px);
    box-shadow: 0 8px 28px rgba(0,87,183,0.3);
  }

  /* ─── SCROLL HINT ─── */
  .scroll-hint {
    position: absolute; bottom: 2rem; left: 50%;
    transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
    color: rgba(240,246,255,0.3); font-size: 0.7rem;
    letter-spacing: 0.2em; text-transform: uppercase;
    animation: fadeUp 1s 1s ease both;
  }
  .scroll-line {
    width: 1px; height: 40px;
    background: linear-gradient(to bottom, rgba(0,87,183,0.7), transparent);
    animation: scrollPulse 2s ease infinite;
  }
  @keyframes scrollPulse {
    0%,100% { opacity: 0.3; } 50% { opacity: 0.9; }
  }

  /* ─── GALLERY SECTION ─── */
  .gallery-section {
    position: relative;
    padding: 4rem 1.5rem;
    background: linear-gradient(180deg, var(--dark2), var(--dark));
  }
  .gallery-container {
    max-width: 1100px;
    margin: 0 auto;
  }
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
  }
  @media (max-width: 768px) {
    .gallery-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
  }
  .gallery-item {
    position: relative;
    overflow: hidden;
    border-radius: 18px;
    box-shadow: 0 12px 48px rgba(0,87,183,0.25);
    transition: transform 0.4s cubic-bezier(0.34,1.2,0.64,1), box-shadow 0.4s ease;
    cursor: pointer;
    aspect-ratio: 4/3;
  }
  .gallery-item:hover {
    transform: translateY(-12px) scale(1.03);
    box-shadow: 0 24px 64px rgba(0,87,183,0.4);
  }
  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: transform 0.6s ease;
  }
  .gallery-item:hover img {
    transform: scale(1.08);
  }
  .gallery-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,87,183,0.4), rgba(232,0,45,0.3), rgba(0,122,53,0.2));
    opacity: 0;
    transition: opacity 0.4s ease;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .gallery-item:hover .gallery-overlay {
    opacity: 1;
  }
  .gallery-label {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.6rem;
    color: var(--white);
    text-align: center;
    letter-spacing: 0.05em;
    text-shadow: 0 4px 16px rgba(0,0,0,0.8);
  }

  /* ─── SECTIONS ─── */
  section { position: relative; padding: 5rem 1.5rem; }
  .container { max-width: 960px; margin: 0 auto; }
  .section-tag {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 0.75rem; font-weight: 700;
    letter-spacing: 0.4em; text-transform: uppercase;
    color: var(--blue-light); margin-bottom: 0.6rem;
  }
  .section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.5rem);
    line-height: 1; letter-spacing: 0.03em; margin-bottom: 1rem;
  }
  .section-intro {
    font-size: 1rem; color: rgba(240,246,255,0.65);
    max-width: 560px; line-height: 1.7; margin-bottom: 3rem;
  }
  .divider {
    height: 2px;
    background: linear-gradient(to right, var(--blue), var(--red), var(--green));
    margin: 0 auto; max-width: 800px; opacity: 0.45; border-radius: 2px;
  }

  /* ─── REQUIREMENTS ─── */
  .req-section { background: var(--dark2); }
  .req-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1.5rem; }
  .req-card {
    background: rgba(0,87,183,0.07);
    border: 1px solid rgba(0,87,183,0.22);
    border-top: 3px solid var(--blue);
    border-radius: 16px; padding: 1.8rem 1.5rem;
    position: relative; overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 8px 24px rgba(0,0,0,0.35);
  }
  .req-card:hover { transform: translateY(-6px) scale(1.02); box-shadow: 0 16px 40px rgba(0,87,183,0.2); }
  .req-num {
    font-family: 'Bebas Neue', sans-serif; font-size: 4rem;
    color: rgba(0,87,183,0.1);
    position: absolute; top: -0.5rem; right: 0.8rem;
    line-height: 1; pointer-events: none;
  }
  .req-icon { font-size: 1.8rem; margin-bottom: 0.8rem; }
  .req-label {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem;
    font-weight: 700; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--blue-light); margin-bottom: 0.4rem;
  }
  .req-title { font-family: 'Barlow Condensed', sans-serif; font-size: 1.15rem; font-weight: 700; margin-bottom: 0.5rem; }
  .req-text { font-size: 0.88rem; color: rgba(240,246,255,0.6); line-height: 1.6; }
  .req-highlight { color: var(--blue-light); font-weight: 700; }

  /* ─── PAYMENT ─── */
  .pay-section { background: var(--dark); }
  .pay-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  @media (max-width: 600px) { .pay-grid { grid-template-columns: 1fr; } }
  .pay-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 16px; padding: 2rem;
    display: flex; flex-direction: column; gap: 0.8rem;
    position: relative; overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 8px 24px rgba(0,0,0,0.3);
  }
  .pay-card:hover { transform: translateY(-6px) scale(1.02); }
  .pay-card::before {
    content: ''; position: absolute; top:0; left:0; right:0; height: 3px;
  }
  .pay-card.digital::before { background: linear-gradient(90deg, var(--green), var(--green-light)); }
  .pay-card.cash::before    { background: linear-gradient(90deg, var(--red-dark), var(--red)); }
  .pay-icon { font-size: 2.2rem; }
  .pay-type {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem;
    font-weight: 700; letter-spacing: 0.3em; text-transform: uppercase; color: var(--gray);
  }
  .pay-title { font-family: 'Bebas Neue', sans-serif; font-size: 1.6rem; line-height: 1.1; }
  .pay-desc { font-size: 0.9rem; color: rgba(240,246,255,0.6); line-height: 1.65; }
  .pay-detail {
    margin-top: 0.5rem; padding: 0.7rem 1rem;
    background: rgba(0,87,183,0.1);
    border-left: 3px solid var(--blue);
    font-size: 0.85rem; color: var(--white); font-weight: 500;
    border-radius: 0 8px 8px 0;
  }
  .alert {
    background: linear-gradient(135deg, rgba(232,0,45,0.12), rgba(232,0,45,0.04));
    border: 1px solid rgba(232,0,45,0.35);
    border-left: 4px solid var(--red);
    padding: 1.2rem 1.5rem; margin-top: 2rem;
    display: flex; gap: 1rem; align-items: flex-start;
    border-radius: 0 12px 12px 0;
  }
  .alert-icon { font-size: 1.4rem; flex-shrink: 0; margin-top: 0.1rem; }
  .alert-text { font-size: 0.9rem; color: rgba(240,246,255,0.8); line-height: 1.65; }
  .alert-text strong { color: var(--white); }

  /* ─── BOTÓN QR ─── */
  .qr-btn-wrap {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
  }
  .btn-qr {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 1rem; font-weight: 700;
    letter-spacing: 0.12em; text-transform: uppercase;
    padding: 0.9rem 2.2rem;
    border-radius: 999px; cursor: pointer;
    display: inline-flex; align-items: center; gap: 0.6rem;
    background: linear-gradient(135deg, rgba(0,184,76,0.18), rgba(0,87,183,0.12));
    color: var(--white);
    border: 1.5px solid rgba(0,184,76,0.5);
    transition: transform 0.15s, box-shadow 0.15s, background 0.15s;
    box-shadow: 0 4px 20px rgba(0,184,76,0.15);
  }
  .btn-qr:hover {
    background: linear-gradient(135deg, rgba(0,184,76,0.32), rgba(0,87,183,0.22));
    border-color: var(--green-light);
    transform: translateY(-2px);
    box-shadow: 0 8px 28px rgba(0,184,76,0.3);
  }
  .btn-qr .qr-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--green-light);
    animation: pulse 1.8s ease infinite;
    flex-shrink: 0;
  }

  /* ─── MODAL QR ─── */
  .qr-modal {
    display: none; position: fixed; inset: 0;
    background: rgba(3,8,16,0.92); backdrop-filter: blur(14px);
    z-index: 4000; align-items: center; justify-content: center;
    padding: 1.5rem;
  }
  .qr-modal.active { display: flex; animation: fadeIn 0.22s ease both; }
  .qr-modal-box {
    background: var(--dark3);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 24px; max-width: 380px; width: 100%;
    overflow: hidden;
    box-shadow: 0 0 80px rgba(0,184,76,0.2), 0 30px 60px rgba(0,0,0,0.8);
    animation: scaleIn 0.3s cubic-bezier(0.34,1.2,0.64,1) both;
  }
  .qr-modal-box.closing { animation: scaleOut 0.2s ease both; }
  .qr-modal-stripe { height: 4px; background: linear-gradient(90deg, var(--green), var(--blue), var(--red)); }
  .qr-modal-header {
    padding: 1.4rem 1.6rem 0.8rem;
    display: flex; align-items: center; justify-content: space-between;
  }
  .qr-modal-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.6rem; letter-spacing: 0.04em; color: var(--white);
  }
  .qr-modal-close {
    width: 34px; height: 34px;
    display: flex; align-items: center; justify-content: center;
    background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
    border-radius: 50%; cursor: pointer; color: rgba(240,246,255,0.45);
    transition: background 0.15s, color 0.15s, transform 0.15s;
    font-size: 0.85rem;
  }
  .qr-modal-close:hover { background: rgba(255,255,255,0.12); color: var(--white); transform: rotate(90deg); }
  .qr-modal-body {
    padding: 0.5rem 1.6rem 1.6rem;
    display: flex; flex-direction: column; align-items: center; gap: 1rem;
  }
  .qr-img-frame {
    background: #ffffff;
    border-radius: 16px;
    padding: 1rem;
    box-shadow: 0 8px 32px rgba(0,0,0,0.5);
    width: 100%; max-width: 260px;
  }
  .qr-img-frame img {
    width: 100%; height: auto; display: block; border-radius: 8px;
  }
  .qr-modal-hint {
    font-size: 0.82rem; color: rgba(240,246,255,0.5);
    text-align: center; line-height: 1.55;
  }
  .qr-modal-hint strong { color: var(--green-light); }
  .qr-modal-footer {
    padding: 0.8rem 1.6rem 1.4rem;
    display: flex; justify-content: center;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .qr-close-btn {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.9rem; font-weight: 700;
    letter-spacing: 0.12em; text-transform: uppercase;
    padding: 0.65rem 2rem; border: 1.5px solid rgba(240,246,255,0.25);
    border-radius: 999px; background: transparent; color: var(--white);
    cursor: pointer; transition: border-color 0.15s, background 0.15s;
  }
  .qr-close-btn:hover { border-color: var(--white); background: rgba(255,255,255,0.06); }

  /* ─── COMMITTEE ─── */
  .committee-section { background: var(--dark2); }
  .committee-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1.5rem; }
  .committee-card {
    background: rgba(0,87,183,0.06);
    border: 1px solid rgba(0,87,183,0.18);
    border-radius: 18px; padding: 2rem 1.5rem; text-align: center;
    position: relative; overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 8px 24px rgba(0,0,0,0.25);
  }
  .committee-card:hover { transform: translateY(-6px) scale(1.02); box-shadow: 0 16px 40px rgba(0,87,183,0.15); }
  .committee-card::after {
    content: ''; position: absolute; bottom:0; left:0; right:0; height: 2px;
    background: linear-gradient(90deg, var(--blue), var(--red), var(--green));
    opacity: 0; transition: opacity 0.3s;
  }
  .committee-card:hover::after { opacity: 1; }
  .committee-avatar {
    width: 72px; height: 72px; border-radius: 50%;
    margin: 0 auto 1rem;
    display: flex; align-items: center; justify-content: center;
    font-size: 2rem; border: 2px solid rgba(0,87,183,0.4);
  }
  .committee-avatar.admin    { background: rgba(0,122,53,0.25); }
  .committee-avatar.audit    { background: rgba(232,0,45,0.2); }
  .committee-avatar.treasury { background: rgba(0,87,183,0.2); }
  .committee-role {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem;
    font-weight: 700; letter-spacing: 0.3em; text-transform: uppercase;
    color: var(--blue-light); margin-bottom: 0.4rem;
  }
  .committee-name { font-family: 'Barlow Condensed', sans-serif; font-size: 1.25rem; font-weight: 700; margin-bottom: 0.3rem; }
  .committee-desc { font-size: 0.82rem; color: rgba(240,246,255,0.45); line-height: 1.5; }

  /* ─── FOOTER ─── */
  .footer-section {
    background: linear-gradient(to bottom, var(--dark2), var(--dark));
    text-align: center; padding: 5rem 1.5rem 3rem;
  }
  .deadline-box {
    display: inline-block;
    border: 1px solid rgba(0,87,183,0.45);
    background: rgba(0,87,183,0.1);
    padding: 2rem 3rem; margin-bottom: 3rem;
    border-radius: 22px; box-shadow: 0 0 50px rgba(0,87,183,0.18);
  }
  .deadline-label {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.7rem;
    font-weight: 700; letter-spacing: 0.4em; text-transform: uppercase;
    color: var(--blue-light); margin-bottom: 0.5rem;
  }
  .deadline-date { font-family: 'Bebas Neue', sans-serif; font-size: clamp(2.5rem, 6vw, 4rem); color: var(--white); line-height: 1; }
  .deadline-sub { font-size: 0.85rem; color: rgba(240,246,255,0.45); margin-top: 0.3rem; }
  .trophy-line { display: flex; align-items: center; justify-content: center; gap: 0.8rem; margin: 1.5rem 0; }
  .trophy-line::before { content: ''; flex: 1; height: 1px; background: linear-gradient(to left, rgba(0,87,183,0.5), transparent); }
  .trophy-line::after  { content: ''; flex: 1; height: 1px; background: linear-gradient(to right, rgba(232,0,45,0.5), transparent); }
  .trophy-emoji { font-size: 1.4rem; }
  .footer-title { font-family: 'Bebas Neue', sans-serif; font-size: clamp(1.8rem, 4vw, 2.8rem); margin-bottom: 0.8rem; }
  .footer-sub { font-size: 0.88rem; color: rgba(240,246,255,0.4); margin-bottom: 2.5rem; }
  .footer-committee {
    font-size: 0.8rem; color: rgba(240,246,255,0.25);
    letter-spacing: 0.1em; text-transform: uppercase;
    margin-top: 3rem; padding-top: 1.5rem;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .scoring-teaser {
    margin-top: 1rem;
    display: inline-flex; align-items: center; gap: 0.5rem;
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.75rem;
    font-weight: 700; letter-spacing: 0.2em; text-transform: uppercase;
    color: #F5A623; opacity: 0.75;
  }
  .scoring-teaser::before {
    content: ''; display: inline-block; width: 6px; height: 6px;
    border-radius: 50%; background: #F5A623; animation: pulse 1.8s ease infinite;
  }
  @keyframes pulse { 0%,100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.4; transform: scale(0.7); } }

  /* ══════════════════════════════════════════
     RESPONSIVE — MOBILE · TABLET · DESKTOP
     ══════════════════════════════════════════ */

  /* ── TABLET (≤ 900px) ── */
  @media (max-width: 900px) {
    section { padding: 4rem 1.5rem; }
    .sc-bonus-grid { grid-template-columns: 1fr 1fr; }
  }

  /* ── TABLET PEQUEÑA / MÓVIL GRANDE (≤ 768px) ── */
  @media (max-width: 768px) {
    /* Hero */
    .hero { padding: 5rem 1.2rem 3rem; min-height: 100svh; }
    .hero-cta { gap: 0.7rem; }

    /* Botones: apilados y ancho completo en hero */
    .hero .hero-cta .btn { width: 100%; text-align: center; }

    /* Galería: una columna */
    .gallery-grid { grid-template-columns: 1fr; gap: 1.2rem; }

    /* Pagos: una columna */
    .pay-grid { grid-template-columns: 1fr; }

    /* Requisitos */
    .req-grid { grid-template-columns: 1fr 1fr; }

    /* Comité: una columna */
    .committee-grid { grid-template-columns: 1fr; }

    /* Footer deadline */
    .deadline-box { padding: 1.5rem 1.5rem; width: 100%; }

    /* Footer CTAs apilados */
    .footer-cta { flex-direction: column; align-items: center; }
    .footer-cta .btn,
    .footer-cta a.btn { width: 100%; max-width: 420px; text-align: center; }

    /* Modales: padding reducido */
    .wc-modal-header { padding: 1.4rem 1.3rem 0.8rem; }
    .wc-modal-body   { padding: 0 1.3rem 1.5rem; }
    .wc-modal-footer { padding: 0.8rem 1.3rem 1.2rem; }
    .sc-header { padding: 1.3rem 1.3rem 0.8rem; }
    .sc-body   { padding: 0 1.3rem 1.2rem; }
    .sc-footer { padding: 0.8rem 1.3rem 1.2rem; }

    /* Modal scoring bonus: 1 columna */
    .sc-bonus-grid { grid-template-columns: 1fr; }
    .sc-bonus-card[style*="span 2"] { grid-column: span 1; }
  }

  /* ── MÓVIL (≤ 640px) ── */
  @media (max-width: 640px) {
    /* Secciones */
    section { padding: 3rem 1rem; }

    /* Títulos de sección */
    .section-title { font-size: clamp(1.8rem, 7vw, 2.4rem); }

    /* Requisitos: 2 columnas pequeñas */
    .req-grid { grid-template-columns: 1fr 1fr; gap: 0.9rem; }
    .req-card { padding: 1.2rem 1rem; }

    /* Comité */
    .committee-grid { grid-template-columns: 1fr; max-width: 360px; margin: 0 auto; }

    /* Deadline */
    .deadline-box { padding: 1.2rem 1rem; }
    .deadline-date { font-size: clamp(2rem, 8vw, 3rem); }

    /* QR */
    .qr-image-wrapper { padding: 1.2rem; }

    /* Tabla scoring */
    .sc-table th, .sc-table td { padding: 0.4rem 0.6rem; font-size: 0.8rem; }

    /* Ejemplos scoring */
    .sc-example { padding: 0.7rem 0.85rem; }

    /* Colombia box */
    .sc-colombia { padding: 0.9rem 1rem; }

    /* Premios modal: columna única */
    .prize-grid { grid-template-columns: 1fr; }
    .tie-grid   { grid-template-columns: 1fr; }

    /* Fases modal */
    .responsible-row { flex-direction: column; gap: 0.5rem; }
  }

  /* ── MÓVIL PEQUEÑO (≤ 480px) ── */
  @media (max-width: 480px) {
    /* Requisitos: 1 columna */
    .req-grid { grid-template-columns: 1fr; }

    /* Hero label texto más corto */
    .hero-label { font-size: 0.72rem; letter-spacing: 0.2em; padding: 0.3rem 0.9rem; }

    /* Botones más pequeños */
    .btn { font-size: 0.9rem; padding: 0.75rem 1.5rem; }

    /* Modal ancho total */
    .wc-modal { padding: 0.6rem; }
    .wc-modal-box { border-radius: 18px; max-height: 96vh; }
    .scoring-modal-content { border-radius: 18px; max-height: 96vh; }
    .qr-modal { padding: 0.6rem; }
    .qr-modal-box { border-radius: 18px; max-width: 100%; }

    /* Títulos modales */
    .wc-modal-title { font-size: 1.7rem; }
    .sc-title        { font-size: 1.7rem; }

    /* Tabla en móvil: padding reducido */
    .sc-table th, .sc-table td { padding: 0.5rem 0.7rem; font-size: 0.8rem; }

    /* Scroll hint oculto en móvil muy pequeño */
    .scroll-hint { display: none; }

    /* Scoring summary */
    .sc-summary-row { font-size: 0.78rem; }
    .sc-summary-row .sr-pts { font-size: 0.95rem; }
  }

  /* ── PANTALLAS MUY ANCHAS (≥ 1400px) ── */
  @media (min-width: 1400px) {
    .container { max-width: 1100px; }
    .gallery-container { max-width: 1300px; }
    .gallery-grid { grid-template-columns: repeat(2, 1fr); }
  }

  /* ─── SCORING MODAL ─── */
  /* ─── SCORING MODAL (REGLAMENTO) ─── */
  .scoring-modal {
    display: none; position: fixed; inset: 0;
    background: rgba(3,8,16,0.92); backdrop-filter: blur(12px);
    z-index: 3000; align-items: center; justify-content: center;
    padding: 1.2rem; overflow-y: auto;
  }
  .scoring-modal.active { display: flex; animation: fadeIn 0.25s ease both; }
  @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  .scoring-modal-content {
    background: var(--dark3);
    border: 1px solid rgba(255,255,255,0.08); border-radius: 24px;
    max-width: 660px; width: 100%;
    position: relative; box-shadow: 0 0 100px rgba(0,87,183,0.22), 0 40px 80px rgba(0,0,0,0.8);
    animation: scaleIn 0.3s cubic-bezier(0.34,1.2,0.64,1) both;
    overflow: hidden; max-height: 92vh;
    display: flex; flex-direction: column;
  }
  @keyframes scaleIn { from { opacity: 0; transform: scale(0.9) translateY(28px); } to { opacity: 1; transform: scale(1) translateY(0); } }
  .scoring-modal-content.closing { animation: scaleOut 0.22s ease both; }
  @keyframes scaleOut { from { opacity:1; transform: scale(1); } to { opacity:0; transform: scale(0.93) translateY(16px); } }

  /* Stripe top */
  .sc-stripe { height: 4px; background: linear-gradient(90deg, var(--blue), var(--red), var(--green)); flex-shrink: 0; }

  /* Header */
  .sc-header { padding: 1.6rem 2rem 1rem; display: flex; align-items: flex-start; justify-content: space-between; gap: 1rem; flex-shrink: 0; }
  .sc-header-left { display: flex; flex-direction: column; gap: 0.4rem; }
  .sc-badge { font-family: 'Barlow Condensed', sans-serif; font-size: 0.68rem; font-weight: 700; letter-spacing: 0.35em; text-transform: uppercase; padding: 0.28rem 0.9rem; border-radius: 999px; color: #F5A623; background: rgba(245,166,35,0.1); border: 1px solid rgba(245,166,35,0.35); width: fit-content; }
  .sc-title { font-family: 'Bebas Neue', sans-serif; font-size: clamp(1.8rem, 4.5vw, 2.4rem); color: var(--white); line-height: 1; letter-spacing: 0.03em; }
  .sc-close-x { width: 36px; height: 36px; flex-shrink: 0; display: flex; align-items: center; justify-content: center; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 50%; cursor: pointer; color: rgba(240,246,255,0.45); transition: background 0.15s, color 0.15s, transform 0.15s; line-height: 1; font-size: 0.85rem; }
  .sc-close-x:hover { background: rgba(255,255,255,0.12); color: var(--white); transform: rotate(90deg); }

  /* Body scrollable */
  .sc-body { padding: 0 2rem 1.5rem; overflow-y: auto; scrollbar-width: thin; scrollbar-color: rgba(0,87,183,0.4) transparent; }
  .sc-body::-webkit-scrollbar { width: 4px; }
  .sc-body::-webkit-scrollbar-thumb { background: rgba(0,87,183,0.4); border-radius: 4px; }

  /* Section labels */
  .sc-label { font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem; font-weight: 700; letter-spacing: 0.4em; text-transform: uppercase; margin: 1.5rem 0 0.75rem; display: flex; align-items: center; gap: 0.6rem; }
  .sc-label::after { content: ''; flex: 1; height: 1px; background: rgba(255,255,255,0.08); }

  /* Rule principal */
  .sc-rule-box { background: rgba(0,87,183,0.1); border: 1px solid rgba(0,87,183,0.3); border-left: 3px solid var(--blue); border-radius: 0 12px 12px 0; padding: 1rem 1.2rem; margin-bottom: 1rem; font-size: 0.9rem; color: rgba(240,246,255,0.85); line-height: 1.65; }
  .sc-rule-box strong { color: var(--white); }

  /* Ejemplos */
  .sc-examples { display: flex; flex-direction: column; gap: 0.6rem; margin-bottom: 1rem; }
  .sc-example { background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.07); border-radius: 12px; padding: 0.85rem 1rem; font-size: 0.82rem; line-height: 1.6; color: rgba(240,246,255,0.65); }
  .sc-example .ex-title { font-family: 'Barlow Condensed', sans-serif; font-weight: 700; font-size: 0.8rem; color: rgba(240,246,255,0.5); letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 0.4rem; }
  .sc-example .match { font-family: 'Barlow Condensed', sans-serif; font-size: 1rem; font-weight: 700; color: var(--white); margin-bottom: 0.3rem; }
  .sc-example .ex-ok  { color: var(--green-light); }
  .sc-example .ex-no  { color: rgba(232,0,45,0.75); }
  .sc-example .ex-total { font-weight: 700; color: #F5A623; margin-top: 0.3rem; }

  /* Tabla de puntos — fondo sólido para visibilidad en GitHub Pages */
  .sc-table {
    width: 100%; border-collapse: collapse; margin-bottom: 1rem;
    font-size: 0.85rem;
    background: #0D1826;
    border-radius: 12px; overflow: hidden;
    border: 1px solid rgba(0,87,183,0.35);
  }
  .sc-table thead { background: #0A1020; }
  .sc-table th {
    font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem;
    font-weight: 700; letter-spacing: 0.25em; text-transform: uppercase;
    color: #4A90FF; padding: 0.65rem 1rem; text-align: left;
    border-bottom: 2px solid rgba(0,87,183,0.4);
  }
  .sc-table td {
    padding: 0.5rem 1rem; color: #C8D8F0;
    border-bottom: 1px solid rgba(255,255,255,0.06);
    background: #0D1826;
  }
  .sc-table tr:last-child td { border-bottom: none; }
  .sc-table tr:nth-child(even) td { background: #101E30; }
  .sc-table td:last-child {
    color: #F5A623; font-weight: 700;
    font-family: 'Barlow Condensed', sans-serif; font-size: 1.05rem;
  }

  /* Bonus grid */
  .sc-bonus-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.7rem; margin-bottom: 1rem; }
  @media (max-width: 480px) { .sc-bonus-grid { grid-template-columns: 1fr; } }
  .sc-bonus-card { background: rgba(0,87,183,0.07); border: 1px solid rgba(0,87,183,0.2); border-radius: 12px; padding: 0.9rem 1rem; display: flex; align-items: flex-start; gap: 0.65rem; }
  .sc-bonus-card .bc-icon { font-size: 1.4rem; flex-shrink: 0; }
  .sc-bonus-card .bc-text { font-size: 0.8rem; color: rgba(240,246,255,0.6); line-height: 1.5; }
  .sc-bonus-card .bc-pts { font-family: 'Bebas Neue', sans-serif; font-size: 1.4rem; color: #F5A623; line-height: 1; }
  .sc-bonus-card .bc-label { font-family: 'Barlow Condensed', sans-serif; font-size: 0.72rem; font-weight: 700; color: rgba(240,246,255,0.75); margin-bottom: 0.15rem; }

  /* Colombia especial */
  .sc-colombia { background: linear-gradient(135deg, rgba(252,209,22,0.08), rgba(0,87,183,0.08), rgba(206,43,55,0.06)); border: 1px solid rgba(252,209,22,0.25); border-radius: 14px; padding: 1.1rem 1.2rem; margin-bottom: 1rem; }
  .sc-colombia-head { display: flex; align-items: center; gap: 0.6rem; margin-bottom: 0.6rem; }
  .sc-colombia-head span { font-family: 'Bebas Neue', sans-serif; font-size: 1.1rem; color: #FCD116; letter-spacing: 0.05em; }
  .sc-colombia-rule { font-size: 0.85rem; color: rgba(240,246,255,0.7); line-height: 1.65; }
  .sc-colombia-rule strong { color: #FCD116; }

  /* Resumen final */
  .sc-summary { background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.08); border-radius: 14px; overflow: hidden; margin-bottom: 0.5rem; }
  .sc-summary-row { display: flex; align-items: center; justify-content: space-between; padding: 0.55rem 1rem; font-size: 0.85rem; color: rgba(240,246,255,0.65); border-bottom: 1px solid rgba(255,255,255,0.05); }
  .sc-summary-row:last-child { border-bottom: none; }
  .sc-summary-row .sr-pts { font-family: 'Bebas Neue', sans-serif; font-size: 1.1rem; color: #F5A623; }

  /* Footer */
  .sc-footer { padding: 1rem 2rem 1.5rem; display: flex; justify-content: center; flex-shrink: 0; border-top: 1px solid rgba(255,255,255,0.05); }
  .sc-close-btn { font-family: 'Barlow Condensed', sans-serif; font-size: 0.95rem; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; padding: 0.7rem 2.4rem; border: 1.5px solid rgba(240,246,255,0.25); border-radius: 999px; background: transparent; color: var(--white); cursor: pointer; transition: border-color 0.15s, background 0.15s, transform 0.15s; }
  .sc-close-btn:hover { border-color: var(--white); background: rgba(255,255,255,0.06); transform: translateY(-1px); }

  /* Compat aliases (por si algo del HTML antiguo los referencia) */
  .scoring-badge { display: none; }
  .scoring-modal-title { display: none; }
  .scoring-modal-text { display: none; }
  .scoring-close-btn { display: none; }
  .scoring-modal-close-x { display: none; }

  /* ─── WC MODALS (Premiaciones / Fases) ─── */
  .wc-modal {
    display: none; position: fixed; inset: 0;
    background: rgba(3,8,16,0.9); backdrop-filter: blur(12px);
    z-index: 2000; align-items: center; justify-content: center;
    padding: 1.2rem; overflow-y: auto;
  }
  .wc-modal.active { display: flex; animation: modalFadeIn 0.25s ease both; }
  @keyframes modalFadeIn { from { opacity: 0; } to { opacity: 1; } }
  .wc-modal-box {
    background: var(--dark3); border: 1px solid rgba(255,255,255,0.08);
    border-radius: 24px; max-width: 600px; width: 100%;
    position: relative; box-shadow: 0 0 100px rgba(0,87,183,0.22), 0 40px 80px rgba(0,0,0,0.8);
    animation: modalSlideIn 0.3s cubic-bezier(0.34,1.2,0.64,1) both;
    overflow: hidden; max-height: 92vh;
    display: flex; flex-direction: column;
  }
  @keyframes modalSlideIn { from { opacity: 0; transform: scale(0.9) translateY(28px); } to { opacity: 1; transform: scale(1) translateY(0); } }
  .wc-modal-box.closing { animation: modalSlideOut 0.22s ease both; }
  @keyframes modalSlideOut { from { opacity: 1; transform: scale(1); } to { opacity: 0; transform: scale(0.93) translateY(16px); } }
  .wc-modal-stripe { height: 4px; background: linear-gradient(90deg, var(--blue), var(--red), var(--green)); flex-shrink: 0; }
  .wc-modal-header { padding: 1.8rem 2rem 1.2rem; display: flex; align-items: flex-start; justify-content: space-between; gap: 1rem; flex-shrink: 0; }
  .wc-modal-header-left { display: flex; flex-direction: column; gap: 0.4rem; }
  .wc-modal-badge { font-family: 'Barlow Condensed', sans-serif; font-size: 0.68rem; font-weight: 700; letter-spacing: 0.35em; text-transform: uppercase; padding: 0.28rem 0.9rem; border-radius: 999px; }
  .badge-gold  { color: #F5C518; background: rgba(245,197,24,0.12); border: 1px solid rgba(245,197,24,0.35); }
  .badge-green { color: var(--green-light); background: rgba(0,184,76,0.1); border: 1px solid rgba(0,184,76,0.3); }
  .wc-modal-title { font-family: 'Bebas Neue', sans-serif; font-size: clamp(1.8rem, 4.5vw, 2.4rem); color: var(--white); line-height: 1; letter-spacing: 0.03em; }
  .wc-modal-close { width: 36px; height: 36px; flex-shrink: 0; display: flex; align-items: center; justify-content: center; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 50%; cursor: pointer; color: rgba(240,246,255,0.45); transition: background 0.15s, color 0.15s, transform 0.15s; line-height: 1; }
  .wc-modal-close:hover { background: rgba(255,255,255,0.12); color: var(--white); transform: rotate(90deg); }
  .wc-modal-body { padding: 0 2rem 2rem; overflow-y: auto; scrollbar-width: thin; scrollbar-color: rgba(0,87,183,0.4) transparent; }
  .wc-modal-body::-webkit-scrollbar { width: 4px; }
  .wc-modal-body::-webkit-scrollbar-thumb { background: rgba(0,87,183,0.4); border-radius: 4px; }
  .wc-section-label { font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem; font-weight: 700; letter-spacing: 0.4em; text-transform: uppercase; margin: 1.6rem 0 0.8rem; display: flex; align-items: center; color: rgba(240,246,255,0.6); }
  .wc-section-label::after { content: ''; flex: 1; height: 1px; background: rgba(255,255,255,0.08); }

  /* Prize cards */
  .prize-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 0.9rem; margin-bottom: 1.4rem; }
  @media (max-width: 480px) { .prize-grid { grid-template-columns: 1fr; } }
  .prize-card { border-radius: 16px; padding: 1.4rem 1rem; text-align: center; border: 1px solid transparent; position: relative; overflow: hidden; }
  .prize-card::before { content: ''; position: absolute; top:0; left:0; right:0; height:3px; border-radius: 16px 16px 0 0; }
  .prize-card.gold   { background: rgba(245,197,24,0.08); border-color: rgba(245,197,24,0.25); }
  .prize-card.silver { background: rgba(180,190,200,0.07); border-color: rgba(180,190,200,0.2); }
  .prize-card.bronze { background: rgba(205,127,50,0.08); border-color: rgba(205,127,50,0.22); }
  .prize-card.gold::before   { background: linear-gradient(90deg,#B8860B,#F5C518,#B8860B); }
  .prize-card.silver::before { background: linear-gradient(90deg,#888,#C0C8D0,#888); }
  .prize-card.bronze::before { background: linear-gradient(90deg,#8B4513,#CD7F32,#8B4513); }
  .prize-medal { font-size: 2rem; margin-bottom: 0.4rem; display: block; }
  .prize-place { font-family: 'Barlow Condensed', sans-serif; font-size: 0.65rem; font-weight: 700; letter-spacing: 0.3em; text-transform: uppercase; margin-bottom: 0.3rem; }
  .prize-card.gold   .prize-place { color: #F5C518; }
  .prize-card.silver .prize-place { color: #C0C8D0; }
  .prize-card.bronze .prize-place { color: #CD7F32; }
  .prize-pct { font-family: 'Bebas Neue', sans-serif; font-size: 2.2rem; line-height: 1; }
  .prize-card.gold   .prize-pct { color: #F5C518; }
  .prize-card.silver .prize-pct { color: #C0C8D0; }
  .prize-card.bronze .prize-pct { color: #CD7F32; }
  .prize-desc { font-size: 0.75rem; color: rgba(240,246,255,0.5); margin-top: 0.25rem; line-height: 1.45; }

  /* Tie cards */
  .tie-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.85rem; margin-bottom: 1rem; }
  @media (max-width: 420px) { .tie-grid { grid-template-columns: 1fr; } }
  .tie-card { background: rgba(0,87,183,0.07); border: 1px solid rgba(0,87,183,0.2); border-radius: 14px; padding: 1.1rem 1rem; display: flex; align-items: flex-start; gap: 0.75rem; }
  .tie-icon { font-size: 1.5rem; flex-shrink: 0; }
  .tie-title { font-family: 'Barlow Condensed', sans-serif; font-weight: 700; font-size: 0.9rem; margin-bottom: 0.25rem; color: var(--white); }
  .tie-text { font-size: 0.78rem; color: rgba(240,246,255,0.5); line-height: 1.5; }

  /* Phase blocks */
  .phase-block { background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.08); border-radius: 18px; padding: 1.4rem 1.5rem; margin-bottom: 1.1rem; position: relative; overflow: hidden; }
  .phase-block::before { content: ''; position: absolute; top:0; left:0; bottom:0; width:3px; border-radius: 18px 0 0 18px; }
  .phase-block.phase-1::before { background: var(--blue); }
  .phase-block.phase-2::before { background: var(--green-light); }
  .phase-block-head { display: flex; align-items: center; gap: 0.8rem; margin-bottom: 1rem; }
  .phase-num { font-family: 'Bebas Neue', sans-serif; font-size: 2.5rem; line-height: 1; opacity: 0.15; position: absolute; top: 0.6rem; right: 1rem; }
  .phase-icon { font-size: 1.6rem; }
  .phase-tag { font-family: 'Barlow Condensed', sans-serif; font-size: 0.6rem; font-weight: 700; letter-spacing: 0.35em; text-transform: uppercase; margin-bottom: 0.1rem; }
  .phase-block.phase-1 .phase-tag { color: var(--blue-light); }
  .phase-block.phase-2 .phase-tag { color: var(--green-light); }
  .phase-name { font-family: 'Barlow Condensed', sans-serif; font-size: 1.1rem; font-weight: 700; color: var(--white); }
  .phase-desc { font-size: 0.88rem; color: rgba(240,246,255,0.6); line-height: 1.65; margin-bottom: 0.85rem; }
  .phase-list { list-style: none; padding: 0; margin: 0; display: flex; flex-direction: column; gap: 0.4rem; }
  .phase-list li { font-size: 0.84rem; color: rgba(240,246,255,0.65); display: flex; align-items: flex-start; gap: 0.55rem; line-height: 1.5; }
  .phase-list li span.icon { flex-shrink: 0; }
  .scoring-pill { display: inline-flex; align-items: center; gap: 0.4rem; font-family: 'Barlow Condensed', sans-serif; font-size: 0.72rem; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase; padding: 0.35rem 0.9rem; border-radius: 999px; }
  .pill-blue  { background: rgba(0,87,183,0.18); border: 1px solid rgba(0,87,183,0.4); color: var(--blue-light); }
  .pill-green { background: rgba(0,122,53,0.18); border: 1px solid rgba(0,184,76,0.35); color: var(--green-light); }
  .responsible-row { display: flex; gap: 0.7rem; flex-wrap: wrap; margin-top: 0.8rem; }
  .responsible-tag { display: inline-flex; align-items: center; gap: 0.4rem; font-size: 0.8rem; font-weight: 600; background: rgba(0,122,53,0.12); border: 1px solid rgba(0,184,76,0.28); color: var(--green-light); padding: 0.4rem 0.75rem; border-radius: 6px; }
  .wc-modal-footer { padding: 1rem 2rem 1.5rem; display: flex; justify-content: center; flex-shrink: 0; border-top: 1px solid rgba(255,255,255,0.05); margin-top: 0.5rem; }
  .wc-close-btn { font-family: 'Barlow Condensed', sans-serif; font-size: 0.95rem; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; padding: 0.7rem 2.4rem; border: 1.5px solid rgba(240,246,255,0.25); border-radius: 999px; background: transparent; color: var(--white); cursor: pointer; transition: border-color 0.15s, background 0.15s, transform 0.15s; }
  .wc-close-btn:hover { border-color: var(--white); color: var(--white); background: rgba(255,255,255,0.06); transform: translateY(-1px); }
</style>
</head>
<body>

<!-- ══════ HERO ══════ -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="ball b1"></div><div class="ball b2"></div>
  <div class="ball b3"></div><div class="ball b4"></div>
  <div style="position:relative;z-index:2;">
    <div class="hero-label">⚽ Operaciones &amp; Logística · FIFA World Cup 2026</div>
    <h1 class="hero-title">
      <span class="blue">PORRA</span><br>
      <span class="red">MUNDIALISTA</span><br>
      <span>2026</span>
    </h1>
    <p class="hero-subtitle">El Torneo de Predicciones del Área</p>
    <p class="hero-tagline">En Operaciones Logísticas Unidad, queremos convertir esta experiencia en una actividad para compartir, disfrutar y fortalecer el trabajo en equipo. Más allá de los resultados, esta es una oportunidad para demostrar tu visión, tu precisión y tu capacidad para anticiparte a cada jugada.</p>
    <div class="hero-cta">
      <button onclick="document.getElementById('requisitos').scrollIntoView({behavior:'smooth'})" class="btn btn-primary">📥 Quiero participar</button>
      <button onclick="document.getElementById('comite').scrollIntoView({behavior:'smooth'})" class="btn btn-outline">Ver el comité</button>
    </div>
    <div class="hero-cta" style="margin-top:1rem;">
      <button onclick="openModal('modal-premiacion')" class="btn btn-info">🏆 Premiaciones</button>
      <button onclick="openModal('modal-fases')" class="btn btn-phases">📊 Fases del Evento</button>
    </div>
  </div>
  <div class="scroll-hint"><div class="scroll-line"></div>scroll</div>
</section>

<!-- ══════ GALLERY SECTION ══════ -->
<!-- 
  ✅ CORRECCIÓN APLICADA:
  Los nombres originales (stadium.jpg / player.jpg) no existen en el repositorio.
  Los archivos reales en GitHub son:
    - "ChatGPT Image 1 jun 2026, 08_21_29.png"
    - "ChatGPT Image 2 jun 2026, 09_46_49.png"
  RECOMENDACIÓN: Renombra esos archivos en GitHub a "stadium.png" y "player.png"
  para evitar problemas con espacios y comas en la URL. Luego actualiza los src abajo.
  Si NO los renombras, usa los nombres codificados como se muestra en el atributo src.
-->
<section class="gallery-section">
  <div class="gallery-container">
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="ChatGPT%20Image%201%20jun%202026%2C%2008_21_29.png" alt="Estadio lleno de afición mundialista">
        <div class="gallery-overlay">
          <span class="gallery-label">🏟️ LA PASIÓN</span>
        </div>
      </div>
      <div class="gallery-item">
        <img src="ChatGPT%20Image%202%20jun%202026%2C%2009_46_49.png" alt="Jugador en acción - Copa Mundial 2026">
        <div class="gallery-overlay">
          <span class="gallery-label">⚽ LA TÉCNICA</span>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ══════ REQUISITOS ══════ -->
<section class="req-section" id="requisitos">
  <div class="container">
    <div class="section-tag">📝 Hoja de ruta</div>
    <h2 class="section-title">Requisitos para<br>Participar</h2>
    <p class="section-intro">Cuatro pasos simples para asegurar tu cupo en el torneo más épico del área.</p>
    <div class="req-grid">
      <div class="req-card"><div class="req-num">1</div><div class="req-icon">💰</div><div class="req-label">Paso 1</div><div class="req-title">Inversión</div><p class="req-text">El valor de inscripción es <span class="req-highlight">$20.000</span> COP por participante.</p></div>
      <div class="req-card"><div class="req-num">2</div><div class="req-icon">📅</div><div class="req-label">Paso 2</div><div class="req-title">Fecha Límite</div><p class="req-text">Tienes plazo máximo hasta <span class="req-highlight">10 de junio de 2026</span> para inscribirse.</p></div>
      <div class="req-card"><div class="req-num">3</div><div class="req-icon">📊</div><div class="req-label">Paso 3</div><div class="req-title">Tu Pronóstico</div><p class="req-text">Descarga y llena el archivo Excel con tus predicciones del mundial.</p></div>
      <div class="req-card"><div class="req-num">4</div><div class="req-icon">📧</div><div class="req-label">Paso 4</div><div class="req-title">Envío</div><p class="req-text">Envía tu Excel diligenciado a los responsables del evento.</p></div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ══════ PAGOS ══════ -->
<section class="pay-section" id="pagos">
  <div class="container">
    <div class="section-tag">💳 Métodos habilitados</div>
    <h2 class="section-title">¿Cómo pago?</h2>
    <p class="section-intro">Elige el método que más te convenga. Recuerda siempre enviar el comprobante para validar tu participación.</p>
    <div class="pay-grid">
      <div class="pay-card digital">
        <div class="pay-icon">📱</div>
        <div class="pay-type">Opción A</div>
        <div class="pay-title">Pago Digital<br>QR Bancario</div>
        <p class="pay-desc">Escanea el código QR adjunto en el correo para realizar tu pago de forma rápida y segura.</p>
        <div class="pay-detail">📲 Envía el comprobante por WhatsApp al<br><strong style="font-size:1.05rem;">322 363 6928</strong></div>
      </div>
      <div class="pay-card cash">
        <div class="pay-icon">💵</div>
        <div class="pay-type">Opción B</div>
        <div class="pay-title">Pago en<br>Efectivo</div>
        <p class="pay-desc">Entrega el valor de inscripción directamente a la tesorera del evento.</p>
        <div class="pay-detail">🙋‍♀️ Entregar directamente a:<br><strong style="font-size:1.05rem;">Francia Motta</strong></div>
      </div>
    </div>

    <!-- ✅ QR: botón que abre modal -->
    <div class="qr-btn-wrap">
      <button class="btn-qr" onclick="openQrModal()">
        <span class="qr-dot"></span>
        📲 Ver QR de pago
      </button>
    </div>

    <div class="alert">
      <div class="alert-icon">📌</div>
      <div class="alert-text"><strong>¡Importante!</strong> Asegúrate de registrar tu pago correctamente y enviar el soporte para validar tu participación. Si no hay soporte o entrega, <strong>la participación no será válida</strong>.</div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ══════ COMITÉ ══════ -->
<section class="committee-section" id="comite">
  <div class="container">
    <div class="section-tag">⚖️ Comité Organizador</div>
    <h2 class="section-title">Transparencia<br>Total</h2>
    <p class="section-intro">Para garantizar que esta operación sea tan exacta como nuestros inventarios, contamos con un equipo asignado.</p>
    <div class="committee-grid">
      <div class="committee-card"><div class="committee-avatar admin">🏃‍♂️</div><div class="committee-role">Administrador</div><div class="committee-name">Sebastián Díaz</div><p class="committee-desc">Gestiona el torneo, valida los pagos y coordina el evento completo.</p></div>
      <div class="committee-card"><div class="committee-avatar audit">🔍</div><div class="committee-role">Auditora de Resultados</div><div class="committee-name">Laura Xiomara</div><p class="committee-desc">Verifica los pronósticos y calcula los resultados finales de forma imparcial.</p></div>
      <div class="committee-card"><div class="committee-avatar treasury">💰</div><div class="committee-role">Tesorera</div><div class="committee-name">Francia Motta</div><p class="committee-desc">Gestiona los fondos recaudados y distribuye los premios según las reglas.</p></div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ══════ FOOTER ══════ -->
<section class="footer-section">
  <div class="container">
    <div class="deadline-box">
      <div class="deadline-label">⏰ Fecha límite de inscripción</div>
      <div class="deadline-date">Miércoles 10 de Junio</div>
      <div class="deadline-sub">No pierdas tu cupo — cupos limitados</div>
    </div>
    <div class="trophy-line"><span class="trophy-emoji">🏆</span></div>
    <h2 class="footer-title">¿Estás listo para demostrar<br>quién es el verdadero estratega?</h2>
    <p class="footer-sub">Descarga tu Excel, asegura tu cupo con Francia y <strong style="color:var(--blue-light)">¡que empiece el juego!</strong></p>
    <div class="hero-cta footer-cta">
      <button onclick="openScoringModal()" class="btn btn-scoring">📋 ¿Cómo se calificarán los resultados?</button>
    </div>
    <div class="scoring-teaser">⚡ Reglamento oficial publicado — ¡ya puedes consultarlo!</div>
    <p class="footer-committee">© 2026 · Comité Organizador Mundialista · Operaciones &amp; Logística</p>
  </div>
</section>

<!-- ══════ MODAL: QR DE PAGO ══════ -->
<div id="qr-modal" class="qr-modal" onclick="if(event.target===this)closeQrModal()">
  <div class="qr-modal-box">
    <div class="qr-modal-stripe"></div>
    <div class="qr-modal-header">
      <span class="qr-modal-title">💳 QR de Pago</span>
      <button class="qr-modal-close" onclick="closeQrModal()">✕</button>
    </div>
    <div class="qr-modal-body">
      <div class="qr-img-frame">
        <img src="imagen%20(15).png" alt="Código QR de pagos - Porra Mundialista 2026">
      </div>
      <p class="qr-modal-hint">
        Escanea este código con tu app bancaria.<br>
        Luego envía el comprobante por WhatsApp al<br>
        <strong>322 363 6928</strong>
      </p>
    </div>
    <div class="qr-modal-footer">
      <button class="qr-close-btn" onclick="closeQrModal()">Cerrar</button>
    </div>
  </div>
</div>

<!-- ══════ MODAL: SCORING / REGLAMENTO ══════ -->
<div id="scoring-modal" class="scoring-modal" onclick="if(event.target===this)closeScoringModal()">
  <div class="scoring-modal-content">

    <div class="sc-stripe"></div>

    <!-- Header -->
    <div class="sc-header">
      <div class="sc-header-left">
        <span class="sc-badge">📋 Reglamento Oficial</span>
        <h3 class="sc-title">Sistema de<br>Puntuación</h3>
      </div>
      <button class="sc-close-x" onclick="closeScoringModal()">✕</button>
    </div>

    <!-- Body -->
    <div class="sc-body">

      <!-- REGLA PRINCIPAL -->
      <div class="sc-label" style="color:var(--blue-light);">🎯 Regla principal</div>
      <div class="sc-rule-box">
        Cada <strong>gol acertado</strong> en el marcador final equivale a <strong>1 punto</strong>.<br>
        No es obligatorio acertar el resultado completo para sumar puntos.
      </div>

      <!-- EJEMPLOS MARCADORES -->
      <div class="sc-label" style="color:rgba(240,246,255,0.5);">📌 Ejemplos de puntuación</div>
      <div class="sc-examples">
        <div class="sc-example">
          <div class="ex-title">Ej. 1 · Marcador exacto</div>
          <div class="match">🇨🇴 Colombia 2 – 0 Brasil 🇧🇷</div>
          <div class="ex-title">Ej. 1 · Marcador Pronosticado</div>
          <div class="match">🇨🇴 Colombia 2 – 0 Brasil 🇧🇷</div>
          <div class="ex-ok">✅ 2 goles Colombia = 2 pts &nbsp;|&nbsp; ✅ 0 goles Brasil = 1 pt</div>
          <div class="ex-total">Total: 3 puntos</div>
        </div>
        <div class="sc-example">
          <div class="ex-title">Ej. 2 · Solo acertó un equipo</div>
          <div class="match">🇨🇴 Colombia 2 – 0 Brasil 🇧🇷 &nbsp;·&nbsp; Real: 2–1</div>
          <div class="ex-ok">✅ 2 goles Colombia = 2 pts</div>
          <div class="ex-no">❌ No acertó goles de Brasil</div>
          <div class="ex-total">Total: 2 puntos</div>
        </div>
        <div class="sc-example">
          <div class="ex-title">Ej. 3 · Sin aciertos</div>
          <div class="match">Pronóstico 1–0 &nbsp;·&nbsp; Real: 2–3</div>
          <div class="ex-no">❌ No acertó ningún marcador</div>
          <div class="ex-total">Total: 0 puntos</div>
        </div>
      </div>

      <!-- TABLA RÁPIDA -->
      <div class="sc-label" style="color:var(--blue-light);">📊 Tabla rápida</div>
      <table class="sc-table">
        <thead><tr><th>Goles acertados</th><th>Puntos</th></tr></thead>
        <tbody>
          <tr><td>0 goles</td><td>0</td></tr>
          <tr><td>1 gol</td><td>1</td></tr>
          <tr><td>2 goles</td><td>2</td></tr>
          <tr><td>3 goles</td><td>3</td></tr>
          <tr><td>4 goles</td><td>4</td></tr>
          <tr><td>5+ goles</td><td>5+</td></tr>
        </tbody>
      </table>

      <!-- BONUS -->
      <div class="sc-label" style="color:#F5A623;">⭐ Puntos Bonus</div>
      <div class="sc-bonus-grid">
        <div class="sc-bonus-card">
          <div class="bc-icon">🏅</div>
          <div>
            <div class="bc-label">Acertar ganador / empate</div>
            <div class="bc-pts">+2</div>
            <div class="bc-text">Por cada partido donde aciertes quién gana o si termina en empate.</div>
          </div>
        </div>
        <div class="sc-bonus-card">
          <div class="bc-icon">⚽</div>
          <div>
            <div class="bc-label">Clasificado a 1/16 correcto</div>
            <div class="bc-pts">+2</div>
            <div class="bc-text">Por cada selección que pronosticaste clasificar a los dieciseisavos.</div>
          </div>
        </div>
        <div class="sc-bonus-card">
          <div class="bc-icon">🏆</div>
          <div>
            <div class="bc-label">Acertar Campeón</div>
            <div class="bc-pts">+5</div>
            <div class="bc-text">Si aciertas el equipo campeón del mundo.</div>
          </div>
        </div>
        <div class="sc-bonus-card">
          <div class="bc-icon">🥈</div>
          <div>
            <div class="bc-label">Acertar Subcampeón</div>
            <div class="bc-pts">+3</div>
            <div class="bc-text">Si aciertas el equipo finalista perdedor.</div>
          </div>
        </div>
        <div class="sc-bonus-card" style="grid-column: span 2;">
          <div class="bc-icon">🥉</div>
          <div>
            <div class="bc-label">Acertar Tercer Lugar</div>
            <div class="bc-pts">+2</div>
            <div class="bc-text">Si aciertas el equipo que obtiene el tercer puesto del torneo.</div>
          </div>
        </div>
      </div>

      <!-- COLOMBIA ESPECIAL -->
      <div class="sc-label" style="color:#FCD116;">🇨🇴 Bonus especial – Partidos de Colombia</div>
      <div class="sc-colombia">
        <div class="sc-colombia-head">
          <span>⚽ Valor especial de goles</span>
        </div>
        <p class="sc-colombia-rule">
          En los partidos donde participe Colombia, cada gol acertado vale <strong>3 puntos</strong> en lugar de 1.<br><br>
          <strong>Ejemplo:</strong> Colombia 2–1 Japón acertado exactamente →<br>
          ✅ 2 goles Colombia = 6 pts &nbsp;|&nbsp; ✅ 1 gol Japón = 3 pts &nbsp;= <strong style="color:#FCD116;">9 puntos</strong><br><br>
          El bono de <strong>+2 por acertar ganador/empate también aplica</strong> en estos partidos.
        </p>
      </div>

      <!-- RESUMEN GENERAL -->
      <div class="sc-label" style="color:rgba(240,246,255,0.5);">📋 Resumen de bonificaciones</div>
      <div class="sc-summary">
        <div class="sc-summary-row"><span>Acertar ganador del partido</span><span class="sr-pts">+2</span></div>
        <div class="sc-summary-row"><span>Acertar empate del partido</span><span class="sr-pts">+2</span></div>
        <div class="sc-summary-row"><span>Cada clasificado correcto a 1/16</span><span class="sr-pts">+2</span></div>
        <div class="sc-summary-row"><span>Acertar campeón del Mundial</span><span class="sr-pts">+5</span></div>
        <div class="sc-summary-row"><span>Acertar subcampeón</span><span class="sr-pts">+3</span></div>
        <div class="sc-summary-row"><span>Acertar tercer lugar</span><span class="sr-pts">+2</span></div>
        <div class="sc-summary-row" style="background:rgba(252,209,22,0.05);"><span>🇨🇴 Gol acertado en partido de Colombia</span><span class="sr-pts" style="color:#FCD116;">×3</span></div>
      </div>

    </div><!-- /sc-body -->

    <div class="sc-footer">
      <button class="sc-close-btn" onclick="closeScoringModal()">Cerrar</button>
    </div>

  </div>
</div>

<!-- ══════ MODAL: PREMIACIONES ══════ -->
<div id="modal-premiacion" class="wc-modal" onclick="if(event.target===this)closeModal('modal-premiacion')">
  <div class="wc-modal-box">
    <div class="wc-modal-stripe"></div>
    <div class="wc-modal-header">
      <div class="wc-modal-header-left">
        <span class="wc-modal-badge badge-gold">🎯 Premiación Oficial</span>
        <h3 class="wc-modal-title">Distribución<br>de Premios</h3>
      </div>
      <button class="wc-modal-close" onclick="closeModal('modal-premiacion')">✕</button>
    </div>
    <div class="wc-modal-body">
      <div class="wc-section-label" style="color:rgba(245,197,24,0.8);">🏅 Posiciones reconocidas</div>
      <div class="prize-grid">
        <div class="prize-card gold"><span class="prize-medal">🥇</span><div class="prize-place">Primer lugar</div><div class="prize-pct">70%</div><div class="prize-desc">del valor total recaudado</div></div>
        <div class="prize-card silver"><span class="prize-medal">🥈</span><div class="prize-place">Segundo lugar</div><div class="prize-pct">20%</div><div class="prize-desc">del valor total recaudado</div></div>
        <div class="prize-card bronze"><span class="prize-medal">🥉</span><div class="prize-place">Tercer lugar</div><div class="prize-pct">10%</div><div class="prize-desc">del valor total recaudado</div></div>
        <div class="prize-card bronze"><span class="prize-medal">🚨</span><div class="prize-place">Ultimo Lugar</div><div class="prize-pct">0%</div><div class="prize-desc">del valor total recaudado, pero con premio sorpresa</div></div>
      </div>
      <div class="wc-section-label" style="color:rgba(232,0,45,0.75);">⚖️ En caso de empate</div>
      <p style="font-size:0.88rem;color:rgba(240,246,255,0.6);line-height:1.7;margin-bottom:1rem;">Si dos o más participantes empatan en cualquiera de las posiciones premiadas, los involucrados podrán elegir entre:</p>
      <div class="tie-grid">
        <div class="tie-card"><div class="tie-icon">🎲</div><div><div class="tie-title">Nuevo sorteo</div><div class="tie-text">Se realizará un sorteo para definir a un único ganador dentro de la posición que se encuentra empatada.</div></div></div>
        <div class="tie-card"><div class="tie-icon">🤝</div><div><div class="tie-title">División igualitaria</div><div class="tie-text">El valor del premio correspondiente se divide en partes iguales entre todos los empatados.</div></div></div>
      </div>
    </div>
    <div class="wc-modal-footer"><button class="wc-close-btn" onclick="closeModal('modal-premiacion')">Cerrar</button></div>
  </div>
</div>

<!-- ══════ MODAL: FASES ══════ -->
<div id="modal-fases" class="wc-modal" onclick="if(event.target===this)closeModal('modal-fases')">
  <div class="wc-modal-box">
    <div class="wc-modal-stripe"></div>
    <div class="wc-modal-header">
      <div class="wc-modal-header-left">
        <span class="wc-modal-badge badge-green">📊 Estructura del Torneo</span>
        <h3 class="wc-modal-title">Fases del<br>Evento</h3>
      </div>
      <button class="wc-modal-close" onclick="closeModal('modal-fases')">✕</button>
    </div>
    <div class="wc-modal-body">
      <div class="phase-block phase-1">
        <div class="phase-num">01</div>
        <div class="phase-block-head"><div class="phase-icon">⚽</div><div class="phase-title-wrap"><div class="phase-tag">Fase 1</div><div class="phase-name">Fase de Grupos</div></div></div>
        <p class="phase-desc">Completa el <strong style="color:#F0F6FF">primer archivo de Excel</strong> enviado por correo electrónico con tus pronósticos para todos los partidos de la fase de grupos.</p>
        <div class="wc-section-label" style="color:#4A90FF;margin-top:0;">📋 Actividades requeridas</div>
        <ul class="phase-list">
          <li><span class="icon">⚽</span><span>Registrar los marcadores de todos los partidos de la fase de grupos.</span></li>
          <li><span class="icon">⚽</span><span></span>En caso de empate entre equipos, selecciona manualmente las posiciones para definir los clasificados a los dieciseisavos de final. Las opciones aparecerán  automáticamente en el archivo de Excel cuando sean necesarias.</li>
          <li><span class="icon">🥇</span><span>Pronosticar el equipo que será <strong style="color:#F0F6FF">Campeón</strong> del mundial.</span></li>
          <li><span class="icon">🥈</span><span>Pronosticar el equipo que será <strong style="color:#F0F6FF">Subcampeón</strong> del mundial.</span></li>
          <li><span class="icon">🥉</span><span>Pronosticar el equipo que ocupará el <strong style="color:#F0F6FF">tercer lugar</strong> del mundial.</span></li>
        </ul>
        <div class="wc-section-label" style="color:#4A90FF;margin-top:1rem;">🎯 Sistema de puntuación</div>
        <ul class="phase-list">
          <li><span class="icon">📈</span><span>Se asignan puntos según la precisión de cada pronóstico registrado.</span></li>
          <li><span class="icon">✅</span><span>A mayor exactitud en los resultados, <strong style="color:#F0F6FF">mayor puntuación obtenida</strong>.</span></li>
        </ul>
        <span class="scoring-pill pill-blue">⭐ Los puntos se acumulan en la Fase 2</span>
      </div>
      <div class="phase-block phase-2">
        <div class="phase-num">02</div>
        <div class="phase-block-head"><div class="phase-icon">🏆</div><div class="phase-title-wrap"><div class="phase-tag">Fase 2</div><div class="phase-name">Fase Eliminatoria</div></div></div>
        <p class="phase-desc">Una vez finalizada la fase de grupos, recibirás por correo un <strong style="color:#F0F6FF">segundo archivo de Excel</strong> para completar los pronósticos de la etapa eliminatoria.</p>
        <div class="wc-section-label" style="color:#00B84C;margin-top:0;">📋 Actividades requeridas</div>
        <ul class="phase-list">
          <li><span class="icon">⚽</span><span>Registrar los marcadores de <strong style="color:#F0F6FF">todos los encuentros</strong> de la fase eliminatoria.</span></li>
          <li><span class="icon">📧</span><span>El archivo será enviado por correo electrónico al iniciar esta fase.</span></li>
        </ul>
        <div class="wc-section-label" style="color:#00B84C;margin-top:1rem;">👥 Enviar el archivo a los responsables</div>
        <div class="responsible-row">
          <span class="responsible-tag">🏃‍♂️ Sebastián Díaz</span>
          <span class="responsible-tag">🔍 Laura Xiomara</span>
        </div>
        <span class="scoring-pill pill-green" style="margin-top:0.9rem;">🔗 Los puntos de la Fase 1 se suman aquí</span>
      </div>
    </div>
    <div class="wc-modal-footer"><button class="wc-close-btn" onclick="closeModal('modal-fases')">Cerrar</button></div>
  </div>
</div>

<script>
  function openQrModal() {
    var el = document.getElementById('qr-modal');
    el.classList.add('active');
    document.body.style.overflow = 'hidden';
  }
  function closeQrModal() {
    var el = document.getElementById('qr-modal');
    var box = el.querySelector('.qr-modal-box');
    if (box) {
      box.classList.add('closing');
      setTimeout(function() {
        el.classList.remove('active');
        box.classList.remove('closing');
        document.body.style.overflow = '';
      }, 200);
    } else {
      el.classList.remove('active');
      document.body.style.overflow = '';
    }
  }
  function openScoringModal() {
    document.getElementById('scoring-modal').classList.add('active');
    document.body.style.overflow = 'hidden';
  }
  function closeScoringModal() {
    document.getElementById('scoring-modal').classList.remove('active');
    document.body.style.overflow = '';
  }
  function openModal(id) {
    var el = document.getElementById(id);
    if (!el) return;
    el.classList.add('active');
    document.body.style.overflow = 'hidden';
    var b = el.querySelector('.wc-modal-body');
    if (b) b.scrollTop = 0;
  }
  function closeModal(id) {
    var el = document.getElementById(id);
    if (!el) return;
    var box = el.querySelector('.wc-modal-box');
    if (box) {
      box.classList.add('closing');
      setTimeout(function() {
        el.classList.remove('active');
        box.classList.remove('closing');
        document.body.style.overflow = '';
      }, 200);
    } else {
      el.classList.remove('active');
      document.body.style.overflow = '';
    }
  }
  document.addEventListener('keydown', function(e) {
    if (e.key !== 'Escape') return;
    closeQrModal();
    closeScoringModal();
    ['modal-premiacion','modal-fases'].forEach(function(id) {
      var el = document.getElementById(id);
      if (el && el.classList.contains('active')) closeModal(id);
    });
  });
</script>
</body>
</html>
   
   
