<!DOCTYPE html>
<html lang="mn">
<head>
 <meta charset="UTF-8" />
 <meta name="viewport" content="width=device-width, initial-scale=1.0" />
 <title>Ногоон хана төсөл</title>
 <style>
 * { box-sizing: border-box; margin: 0; padding: 0; }
 html { scroll-behavior: smooth; }
 body {
 font-family: Arial, sans-serif;
 background: linear-gradient(135deg, #071b11, #113322, #1f5c3c);
 color: #f4fff4;
 line-height: 1.6;
 overflow-x: hidden;
 }

 .bg-bubbles {
 position: fixed;
 inset: 0;
 pointer-events: none;
 z-index: 0;
 overflow: hidden;
 }
 .bubble {
 position: absolute;
 bottom: -100px;
 width: 24px;
 height: 24px;
 background: rgba(146, 255, 175, 0.08);
 border-radius: 50%;
 animation: rise 18s infinite linear;
 }
 .bubble:nth-child(1) { left: 6%; animation-duration: 14s; }
 .bubble:nth-child(2) { left: 18%; width: 16px; height: 16px; animation-duration: 20s; }
 .bubble:nth-child(3) { left: 34%; width: 28px; height: 28px; animation-duration: 17s; }
 .bubble:nth-child(4) { left: 52%; width: 22px; height: 22px; animation-duration: 21s; }
 .bubble:nth-child(5) { left: 68%; width: 18px; height: 18px; animation-duration: 16s; }
 .bubble:nth-child(6) { left: 82%; width: 30px; height: 30px; animation-duration: 22s; }
 .bubble:nth-child(7) { left: 92%; width: 15px; height: 15px; animation-duration: 19s; }


 @keyframes rise {
 from { transform: translateY(0) scale(1); opacity: 0; }
 10% { opacity: 1; }
 to { transform: translateY(-120vh) scale(1.4); opacity: 0; }
 }


 header, nav, section, footer { position: relative; z-index: 1; }


 header {
 min-height: 100vh;
 display: flex;
 align-items: center;
 justify-content: center;
 text-align: center;
 padding: 20px;
 position: relative;
 overflow: hidden;
 background:
 radial-gradient(circle at top, rgba(154,255,168,0.15), transparent 35%),
 linear-gradient(180deg, rgba(0,0,0,0.15), rgba(0,0,0,0.45));
 }
 .floating-leaf {
 position: absolute;
 width: 18px;
 height: 18px;
 background: rgba(132, 255, 161, 0.22);
 border-radius: 60% 40% 70% 30%;
 animation: floatLeaf 10s linear infinite;
 }
 .leaf1 { left: 10%; top: 15%; animation-delay: 0s; }
 .leaf2 { left: 75%; top: 20%; animation-delay: 2s; }
 .leaf3 { left: 20%; top: 70%; animation-delay: 4s; }
 .leaf4 { left: 85%; top: 75%; animation-delay: 1s; }


 @keyframes floatLeaf {
 0% { transform: translateY(0) rotate(0deg); opacity: 0.2; }
 50% { opacity: 0.8; }
 100% { transform: translateY(-120px) rotate(360deg); opacity: 0.1; }
 }


 .hero {
 max-width: 950px;
 z-index: 2;
 animation: fadeUp 1.2s ease;
 }
 @keyframes fadeUp {
 from { opacity: 0; transform: translateY(30px); }
 to { opacity: 1; transform: translateY(0); }
 }


 .hero h1 {
 font-size: 3.5rem;
 margin-bottom: 16px;
 color: #caffd0;
 text-shadow: 0 0 20px rgba(106, 255, 143, 0.35);
 animation: glow 2.4s infinite alternate;
 }
 @keyframes glow {
 from { text-shadow: 0 0 10px rgba(106,255,143,0.25); }
 to { text-shadow: 0 0 28px rgba(106,255,143,0.55); }
 }


 .hero p {
 font-size: 1.1rem;
 max-width: 760px;
 margin: 0 auto 24px;
 color: #e9ffe9;
 }
 .hero-buttons {
 display: flex;
 gap: 14px;
 justify-content: center;
 flex-wrap: wrap;
 }
 .btn {
 border: none;
 padding: 14px 24px;
 font-size: 1rem;
 border-radius: 999px;
 cursor: pointer;
 transition: 0.3s ease;
 text-decoration: none;
 display: inline-block;
 font-weight: bold;
 }
 .btn-primary {
 background: #7cff9b;
 color: #10301c;
 box-shadow: 0 8px 25px rgba(124, 255, 155, 0.25);
 }
 .btn-primary:hover { transform: translateY(-3px) scale(1.03); }
 .btn-secondary {
 background: transparent;
 color: white;
 border: 2px solid rgba(255,255,255,0.4);
 }
 .btn-secondary:hover { background: rgba(255,255,255,0.08); }


 nav {
 position: sticky;
 top: 0;
 z-index: 10;
 background: rgba(10, 28, 19, 0.85);
 backdrop-filter: blur(8px);
 padding: 12px 20px;
 border-bottom: 1px solid rgba(255,255,255,0.08);
 }
 nav ul {
 display: flex;
 justify-content: center;
 list-style: none;
 gap: 18px;
 flex-wrap: wrap;
 }
 nav a {
 color: #eaffea;
 text-decoration: none;
 font-weight: bold;
 transition: 0.3s;
 }
 nav a:hover { color: #8bffab; }


 section {
 max-width: 1150px;
 margin: auto;
 padding: 80px 20px;
 }
 .section-title {
 font-size: 2.1rem;
 margin-bottom: 24px;
 color: #bfffc9;
 text-align: center;
 }
 .section-sub {
 text-align: center;
 max-width: 760px;
 margin: 0 auto 30px;
 color: #e8ffe9;
 opacity: 0.95;
 }
 .card-grid {
 display: grid;
 grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
 gap: 20px;
 }
 .card {
 background: rgba(255,255,255,0.08);
 border: 1px solid rgba(255,255,255,0.1);
 border-radius: 20px;
 padding: 22px;
 box-shadow: 0 10px 30px rgba(0,0,0,0.18);
 transition: 0.3s ease;
 }
 .card:hover {
 transform: translateY(-6px) scale(1.01);
 background: rgba(255,255,255,0.11);
 }
 .card h3 {
 margin-bottom: 10px;
 color: #d5ffdb;
 }


 .two-col {
 display: grid;
 grid-template-columns: 1fr 1fr;
 gap: 24px;
 align-items: start;
 }
 .list-box {
 background: rgba(255,255,255,0.07);
 border-radius: 20px;
 padding: 24px;
 box-shadow: 0 10px 25px rgba(0,0,0,0.15);
 }
 .list-box ul, .list-box ol { padding-left: 20px; }
 .list-box li { margin-bottom: 10px; }


 .slider-wrap {
 position: relative;
 max-width: 980px;
 margin: 0 auto;
 }
 .slider {
 position: relative;
 height: 430px;
 border-radius: 28px;
 overflow: hidden;
 box-shadow: 0 20px 50px rgba(0,0,0,0.28);
 background: rgba(255,255,255,0.05);
 border: 1px solid rgba(255,255,255,0.08);
 }
 .slide {
 position: absolute;
 inset: 0;
 opacity: 0;
 transition: opacity 0.8s ease;
 background-size: cover;
 background-position: center;
 }
 .slide.active { opacity: 1; }
 .slide-overlay {
 position: absolute;
 inset: 0;
 background: linear-gradient(180deg, rgba(0,0,0,0.08), rgba(0,0,0,0.55));
 display: flex;
 align-items: end;
 padding: 32px;
 }
 .slide-caption {
 max-width: 540px;
 background: rgba(0,0,0,0.28);
 padding: 16px 20px;
 border-radius: 18px;
 backdrop-filter: blur(4px);
 }
 .slide-caption h3 { margin-bottom: 8px; }
 .slider-controls {
 display: flex;
 justify-content: center;
 gap: 12px;
 margin-top: 16px;
 }
 .dot {
 width: 12px;
 height: 12px;
 border-radius: 50%;
 background: rgba(255,255,255,0.35);
 cursor: pointer;
 transition: 0.3s;
 }
 .dot.active { background: #7cff9b; transform: scale(1.2); }


 .demo-panel {
 display: grid;
 grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
 gap: 18px;
 margin-top: 25px;
 }
 .sensor-box {
 background: rgba(0,0,0,0.25);
 border-radius: 18px;
 padding: 20px;
 text-align: center;
 border: 1px solid rgba(255,255,255,0.09);
 }
 .sensor-value {
 font-size: 2rem;
 font-weight: bold;
 margin: 10px 0;
 color: #92ffaf;
 }
 .status {
 margin-top: 10px;
 display: inline-block;
 padding: 6px 14px;
 border-radius: 999px;
 font-size: 0.9rem;
 background: rgba(255,255,255,0.12);
 }


 .image-placeholder {
 min-height: 280px;
 border: 2px dashed rgba(255,255,255,0.25);
 border-radius: 20px;
 display: flex;
 align-items: center;
 justify-content: center;
 text-align: center;
 padding: 20px;
 color: #dfffe6;
 background: rgba(255,255,255,0.04);
 }


 .team-grid {
 display: grid;
 grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
 gap: 22px;
 }
 .team-card {
 background: rgba(255,255,255,0.08);
 border-radius: 24px;
 overflow: hidden;
 border: 1px solid rgba(255,255,255,0.1);
 box-shadow: 0 16px 40px rgba(0,0,0,0.2);
 transition: 0.35s ease;
 }
 .team-card:hover { transform: translateY(-8px); }
 .team-photo {
 height: 240px;
 background-size: cover;
 background-position: center;
 position: relative;
 }
 .team-photo::after {
 content: "";
 position: absolute;
 inset: 0;
 background: linear-gradient(180deg, transparent, rgba(0,0,0,0.2));
 }
 .team-info { padding: 18px; }
 .team-role {
 display: inline-block;
 margin-top: 8px;
 padding: 6px 12px;
 border-radius: 999px;
 background: rgba(124,255,155,0.15);
 color: #a7ffbb;
 font-size: 0.9rem;
 }
.box{
  float: right;
  width: 300px;
  height: 300px;
}

 .schematic-box {
 background: rgba(255,255,255,0.06);
 border-radius: 24px;
 padding: 20px;
 border: 1px solid rgba(255,255,255,0.08);
 box-shadow: 0 15px 35px rgba(0,0,0,0.18);
 }
 .schematic-box img {
 width: 100%;
 border-radius: 18px;
 display: block;
 margin-bottom: 14px;
 }
Img {
  width: 100%;
  height: 100%;
  border-radius: 10px;
  height: 400px;
  object-fit: cover;

}
 footer {
 text-align: center;
 padding: 28px 20px 40px;
 background: rgba(0,0,0,0.22);
 color: #d8f7dc;
 }


 @media (max-width: 768px) {
 .hero h1 { font-size: 2.4rem; }
 .two-col { grid-template-columns: 1fr; }
 .slider { height: 320px; }
 .slide-overlay { padding: 20px; }
 }
 </style>
</head>
<body>
 <div class="bg-bubbles">
 <div class="bubble"></div>
 <div class="bubble"></div>
 <div class="bubble"></div>
 <div class="bubble"></div>
 <div class="bubble"></div>
 <div class="bubble"></div>
 <div class="bubble"></div>
 </div>


 <header id="home">
 <div class="floating-leaf leaf1"></div>
 <div class="floating-leaf leaf2"></div>
 <div class="floating-leaf leaf3"></div>
 <div class="floating-leaf leaf4"></div>


 <div class="hero">
 <h1>Ногоон хана төсөл</h1>
 <p>
 Байгальд ээлтэй, ухаалаг технологитой, дотоод орчныг илүү эрүүл, үзэмжтэй болгох
 ногоон ханын төсөл.
 </p>
 <div class="hero-buttons">
 <a href="#slider-section" class="btn btn-primary">Төсөл бүтээх явц</a>
 <button class="btn btn-secondary" onclick="startDemo()">Demo эхлүүлэх</button>
 </div>
 </div>
 </header>


 <nav>
 <ul>
 <li><a href="#slider-section">Төсөл бүтээх явц</a></li>
 <li><a href="#about">Танилцуулга</a></li>
 <li><a href="#team">Баг</a></li>
 <li><a href="#demo">Smart Demo</a></li>
 <li><a href="#gallery">Галлерей</a></li>
 </ul>
 </nav>
 <section id="slider-section">
 <h2 class="section-title">Төсөл бүтээх үйл явц</h2>
 <div class="slider-wrap">
 <div class="slider">

<div class="slide"></div> 
<img src="image/bot.jpg" width="200"> 

 <div class="slide-overlay">
 <div class="slide-caption">
 <h3>Ногоон орчин</h3>
 <p>Төслийн гол санаа нь бага зайд илүү их ногоон байгууламж бий болгох юм.</p>
 </div>
 </div>
 </div>
 <div class="slide"> <img src="image/guy.jpg" width="200"> 

 <div class="slide-overlay">
 <div class="slide-caption">
 <h3>Ургамлын өсөлт</h3>
 <p>Үрсэлгээ, ургалтын явцыг зураг болон видео хэлбэрээр баримтжуулна.</p>
 </div>
 </div>
 </div>
 <div class="slide">
<img src="image/zurg.jpg" width="200"> 
 <div class="slide-overlay">
 <div class="slide-caption">
 <h3>Ухаалаг хяналт</h3>
 <p>Чийг, температур хэмжиж автомат усалгааны систем ажиллуулна.</p>
 </div>
 </div>
 </div>
 </div>
 <div class="slider-controls">
 <span class="dot active" onclick="showSlide(0)"></span>
 <span class="dot" onclick="showSlide(1)"></span>
 <span class="dot" onclick="showSlide(2)"></span>
 </div>
 </div>
 </section>


 <section id="about">
 <h2 class="section-title">Төслийн танилцуулга</h2>
 <div class="">
 <div class="list-box">
 <p>
 “Green Wall” төсөл нь агаарын бохирдлыг бууруулах, чийгшлийг нэмэгдүүлэх,
 эрүүл орчин бүрдүүлэх, мөн бага зайд илүү их ногоон байгууламж бий болгох
 зорилготой ухаалаг ногоон ханын шийдэл юм.
 </p>
 <br>
 <p>
 Энэхүү төсөлд Arduino IDE, soil moisture sensor, DHT11, LCD 16x2, relay,
 автомат усалгааны систем зэрэг технологийг ашиглан ургамлын арчилгааг
 ухаалаг аргаар хийхээр төлөвлөсөн.
 </p>
 </div>

 <img src="image/zurag.jpg" width=""> 
 </div>
 </section>


 <section id="team">
 <h2 class="section-title">Багийн гишүүд</h2>
 <div class="team-grid">
 <div class="team-card">
<img src="image/Screenshot 2026-04-21 at 19.45.54.png" width="50"> <div class="team-info">
    
 <h3>Ундрал</h3>
 <p>Ургамлын ургалтын зураг, видео баримтжуулах, ургамал арчлах ажилд оролцоно.</p>
 <span class="team-role">Баримтжуулалт</span>
 </div>
 </div>
 <div class="team-card">
    <img src="image/IMG_3588.jpeg" width="200"> <div class="team-info">
 <h3>Тулд</h3>
 <p>Код бичих, soil sensor холболт, автомат системийн үндсэн логик дээр ажиллана.</p>
 <span class="team-role">Код ба холболт</span>
 </div>
 </div>
 <div class="team-card">
    <img src="image/IMG_3583.jpeg" width="200"> <div class="team-info">
 <h3>Алтан-Ураг</h3>
 <p>Үрсэлгээ, код бичих, ургамлын арчилгаа болон системийн дэмжлэг дээр ажиллана.</p>
 <span class="team-role">Системийн дэмжлэг</span>
 </div>
 </div>
 <div class="team-card">
    <img src="image/IMG_3586.jpeg" width="200"> <div class="team-info">
 <h3>Төгсбаяр</h3>
 <p>Туслах код бичих, soil sensor холболт, ургамал арчилгаа,веб бичих.</p>
 <span class="team-role">холболт</span>
 </div>
 </div>
 </section>


 <section id="demo">
 <h2 class="section-title">Smart System Demo</h2>
 <p class="section-sub">
 Энэ хэсэг нь жинхэнэ Arduino биш, харин төслийн ухаалаг ажиллагааг ойлгуулах энгийн JS demo юм.
 </p>


 <div class="demo-panel">
 <div class="sensor-box">
 <h3>Температур</h3>
 <div class="sensor-value"><span id="temp">26</span>°C</div>
 <div class="status" id="fanStatus">Цонх хаах</div>
 </div>
 <div class="sensor-box">
 <h3>Чийгшил</h3>
 <div class="sensor-value"><span id="humidity">61</span>%</div>
 <div class="status">Орчны чийг</div>
 </div>
 <div class="sensor-box">
 <h3>Хөрсний чийг</h3>
 <div class="sensor-value"><span id="soil">520</span></div>
 <div class="status" id="pumpStatus">Pump OFF</div>
 </div>
 <div class="sensor-box">
 <h3>Ургамлын төлөв</h3>
 <div class="sensor-value" id="plantMood">🌿</div>
 <div class="status" id="plantText">Эрүүл байна</div>
 </div>
 </div>


 <div style="text-align:center; margin-top:24px; display:flex; justify-content:center; gap:12px; flex-wrap:wrap;">
 <button class="btn btn-primary" onclick="randomUpdate()">Мэдээлэл шинэчлэх</button>
 <button class="btn btn-secondary" onclick="waterNow()">Одоо услах</button>
 </div>
 </section>


 <section id="gallery">
 <h2 class="section-title">Green Wall зураг </h2>
 <div class="card-grid">

 </div>
  <img src="image/zurag.jpg" width="50px "> 
 </div>
 <br>
 <br>
<img src="image/IMG_3563.jpeg" width="50px"> 
 </div>
 </section>


 <footer>
 <p><strong>Green Wall Project</strong></p>
 <p>НЭСТ ЭДҮКЭЙШН АЙ ТИ ДУНД СУРГУУЛЬ</p>
 <p>Байгальд ээлтэй · Ухаалаг · Ирээдүйд чиглэсэн</p>
 </footer>


 <script>
 const tempEl = document.getElementById('temp');
 const humidityEl = document.getElementById('humidity');
 const soilEl = document.getElementById('soil');
 const fanStatus = document.getElementById('fanStatus');
 const pumpStatus = document.getElementById('pumpStatus');
 const plantMood = document.getElementById('plantMood');
 const plantText = document.getElementById('plantText');


 function updateSystem(temp, humidity, soil) {
 tempEl.textContent = temp;
 humidityEl.textContent = humidity;
 soilEl.textContent = soil;


 if (temp > 28) {
 fanStatus.textContent = 'Цонх онгойлгох';
 } else {
 fanStatus.textContent = 'Цонх хаах';
 }


 if (soil > 700) {
 pumpStatus.textContent = 'Pump ON';
 plantMood.textContent = '💧';
 plantText.textContent = 'Усалгаа ажиллаж байна';
 } else if (soil > 600) {
 pumpStatus.textContent = 'Pump Standby';
 plantMood.textContent = '🌱';
 plantText.textContent = 'Бага зэрэг хуурай';
 } else {
 pumpStatus.textContent = 'Pump OFF';
 plantMood.textContent = '🌿';
 plantText.textContent = 'Эрүүл байна';
 }
 }


 function randomUpdate() {
 const temp = Math.floor(Math.random() * 10) + 23;
 const humidity = Math.floor(Math.random() * 25) + 45;
 const soil = Math.floor(Math.random() * 350) + 450;
 updateSystem(temp, humidity, soil);
 }


 function waterNow() {
 updateSystem(parseInt(tempEl.textContent), parseInt(humidityEl.textContent), 760);
 setTimeout(() => {
 updateSystem(26, 64, 560);
 }, 1800);
 }


 function startDemo() {
 document.getElementById('demo').scrollIntoView({ behavior: 'smooth' });
 randomUpdate();
 }


 const slides = document.querySelectorAll('.slide');
 const dots = document.querySelectorAll('.dot');
 let currentSlide = 0;


 function showSlide(index) {
 slides.forEach((slide, i) => {
 slide.classList.toggle('active', i === index);
 dots[i].classList.toggle('active', i === index);
 });
 currentSlide = index;
 }


 setInterval(() => {
 currentSlide = (currentSlide + 1) % slides.length;
 showSlide(currentSlide);
 }, 4000);
 </script>
</body>
</html>
