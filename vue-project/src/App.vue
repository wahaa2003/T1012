<script setup></script>

<template>
  <div class="container">
    <header class="header">
      <h1 class="title">Chen</h1>
      <p class="subtitle">AI 協作網站開發課程練習作品</p>
    </header>

    <main class="main-content">
      <section class="card" id="about">
        <h2 class="card-title">自我介紹</h2>
        <p class="card-text">CYCU student</p>
      </section>

      <section class="card" id="interests">
        <h2 class="card-title">學習興趣</h2>
        <p class="card-text">none</p>
      </section>

      <section class="card" id="skills">
        <h2 class="card-title">目前正在學習的技能</h2>
        <p class="card-text">Website Architecture and Design</p>
      </section>

      <section class="card" id="projects">
        <h2 class="card-title">作品介紹</h2>
        <div class="projects-grid">
          <article class="project-card">
            <h3 class="project-title">VCC</h3>
            <p class="project-desc">虛擬電廠數位孿生系統</p>
          </article>
          <article class="project-card">
            <h3 class="project-title">HE</h3>
            <p class="project-desc">家用電器智慧控制系統</p>
          </article>
        </div>
      </section>
    </main>

    <footer class="footer">
      <p>&copy; Chen. All rights reserved.</p>
    </footer>
  </div>
</template>

<style>
/* ==========================================================================
   全域設定與變數 (Global Settings & Variables)
   ========================================================================== */
:root {
  --bg-color: #e2e8f0;
  --card-bg: #ffffff;
  --text-main: #0f172a;
  --text-muted: #475569;
  --primary-color: #2563eb;
  --primary-dark: #1e40af;
  --border-color: #cbd5e1;
  --shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.07), 0 4px 6px -4px rgba(0, 0, 0, 0.05);
  --radius: 12px;
  --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "PingFang TC", "Microsoft JhengHei", sans-serif;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-family);
  background: linear-gradient(180deg, #e2e8f0 0%, #cbd5e1 100%);
  background-attachment: fixed;
  color: var(--text-main);
  line-height: 1.7;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 48px 20px;
}

/* ==========================================================================
   容器與版面佈局 (Layout & Container)
   ========================================================================== */
.container {
  width: 100%;
  max-width: 820px;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

/* ==========================================================================
   頁首 (Header)
   ========================================================================== */
.header {
  background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary-color) 100%);
  color: #ffffff;
  padding: 40px 32px;
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  text-align: center;
}

.title {
  font-size: 2.25rem;
  font-weight: 700;
  color: #ffffff;
  letter-spacing: -0.025em;
  margin-bottom: 10px;
}

.subtitle {
  font-size: 1.05rem;
  color: #dbeafe;
}

/* ==========================================================================
   主要內容區塊 (Main Content & Cards)
   ========================================================================== */
.main-content {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card {
  background-color: var(--card-bg);
  padding: 26px 32px;
  border-radius: var(--radius);
  border: 1px solid var(--border-color);
  border-left: 6px solid var(--primary-color);
  box-shadow: var(--shadow);
}

.card-title {
  font-size: 1.15rem;
  font-weight: 600;
  color: var(--primary-dark);
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.card-title::before {
  content: "";
  display: inline-block;
  width: 4px;
  height: 1.1rem;
  background-color: var(--primary-color);
  border-radius: 2px;
}

.card-text {
  font-size: 1.05rem;
  color: var(--text-main);
  word-break: break-word;
}

/* ==========================================================================
   作品介紹區塊 (Projects Grid & Cards)
   ========================================================================== */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
  margin-top: 14px;
}

.project-card {
  background-color: #f8fafc;
  border: 1px solid var(--border-color);
  border-radius: 8px;
  padding: 18px 20px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.project-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px -2px rgba(0, 0, 0, 0.06);
}

.project-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--primary-dark);
  margin-bottom: 6px;
}

.project-desc {
  font-size: 0.95rem;
  color: var(--text-main);
  line-height: 1.5;
  word-break: break-word;
}

/* ==========================================================================
   頁尾 (Footer)
   ========================================================================== */
.footer {
  text-align: center;
  padding: 16px;
  font-size: 0.9rem;
  color: var(--text-muted);
}

/* ==========================================================================
   響應式設計 (Responsive Design - Mobile Friendly)
   ========================================================================== */
@media (max-width: 600px) {
  body {
    padding: 20px 14px;
  }

  .container {
    gap: 16px;
  }

  .header {
    padding: 28px 20px;
  }

  .title {
    font-size: 1.85rem;
  }

  .subtitle {
    font-size: 0.95rem;
  }

  .card {
    padding: 20px 18px;
    border-left-width: 4px;
  }

  .card-title {
    font-size: 1.05rem;
  }

  .card-text {
    font-size: 1rem;
  }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: 12px;
  }

  .project-card {
    padding: 16px 18px;
  }

  .project-title {
    font-size: 1.05rem;
  }

  .project-desc {
    font-size: 0.9rem;
  }
}
</style>

