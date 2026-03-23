<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>HotVibe — Premium Content Marketplace</title>
  <meta name="description" content="HotVibe is a premium digital content marketplace where creators showcase and sell exclusive content packs." />
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <!-- Loading Screen -->
  <div id="loader" class="loader" aria-hidden="true">
    <div class="loader__ring"></div>
    <p>Loading HotVibe...</p>
  </div>

  <!-- Scroll Progress Bar -->
  <div id="progressBar" class="progress-bar" aria-hidden="true"></div>

  <!-- Toasts / Notifications -->
  <div id="toastContainer" class="toast-container" aria-live="polite" aria-atomic="true"></div>

  <!-- Back to Top -->
  <button id="backToTop" class="back-to-top" aria-label="Back to top">↑</button>

  <!-- Header / Navigation -->
  <header id="navbar" class="navbar">
    <div class="container nav-inner">
      <a href="#home" class="logo" aria-label="HotVibe Home">
        <span class="logo-mark">●</span> HotVibe
      </a>

      <nav class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#explore">Explore</a>
        <a href="#pricing">Pricing</a>
        <a href="#auth">Login</a>
        <a href="#auth" class="nav-cta" id="openSignup">Sign Up</a>
      </nav>

      <div class="nav-actions">
        <button id="themeToggle" class="icon-btn" aria-label="Toggle theme">
          ☾
        </button>
        <button id="mobileToggle" class="icon-btn mobile-toggle" aria-label="Open menu">
          ☰
        </button>
      </div>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section id="home" class="hero section">
      <div class="hero-bg"></div>
      <div class="container hero-grid">
        <div class="hero-copy reveal">
          <span class="eyebrow">Premium digital content marketplace</span>
          <h1>Unlock Exclusive Content</h1>
          <p class="hero-text">
            Discover elegant creator packs, premium drops, and exclusive digital experiences inside one modern, high-end platform.
          </p>

          <div class="hero-actions">
            <a href="#explore" class="btn btn-primary">Explore Packs</a>
            <button class="btn btn-secondary" id="joinNowBtn">Join Now</button>
          </div>

          <div class="hero-stats">
            <div class="stat-card">
              <strong class="counter" data-target="250">0</strong>
              <span>Creators</span>
            </div>
            <div class="stat-card">
              <strong class="counter" data-target="12000">0</strong>
              <span>Downloads</span>
            </div>
            <div class="stat-card">
              <strong class="counter" data-target="98">0</strong>
              <span>Satisfaction %</span>
            </div>
          </div>
        </div>

        <div class="hero-showcase reveal">
          <div class="glass-panel featured-preview">
            <div class="preview-top">
              <span class="live-dot"></span>
              Live marketplace activity
            </div>
            <div class="preview-stack" id="heroPreview"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Featured Content -->
    <section class="section">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">Featured content</span>
          <h2>Hand-picked premium packs</h2>
          <p>Top-performing creator packs with polished presentation and strong buyer appeal.</p>
        </div>

        <div id="featuredGrid" class="card-grid featured-grid"></div>
      </div>
    </section>

    <!-- Explore / Gallery -->
    <section id="explore" class="section section-alt">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">Explore</span>
          <h2>Browse the gallery system</h2>
          <p>Search, filter, and preview content packs instantly with a responsive marketplace layout.</p>
        </div>

        <div class="explore-toolbar reveal">
          <div class="search-wrap">
            <span class="input-icon">⌕</span>
            <input id="searchInput" type="search" placeholder="Search packs..." aria-label="Search packs" />
          </div>

          <div class="filter-row" id="categoryFilters"></div>

          <div class="select-wrap">
            <label for="priceFilter">Price</label>
            <select id="priceFilter" aria-label="Filter by price">
              <option value="all">All</option>
              <option value="under20">Under $20</option>
              <option value="20to40">$20 - $40</option>
              <option value="40plus">$40+</option>
            </select>
          </div>
        </div>

        <div id="exploreGrid" class="card-grid explore-grid"></div>
      </div>
    </section>

    <!-- Pricing -->
    <section id="pricing" class="section">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">Pricing</span>
          <h2>Simple plans for every creator</h2>
          <p>Clear tiers designed to convert with a premium, luxury-first presentation.</p>
        </div>

        <div class="pricing-grid reveal">
          <article class="pricing-card">
            <h3>Basic</h3>
            <div class="price">$9<span>/month</span></div>
            <ul>
              <li>1 content pack listing</li>
              <li>Standard analytics</li>
              <li>Email support</li>
            </ul>
            <button class="btn btn-secondary">Choose Basic</button>
          </article>

          <article class="pricing-card popular">
            <div class="popular-badge">Most Popular</div>
            <h3>Premium</h3>
            <div class="price">$29<span>/month</span></div>
            <ul>
              <li>10 content pack listings</li>
              <li>Advanced analytics</li>
              <li>Priority support</li>
              <li>Featured placement</li>
            </ul>
            <button class="btn btn-primary">Choose Premium</button>
          </article>

          <article class="pricing-card">
            <h3>VIP</h3>
            <div class="price">$79<span>/month</span></div>
            <ul>
              <li>Unlimited listings</li>
              <li>Full analytics suite</li>
              <li>Dedicated manager</li>
              <li>VIP homepage exposure</li>
            </ul>
            <button class="btn btn-secondary">Choose VIP</button>
          </article>
        </div>
      </div>
    </section>

    <!-- Auth -->
    <section id="auth" class="section section-alt">
      <div class="container auth-layout">
        <div class="auth-copy reveal">
          <span class="eyebrow">Authentication</span>
          <h2>Create or access your account</h2>
          <p>Clean sign in and sign up flows with validation, icons, and smooth tab switching.</p>
        </div>

        <div class="auth-card reveal">
          <div class="auth-tabs">
            <button class="tab-btn active" data-tab="login">Login</button>
            <button class="tab-btn" data-tab="signup">Sign Up</button>
          </div>

          <form id="loginForm" class="auth-form active" novalidate>
            <div class="field">
              <label>Email</label>
              <div class="input-shell">
                <span class="field-icon">✉</span>
                <input type="email" name="email" placeholder="you@example.com" />
              </div>
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Password</label>
              <div class="input-shell">
                <span class="field-icon">🔒</span>
                <input type="password" name="password" placeholder="Your password" />
              </div>
              <small class="error-msg"></small>
            </div>

            <label class="check-row">
              <input type="checkbox" name="remember" />
              <span>Remember me</span>
            </label>

            <button type="submit" class="btn btn-primary btn-full">Login</button>
          </form>

          <form id="signupForm" class="auth-form" novalidate>
            <div class="field">
              <label>Username</label>
              <div class="input-shell">
                <span class="field-icon">⌂</span>
                <input type="text" name="username" placeholder="Your username" />
              </div>
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Email</label>
              <div class="input-shell">
                <span class="field-icon">✉</span>
                <input type="email" name="email" placeholder="you@example.com" />
              </div>
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Password</label>
              <div class="input-shell">
                <span class="field-icon">🔒</span>
                <input type="password" name="password" placeholder="Create password" />
              </div>
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Confirm Password</label>
              <div class="input-shell">
                <span class="field-icon">🔒</span>
                <input type="password" name="confirmPassword" placeholder="Confirm password" />
              </div>
              <small class="error-msg"></small>
            </div>

            <button type="submit" class="btn btn-primary btn-full">Create Account</button>
          </form>
        </div>
      </div>
    </section>

    <!-- Checkout -->
    <section id="checkout" class="section">
      <div class="container checkout-grid">
        <div class="checkout-copy reveal">
          <span class="eyebrow">Checkout</span>
          <h2>Simulated payment UI</h2>
          <p>Validated payment form with card and PayPal-style options, built for a realistic front-end demo.</p>

          <div class="checkout-summary glass-panel">
            <h3>Selected item</h3>
            <p id="selectedPackTitle">No pack selected yet.</p>
            <strong id="selectedPackPrice">$0.00</strong>
          </div>
        </div>

        <div class="checkout-card reveal">
          <form id="paymentForm" novalidate>
            <div class="payment-methods">
              <label class="payment-option">
                <input type="radio" name="method" value="card" checked />
                <span>Card</span>
              </label>
              <label class="payment-option">
                <input type="radio" name="method" value="paypal" />
                <span>PayPal</span>
              </label>
            </div>

            <div class="field">
              <label>Name</label>
              <input type="text" name="name" placeholder="Full name" />
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Email</label>
              <input type="email" name="email" placeholder="you@example.com" />
              <small class="error-msg"></small>
            </div>

            <div class="field">
              <label>Card Number</label>
              <input type="text" name="cardNumber" placeholder="1234 5678 9012 3456" inputmode="numeric" />
              <small class="error-msg"></small>
            </div>

            <div class="inline-fields">
              <div class="field">
                <label>Expiry</label>
                <input type="text" name="expiry" placeholder="MM/YY" />
                <small class="error-msg"></small>
              </div>

              <div class="field">
                <label>CVV</label>
                <input type="text" name="cvv" placeholder="123" inputmode="numeric" />
                <small class="error-msg"></small>
              </div>
            </div>

            <button type="submit" class="btn btn-primary btn-full">Pay Now</button>
            <div id="paymentSuccess" class="payment-success" hidden>
              Payment successful. Your access is ready.
            </div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <!-- Product Modal -->
  <div id="productModal" class="modal" aria-hidden="true" role="dialog" aria-modal="true">
    <div class="modal-backdrop" data-close="true"></div>
    <div class="modal-panel glass-panel">
      <button class="modal-close" id="closeModal" aria-label="Close modal">×</button>
      <div class="modal-grid">
        <div class="modal-image-wrap">
          <img id="modalImage" src="" alt="Product preview" />
        </div>
        <div class="modal-content">
          <div class="modal-header">
            <span id="modalCategory" class="pill"></span>
            <button id="favoriteBtn" class="favorite-btn" aria-label="Favorite">♡</button>
          </div>
          <h3 id="modalTitle"></h3>
          <p id="modalDescription"></p>
          <div class="modal-price" id="modalPrice"></div>
          <div class="modal-actions">
            <button id="purchaseBtn" class="btn btn-primary">Purchase</button>
            <button id="modalSecondaryBtn" class="btn btn-secondary">Save for later</button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="footer">
    <div class="container footer-grid">
      <div>
        <a href="#home" class="logo footer-logo"><span class="logo-mark">●</span> HotVibe</a>
        <p>Premium marketplace UI for exclusive digital content packs.</p>
      </div>

      <div class="footer-links">
        <a href="#home">About</a>
        <a href="#home">Privacy</a>
        <a href="#home">Terms</a>
      </div>

      <div class="footer-social">
        <a href="#" aria-label="Instagram">IG</a>
        <a href="#" aria-label="X">X</a>
        <a href="#" aria-label="TikTok">TT</a>
      </div>
    </div>

    <div class="container footer-bottom">
      <p>© 2026 HotVibe. All rights reserved.</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
