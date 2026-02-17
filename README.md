<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAM BILTONG | Northern Irish Biltong</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0a0a0a;
            --bg-secondary: #111111;
            --text-primary: #ffffff;
            --text-secondary: #888888;
            --accent-gold: #d4af37;
            --accent-gold-light: #f4d03f;
            --border-color: #222222;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: linear-gradient(to bottom, rgba(0,0,0,0.9), transparent);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: 2px;
            color: var(--text-primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.85rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent-gold);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            position: relative;
            background: radial-gradient(circle at center, #1a1a1a 0%, #0a0a0a 100%);
        }

        .hero-logo {
            width: 300px;
            height: 300px;
            margin-bottom: 2rem;
            filter: drop-shadow(0 0 30px rgba(212, 175, 55, 0.3));
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 900;
            letter-spacing: 8px;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .hero-subtitle {
            font-size: 1.2rem;
            color: var(--accent-gold);
            letter-spacing: 4px;
            margin-bottom: 1.5rem;
            text-transform: uppercase;
        }

        .hero-tagline {
            font-size: 1.1rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin-bottom: 3rem;
            line-height: 1.8;
        }

        .origin-badge {
            display: inline-block;
            padding: 0.8rem 2rem;
            border: 1px solid var(--border-color);
            font-size: 0.8rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            color: var(--text-secondary);
            margin-bottom: 4rem;
        }

        /* Next Drop Section */
        .next-drop {
            background: var(--bg-secondary);
            padding: 6rem 5%;
            text-align: center;
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
        }

        .section-label {
            font-size: 0.8rem;
            letter-spacing: 4px;
            color: var(--accent-gold);
            text-transform: uppercase;
            margin-bottom: 1rem;
        }

        .batch-title {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .batch-subtitle {
            color: var(--text-secondary);
            font-size: 1.1rem;
        }

        /* Lineup Section */
        .lineup {
            padding: 6rem 5%;
            text-align: center;
        }

        .lineup h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .lineup-description {
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto 4rem;
            font-size: 1.1rem;
        }

        .flavors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .flavor-card {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            padding: 3rem 2rem;
            transition: transform 0.3s, border-color 0.3s;
            cursor: pointer;
        }

        .flavor-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent-gold);
        }

        .flavor-number {
            font-size: 3rem;
            font-weight: 900;
            color: var(--accent-gold);
            opacity: 0.3;
            margin-bottom: 1rem;
        }

        .flavor-name {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .flavor-desc {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Origin Story Section */
        .origin {
            padding: 6rem 5%;
            background: var(--bg-secondary);
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
        }

        .origin-content h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            line-height: 1.2;
        }

        .origin-content p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .origin-content strong {
            color: var(--text-primary);
        }

        .origin-image {
            text-align: center;
        }

        .origin-image img {
            width: 100%;
            max-width: 400px;
            filter: drop-shadow(0 0 40px rgba(212, 175, 55, 0.2));
        }

        /* Stats Section */
        .stats {
            padding: 4rem 5%;
            text-align: center;
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
        }

        .stat-number {
            font-size: 4rem;
            font-weight: 900;
            color: var(--accent-gold);
            display: block;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.9rem;
        }

        /* Drop History */
        .history {
            padding: 6rem 5%;
            text-align: center;
        }

        .history h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .history-subtitle {
            color: var(--text-secondary);
            margin-bottom: 4rem;
        }

        .timeline {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }

        .timeline-item {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            padding: 2rem;
            margin-bottom: 2rem;
            text-align: left;
            position: relative;
            transition: border-color 0.3s;
        }

        .timeline-item:hover {
            border-color: var(--accent-gold);
        }

        .timeline-item.coming-soon {
            border-color: var(--accent-gold);
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.1), transparent);
        }

        .timeline-badge {
            position: absolute;
            top: -10px;
            right: 2rem;
            background: var(--accent-gold);
            color: var(--bg-primary);
            padding: 0.3rem 1rem;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .timeline-title {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .timeline-desc {
            color: var(--text-secondary);
        }

        /* Contact Section */
        .contact {
            padding: 6rem 5%;
            background: var(--bg-secondary);
            text-align: center;
        }

        .contact h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 900;
        }

        .contact-subtitle {
            color: var(--text-secondary);
            margin-bottom: 3rem;
            font-size: 1.1rem;
        }

        .contact-email {
            display: inline-block;
            color: var(--accent-gold);
            text-decoration: none;
            font-size: 1.5rem;
            letter-spacing: 2px;
            margin-bottom: 4rem;
            border-bottom: 2px solid transparent;
            transition: border-color 0.3s;
        }

        .contact-email:hover {
            border-color: var(--accent-gold);
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            text-align: left;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            font-size: 0.8rem;
            letter-spacing: 1px;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            background: var(--bg-primary);
            border: 1px solid var(--border-color);
            color: var(--text-primary);
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent-gold);
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        .submit-btn {
            width: 100%;
            padding: 1.2rem;
            background: var(--accent-gold);
            color: var(--bg-primary);
            border: none;
            font-size: 1rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        /* Footer */
        footer {
            padding: 3rem 5%;
            text-align: center;
            border-top: 1px solid var(--border-color);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: 2px;
            color: var(--text-primary);
            margin-bottom: 1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .origin {
                grid-template-columns: 1fr;
            }
            
            .nav-links {
                display: none;
            }
            
            .flavors-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s, transform 0.8s;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">RAM BILTONG</div>
        <ul class="nav-links">
            <li><a href="#lineup">Lineup</a></li>
            <li><a href="#origin">Origin</a></li>
            <li><a href="#history">Drops</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section class="hero">
        <img src="https://files.oaiusercontent.com/file-JQj9K1iB9qSHaXZqXvQ3tM?se=2025-12-31T23%3A59%3A59Z&sp=r&sv=2024-08-04&sr=b&rscc=max-age%3D299%2C%20immutable%2C%20private&rscd=attachment%3B%20filename%3Dfile-JQj9K1iB9qSHaXZqXvQ3tM&sig=placeholder" alt="RAM BILTONG Logo" class="hero-logo">
        <h1>RAM BILTONG</h1>
        <p class="hero-subtitle">Northern Irish Biltong</p>
        <p class="hero-tagline">Small batch. Air-dried. Made for those who demand more from their protein.</p>
        <div class="origin-badge">Made in Northern Ireland</div>
    </section>

    <section class="next-drop">
        <p class="section-label">Next Drop</p>
        <h2 class="batch-title">Batch 004</h2>
        <p class="batch-subtitle">Lamb Edition — Limited to 150 packs</p>
    </section>

    <section class="lineup" id="lineup">
        <h2>The Lineup</h2>
        <p class="lineup-description">Four flavours. Zero compromise. Each batch numbered, limited, and never repeated.</p>
        
        <div class="flavors-grid">
            <div class="flavor-card">
                <div class="flavor-number">01</div>
                <h3 class="flavor-name">The Original</h3>
                <p class="flavor-desc">Coriander seed, black pepper, and sea salt. The classic that started it all.</p>
            </div>
            <div class="flavor-card">
                <div class="flavor-number">02</div>
                <h3 class="flavor-name">Chilli & Garlic</h3>
                <p class="flavor-desc">Bird's eye chilli and roasted garlic. For those who like it hot.</p>
            </div>
            <div class="flavor-card">
                <div class="flavor-number">03</div>
                <h3 class="flavor-name">Smoked Paprika</h3>
                <p class="flavor-desc">Oak-smoked Spanish paprika with a hint of brown sugar.</p>
            </div>
            <div class="flavor-card">
                <div class="flavor-number">04</div>
                <h3 class="flavor-name">Lamb Edition</h3>
                <p class="flavor-desc">Rosemary and mint. Our first ever lamb biltong. Limited release.</p>
            </div>
        </div>
    </section>

    <section class="origin" id="origin">
        <div class="origin-content">
            <h2>Built Different.<br>Dried Better.</h2>
            <p>RAM BILTONG was born in a small kitchen in Belfast, out of frustration with mass-produced jerky that tasted like cardboard and packed more sugar than protein.</p>
            <p>We started with one simple rule: <strong>use the best Northern Irish beef and lamb, season it properly, and let time do the work.</strong></p>
            <p>No dehydrators blasting heat. No preservatives. No shortcuts. Just traditional air-drying methods that take 5-7 days per batch.</p>
            <p>Every batch is numbered. Every pack is hand-cut. And when it's gone, it's gone — until the next drop.</p>
        </div>
        <div class="origin-image">
            <img src="https://files.oaiusercontent.com/file-JQj9K1iB9qSHaXZqXvQ3tM?se=2025-12-31T23%3A59%3A59Z&sp=r&sv=2024-08-04&sr=b&rscc=max-age%3D299%2C%20immutable%2C%20private&rscd=attachment%3B%20filename%3Dfile-JQj9K1iB9qSHaXZqXvQ3tM&sig=placeholder" alt="RAM Logo">
        </div>
    </section>

    <section class="stats">
        <span class="stat-number">001-003</span>
        <span class="stat-label">Sold Out in 48 Hrs</span>
    </section>

    <section class="history" id="history">
        <h2>Drop History</h2>
        <p class="history-subtitle">Every batch tells a story. Here's where we've been.</p>
        
        <div class="timeline">
            <div class="timeline-item coming-soon">
                <span class="timeline-badge">Coming Soon</span>
                <h3 class="timeline-title">Batch 004</h3>
                <p class="timeline-desc">Lamb Edition — First ever lamb biltong from RAM</p>
            </div>
            <div class="timeline-item">
                <h3 class="timeline-title">Batch 003</h3>
                <p class="timeline-desc">Smoked Paprika — Sold out in 36 hours</p>
            </div>
            <div class="timeline-item">
                <h3 class="timeline-title">Batch 002</h3>
                <p class="timeline-desc">Chilli & Garlic — Sold out in 48 hours</p>
            </div>
            <div class="timeline-item">
                <h3 class="timeline-title">Batch 001</h3>
                <p class="timeline-desc">The Original — Sold out in 52 hours</p>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <h2>Get In<br>Touch.</h2>
        <p class="contact-subtitle">Wholesale inquiries, bulk orders, or just want to say hello? We're always listening.</p>
        
        <a href="mailto:hello@rambiltong.com" class="contact-email">HELLO@RAMBILTONG.COM</a>
        
        <form class="contact-form" onsubmit="event.preventDefault(); alert('Message sent!');">
            <div class="form-group">
                <label>Send a Message</label>
                <input type="text" placeholder="Your Name" required>
            </div>
            <div class="form-group">
                <input type="email" placeholder="Your Email" required>
            </div>
            <div class="form-group">
                <textarea placeholder="Your Message" required></textarea>
            </div>
            <button type="submit" class="submit-btn">Send Message</button>
        </form>
    </section>

    <footer>
        <div class="footer-logo">RAM BILTONG</div>
        <p>&copy; 2024 RAM BILTONG. All rights reserved.</p>
        <p style="margin-top: 0.5rem; font-size: 0.8rem;">Made in Northern Ireland</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Fade in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        // Add fade-in class to elements
        document.querySelectorAll('.flavor-card, .timeline-item, .origin-content, .origin-image').forEach(el => {
            el.classList.add('fade-in');
            observer.observe(el);
        });

        // Navbar background on scroll
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 100) {
                nav.style.background = 'rgba(10, 10, 10, 0.95)';
                nav.style.backdropFilter = 'blur(10px)';
            } else {
                nav.style.background = 'linear-gradient(to bottom, rgba(0,0,0,0.9), transparent)';
                nav.style.backdropFilter = 'none';
            }
        });
    </script>
</body>
</html>
