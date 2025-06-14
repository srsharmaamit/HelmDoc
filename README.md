<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Docs - Airflow Style (Grid)</title>
  <style>
    :root {
      --header-height: 60px;
      --sidebar-width: 260px;
      --toc-width: 220px;
      --content-max-width: 900px;
      --primary-color: #017CEE;
      --bg-color: #f8f9fb;
      --font-color: #333;
      --font-family: "Segoe UI", Tahoma, sans-serif;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: var(--font-family);
      color: var(--font-color);
      background-color: var(--bg-color);
    }

    /* Header */
    header {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: var(--header-height);
      background-color: #fff;
      border-bottom: 1px solid #ddd;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 20px;
      z-index: 1000;
    }

    header .logo {
      font-weight: bold;
      font-size: 1.4rem;
      color: var(--primary-color);
    }

    header nav a {
      margin-left: 20px;
      text-decoration: none;
      color: var(--font-color);
      font-weight: 500;
    }

    /* Grid Layout */
    .main-grid {
      display: grid;
      grid-template-columns: var(--sidebar-width) 1fr var(--toc-width);
      grid-template-rows: 1fr;
      margin-top: var(--header-height);
      min-height: calc(100vh - var(--header-height));
    }

    .sidebar {
      background: #fff;
      border-right: 1px solid #ddd;
      padding: 20px;
      position: sticky;
      top: var(--header-height);
      height: calc(100vh - var(--header-height));
      overflow-y: auto;
    }

    .content {
      background: #fff;
      padding: 40px;
      max-width: var(--content-max-width);
      margin: 0 auto;
    }

    .toc {
      background: #fff;
      border-left: 1px solid #ddd;
      padding: 20px;
      position: sticky;
      top: var(--header-height);
      height: calc(100vh - var(--header-height));
      overflow-y: auto;
    }

    .sidebar ul, .toc ul {
      list-style: none;
    }

    .sidebar a, .toc a {
      display: block;
      text-decoration: none;
      color: var(--font-color);
      margin-bottom: 12px;
      font-weight: 500;
    }

    .sidebar a:hover, .toc a:hover {
      color: var(--primary-color);
    }

    h1 {
      margin-bottom: 20px;
    }

    p {
      margin-bottom: 16px;
      line-height: 1.6;
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">MyDocs</div>
    <nav>
      <a href="#">Docs</a>
      <a href="#">API</a>
      <a href="#">Community</a>
      <a href="#">GitHub</a>
    </nav>
  </header>

  <div class="main-grid">
    <!-- Left Sidebar -->
    <aside class="sidebar">
      <h3>Navigation</h3>
      <ul>
        <li><a href="#">Introduction</a></li>
        <li><a href="#">Installation</a></li>
        <li><a href="#">Quick Start</a></li>
        <li><a href="#">Configuration</a></li>
        <li><a href="#">API Reference</a></li>
        <li><a href="#">FAQ</a></li>
      </ul>
    </aside>

    <!-- Main Content -->
    <main class="content">
      <h1>Welcome to MyDocs</h1>
      <p>This documentation layout is fully built with CSS Grid, closely following Airflow’s official docs design.</p>
      <p>You can easily extend this for your repo, add Markdown renderers, etc.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sed laoreet nunc, sed dapibus turpis. Duis vitae justo a urna sollicitudin laoreet. Sed cursus libero sed posuere bibendum.</p>
    </main>

    <!-- Right Sidebar (TOC) -->
    <aside class="toc">
      <h3>On this page</h3>
      <ul>
        <li><a href="#">Section 1</a></li>
        <li><a href="#">Section 2</a></li>
        <li><a href="#">Section 3</a></li>
        <li><a href="#">Section 4</a></li>
      </ul>
    </aside>
  </div>

</body>
</html>
