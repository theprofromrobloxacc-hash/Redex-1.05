
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Redex 1.05 | Official Website</title>

  <style>
    :root {
      --bg: #080808;
      --card: #151515;
      --accent: #ff2020;
      --text: #ffffff;
      --muted: #aaaaaa;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: Arial, sans-serif;
      transition: background 0.3s;
    }

    header {
      background: #101010;
      border-bottom: 1px solid #292929;
      padding: 17px 6%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo {
      color: var(--accent);
      font-size: 25px;
      font-weight: 900;
      letter-spacing: 1px;
      text-shadow: 0 0 12px var(--accent);
    }

    nav {
      display: flex;
      gap: 22px;
    }

    nav a {
      color: #ddd;
      text-decoration: none;
      font-size: 14px;
    }

    nav a:hover {
      color: var(--accent);
    }

    .menu-button {
      display: none;
      background: none;
      color: white;
      border: none;
      font-size: 26px;
    }

    .hero {
      padding: 95px 20px;
      text-align: center;
      background: radial-gradient(ellipse at top, #4a0808 0%, #080808 65%);
    }

    .hero h1 {
      font-size: clamp(38px, 8vw, 68px);
      font-weight: 900;
      margin-bottom: 15px;
    }

    .hero h1 span {
      color: var(--accent);
      text-shadow: 0 0 20px var(--accent);
    }

    .hero p {
      color: var(--muted);
      font-size: 16px;
      line-height: 1.7;
      max-width: 550px;
      margin: auto;
    }

    .button {
      display: inline-block;
      margin-top: 25px;
      padding: 13px 25px;
      background: var(--accent);
      color: white;
      text-decoration: none;
      border-radius: 9px;
      font-weight: bold;
      border: none;
      cursor: pointer;
      transition: 0.2s;
    }

    .button:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 20px var(--accent);
    }

    .section {
      padding: 55px 6%;
      max-width: 1200px;
      margin: auto;
    }

    .section h2 {
      font-size: 28px;
      margin-bottom: 10px;
    }

    .section-description {
      color: var(--muted);
      margin-bottom: 25px;
      line-height: 1.6;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 18px;
    }

    .card {
      background: var(--card);
      border: 1px solid #292929;
      padding: 24px;
      border-radius: 13px;
      transition: 0.2s;
    }

    .card:hover {
      border-color: var(--accent);
      transform: translateY(-4px);
      box-shadow: 0 0 15px #ff202022;
    }

    .card h3 {
      margin-bottom: 10px;
      font-size: 19px;
    }

    .card p {
      color: var(--muted);
      line-height: 1.6;
      font-size: 14px;
    }

    .card a {
      display: inline-block;
      color: var(--accent);
      text-decoration: none;
      margin-top: 17px;
      font-weight: bold;
    }

    .status {
      display: inline-block;
      background: #102b17;
      color: #55ed78;
      border: 1px solid #286c39;
      padding: 8px 13px;
      border-radius: 30px;
      font-size: 13px;
      margin-top: 20px;
    }

    .settings-button {
      padding: 10px 17px;
      margin: 5px;
      border-radius: 8px;
      border: 1px solid #444;
      background: #202020;
      color: white;
      cursor: pointer;
    }

    .settings-button:hover {
      border-color: var(--accent);
    }

    footer {
      text-align: center;
      padding: 30px 15px;
      border-top: 1px solid #292929;
      color: var(--muted);
      font-size: 13px;
      line-height: 2;
    }

    @media (max-width: 700px) {
      header {
        padding: 15px 5%;
      }

      .menu-button {
        display: block;
      }

      nav {
        display: none;
        position: absolute;
        top: 62px;
        left: 0;
        width: 100%;
        background: #101010;
        padding: 20px;
        flex-direction: column;
        gap: 18px;
        border-bottom: 1px solid #333;
      }

      nav.open {
        display: flex;
      }

      .hero {
        padding: 75px 18px;
      }

      .section {
        padding: 40px 5%;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="logo">REDEX 1.05</div>

    <button class="menu-button" onclick="toggleMenu()">☰</button>

    <nav id="navigation">
      <a href="#home" onclick="closeMenu()">Home</a>
      <a href="#games" onclick="closeMenu()">Games</a>
      <a href="#tutorials" onclick="closeMenu()">Tutorials</a>
      <a href="#utilities" onclick="closeMenu()">Utilities</a>
      <a href="#plus" onclick="closeMenu()">Redex Plus</a>
      <a href="#settings" onclick="closeMenu()">Settings</a>
    </nav>
  </header>

  <main>

    <section class="hero" id="home">
      <h1>WELCOME TO <span>REDEX.</span></h1>
      <p>
        Your central hub for gaming, tutorials, resources,
        utilities and the Redex community.
      </p>
      <div class="status">● Redex website is online</div>
      <br>
      <a href="#explore" class="button">Explore Redex</a>
    </section>

    <section class="section" id="explore">
      <h2>Explore Redex</h2>
      <p class="section-description">
        Find everything you need in one place.
      </p>

      <div class="grid">
        <div class="card" id="games">
          <h3>🎮 Games</h3>
          <p>Discover games and gaming-related content from Redex.</p>
          <a href="#games">Explore →</a>
        </div>

        <div class="card" id="tutorials">
          <h3>📚 Tutorials</h3>
          <p>Learn new things with helpful guides and walkthroughs.</p>
          <a href="#tutorials">View tutorials →</a>
        </div>

        <div class="card" id="utilities">
          <h3>🛠️ Utilities</h3>
          <p>Explore useful utilities and website features.</p>
          <a href="#utilities">Explore utilities →</a>
        </div>

        <div class="card" id="plus">
          <h3>⭐ Redex Plus</h3>
          <p>Discover our upcoming premium membership and exclusive content.</p>
          <a href="https://discord.gg/sEx5WR2PD">Learn more →</a>
        </div>
      </div>
    </section>

    <section class="section" id="resources">
      <h2>Resources</h2>
      <p class="section-description">
        More places to explore around Redex.
      </p>

      <div class="grid">
        <div class="card">
          <h3>💻 Scripts</h3>
          <p>A home for script-related resources and information.</p>
          <a href="#resources">Explore →</a>
        </div>

        <div class="card">
          <h3>🏆 Showcase</h3>
          <p>See projects and creations shared by the community.</p>
          <a href="#resources">View showcase →</a>
        </div>

        <div class="card">
          <h3>📢 Updates</h3>
          <p>Keep up with new features and Redex announcements.</p>
          <a href="#resources">View updates →</a>
        </div>

        <div class="card">
          <h3>❓ FAQ & Support</h3>
          <p>Get help and find answers to common questions.</p>
          <a href="https://discord.gg/sEx5WR2PD">Get support →</a>
        </div>
      </div>
    </section>

    <section class="section" id="community">
      <div class="card">
        <h2>Join the Redex community</h2>
        <p class="section-description">
          Meet other members, get updates and share your ideas.
        </p>
        <a class="button" href="https://discord.gg/sEx5WR2PD">
          Join our Discord
        </a>
      </div>
    </section>

    <section class="section" id="settings">
      <h2>Website settings</h2>
      <p class="section-description">
        Choose a theme for your Redex experience.
        Your selection will be saved on this device.
      </p>

      <div class="card">
        <h3>Choose your theme</h3>
        <br>
        <button class="settings-button" onclick="setTheme('#ff2020')">
          Red
        </button>
        <button class="settings-button" onclick="setTheme('#258cff')">
          Blue
        </button>
        <button class="settings-button" onclick="setTheme('#a855f7')">
          Purple
        </button>
        <button class="settings-button" onclick="setTheme('#ffffff')">
          White
        </button>
      </div>
    </section>

  </main>

  <footer>
    <strong style="color: var(--accent)">REDEX 1.05</strong>
    <br>
    Gaming • Tutorials • Resources • Community
    <br>
    © 2026 Redex. All rights reserved.
  </footer>

  <script>
    function toggleMenu() {
      document.getElementById("navigation").classList.toggle("open");
    }

    function closeMenu() {
      document.getElementById("navigation").classList.remove("open");
    }

    function setTheme(color) {
      document.documentElement.style.setProperty("--accent", color);
      localStorage.setItem("redexTheme", color);
    }

    const savedTheme = localStorage.getItem("redexTheme");

    if (savedTheme) {
      document.documentElement.style.setProperty("--accent", savedTheme);
    }
  </script>

</body>
</html>
