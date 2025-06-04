# HTML_CSS
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tran Van Thuan - Software Engineer Portfolio</title>
    <!-- Google Fonts -->
    <link
      href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;700&display=swap"
      rel="stylesheet"
    />
    <!-- Font Awesome -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />
    <style>
      body {
        margin: 0;
        font-family: "Space Grotesk", Arial, sans-serif;
        background: linear-gradient(120deg, #fff 0%, #38bdf8 100%);
        color: #22223b;
        min-height: 100vh;
      }
      .container {
        max-width: 900px;
        margin: 40px auto 0 auto;
        background: rgba(255, 255, 255, 0.98);
        border-radius: 18px;
        box-shadow: 0 8px 32px rgba(30, 41, 59, 0.13);
        padding: 40px 32px 32px 32px;
        animation: fadeInUp 1.2s;
      }
      @keyframes fadeInUp {
        from {
          opacity: 0;
          transform: translateY(40px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      header {
        display: flex;
        align-items: center;
        gap: 32px;
        border-bottom: 1px solid #e0e7ef;
        padding-bottom: 32px;
        flex-wrap: wrap;
      }
      .avatar {
        width: 130px;
        height: 130px;
        border-radius: 50%;
        border: 5px solid #38bdf8;
        object-fit: cover;
        box-shadow: 0 4px 24px rgba(56, 189, 248, 0.18);
        background: #fff;
      }
      .intro {
        flex: 1;
        min-width: 220px;
      }
      .intro h1 {
        font-size: 2.3rem;
        color: #38bdf8;
        margin: 0 0 8px 0;
        letter-spacing: 1px;
      }
      .intro h2 {
        font-size: 1.1rem;
        color: #0ea5e9;
        margin: 0 0 16px 0;
        font-weight: 400;
      }
      .intro p {
        color: #22223b;
        margin-bottom: 18px;
        font-size: 1.08rem;
      }
      .social {
        margin-top: 10px;
      }
      .social a {
        color: #38bdf8;
        margin-right: 18px;
        font-size: 1.7rem;
        transition: color 0.2s, transform 0.2s;
        text-decoration: none;
      }
      .social a:hover {
        color: #0ea5e9;
        transform: scale(1.2);
      }
      .info-list {
        display: flex;
        flex-wrap: wrap;
        gap: 24px;
        margin: 28px 0 0 0;
        padding: 0;
        list-style: none;
      }
      .info-list li {
        background: #e0f2fe;
        border-radius: 8px;
        padding: 14px 22px;
        color: #22223b;
        font-size: 1.08rem;
        min-width: 180px;
        box-shadow: 0 2px 8px rgba(56, 189, 248, 0.08);
        display: flex;
        align-items: center;
        gap: 10px;
      }
      .highlight {
        color: #38bdf8;
        font-weight: bold;
      }
      /* Skills Progress Bar */
      .skills {
        margin: 38px 0 0 0;
      }
      .skills-title {
        color: #38bdf8;
        font-size: 1.2rem;
        margin-bottom: 12px;
        font-weight: bold;
      }
      .skill-bar {
        margin-bottom: 16px;
      }
      .skill-label {
        font-size: 1rem;
        margin-bottom: 4px;
        color: #0ea5e9;
      }
      .bar-bg {
        background: #e0e7ef;
        border-radius: 8px;
        height: 12px;
        width: 100%;
        overflow: hidden;
      }
      .bar-fill {
        height: 100%;
        border-radius: 8px;
        background: linear-gradient(90deg, #38bdf8 60%, #0ea5e9 100%);
        transition: width 0.6s;
      }
      /* Buttons */
      .btn-main {
        display: inline-block;
        margin-top: 18px;
        padding: 10px 22px;
        background: linear-gradient(90deg, #38bdf8 60%, #0ea5e9 100%);
        color: #fff;
        font-weight: bold;
        border: none;
        border-radius: 8px;
        font-size: 1.08rem;
        text-decoration: none;
        box-shadow: 0 2px 8px rgba(56, 189, 248, 0.13);
        transition: background 0.2s, transform 0.15s, box-shadow 0.2s;
        cursor: pointer;
      }
      .btn-main i {
        margin-right: 8px;
      }
      .btn-main:hover {
        background: linear-gradient(90deg, #0ea5e9 60%, #38bdf8 100%);
        transform: translateY(-2px) scale(1.07);
        box-shadow: 0 8px 24px rgba(56, 189, 248, 0.18);
        color: #fff;
        text-decoration: none;
      }
      /* Section Titles */
      .section-title {
        color: #38bdf8;
        font-size: 1.3rem;
        margin-bottom: 18px;
        font-weight: bold;
        letter-spacing: 1px;
      }
      /* Projects */
      .projects {
        margin: 48px 0 0 0;
      }
      .projects h3 {
        color: #38bdf8;
        font-size: 1.2rem;
        margin-bottom: 18px;
        font-weight: bold;
      }
      .project-card {
        background: #f1f5f9;
        border-radius: 12px;
        padding: 22px 24px;
        margin-bottom: 18px;
        box-shadow: 0 2px 8px rgba(56, 189, 248, 0.08);
        transition: transform 0.15s, box-shadow 0.15s;
        border-left: 6px solid #38bdf8;
        animation: fadeInUp 1s;
      }
      .project-card:hover {
        transform: translateY(-4px) scale(1.02);
        box-shadow: 0 6px 24px rgba(56, 189, 248, 0.13);
      }
      .project-title {
        font-size: 1.15rem;
        color: #22223b;
        margin-bottom: 8px;
        font-weight: bold;
      }
      .project-desc {
        color: #0f172a;
        font-size: 1.05rem;
        margin-bottom: 6px;
      }
      .project-link {
        color: #38bdf8;
        text-decoration: none;
        font-size: 1rem;
      }
      .project-link:hover {
        text-decoration: underline;
      }
      /* Experience */
      .experience {
        margin: 40px 0 0 0;
      }
      .exp-list {
        list-style: none;
        padding: 0;
        margin: 0;
      }
      .exp-list li {
        margin-bottom: 12px;
        color: #22223b;
        font-size: 1.05rem;
        padding-left: 24px;
        position: relative;
      }
      .exp-list li:before {
        content: "★";
        color: #38bdf8;
        position: absolute;
        left: 0;
        font-size: 1rem;
      }
      /* Responsive */
      @media (max-width: 700px) {
        .container {
          padding: 18px 4vw;
        }
        header {
          flex-direction: column;
          gap: 18px;
          padding-bottom: 18px;
        }
        .info-list {
          flex-direction: column;
          gap: 12px;
        }
      }
      footer {
        text-align: center;
        padding: 22px 0 10px 0;
        color: #38bdf8;
        font-size: 15px;
        margin-top: 40px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- Header: Avatar, Name, Intro, Social -->
      <header>
        <img
          src="https://avatars.githubusercontent.com/u/151687803?v=4"
          alt="Avatar"
          class="avatar"
        />
        <div class="intro">
          <h1>Tran Van Thuan</h1>
          <h2>
            Software Engineering Student<br />FPT University Da Nang Campus
          </h2>
          <p>
            Outgoing, eager to learn, and passionate about technology.<br />
            Mentor in C, experienced in Java, fluent in English & Japanese.<br />
            GPA: <span class="highlight">3.5</span>
          </p>
          <div class="social">
            <a
              href="https://www.facebook.com/tran.van.thuan.499718"
              target="_blank"
              title="Facebook"
              ><i class="fab fa-facebook"></i
            ></a>
            <a href="mailto:Tranvanthuan2005tt@gmail.com" title="Gmail"
              ><i class="fas fa-envelope"></i
            ></a>
            <a
              href="https://github.com/Tranvanthuan1805"
              target="_blank"
              title="GitHub"
              ><i class="fab fa-github"></i
            ></a>
            <a href="https://zalo.me/0335111783" target="_blank" title="Zalo"
              ><i class="fas fa-phone"></i
            ></a>
          </div>
          <a href="mailto:Tranvanthuan2005tt@gmail.com" class="btn-main"
            ><i class="fas fa-chalkboard-teacher"></i>Hire me for Java/C
            tutoring</a
          >
        </div>
      </header>

      <!-- Quick Info -->
      <ul class="info-list">
        <li><i class="fas fa-language"></i> Fluent in English & Japanese</li>
        <li><i class="fas fa-user-tie"></i> Mentor in C, Java experience</li>
        <li>
          <i class="fas fa-graduation-cap"></i> GPA:
          <span class="highlight">3.5</span>
        </li>
        <li><i class="fas fa-users"></i> Member of F2K, ITSC clubs</li>
      </ul>

      <!-- Skills -->
      <div class="skills">
        <div class="skills-title">
          <i class="fas fa-code"></i> Programming Skills
        </div>
        <div class="skill-bar">
          <div class="skill-label">Java</div>
          <div class="bar-bg">
            <div class="bar-fill" style="width: 90%"></div>
          </div>
        </div>
        <div class="skill-bar">
          <div class="skill-label">C</div>
          <div class="bar-bg">
            <div class="bar-fill" style="width: 95%"></div>
          </div>
        </div>
        <div class="skill-bar">
          <div class="skill-label">Python</div>
          <div class="bar-bg">
            <div class="bar-fill" style="width: 75%"></div>
          </div>
        </div>
      </div>

      <!-- Projects -->
      <section class="projects">
        <h3 class="section-title">
          <i class="fas fa-laptop-code"></i> Projects
        </h3>
        <div class="project-card">
          <div class="project-title">F2GO.com.vn</div>
          <div class="project-desc">
            Developed an online learning platform for students to access
            high-quality programming courses with a friendly UI/UX.
          </div>
          <a href="https://F2GO.com.vn" class="btn-main" target="_blank"
            ><i class="fas fa-external-link-alt"></i> Visit Project</a
          >
        </div>
      </section>

      <!-- Experience & Activities -->
      <section class="experience">
        <h3 class="section-title">
          <i class="fas fa-briefcase"></i> Experience & Activities
        </h3>
        <ul class="exp-list">
          <li>Mentor for C programming at FPT University</li>
          <li>Active member of F2K and ITSC clubs</li>
          <li>Organizing committee - FUDA FEST 2024 at FPT University</li>
        </ul>
      </section>
    </div>
    <footer>&copy; 2025 Tran Van Thuan. All rights reserved.</footer>
  </body>
</html>