/* ================================
   HotVibe — Premium Marketplace UI
   ================================ */

:root {
  --bg: #0a0a0a;
  --bg-2: #111111;
  --surface: rgba(255, 255, 255, 0.06);
  --surface-2: rgba(255, 255, 255, 0.09);
  --text: #f5f5f7;
  --muted: rgba(245, 245, 247, 0.72);
  --border: rgba(255, 255, 255, 0.12);
  --shadow: 0 18px 50px rgba(0, 0, 0, 0.45);

  --purple: #b84cff;
  --pink: #ff4fd8;
  --blue: #4cc9ff;
  --green: #37e6a6;

  --radius-sm: 12px;
  --radius-md: 16px;
  --radius-lg: 20px;

  --container: 1180px;
  --transition: 220ms ease;
}

[data-theme="light"] {
  --bg: #f6f7fb;
  --bg-2: #ffffff;
  --surface: rgba(10, 10, 10, 0.04);
  --surface-2: rgba(10, 10, 10, 0.07);
  --text: #101114;
  --muted: rgba(16, 17, 20, 0.72);
  --border: rgba(10, 10, 10, 0.1);
  --shadow: 0 18px 50px rgba(12, 14, 28, 0.08);
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: Inter, Poppins, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  background:
    radial-gradient(circle at top left, rgba(184, 76, 255, 0.12), transparent 28%),
    radial-gradient(circle at top right, rgba(76, 201, 255, 0.09), transparent 24%),
    linear-gradient(180deg, var(--bg), var(--bg-2));
  color: var(--text);
  min-height: 100vh;
  overflow-x: hidden;
}

img {
  max-width: 100%;
  display: block;
}

a {
  color: inherit;
  text-decoration: none;
}

button,
input,
select {
  font: inherit;
}

.container {
  width: min(100% - 32px, var(--container));
  margin: 0 auto;
}

.section {
  padding: 92px 0;
  position: relative;
}

.section-alt {
  background: linear-gradient(180deg, transparent, rgba(255,255,255,0.02), transparent);
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  font-size: 0.75rem;
  color: var(--muted);
  margin-bottom: 14px;
}

.section-head {
  max-width: 680px;
  margin-bottom: 28px;
}

.section-head h2,
.hero-copy h1,
.auth-copy h2,
.checkout-copy h2 {
  line-height: 1.05;
  letter-spacing: -0.04em;
  margin: 0;
}

.section-head h2 {
  font-size: clamp(2rem, 5vw, 3.5rem);
}

.section-head p,
.hero-text,
.auth-copy p,
.checkout-copy p,
.footer p {
  color: var(--muted);
  line-height: 1.7;
}

