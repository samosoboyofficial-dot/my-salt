<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>SAMOSOBOY — официальная страница</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

    body {
      margin: 0;
      font-family: 'Poppins', 'Segoe UI', Arial, sans-serif;
      background: #F7F7F7;
      color: #333;
      position: relative;
      overflow-x: hidden;
    }

    @keyframes gradientMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    header {
      text-align: center;
      padding: 80px 20px;
      background: linear-gradient(135deg, #064E40, #00695C, #FFB974, #FF6B6B);
      border-bottom: 1px solid #e0f2f1;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
      position: relative;
      overflow: hidden;
    }

    header h1 {
      font-size: 4em;
      letter-spacing: 3px;
      margin: 0;
      font-weight: 700;
      background: linear-gradient(270deg, #FF6B6B, #FFB974, #00BFA5, #064E40);
      background-size: 800% 800%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientMove 15s ease infinite;
      text-shadow: 1px 1px 5px rgba(0,0,0,0.15);
    }

    .content {
      max-width: 1000px;
      margin: 50px auto;
      padding: 0 20px;
      position: relative;
      z-index: 2;
    }

    h2 {
      font-size: 2em;
      margin-bottom: 20px;
      color: #064E40;
      position: relative;
    }

    h2::after {
      content: '';
      display: block;
      width: 60px;
      height: 4px;
      background: linear-gradient(90deg, #FF6B6B, #FFB974, #00BFA5);
      border-radius: 2px;
      margin-top: 8px;
    }

    p {
      font-size: 1.1em;
      line-height: 1.7em;
      color: #333;
    }

    .video-container {
      position: relative;
      width: 100%;
      padding-bottom: 56.25%;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 6px 20px rgba(0,0,0,0.15);
      margin-top: 25px;
      transition: transform 0.3s;
    }

    .video-container:hover {
      transform: scale(1.02);
    }

    .video-container iframe {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      border-radius: 15px;
    }

    .catalogue, .socials, .gallery {
      background: rgba(255,255,255,0.95);
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.08);
      border: 1px solid #e0f2f1;
      transition: transform 0.3s, box-shadow 0.3s;
      position: relative;
      z-index: 2;
    }

    .catalogue:hover, .socials:hover, .gallery:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 30px rgba(0,0,0,0.15);
    }

    .catalogue a, .socials a {
      color: #00695C;
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s;
    }

    .catalogue a:hover, .socials a:hover {
      color: #00BFA5;
    }

    .socials a {
      display: inline-block;
      margin-right: 15px;
      padding: 8px 18px;
      border-radius: 12px;
      background: #FFB974;
      color: #FFFFFF;
      transition: background 0.3s, transform 0.3s;
    }

    .socials a:hover {
      background: #FF6B6B;
      transform: scale(1.05);
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      margin-top: 25px;
    }

    .gallery-grid img {
      width: 100%;
      height: auto;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.12);
      transition: transform 0.4s, box-shadow 0.4s;
    }

    .gallery-grid img:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 30px rgba(0,0,0,0.18);
    }

    footer {
      text-align: center;
      padding: 40px 10px;
      background: linear-gradient(135deg, #00695C, #004D40, #00BFA5);
      font-size: 0.9em;
      color: #ffffff;
      border-top: 1px solid #004D40;
      position: relative;
      z-index: 2;
    }

    /* Фоновые элементы с параллаксом */
    .background-element {
      position: fixed;
      opacity: 0.08;
      z-index: 0;
      transition: transform 0.2s ease, opacity 0.2s ease;
      pointer-events: none;
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center;
    }

    .bg-guitar { 
      bottom: 10px; left: 10px; 
      width: 250px; 
      height: 250px;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/4/4d/Acoustic_guitar.png');
    }

    .bg-dostoevsky { 
      top: 5%; right: 10%; 
      width: 150px; 
      height: 200px;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/6/6c/Dostoevsky_portrait.jpg');
    }

    .bg-brodsky { 
      top: 15%; left: 10%; 
      width: 150px; 
      height: 200px;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/b/b6/Joseph_Brodsky_1972.jpg');
    }

    .bg-bulgakov { 
      bottom: 10%; right: 15%; 
      width: 150px; 
      height: 200px;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/0/0b/Bulgakov_Mikhail.jpg');
    }

    .bg-pushkin { 
      top: 50%; left: 50%; 
      width: 200px; 
      height: 250px;
      transform: translate(-50%, -50%);
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/3/3b/Pushkin_portrait_miniature.jpg');
    }
  </style>
</head>
<body>

  <!-- Фоновые элементы -->
  <div class="background-element bg-guitar" data-speed="0.2"></div>
  <div class="background-element bg-dostoevsky" data-speed="0.15"></div>
  <div class="background-element bg-brodsky" data-speed="0.1"></div>
  <div class="background-element bg-bulgakov" data-speed="0.18"></div>
  <div class="background-element bg-pushkin" data-speed="0.12"></div>

  <header>
    <h1>SAMOSOBOY</h1>
  </header>

  <div class="content">

    <section class="about">
      <h2>О группе</h2>
      <p>Мы — SAMOSOBOY, поп-рок группа. Добро пожаловать на наш сайт!</p>
    </section>

    <section class="videos">
      <h2>Видео</h2>
      <div class="video-container">
        <iframe src="https://vk.com/video_ext.php?oid=-154957342&id=456239545&autoplay=0&hd=2"
                frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
      </div>
    </section>

    <section class="catalogue">
      <h2>Тексты и файлы</h2>
      <p>Тексты песен и материалы — в нашем сообществе VK:</p>
      <p><a href="https://vk.com/samoso_boy" target="_blank">VK — SAMOSOBOY</a></p>
    </section>

    <section class="gallery">
      <h2>Постер группы</h2>
      <div class="gallery-grid">
        <img src="https://sun9-30.userapi.com/s/v1/ig2/vzh-SMed0yPEnBPZRxBI08cpw8v6DwjDTXaypOwQUtlRFjwf0zB6zLHSpO_Do8_lIc9uVQqLCjZ8dgKZHey7oHAJ.jpg?quality=95" alt="SAMOSOBOY">
        <img src="https://sun9-23.userapi.com/s/v1/ig2/SC610v6JsVFZH3C4xjGaMOrlIY-Pcbk0woteDLh7BGOReYWc4qBxpjCQrUIuacsrfG2bBnguXCkyeDmSLOIpwn7S.jpg?quality=95" alt="SAMOSOBOY">
      </div>
    </section>

    <section class="socials">
      <h2>Мы в соцсетях</h2>
      <a href="https://youtube.com/@ssamosoboyofficial" target="_blank">YouTube</a>
      <a href="https://t.me/Samosoboy123" target="_blank">Telegram</a>
    </section>

  </div>

  <footer>
    © 2025 SAMOSOBOY — официальный сайт
  </footer>

  <script>
    // Параллакс фона
    const bgElements = document.querySelectorAll('.background-element');

    window.addEventListener('scroll', () => {
      const scrollY = window.scrollY;
      bgElements.forEach(el => {
        const speed = parseFloat(el.dataset.speed);
        el.style.transform = `translateY(${scrollY * speed}px)`;
      });
    });
  </script>
</body>
</html>
