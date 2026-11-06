HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DevScale — Responsive Landing Page</title>
    <meta name="description" content="A fully responsive modern landing page built using CSS Grid, Flexbox, and semantic HTML5.">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- 3 & 4. Semantic Header & Navigation -->
    <header class="site-header">
        <div class="nav-container">
            <div class="logo">
                <a href="#">DevScale</a>
            </div>
            <nav class="nav-menu">
                <ul class="nav-links">
                    <li><a href="#hero" class="active">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#showcase">Showcase</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="header-action">
                <a href="#contact" class="btn btn-primary">Get Started</a>
            </div>
        </div>
    </header>

    <!-- Main Content Area -->
    <main class="site-main">
        <!-- 4. Hero Section -->
        <section id="hero" class="hero-section">
            <div class="hero-container">
                <div class="hero-text">
                    <span class="badge">Reference Architecture</span>
                    <h1>Build Enterprise-Ready Web Applications</h1>
                    <p>Leverage modular design systems, advanced CSS layout engines, and semantic markup to deliver exceptional digital experiences.</p>
                    <div class="hero-buttons">
                        <a href="#features" class="btn btn-primary btn-lg">Explore Features</a>
                        <a href="https://github.com/AtimAkhtar" target="_blank" rel="noopener" class="btn btn-outline btn-lg">View GitHub</a>
                    </div>
                </div>
                <div class="hero-image-wrapper">
                    <img src="images/hero-illustration.jpg" alt="Developer illustration showcasing responsive web layout design" class="hero-img">
                </div>
            </div>
        </section>

        <!-- 4. Feature Cards Section -->
        <section id="features" class="features-section">
            <div class="section-header">
                <h2>Core Platform Capabilities</h2>
                <p>Engineered for high performance, maintainability, and seamless scalability.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="card-icon">⚡</div>
                    <h3>CSS Grid Architecture</h3>
                    <p>Construct complex two-dimensional macro layouts with precise column tracks, auto-fit flows, and named grid areas.</p>
                </div>
                <div class="feature-card">
                    <div class="card-icon">🎯</div>
                    <h3>Flexbox Micro Alignment</h3>
                    <p>Manage flexible component alignments, navigation bars, and responsive wrapping with robust one-dimensional controls.</p>
                </div>
                <div class="feature-card">
                    <div class="card-icon">📱</div>
                    <h3>Mobile-First Scaling</h3>
                    <p>Ensure fluid adaptability across mobile devices, tablets, and ultra-wide desktop displays using progressive breakpoints.</p>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer Section -->
    <footer id="contact" class="site-footer">
        <div class="footer-container">
            <div class="footer-info">
                <h3>DevScale</h3>
                <p>Department of Computer Science Engineering, Invertis University, Bareilly</p>
            </div>
            <ul class="footer-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="https://github.com/AtimAkhtar" target="_blank" rel="noopener">GitHub Repository</a></li>
            </ul>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Atim Akhtar. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
CSS
/* style.css */
:root {
    --primary-color: #0284c7;
    --primary-hover: #0369a1;
    --secondary-color: #0f172a;
    --bg-color: #f8fafc;
    --surface-color: #ffffff;
    --text-color: #334155;
    --text-muted: #64748b;
    --border-color: #e2e8f0;
    
    --space-sm: 8px;
    --space-md: 16px;
    --space-lg: 24px;
    --space-xl: 40px;
    
    --radius-md: 8px;
    --radius-lg: 12px;
    --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    --shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

/* Header & Navigation (Flexbox) */
.site-header {
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: var(--space-md) var(--space-xl);
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-md);
}

.logo a {
    font-size: 1.25rem;
    font-weight: bold;
    color: var(--surface-color);
    text-decoration: none;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: var(--space-lg);
}

