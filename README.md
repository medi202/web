<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dark Theme Header - Lash Therapy</title>
  <link rel="stylesheet" href="shop.html">
  
  
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #121212;
      color: #fff;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    header {
      width: 100%;
      background-color: #1f1f1f;
      padding: 16px 32px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.6);
    }

    .logo {
      font-size: 1.6rem;
      font-weight: bold;
      color: #ff69b4;
      letter-spacing: 1px;
    }

    .nav-links {
      display: flex;
      gap: 24px;
    }

    .nav-links a {
      font-weight: 500;
      padding: 6px 0;
      transition: color 0.3s ease;
      color: #ccc;
    }

    .nav-links a:hover {
      color: #ff69b4;
    }

    .menu-toggle {
      display: none;
      font-size: 24px;
      cursor: pointer;
      color: #fff;
    }

    /* Mobile Menu */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 72px;
        right: 0;
        background-color: #1f1f1f;
        width: 220px;
        padding: 20px;
        box-shadow: -4px 4px 12px rgba(0,0,0,0.5);
      }

      .nav-links.active {
        display: flex;
      }

      .menu-toggle {
        display: block;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">Lash Therapy</div>
    <nav class="nav-links" id="navLinks">
      <a href="#features">SHOP</a>
      <a href="#benefits">REVIEWS</a>
      <a href="#reviews">STOCKISTS</a>
      <a href="#shop">ABOUT US</a>
    </nav>
    <div class="menu-toggle" id="menuToggle">
      <i class="fas fa-bars"></i>
    </div>
  </header>

  <script>
    // Toggle mobile menu
    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {
      navLinks.classList.toggle("active");
    });
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Eyeliner Hero Section</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: #111;
      color: #fff;
    }

    .hero {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 80px 20px;
      text-align: center;
      background: linear-gradient(to bottom, #000, #111);
      background-image:url();
      background-size: cover;
      background-position: center;
      position: relative;
    }

    .hero::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.7);
      z-index: 1;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 800px;
    }

    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      margin-bottom: 20px;
      color: #f3c1d8;
    }

    .hero p {
      font-size: 1.2rem;
      margin-bottom: 30px;
      color: #ddd;
    }

    .hero .cta-button {
      background-color: #f3c1d8;
      color: #111;
      border: none;
      padding: 14px 30px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .hero .cta-button:hover {
      background-color: #eaa8c3;
    }

    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.2rem;
      }

      .hero p {
        font-size: 1rem;
      }
    }

    @media (max-width: 480px) {
      .hero {
        padding: 60px 15px;
      }

      .hero h1 {
        font-size: 1.8rem;
      }

      .hero .cta-button {
        width: 100%;
        padding: 12px;
      }
    }
  </style>
</head>
<body>

  <section class="hero">
    <div class="hero-content">
      <h1>Define Your Eyes with Elegance</h1>
      <p>Smudge-proof. All-day wear. Effortless beauty at your fingertips.</p>
      <button class="cta-button">Shop Now</button>
    </div>
  </section>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Key Benefits Section</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
      margin: 0;
      background-color: #111;
      color: #fff;
    }

    .benefits-section {
      padding: 60px 20px;
      text-align: center;
      background-color: #111;
    }

    .benefits-section h2 {
      font-size: 2.2rem;
      margin-bottom: 40px;
      color: #f3c1d8;
    }

    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 30px;
      max-width: 1000px;
      margin: 0 auto;
    }

    .benefit-item {
      background-color: #1a1a1a;
      border-radius: 16px;
      padding: 30px 20px;
      transition: transform 0.3s ease, background 0.3s ease;
      border: 1px solid #333;
    }

    .benefit-item:hover {
      background-color: #222;
      transform: translateY(-5px);
    }

    .benefit-icon {
      font-size: 2.5rem;
      color: #f3c1d8;
      margin-bottom: 15px;
    }

    .benefit-title {
      font-size: 1.2rem;
      margin-bottom: 10px;
      font-weight: 600;
    }

    .benefit-desc {
      font-size: 0.95rem;
      color: #ccc;
    }

    @media (max-width: 480px) {
      .benefits-section h2 {
        font-size: 1.8rem;
      }

      .benefit-item {
        padding: 25px 15px;
      }
    }
  </style>
