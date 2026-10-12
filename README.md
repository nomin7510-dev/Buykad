<!doctype html>
<html lang="mn">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <meta name="description" content="Төрсөн өдрийн бяцхан сюрприз — Buyka-д зориулсан захиа, дурсамж, хөгжимтэй сайхан хуудас.">
  <meta name="theme-color" content="#fff0f6">
  <title>Happy 17th Birthday, Buyka! 💗</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Montserrat:wght@300;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --fg:#5b3a4b;
      --muted:#7e5770;
      --pink-1:#ffd6e8;
      --pink-2:#ff9cc1;
      --lavender:#cdb4ff;
      --mint:#c9f6e6;
      --glass-border: rgba(255,255,255,0.42);
      --card-radius:28px;
      --ease: cubic-bezier(.2,.9,.25,1);
    }

    *{ box-sizing:border-box; }
    html{ scroll-behavior:smooth; }
    body{
      margin:0;
      font-family:"Montserrat",system-ui,-apple-system,Segoe UI,Roboto,Arial;
      color:var(--fg);
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      background:linear-gradient(135deg,#fff5fb 0%,#fffafc 38%,#fff4ff 100%);
      padding:28px;
      overflow-x:hidden;
      -webkit-font-smoothing:antialiased;
      position:relative;
    }

    body::before{
      content:"";
      position:fixed; inset:0; pointer-events:none;
      background:
        radial-gradient(circle at 15% 20%, rgba(255,184,205,0.12), transparent 10%),
        radial-gradient(circle at 80% 80%, rgba(198,182,255,0.10), transparent 11%),
        radial-gradient(circle at 50% 35%, rgba(255,240,245,0.08), transparent 8%);
      animation:bgMove 12s linear infinite;
    }
    @keyframes bgMove{
      0%,100%{ transform:translateY(0); }
      50%{ transform:translateY(-10px); }
    }

    .skip-link{
      position:fixed;
      left:16px;
      top:16px;
      z-index:9999;
      background:#fff;
      color:var(--fg);
      text-decoration:none;
      padding:10px 14px;
      border-radius:12px;
      font-weight:700;
      box-shadow:0 10px 28px rgba(122,78,103,0.08);
      opacity:0;
      transform:translateY(-14px);
      pointer-events:none;
      transition:opacity .18s ease, transform .18s ease;
    }
    .skip-link:focus{
      opacity:1;
      transform:translateY(0);
      pointer-events:auto;
      outline:3px solid rgba(197,91,143,0.12);
      outline-offset:4px;
    }

    main{
      width:100%;
      display:flex;
      align-items:center;
      justify-content:center;
    }

    section{
      min-height:100svh;
      width:100%;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:18px;
      position:relative;
      z-index:1;
      pointer-events:none;
      opacity:0;
      transform:translateY(10px);
      transition: opacity .5s var(--ease), transform .5s var(--ease);
    }

    section.active{
      pointer-events:auto;
      opacity:1;
      transform:translateY(0);
    }

    .card{
      width:100%;
      max-width:720px;
      border-radius:var(--card-radius);
      background:linear-gradient(180deg, rgba(255,255,255,0.23), rgba(255,249,252,0.10));
      border:1px solid var(--glass-border);
      backdrop-filter: blur(12px) saturate(120%);
      -webkit-backdrop-filter: blur(12px) saturate(120%);
      box-shadow:0 18px 50px rgba(122,78,103,0.07);
      padding:36px;
      position:relative;
      overflow:hidden;
      transform-origin:center;
    }

    .card::after{
      content:"";
      position:absolute; left:-30%; top:-40%;
      width:60%; height:200%;
      background:linear-gradient(120deg, rgba(255,255,255,0.28), rgba(255,255,255,0.04), rgba(255,255,255,0));
      transform: rotate(-25deg);
      pointer-events:none;
      mix-blend-mode:overlay;
      animation:sheen 5s linear infinite;
    }
    @keyframes sheen{
      from{ transform:translateX(-120%) rotate(-25deg); }
      to{ transform:translateX(220%) rotate(-25deg); }
    }

    .tag{
      color:#d46f9a;
      font-size:12px;
      font-weight:800;
      letter-spacing:2px;
    }

    .date{
      display:inline-block;
      margin:12px 0;
      padding:8px 16px;
      border-radius:999px;
      background:var(--pink-1);
      color:#c35b8a;
      font-weight:700;
    }

    h1{
      font-family:"Great Vibes", cursive;
      font-size:clamp(34px,6.5vw,56px);
      line-height:0.96;
      color:#d4548c;
      margin:10px 0;
    }

    h2{
      font-family:"Montserrat", system-ui, sans-serif;
      font-weight:800;
      color:#d4548c;
      margin:8px 0 0;
    }

    .age{
      font-weight:900;
      color:var(--pink-2);
      font-size:88px;
      line-height:1;
      text-shadow:3px 4px rgba(255,220,235,0.6);
      margin:6px 0;
    }
    .age small{
      display:block;
      font-size:15px;
      letter-spacing:1px;
      color:rgba(213,84,140,0.9);
      margin-top:8px;
      font-weight:800;
    }

    p{
      color:#6a465a;
      line-height:1.8;
      font-size:15px;
    }

    button{
      background:linear-gradient(90deg,#ff9cc1,#cdb4ff);
      color:#fff;
      border:0;
      border-radius:999px;
      padding:12px 22px;
      font-weight:700;
      font-size:15px;
      cursor:pointer;
      box-shadow:0 10px 30px rgba(201,114,160,0.12);
      transition: transform .14s var(--ease), box-shadow .2s ease, opacity .2s ease;
      min-height:44px;
    }
    button:hover{
      transform:translateY(-1px);
    }
    button:active{
      transform:translateY(1px);
    }
    button:focus{
      outline:3px solid rgba(197,91,143,0.12);
      outline-offset:4px;
    }

    #audioToggle{
      background:transparent;
      color:#d4548c;
      border-radius:8px;
      padding:8px 10px;
      margin-left:10px;
      font-size:18px;
      box-shadow:none;
      border:1px solid rgba(255,220,235,0.5);
      min-width:46px;
    }

    #balloons{
      height:150px;
      position:relative;
      margin:6px 0 10px;
      overflow:visible;
    }

    .balloon{
      position:absolute;
      bottom:-120px;
      width:62px;
      height:72px;
      border-radius:48% 52% 50% 50%;
      box-shadow: inset -8px -6px 0 rgba(0,0,0,0.03), 0 12px 26px rgba(122,78,103,0.06);
      animation: float 4s ease-in-out infinite;
    }
    @keyframes float{
      0%{ transform:translateY(0) rotate(-4deg); opacity:0; }
      8%{ opacity:1; }
      50%{ transform:translateY(-36px) rotate(6deg); }
      100%{ transform:translateY(0) rotate(-4deg); opacity:1; }
    }

    [data-reveal]{
      opacity:0;
      transform:translateY(8px) scale(.995);
      transition: opacity .38s var(--ease), transform .38s var(--ease);
      will-change: opacity, transform;
    }
    [data-reveal].revealed{
      opacity:1;
      transform:translateY(0) scale(1);
    }

    .letter{
      text-align:left;
      white-space:pre-line;
      line-height:1.9;
      font-size:15px;
      background:linear-gradient(180deg, rgba(255,247,251,0.7), rgba(255,247,251,0.45));
      border:1px solid rgba(255,218,234,0.55);
      padding:20px;
      border-radius:18px;
      margin-top:18px;
      box-shadow:0 8px 22px rgba(122,78,103,0.04);
    }

    .signature{
      text-align:center;
      color:#d65d9b;
      font-weight:700;
      margin-top:16px;
    }

    .gallery{
      margin-top:20px;
      position:relative;
      overflow:hidden;
    }
    .slides{
      display:flex;
      transition:transform .45s ease;
      width:100%;
    }
    .slide{
      min-width:100%;
      display:block;
    }
    .slide img{
      display:block;
      width:100%;
      height:auto;
      max-height:62vh;
      object-fit:cover;
      border-radius:14px;
    }
    figcaption{
      margin-top:10px;
      text-align:center;
      color:#7d5068;
      font-size:14px;
      font-weight:600;
    }

    .carousel-controls{
      display:flex;
      justify-content:center;
      align-items:center;
      gap:12px;
      margin-top:16px;
    }
    .carousel-btn{
      background: rgba(255,255,255,0.5);
      color:#c36395;
      border:1px solid rgba(255,221,233,0.8);
      box-shadow:none;
    }
    .dots{
      display:flex;
      gap:8px;
      justify-content:center;
      align-items:center;
      flex:1;
    }
    .dot{
      width:10px;
      height:10px;
      border-radius:50%;
      background: rgba(208,153,180,0.35);
      border:none;
      padding:0;
      cursor:pointer;
    }
    .dot.active{
      background:linear-gradient(90deg,#ff9cc1,#cdb4ff);
      transform:scale(1.2);
    }

    .hidden{
      display:none !important;
    }

    .center{
      text-align:center;
    }

    .credit{
      margin-top:24px;
      color:#b37fa0;
      font-size:13px;
    }

    @media (min-width:720px){
      .card{
        padding:40px;
      }
      .gallery{
        max-width:620px;
        margin-left:auto;
        margin-right:auto;
      }
    }

    @media (max-width:420px){
      .age{ font-size:64px; }
      .card{ padding:24px 18px; }
      #audioToggle{ margin-left:6px; }
    }

    @media (prefers-reduced-motion: reduce){
      *{
        animation-duration:.001ms !important;
        animation-iteration-count:1 !important;
        transition-duration:.001ms !important;
      }
      .card::after{
        display:none;
      }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#startButton">Skip to primary action</a>

  <main>
    <section id="welcome" class="active">
      <div class="card" aria-labelledby="welcomeTitle">
        <div class="tag" data-reveal="1">A SWEET SURPRISE FOR YOU ♡</div>

        <div class="date" data-reveal="2">🎀 10 / 13 · 17 НАС 🎀</div>

        <div id="balloons" aria-hidden="true" data-reveal="3"></div>

        <div class="age center" aria-hidden="true" data-reveal="4">
          17
          <small>TH BIRTHDAY</small>
        </div>

        <h1 id="welcomeTitle" data-reveal="5">Төрсөн өдрийн<br>мэнд, Buyka! 💗</h1>

        <p data-reveal="6">Энэ бяцхан сайтаар найздаа мэнд хүргэе. Доорх товчийг дараарай 🎁</p>

        <div class="center" style="margin-top:12px; display:flex; justify-content:center; gap:8px; align-items:center;" data-reveal="7">
          <button id="startButton" type="button" aria-controls="letterScreen">🎈 Эхлэх</button>
          <button id="audioToggle" type="button" aria-pressed="false" aria-label="Play music" title="Play / Pause music">🎵</button>
        </div>
      </div>
    </section>

    <section id="letterScreen" class="">
      <div class="card" aria-labelledby="letterTitle">
        <div class="tag" data-reveal="1">💌 A LETTER FOR MY BESTIE</div>
        <div class="date" data-reveal="2">10.13 · 17 & BLOOMING 🌷</div>

        <h2 id="letterTitle" data-reveal="3">Буякад зориулсан захиа 💗</h2>

        <div id="sender" aria-live="polite" style="min-height:40px; font-weight:700; color:#c75b8f;" data-reveal="4"></div>

        <div style="margin-top:10px" data-reveal="5">
          <button id="readButton" class="hidden" type="button" aria-controls="letter">💌 Захиа унших</button>
        </div>

        <div id="letter" class="letter hidden" tabindex="0" data-reveal="6">
          <h3 style="text-align:center; font-family:'Great Vibes', cursive; color:#d4548c; font-weight:400">Эрхэм хүндэт үзэсгэлэнт Гоо найз минь ээ 💗</h3>

Эрхэм хүндэт үзэгслэн Гоо Найз минь ээ
Бие биенийгээ мэддэг болоод, таньдаг болоод 12 жилийн хугацаа өнгөрчээ. Хэрвээ 80 наслах юм бол амьдралынхаа 15% ийг хамтдаа өнгрөөжээ. Цаашдаа ч 20,30 давраад 70,80 жил хөгшин буурал болтлоо андууд байя.
Хэдий өдөр болгон хамт нэг ангид байдаггүй ч хөндийрөлгүй найз минь байдагт баярлалаа. Холбогч гүүргүй үргэлжилдэг цөөхөн харилцааны минь нэг шүү.
Гэхдээ 진짜 тэр өдөр 너무 너무 баярласаан
Бид 3 ийг гээд зориод бэлэг өгдөг найзтай байна гэдэг надад үнэхээр гоё байсаан тэр үед бүр үнэхээр баярласан шүү уйлах аа шахсан.
Одоо бичиж байхдаа баярлаад нулимс урсаж байна ㅋㅋㅋ.
Бид нарын биесийн зай холдож ирээдүйд бүр илүү холдох ч хэдүүлээ сэтгэлээрээ дандаа цуг байцгаая. Яаанаа баахан алдаатай бичээд онигоо болох вий дээ хха.
Заа ингээд хөөрхөн найздаа төрсөн өдрийн баярын мэнд хүргэе найздаа хайртай шүү.
Ному ному саранхэёо чингүяа🫶🏻❤️❤️❤️

          <div class="signature">Ному ному саранхэёа, чингүяа 🫶🏻❤️❤️❤️</div>
        </div>

        <div style="margin-top:16px" data-reveal="7">
          <button id="photosButton" class="hidden" type="button" aria-controls="memories">📸 Бидний дурсамж ↓</button>
        </div>
      </div>
    </section>

    <section id="memories" class="">
      <div class="card" aria-labelledby="memTitle">
        <div class="tag" data-reveal="1">OUR LITTLE MEMORIES ♡</div>
        <h2 id="memTitle" data-reveal="2">Бидний дурсамж 💞</h2>
        <p data-reveal="3">Хол байсан ч гоё дурсамжууд маань үргэлж хамт шүү.</p>

        <div class="gallery" data-reveal="4">
          <div class="slides" id="slides" aria-live="polite">
            <figure class="slide">
              <img src="https://kommodo.ai/i/BxoRloQXfhku3joVMJ3p" alt="Бидний ангийн дурсамж" loading="lazy">
              <figcaption>Хамтдаа өнгөрүүлсэн мөчүүд 🎈</figcaption>
            </figure>
            <figure class="slide">
              <img src="https://kommodo.ai/i/SM2861K6Mq0z5fYjjAEm" alt="Найзуудын зураг" loading="lazy">
              <figcaption>Гоё дурсамжууд минь 💗</figcaption>
            </figure>
            <figure class="slide">
              <img src="https://kommodo.ai/i/JouJ4QPir2GaIxrHmqQC" alt="Гэрэлтэй гудамжны дурсамж" loading="lazy">
              <figcaption>Мартагдашгүй мөчүүд ✨</figcaption>
            </figure>
          </div>

          <div class="carousel-controls" data-reveal="5">
            <button class="carousel-btn" id="prevBtn" type="button" aria-label="Previous photo">◀</button>
            <div class="dots" id="dots" aria-label="Photo navigation">
              <button class="dot active" type="button" aria-label="Go to photo 1"></button>
              <button class="dot" type="button" aria-label="Go to photo 2"></button>
              <button class="dot" type="button" aria-label="Go to photo 3"></button>
            </div>
            <button class="carousel-btn" id="nextBtn" type="button" aria-label="Next photo">▶</button>
          </div>
        </div>

        <div class="credit center" data-reveal="6">Made with 💗<br><strong>Made by Erkhes</strong></div>
      </div>
    </section>
  </main>

  <audio id="birthdayMusic" loop preload="auto" aria-hidden="true">
    <source src="birthday.mp3" type="audio/mpeg">
  </audio>

  <script>
    const sections = [...document.querySelectorAll('section')];
    const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

    function showSection(id){
      sections.forEach(s => {
        if(s.id === id){
          s.classList.add('active');
          revealElementsInSection(s);

          const firstInteractive = s.querySelector('button, [href], input, textarea, select, [tabindex]:not([tabindex="-1"])');
          if(firstInteractive && !reduceMotion){
            setTimeout(() => firstInteractive.focus(), 420);
          }

          s.scrollIntoView({ behavior: 'smooth', block: 'start' });
        } else {
          s.classList.remove('active');
          s.querySelectorAll('[data-reveal]').forEach(el => el.classList.remove('revealed'));
        }
      });
    }

    function revealElementsInSection(section){
      const reveals = [...section.querySelectorAll('[data-reveal]')];
      reveals.sort((a,b) => {
        const na = Number(a.getAttribute('data-reveal') || 0);
        const nb = Number(b.getAttribute('data-reveal') || 0);
        return na - nb;
      });
      reveals.forEach((el, idx) => {
        setTimeout(() => el.classList.add('revealed'), idx * 260);
      });
    }

    const colors = ["#ff9cc1","#cdb4ff","#ffd6e8","#ffb7da","#a7f0e8"];
    const balloonArea = document.getElementById("balloons");

    function makeBalloons(n=8){
      if(!balloonArea) return;
      balloonArea.innerHTML = "";
      for(let i=0;i<n;i++){
        const b = document.createElement("div");
        b.className = "balloon";
        const left = Math.random() * 85;
        const size = 40 + Math.random() * 38;
        b.style.left = `${left}%`;
        b.style.width = `${size}px`;
        b.style.height = `${Math.round(size * 1.15)}px`;
        b.style.background = `linear-gradient(180deg, ${colors[i % colors.length]}, rgba(255,255,255,0.1))`;
        b.style.animationDelay = `${(Math.random() * 0.8).toFixed(2)}s`;
        balloonArea.appendChild(b);
      }
    }

    function confetti(count=16){
      const symbols = ["💗","✨","🌸","💕","🎀"];
      for(let i=0;i<count;i++){
        const s = document.createElement("span");
        s.textContent = symbols[Math.floor(Math.random()*symbols.length)];
        s.style.position = "fixed";
        s.style.left = (Math.random()*100) + "vw";
        s.style.top = "-20px";
        s.style.zIndex = "9999";
        s.style.fontSize = (12 + Math.random()*18) + "px";
        s.style.pointerEvents = "none";
        s.style.animation = `fall ${4 + Math.random()*3}s linear forwards`;
        s.style.filter = "drop-shadow(0 8px 14px rgba(122,78,103,0.06))";
        document.body.appendChild(s);
        s.addEventListener('animationend', () => s.remove());
      }
    }

    const style = document.createElement('style');
    style.textContent = `
      @keyframes fall{
        0%{ transform:translate3d(0,0,0) rotate(0deg); opacity:1; }
        100%{ transform:translate3d(12px,110vh,0) rotate(420deg); opacity:0; }
      }
    `;
    document.head.appendChild(style);

    const slides = document.getElementById("slides");
    const dots = [...document.querySelectorAll(".dot")];
    const prevBtn = document.getElementById("prevBtn");
    const nextBtn = document.getElementById("nextBtn");
    let currentSlide = 0;
    const totalSlides = dots.length || 1;

    function renderCarousel(){
      if(!slides) return;
      slides.style.transform = `translateX(-${currentSlide * 100}%)`;
      dots.forEach((dot, index) => dot.classList.toggle('active', index === currentSlide));
    }

    if(prevBtn){
      prevBtn.addEventListener('click', () => {
        currentSlide = (currentSlide -1 + totalSlides) % totalSlides;
        renderCarousel();
      });
    }
    if(nextBtn){
      nextBtn.addEventListener('click', () => {
        currentSlide = (currentSlide +1) % totalSlides;
        renderCarousel();
      });
    }
    dots.forEach((dot, i) => {
      dot.addEventListener('click', () => {
        currentSlide = i;
        renderCarousel();
      });
    });

    let carouselInterval = setInterval(() => {
      const mem = document.getElementById('memories');
      if(mem && mem.classList.contains('active')){
        currentSlide = (currentSlide + 1) % totalSlides;
        renderCarousel();
      }
    }, 3800);

    const startBtn = document.getElementById("startButton");
    const readBtn = document.getElementById("readButton");
    const photosBtn = document.getElementById("photosButton");
    const letter = document.getElementById("letter");
    const sender = document.getElementById("sender");
    const music = document.getElementById("birthdayMusic");
    const audioToggle = document.getElementById("audioToggle");

    let musicPlaying = false;

    makeBalloons();

    function setAudioUI(on){
      if(audioToggle){
        audioToggle.textContent = on ? '🔊' : '🎵';
        audioToggle.setAttribute('aria-pressed', String(!!on));
        audioToggle.setAttribute('aria-label', on ? 'Pause music' : 'Play music');
      }
    }

    function playSenderThenShowButton(){
      if(!sender) return;
      const text = "Буяндэлгэрт Эрхэсээс 💌";
      let i = 0;
      sender.textContent = "";
      const t = setInterval(() => {
        sender.textContent += text[i++] || "";
        if(i > text.length){
          clearInterval(t);
          setTimeout(() => {
            sender.textContent = "";
            if(readBtn){
              readBtn.classList.remove('hidden');
              readBtn.classList.add('revealed');
              readBtn.focus();
            }
          }, 600);
        }
      }, 60);
    }

    function toggleMusic(){
      if(!music) return;
      if(musicPlaying){
        music.pause();
        musicPlaying = false;
        setAudioUI(false);
      } else {
        music.play()
          .then(() => {
            musicPlaying = true;
            setAudioUI(true);
          })
          .catch(() => {
            musicPlaying = false;
            setAudioUI(false);
          });
      }
    }

    function showLetterScreen(){
      showSection('letterScreen');
      makeBalloons(6);
      confetti(18);
      setTimeout(() => playSenderThenShowButton(), 220);
      if(letter) letter.classList.add('hidden');
    }

    function openLetter(){
      if(letter){
        letter.classList.remove('hidden');
        revealElementsInSection(letter.closest('section'));
        setTimeout(() => {
          if(photosBtn){
            photosBtn.classList.remove('hidden');
            photosBtn.classList.add('revealed');
          }
        }, 500);
        confetti(10);
      }
    }

    function showPhotos(){
      showSection('memories');
      confetti(16);
      renderCarousel();
    }

    function tryPlayMusic(){
      if(music && !musicPlaying){
        music.play()
          .then(() => {
            musicPlaying = true;
            setAudioUI(true);
          })
          .catch(() => {
            musicPlaying = false;
            setAudioUI(false);
          });
      }
    }

    if(startBtn){
      startBtn.addEventListener('click', () => {
        showLetterScreen();
        tryPlayMusic();
      });
    }
    if(readBtn) readBtn.addEventListener('click', openLetter);
    if(photosBtn) photosBtn.addEventListener('click', showPhotos);
    if(audioToggle) audioToggle.addEventListener('click', toggleMusic);

    document.addEventListener('keydown', (e) => {
      const memActive = document.getElementById('memories')?.classList.contains('active');

      if(e.key === 'Escape'){
        showSection('welcome');
        return;
      }

      if(memActive){
        if(e.key === 'ArrowLeft'){
          currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
          renderCarousel();
        }
        if(e.key === 'ArrowRight'){
          currentSlide = (currentSlide + 1) % totalSlides;
          renderCarousel();
        }
      }
    });

    let startX = null;
    if(slides){
      slides.addEventListener('touchstart', e => {
        startX = e.touches[0].clientX;
      });
      slides.addEventListener('touchend', e => {
        if(startX === null) return;
        const dx = e.changedTouches[0].clientX - startX;
        if(dx > 40){
          currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
          renderCarousel();
        }
        if(dx < -40){
          currentSlide = (currentSlide + 1) % totalSlides;
          renderCarousel();
        }
        startX = null;
      });
    }

    document.addEventListener('DOMContentLoaded', () => {
      const active = document.querySelector('section.active');
      if(active) revealElementsInSection(active);
    });
  </script>
</body>
</html>