.nav-links a {
    color: #94a3b8;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

.nav-links a:hover,
.nav-links a.active {
    color: #38bdf8;
}

.header-action {
    display: flex;
    align-items: center;
}

/* Main Content Area */
.site-main {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    gap: 5rem;
    padding: 3rem 0;
}

/* Hero Section (Flexbox) */
.hero-section {
    padding: 0 var(--space-xl);
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3rem;
    flex-wrap: wrap;
}

.hero-text {
    flex: 1 1 340px;
    max-width: 560px;
}

.badge {
    display: inline-block;
    background-color: #e0f2fe;
    color: var(--primary-color);
    font-size: 0.75rem;
    font-weight: bold;
    padding: 4px 12px;
    border-radius: 20px;
    text-transform: uppercase;
    margin-bottom: var(--space-md);
}

.hero-text h1 {
    font-size: clamp(2.25rem, 4vw, 3rem);
    color: var(--secondary-color);
    line-height: 1.2;
    margin-bottom: var(--space-md);
}

.hero-text p {
    font-size: 1.125rem;
    color: var(--text-muted);
    margin-bottom: var(--space-lg);
}

.hero-buttons {
    display: flex;
    gap: var(--space-md);
    flex-wrap: wrap;
}

.hero-image-wrapper {
    flex: 1 1 340px;
    max-width: 520px;
    background-color: var(--border-color);
    border-radius: var(--radius-lg);
    overflow: hidden;
    box-shadow: var(--shadow-md);
}

.hero-img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
}

/* Features Section (CSS Grid) */
.features-section {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 var(--space-xl);
    width: 100%;
}

.section-header {
    text-align: center;
    margin-bottom: 3rem;
}

.section-header h2 {
    font-size: 2rem;
    color: var(--secondary-color);
    margin-bottom: 0.5rem;
}

.section-header p {
    color: var(--text-muted);
    font-size: 1.1rem;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--space-xl);
}

.feature-card {
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    border-radius: var(--radius-lg);
    padding: 2.5rem 2rem;
    box-shadow: var(--shadow-sm);
    display: flex;
    flex-direction: column;
    gap: var(--space-md);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-md);
}

.card-icon {
    font-size: 2.5rem;
    background-color: #f1f5f9;
    width: 60px;
    height: 60px;
    border-radius: var(--radius-md);
    display: flex;
    justify-content: center;
    align-items: center;
}

.feature-card h3 {
    font-size: 1.25rem;
    color: var(--secondary-color);
}

.feature-card p {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* Footer Section */
.site-footer {
    background-color: var(--secondary-color);
    color: var(--surface-color);
    padding: 3rem var(--space-xl) 1.5rem var(--space-xl);
    margin-top: auto;
    border-top: 1px solid var(--border-color);
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: var(--space-lg);
    padding-bottom: 2rem;
    border-bottom: 1px solid #1e293b;
}

.footer-info h3 {
    font-size: 1.25rem;
    margin-bottom: 4px;
}

.footer-info p {
    color: var(--text-muted);
    font-size: 0.875rem;
}

.footer-links {
    list-style: none;
    display: flex;
    gap: var(--space-lg);
}

.footer-links a {
    color: var(--text-muted);
    text-decoration: none;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

.footer-links a:hover {
    color: var(--surface-color);
}

.footer-bottom {
    max-width: 1200px;
    margin: 1.5rem auto 0 auto;
    text-align: center;
    color: var(--text-muted);
    font-size: 0.875rem;
}

/* Buttons */
.btn {
    padding: 0.6rem 1.25rem;
    font-size: 0.95rem;
    font-weight: bold;
    border-radius: var(--radius-md);
    text-decoration: none;
    cursor: pointer;
    transition: background-color 0.2s ease;
    display: inline-block;
    text-align: center;
    border: none;
}

.btn-primary {
    background-color: var(--primary-color);
    color: var(--surface-color);
}

.btn-primary:hover {
    background-color: var(--primary-hover);
}

.btn-outline {
    background-color: transparent;
    border: 1px solid var(--border-color);
    color: var(--secondary-color);
}

.btn-outline:hover {
    background-color: #f1f5f9;
    border-color: var(--text-muted);
}

.btn-lg {
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
}