/* Loader */
.loader {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: grid;
  place-items: center;
  gap: 16px;
  background: rgba(10, 10, 10, 0.96);
  transition: opacity 300ms ease, visibility 300ms ease;
}

.loader.hidden {
  opacity: 0;
  visibility: hidden;
  pointer-events: none;
}

.loader__ring {
  width: 54px;
  height: 54px;
  border-radius: 50%;
  border: 3px solid rgba(255,255,255,0.12);
  border-top-color: var(--purple);
  border-right-color: var(--pink);
  animation: spin 0.9s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.progress-bar {
  position: fixed;
  top: 0;
  left: 0;
  height: 3px;
  width: 0%;
  z-index: 1200;
  background: linear-gradient(90deg, var(--purple), var(--pink), var(--blue));
  box-shadow: 0 0 20px rgba(184, 76, 255, 0.35);
}

/* Navbar */
.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
  padding: 14px 0;
  transition: background 220ms ease, backdrop-filter 220ms ease, border-color 220ms ease;
  background: transparent;
  border-bottom: 1px solid transparent;
}

.navbar.scrolled {
  background: rgba(10, 10, 10, 0.78);
  backdrop-filter: blur(16px);
  border-bottom-color: var(--border);
}

[data-theme="light"] .navbar.scrolled {
  background: rgba(246, 247, 251, 0.82);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
}

.logo {
  font-weight: 800;
  letter-spacing: -0.04em;
  font-size: 1.15rem;
  display: inline-flex;
  align-items: center;
  gap: 8px;
}

.logo-mark {
  color: var(--pink);
  text-shadow: 0 0 18px rgba(255, 79, 216, 0.65);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 22px;
}

.nav-links a {
  color: var(--muted);
  transition: color var(--transition), transform var(--transition);
}

.nav-links a:hover {
  color: var(--text);
}

.nav-cta {
  padding: 10px 16px;
  background: linear-gradient(135deg, rgba(184, 76, 255, 0.2), rgba(76, 201, 255, 0.14));
  border: 1px solid var(--border);
  border-radius: 999px;
  color: var(--text) !important;
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 10px;
}

.icon-btn {
  width: 42px;
  height: 42px;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: var(--surface);
  color: var(--text);
  display: grid;
  place-items: center;
  cursor: pointer;
  transition: transform var(--transition), box-shadow var(--transition), background var(--transition);
}

.icon-btn:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow);
  background: var(--surface-2);
}

.mobile-toggle {
  display: none;
}

/* Hero */
.hero {
  min-height: 100vh;
  display: grid;
  align-items: center;
  padding-top: 40px;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(circle at 20% 20%, rgba(184, 76, 255, 0.18), transparent 20%),
    radial-gradient(circle at 80% 10%, rgba(76, 201, 255, 0.16), transparent 18%),
    radial-gradient(circle at 70% 75%, rgba(255, 79, 216, 0.1), transparent 20%);
  filter: blur(4px);
  animation: floatBg 12s ease-in-out infinite alternate;
  pointer-events: none;
}

@keyframes floatBg {
  from { transform: translateY(0px) scale(1); }
  to { transform: translateY(18px) scale(1.02); }
}

.hero-grid {
  position: relative;
  z-index: 1;
  display: grid;
  grid-template-columns: 1.15fr 0.85fr;
  gap: 34px;
  align-items: center;
}

.hero-copy h1 {
  font-size: clamp(3rem, 8vw, 6rem);
  margin-bottom: 18px;
}

.hero-text {
  max-width: 600px;
  margin-bottom: 26px;
  font-size: 1.05rem;
}

.hero-actions {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  margin-bottom: 34px;
}

.btn {
  border: 0;
  outline: 0;
  border-radius: 999px;
  padding: 13px 20px;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  font-weight: 700;
  transition: transform var(--transition), box-shadow var(--transition), opacity var(--transition), background var(--transition);
}

.btn:hover {
  transform: translateY(-2px);
}

.btn-primary {
  color: #fff;
  background: linear-gradient(135deg, var(--purple), var(--pink));
  box-shadow: 0 12px 30px rgba(184, 76, 255, 0.25);
}

.btn-secondary {
  color: var(--text);
  background: var(--surface);
  border: 1px solid var(--border);
}

.btn-full {
  width: 100%;
}

.hero-stats {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

.stat-card {
  min-width: 132px;
  padding: 18px 20px;
  border-radius: var(--radius-md);
  background: var(--surface);
  border: 1px solid var(--border);
  backdrop-filter: blur(14px);
}

.stat-card strong {
  font-size: 1.6rem;
  display: block;
  margin-bottom: 6px;
}

.stat-card span {
  color: var(--muted);
  font-size: 0.92rem;
}

.glass-panel {
  background: var(--surface);
  border: 1px solid var(--border);
  backdrop-filter: blur(18px);
  box-shadow: var(--shadow);
  border-radius: var(--radius-lg);
}

.featured-preview {
  padding: 18px;
}

.preview-top {
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--muted);
  margin-bottom: 16px;
  font-size: 0.95rem;
}

.live-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: var(--green);
  box-shadow: 0 0 12px rgba(55, 230, 166, 0.8);
}

.preview-stack {
  display: grid;
  gap: 12px;
}

.preview-item {
  display: grid;
  grid-template-columns: 78px 1fr auto;
  gap: 14px;
  align-items: center;
  padding: 14px;
  border-radius: var(--radius-md);
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
}

.preview-item img {
  width: 78px;
  height: 78px;
  border-radius: 14px;
  object-fit: cover;
}

.preview-item strong {
  display: block;
  margin-bottom: 5px;
}

.preview-item span {
  color: var(--muted);
  font-size: 0.88rem;
}

.preview-price {
  color: var(--pink);
  font-weight: 800;
}

/* Grids */
.card-grid {
  display: grid;
  gap: 16px;
}

.featured-grid,
.explore-grid {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.content-card {
  position: relative;
  overflow: hidden;
  border-radius: var(--radius-lg);
  background: var(--surface);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  transition: transform var(--transition), box-shadow var(--transition), border-color var(--transition);
}

.content-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 24px 64px rgba(0, 0, 0, 0.42);
  border-color: rgba(184, 76, 255, 0.35);
}

.content-thumb {
  position: relative;
  aspect-ratio: 4 / 5;
  overflow: hidden;
}

.content-thumb img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 360ms ease;
}

.content-card:hover .content-thumb img {
  transform: scale(1.07);
}

.content-overlay {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: end;
  justify-content: space-between;
  padding: 14px;
  background: linear-gradient(180deg, transparent 40%, rgba(0,0,0,0.66));
  opacity: 0;
  transition: opacity var(--transition);
}

.content-card:hover .content-overlay {
  opacity: 1;
}

.quick-view {
  padding: 10px 14px;
  border-radius: 999px;
  border: 0;
  background: rgba(255,255,255,0.16);
  color: #fff;
  cursor: pointer;
  backdrop-filter: blur(10px);
}

