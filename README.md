<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#ffe4ee">
<title>Для Дианочки 💌</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Manrope:wght@400;500;600;700;800&display=swap');

:root {
  --pink: #ff4f87;
  --deep: #a81753;
  --cream: #fff8fb;
}
* { box-sizing: border-box; }
html, body { width: 100%; min-height: 100%; margin: 0; }
body {
  min-height: 100vh;
  overflow: hidden;
  display: grid;
  place-items: center;
  padding: 22px;
  font-family: 'Manrope', 'Segoe UI', sans-serif;
  color: var(--deep);
  background:
    radial-gradient(circle at 15% 15%, #fff 0 2px, transparent 3px),
    radial-gradient(circle at 82% 28%, #fff9 0 3px, transparent 4px),
    radial-gradient(ellipse at 15% 85%, #ffc1d8 0, transparent 38%),
    radial-gradient(ellipse at 85% 10%, #ffd6e5 0, transparent 35%),
    linear-gradient(135deg, #ffe9f1, #ffb8d0 52%, #ffdbe8);
  background-size: 120px 120px, 170px 170px, auto, auto, auto;
}
.glow {
  position: fixed; width: 360px; height: 360px; border-radius: 50%;
  filter: blur(70px); opacity: .5; pointer-events: none;
  animation: glow 8s ease-in-out infinite alternate;
}
.glow.one { background: #ff7fac; top: -150px; left: -120px; }
.glow.two { background: #fff; bottom: -180px; right: -100px; animation-delay: -4s; }
.card {
  position: relative; z-index: 2;
  width: min(100%, 690px);
  padding: clamp(34px, 7vw, 66px) clamp(22px, 6vw, 58px);
  text-align: center;
  border: 1px solid #ffffffd9;
  border-radius: 34px;
  background: linear-gradient(145deg, #ffffffd9, #fff7fbd9);
  box-shadow: 0 28px 80px #a8175326, inset 0 1px 0 #fff;
  backdrop-filter: blur(18px);
  animation: cardIn 1.1s cubic-bezier(.2,.8,.2,1) both;
}
.top-label {
  display: inline-flex; align-items: center; gap: 9px;
  padding: 9px 15px; border: 1px solid #ffb4cd;
  border-radius: 999px; background: #fff0f6;
  color: #c33d70; font-size: 11px; font-weight: 800;
  letter-spacing: .18em; text-transform: uppercase;
}
.mini-heart { color: var(--pink); font-size: 14px; animation: beat 1.2s infinite; }
.envelope-wrap {
  width: 106px; height: 106px; margin: 28px auto 24px;
  display: grid; place-items: center; position: relative;
  border-radius: 32px; transform: rotate(-5deg);
  background: linear-gradient(145deg, #ffdae7, #fff0f6);
  box-shadow: 0 12px 30px #e95b8c26, inset 0 0 0 1px #fff;
}
.envelope-wrap::before, .envelope-wrap::after {
  content: '♥'; position: absolute; color: #ff7da8;
  animation: orbit 5s ease-in-out infinite;
}
.envelope-wrap::before { font-size: 18px; top: -13px; right: -9px; }
.envelope-wrap::after { font-size: 12px; bottom: -9px; left: -12px; animation-delay: -2s; }
.envelope { font-size: 51px; filter: drop-shadow(0 5px 4px #c13e6a20); }
h1 {
  margin: 0 auto;
  max-width: 550px;
  font-size: clamp(28px, 5.2vw, 43px);
  line-height: 1.24;
  letter-spacing: -.045em;
  font-weight: 800;
  color: #a81753;
}
h1 span {
  display: inline-block;
  font-family: 'Great Vibes', 'Segoe Script', cursive;
  font-size: 1.25em;
  font-weight: 400;
  letter-spacing: 0;
  color: #f04480;
  text-shadow: 0 4px 18px #ff9fc24d;
}
.rule {
  width: 68px; height: 3px; margin: 25px auto 20px;
  border-radius: 9px;
  background: linear-gradient(90deg, #ff9abc, #ff4f87, #ffc0d5);
}
.subtitle {
  margin: 0;
  color: #b34c76;
  font-size: clamp(14px, 2.7vw, 16px);
  line-height: 1.8;
  font-weight: 500;
}
.bottom-hearts { margin-top: 25px; color: #f35a91; letter-spacing: 8px; font-size: 18px; }
.heart {
  position: fixed; z-index: 1; bottom: -70px; left: var(--x);
  color: var(--c); font-size: var(--s);
  opacity: 0; pointer-events: none;
  animation: floatUp var(--d) linear var(--delay) infinite;
  filter: drop-shadow(0 5px 8px #c52c6420);
}
.sparkle {
  position: fixed; z-index: 1; left: var(--x); top: var(--y);
  color: #fff; font-size: var(--s); opacity: .85;
  animation: twinkle var(--d) ease-in-out var(--delay) infinite alternate;
  pointer-events: none;
}
@keyframes floatUp {
  0% { transform: translate3d(0, 0, 0) rotate(-15deg) scale(.8); opacity: 0; }
  12% { opacity: .85; }
  85% { opacity: .65; }
  100% { transform: translate3d(var(--drift), -120vh, 0) rotate(25deg) scale(1.15); opacity: 0; }
}
@keyframes beat { 0%,100% { transform: scale(1); } 50% { transform: scale(1.28); } }
@keyframes cardIn { from { opacity: 0; transform: translateY(24px) scale(.97); } to { opacity: 1; transform: translateY(0) scale(1); } }
@keyframes glow { from { transform: scale(.9); } to { transform: scale(1.12); } }
@keyframes orbit { 0%,100% { transform: translateY(0) rotate(-8deg); } 50% { transform: translateY(-7px) rotate(10deg); } }
@keyframes twinkle { from { opacity: .25; transform: scale(.7) rotate(0deg); } to { opacity: 1; transform: scale(1.2) rotate(25deg); } }
@media (max-width: 480px) {
  .card { border-radius: 27px; }
  .envelope-wrap { width: 88px; height: 88px; border-radius: 27px; margin-top: 25px; }
  .envelope { font-size: 43px; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { animation-duration: .01ms !important; animation-iteration-count: 1 !important; }
}
</style>
</head>
<body>
<div class="glow one"></div>
<div class="glow two"></div>

<div class="card">
  <div class="top-label"><span class="mini-heart">♥</span> маленький сюрприз <span class="mini-heart">♥</span></div>
  <div class="envelope-wrap"><div class="envelope">💌</div></div>
  <h1>Спустись и проверь свой почтовый ящик,<br><span>Дианочка</span> ♥</h1>
  <div class="rule"></div>
  <p class="subtitle">Тебя там ждёт кое-что особенное…<br>Улыбнись, это для тебя 💗</p>
  <div class="bottom-hearts">♡ ♥ ♡</div>
</div>

<script>
const colors = ['#ff4f87', '#ff78a5', '#e83e78', '#ffa6c3', '#d92d6b'];
for (let i = 0; i < 22; i++) {
  const heart = document.createElement('div');
  heart.className = 'heart';
  heart.textContent = Math.random() > 0.25 ? '♥' : '♡';
  heart.style.setProperty('--x', Math.random() * 100 + 'vw');
  heart.style.setProperty('--s', (14 + Math.random() * 34) + 'px');
  heart.style.setProperty('--c', colors[Math.floor(Math.random() * colors.length)]);
  heart.style.setProperty('--d', (7 + Math.random() * 10) + 's');
  heart.style.setProperty('--delay', (-Math.random() * 17) + 's');
  heart.style.setProperty('--drift', (Math.random() * 100 - 50) + 'px');
  document.body.appendChild(heart);
}
for (let i = 0; i < 18; i++) {
  const star = document.createElement('div');
  star.className = 'sparkle';
  star.textContent = '✦';
  star.style.setProperty('--x', Math.random() * 100 + 'vw');
  star.style.setProperty('--y', Math.random() * 100 + 'vh');
  star.style.setProperty('--s', (8 + Math.random() * 13) + 'px');
  star.style.setProperty('--d', (1.5 + Math.random() * 3) + 's');
  star.style.setProperty('--delay', (-Math.random() * 4) + 's');
  document.body.appendChild(star);
}
</script>
</body>
</html>
