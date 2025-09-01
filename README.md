<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="A Bahamian in China sharing food, language, beauty, weight loss, and dating adventures. Join Tanjanique's journey!">
  <title>Living With Me | A Bahamian in China</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
  
  <!-- Font Awesome for Icons -->
  <script src="https://kit.fontawesome.com/8a9b6a5e3c.js" crossorigin="anonymous"></script>

  <style>
    :root {
      --night-red: #9C1C26;
      --gilded-gold: #D4AF37;
      --bahamas-black: #000000;
      --aqua-blue: #00C7C7;
      --cream: #F8F5F0;
      --shadow: 0 10px 20px rgba(0,0,0,0.3);
      --transition: all 0.3s ease;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: var(--bahamas-black);
      color: white;
      line-height: 1.8;
      overflow-x: hidden;
    }

    h1, h2, h3, h4 {
      font-family: 'Playfair Display', serif;
      margin-bottom: 15px;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 20px;
    }

    /* === Header & Hero === */
    header {
      background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1566554588707-78be08361feb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
      height: 70vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      position: relative;
    }

    .hero-content {
      z-index: 2;
    }

    .hero-content h1 {
      font-size: 3.5em;
      color: var(--aqua-blue);
      text-shadow: 2px 2px 10px rgba(0,0,0,0.9);
      animation: glow 2s infinite alternate;
    }

    .hero-content p {
      font-size: 1.4em;
      color: var(--gilded-gold);
      max-width: 800px;
      margin: 20px auto;
    }

    @keyframes glow {
      0% { text-shadow: 0 0 5px var(--gilded-gold); }
      100% { text-shadow: 0 0 20px var(--gilded-gold), 0 0 30px var(--aqua-blue); }
    }

    /* === Nav === */
    nav {
      background: rgba(0,0,0,0.8);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      padding: 10px 0;
      transition: var(--transition);
    }

    nav ul {
      display: flex;
      justify-content: center;
      list-style: none;
      flex-wrap: wrap;
    }

    nav a {
      color: var(--cream);
      text-decoration: none;
      margin: 0 15px;
      font-weight: 500;
      font-size: 1.1em;
      transition: var(--transition);
      position: relative;
    }

    nav a:hover {
      color: var(--aqua-blue);
    }

    nav a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -5px;
      left: 50%;
      background-color: var(--gilded-gold);
      transition: var(--transition);
    }

    nav a:hover::after {
      width: 100%;
      left: 0;
    }

    /* === About === */
    .about {
      padding: 80px 0;
      background: var(--night-red);
    }

    .profile-img {
      width: 180px;
      height: 180px;
      border-radius: 50%;
      border: 6px solid var(--gilded-gold);
      float: left;
      margin: 0 25px 20px 0;
      box-shadow: 0 0 15px rgba(212, 175, 55, 0.6);
    }

    .about-text p {
      margin-bottom: 15px;
    }

    .about-text strong {
      color: var(--aqua-blue);
    }

    /* === Blog Grid === */
    .blog-grid {
      padding: 80px 0;
      background: var(--bahamas-black);
    }

    .blog-grid h2 {
      text-align: center;
      margin-bottom: 50px;
      color: var(--aqua-blue);
      font-size: 2.2em;
    }

    .card {
      background: #1a1a1a;
      border-left: 5px solid var(--gilded-gold);
      padding: 25px;
      margin: 20px 0;
      border-radius: 12px;
      cursor: pointer;
      transition: var(--transition);
      box-shadow: var(--shadow);
      transform: translateY(0);
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 18px 35px rgba(0,0,0,0.5);
      border-color: var(--aqua-blue);
    }

    .card h3 {
      color: var(--gilded-gold);
      font-size: 1.5em;
    }

    .rating {
      color: var(--aqua-blue);
      font-size: 1.3em;
    }

    .hsk-glow {
      color: var(--gilded-gold);
      font-weight: bold;
      text-shadow: 0 0 12px rgba(212, 175, 55, 0.8);
      font-size: 1.3em;
      background: rgba(212, 175, 55, 0.1);
      padding: 2px 8px;
      border-radius: 5px;
    }

    /* === Gallery === */
    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
      margin-top: 20px;
    }

    .gallery img {
      width: 150px;
      height: 150px;
      object-fit: cover;
      border-radius: 10px;
      border: 3px solid var(--gilded-gold);
      transition: var(--transition);
    }

    .gallery img:hover {
      transform: scale(1.1) rotate(3deg);
      box-shadow: 0 0 20px var(--aqua-blue);
    }

    /* === Contact Form === */
    .contact {
      padding: 80px 0;
      background: #0a0a0a;
      text-align: center;
    }

    .contact h2 {
      color: var(--aqua-blue);
      margin-bottom: 30px;
    }

    .form-container {
      max-width: 600px;
      margin: 0 auto;
      background: #1a1a1a;
      padding: 30px;
      border-radius: 15px;
      box-shadow: var(--shadow);
      border: 1px solid var(--gilded-gold);
    }

    .form-group {
      margin-bottom: 20px;
      text-align: left;
    }

    .form-group label {
      display: block;
      margin-bottom: 8px;
      color: var(--gilded-gold);
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #444;
      background: #222;
      color: white;
      border-radius: 8px;
      font-family: 'Poppins', sans-serif;
    }

    .form-group textarea {
      height: 120px;
    }

    .btn {
      background: var(--gilded-gold);
      color: black;
      padding: 12px 30px;
      border: none;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
      transition: var(--transition);
      font-size: 1.1em;
    }

    .btn:hover {
      background: var(--aqua-blue);
      color: white;
      transform: scale(1.05);
    }

    /* === Footer === */
    footer {
      background: var(--night-red);
      text-align: center;
      padding: 30px 0;
      font-size: 0.95em;
    }

    .social-links a {
      color: var(--aqua-blue);
      margin: 0 10px;
      font-size: 1.5em;
      transition: var(--transition);
    }

    .social-links a:hover {
      color: var(--gilded-gold);
      transform: scale(1.2);
    }

    /* === Modal === */
    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.95);
      overflow: auto;
      animation: fadeIn 0.5s;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .modal-content {
      background: #111;
      margin: 8% auto;
      padding: 35px;
      width: 85%;
      max-width: 650px;
      border-radius: 20px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.6);
      position: relative;
      border: 2px solid var(--gilded-gold);
      color: white;
    }

    .close {
      position: absolute;
      top: 15px;
      right: 25px;
      font-size: 2.2em;
      color: #aaa;
      cursor: pointer;
      font-weight: bold;
    }

    .close:hover {
      color: var(--aqua-blue);
    }

    .modal-content h2 {
      color: var(--gilded-gold);
      text-align: center;
      margin-bottom: 20px;
    }

    /* === Ad Space (Future Monetization) === */
    .ad-space {
      text-align: center;
      margin: 40px 0;
      padding: 20px;
      background: rgba(212, 175, 55, 0.1);
      border: 1px dashed var(--gilded-gold);
      border-radius: 10px;
      color: var(--gilded-gold);
      font-style: italic;
    }

    /* === Responsive === */
    @media (max-width: 768px) {
      .hero-content h1 {
        font-size: 2.5em;
      }
      .hero-content p {
        font-size: 1.1em;
      }
      nav ul {
        gap: 10px;
      }
      .profile-img {
        float: none;
        display: block;
        margin: 0 auto 20px;
      }
      .about-text {
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#journey">Journey</a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#social">Follow Me</a></li>
    </ul>
  </nav>

  <!-- Hero -->
  <header>
    <div class="hero-content">
      <h1>Living With Me</h1>
      <p>Hi, I'm Tanjanique — from the Bahamas to Nanjing, China. One 🥢, 💪, ✍️, 💅🏽, and ❤️ at a time.</p>
    </div>
  </header>

  <!-- About -->
  <section id="about" class="about">
    <div class="container">
      <img src="https://via.placeholder.com/300" alt="Tanjanique" class="profile-img"/>
      <div class="about-text">
        <h2>About Me</h2>
        <p>
          I’m from the sun-kissed shores of the Bahamas, where the ocean sings and life moves at island time. Now, I’m living a whole new rhythm in Nanjing, China—a city of ancient temples, night markets, and steaming bowls of noodles.
        </p>
        <p>
          This blog? It’s my way of sharing this wild, beautiful journey with you. From learning Mandarin one character at a time, to trying stinky tofu (and surviving!), to losing weight, loving my skin, and figuring out love in a new culture—I’m documenting it all.
        </p>
        <p>
          I’m not perfect. I’m learning. I’m growing. And I want you to come along. Grab a snack, kick back, and let’s live this world through my lens. You’re welcome here. Let’s explore.
        </p>
        <p><strong>💛 With love,<br>Tanjanique</strong></p>
      </div>
    </div>
  </section>

  <!-- Journey -->
  <section id="journey" class="blog-grid">
    <div class="container">
      <h2>My Journey</h2>

      <div class="card" onclick="openModal('foodModal')">
        <h3>🍜 Food Adventures</h3>
        <p>Rating: <span class="rating">🥢🥢🥢🥢</span></p>
        <p>Tasting life one bite at a time.</p>
      </div>

      <div class="card" onclick="openModal('weightModal')">
        <h3>💪 Weight Loss Journey</h3>
        <p>Progress: <span class="rating">💪💪💪</span></p>
        <p>One step, one meal, one day at a time.</p>
      </div>

      <div class="card" onclick="openModal('languageModal')">
        <h3>✍️ Learning Mandarin</h3>
        <p>HSK Level: <span class="hsk-glow">HSK 3</span></p>
        <p>Difficulty: <span class="rating">✍️✍️✍️</span></p>
      </div>

      <div class="card" onclick="openModal('beautyModal')">
        <h3>💅🏽 Beauty & Self-Care</h3>
        <p>Routine: <span class="rating">💅🏽💅🏽💅🏽💅🏽</span></p>
        <p>Skincare, haircare, and feeling like me.</p>
      </div>

      <div class="card" onclick="openModal('datingModal')">
        <h3>❤️ Dating in China</h3>
        <p>Vibe: <span class="rating">❤️❤️❤️</span></p>
        <p>Cultural collisions and cute connections.</p>
      </div>

      <div class="card" onclick="openModal('galleryModal')">
        <h3>📸 Photo Gallery</h3>
        <p>Click to see my world.</p>
      </div>

      <div class="card" onclick="openModal('socialModal')">
        <h3>📱 Follow My Journey</h3>
        <p>@livinwithme | @islandbliss-inchina</p>
      </div>
    </div>
  </section>

  <!-- Gallery Modal -->
  <div id="galleryModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('galleryModal')">&times;</span>
      <h2>📸 My World in Pictures</h2>
      <div class="gallery">
        <img src="https://images.unsplash.com/photo-1595218309845-6f37f6a6634a?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Nanjing">
        <img src="https://images.unsplash.com/photo-1607900471727-c95837a568d1?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Night Market">
        <img src="https://images.unsplash.com/photo-1546074174-98edf549ba0f?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Food">
        <img src="https://images.unsplash.com/photo-1587806571254-708efc4f5e84?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Temple">
      </div>
    </div>
  </div>

  <!-- Social Modal -->
  <div id="socialModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('socialModal')">&times;</span>
      <h2>📱 Follow My Journey</h2>
      <p><i class="fab fa-instagram"></i> <a href="https://instagram.com/livinwithme" target="_blank">@livinwithme</a></p>
      <p><i class="fab fa-tiktok"></i> <a href="https://tiktok.com/@islandbliss-inchina" target="_blank">@islandbliss-inchina</a></p>
      <p><i class="fab fa-youtube"></i> <a href="https://youtube.com/@IslandBliss-inChina" target="_blank">@IslandBliss-inChina</a></p>
      <p><strong>Latest Post:</strong> “My First Hot Pot Experience!” — check it out!</p>
    </div>
  </div>

  <!-- Other Modals (Food, Weight, etc.) -->
  <div id="foodModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('foodModal')">&times;</span>
      <h2>🥢 Food Adventures</h2>
      <p><strong>Spicy Dan Dan Noodles – 🥢🥢🥢🥢</strong><br>So nummy but my nose won’t stop running!</p>
      <p><strong>Stinky Tofu – 🥢🥢🥢</strong><br>Smelled like trash… tasted like heaven?</p>
      <p><strong>Homemade Conch Fritters – 🥢🥢🥢🥢🥢</strong><br>Brought a taste of home to China!</p>
    </div>
  </div>

  <div id="weightModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('weightModal')">&times;</span>
      <h2>💪 Weight Loss Journey</h2>
      <p><strong>Day 12:</strong> 30-min walk + no sugar – 💪💪💪</p>
      <p>Focusing on portion control and daily movement. Progress takes time!</p>
    </div>
  </div>

  <div id="languageModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('languageModal')">&times;</span>
      <h2>✍️ Learning Mandarin</h2>
      <p><strong>HSK 3 Word:</strong> 喜欢 (xǐhuan) – to like</p>
      <p>Difficulty: <span class="rating">✍️✍️</span></p>
      <p>Still mixing it up with 爱 (ài)… but getting there!</p>
    </div>
  </div>

  <div id="beautyModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('beautyModal')">&times;</span>
      <h2>💅🏽 Beauty & Self-Care</h2>
      <p><strong>DIY Rice Water Rinse – 💅🏽💅🏽💅🏽💅🏽</strong><br>My hair feels like silk!</p>
      <p>Using local Chinese products + island remedies.</p>
    </div>
  </div>

  <div id="datingModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('datingModal')">&times;</span>
      <h2>❤️ Dating in China</h2>
      <p><strong>Tinder in Nanjing – ❤️❤️</strong><br>Cute messages, but… language barrier!</p>
      <p>Learning how love works here — it’s different, but beautiful.</p>
    </div>
  </div>

  <!-- Contact -->
  <section id="contact" class="contact">
    <div class="container">
      <h2>💌 Send Me a Message</h2>
      <div class="form-container">
        <form action="https://formspree.io/f/travelingislandbliss@gmail.com" method="POST">
          <div class="form-group">
            <label for="name">Your Name</label>
            <input type="text" id="name" name="name" required />
          </div>
          <div class="form-group">
            <label for="email">Your Email</label>
            <input type="email" id="email" name="email" required />
          </div>
          <div class="form-group">
            <label for="message">Your Message</label>
            <textarea id="message" name="message" required></textarea>
          </div>
          <button type="submit" class="btn">Send Message</button>
        </form>
      </div>
      <div class="ad-space">
        Future Ad Space for Google AdSense (Monetization Coming Soon!)
      </div>
    </div>
  </section>

  <!-- Social Footer -->
  <section id="social" class="about">
    <div class="container" style="text-align:center;">
      <h2>Let’s Connect!</h2>
      <div class="social-links">
        <a href="https://instagram.com/livinwithme" target="_blank"><i class="fab fa-instagram"></i></a>
        <a href="https://tiktok.com/@islandbliss-inchina" target="_blank"><i class="fab fa-tiktok"></i></a>
        <a href="https://youtube.com/@IslandBliss-inChina" target="_blank"><i class="fab fa-youtube"></i></a>
      </div>
      <p style="margin-top:20px;">New videos and updates weekly!</p>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 Tanjanique | <strong>Living With Me</strong>. All rights reserved.</p>
      <p>From the Bahamas to China — one adventure at a time.</p>
    </div>
  </footer>

  <!-- JavaScript -->
  <script>
    function openModal(id) {
      document.getElementById(id).style.display = "block";
    }

    function closeModal(id) {
      document.getElementById(id).style.display = "none";
    }

    // Close modal when clicking outside
    window.onclick = function(event) {
      const modals = document.querySelectorAll('.modal');
      modals.forEach(modal => {
        if (event.target === modal) {
          modal.style.display = "none";
        }
      });
    }

    // Smooth scroll for nav
    document.querySelectorAll('nav a').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        window.scrollTo({
          top: target.offsetTop - 80,
          behavior: 'smooth'
        });
      });
    });
  </script>

</body>
</html>