.card-body {
  padding: 14px;
}

.card-body h3 {
  margin: 0 0 8px;
  font-size: 1rem;
}

.card-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.card-price {
  font-weight: 800;
  color: var(--pink);
}

.card-sub {
  color: var(--muted);
  font-size: 0.9rem;
  margin: 0 0 14px;
}

/* Explore Toolbar */
.explore-toolbar {
  display: grid;
  grid-template-columns: 1.2fr 1.2fr auto;
  gap: 14px;
  align-items: center;
  margin-bottom: 22px;
}

.search-wrap,
.select-wrap {
  display: flex;
  align-items: center;
  gap: 10px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 10px 14px;
}

.search-wrap input,
.select-wrap select {
  width: 100%;
  border: 0;
  outline: 0;
  color: var(--text);
  background: transparent;
}

.select-wrap label {
  color: var(--muted);
  font-size: 0.92rem;
}

.input-icon {
  color: var(--muted);
}

.filter-row {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.filter-btn {
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
  padding: 10px 14px;
  border-radius: 999px;
  cursor: pointer;
  transition: transform var(--transition), background var(--transition), border-color var(--transition);
}

.filter-btn.active,
.filter-btn:hover {
  background: linear-gradient(135deg, rgba(184, 76, 255, 0.2), rgba(76, 201, 255, 0.12));
  border-color: rgba(184, 76, 255, 0.3);
  transform: translateY(-1px);
}

/* Pricing */
.pricing-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.pricing-card {
  padding: 28px;
  border-radius: var(--radius-lg);
  background: var(--surface);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  position: relative;
}

.pricing-card h3 {
  margin: 0 0 14px;
  font-size: 1.3rem;
}

.price {
  font-size: 2.5rem;
  font-weight: 900;
  margin-bottom: 18px;
}

.price span {
  font-size: 1rem;
  color: var(--muted);
  font-weight: 600;
}

.pricing-card ul {
  padding-left: 18px;
  color: var(--muted);
  line-height: 1.8;
  margin-bottom: 22px;
}

.popular {
  border-color: rgba(184, 76, 255, 0.32);
  transform: translateY(-8px);
}

.popular-badge {
  position: absolute;
  top: 18px;
  right: 18px;
  padding: 8px 12px;
  border-radius: 999px;
  background: linear-gradient(135deg, var(--purple), var(--pink));
  color: #fff;
  font-size: 0.75rem;
  font-weight: 800;
}

/* Auth */
.auth-layout {
  display: grid;
  grid-template-columns: 0.95fr 1.05fr;
  gap: 24px;
  align-items: start;
}

.auth-card,
.checkout-card {
  padding: 24px;
  border-radius: var(--radius-lg);
  background: var(--surface);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
}

.auth-tabs {
  display: flex;
  gap: 10px;
  margin-bottom: 18px;
}

.tab-btn {
  flex: 1;
  border-radius: 999px;
  padding: 12px 14px;
  border: 1px solid var(--border);
  background: transparent;
  color: var(--muted);
  cursor: pointer;
  transition: background var(--transition), color var(--transition), transform var(--transition);
}

.tab-btn.active {
  color: var(--text);
  background: linear-gradient(135deg, rgba(184, 76, 255, 0.2), rgba(76, 201, 255, 0.12));
  transform: translateY(-1px);
}

.auth-form {
  display: none;
}

.auth-form.active {
  display: block;
}

.field {
  margin-bottom: 16px;
}

.field label {
  display: block;
  margin-bottom: 8px;
  color: var(--muted);
  font-size: 0.95rem;
}

.input-shell {
  display: flex;
  align-items: center;
  gap: 10px;
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 12px 14px;
  transition: border-color var(--transition), box-shadow var(--transition);
}

.input-shell:focus-within,
.field input:focus,
.select-wrap select:focus,
.search-wrap input:focus {
  border-color: rgba(184, 76, 255, 0.45);
  box-shadow: 0 0 0 4px rgba(184, 76, 255, 0.08);
}

.field input {
  width: 100%;
  border: 0;
  outline: 0;
  background: transparent;
  color: var(--text);
}

.field-icon {
  color: var(--muted);
}

.check-row {
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--muted);
  margin-bottom: 18px;
}

.error-msg {
  display: block;
  min-height: 18px;
  margin-top: 6px;
  color: #ff7979;
  font-size: 0.84rem;
}

.auth-form .btn-full {
  margin-top: 8px;
}

/* Checkout */
.checkout-grid {
  display: grid;
  grid-template-columns: 0.9fr 1.1fr;
  gap: 24px;
  align-items: start;
}

.checkout-summary {
  padding: 18px;
  margin-top: 18px;
}

.checkout-summary h3 {
  margin: 0 0 10px;
}

.checkout-summary p {
  margin: 0 0 12px;
  color: var(--muted);
}

.checkout-summary strong {
  font-size: 1.4rem;
}

.payment-methods {
  display: flex;
  gap: 10px;
  margin-bottom: 18px;
}

.payment-option {
  flex: 1;
  position: relative;
}

.payment-option input {
  position: absolute;
  opacity: 0;
  pointer-events: none;
}

.payment-option span {
  display: block;
  text-align: center;
  padding: 12px 14px;
  border-radius: var(--radius-md);
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.04);
  color: var(--muted);
  cursor: pointer;
  transition: background var(--transition), color var(--transition), transform var(--transition);
}

.payment-option input:checked + span {
  background: linear-gradient(135deg, rgba(184, 76, 255, 0.2), rgba(76, 201, 255, 0.12));
  color: var(--text);
  transform: translateY(-1px);
}

.inline-fields {
  display: grid;
  grid-template-columns: 1fr 0.7fr;
  gap: 12px;
}

.payment-success {
  margin-top: 14px;
  padding: 14px 16px;
  border-radius: var(--radius-md);
  background: rgba(55, 230, 166, 0.12);
  border: 1px solid rgba(55, 230, 166, 0.3);
  color: #bff7de;
}

/* Modal */
.modal {
  position: fixed;
  inset: 0;
  z-index: 1500;
  display: none;
}

.modal.open {
  display: block;
}

.modal-backdrop {
  position: absolute;
  inset: 0;
  background: rgba(0,0,0,0.72);
  backdrop-filter: blur(8px);
}

.modal-panel {
  position: relative;
  width: min(100% - 24px, 980px);
  margin: 5vh auto 0;
  padding: 18px;
  transform: translateY(18px) scale(0.98);
  opacity: 0;
  animation: modalIn 260ms ease forwards;
}

@keyframes modalIn {
  to { transform: translateY(0) scale(1); opacity: 1; }
}

.modal-close {
  position: absolute;
  top: 14px;
  right: 14px;
  width: 42px;
  height: 42px;
  border-radius: 999px;
  border: 0;
  background: rgba(255,255,255,0.08);
  color: var(--text);
  cursor: pointer;
  font-size: 1.4rem;
}

