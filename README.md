<!DOCTYPE html>
<html lang="bg">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>RadevTech - Програмиране и Игри</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background: #0a0d18;
      color: #e0e6f3;
      line-height: 1.6;
    }
    a {
      color: #4fc3f7;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
    header {
      background: #121726;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 10px rgba(79,195,247,0.3);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    header h1 {
      margin: 0;
      font-weight: 700;
      color: #4fc3f7;
      letter-spacing: 2px;
      cursor: default;
    }
    nav a {
      margin-left: 25px;
      font-weight: 600;
      transition: color 0.3s ease;
    }
    nav a:hover {
      color: #82ccff;
    }
    #hero {
      background: linear-gradient(135deg, #0a0d18, #1f2a4d);
      position: relative;
      text-align: center;
      padding: 140px 20px 100px;
      overflow: hidden;
    }
    #hero::before {
      content: "";
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle at center, rgba(79,195,247,0.25), transparent 70%);
      animation: moveGlow 6s linear infinite;
      z-index: 0;
    }
    @keyframes moveGlow {
      0% { transform: translate(0,0); }
      50% { transform: translate(30px,30px); }
      100% { transform: translate(0,0); }
    }
    #hero h2 {
      font-size: 3.6rem;
      margin-bottom: 15px;
      position: relative;
      z-index: 1;
      overflow: hidden;
      white-space: nowrap;
      border-right: 3px solid #4fc3f7;
      animation: typing 3s steps(14) forwards, pulse 2s ease-in-out infinite;
      max-width: 14ch;
      margin-left: auto;
      margin-right: auto;
    }
    @keyframes typing {
      from { width: 0; }
      to { width: 14ch; }
    }
    @keyframes pulse {
      0%, 100% { text-shadow: 0 0 8px #4fc3f7; }
      50% { text-shadow: 0 0 24px #82ccff; }
    }
    #hero p {
      font-size: 1.4rem;
      max-width: 600px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
      color: #a8b9d9;
    }
    section {
      max-width: 900px;
      margin: 80px auto;
      padding: 0 20px;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.8s ease-out, transform 0.8s ease-out;
    }
    section.visible {
      opacity: 1;
      transform: none;
    }
    section h3 {
      font-size: 2.2rem;
      margin-bottom: 20px;
      color: #4fc3f7;
      border-bottom: 2px solid #4fc3f7;
      display: inline-block;
      padding-bottom: 6px;
    }
    section p {
      font-size: 1.1rem;
      color: #c3cee5;
    }
    button {
      cursor: pointer;
      background: linear-gradient(45deg, #4fc3f7, #82ccff);
      box-shadow: 0 5px 20px rgba(130, 204, 255, 0.6);
      border: none;
      color: #fff;
      font-weight: 700;
      padding: 12px 30px;
      font-size: 1.1rem;
      border-radius: 30px;
      transition: background-position 0.6s ease, box-shadow 0.3s ease;
      background-size: 200% 200%;
      background-position: 0% 50%;
      margin-top: 20px;
      display: inline-block;
    }
    button:hover {
      background-position: 100% 50%;
      box-shadow: 0 8px 30px rgba(130, 204, 255, 0.9);
    }
    footer {
      text-align: center;
      padding: 30px 15px;
      background: #121726;
      color: #556688;
      font-size: 0.9rem;
      margin-top: 80px;
      letter-spacing: 1px;
    }
    @media (max-width: 600px) {
      #hero h2 {
        font-size: 2.6rem;
        max-width: 100%;
        border-right: none;
        animation: none;
      }
      nav a {
        margin-left: 15px;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>RadevTech</h1>
  <nav>
    <a href="#hero">Начало</a>
    <a href="#products">Продукти</a>
    <a href="#about">За нас</a>
    <a href="#contact">Контакт</a>
  </nav>
</header>

<main>
  <section id="hero" aria-label="Въведение">
    <h2>RadevTech</h2>
    <p>Създаваме висококачествени приложения и игри, които вдъхновяват и забавляват потребителите.</p>
  </section>

  <section id="products" aria-label="Нашите продукти">
    <h3>Нашите продукти</h3>
    <p>Разработваме мобилни и десктоп приложения, както и игри с уникален дизайн и иновативни функции.</p>
    <a href="CryptoTraderGame3.0.zip" download>
      <button>Изтегли Crypto Trader Game 3.0</button>
    </a>
  </section>

  <section id="about" aria-label="За компанията">
    <h3>За нас</h3>
    <p>RadevTech е българска софтуерна агенция, фокусирана върху създаването на качествени и иновативни дигитални продукти.</p>
  </section>

  <section id="contact" aria-label="Свържете се с нас">
    <h3>Свържете се с нас</h3>
    <p>Имейл: info@radevtech.bg</p>
    <p>Телефон: +359 88 123 4567</p>
    <button onclick="window.location='mailto:info@radevtech.bg'">Пишете ни</button>
  </section>
</main>

<footer>
  &copy; 2025 RadevTech. Всички права запазени.
</footer>

<script>
  function fadeInOnScroll() {
    const sections = document.querySelectorAll('section');
    const windowBottom = window.innerHeight + window.pageYOffset;

    sections.forEach(section => {
      if (section.offsetTop < windowBottom - 50) {
        section.classList.add('visible');
      }
    });
  }
  window.addEventListener('scroll', fadeInOnScroll);
  window.addEventListener('load', fadeInOnScroll);
</script>

</body>
</html>
