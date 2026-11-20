<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Flexbox Layout | Gamified Quizzes</title>
<style>
  * { box-sizing: border-box; }
  body { margin: 0; font-family: Arial, sans-serif; background-color: #f2f6ff; }

  /* ===== Flexbox responsive navigation menu ===== */
  header {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    background-color: #333399;
    padding: 0 20px;
  }
  .logo { color: white; font-size: 22px; font-weight: bold; padding: 14px 0; }

  nav ul {
    list-style: none;
    margin: 0; padding: 0;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  nav li { position: relative; }
  nav a {
    display: inline-block;
    padding: 16px 18px;
    color: white;
    text-decoration: none;
  }
  nav a:hover { background-color: #4b5dcc; }

  /* Hover drop-down menu */
  .dropdown {
    display: none;
    position: absolute;
    top: 100%; left: 0;
    z-index: 10;
    min-width: 170px;
    background-color: #333399;
    flex-direction: column;
  }
  nav li:hover > .dropdown { display: flex; }
  .dropdown a { display: block; border-top: 1px solid #667eea; }

  /* ===== Hero + cards using flexbox ===== */
  .hero { text-align: center; padding: 30px 15px 10px; }
  .hero h1 { color: #333399; margin-bottom: 5px; }

  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
  }
  .card {
    flex: 1 1 220px;
    max-width: 300px;
    background-color: white;
    border: 2px solid #667eea;
    border-radius: 15px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 0 8px gray;
  }
  .card h3 { color: #333399; }
  .card button {
    padding: 10px 18px; border: none; border-radius: 8px;
    background-color: #667eea; color: white; cursor: pointer;
  }
  .card button:hover { background-color: #4b5dcc; }

  footer {
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #333399;
    color: white;
    padding: 12px;
    text-align: center;
  }

  /* ===== Responsive: tablet and phone ===== */
  @media (max-width: 768px) {
    header { justify-content: center; }
    nav { width: 100%; }
    nav ul { flex-wrap: wrap; }
  }
  @media (max-width: 480px) {
    header { flex-direction: column; }
    nav ul { flex-direction: column; width: 100%; }
    nav li { width: 100%; text-align: center; }
    nav a { display: block; }
    .dropdown { position: static; }
    footer { flex-direction: column; gap: 6px; }
  }
</style>
</head>
<body>

<header>
  <div class="logo">🎮 QuizQuest</div>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#quizzes">Quizzes ▾</a>
        <ul class="dropdown">
          <li><a href="#html">HTML Quiz</a></li>
          <li><a href="#css">CSS Quiz</a></li>
          <li><a href="#js">JavaScript Quiz</a></li>
        </ul>
      </li>
      <li><a href="#leaderboard">Leaderboard</a></li>
      <li><a href="#rewards">Rewards</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<section class="hero" id="home">
  <h1>Gamified Quizzes for Interactive Learning</h1>
  <p>Learn, play, earn points and level up!</p>
</section>

<section class="cards" id="quizzes">
  <div class="card" id="html">
    <h3>📘 HTML Quiz</h3>
    <p>Test your knowledge of tags and page structure.</p>
    <button>Start</button>
  </div>
  <div class="card" id="css">
    <h3>🎨 CSS Quiz</h3>
    <p>Colors, layouts, flexbox and grid challenges.</p>
    <button>Start</button>
  </div>
  <div class="card" id="js">
    <h3>⚡ JavaScript Quiz</h3>
    <p>Events, DOM and logic questions with bonus points.</p>
    <button>Start</button>
  </div>
</section>

<section class="cards">
  <div class="card" id="leaderboard">
    <h3>🏆 Leaderboard</h3>
    <p>See the top players this week.</p>
  </div>
  <div class="card" id="rewards">
    <h3>🎁 Rewards</h3>
    <p>Collect badges and unlock new levels.</p>
  </div>
</section>

<footer id="contact">
  <span>© 2026 QuizQuest</span>
  <span>Email: support@quizquest.com</span>
  <span>Built with Flexbox</span>
</footer>

</body>
</html>