.modal-grid {
  display: grid;
  grid-template-columns: 0.95fr 1.05fr;
  gap: 18px;
  align-items: center;
}

.modal-image-wrap img {
  width: 100%;
  border-radius: var(--radius-lg);
  aspect-ratio: 4 / 5;
  object-fit: cover;
}

.modal-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 14px;
  margin-bottom: 12px;
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 12px;
  border-radius: 999px;
  background: rgba(184, 76, 255, 0.16);
  border: 1px solid rgba(184, 76, 255, 0.28);
  color: var(--text);
  font-size: 0.82rem;
}

.favorite-btn {
  width: 44px;
  height: 44px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
  cursor: pointer;
  font-size: 1.1rem;
}

.favorite-btn.active {
  color: #ff6b9f;
  text-shadow: 0 0 10px rgba(255, 107, 159, 0.65);
}

.modal-content h3 {
  margin: 0 0 12px;
  font-size: clamp(1.6rem, 4vw, 2.6rem);
}

.modal-content p {
  color: var(--muted);
  line-height: 1.7;
}

.modal-price {
  margin: 18px 0;
  font-weight: 900;
  font-size: 2rem;
  color: var(--blue);
}

.modal-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

/* Toasts */
.toast-container {
  position: fixed;
  right: 16px;
  bottom: 16px;
  z-index: 2000;
  display: grid;
  gap: 10px;
}

.toast {
  min-width: 260px;
  max-width: 320px;
  padding: 14px 16px;
  border-radius: var(--radius-md);
  background: rgba(17, 17, 17, 0.9);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  color: #fff;
  animation: toastIn 280ms ease;
}

[data-theme="light"] .toast {
  background: rgba(255,255,255,0.94);
  color: #111;
}

.toast small {
  display: block;
  color: var(--muted);
  margin-top: 4px;
}

