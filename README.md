[index.html](https://github.com/user-attachments/files/27751624/index.html)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>WealthWise — Personal Finance & Investment Insights</title>
  <meta name="description" content="Expert insights on personal finance, investing, real estate, and building lasting wealth in the modern economy."/>

  <!-- ✅ ADSENSE SCRIPT (ganti dengan kode asli dari akun AdSense kamu) -->
  <!--
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXX" crossorigin="anonymous"></script>
  -->

  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,600&family=Crimson+Pro:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Barlow:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>

  <style>
    /* ─────────────────────────────────────────
       CSS VARIABLES & RESET
    ───────────────────────────────────────── */
    :root {
      --bg:         #FAFAF7;
      --bg2:        #F2F0EA;
      --bg-dark:    #0D1B0F;
      --bg-mid:     #162015;
      --text:       #1C1C18;
      --text-muted: #6B7264;
      --gold:       #C8922A;
      --gold-light: #E8BE6A;
      --emerald:    #2A6B3C;
      --border:     #DDD9CF;
      --white:      #FFFFFF;
      --ff-display: 'Cormorant Garamond', Georgia, serif;
      --ff-body:    'Crimson Pro', Georgia, serif;
      --ff-ui:      'Barlow', sans-serif;
      --max-w:      1280px;
      --r:          4px;
      --shadow:     0 2px 20px rgba(0,0,0,0.08);
      --shadow-lg:  0 8px 40px rgba(0,0,0,0.14);
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: var(--ff-body);
      background: var(--bg);
      color: var(--text);
      font-size: 18px;
      line-height: 1.7;
      overflow-x: hidden;
    }
    a { color: inherit; text-decoration: none; }
    img { display: block; max-width: 100%; height: auto; }

    /* ─────────────────────────────────────────
       AD UNIT STYLES — SEMUA TIPE ADSENSE
    ───────────────────────────────────────── */

    /* Label "Advertisement" wajib oleh AdSense */
    .ad-label {
      font-family: var(--ff-ui);
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--text-muted);
      text-align: center;
      display: block;
      margin-bottom: 4px;
    }
    .ad-wrap { text-align: center; }

    /* Placeholder style untuk demo (diganti <ins class="adsbygoogle"> saat live) */
    .ad-slot {
      background: linear-gradient(135deg, #f0ede4 0%, #e8e4d8 100%);
      border: 1.5px dashed #C8B88A;
      border-radius: var(--r);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 6px;
      margin: 0 auto;
      position: relative;
      overflow: hidden;
    }
    .ad-slot::before {
      content: '';
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        45deg, transparent, transparent 12px,
        rgba(200,146,42,0.04) 12px, rgba(200,146,42,0.04) 24px
      );
    }
    .ad-slot-inner {
      position: relative;
      z-index: 1;
      text-align: center;
    }
    .ad-slot-inner .ad-type {
      font-family: var(--ff-ui);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--gold);
    }
    .ad-slot-inner .ad-size {
      font-family: var(--ff-ui);
      font-size: 13px;
      color: var(--text-muted);
      margin-top: 2px;
    }
    .ad-slot-inner .ad-cpm {
      font-family: var(--ff-ui);
      font-size: 11px;
      background: var(--emerald);
      color: #fff;
      padding: 2px 8px;
      border-radius: 20px;
      margin-top: 4px;
      display: inline-block;
    }

    /* 1. ANCHOR AD — Sticky bottom bar */
    .ad-anchor {
      position: fixed;
      bottom: 0; left: 0; right: 0;
      z-index: 999;
      background: var(--bg-dark);
      padding: 8px 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 16px;
      box-shadow: 0 -4px 24px rgba(0,0,0,0.3);
    }
    .ad-anchor .ad-label { color: #888; margin: 0; }
    .ad-anchor .ad-slot {
      width: 320px; height: 50px;
      border-color: #444;
      background: linear-gradient(135deg, #1a2a1c, #0f1e11);
    }
    .ad-anchor .ad-slot-inner .ad-size { color: #aaa; }
    .ad-anchor-close {
      position: absolute; right: 12px; top: 50%; transform: translateY(-50%);
      font-family: var(--ff-ui); font-size: 20px; cursor: pointer;
      color: #888; line-height: 1;
      background: none; border: none; padding: 4px 8px;
      transition: color 0.2s;
    }
    .ad-anchor-close:hover { color: #fff; }

    /* 2. LEADERBOARD — Top of page */
    .ad-leaderboard-wrap {
      background: var(--bg-dark);
      padding: 8px 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
    }
    .ad-leaderboard-wrap .ad-label { color: #666; margin: 0; }
    .ad-leaderboard { width: 728px; height: 90px; max-width: 100%; }

    /* 3. BILLBOARD */
    .ad-billboard-wrap {
      padding: 24px 0;
      background: var(--bg2);
      text-align: center;
    }
    .ad-billboard { width: 970px; height: 250px; max-width: 100%; }

    /* 4. DISPLAY 300x250 */
    .ad-display-300 { width: 300px; height: 250px; }

    /* 5. DISPLAY 300x600 Half-Page */
    .ad-display-300x600 { width: 300px; height: 600px; }

    /* 6. IN-ARTICLE 336x280 */
    .ad-inarticle { width: 336px; height: 280px; float: right; margin: 8px 0 16px 24px; }
    .ad-inarticle-center { width: 336px; height: 280px; margin: 24px auto; }

    /* 7. IN-FEED NATIVE */
    .ad-infeed {
      width: 100%;
      height: 120px;
      background: linear-gradient(135deg, #EDF5EF 0%, #E4F0E6 100%);
      border: 1.5px dashed #6BAF80;
    }
    .ad-infeed .ad-slot-inner .ad-type { color: var(--emerald); }

    /* 8. MULTIPLEX */
    .ad-multiplex { width: 100%; height: 300px; }
    .ad-multiplex .ad-slot-inner .ad-type { color: var(--gold); }

    /* ─────────────────────────────────────────
       LAYOUT
    ───────────────────────────────────────── */
    .container {
      max-width: var(--max-w);
      margin: 0 auto;
      padding: 0 24px;
    }
    .layout-main {
      display: grid;
      grid-template-columns: 1fr 320px;
      gap: 48px;
      align-items: start;
    }
    .sidebar {
      position: sticky;
      top: 24px;
      display: flex;
      flex-direction: column;
      gap: 32px;
    }

    /* ─────────────────────────────────────────
       HEADER
    ───────────────────────────────────────── */
    .site-header {
      background: var(--bg-dark);
      color: var(--white);
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 20px rgba(0,0,0,0.4);
    }
    .header-top {
      border-bottom: 1px solid rgba(255,255,255,0.08);
      padding: 6px 0;
    }
    .header-top .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .header-date {
      font-family: var(--ff-ui);
      font-size: 11px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: #888;
    }
    .header-tag {
      font-family: var(--ff-ui);
      font-size: 11px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--gold-light);
    }
    .header-main {
      padding: 16px 0;
    }
    .header-main .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .site-logo {
      display: flex;
      flex-direction: column;
      line-height: 1;
    }
    .logo-mark {
      font-family: var(--ff-display);
      font-size: 42px;
      font-weight: 600;
      letter-spacing: -1px;
      color: var(--white);
    }
    .logo-mark span { color: var(--gold-light); }
    .logo-sub {
      font-family: var(--ff-ui);
      font-size: 10px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: #888;
      margin-top: 2px;
    }
    nav {
      display: flex;
      gap: 28px;
    }
    nav a {
      font-family: var(--ff-ui);
      font-size: 13px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #bbb;
      transition: color 0.2s;
      padding-bottom: 2px;
      border-bottom: 1px solid transparent;
    }
    nav a:hover, nav a.active {
      color: var(--gold-light);
      border-bottom-color: var(--gold-light);
    }
    .header-actions {
      display: flex;
      gap: 12px;
      align-items: center;
    }
    .btn-subscribe {
      font-family: var(--ff-ui);
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      background: var(--gold);
      color: var(--bg-dark);
      padding: 9px 20px;
      border-radius: 2px;
      cursor: pointer;
      border: none;
      transition: background 0.2s;
    }
    .btn-subscribe:hover { background: var(--gold-light); }
    .header-nav-row {
      border-top: 1px solid rgba(255,255,255,0.06);
      padding: 10px 0;
    }
    .header-nav-row .container {
      display: flex;
      gap: 32px;
      overflow-x: auto;
    }

    /* ─────────────────────────────────────────
       HERO SECTION
    ───────────────────────────────────────── */
    .hero {
      background: var(--bg-mid);
      color: var(--white);
      padding: 60px 0;
    }
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 420px;
      gap: 48px;
      align-items: center;
    }
    .hero-category {
      font-family: var(--ff-ui);
      font-size: 11px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--gold-light);
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 16px;
    }
    .hero-category::before {
      content: '';
      width: 32px; height: 1px;
      background: var(--gold);
    }
    .hero-title {
      font-family: var(--ff-display);
      font-size: 58px;
      font-weight: 300;
      line-height: 1.1;
      letter-spacing: -1px;
      margin-bottom: 20px;
    }
    .hero-title em {
      font-style: italic;
      color: var(--gold-light);
    }
    .hero-excerpt {
      font-family: var(--ff-body);
      font-size: 18px;
      color: #aab5a0;
      line-height: 1.7;
      margin-bottom: 28px;
      font-weight: 300;
    }
    .hero-meta {
      font-family: var(--ff-ui);
      font-size: 12px;
      color: #777;
      letter-spacing: 0.5px;
    }
    .hero-meta span { color: var(--gold-light); }
    .hero-image {
      border-radius: 2px;
      overflow: hidden;
      aspect-ratio: 4/3;
      background: linear-gradient(135deg, #1E3A22 0%, #0A2010 50%, #162A18 100%);
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .hero-img-placeholder {
      text-align: center;
    }
    .hero-img-placeholder .chart {
      font-size: 80px;
      display: block;
      margin-bottom: 8px;
    }
    .hero-img-placeholder p {
      font-family: var(--ff-ui);
      font-size: 12px;
      color: #4a6a50;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
    .hero-sidebar {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    .hero-secondary {
      border-left: 2px solid rgba(255,255,255,0.08);
      padding-left: 24px;
    }
    .hero-secondary-cat {
      font-family: var(--ff-ui);
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--gold-light);
      margin-bottom: 8px;
    }
    .hero-secondary h3 {
      font-family: var(--ff-display);
      font-size: 22px;
      font-weight: 400;
      line-height: 1.25;
      color: #e0dbd0;
    }
    .hero-secondary h3:hover { color: var(--gold-light); cursor: pointer; }
    .hero-divider {
      height: 1px;
      background: rgba(255,255,255,0.06);
    }

    /* ─────────────────────────────────────────
       SECTION LABELS
    ───────────────────────────────────────── */
    .section-header {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-bottom: 28px;
      padding-bottom: 14px;
      border-bottom: 2px solid var(--text);
    }
    .section-title {
      font-family: var(--ff-ui);
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 3px;
      text-transform: uppercase;
    }
    .section-line {
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* ─────────────────────────────────────────
       ARTICLE CARDS
    ───────────────────────────────────────── */
    .articles-feed {
      display: flex;
      flex-direction: column;
      gap: 0;
    }
    .article-card {
      display: grid;
      grid-template-columns: 200px 1fr;
      gap: 20px;
      padding: 24px 0;
      border-bottom: 1px solid var(--border);
      cursor: pointer;
      transition: transform 0.15s;
    }
    .article-card:hover { transform: translateX(3px); }
    .article-card:first-child { padding-top: 0; }
    .article-thumb {
      border-radius: 2px;
      overflow: hidden;
      aspect-ratio: 3/2;
    }
    .thumb-placeholder {
      width: 100%; height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 36px;
    }
    .article-cat {
      font-family: var(--ff-ui);
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--emerald);
      margin-bottom: 8px;
      font-weight: 600;
    }
    .article-title {
      font-family: var(--ff-display);
      font-size: 22px;
      font-weight: 500;
      line-height: 1.25;
      margin-bottom: 10px;
    }
    .article-title:hover { color: var(--gold); }
    .article-excerpt {
      font-size: 15px;
      color: var(--text-muted);
      line-height: 1.6;
      margin-bottom: 12px;
      font-weight: 300;
    }
    .article-meta {
      font-family: var(--ff-ui);
      font-size: 11px;
      color: var(--text-muted);
      display: flex;
      gap: 12px;
      align-items: center;
    }
    .article-meta .read-time {
      background: var(--bg2);
      padding: 2px 8px;
      border-radius: 20px;
    }

    /* ─────────────────────────────────────────
       FEATURED ARTICLE (LONG FORM)
    ───────────────────────────────────────── */
    .featured-section {
      background: var(--bg2);
      padding: 64px 0;
      margin: 48px 0;
    }
    .article-full {
      max-width: 720px;
    }
    .article-full .article-cat {
      font-size: 11px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .article-full .article-cat::before {
      content: '';
      width: 24px; height: 2px;
      background: var(--emerald);
      display: inline-block;
    }
    .article-full h1 {
      font-family: var(--ff-display);
      font-size: 52px;
      font-weight: 400;
      line-height: 1.1;
      letter-spacing: -0.5px;
      margin: 16px 0 20px;
    }
    .article-full h2 {
      font-family: var(--ff-display);
      font-size: 30px;
      font-weight: 500;
      margin: 36px 0 14px;
      color: var(--bg-mid);
    }
    .article-full .article-byline {
      font-family: var(--ff-ui);
      font-size: 13px;
      color: var(--text-muted);
      padding: 16px 0;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      margin-bottom: 28px;
      display: flex;
      gap: 16px;
      align-items: center;
    }
    .article-full .author-dot {
      width: 40px; height: 40px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--emerald), var(--bg-mid));
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--ff-display);
      font-size: 18px;
      font-weight: 600;
      color: white;
      flex-shrink: 0;
    }
    .article-full p {
      margin-bottom: 22px;
      font-size: 19px;
      line-height: 1.75;
      font-weight: 300;
      color: #2a2a25;
    }
    .article-full .pullquote {
      font-family: var(--ff-display);
      font-size: 28px;
      font-weight: 400;
      font-style: italic;
      line-height: 1.4;
      color: var(--bg-mid);
      border-left: 4px solid var(--gold);
      padding: 20px 28px;
      margin: 36px 0;
      background: white;
    }
    .clearfix::after { content: ''; display: block; clear: both; }

    /* ─────────────────────────────────────────
       SIDEBAR WIDGETS
    ───────────────────────────────────────── */
    .sidebar-widget {
      background: white;
      border-radius: var(--r);
      padding: 20px;
      border: 1px solid var(--border);
    }
    .widget-title {
      font-family: var(--ff-ui);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 16px;
      padding-bottom: 10px;
      border-bottom: 2px solid var(--text);
    }
    .trending-item {
      display: flex;
      gap: 12px;
      align-items: flex-start;
      padding: 12px 0;
      border-bottom: 1px solid var(--bg2);
      cursor: pointer;
    }
    .trending-item:last-child { border-bottom: none; padding-bottom: 0; }
    .trending-num {
      font-family: var(--ff-display);
      font-size: 28px;
      font-weight: 300;
      color: var(--border);
      line-height: 1;
      flex-shrink: 0;
      width: 32px;
    }
    .trending-title {
      font-family: var(--ff-display);
      font-size: 17px;
      font-weight: 500;
      line-height: 1.3;
    }
    .trending-title:hover { color: var(--gold); }
    .ticker-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 0;
      border-bottom: 1px solid var(--bg2);
      font-family: var(--ff-ui);
    }
    .ticker-item:last-child { border-bottom: none; }
    .ticker-sym { font-weight: 700; font-size: 14px; }
    .ticker-val { font-size: 13px; color: var(--text-muted); }
    .ticker-chg { font-size: 13px; font-weight: 600; }
    .up { color: #2D8A4E; }
    .down { color: #C84A3A; }

    /* ─────────────────────────────────────────
       MULTIPLEX AD SECTION
    ───────────────────────────────────────── */
    .multiplex-section {
      padding: 48px 0;
      border-top: 2px solid var(--text);
      border-bottom: 2px solid var(--text);
      margin: 48px 0;
    }

    /* ─────────────────────────────────────────
       NEWSLETTER
    ───────────────────────────────────────── */
    .newsletter-section {
      background: var(--bg-dark);
      color: white;
      padding: 64px 0;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .newsletter-section::before {
      content: '$';
      position: absolute;
      font-family: var(--ff-display);
      font-size: 400px;
      font-weight: 700;
      color: rgba(255,255,255,0.02);
      top: -80px;
      left: -40px;
      line-height: 1;
    }
    .newsletter-section::after {
      content: '%';
      position: absolute;
      font-family: var(--ff-display);
      font-size: 300px;
      font-weight: 700;
      color: rgba(200,146,42,0.04);
      bottom: -60px;
      right: 0;
      line-height: 1;
    }
    .newsletter-title {
      font-family: var(--ff-display);
      font-size: 48px;
      font-weight: 300;
      letter-spacing: -0.5px;
      margin-bottom: 12px;
      position: relative;
    }
    .newsletter-sub {
      font-family: var(--ff-body);
      font-size: 18px;
      color: #888;
      margin-bottom: 32px;
      font-weight: 300;
      position: relative;
    }
    .newsletter-form {
      display: flex;
      gap: 0;
      max-width: 480px;
      margin: 0 auto;
      position: relative;
    }
    .newsletter-input {
      flex: 1;
      padding: 14px 18px;
      font-family: var(--ff-ui);
      font-size: 14px;
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(255,255,255,0.15);
      border-right: none;
      color: white;
      outline: none;
    }
    .newsletter-input::placeholder { color: #555; }
    .newsletter-btn {
      font-family: var(--ff-ui);
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      background: var(--gold);
      color: var(--bg-dark);
      padding: 14px 24px;
      border: none;
      cursor: pointer;
      transition: background 0.2s;
    }
    .newsletter-btn:hover { background: var(--gold-light); }

    /* ─────────────────────────────────────────
       CATEGORIES STRIP
    ───────────────────────────────────────── */
    .categories-strip {
      background: white;
      padding: 20px 0;
      border-bottom: 1px solid var(--border);
    }
    .cat-list {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      align-items: center;
    }
    .cat-pill {
      font-family: var(--ff-ui);
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.5px;
      padding: 6px 16px;
      border-radius: 20px;
      border: 1.5px solid var(--border);
      white-space: nowrap;
      cursor: pointer;
      transition: all 0.2s;
    }
    .cat-pill:hover, .cat-pill.active {
      background: var(--text);
      color: white;
      border-color: var(--text);
    }

    /* ─────────────────────────────────────────
       FOOTER
    ───────────────────────────────────────── */
    footer {
      background: var(--bg-mid);
      color: #888;
      padding: 48px 0 100px; /* space for anchor ad */
    }
    .footer-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 40px;
      padding-bottom: 40px;
      border-bottom: 1px solid rgba(255,255,255,0.06);
      margin-bottom: 24px;
    }
    .footer-brand .logo-mark {
      font-size: 32px;
      margin-bottom: 8px;
    }
    .footer-brand p {
      font-family: var(--ff-body);
      font-size: 14px;
      line-height: 1.7;
      margin-top: 8px;
    }
    .footer-col h4 {
      font-family: var(--ff-ui);
      font-size: 11px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #ccc;
      margin-bottom: 16px;
    }
    .footer-col a {
      display: block;
      font-family: var(--ff-ui);
      font-size: 13px;
      margin-bottom: 10px;
      color: #777;
      transition: color 0.2s;
    }
    .footer-col a:hover { color: var(--gold-light); }
    .footer-bottom {
      font-family: var(--ff-ui);
      font-size: 12px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .footer-bottom .adsense-note {
      font-size: 11px;
      color: var(--gold);
      background: rgba(200,146,42,0.1);
      padding: 3px 10px;
      border-radius: 2px;
      letter-spacing: 0.5px;
    }

    /* ─────────────────────────────────────────
       AD STRATEGY PANEL
    ───────────────────────────────────────── */
    .strategy-panel {
      background: linear-gradient(135deg, #0D1B0F, #162015);
      color: white;
      padding: 64px 0;
    }
    .strategy-title {
      font-family: var(--ff-display);
      font-size: 40px;
      font-weight: 300;
      color: var(--gold-light);
      margin-bottom: 8px;
    }
    .strategy-sub {
      font-family: var(--ff-ui);
      font-size: 13px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #555;
      margin-bottom: 40px;
    }
    .strategy-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 24px;
      margin-bottom: 48px;
    }
    .strategy-card {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: var(--r);
      padding: 24px;
    }
    .strategy-card .s-num {
      font-family: var(--ff-display);
      font-size: 48px;
      font-weight: 300;
      color: var(--gold);
      line-height: 1;
      margin-bottom: 8px;
    }
    .strategy-card h3 {
      font-family: var(--ff-ui);
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #ccc;
      margin-bottom: 10px;
    }
    .strategy-card p {
      font-family: var(--ff-body);
      font-size: 15px;
      color: #777;
      line-height: 1.6;
    }
    .revenue-table {
      width: 100%;
      border-collapse: collapse;
      font-family: var(--ff-ui);
      font-size: 14px;
    }
    .revenue-table th {
      text-align: left;
      padding: 12px 16px;
      font-size: 11px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: #666;
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }
    .revenue-table td {
      padding: 14px 16px;
      border-bottom: 1px solid rgba(255,255,255,0.04);
      color: #bbb;
    }
    .revenue-table tr:hover td { background: rgba(255,255,255,0.02); }
    .revenue-table .td-type { color: var(--gold-light); font-weight: 600; }
    .revenue-table .td-rev { color: #4CAF76; font-weight: 700; }
    .revenue-table .td-total {
      background: rgba(200,146,42,0.08);
      color: var(--gold-light);
      font-weight: 700;
      font-size: 16px;
    }
    .revenue-table tfoot td { border-top: 2px solid rgba(200,146,42,0.3); }

    /* Spacing helpers */
    .mt-8 { margin-top: 8px; }
    .mt-16 { margin-top: 16px; }
    .mt-24 { margin-top: 24px; }
    .mt-32 { margin-top: 32px; }
    .mt-48 { margin-top: 48px; }
    .mb-8 { margin-bottom: 8px; }
    .mb-16 { margin-bottom: 16px; }
    .mb-24 { margin-bottom: 24px; }
    .mb-32 { margin-bottom: 32px; }
    .mb-48 { margin-bottom: 48px; }
    .py-48 { padding: 48px 0; }

    /* Page Load Animation */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .hero-title { animation: fadeUp 0.7s ease both; }
    .hero-excerpt { animation: fadeUp 0.7s 0.1s ease both; }
    .hero-meta { animation: fadeUp 0.7s 0.2s ease both; }

    /* ─────────────────────────────────────────
       RESPONSIVE
    ───────────────────────────────────────── */
    @media (max-width: 1024px) {
      .layout-main { grid-template-columns: 1fr; }
      .sidebar { position: static; }
      .hero-grid { grid-template-columns: 1fr; }
      .hero-title { font-size: 40px; }
      .strategy-grid { grid-template-columns: repeat(2, 1fr); }
      .footer-grid { grid-template-columns: 1fr 1fr; }
    }
    @media (max-width: 768px) {
      .article-card { grid-template-columns: 1fr; }
      .article-thumb { display: none; }
      .hero-title { font-size: 32px; }
      nav { display: none; }
      .ad-leaderboard { width: 320px; height: 50px; }
      .ad-billboard { width: 320px; height: 100px; }
      .ad-inarticle { float: none; width: 100%; height: auto; aspect-ratio: 6/2; }
      .strategy-grid { grid-template-columns: 1fr; }
      .footer-grid { grid-template-columns: 1fr; }
      .footer-bottom { flex-direction: column; gap: 8px; text-align: center; }
    }
  </style>
</head>

<body>

<!-- ═══════════════════════════════════════════════════
     1. ANCHOR AD — Sticky Bottom (selalu terlihat)
══════════════════════════════════════════════════════ -->
<div class="ad-anchor" id="anchor-ad">
  <span class="ad-label">Advertisement</span>
  <div class="ad-slot ad-slot" style="width:320px;height:50px;">
    <div class="ad-slot-inner">
      <div class="ad-type">Anchor Ad</div>
      <div class="ad-size">320×50 / 728×90 Mobile Sticky</div>
      <div class="ad-cpm">Est. CPM: $4–8</div>
    </div>
  </div>
  <!-- Real AdSense code:
  <ins class="adsbygoogle" style="display:inline-block;width:320px;height:50px"
    data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
  <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  -->
  <button class="ad-anchor-close" onclick="document.getElementById('anchor-ad').style.display='none'">✕</button>
</div>

<!-- ═══════════════════════════════════════════════════
     2. LEADERBOARD AD — Paling atas, highest viewability
══════════════════════════════════════════════════════ -->
<div class="ad-leaderboard-wrap">
  <span class="ad-label">Advertisement</span>
  <div class="ad-slot ad-leaderboard">
    <div class="ad-slot-inner">
      <div class="ad-type">Leaderboard</div>
      <div class="ad-size">728×90 px</div>
      <div class="ad-cpm">Est. CPM: $6–15 (Finance niche)</div>
    </div>
  </div>
  <!-- Real:
  <ins class="adsbygoogle" style="display:inline-block;width:728px;height:90px"
    data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
  -->
</div>

<!-- ═══════════════════════════════════════════════════
     SITE HEADER
══════════════════════════════════════════════════════ -->
<header class="site-header">
  <div class="header-top">
    <div class="container">
      <span class="header-date">Thursday, 14 May 2026</span>
      <span class="header-tag">★ Finance · Investing · Wealth · Economy</span>
    </div>
  </div>
  <div class="header-main">
    <div class="container">
      <a href="#" class="site-logo">
        <div class="logo-mark">Wealth<span>Wise</span></div>
        <div class="logo-sub">Personal Finance & Investment</div>
      </a>
      <nav>
        <a href="#" class="active">Home</a>
        <a href="#">Investing</a>
        <a href="#">Real Estate</a>
        <a href="#">Markets</a>
        <a href="#">Crypto</a>
        <a href="#">Retirement</a>
        <a href="#">Tax</a>
      </nav>
      <div class="header-actions">
        <button class="btn-subscribe">Subscribe Free</button>
      </div>
    </div>
  </div>
</header>

<!-- ═══════════════════════════════════════════════════
     CATEGORIES STRIP
══════════════════════════════════════════════════════ -->
<div class="categories-strip">
  <div class="container">
    <div class="cat-list">
      <div class="cat-pill active">All</div>
      <div class="cat-pill">Stock Market</div>
      <div class="cat-pill">ETF & Index Funds</div>
      <div class="cat-pill">Real Estate</div>
      <div class="cat-pill">Cryptocurrency</div>
      <div class="cat-pill">Retirement Planning</div>
      <div class="cat-pill">Tax Strategy</div>
      <div class="cat-pill">Budgeting</div>
      <div class="cat-pill">Side Hustle</div>
      <div class="cat-pill">Insurance</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     HERO SECTION
══════════════════════════════════════════════════════ -->
<section class="hero">
  <div class="container">
    <div class="hero-grid">
      <div>
        <div class="hero-category">Cover Story — Investing</div>
        <h1 class="hero-title">
          Why <em>Index Funds</em> Will<br/>
          Still Beat 94% of Investors<br/>
          Over the Next Decade
        </h1>
        <p class="hero-excerpt">
          Despite the rise of AI-driven trading, quantitative hedge funds, and celebrity stock-pickers, 
          the boring old index fund remains the single most powerful wealth-building tool available to 
          ordinary people. Here's the math — and the mindset — behind why.
        </p>
        <div class="hero-meta">
          By <span>Jonathan Marsh</span> · May 14, 2026 · 12 min read
        </div>
      </div>
      <div class="hero-sidebar">
        <div class="hero-image">
          <div class="hero-img-placeholder">
            <span class="chart">📈</span>
            <p>Market Analysis 2026</p>
          </div>
        </div>
        <div class="hero-secondary">
          <div class="hero-secondary-cat">Real Estate</div>
          <h3>Is Now Really a Good Time to Buy Property? What the Data Says</h3>
        </div>
        <div class="hero-divider"></div>
        <div class="hero-secondary">
          <div class="hero-secondary-cat">Tax Strategy</div>
          <h3>7 Legal Tax Deductions Most People Completely Miss Every Year</h3>
        </div>
        <div class="hero-divider"></div>
        <div class="hero-secondary">
          <div class="hero-secondary-cat">Retirement</div>
          <h3>The 4% Rule Is Broken. Here's What Experts Recommend Instead</h3>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════════
     3. BILLBOARD AD — Below hero, very high CTR zone
══════════════════════════════════════════════════════ -->
<div class="ad-billboard-wrap">
  <span class="ad-label">Advertisement</span>
  <div class="ad-slot ad-billboard">
    <div class="ad-slot-inner">
      <div class="ad-type">Billboard / Pushdown</div>
      <div class="ad-size">970×250 px — Premium placement below hero</div>
      <div class="ad-cpm">Est. CPM: $10–25 (Finance niche, high intent)</div>
    </div>
  </div>
  <!-- Real:
  <ins class="adsbygoogle" style="display:block;width:970px;height:250px;"
    data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
  -->
</div>

<!-- ═══════════════════════════════════════════════════
     MAIN CONTENT + SIDEBAR
══════════════════════════════════════════════════════ -->
<div class="container py-48">
  <div class="layout-main">

    <!-- MAIN CONTENT AREA -->
    <main>
      <div class="section-header">
        <span class="section-title">Latest Articles</span>
        <span class="section-line"></span>
        <span style="font-family:var(--ff-ui);font-size:11px;color:var(--text-muted);">Updated daily</span>
      </div>

      <div class="articles-feed">

        <!-- Article 1 -->
        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#1E4A2A,#0D2B15)">📊</div>
          </div>
          <div>
            <div class="article-cat">Investing</div>
            <h2 class="article-title">Dollar-Cost Averaging: The Silent Wealth Machine Almost Nobody Uses Correctly</h2>
            <p class="article-excerpt">Most investors understand the concept, but dramatically underestimate the compounding advantage of strict, emotionless DCA discipline during market corrections.</p>
            <div class="article-meta">
              <span>Sarah Chen · May 13</span>
              <span class="read-time">8 min read</span>
            </div>
          </div>
        </article>

        <!-- Article 2 -->
        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#4A1E1E,#2B0D0D)">🏠</div>
          </div>
          <div>
            <div class="article-cat">Real Estate</div>
            <h2 class="article-title">REITs vs Physical Property in 2026: A Side-by-Side Comparison for Regular Investors</h2>
            <p class="article-excerpt">With interest rates stabilizing, both options look attractive — but for very different investor profiles. We break down liquidity, returns, tax treatment, and effort.</p>
            <div class="article-meta">
              <span>Marcus Hill · May 12</span>
              <span class="read-time">10 min read</span>
            </div>
          </div>
        </article>

        <!-- Article 3 -->
        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#2A3A4A,#0D1B2B)">💎</div>
          </div>
          <div>
            <div class="article-cat">Crypto</div>
            <h2 class="article-title">Bitcoin as a Retirement Asset: Portfolio Managers Are Changing Their Tune</h2>
            <p class="article-excerpt">Institutional adoption, spot ETFs, and the fourth halving have fundamentally shifted how fiduciaries think about digital assets in long-horizon portfolios.</p>
            <div class="article-meta">
              <span>Alex Rodriguez · May 11</span>
              <span class="read-time">7 min read</span>
            </div>
          </div>
        </article>

      </div><!-- end articles-feed -->

      <!-- ─────────────────────────────────────
           4. IN-FEED AD — Naturally inside article feed
      ───────────────────────────────────────── -->
      <div style="padding: 20px 0; border-bottom: 1px solid var(--border);">
        <span class="ad-label">Sponsored Content</span>
        <div class="ad-slot ad-infeed">
          <div class="ad-slot-inner">
            <div class="ad-type">In-Feed Native Ad</div>
            <div class="ad-size">Full-width responsive — blends with article feed</div>
            <div class="ad-cpm">Est. CPM: $5–12 · High CTR (native)</div>
          </div>
        </div>
        <!-- Real:
        <ins class="adsbygoogle" style="display:block"
          data-ad-format="fluid" data-ad-layout-key="-6t+ed+2i-1n-4w"
          data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
        -->
      </div>

      <!-- More Articles After In-Feed Ad -->
      <div class="articles-feed mt-8">

        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#3A2A4A,#1B0D2B)">📋</div>
          </div>
          <div>
            <div class="article-cat">Tax Strategy</div>
            <h2 class="article-title">How to Harvest Tax Losses Without Violating the Wash-Sale Rule</h2>
            <p class="article-excerpt">Tax-loss harvesting is a genuinely powerful strategy — but it has strict rules. Here's the complete playbook for doing it right before year-end.</p>
            <div class="article-meta">
              <span>Diana Park · May 10</span>
              <span class="read-time">9 min read</span>
            </div>
          </div>
        </article>

        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#1A3A2A,#0D2B1A)">🎯</div>
          </div>
          <div>
            <div class="article-cat">Retirement</div>
            <h2 class="article-title">Maxing Out Your 401(k) in 2026: New Contribution Limits and Catch-Up Rules</h2>
            <p class="article-excerpt">New legislation increased catch-up contribution limits for workers aged 60–63. Here's exactly how to take advantage and shelter more money from taxes today.</p>
            <div class="article-meta">
              <span>Tom Wilson · May 9</span>
              <span class="read-time">6 min read</span>
            </div>
          </div>
        </article>

        <article class="article-card">
          <div class="article-thumb">
            <div class="thumb-placeholder" style="background:linear-gradient(135deg,#4A3A1A,#2B200D)">💰</div>
          </div>
          <div>
            <div class="article-cat">Budgeting</div>
            <h2 class="article-title">The Zero-Based Budget Method: Assign Every Dollar Before the Month Starts</h2>
            <p class="article-excerpt">Forget the 50/30/20 rule. Zero-based budgeting forces intentional spending at a level that transforms your financial behavior within 90 days.</p>
            <div class="article-meta">
              <span>Priya Nair · May 8</span>
              <span class="read-time">5 min read</span>
            </div>
          </div>
        </article>

      </div><!-- end articles-feed -->

      <!-- ─────────────────────────────────────
           5. IN-FEED AD #2
      ───────────────────────────────────────── -->
      <div style="padding: 20px 0; border-bottom: 1px solid var(--border);">
        <span class="ad-label">Sponsored Content</span>
        <div class="ad-slot ad-infeed">
          <div class="ad-slot-inner">
            <div class="ad-type">In-Feed Native Ad #2</div>
            <div class="ad-size">Full-width · Appears naturally in feed</div>
            <div class="ad-cpm">Est. CPM: $5–12</div>
          </div>
        </div>
      </div>

    </main>

    <!-- SIDEBAR -->
    <aside class="sidebar">

      <!-- 6. DISPLAY AD 300x250 — Most clicked ad size -->
      <div class="sidebar-widget" style="padding:12px;">
        <span class="ad-label">Advertisement</span>
        <div class="ad-slot ad-display-300">
          <div class="ad-slot-inner">
            <div class="ad-type">Medium Rectangle</div>
            <div class="ad-size">300×250 px</div>
            <div class="ad-cpm">Highest CTR format · CPM $8–20</div>
          </div>
        </div>
        <!-- Real:
        <ins class="adsbygoogle" style="display:inline-block;width:300px;height:250px"
          data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
        -->
      </div>

      <!-- TRENDING WIDGET -->
      <div class="sidebar-widget">
        <div class="widget-title">Trending Now</div>
        <div class="trending-item">
          <div class="trending-num">01</div>
          <div class="trending-title">Emergency Fund Size in High-Inflation Era</div>
        </div>
        <div class="trending-item">
          <div class="trending-num">02</div>
          <div class="trending-title">Should You Pay Off Mortgage Early?</div>
        </div>
        <div class="trending-item">
          <div class="trending-num">03</div>
          <div class="trending-title">Roth vs Traditional IRA: 2026 Guide</div>
        </div>
        <div class="trending-item">
          <div class="trending-num">04</div>
          <div class="trending-title">Best High-Yield Savings Accounts</div>
        </div>
        <div class="trending-item">
          <div class="trending-num">05</div>
          <div class="trending-title">FIRE Movement: Early Retirement Math</div>
        </div>
      </div>

      <!-- MARKET TICKER WIDGET -->
      <div class="sidebar-widget">
        <div class="widget-title">Market Snapshot</div>
        <div class="ticker-item">
          <span class="ticker-sym">S&P 500</span>
          <span class="ticker-val">5,842.10</span>
          <span class="ticker-chg up">+0.73%</span>
        </div>
        <div class="ticker-item">
          <span class="ticker-sym">NASDAQ</span>
          <span class="ticker-val">18,294.50</span>
          <span class="ticker-chg up">+1.12%</span>
        </div>
        <div class="ticker-item">
          <span class="ticker-sym">DOW</span>
          <span class="ticker-val">42,118.30</span>
          <span class="ticker-chg down">−0.18%</span>
        </div>
        <div class="ticker-item">
          <span class="ticker-sym">BTC</span>
          <span class="ticker-val">$89,420</span>
          <span class="ticker-chg up">+2.34%</span>
        </div>
        <div class="ticker-item">
          <span class="ticker-sym">GOLD</span>
          <span class="ticker-val">$3,181</span>
          <span class="ticker-chg up">+0.44%</span>
        </div>
      </div>

      <!-- 7. DISPLAY AD 300x600 Half-Page — Premium sidebar -->
      <div class="sidebar-widget" style="padding:12px;">
        <span class="ad-label">Advertisement</span>
        <div class="ad-slot ad-display-300x600">
          <div class="ad-slot-inner">
            <div class="ad-type">Half-Page / 300×600</div>
            <div class="ad-size">300×600 px — Premium size</div>
            <div class="ad-cpm">CPM: $12–30 · High viewability</div>
          </div>
        </div>
        <!-- Real:
        <ins class="adsbygoogle" style="display:inline-block;width:300px;height:600px"
          data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
        -->
      </div>

    </aside>
  </div><!-- end layout-main -->
</div><!-- end container -->

<!-- ═══════════════════════════════════════════════════
     FEATURED LONG-FORM ARTICLE WITH IN-ARTICLE ADS
══════════════════════════════════════════════════════ -->
<section class="featured-section">
  <div class="container">
    <div class="section-header" style="margin-bottom:40px;">
      <span class="section-title">Featured Deep Dive</span>
      <span class="section-line"></span>
    </div>

    <div class="layout-main">
      <article class="article-full">
        <div class="article-cat">Cover Story · Investing</div>
        <h1>Why Index Funds Will Still Beat 94% of Investors Over the Next Decade</h1>
        <div class="article-byline">
          <div class="author-dot">J</div>
          <div>
            <strong>Jonathan Marsh</strong>, Senior Investment Editor<br/>
            <span style="font-size:12px;color:var(--text-muted);">May 14, 2026 · 12 min read · Fact-checked</span>
          </div>
        </div>

        <p>
          Every year, thousands of investors pay high fees to active fund managers who promise to beat the market. 
          And every year, the data tells the same uncomfortable story: the vast majority of those managers fail to 
          outperform a simple index fund tracking the S&P 500.
        </p>

        <p>
          According to the latest SPIVA report — the gold standard for tracking active vs. passive fund performance — 
          94.2% of large-cap active funds underperformed the S&P 500 over a 20-year period ending in 2025. 
          The figure for mid-cap funds was 95.7%. For small-cap, 91.4%.
        </p>

        <!-- ─────────────────────────────────
             8. IN-ARTICLE AD (Right-Float)
        ──────────────────────────────────── -->
        <div class="clearfix">
          <div class="ad-wrap">
            <span class="ad-label">Advertisement</span>
            <div class="ad-slot ad-inarticle">
              <div class="ad-slot-inner">
                <div class="ad-type">In-Article Ad</div>
                <div class="ad-size">336×280 px · Float Right</div>
                <div class="ad-cpm">CPM: $8–18</div>
              </div>
            </div>
          </div>
          <!-- Real:
          <ins class="adsbygoogle" style="display:inline-block;width:336px;height:280px;float:right;margin:8px 0 16px 24px"
            data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
          -->

          <h2>The Mathematics of Compounding</h2>
          <p>
            Consider the compounding math over 30 years. A $10,000 investment in an S&P 500 index fund 
            with 0.03% expense ratio (such as Vanguard's VOO) at the historical 10.5% average annual return 
            grows to approximately $198,000. The same investment in an average active fund — 
            charging 1% fees and returning 9% annually after underperformance — grows to only $132,000.
          </p>

          <p>
            That difference of $66,000 is entirely attributable to fees and underperformance. The compounding 
            drag of even a 1.5% annual fee is extraordinary over multi-decade timeframes. Yet the mutual fund 
            industry collectively charges over $100 billion in management fees annually in the United States alone.
          </p>
        </div>

        <div class="pullquote">
          "The investor's chief problem — and even his worst enemy — is likely to be himself." — Benjamin Graham
        </div>

        <h2>Why Smart People Keep Making Dumb Choices</h2>
        <p>
          If the data is so overwhelming, why do investors keep pouring money into actively managed funds? 
          The answer lies in behavioral psychology. Humans are wired to believe that effort and intelligence 
          should translate into better outcomes — a trait that serves us well in most areas of life, 
          but catastrophically in markets.
        </p>

        <!-- ─────────────────────────────────
             9. IN-ARTICLE AD (Centered)
        ──────────────────────────────────── -->
        <div class="ad-wrap">
          <span class="ad-label">Advertisement</span>
          <div class="ad-slot ad-inarticle-center">
            <div class="ad-slot-inner">
              <div class="ad-type">In-Article Ad #2</div>
              <div class="ad-size">336×280 px · Centered between paragraphs</div>
              <div class="ad-cpm">CPM: $8–18 · High viewability (mid-article)</div>
            </div>
          </div>
          <!-- Real:
          <ins class="adsbygoogle" style="display:block;text-align:center"
            data-ad-layout="in-article" data-ad-format="fluid"
            data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
          -->
        </div>

        <p>
          Markets are also increasingly efficient. Every trade has a counterparty — when a fund manager buys 
          a stock believing it's undervalued, someone else is selling it believing it's overvalued. For every 
          winner in active management, there is necessarily a loser. After transaction costs, the aggregate 
          active manager must underperform the passive index by the amount of costs. This is not an opinion — 
          it is an arithmetic identity, first articulated by Nobel laureate William Sharpe.
        </p>

        <h2>The Correct Portfolio for Most People</h2>
        <p>
          For most investors — those without a multi-billion dollar research budget, access to private deals, 
          or algorithmic edge — a simple three-fund portfolio remains the empirically superior choice: 
          a domestic index fund, an international index fund, and a bond index fund, with allocations 
          adjusted for age and risk tolerance.
        </p>

        <p>
          The discipline required is not financial knowledge. It is emotional fortitude: the ability to 
          continue buying during crashes, to resist the narrative pull of the next hot sector, 
          and to ignore every persuasive-sounding fund manager on financial television.
        </p>

        <!-- ─────────────────────────────────
             10. IN-ARTICLE AD #3 (near end)
        ──────────────────────────────────── -->
        <div class="ad-wrap">
          <span class="ad-label">Advertisement</span>
          <div class="ad-slot ad-inarticle-center" style="height:100px;">
            <div class="ad-slot-inner">
              <div class="ad-type">In-Article Ad #3</div>
              <div class="ad-size">Full-width fluid · End of article</div>
              <div class="ad-cpm">CPM: $6–14 · Post-read intent = high conversion</div>
            </div>
          </div>
        </div>

      </article>

      <!-- Sidebar -->
      <aside class="sidebar">
        <div class="sidebar-widget" style="padding:12px;">
          <span class="ad-label">Advertisement</span>
          <div class="ad-slot ad-display-300">
            <div class="ad-slot-inner">
              <div class="ad-type">Medium Rectangle</div>
              <div class="ad-size">300×250 px</div>
              <div class="ad-cpm">CPM: $8–20</div>
            </div>
          </div>
        </div>
        <div class="sidebar-widget">
          <div class="widget-title">Also Read</div>
          <div class="trending-item">
            <div class="trending-num">01</div>
            <div class="trending-title">How to Backtest Your Investment Strategy</div>
          </div>
          <div class="trending-item">
            <div class="trending-num">02</div>
            <div class="trending-title">The Real Cost of Inflation on Savings</div>
          </div>
          <div class="trending-item">
            <div class="trending-num">03</div>
            <div class="trending-title">Warren Buffett's 3 Rules for Stock Selection</div>
          </div>
        </div>
        <div class="sidebar-widget" style="padding:12px;">
          <span class="ad-label">Advertisement</span>
          <div class="ad-slot ad-display-300x600">
            <div class="ad-slot-inner">
              <div class="ad-type">Half-Page</div>
              <div class="ad-size">300×600 px</div>
              <div class="ad-cpm">CPM: $12–30</div>
            </div>
          </div>
        </div>
      </aside>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════════
     11. MULTIPLEX AD — Grid of multiple ads in one unit
══════════════════════════════════════════════════════ -->
<div class="multiplex-section container">
  <div class="section-header">
    <span class="section-title">From Our Partners</span>
    <span class="section-line"></span>
  </div>
  <span class="ad-label">Advertisement</span>
  <div class="ad-slot ad-multiplex">
    <div class="ad-slot-inner">
      <div class="ad-type">Multiplex Ad (Grid)</div>
      <div class="ad-size">Full-width responsive · Shows 4–8 native ad cards in a grid</div>
      <div class="ad-cpm" style="margin-top:8px;">Best for: End of article / Below content · CPM: $4–10</div>
    </div>
  </div>
  <!-- Real:
  <ins class="adsbygoogle" style="display:block"
    data-ad-format="autorelaxed"
    data-ad-client="ca-pub-XXXXX" data-ad-slot="XXXXXXX"></ins>
  -->
</div>

<!-- ═══════════════════════════════════════════════════
     NEWSLETTER
══════════════════════════════════════════════════════ -->
<section class="newsletter-section">
  <h2 class="newsletter-title">Smarter Money, Every Morning</h2>
  <p class="newsletter-sub">Join 280,000 readers who get our free weekly finance digest.</p>
  <div class="newsletter-form">
    <input class="newsletter-input" type="email" placeholder="Your email address"/>
    <button class="newsletter-btn">Subscribe</button>
  </div>
</section>

<!-- ═══════════════════════════════════════════════════
     12. INTERSTITIAL / VIGNETTE — Between page loads
        (Aktif otomatis di AdSense Auto Ads)
══════════════════════════════════════════════════════ -->
<div style="background:var(--bg2);padding:24px 0;text-align:center;border-top:1px solid var(--border);">
  <span class="ad-label">Advertisement</span>
  <div class="ad-slot ad-billboard" style="width:600px;height:160px;margin:0 auto;">
    <div class="ad-slot-inner">
      <div class="ad-type">Interstitial / Vignette (Auto Ads)</div>
      <div class="ad-size">Fullscreen between page navigation · Managed by Google Auto Ads</div>
      <div class="ad-cpm">CPM: $15–40 · Highest-earning format (by impression value)</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     AD REVENUE STRATEGY PANEL
══════════════════════════════════════════════════════ -->
<section class="strategy-panel">
  <div class="container">
    <div class="strategy-sub">AdSense Monetization Blueprint</div>
    <h2 class="strategy-title">Revenue Scenario: 100,000 Monthly Pageviews</h2>

    <div class="strategy-grid">
      <div class="strategy-card">
        <div class="s-num">7</div>
        <h3>Ad Types Active</h3>
        <p>Leaderboard, Display 300x250, 300x600, In-Feed, In-Article, Multiplex, Anchor, Interstitial</p>
      </div>
      <div class="strategy-card">
        <div class="s-num">$18</div>
        <h3>Avg Page RPM</h3>
        <p>Finance niche earns $12–25 RPM. With multiple ad units + high-intent audience, $18 is conservative.</p>
      </div>
      <div class="strategy-card">
        <div class="s-num">68%</div>
        <h3>Revenue Share</h3>
        <p>Google pays publishers 68% of ad revenue. The remaining 32% goes to Google for the platform.</p>
      </div>
      <div class="strategy-card">
        <div class="s-num">$1,800</div>
        <h3>Est. Monthly Net</h3>
        <p>At 100K pageviews × $18 RPM = $1,800/mo. At 500K pageviews: ~$9,000/mo.</p>
      </div>
    </div>

    <div style="overflow-x:auto;">
      <table class="revenue-table">
        <thead>
          <tr>
            <th>Ad Unit Type</th>
            <th>Placement</th>
            <th>Size</th>
            <th>Est. CPM (Finance)</th>
            <th>Impr/Month</th>
            <th>Est. Revenue</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="td-type">Leaderboard</td>
            <td>Top of every page</td>
            <td>728×90</td>
            <td>$8–15</td>
            <td>100,000</td>
            <td class="td-rev">~$110</td>
          </tr>
          <tr>
            <td class="td-type">Billboard</td>
            <td>Below hero section</td>
            <td>970×250</td>
            <td>$12–22</td>
            <td>100,000</td>
            <td class="td-rev">~$170</td>
          </tr>
          <tr>
            <td class="td-type">In-Feed Native</td>
            <td>Between article cards</td>
            <td>Fluid</td>
            <td>$6–12</td>
            <td>80,000</td>
            <td class="td-rev">~$96</td>
          </tr>
          <tr>
            <td class="td-type">Display 300×250</td>
            <td>Sidebar</td>
            <td>300×250</td>
            <td>$10–20</td>
            <td>100,000</td>
            <td class="td-rev">~$150</td>
          </tr>
          <tr>
            <td class="td-type">Half-Page 300×600</td>
            <td>Sidebar sticky</td>
            <td>300×600</td>
            <td>$15–28</td>
            <td>70,000</td>
            <td class="td-rev">~$168</td>
          </tr>
          <tr>
            <td class="td-type">In-Article (×3)</td>
            <td>Between paragraphs</td>
            <td>336×280</td>
            <td>$10–18</td>
            <td>180,000</td>
            <td class="td-rev">~$252</td>
          </tr>
          <tr>
            <td class="td-type">Multiplex</td>
            <td>End of article</td>
            <td>Fluid grid</td>
            <td>$5–10</td>
            <td>80,000</td>
            <td class="td-rev">~$72</td>
          </tr>
          <tr>
            <td class="td-type">Anchor Sticky</td>
            <td>Fixed bottom bar</td>
            <td>320×50</td>
            <td>$4–8</td>
            <td>200,000</td>
            <td class="td-rev">~$120</td>
          </tr>
          <tr>
            <td class="td-type">Interstitial</td>
            <td>Between page loads (Auto)</td>
            <td>Fullscreen</td>
            <td>$20–40</td>
            <td>30,000</td>
            <td class="td-rev">~$270</td>
          </tr>
        </tbody>
        <tfoot>
          <tr>
            <td colspan="5" class="td-total" style="font-size:14px;letter-spacing:1px;text-transform:uppercase;">Total Estimated Monthly Revenue (100K PV)</td>
            <td class="td-total">~$1,408–$2,800</td>
          </tr>
        </tfoot>
      </table>
    </div>

    <p style="font-family:var(--ff-ui);font-size:12px;color:#444;margin-top:16px;">
      * Estimates based on Finance niche CPM benchmarks. Actual earnings vary by geography, traffic quality, season, and content. Q4 (Oct–Dec) typically 40–60% higher due to advertiser spending.
    </p>
  </div>
</section>

<!-- ═══════════════════════════════════════════════════
     FOOTER
══════════════════════════════════════════════════════ -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="logo-mark" style="color:#ccc;font-size:32px">Wealth<span style="color:var(--gold-light)">Wise</span></div>
        <p>Expert insights on personal finance, investing, and building lasting wealth. Published weekdays with in-depth analysis trusted by 280,000+ readers.</p>
      </div>
      <div class="footer-col">
        <h4>Topics</h4>
        <a href="#">Investing</a>
        <a href="#">Real Estate</a>
        <a href="#">Cryptocurrency</a>
        <a href="#">Retirement</a>
        <a href="#">Tax Strategy</a>
      </div>
      <div class="footer-col">
        <h4>Company</h4>
        <a href="#">About Us</a>
        <a href="#">Editorial Policy</a>
        <a href="#">Advertise</a>
        <a href="#">Privacy Policy</a>
        <a href="#">Terms of Use</a>
      </div>
      <div class="footer-col">
        <h4>Resources</h4>
        <a href="#">Investment Calculator</a>
        <a href="#">Budget Planner</a>
        <a href="#">Retirement Estimator</a>
        <a href="#">Newsletter Archive</a>
        <a href="#">RSS Feed</a>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 WealthWise Media. All rights reserved.</span>
      <span class="adsense-note">✦ AdSense Optimized — 9 Ad Formats Active</span>
      <span>Disclosure: This site contains advertising from Google AdSense.</span>
    </div>
  </div>
</footer>

<script>
  // Smooth category filter
  document.querySelectorAll('.cat-pill').forEach(pill => {
    pill.addEventListener('click', () => {
      document.querySelectorAll('.cat-pill').forEach(p => p.classList.remove('active'));
      pill.classList.add('active');
    });
  });

  // Intersection Observer for ad visibility logging (useful for optimization)
  if ('IntersectionObserver' in window) {
    const adSlots = document.querySelectorAll('.ad-slot');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.borderColor = '#2D6A4F';
          // In production: trigger ad load here for lazy-loading
        }
      });
    }, { threshold: 0.5 });
    adSlots.forEach(slot => observer.observe(slot));
  }

  // Ticker animation
  const tickers = document.querySelectorAll('.ticker-chg');
  setInterval(() => {
    tickers.forEach(t => {
      const isUp = t.classList.contains('up');
      const base = parseFloat(t.textContent.replace(/[^0-9.]/g, ''));
      const delta = (Math.random() * 0.1 - 0.05).toFixed(2);
      const newVal = (base + parseFloat(delta)).toFixed(2);
      t.textContent = (isUp ? '+' : '−') + newVal + '%';
    });
  }, 3000);

  // Newsletter button
  document.querySelector('.newsletter-btn').addEventListener('click', function() {
    const input = document.querySelector('.newsletter-input');
    if (input.value) {
      this.textContent = '✓ Subscribed!';
      this.style.background = '#2D6A4F';
      input.value = '';
      setTimeout(() => {
        this.textContent = 'Subscribe';
        this.style.background = '';
      }, 3000);
    }
  });
</script>

</body>
</html>
