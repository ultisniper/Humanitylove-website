# Humanitylove.com
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HumanityLove - Spreading Compassion Worldwide</title>
    <meta name="description" content="Join us in making the world a better place through acts of kindness and charitable donations">
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    
    <!-- Critical CSS -->
    <style>
        :root {
            --primary-color: #e74c3c;
            --secondary-color: #3498db;
            --dark-color: #2c3e50;
            --light-color: #ecf0f1;
            --success-color: #2ecc71;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }
        
        .loading {
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .loaded {
            opacity: 1;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 600;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--dark-color);
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero-bg.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 12rem 2rem 8rem;
            margin-top: 80px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .cta-button {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .cta-button:hover {
            background: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        /* Why Donate Section */
        .section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.2rem;
            color: var(--dark-color);
        }
        
        .reasons-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .reason-card {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .reason-card:hover {
            transform: translateY(-10px);
        }
        
        .reason-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .reason-card h3 {
            margin-bottom: 1rem;
            color: var(--dark-color);
        }
        
        /* Progress Section */
        .progress-stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 3rem 0;
        }
        
        .stat {
            text-align: center;
            margin: 1rem;
            flex: 1;
            min-width: 150px;
        }
        
        .number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }
        
        .label {
            font-size: 1.1rem;
            color: var(--dark-color);
        }
        
        .progress-bar {
            background: #f0f0f0;
            border-radius: 50px;
            height: 30px;
            margin: 2rem 0;
            overflow: hidden;
        }
        
        .current-progress {
            background: var(--primary-color);
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            width: 65%;
        }
        
        /* Video Gallery */
        .video-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .video-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .video-card iframe {
            width: 100%;
            height: 200px;
            border: none;
        }
        
        .video-card h3 {
            padding: 1rem;
            color: var(--dark-color);
        }
        
        .load-more {
            display: block;
            margin: 2rem auto 0;
            background: var(--secondary-color);
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .load-more:hover {
            background: #2980b9;
        }
        
        /* Donation Portal */
        .donation-options {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .amount-options {
            flex: 1;
            min-width: 300px;
        }
        
        .amount-btn {
            background: white;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            padding: 0.8rem 1.5rem;
            margin: 0.5rem;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .amount-btn:hover, .amount-btn.active {
            background: var(--primary-color);
            color: white;
        }
        
        .custom-amount {
            margin-top: 1rem;
            display: flex;
            align-items: center;
        }
        
        .custom-amount span {
            font-size: 1.2rem;
            margin-right: 0.5rem;
        }
        
        .custom-amount input {
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
            width: 150px;
        }
        
        #donation-form {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark-color);
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        .donate-btn {
            width: 100%;
            padding: 1rem;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .donate-btn:hover {
            background: #c0392b;
        }
        
        .security-badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .security-badges img {
            height: 50px;
        }
        
        /* Social Media Section */
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .social-icons a {
            color: var(--dark-color);
            font-size: 2rem;
            transition: color 0.3s;
        }
        
        .social-icons a:hover {
            color: var(--primary-color);
        }
        
        .social-share {
            text-align: center;
            margin-top: 2rem;
        }
        
        .share-btn {
            padding: 0.6rem 1.2rem;
            margin: 0 0.5rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .share-btn.facebook {
            background: #3b5998;
            color: white;
        }
        
        .share-btn.twitter {
            background: #1da1f2;
            color: white;
        }
        
        .share-btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        /* Footer */
        footer {
            background: var(--dark-color);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        .copyright {
            margin-top: 1rem;
            font-size: 0.9rem;
            color: rgba(255,255,255,0.7);
        }
        
        /* Cookie Consent */
        .cookie-consent {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: var(--dark-color);
            color: white;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            z-index: 1000;
            display: none;
        }
        
        .cookie-consent p {
            margin-right: 1rem;
            flex: 1;
            min-width: 200px;
        }
        
        .cookie-consent a {
            color: var(--secondary-color);
            text-decoration: none;
        }
        
        .cookie-consent button {
            padding: 0.5rem 1rem;
            margin: 0.3rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        
        #acceptCookies {
            background: var(--success-color);
            color: white;
        }
        
        #rejectCookies {
            background: #e74c3c;
            color: white;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .hero {
                padding: 8rem 1rem 5rem;
                margin-top: 60px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 60px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 60px);
                background: white;
                flex-direction: column;
                align-items: center;
                padding-top: 2rem;
                transition: left 0.3s;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 1rem 0;
            }
            
            .donation-options {
                flex-direction: column;
            }
        }
    </style>
    
    <!-- Full CSS (loaded asynchronously) -->
    <link rel="stylesheet" href="styles.css" media="print" onload="this.media='all'">
    
    <!-- Schema.org markup -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "NGO",
      "name": "HumanityLove",
      "url": "https://humanitylove.org",
      "logo": "https://humanitylove.org/logo.png",
      "description": "Spreading compassion worldwide through charitable actions",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "123 Charity Lane",
        "addressLocality": "New York",
        "addressRegion": "NY",
        "postalCode": "10001",
        "addressCountry": "US"
      },
      "funder": {
        "@type": "Organization",
        "name": "HumanityLove Donors"
      }
    }
    </script>
</head>
<body class="loading">
    <!-- Cookie Consent -->
    <div class="cookie-consent" id="cookieConsent">
        <p>We use cookies to enhance your experience. By continuing, you agree to our <a href="/privacy">Privacy Policy</a>.</p>
        <button id="acceptCookies">Accept</button>
        <button id="rejectCookies">Reject</button>
    </div>
    
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="/" class="logo">HumanityLove</a>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#about">About</a></li>
                    <li><a href="#impact">Impact</a></li>
                    <li><a href="#donate">Donate</a></li>
                    <li><a href="#videos">Videos</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Spread Love, Change Lives</h1>
            <p>Every donation helps us create real impact in communities worldwide. Join our movement of compassion today.</p>
            <a href="#donate" class="cta-button">Donate Now</a>
        </div>
    </section>
    
    <!-- Why Donate Section -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">Why Your Donation Matters</h2>
            <div class="reasons-grid">
                <div class="reason-card">
                    <i class="fas fa-heart"></i>
                    <h3>Direct Impact</h3>
                    <p>90% of funds go directly to programs helping people in need</p>
                </div>
                <div class="reason-card">
                    <i class="fas fa-chart-line"></i>
                    <h3>Measurable Results</h3>
                    <p>See exactly how your contribution makes a difference</p>
                </div>
                <div class="reason-card">
                    <i class="fas fa-globe"></i>
                    <h3>Global Reach</h3>
                    <p>We operate in 15 countries across 3 continents</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Progress Section -->
    <section class="section" id="impact">
        <div class="container">
            <h2 class="section-title">Our Impact So Far</h2>
            <div class="progress-stats">
                <div class="stat">
                    <div class="number" id="people-helped">10,000+</div>
                    <div class="label">People Helped</div>
                </div>
                <div class="stat">
                    <div class="number" id="projects-completed">47</div>
                    <div class="label">Projects Completed</div>
                </div>
                <div class="stat">
                    <div class="number" id="donations">$250,000+</div>
                    <div class="label">Raised</div>
                </div>
            </div>
            <div class="progress-bar">
                <div class="current-progress" style="width: 65%;">
                    <span>Current Project: 65% Funded</span>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Video Gallery Section -->
    <section class="section" id="videos">
        <div class="container">
            <h2 class="section-title">See Our Work in Action</h2>
            <div class="video-container">
                <div class="video-card">
                    <iframe src="https://www.youtube-nocookie.com/embed/your-video-id" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <h3>School Building in Kenya</h3>
                </div>
                <div class="video-card">
                    <iframe src="https://www.youtube-nocookie.com/embed/your-video-id" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <h3>Food Distribution in India</h3>
                </div>
            </div>
            <button class="load-more">View More Videos</button>
        </div>
    </section>
    
    <!-- Donation Portal -->
    <section class="section" id="donate">
        <div class="container">
            <h2 class="section-title">Make a Difference Today</h2>
            <div class="donation-options">
                <div class="amount-options">
                    <h3>Select Amount</h3>
                    <button class="amount-btn" data-amount="25">$25</button>
                    <button class="amount-btn" data-amount="50">$50</button>
                    <button class="amount-btn" data-amount="100">$100</button>
                    <button class="amount-btn" data-amount="250">$250</button>
                    <div class="custom-amount">
                        <span>$</span>
                        <input type="number" id="custom-amount" placeholder="Other amount">
                    </div>
                </div>
                <form id="donation-form">
                    <div class="form-group">
                        <label for="name">Full Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="payment">Payment Method</label>
                        <select id="payment" required>
                            <option value="">Select payment method</option>
                            <option value="credit">Credit Card</option>
                            <option value="paypal">PayPal</option>
                            <option value="bank">Bank Transfer</option>
                        </select>
                    </div>
                    <button type="submit" class="donate-btn">Donate Now</button>
                </form>
            </div>
            <div class="security-badges">
                <img src="ssl-secure.png" alt="SSL Secure" loading="lazy">
                <img src="pci-compliant.png" alt="PCI Compliant" loading="lazy">
            </div>
        </div>
    </section>
    
    <!-- Social Media Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">Join Our Community</h2>
            <div class="social-icons">
                <a href="https://facebook.com/yourpage" target="_blank" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="https://twitter.com/yourhandle" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="https://instagram.com/yourprofile" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="https://youtube.com/yourchannel" target="_blank" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
                <a href="https://linkedin.com/yourcompany" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
            </div>
            <div class="social-share">
                <p>Help us spread the word:</p>
                <button class="share-btn facebook"><i class="fab fa-facebook"></i> Share</button>
                <button class="share-btn twitter"><i class="fab fa-twitter"></i> Tweet</button>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-links">
                <a href="/about">About Us</a>
                <a href="/projects">Our Projects</a>
                <a href="/financials">Financial Reports</a>
                <a href="/blog">Blog</a>
                <a href="/contact">Contact</a>
                <a href="/privacy">Privacy Policy</a>
                <a href="/terms">Terms of Service</a>
            </div>
            <p class="copyright">© 2023 HumanityLove. All rights reserved.</p>
        </div>
    </footer>
    
    <!-- JavaScript -->
    <script>
        // Wait for DOM to load
        document.addEventListener('DOMContentLoaded', function() {
            // Show page content
            document.body.classList.remove('loading');
            document.body.classList.add('loaded');
            
            // Mobile menu toggle
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const navLinks = document.getElementById('navLinks');
            
            mobileMenuBtn.addEventListener('click', function() {
                navLinks.classList.toggle('active');
                this.innerHTML = navLinks.classList.contains('active') ? 
                    '<i class="fas fa-times"></i>' : '<i class="fas