@keyframes toastIn {
  from { transform: translateX(16px); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

/* Back to top */
.back-to-top {
  position: fixed;
  right: 18px;
  bottom: 86px;
  width: 46px;
  height: 46px;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: var(--surface);
  color: var(--text);
  box-shadow: var(--shadow);
  opacity: 0;
  visibility: hidden;
  transform: translateY(12px);
  transition: opacity var(--transition), visibility var(--transition), transform var(--transition);
  z-index: 1200;
  cursor: pointer;
}

.back-to-top.show {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}

/* Footer */
.footer {
  padding: 44px 0 28px;
  border-top: 1px solid var(--border);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr 0.8fr;
  gap: 20px;
  align-items: start;
}

.footer-links,
.footer-social {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  color: var(--muted);
}

.footer-social a {
  width: 42px;
  height: 42px;
  display: grid;
  place-items: center;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: var(--surface);
}

.footer-bottom {
  margin-top: 26px;
  color: var(--muted);
  font-size: 0.92rem;
}

.reveal {
  opacity: 0;
  transform: translateY(22px);
  transition: opacity 700ms ease, transform 700ms ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Responsive */
@media (max-width: 1100px) {
  .hero-grid,
  .auth-layout,
  .checkout-grid,
  .modal-grid {
    grid-template-columns: 1fr;
  }

  .pricing-grid {
    grid-template-columns: 1fr;
  }

  .popular {
    transform: none;
  }

  .explore-toolbar {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 860px) {
  .nav-links {
    position: fixed;
    top: 76px;
    left: 16px;
    right: 16px;
    display: grid;
    gap: 10px;
    padding: 16px;
    background: rgba(10, 10, 10, 0.92);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg);
    backdrop-filter: blur(14px);
    transform: translateY(-20px);
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
    transition: opacity var(--transition), transform var(--transition), visibility var(--transition);
  }

  [data-theme="light"] .nav-links {
    background: rgba(255,255,255,0.95);
  }

  .nav-links.open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
    pointer-events: auto;
  }

  .mobile-toggle {
    display: grid;
  }

  .featured-grid,
  .explore-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .footer-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 640px) {
  .section {
    padding: 72px 0;
  }

  .hero-copy h1 {
    font-size: clamp(2.7rem, 14vw, 4.1rem);
  }

  .featured-grid,
  .explore-grid {
    grid-template-columns: 1fr;
  }

  .hero-stats {
    flex-direction: column;
  }

  .payment-methods,
  .modal-actions {
    flex-direction: column;
  }

  .inline-fields {
    grid-template-columns: 1fr;
  }
}
/* ================================
   HotVibe — Marketplace Interactivity
   ================================ */

const state = {
  activeCategory: "all",
  activePrice: "all",
  searchTerm: "",
  selectedProduct: null,
  favorite: false,
};

const products = [
  {
    id: 1,
    title: "Neon Velvet",
    category: "Lifestyle",
    price: 14,
    description: "A sleek premium pack with cinematic tones, refined styling, and a polished visual identity.",
    featured: true,
    badge: "Best Seller",
  },
  {
    id: 2,
    title: "Midnight Aura",
    category: "Editorial",
    price: 24,
    description: "Elegant editorial content with bold highlights and a luxury night-shoot atmosphere.",
    featured: true,
    badge: "New Drop",
  },
  {
    id: 3,
    title: "Electric Bloom",
    category: "Portrait",
    price: 18,
    description: "Color-rich portrait pack designed to stand out with premium lighting and a clean finish.",
    featured: true,
    badge: "Trending",
  },
  {
    id: 4,
    title: "Velvet Sessions",
    category: "Studio",
    price: 39,
    description: "A studio-crafted content set with striking composition and a refined premium layout.",
    featured: true,
    badge: "Exclusive",
  },
  {
    id: 5,
    title: "Chrome Afterglow",
    category: "BTS",
    price: 9,
    description: "A behind-the-scenes pack with authentic moments and polished creator energy.",
    featured: true,
    badge: "Hot Deal",
  },
  {
    id: 6,
    title: "Lunar Heat",
    category: "Lifestyle",
    price: 49,
    description: "A luxury-toned drop built for creators who want a richer visual story and premium presence.",
    featured: true,
    badge: "VIP",
  },
  {
    id: 7,
    title: "Pulse Prime",
    category: "Portrait",
    price: 22,
    description: "Sharp, modern visuals with elegant contrast and a premium social-ready look.",
    featured: false,
    badge: "Fresh",
  },
  {
    id: 8,
    title: "After Dark",
    category: "Editorial",
    price: 56,
    description: "A moody, high-end editorial set with glossy contrast and cinematic composition.",
    featured: false,
    badge: "Elite",
  },
  {
    id: 9,
    title: "Glow District",
    category: "Studio",
    price: 30,
    description: "Studio lighting with modern gradients and a premium marketplace presentation.",
    featured: false,
    badge: "Popular",
  },
  {
    id: 10,
    title: "Private Frame",
    category: "BTS",
    price: 12,
    description: "Minimalist behind-the-scenes pack for creators who want authenticity with style.",
    featured: false,
    badge: "Limited",
  },
  {
    id: 11,
    title: "Chrome Luxe",
    category: "Lifestyle",
    price: 64,
    description: "Luxury lifestyle content with an upscale aesthetic and powerful conversion appeal.",
    featured: false,
    badge: "Ultra",
  },
  {
    id: 12,
    title: "Night Frequency",
    category: "Editorial",
    price: 44,
    description: "A sleek evening pack with premium tones, strong visual hierarchy, and polished detail.",
    featured: false,
    badge: "Signature",
  },
];

const categorySet = ["all", ...new Set(products.map((item) => item.category))];

const els = {
  loader: document.getElementById("loader"),
  progressBar: document.getElementById("progressBar"),
  navbar: document.getElementById("navbar"),
  backToTop: document.getElementById("backToTop"),
  toastContainer: document.getElementById("toastContainer"),
  heroPreview: document.getElementById("heroPreview"),
  featuredGrid: document.getElementById("featuredGrid"),
  exploreGrid: document.getElementById("exploreGrid"),
  categoryFilters: document.getElementById("categoryFilters"),
  searchInput: document.getElementById("searchInput"),
  priceFilter: document.getElementById("priceFilter"),
  modal: document.getElementById("productModal"),
  modalImage: document.getElementById("modalImage"),
  modalCategory: document.getElementById("modalCategory"),
  modalTitle: document.getElementById("modalTitle"),
  modalDescription: document.getElementById("modalDescription"),
  modalPrice: document.getElementById("modalPrice"),
  favoriteBtn: document.getElementById("favoriteBtn"),
  purchaseBtn: document.getElementById("purchaseBtn"),
  closeModal: document.getElementById("closeModal"),
  selectedPackTitle: document.getElementById("selectedPackTitle"),
  selectedPackPrice: document.getElementById("selectedPackPrice"),
  paymentSuccess: document.getElementById("paymentSuccess"),
  loginForm: document.getElementById("loginForm"),
  signupForm: document.getElementById("signupForm"),
  paymentForm: document.getElementById("paymentForm"),
  themeToggle: document.getElementById("themeToggle"),
  mobileToggle: document.getElementById("mobileToggle"),
  navLinks: document.getElementById("navLinks"),
  joinNowBtn: document.getElementById("joinNowBtn"),
  openSignup: document.getElementById("openSignup"),
};

function svgThumb(title, category, accent1, accent2) {
  const safeTitle = title.replace(/&/g, "&amp;").replace(/</g, "&lt;");
  const safeCat = category.replace(/&/g, "&amp;").replace(/</g, "&lt;");
  const svg = `
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 750">
      <defs>
        <linearGradient id="g" x1="0%" y1="0%" x2="100%" y2="100%">
          <stop offset="0%" stop-color="${accent1}"/>
          <stop offset="100%" stop-color="${accent2}"/>
        </linearGradient>
        <filter id="blur">
          <feGaussianBlur stdDeviation="40" />
        </filter>
      </defs>
      <rect width="600" height="750" fill="#0b0b0f"/>
      <circle cx="140" cy="130" r="110" fill="${accent1}" opacity="0.35" filter="url(#blur)" />
      <circle cx="470" cy="190" r="130" fill="${accent2}" opacity="0.32" filter="url(#blur)" />
      <rect x="50" y="60" width="500" height="630" rx="34" fill="url(#g)" opacity="0.18" stroke="rgba(255,255,255,0.16)" />
      <rect x="78" y="88" width="444" height="574" rx="28" fill="rgba(255,255,255,0.04)" stroke="rgba(255,255,255,0.14)" />
      <text x="100" y="180" font-size="54" font-family="Arial, sans-serif" fill="#ffffff" font-weight="700">${safeTitle}</text>
      <text x="100" y="238" font-size="24" font-family="Arial, sans-serif" fill="rgba(255,255,255,0.76)">${safeCat}</text>
      <rect x="100" y="290" width="210" height="8" rx="4" fill="rgba(255,255,255,0.24)" />
      <rect x="100" y="320" width="320" height="8" rx="4" fill="rgba(255,255,255,0.18)" />
      <rect x="100" y="350" width="260" height="8" rx="4" fill="rgba(255,255,255,0.18)" />
      <circle cx="430" cy="470" r="120" fill="${accent1}" opacity="0.35" />
      <circle cx="300" cy="520" r="78" fill="${accent2}" opacity="0.42" />
      <text x="100" y="640" font-size="28" font-family="Arial, sans-serif" fill="#ffffff" font-weight="600">HotVibe Exclusive Pack</text>
    </svg>
  `;
  return `data:image/svg+xml;charset=UTF-8,${encodeURIComponent(svg)}`;
}

function getAccentPair(index) {
  const palette = [
    ["#b84cff", "#4cc9ff"],
    ["#ff4fd8", "#b84cff"],
    ["#4cc9ff", "#37e6a6"],
    ["#ff7a59", "#ff4fd8"],
  ];
  return palette[index % palette.length];
}

function formatPrice(value) {
  return `$${Number(value).toFixed(2)}`;
}

function createCard(product, featured = false) {
  const [a1, a2] = getAccentPair(product.id);
  const img = svgThumb(product.title, product.category, a1, a2);

  const card = document.createElement("article");
  card.className = "content-card reveal";
  card.dataset.category = product.category;
  card.dataset.price = product.price;
  card.dataset.title = product.title.toLowerCase();

  card.innerHTML = `
    <div class="content-thumb">
      <img loading="lazy" src="${img}" alt="${product.title} preview" />
      <div class="content-overlay">
        <button class="quick-view" data-action="view">View Details</button>
        <span class="pill">${product.badge}</span>
      </div>
    </div>
    <div class="card-body">
      <h3>${product.title}</h3>
      <p class="card-sub">${product.category}</p>
      <div class="card-row">
        <span class="card-price">${formatPrice(product.price)}</span>
        <button class="btn btn-secondary" data-action="view">${featured ? "View" : "View Details"}</button>
      </div>
    </div>
  `;

  card.querySelectorAll('[data-action="view"]').forEach((btn) => {
    btn.addEventListener("click", () => openProductModal(product));
  });

  return card;
}

function renderFeatured() {
  const featured = products.filter((p) => p.featured).slice(0, 6);
  els.featuredGrid.innerHTML = "";
  featured.forEach((product) => {
    els.featuredGrid.appendChild(createCard(product, true));
  });
}

function renderHeroPreview() {
  const items = products.slice(0, 3);
  els.heroPreview.innerHTML = items
    .map((product) => {
      const [a1, a2] = getAccentPair(product.id);
      return `
        <div class="preview-item">
          <img src="${svgThumb(product.title, product.category, a1, a2)}" alt="${product.title}" loading="lazy" />
          <div>
            <strong>${product.title}</strong>
            <span>${product.category} • ${product.badge}</span>
          </div>
          <div class="preview-price">${formatPrice(product.price)}</div>
        </div>
      `;
    })
    .join("");
}

function renderCategories() {
  els.categoryFilters.innerHTML = "";
  categorySet.forEach((category) => {
    const button = document.createElement("button");
    button.className = `filter-btn ${category === "all" ? "active" : ""}`;
    button.textContent = category === "all" ? "All" : category;
    button.dataset.category = category;

    button.addEventListener("click", () => {
      state.activeCategory = category;
      document.querySelectorAll(".filter-btn").forEach((btn) => btn.classList.remove("active"));
      button.classList.add("active");
      renderExplore();
    });

    els.categoryFilters.appendChild(button);
  });
}

function matchesPrice(price) {
  switch (state.activePrice) {
    case "under20":
      return price < 20;
    case "20to40":
      return price >= 20 && price <= 40;
    case "40plus":
      return price > 40;
    default:
      return true;
  }
}

function renderExplore() {
  const term = state.searchTerm.trim().toLowerCase();

  const filtered = products.filter((product) => {
    const matchesCategory = state.activeCategory === "all" || product.category === state.activeCategory;
    const matchesSearch =
      !term ||
      product.title.toLowerCase().includes(term) ||
      product.category.toLowerCase().includes(term) ||
      product.description.toLowerCase().includes(term);
    const matchesPriceRange = matchesPrice(product.price);

    return matchesCategory && matchesSearch && matchesPriceRange;
  });

  els.exploreGrid.innerHTML = "";
  filtered.forEach((product) => els.exploreGrid.appendChild(createCard(product)));

  if (filtered.length === 0) {
    const empty = document.createElement("div");
    empty.className = "glass-panel";
    empty.style.padding = "24px";
    empty.style.gridColumn = "1 / -1";
    empty.innerHTML = `<strong>No packs found.</strong><p style="color: var(--muted); margin: 8px 0 0;">Try a different search or filter.</p>`;
    els.exploreGrid.appendChild(empty);
  }

  observeReveals();
}

function openProductModal(product) {
  state.selectedProduct = product;
  state.favorite = false;
  els.favoriteBtn.classList.remove("active");
  els.modalImage.src = svgThumb(product.title, product.category, ...getAccentPair(product.id));
  els.modalCategory.textContent = product.category;
  els.modalTitle.textContent = product.title;
  els.modalDescription.textContent = product.description;
  els.modalPrice.textContent = formatPrice(product.price);

  els.modal.classList.add("open");
  els.modal.setAttribute("aria-hidden", "false");
  document.body.style.overflow = "hidden";
}

function closeProductModal() {
  els.modal.classList.remove("open");
  els.modal.setAttribute("aria-hidden", "true");
  document.body.style.overflow = "";
}

function showToast(title, subtitle = "") {
  const toast = document.createElement("div");
  toast.className = "toast";
  toast.innerHTML = `<strong>${title}</strong>${subtitle ? `<small>${subtitle}</small>` : ""}`;
  els.toastContainer.appendChild(toast);

  setTimeout(() => {
    toast.style.opacity = "0";
    toast.style.transform = "translateX(16px)";
    toast.style.transition = "260ms ease";
  }, 2600);

  setTimeout(() => toast.remove(), 3100);
}

function validateField(input, message) {
  const field = input.closest(".field");
  const error = field ? field.querySelector(".error-msg") : null;
  if (!input.value.trim()) {
    if (error) error.textContent = message;
    return false;
  }
  if (error) error.textContent = "";
  return true;
}

function validateEmail(value) {
  return /^\S+@\S+\.\S+$/.test(value);
}

function validateExpiry(value) {
  return /^(0[1-9]|1[0-2])\/\d{2}$/.test(value);
}

function validateCard(value) {
  return /^\d{16}$/.test(value.replace(/\s/g, ""));
}

function validateCVV(value) {
  return /^\d{3,4}$/.test(value);
}

function setSelectedPack(product) {
  els.selectedPackTitle.textContent = product.title;
  els.selectedPackPrice.textContent = formatPrice(product.price);
}

function applyTheme(theme) {
  document.documentElement.setAttribute("data-theme", theme);
  els.themeToggle.textContent = theme === "light" ? "☀" : "☾";
  localStorage.setItem("hotvibe-theme", theme);
}

function toggleTheme() {
  const current = document.documentElement.getAttribute("data-theme") || "dark";
  applyTheme(current === "dark" ? "light" : "dark");
}

function observeReveals() {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
          observer.unobserve(entry.target);
        }
      });
    },
    { threshold: 0.15 }
  );

  document.querySelectorAll(".reveal:not(.visible)").forEach((el) => observer.observe(el));
}

