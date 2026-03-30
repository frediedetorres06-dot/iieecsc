# iieecsc
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>IIEE - CSC</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: #0f172a;
  color: white;
  scroll-behavior: smooth;

  /* ADDED ONLY */
  padding-top: 110px;
}

/* NAVBAR */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  background: rgba(0,0,0,0.6);
  backdrop-filter: blur(10px);
  border-radius: 50px;
  margin: 20px;

  /* ADDED ONLY */
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 999;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 600;
}

.logo img {
  width: 40px;
}

.logo-text {
  display: flex;
  flex-direction: column;
  font-size: 12px;
  line-height: 1.2;
}

.nav-links {
  display: flex;
  gap: 25px;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-size: 14px;
  transition: 0.3s;
  cursor: pointer;
}

.nav-links a:hover {
  opacity: 0.7;
}

/* HERO */
.hero {
  margin: 40px;
  padding: 80px 40px;
  border-radius: 30px;
  background: linear-gradient(135deg, #ff004c, #ff7a00, #00c6ff, #7b2ff7);
  background-size: 300% 300%;
  animation: gradientMove 5s ease infinite;
  text-align: center;
}

@keyframes gradientMove {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.hero h1 {
  font-size: 48px;
  font-weight: 700;
}

.hero p {
  margin-top: 10px;
  font-size: 18px;
  opacity: 0.9;
}

.hero .logos img {
  width: 120px;
  margin: 0 15px;
}

/* BUTTONS */
.btn {
  padding: 10px 20px;
  border-radius: 25px;
  border: none;
  margin: 5px;
  cursor: pointer;
  font-weight: 500;
  transition: 0.3s;
}

.btn-primary {
  background: white;
  color: black;
}

.btn-outline {
  background: transparent;
  border: 1px solid white;
  color: white;
}

.btn:hover {
  transform: scale(1.05);
}

/* ABOUT */
.about {
  margin: 40px;
  padding: 60px 40px;
  border-radius: 30px;
  background: linear-gradient(135deg, rgba(255, 0, 76, 0.25), rgba(0, 198, 255, 0.15), rgba(123, 47, 247, 0.2));
  backdrop-filter: blur(12px);
  text-align: center;
  border: 1px solid rgba(255,255,255,0.1);

  display: none;
}

.about-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
  margin-bottom: 10px;
}

.about-header img {
  width: 150px;
  height: auto;
}

.about h2 {
  font-size: 36px;
}

.about p {
  max-width: 900px;
  margin: 10px auto 30px;
  font-size: 16px;
  opacity: 0.85;
  line-height: 1.6;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
}

.about-card {
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 20px;
  padding: 25px;
  backdrop-filter: blur(15px);
  text-align: left;
  transition: 0.3s;
}

.about-card:hover {
  transform: translateY(-5px);
  background: rgba(255,255,255,0.12);
}

.about-card h3 {
  margin-bottom: 10px;
}

.about-card p,
.about-card li {
  font-size: 14px;
  opacity: 0.9;
  line-height: 1.5;
}

.about-card ul {
  padding-left: 18px;
}

/* FOOTER */
footer {
  text-align: center;
  margin-top: 40px;
  padding: 20px;
  opacity: 0.7;
}

/* LIGHT MODE ONLY */
body.light-mode {
  background: #f5f7ff;
  color: #111;
}

body.light-mode .navbar {
  background: rgba(255,255,255,0.7);
}

body.light-mode .nav-links a {
  color: #111;
}

body.light-mode .about-card {
  background: rgba(0,0,0,0.05);
  border: 1px solid rgba(0,0,0,0.1);
}

body.light-mode footer {
  color: #111;
}
</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">
  <div class="logo">
    <img src="iiee.png">
    <img src="csc.png">
    <div class="logo-text">
      <span>Institute of Integrated Electrical Engineers of the Philippines Inc.</span>
      <span>Council of Student Chapters</span>
    </div>
  </div>

  <div class="nav-links">
    <a onclick="showHome()">Home</a>
    <a onclick="showAbout()">About</a>
    <a href="#">Events</a>
    <a href="#">Officers</a>
    <a href="#">Membership</a>
    <a href="#">Contact</a>
    <a onclick="toggleTheme()">🌓</a>
  </div>
</div>

<!-- HERO -->
<section class="hero" id="home">
  <div class="logos">
    <img src="iiee.png">
    <img src="csc.png">
  </div>

  <h1>IIEE - Council of Student Chapters</h1>
  <p>Committed to serve and cultivate future Electrical Engineers</p>
</section>

<!-- ABOUT -->
<section class="about" id="about">

  <div class="about-header">
    <img src="csc.png">
    <h2>WHAT IS IIEE-CSC?</h2>
  </div>

  <p>
    The IIEE-CSC is a non-stock, non-profit organization that serves as the official umbrella organization of all recognized electrical engineering and electrical technology student chapters across the country. It functions under the supervision of the IIEE Student Affairs Committee (SAC).
  </p>

  <div class="about-grid">

    <div class="about-card">
      <h3>OUR VISION</h3>
      <p>To be the best and most prestigious technical student organization in the Philippines.</p>
    </div>

    <div class="about-card">
      <h3>OUR MISSION</h3>
      <ul>
        <li>To help in improving the academic performance of all Electrical Engineering (EE) and Electrical Technology (ET) students in the archipelago and to serve as a channel of information about current issues and trends in EE and ET education system and industry.</li>
        <li>To hone and nurture the leadership abilities, skills, and principles of student members in order to act with integrity and passion to serve as future leaders of the IIEE and its country.</li>
        <li>To foster unity among its members by acting as the core and prime mover for programs and activities that will provide opportunities for personal growth and self-development of its members.</li>
        <li>To encourage its members to support, participate, and undertake the challenges of globalization and social awareness.</li>
      </ul>
    </div>

    <div class="about-card">
      <h3>OUR PURPOSE</h3>
      <ul>
        The IIEE-CSC shall at all times:
        <li>Provide students with beneficial opportunities participate in relevant academic, professional, networking, and cultural activities;</li>
        <li>Energize student interest, awareness, and understanding of the duties and responsibilities of an electrical engineering student and imbibe them with desirable motivations and correct values;</li>
        <li>Formulate and adopt policies, measures, and programs with the view of fostering the educational advancement In the field of electricity;</li>
        <li>Establish unity and closer cooperative relationships among students of different schools and between student-professional, and studentgraduate. and;</li>
        <li>Defend, promote and protect the rights and welfare of the students.</li>
      </ul>
    </div>

  </div>
</section>

<footer>
© 2026 IIEE-CSC | All Rights Reserved
</footer>

<script>
function showAbout() {
  document.getElementById("about").style.display = "block";
  document.getElementById("home").style.display = "none";
}

function showHome() {
  document.getElementById("about").style.display = "none";
  document.getElementById("home").style.display = "block";
}

showHome();

function toggleTheme() {
  document.body.classList.toggle("light-mode");
}
</script>

</body>
</html>
