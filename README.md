<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Новогоднее поздравление 🎄</title>
  <style>
    /* Все предыдущие стили остаются без изменений... */
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: 
        radial-gradient(circle at 20% 80%, rgba(255, 215, 0, 0.15) 0%, transparent 20%),
        radial-gradient(circle at 80% 20%, rgba(255, 20, 147, 0.15) 0%, transparent 20%),
        linear-gradient(135deg, #0a1d3f 0%, #0c2b5e 25%, #0d3b7a 50%, #0f4a97 75%, #1159b4 100%);
      color: white;
      text-align: center;
      overflow-x: hidden;
      position: relative;
      min-height: 100vh;
    }

    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M50,10 L60,40 L90,40 L65,60 L75,90 L50,70 L25,90 L35,60 L10,40 L40,40 Z" fill="gold" opacity="0.1"/></svg>'),
        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="10" fill="red" opacity="0.1"/></svg>'),
        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><polygon points="50,10 60,30 80,30 65,45 75,65 50,55 25,65 35,45 20,30 40,30" fill="silver" opacity="0.1"/></svg>');
      background-size: 80px, 60px, 70px;
      background-position: 10% 20%, 85% 40%, 15% 70%;
      background-repeat: no-repeat;
      pointer-events: none;
      z-index: -1;
    }

    .sparkle {
      position: fixed;
      width: 4px;
      height: 4px;
      background: gold;
      border-radius: 50%;
      animation: sparkle 3s infinite;
      pointer-events: none;
      z-index: -1;
    }

    @keyframes sparkle {
      0%, 100% { opacity: 0; transform: scale(0); }
      50% { opacity: 1; transform: scale(1); }
    }

    h1 {
      margin-top: 20px;
      font-size: 2.8em;
      text-shadow: 0 0 10px rgba(255, 215, 0, 0.7),
                   0 0 20px rgba(255, 20, 147, 0.5),
                   2px 2px 4px rgba(0, 0, 0, 0.3);
      background: linear-gradient(45deg, #FFD700, #FF69B4, #00CED1);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      padding: 10px;
    }

    #countdown {
      font-size: 1.8em;
      margin: 20px 0;
      padding: 15px;
      background: rgba(0, 0, 0, 0.3);
      border-radius: 15px;
      display: inline-block;
      border: 2px solid gold;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
      backdrop-filter: blur(5px);
    }

    button {
      padding: 12px 25px;
      margin: 10px;
      border: none;
      border-radius: 8px;
      background: linear-gradient(45deg, #FF416C, #FF4B2B);
      color: white;
      cursor: pointer;
      font-size: 1.1em;
      font-weight: bold;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(255, 65, 108, 0.4);
      position: relative;
      overflow: hidden;
    }

    button:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(255, 65, 108, 0.6);
      background: linear-gradient(45deg, #FF4B2B, #FF416C);
    }

    button:active {
      transform: translateY(1px);
    }

    button::after {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      transition: 0.5s;
    }

    button:hover::after {
      left: 100%;
    }

    #card, #wish, #gallery, #game {
      margin: 30px auto;
      padding: 25px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      width: 80%;
      max-width: 800px;
      border: 1px solid rgba(255, 215, 0, 0.3);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
      backdrop-filter: blur(10px);
      position: relative;
      overflow: hidden;
    }

    #card::before, #wish::before, #gallery::before, #game::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, #FFD700, #FF69B4, #00CED1, #FFD700);
      background-size: 400% 100%;
      animation: shimmer 3s linear infinite;
    }

    @keyframes shimmer {
      0% { background-position: 0% 0; }
      100% { background-position: 400% 0; }
    }

    /* Стили для изображений в галерее (остаются) */
    #gallery img {
      width: 180px;
      height: 180px;
      margin: 15px;
      border: 3px solid rgba(255, 215, 0, 0.5);
      border-radius: 15px;
      transition: all 0.3s ease;
      object-fit: cover;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
      cursor: pointer; /* Добавляем курсор-указатель */
    }

    #gallery img:hover {
      transform: scale(1.05);
      border-color: #FF69B4;
      box-shadow: 0 8px 25px rgba(255, 105, 180, 0.4);
    }

    .snowflake {
      position: fixed;
      top: -10px;
      color: white;
      font-size: 24px;
      animation: fall linear infinite;
      text-shadow: 0 0 5px rgba(255, 255, 255, 0.8);
      opacity: 0.8;
      z-index: -1;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }

    #gameCanvas {
      background: linear-gradient(to bottom, #001a33, #003366);
      border: 3px solid gold;
      border-radius: 10px;
      display: block;
      margin: 20px auto;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.3);
    }

    .controls {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin: 15px 0;
      align-items: center;
    }

    .key {
      padding: 8px 15px;
      background: rgba(255, 255, 255, 0.2);
      border-radius: 5px;
      border: 1px solid gold;
      font-weight: bold;
      min-width: 40px;
    }

    .game-stats {
      display: flex;
      justify-content: center;
      gap: 30px;
      margin: 15px 0;
      flex-wrap: wrap;
    }

    .stat-item {
      background: rgba(255, 255, 255, 0.1);
      padding: 10px 20px;
      border-radius: 10px;
      border: 1px solid rgba(255, 215, 0, 0.3);
    }

    .music-note {
      position: fixed;
      bottom: 20px;
      right: 20px;
      color: gold;
      font-size: 24px;
      animation: bounce 2s infinite;
      z-index: 1000;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    @media (max-width: 768px) {
      h1 { font-size: 2em; }
      #countdown { font-size: 1.3em; }
      #gallery img { width: 140px; height: 140px; }
      button { padding: 10px 20px; font-size: 1em; }
      .game-stats { gap: 15px; }
      .stat-item { padding: 8px 15px; font-size: 0.9em; }
      .music-note { bottom: 10px; right: 10px; font-size: 20px; }
    }

    /* === ДОБАВЛЯЕМ ТОЛЬКО ЭТИ СТИЛИ ДЛЯ МОДАЛЬНОГО ОКНА === */
    
    /* Модальное окно */
    .modal {
      display: none;
      position: fixed;
      z-index: 9999;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.9);
      animation: fadeIn 0.3s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* Изображение в модальном окне */
    .modal-content {
      margin: auto;
      display: block;
      max-width: 90%;
      max-height: 85vh;
      border-radius: 10px;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
      animation: zoomIn 0.3s ease;
    }

    @keyframes zoomIn {
      from { transform: scale(0.9); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    /* Кнопка закрытия */
    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      color: white;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s ease;
      z-index: 10000;
    }

    .close:hover {
      color: #FF69B4;
      transform: rotate(90deg) scale(1.1);
    }

    /* Подпись к изображению */
    #caption {
      margin: 15px auto;
      text-align: center;
      color: white;
      font-size: 1.2em;
      max-width: 700px;
      padding: 10px;
    }

    /* Кнопки навигации (лево/право) */
    .modal-nav {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background-color: rgba(0, 0, 0, 0.7);
      color: white;
      border: none;
      padding: 15px 20px;
      font-size: 24px;
      cursor: pointer;
      border-radius: 50%;
      transition: all 0.3s ease;
      z-index: 10000;
    }

    .modal-nav:hover {
      background-color: rgba(255, 215, 0, 0.8);
      transform: translateY(-50%) scale(1.1);
    }

    .prev {
      left: 20px;
    }

    .next {
      right: 20px;
    }

    /* Счетчик изображений */
    .image-counter {
      position: absolute;
      top: 20px;
      left: 30px;
      color: white;
      font-size: 18px;
      background: rgba(0, 0, 0, 0.5);
      padding: 8px 15px;
      border-radius: 20px;
      z-index: 10000;
    }

    /* Адаптивность для мобильных */
    @media (max-width: 768px) {
      .modal-nav {
        padding: 10px 15px;
        font-size: 18px;
      }
      
      .prev {
        left: 10px;
      }
      
      .next {
        right: 10px;
      }
      
      .close {
        top: 10px;
        right: 15px;
        font-size: 30px;
      }
      
      .image-counter {
        top: 10px;
        left: 15px;
        font-size: 14px;
        padding: 5px 10px;
      }
    }
  </style>
</head>
<body>
  <!-- Просто музыкальная нота как индикатор -->
  <div class="music-note" title="Играет новогодняя музыка">🎵</div>

  <h1>С Новым Годом, друзья! 🎉</h1>
  <div id="countdown"></div>

  <button onclick="showCard()">🎁 Открытка</button>
  <button onclick="generateWish()">✨ Пожелание</button>
  <button onclick="showGallery()">📸 Галерея</button>
  <button onclick="startGame()">🎮 Помоги Деду Морозу</button>

  <div id="card" style="display:none;">
    <h2>🎄 Персональная открытка</h2>
    <p style="font-size: 1.2em; line-height: 1.6;">
      Дорогие друзья!<br>
      Пусть Новый 2026 год принесёт в ваш дом<br>
      радость, удачу, любовь и исполнение самых сокровенных мечтаний!<br>
      ❤️🎅🌟
    </p>
  </div>

  <div id="wish" style="display:none;">
    <h2>🌟 Случайное пожелание</h2>
    <p id="wishText" style="font-size: 1.3em; font-style: italic;"></p>
  </div>

  <div id="gallery" style="display:none;">
    <h2>🎞️ Галерея воспоминаний</h2>
    <div>
      <!-- Ваши изображения - теперь они кликабельные -->
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/1.jpg" alt="Фото 1" onclick="openModal(0)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/2.jpg" alt="Фото 2" onclick="openModal(1)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/3.jpg" alt="Фото 3" onclick="openModal(2)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/4.jpg" alt="Фото 4" onclick="openModal(3)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/5.jpg" alt="Фото 5" onclick="openModal(4)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/6.jpg" alt="Фото 6" onclick="openModal(5)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/7.jpg" alt="Фото 7" onclick="openModal(6)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/8.jpg" alt="Фото 8" onclick="openModal(7)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/9.jpg" alt="Фото 9" onclick="openModal(8)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/10.jpg" alt="Фото 10" onclick="openModal(9)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/11.jpg" alt="Фото 11" onclick="openModal(10)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/12.jpg" alt="Фото 12" onclick="openModal(11)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/13.jpg" alt="Фото 13" onclick="openModal(12)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/14.jpg" alt="Фото 14" onclick="openModal(13)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/15.jpg" alt="Фото 15" onclick="openModal(14)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/16.jpg" alt="Фото 16" onclick="openModal(15)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/17.jpg" alt="Фото 17" onclick="openModal(16)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/18.jpg" alt="Фото 18" onclick="openModal(17)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/19.jpg" alt="Фото 19" onclick="openModal(18)">
      <img src="C:/Users/Windows10/Desktop/Новая папка/images/20.jpg" alt="Фото 20" onclick="openModal(19)">
    </div>
    
    <p style="margin-top: 20px; opacity: 0.8;">
      <small>🎯 Нажмите на любую фотографию для просмотра в полном размере</small>
    </p>
  </div>

  <!-- Модальное окно для полноразмерного просмотра -->
  <div id="imageModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <div class="image-counter" id="imageCounter">1 / 20</div>
    
    <button class="modal-nav prev" onclick="changeImage(-1)">&#10094;</button>
    <button class="modal-nav next" onclick="changeImage(1)">&#10095;</button>
    
    <img class="modal-content" id="fullImage">
    <div id="caption"></div>
  </div>

  <div id="game" style="display:none;">
    <h2>🎅 Дед Мороз собирает шампанское 🥂</h2>
    <p>Помоги Деду Морозу собрать бутылки шампанского для праздничного стола!</p>
    
    <div class="controls">
      <div class="key">←</div>
      <span>Влево</span>
      <div class="key">→</div>
      <span>Вправо</span>
      <div class="key">Пробел</div>
      <span>Пауза</span>
    </div>
    
    <canvas id="gameCanvas" width="600" height="500"></canvas>
    
    <div class="game-stats">
      <div class="stat-item" style="color: gold;">
        🏆 Очки: <span id="score">0</span>
      </div>
      <div class="stat-item" style="color: #4CAF50;">
        🥂 Поймано: <span id="caught">0</span>
      </div>
      <div class="stat-item" style="color: #FF416C;">
        💔 Упущено: <span id="missed">0</span>/10
      </div>
      <div class="stat-item" style="color: #00CED1;">
        ⏱️ Время: <span id="gameTime">00:00</span>
      </div>
    </div>
    
    <div id="message" style="color: #FFD700; font-weight: bold; height: 40px; margin-top: 15px; font-size: 1.1em;"></div>
    
    <div style="margin-top: 20px; font-size: 0.9em; opacity: 0.8;">
      <p>📈 Сложность увеличивается каждые 30 секунд!</p>
    </div>
  </div>

  <script>
    // ============= ФУНКЦИИ ДЛЯ МОДАЛЬНОГО ОКНА =============
    let currentImageIndex = 0;
    
    // Массив с путями к изображениям
    const galleryImages = [
      "C:/Users/Windows10/Desktop/Новая папка/images/1.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/2.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/3.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/4.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/5.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/6.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/7.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/8.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/9.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/10.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/11.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/12.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/13.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/14.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/15.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/16.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/17.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/18.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/19.jpg",
      "C:/Users/Windows10/Desktop/Новая папка/images/20.jpg"
    ];

    // Открыть модальное окно с изображением
    function openModal(index) {
      currentImageIndex = index;
      updateModal();
      document.getElementById('imageModal').style.display = 'block';
      document.body.style.overflow = 'hidden';
    }

    // Закрыть модальное окно
    function closeModal() {
      document.getElementById('imageModal').style.display = 'none';
      document.body.style.overflow = 'auto';
    }

    // Обновить содержимое модального окна
    function updateModal() {
      const modalImg = document.getElementById('fullImage');
      const caption = document.getElementById('caption');
      const counter = document.getElementById('imageCounter');
      
      modalImg.src = galleryImages[currentImageIndex];
      modalImg.alt = `Фото ${currentImageIndex + 1}`;
      caption.textContent = `Воспоминание ${currentImageIndex + 1} из ${galleryImages.length}`;
      counter.textContent = `${currentImageIndex + 1} / ${galleryImages.length}`;
    }

    // Переключение между изображениями
    function changeImage(direction) {
      currentImageIndex += direction;
      
      // Зацикливание
      if (currentImageIndex < 0) {
        currentImageIndex = galleryImages.length - 1;
      } else if (currentImageIndex >= galleryImages.length) {
        currentImageIndex = 0;
      }
      
      updateModal();
    }

    // Управление с клавиатуры
    document.addEventListener('keydown', (e) => {
      const modal = document.getElementById('imageModal');
      if (modal.style.display === 'block') {
        switch(e.key) {
          case 'ArrowLeft':
            changeImage(-1);
            break;
          case 'ArrowRight':
            changeImage(1);
            break;
          case 'Escape':
            closeModal();
            break;
        }
      }
    });

    // Закрыть при клике вне изображения
    document.getElementById('imageModal').onclick = function(event) {
      if (event.target.classList.contains('modal')) {
        closeModal();
      }
    };

    // ============= ВСЕ ОСТАЛЬНЫЕ ФУНКЦИИ =============
    
    // ============= ПРОСТАЯ НОВОГОДНЯЯ МУЗЫКА =============
    function playMusic() {
      const audio = new Audio();
      audio.src = "https://assets.mixkit.co/music/preview/mixkit-jingle-bells-311.mp3";
      audio.loop = true;
      audio.volume = 0.3;
      
      const playPromise = audio.play();
      
      if (playPromise !== undefined) {
        playPromise.catch(error => {
          document.body.addEventListener('click', function startMusicOnClick() {
            audio.play();
            document.body.removeEventListener('click', startMusicOnClick);
          }, { once: true });
        });
      }
    }

    // Запускаем музыку при загрузке страницы
    window.addEventListener('DOMContentLoaded', playMusic);

    // ============= ТАЙМЕР ОБРАТНОГО ОТСЧЁТА =============
    function updateCountdown() {
      const newYear = new Date("Jan 1, 2026 00:00:00").getTime();
      const now = new Date().getTime();
      const diff = newYear - now;

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000*60*60));
      const minutes = Math.floor((diff % (1000*60*60)) / (1000*60));
      const seconds = Math.floor((diff % (1000*60)) / 1000);

      document.getElementById("countdown").innerHTML =
        `🎄 До Нового года: <br><span style="color: gold; font-size: 1.2em;">${days}д ${hours}ч ${minutes}м ${seconds}с</span>`;
    }
    setInterval(updateCountdown, 1000);
    updateCountdown();

    // ============= ОТКРЫТКА =============
    function showCard() {
      hideAll();
      document.getElementById("card").style.display = "block";
    }

    // ============= ГЕНЕРАТОР ПОЖЕЛАНИЙ =============
    const wishes = [
      "Пусть счастье будет рядом весь год, а удача никогда не покидает!",
      "Здоровья крепкого, радости безмерной и сказочного настроения!",
      "Пусть мечты исполняются, а улыбки не исчезают с ваших лиц!",
      "Новых побед, ярких впечатлений и теплых встреч в новом году!",
      "Пусть каждый день будет наполнен волшебством и добротой!",
      "Процветания, гармонии и уюта в вашем доме!",
      "Пусть ангел-хранитель всегда будет рядом и оберегает вас!"
    ];

    function generateWish() {
      hideAll();
      document.getElementById("wish").style.display = "block";
      const randomWish = wishes[Math.floor(Math.random() * wishes.length)];
      document.getElementById("wishText").innerHTML = `"${randomWish}"`;
    }

    // ============= ГАЛЕРЕЯ =============
    function showGallery() {
      hideAll();
      document.getElementById("gallery").style.display = "block";
    }

    // ============= ПОЛНЫЙ КОД ИГРЫ "ПОМОГИ ДЕДУ МОРОЗУ" =============
    function startGame() {
      hideAll();
      document.getElementById("game").style.display = "block";
      
      const canvas = document.getElementById("gameCanvas");
      const ctx = canvas.getContext("2d");
      
      // Игровые переменные
      let score = 0;
      let caught = 0;
      let missed = 0;
      let spawnRate = 0.008;
      let gameSpeed = 1.5;
      let bottles = [];
      let gameActive = true;
      let gamePaused = false;
      let startTime = Date.now();
      let gameTime = 0;
      let difficultyLevel = 1;
      
      // Дед Мороз
      const santa = {
        x: canvas.width / 2 - 50,
        y: canvas.height - 150,
        width: 100,
        height: 150,
        speed: 7,
        direction: 0,
        frame: 0,
        animationSpeed: 0.2
      };
      
      // Массив для разных типов шампанского
      const champagneTypes = [
        { name: "Обычное", color: "#FFD700", points: 10, rarity: 70 },
        { name: "Игристое", color: "#FF69B4", points: 15, rarity: 20 },
        { name: "Винтажное", color: "#C0C0C0", points: 25, rarity: 8 },
        { name: "Подарочное", color: "#00CED1", points: 35, rarity: 2 }
      ];
      
      // Создаем бутылку шампанского
      function createBottle() {
        let rand = Math.random() * 100;
        let selectedType = champagneTypes[0];
        let cumulative = 0;
        
        for (const type of champagneTypes) {
          cumulative += type.rarity;
          if (rand <= cumulative) {
            selectedType = type;
            break;
          }
        }
        
        return {
          x: Math.random() * (canvas.width - 40),
          y: -60,
          width: 25,
          height: 60,
          speed: 1.5 + Math.random() * gameSpeed,
          type: selectedType,
          rotation: Math.random() * 0.1 - 0.05,
          angle: 0,
          sparkle: selectedType.name === "Винтажное" || selectedType.name === "Подарочное"
        };
      }
      
      // Рисуем реалистичного Деда Мороза
      function drawSanta() {
        ctx.save();
        ctx.translate(santa.x + santa.width / 2, santa.y + santa.height);
        
        if (santa.direction !== 0) {
          santa.frame += santa.animationSpeed;
          const walkOffset = Math.sin(santa.frame) * 3;
          ctx.translate(0, walkOffset);
        }
        
        // Ноги (валенки)
        ctx.fillStyle = '#8B4513';
        ctx.fillRect(-30, -40, 20, 30);
        ctx.fillRect(10, -40, 20, 30);
        
        // Шуба
        ctx.fillStyle = '#C41E3A';
        ctx.beginPath();
        ctx.roundRect(-40, -120, 80, 80, 20);
        ctx.fill();
        
        // Меховая опушка
        ctx.fillStyle = 'white';
        ctx.fillRect(-40, -120, 80, 15);
        ctx.fillRect(-40, -40, 15, 80);
        ctx.fillRect(25, -40, 15, 80);
        ctx.fillRect(-40, -45, 80, 15);
        
        // Руки
        ctx.fillStyle = '#C41E3A';
        ctx.fillRect(-50, -80, 20, 40);
        ctx.fillRect(30, -80, 20, 40);
        
        // Мех на рукавах
        ctx.fillStyle = 'white';
        ctx.fillRect(-50, -80, 20, 10);
        ctx.fillRect(30, -80, 20, 10);
        ctx.fillRect(-50, -40, 20, 10);
        ctx.fillRect(30, -40, 20, 10);
        
        // Пояс
        ctx.fillStyle = 'black';
        ctx.fillRect(-30, -60, 60, 8);
        
        // Пряжка
        ctx.fillStyle = 'gold';
        ctx.fillRect(-5, -62, 10, 12);
        
        // Голова
        ctx.fillStyle = '#FFE4C4';
        ctx.beginPath();
        ctx.arc(0, -140, 28, 0, Math.PI * 2);
        ctx.fill();
        
        // Щеки
        ctx.fillStyle = 'rgba(255, 100, 100, 0.3)';
        ctx.beginPath();
        ctx.arc(-15, -135, 8, 0, Math.PI * 2);
        ctx.arc(15, -135, 8, 0, Math.PI * 2);
        ctx.fill();
        
        // Глаза
        ctx.fillStyle = 'black';
        ctx.beginPath();
        ctx.arc(-10, -140, 4, 0, Math.PI * 2);
        ctx.arc(10, -140, 4, 0, Math.PI * 2);
        ctx.fill();
        
        // Нос
        ctx.fillStyle = '#FF8C00';
        ctx.beginPath();
        ctx.ellipse(0, -130, 6, 8, 0, 0, Math.PI * 2);
        ctx.fill();
        
        // Борода
        ctx.fillStyle = 'white';
        ctx.beginPath();
        ctx.ellipse(0, -120, 25, 35, 0, 0, Math.PI * 2);
        ctx.fill();
        
        // Усы
        ctx.beginPath();
        ctx.ellipse(0, -125, 20, 15, 0, 0, Math.PI);
        ctx.fill();
        
        // Шапка
        ctx.fillStyle = '#C41E3A';
        ctx.beginPath();
        ctx.moveTo(-28, -140);
        ctx.lineTo(28, -140);
        ctx.lineTo(20, -180);
        ctx.lineTo(-20, -180);
        ctx.closePath();
        ctx.fill();
        
        // Мех на шапке
        ctx.fillStyle = 'white';
        ctx.fillRect(-28, -140, 56, 10);
        ctx.fillRect(-20, -180, 40, 10);
        
        // Помпон
        ctx.fillStyle = 'white';
        ctx.beginPath();
        ctx.arc(0, -180, 12, 0, Math.PI * 2);
        ctx.fill();
        
        // Мешок
        ctx.fillStyle = '#8B4513';
        ctx.beginPath();
        ctx.roundRect(-25, -20, 50, 40, 10);
        ctx.fill();
        
        // Нить
        ctx.strokeStyle = 'white';
        ctx.lineWidth = 3;
        ctx.beginPath();
        ctx.arc(0, -20, 25, 0, Math.PI);
        ctx.stroke();
        
        ctx.restore();
      }
      
      // Рисуем бутылку шампанского
      function drawBottle(bottle) {
        ctx.save();
        ctx.translate(bottle.x + bottle.width / 2, bottle.y + bottle.height / 2);
        ctx.rotate(bottle.angle);
        bottle.angle += bottle.rotation;
        
        ctx.fillStyle = bottle.type.color;
        ctx.beginPath();
        ctx.moveTo(-bottle.width / 2, bottle.height / 2 - 5);
        ctx.lineTo(-bottle.width / 2 + 5, bottle.height / 2);
        ctx.lineTo(bottle.width / 2 - 5, bottle.height / 2);
        ctx.lineTo(bottle.width / 2, bottle.height / 2 - 5);
        ctx.lineTo(bottle.width / 2, -bottle.height / 2 + 20);
        ctx.lineTo(bottle.width / 2 - 3, -bottle.height / 2 + 15);
        ctx.lineTo(bottle.width / 2 - 8, -bottle.height / 2 + 10);
        ctx.lineTo(bottle.width / 2 - 8, -bottle.height / 2);
        ctx.lineTo(-bottle.width / 2 + 8, -bottle.height / 2);
        ctx.lineTo(-bottle.width / 2 + 8, -bottle.height / 2 + 10);
        ctx.lineTo(-bottle.width / 2 + 3, -bottle.height / 2 + 15);
        ctx.lineTo(-bottle.width / 2, -bottle.height / 2 + 20);
        ctx.closePath();
        ctx.fill();
        
        ctx.fillStyle = '#8B4513';
        ctx.fillRect(-6, -bottle.height / 2, 12, 8);
        
        ctx.fillStyle = bottle.sparkle ? 'gold' : 'silver';
        ctx.fillRect(-6, -bottle.height / 2 + 8, 12, 3);
        
        ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
        ctx.fillRect(-8, -15, 16, 20);
        
        ctx.fillStyle = '#333';
        ctx.font = 'bold 10px Arial';
        ctx.textAlign = 'center';
        ctx.fillText('NV', 0, -5);
        ctx.fillText('2025', 0, 5);
        
        if (bottle.sparkle) {
          ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
          ctx.beginPath();
          ctx.arc(0, -25, 3, 0, Math.PI * 2);
          ctx.fill();
        }
        
        if (bottle.type.name === "Игристое" || bottle.type.name === "Подарочное") {
          for (let i = 0; i < 5; i++) {
            const size = 1 + Math.random() * 2;
            ctx.fillStyle = `rgba(255, 255, 255, ${0.3 + Math.random() * 0.4})`;
            ctx.beginPath();
            ctx.arc(
              Math.random() * 12 - 6,
              Math.random() * 30 - 20,
              size,
              0,
              Math.PI * 2
            );
            ctx.fill();
          }
        }
        
        ctx.restore();
      }
      
      // Рисуем фон
      function drawBackground() {
        const gradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
        gradient.addColorStop(0, '#0a1d3f');
        gradient.addColorStop(0.7, '#1a3b7f');
        gradient.addColorStop(1, '#2a5abf');
        ctx.fillStyle = gradient;
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        
        ctx.fillStyle = 'rgba(255, 255, 255, 0.15)';
        ctx.beginPath();
        for (let x = 0; x < canvas.width; x += 20) {
          const height = 30 + Math.sin(x / 50 + Date.now() / 1000) * 5;
          ctx.rect(x, canvas.height - height, 20, height);
        }
        ctx.fill();
        
        ctx.fillStyle = 'rgba(255, 255, 255, 0.2)';
        for (let i = 0; i < 15; i++) {
          const x = (Date.now() / 80 + i * 70) % canvas.width;
          const y = (Date.now() / 60 + i * 50) % canvas.height;
          ctx.beginPath();
          ctx.arc(x, y, 1.5, 0, Math.PI * 2);
          ctx.fill();
        }
      }
      
      // Проверка столкновения
      function checkCollision(bottle) {
        const santaCenterX = santa.x + santa.width / 2;
        const santaCenterY = santa.y + santa.height - 40;
        
        const bottleCenterX = bottle.x + bottle.width / 2;
        const bottleCenterY = bottle.y + bottle.height / 2;
        
        const distance = Math.sqrt(
          Math.pow(santaCenterX - bottleCenterX, 2) + 
          Math.pow(santaCenterY - bottleCenterY, 2)
        );
        
        return distance < 60;
      }
      
      // Обновляем статистику
      function updateStats() {
        document.getElementById('score').textContent = score;
        document.getElementById('caught').textContent = caught;
        document.getElementById('missed').textContent = missed;
        
        const seconds = Math.floor(gameTime / 1000);
        const minutes = Math.floor(seconds / 60);
        const displaySeconds = seconds % 60;
        document.getElementById('gameTime').textContent = 
          `${minutes.toString().padStart(2, '0')}:${displaySeconds.toString().padStart(2, '0')}`;
      }
      
      // Показываем сообщение
      function showMessage(text, color = '#FFD700') {
        const messageEl = document.getElementById('message');
        messageEl.textContent = text;
        messageEl.style.color = color;
        
        messageEl.style.opacity = '0';
        messageEl.style.transform = 'translateY(-10px)';
        
        setTimeout(() => {
          messageEl.style.transition = 'all 0.3s ease';
          messageEl.style.opacity = '1';
          messageEl.style.transform = 'translateY(0)';
        }, 10);
        
        setTimeout(() => {
          if (messageEl.textContent === text) {
            messageEl.style.opacity = '0';
            messageEl.style.transform = 'translateY(10px)';
            setTimeout(() => {
              if (messageEl.textContent === text) {
                messageEl.textContent = '';
              }
            }, 300);
          }
        }, 2000);
      }
      
      // Обновляем сложность
      function updateDifficulty() {
        const newDifficulty = Math.floor(gameTime / 30000) + 1;
        
        if (newDifficulty > difficultyLevel) {
          difficultyLevel = newDifficulty;
          gameSpeed = 1.5 + (difficultyLevel * 0.3);
          spawnRate = 0.008 + (difficultyLevel * 0.002);
          
          showMessage(
            `📈 Уровень ${difficultyLevel}! Быстрее и больше бутылок!`,
            '#FF69B4'
          );
        }
      }
      
      // Управление
      document.addEventListener('keydown', (e) => {
        if (!gameActive || gamePaused) return;
        
        switch(e.key) {
          case 'ArrowLeft':
            santa.x = Math.max(0, santa.x - santa.speed);
            santa.direction = -1;
            break;
          case 'ArrowRight':
            santa.x = Math.min(canvas.width - santa.width, santa.x + santa.speed);
            santa.direction = 1;
            break;
          case ' ':
            gamePaused = !gamePaused;
            showMessage(gamePaused ? '⏸️ Пауза' : '▶️ Игра продолжается!', '#00CED1');
            if (!gamePaused) gameLoop();
            break;
        }
      });
      
      document.addEventListener('keyup', (e) => {
        if (e.key === 'ArrowLeft' || e.key === 'ArrowRight') {
          santa.direction = 0;
        }
      });
      
      // Игровой цикл
      function gameLoop() {
        if (!gameActive || gamePaused) return;
        
        gameTime = Date.now() - startTime;
        drawBackground();
        drawSanta();
        
        if (Math.random() < spawnRate) {
          bottles.push(createBottle());
        }
        
        for (let i = bottles.length - 1; i >= 0; i--) {
          const bottle = bottles[i];
          bottle.y += bottle.speed;
          
          if (checkCollision(bottle)) {
            score += bottle.type.points;
            caught++;
            bottles.splice(i, 1);
            
            switch(bottle.type.name) {
              case "Винтажное":
                showMessage(`🍾 ВИНТАЖНОЕ ШАМПАНСКОЕ! +${bottle.type.points} очков!`, '#C0C0C0');
                break;
              case "Подарочное":
                showMessage(`🎁 ПОДАРОЧНОЕ ШАМПАНСКОЕ! +${bottle.type.points} очков!`, '#00CED1');
                break;
              case "Игристое":
                showMessage(`✨ ИГРИСТОЕ ШАМПАНСКОЕ! +${bottle.type.points} очков!`, '#FF69B4');
                break;
              default:
                showMessage(`🥂 Шампанское поймано! +${bottle.type.points} очков`, '#FFD700');
            }
            continue;
          }
          
          if (bottle.y > canvas.height + 50) {
            bottles.splice(i, 1);
            missed++;
            
            if (missed % 3 === 0 && missed > 0) {
              showMessage(`💔 Разбилась бутылка! Осторожнее!`, '#FF416C');
            }
          }
          
          drawBottle(bottle);
        }
        
        updateDifficulty();
        
        if (missed >= 10) {
          gameActive = false;
          
          setTimeout(() => {
            const resultMessage = `
🎮 Игра окончена!

🏆 Итоговый счёт: ${score}
🥂 Поймано бутылок: ${caught}
⏱️ Время игры: ${Math.floor(gameTime/1000)} сек.
📈 Уровень сложности: ${difficultyLevel}

Хотите сыграть еще раз?
            `;
            
            if (confirm(resultMessage)) {
              restartGame();
            }
          }, 500);
        }
        
        updateStats();
        requestAnimationFrame(gameLoop);
      }
      
      // Перезапуск игры
      function restartGame() {
        score = 0;
        caught = 0;
        missed = 0;
        spawnRate = 0.008;
        gameSpeed = 1.5;
        bottles = [];
        gameActive = true;
        gamePaused = false;
        difficultyLevel = 1;
        santa.x = canvas.width / 2 - 50;
        santa.direction = 0;
        santa.frame = 0;
        startTime = Date.now();
        gameTime = 0;
        document.getElementById('message').textContent = '';
        showMessage('🎮 Удачи! Помоги Деду Морозу!', '#4CAF50');
        gameLoop();
      }
      
      showMessage('🎮 Управляйте Дедом Морозом стрелками ← →', '#4CAF50');
      gameLoop();
    }

    // Скрыть все блоки
    function hideAll(){
      document.getElementById("card").style.display="none";
      document.getElementById("wish").style.display="none";
      document.getElementById("gallery").style.display="none";
      document.getElementById("game").style.display="none";
    }

    // Снежинки на фоне
    function createSnowflake() {
      const snowflake = document.createElement("div");
      snowflake.classList.add("snowflake");
      snowflake.innerHTML = ["❄", "❅", "❆", "✦", "✧"][Math.floor(Math.random()*5)];
      snowflake.style.left = Math.random() * window.innerWidth + "px";
      snowflake.style.animationDuration = (Math.random()*5+3)+"s";
      snowflake.style.fontSize = (Math.random()*20+15)+"px";
      snowflake.style.opacity = Math.random()*0.6+0.4;
      document.body.appendChild(snowflake);
      setTimeout(()=>snowflake.remove(), 8000);
    }
    setInterval(createSnowflake, 150);

    // Создание блесток
    function createSparkle() {
      if (Math.random() > 0.7) {
        const sparkle = document.createElement("div");
        sparkle.classList.add("sparkle");
        sparkle.style.left = Math.random() * window.innerWidth + "px";
        sparkle.style.top = Math.random() * window.innerHeight + "px";
        sparkle.style.animationDelay = Math.random() * 2 + "s";
        sparkle.style.backgroundColor = ["gold", "silver", "#FF69B4"][Math.floor(Math.random()*3)];
        document.body.appendChild(sparkle);
        setTimeout(()=>sparkle.remove(), 3000);
      }
    }
    setInterval(createSparkle, 100);
  </script>
</body>
</html>