function animateCounters() {
  const counters = document.querySelectorAll(".counter");
  const counterObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return;
        const el = entry.target;
        const target = parseInt(el.dataset.target, 10);
        const duration = 1200;
        const start = 0;
        const startTime = performance.now();

        const tick = (time) => {
          const progress = Math.min((time - startTime) / duration, 1);
          const value = Math.floor(start + (target - start) * progress);
          el.textContent = target >= 1000 ? value.toLocaleString() : value;
          if (progress < 1) requestAnimationFrame(tick);
        };

        requestAnimationFrame(tick);
        counterObserver.unobserve(el);
      });
    },
    { threshold: 0.5 }
  );

  counters.forEach((c) => counterObserver.observe(c));
}

function handleScroll() {
  const scrollTop = window.scrollY;
  const docHeight = document.documentElement.scrollHeight - window.innerHeight;
  const percent = (scrollTop / docHeight) * 100;

  els.progressBar.style.width = `${percent}%`;
  els.navbar.classList.toggle("scrolled", scrollTop > 24);
  els.backToTop.classList.toggle("show", scrollTop > 500);
}

function setupNotifications() {
  const messages = [
    "Someone just purchased a pack.",
    "A creator launched a new exclusive drop.",
    "A premium customer joined HotVibe.",
    "A pack is trending right now.",
    "New content was added to the marketplace.",
  ];

  setInterval(() => {
    const message = messages[Math.floor(Math.random() * messages.length)];
    showToast("Live activity", message);
  }, 9000);
}

function initTabs() {
  const tabs = document.querySelectorAll(".tab-btn");
  tabs.forEach((tab) => {
    tab.addEventListener("click", () => {
      tabs.forEach((t) => t.classList.remove("active"));
      tab.classList.add("active");

      const target = tab.dataset.tab;
      els.loginForm.classList.toggle("active", target === "login");
      els.signupForm.classList.toggle("active", target === "signup");
    });
  });
}