</head>
<body>

  <section class="benefits-section">
    <h2>Why You'll Love It</h2>
    <div class="benefits-grid">
      <div class="benefit-item">
        <div class="benefit-icon">💧</div>
        <div class="benefit-title">Waterproof</div>
        <div class="benefit-desc">Rain or shine, your look stays flawless all day.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-icon">🕒</div>
        <div class="benefit-title">Long-Lasting</div>
        <div class="benefit-desc">12+ hour wear with zero smudging or fading.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-icon">🌱</div>
        <div class="benefit-title">Vegan Formula</div>
        <div class="benefit-desc">100% cruelty-free, kind to animals and your skin.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-icon">👁️</div>
        <div class="benefit-title">Gentle on Eyes</div>
        <div class="benefit-desc">Perfect for sensitive eyes and contact lens wearers.</div>
      </div>
    </div>
  </section>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>How It Works</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
      margin: 0;
      background-color: #111;
      color: #fff;
    }

    .how-section {
      padding: 60px 20px;
      background-color: #111;
      text-align: center;
    }

    .how-section h2 {
      font-size: 2.2rem;
      color: #f3c1d8;
      margin-bottom: 40px;
    }

    .steps-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 30px;
      max-width: 1000px;
      margin: 0 auto;
    }

    .step-card {
      background-color: #1a1a1a;
      padding: 30px 20px;
      border-radius: 16px;
      border: 1px solid #333;
      transition: transform 0.3s ease;
    }

    .step-card:hover {
      transform: translateY(-5px);
    }

    .step-number {
      font-size: 1.2rem;
      color: #f3c1d8;
      margin-bottom: 10px;
      font-weight: 600;
    }

    .step-icon {
      font-size: 2.5rem;
      margin-bottom: 15px;
      color: #f3c1d8;
    }

    .step-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .step-desc {
      font-size: 0.95rem;
      color: #ccc;
    }

    @media (max-width: 480px) {
      .how-section h2 {
        font-size: 1.8rem;
      }

      .step-card {
        padding: 25px 15px;
      }
    }
  </style>
</head>
<body>

  <section class="how-section">
    <h2>How to Apply</h2>
    <div class="steps-grid">
      <div class="step-card">
        <div class="step-number">Step 1</div>
        <div class="step-icon">🧼</div>
        <div class="step-title">Prep Your Eyes</div>
        <div class="step-desc">Start with clean, dry eyelids. Apply primer for smooth application.</div>
      </div>
      <div class="step-card">
        <div class="step-number">Step 2</div>
        <div class="step-icon">✍️</div>
        <div class="step-title">Apply Eyeliner</div>
        <div class="step-desc">Draw a precise line along your lash line — thin for daytime, bold for drama.</div>
      </div>
      <div class="step-card">
        <div class="step-number">Step 3</div>
        <div class="step-icon">💁‍♀️</div>
        <div class="step-title">Flaunt Your Look</div>
        <div class="step-desc">Let dry for a few seconds. You're ready to conquer the day — smudge-free.</div>
      </div>
    </div>
  </section>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Social Proof Gallery</title>
  <link rel="stylesheet" href="styles.css" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
</head>
<body>

  <section class="gallery-section">
    <h2>Join the Glow-Up</h2>
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="https://source.unsplash.com/300x300/?makeup,eye1" alt="User Look 1" />
        <div class="caption">@glowwithmia</div>
      </div>
      <div class="gallery-item">
        <img src="https://source.unsplash.com/300x300/?eyeliner,makeup" alt="User Look 2" />
        <div class="caption">@beautybyzara</div>
      </div>
      <div class="gallery-item">
        <img src="https://source.unsplash.com/300x300/?eye,beauty" alt="User Look 3" />
        <div class="caption">@fierceandfine</div>
      </div>
      <div class="gallery-item">
        <img src="https://source.unsplash.com/300x300/?cosmetics,eye" alt="User Look 4" />
        <div class="caption">@linerqueen</div>
      </div>
      <div class="gallery-item">
        <img src="https://source.unsplash.com/300x300/?glam,eye" alt="User Look 5" />
        <div class="caption">@urbanbeauty</div>
      </div>
    </div>
  </section>

</body>
</html>