function attachForms() {
  els.loginForm.addEventListener("submit", (e) => {
    e.preventDefault();
    const email = els.loginForm.querySelector('[name="email"]');
    const password = els.loginForm.querySelector('[name="password"]');

    let ok = true;
    ok &= validateField(email, "Email is required.");
    ok &= validateField(password, "Password is required.");

    if (email.value && !validateEmail(email.value)) {
      email.closest(".field").querySelector(".error-msg").textContent = "Enter a valid email.";
      ok = false;
    }

    if (password.value && password.value.length < 6) {
      password.closest(".field").querySelector(".error-msg").textContent = "Password must be at least 6 characters.";
      ok = false;
    }

    if (ok) {
      showToast("Login successful", "Welcome back to HotVibe.");
      els.loginForm.reset();
    }
  });

  els.signupForm.addEventListener("submit", (e) => {
    e.preventDefault();
    const username = els.signupForm.querySelector('[name="username"]');
    const email = els.signupForm.querySelector('[name="email"]');
    const password = els.signupForm.querySelector('[name="password"]');
    const confirmPassword = els.signupForm.querySelector('[name="confirmPassword"]');

    let ok = true;
    ok &= validateField(username, "Username is required.");
    ok &= validateField(email, "Email is required.");
    ok &= validateField(password, "Password is required.");
    ok &= validateField(confirmPassword, "Please confirm your password.");

    if (email.value && !validateEmail(email.value)) {
      email.closest(".field").querySelector(".error-msg").textContent = "Enter a valid email.";
      ok = false;
    }

    if (password.value && password.value.length < 6) {
      password.closest(".field").querySelector(".error-msg").textContent = "Password must be at least 6 characters.";
      ok = false;
    }

    if (password.value && confirmPassword.value && password.value !== confirmPassword.value) {
      confirmPassword.closest(".field").querySelector(".error-msg").textContent = "Passwords do not match.";
      ok = false;
    }

    if (ok) {
      showToast("Account created", "Your HotVibe profile is ready.");
      els.signupForm.reset();
    }
  });

  els.paymentForm.addEventListener("submit", (e) => {
    e.preventDefault();

    const name = els.paymentForm.querySelector('[name="name"]');
    const email = els.paymentForm.querySelector('[name="email"]');
    const cardNumber = els.paymentForm.querySelector('[name="cardNumber"]');
    const expiry = els.paymentForm.querySelector('[name="expiry"]');
    const cvv = els.paymentForm.querySelector('[name="cvv"]');
    const method = els.paymentForm.querySelector('input[name="method"]:checked').value;

    let ok = true;
    const fields = [name, email, cardNumber, expiry, cvv];

    fields.forEach((input) => {
      const label = input.previousElementSibling?.textContent || "Field";
      if (!validateField(input, `${label} is required.`)) ok = false;
    });

    if (email.value && !validateEmail(email.value)) {
      email.closest(".field").querySelector(".error-msg").textContent = "Enter a valid email.";
      ok = false;
    }

    if (cardNumber.value && !validateCard(cardNumber.value)) {
      cardNumber.closest(".field").querySelector(".error-msg").textContent = "Card number must contain 16 digits.";
      ok = false;
    }

    if (expiry.value && !validateExpiry(expiry.value)) {
      expiry.closest(".field").querySelector(".error-msg").textContent = "Use MM/YY format.";
      ok = false;
    }

    if (cvv.value && !validateCVV(cvv.value)) {
      cvv.closest(".field").querySelector(".error-msg").textContent = "CVV must be 3 or 4 digits.";
      ok = false;
    }

    if (method === "paypal") {
      showToast("PayPal selected", "UI-only payment mode enabled.");
    }

    if (ok) {
      els.paymentSuccess.hidden = false;
      showToast("Payment successful", "Access granted instantly.");
      els.paymentForm.reset();
      setTimeout(() => {
        els.paymentSuccess.hidden = true;
      }, 3200);
    }
  });
}

function initMobileMenu() {
  els.mobileToggle.addEventListener("click", () => {
    els.navLinks.classList.toggle("open");
  });

  els.navLinks.querySelectorAll("a").forEach((link) => {
    link.addEventListener("click", () => {
      els.navLinks.classList.remove("open");
    });
  });
}

function initTheme() {
  const saved = localStorage.getItem("hotvibe-theme") || "dark";
  applyTheme(saved);
  els.themeToggle.addEventListener("click", toggleTheme);
}

function initModal() {
  els.closeModal.addEventListener("click", closeProductModal);
  els.modal.addEventListener("click", (e) => {
    if (e.target.dataset.close === "true") closeProductModal();
  });

  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape" && els.modal.classList.contains("open")) {
      closeProductModal();
    }
  });

  els.favoriteBtn.addEventListener("click", () => {
    state.favorite = !state.favorite;
    els.favoriteBtn.classList.toggle("active", state.favorite);
    els.favoriteBtn.textContent = state.favorite ? "♥" : "♡";
  });

  els.purchaseBtn.addEventListener("click", () => {
    if (state.selectedProduct) {
      setSelectedPack(state.selectedProduct);
      closeProductModal();
      document.querySelector("#checkout").scrollIntoView({ behavior: "smooth" });
      showToast("Added to checkout", `${state.selectedProduct.title} is ready for payment.`);
    }
  });

  document.getElementById("modalSecondaryBtn").addEventListener("click", () => {
    if (state.selectedProduct) {
      showToast("Saved", `${state.selectedProduct.title} saved for later.`);
    }
  });
}

function bindQuickActions() {
  els.searchInput.addEventListener("input", (e) => {
    state.searchTerm = e.target.value;
    renderExplore();
  });

  els.priceFilter.addEventListener("change", (e) => {
    state.activePrice = e.target.value;
    renderExplore();
  });

  els.joinNowBtn.addEventListener("click", () => {
    const signupTab = document.querySelector('.tab-btn[data-tab="signup"]');
    signupTab.click();
    document.querySelector("#auth").scrollIntoView({ behavior: "smooth" });
  });

  els.openSignup.addEventListener("click", () => {
    const signupTab = document.querySelector('.tab-btn[data-tab="signup"]');
    setTimeout(() => signupTab.click(), 50);
  });
}

function initScroll() {
  window.addEventListener("scroll", handleScroll, { passive: true });
  handleScroll();
}

function initBackToTop() {
  els.backToTop.addEventListener("click", () => {
    window.scrollTo({ top: 0, behavior: "smooth" });
  });
}

function hideLoader() {
  window.setTimeout(() => {
    els.loader.classList.add("hidden");
  }, 700);
}

function boot() {
  renderHeroPreview();
  renderFeatured();
  renderCategories();
  renderExplore();
  animateCounters();
  observeReveals();
  initTheme();
  initMobileMenu();
  initModal();
  initTabs();
  attachForms();
  bindQuickActions();
  initScroll();
  initBackToTop();
  setupNotifications();
  hideLoader();

  // Set a default selected pack for checkout preview
  setSelectedPack(products[0]);

  // Reveal cards after render
  setTimeout(() => observeReveals(), 50);
}

window.addEventListener("DOMContentLoaded", boot);
