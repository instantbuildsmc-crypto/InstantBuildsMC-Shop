# InstantBuildsMC-Shop
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InstantBuildsMC | Premium Minecraft Builds Delivered Fast</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Outfit:wght@500;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* ================= VARIABLES & RESET ================= */
        :root {
            --bg: #09090b;
            --surface: #18181b;
            --surface-hover: #27272a;
            --primary: #00ff88;
            --primary-glow: rgba(0, 255, 136, 0.3);
            --secondary: #8b5cf6;
            --text: #f4f4f5;
            --text-muted: #a1a1aa;
            --border: #27272a;
            --font-head: 'Outfit', sans-serif;
            --font-body: 'Inter', sans-serif;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: var(--font-body);
            line-height: 1.6;
            overflow-x: hidden;
        }

        ::selection {
            background: var(--primary);
            color: var(--bg);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: var(--bg); }
        ::-webkit-scrollbar-thumb { background: var(--surface-hover); border-radius: 5px; }
        ::-webkit-scrollbar-thumb:hover { background: var(--primary); }

        /* ================= TYPOGRAPHY & UTILITIES ================= */
        h1, h2, h3, h4 { font-family: var(--font-head); font-weight: 700; line-height: 1.1; }
        h1 { font-size: clamp(2.5rem, 5vw, 4.5rem); font-weight: 900; letter-spacing: -1px; }
        h2 { font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 1rem; }
        h3 { font-size: 1.5rem; margin-bottom: 0.5rem; }
        p { color: var(--text-muted); font-size: 1.1rem; }
        
        .container { max-width: 1200px; margin: 0 auto; padding: 0 2rem; }
        .text-center { text-align: center; }
        .highlight { color: var(--primary); }
        .section-padding { padding: 6rem 0; }

        /* ================= BUTTONS ================= */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            padding: 1rem 2rem;
            font-family: var(--font-head);
            font-weight: 700;
            font-size: 1.1rem;
            border-radius: 4px;
            text-decoration: none;
            transition: var(--transition);
            cursor: pointer;
            border: none;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn-primary {
            background: var(--primary);
            color: var(--bg);
            box-shadow: 0 0 20px var(--primary-glow);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 30px var(--primary-glow);
            background: #00e077;
        }

        .btn-secondary {
            background: transparent;
            color: var(--text);
            border: 2px solid var(--border);
        }

        .btn-secondary:hover {
            border-color: var(--text);
            background: rgba(255, 255, 255, 0.05);
        }

        /* ================= HEADER ================= */
        header {
            position: fixed;
            top: 0; left: 0; right: 0;
            z-index: 1000;
            background: rgba(9, 9, 11, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            transition: var(--transition);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-family: var(--font-head);
            font-size: 1.5rem;
            font-weight: 900;
            color: var(--text);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo i { color: var(--primary); }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }

        .nav-links a:hover { color: var(--primary); }

        /* ================= HERO SECTION ================= */
        #hero {
            padding: 12rem 0 8rem;
            position: relative;
            background: radial-gradient(circle at 50% 0%, rgba(139, 92, 246, 0.15), transparent 50%),
                        radial-gradient(circle at 50% 100%, rgba(0, 255, 136, 0.1), transparent 50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        #hero p { max-width: 600px; margin: 1.5rem auto 2.5rem; font-size: 1.25rem; }
        
        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
        }

        /* ================= TRUST BAR ================= */
        #trust {
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
            background: var(--surface);
            padding: 2rem 0;
        }

        .trust-grid {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .trust-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .stars i { color: #fbbf24; }
        .trust-item span { font-weight: 600; font-family: var(--font-head); font-size: 1.2rem;}

        /* ================= SERVICES ================= */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 8px;
            padding: 2rem;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .card-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .card-price {
            margin-top: 1rem;
            font-family: var(--font-head);
            font-weight: 700;
            color: var(--text);
            font-size: 1.2rem;
        }

        .card .btn { margin-top: 1.5rem; width: 100%; font-size: 1rem; padding: 0.75rem;}

        /* ================= PORTFOLIO ================= */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .portfolio-item {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            aspect-ratio: 16/9;
            background: var(--surface-hover);
            group: hover;
        }

        /* Abstract CSS backgrounds to simulate impressive builds */
        .bg-1 { background: linear-gradient(45deg, #1a1a2e, #16213e); }
        .bg-2 { background: linear-gradient(135deg, #0f2027, #203a43, #2c5364); }
        .bg-3 { background: linear-gradient(to right, #141e30, #243b55); }
        .bg-4 { background: linear-gradient(to bottom, #000000, #434343); }

        .portfolio-overlay {
            position: absolute;
            inset: 0;
            background: rgba(9, 9, 11, 0.9);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: var(--transition);
        }

        .portfolio-item:hover .portfolio-overlay { opacity: 1; }

        /* ================= HOW IT WORKS & WHY US ================= */
        .step-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
            position: relative;
        }

        .step {
            text-align: center;
            padding: 2rem;
            background: var(--surface);
            border-radius: 8px;
            border: 1px solid var(--border);
        }

        .step-num {
            width: 50px;
            height: 50px;
            background: var(--primary);
            color: var(--bg);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 900;
            margin: 0 auto 1.5rem;
            font-family: var(--font-head);
        }

        /* ================= TESTIMONIALS ================= */
        .testimonial-card {
            background: var(--surface);
            border: 1px solid var(--border);
            padding: 2rem;
            border-radius: 8px;
        }

        .user-info {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .avatar {
            width: 50px; height: 50px;
            border-radius: 50%;
            background: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        /* ================= PRICING ================= */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
            align-items: center;
        }

        .pricing-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 8px;
            padding: 3rem 2rem;
            text-align: center;
            position: relative;
        }

        .pricing-card.popular {
            border-color: var(--primary);
            transform: scale(1.05);
            box-shadow: 0 0 30px rgba(0, 255, 136, 0.1);
            background: linear-gradient(180deg, var(--surface) 0%, rgba(0, 255, 136, 0.05) 100%);
        }

        .badge {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            color: var(--bg);
            padding: 0.25rem 1rem;
            border-radius: 20px;
            font-weight: 700;
            font-size: 0.8rem;
            text-transform: uppercase;
        }

        .price {
            font-size: 3rem;
            font-family: var(--font-head);
            font-weight: 900;
            color: var(--text);
            margin: 1.5rem 0;
        }

        .features { list-style: none; margin: 2rem 0; text-align: left; }
        .features li { margin-bottom: 1rem; display: flex; gap: 0.5rem; align-items: center; }
        .features i { color: var(--primary); }

        /* ================= FAQ ================= */
        .faq-container {
            max-width: 800px;
            margin: 3rem auto 0;
        }

        details {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 8px;
            margin-bottom: 1rem;
            overflow: hidden;
        }

        summary {
            padding: 1.5rem;
            font-family: var(--font-head);
            font-weight: 700;
            font-size: 1.2rem;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        summary::-webkit-details-marker { display: none; }
        summary::after {
            content: '\f067'; /* FontAwesome plus */
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            color: var(--primary);
            transition: var(--transition);
        }

        details[open] summary::after { content: '\f068'; /* FontAwesome minus */ }
        details[open] summary { border-bottom: 1px solid var(--border); }
        details p { padding: 1.5rem; margin: 0; }

        /* ================= FINAL CTA & FOOTER ================= */
        #cta {
            background: linear-gradient(45deg, var(--surface), rgba(139, 92, 246, 0.2));
            border-top: 1px solid var(--secondary);
            border-bottom: 1px solid var(--secondary);
            text-align: center;
        }

        footer {
            background: var(--bg);
            padding: 4rem 0 2rem;
            border-top: 1px solid var(--border);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-col h4 { margin-bottom: 1.5rem; }
        .footer-col ul { list-style: none; }
        .footer-col a { color: var(--text-muted); text-decoration: none; transition: var(--transition); display: block; margin-bottom: 0.5rem; }
        .footer-col a:hover { color: var(--primary); }
        .copyright { text-align: center; color: var(--text-muted); border-top: 1px solid var(--border); padding-top: 2rem; }

        /* ================= RESPONSIVE ================= */
        @media (max-width: 992px) {
            .pricing-grid, .step-grid { grid-template-columns: 1fr; }
            .pricing-card.popular { transform: none; }
            .nav-links { display: none; } /* Mobile menu simplified for snippet */
        }
        @media (max-width: 768px) {
            .hero-buttons { flex-direction: column; }
            .trust-grid { justify-content: center; }
            #hero { padding: 8rem 0 4rem; }
        }
    </style>
</head>
<body>

    <header id="header">
        <div class="container">
            <nav>
                <a href="#" class="logo"><i class="fa-solid fa-cube"></i> InstantBuildsMC</a>
                <ul class="nav-links">
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#how-it-works">How it Works</a></li>
                    <li><a href="#faq">FAQ</a></li>
                </ul>
                <a href="#services" class="btn btn-primary" style="padding: 0.5rem 1.5rem; font-size: 0.9rem;">Order Now</a>
            </nav>
        </div>
    </header>

    <section id="hero">
        <div class="container">
            <h1>Premium Minecraft Builds.<br><span class="highlight">Delivered Instantly.</span></h1>
            <p>Get stunning, professional maps for your server without the hassle. Stop waiting weeks for unreliable builders. Launch your community today.</p>
            <div class="hero-buttons">
                <a href="#services" class="btn btn-primary"><i class="fa-solid fa-bolt"></i> Get Your Build</a>
                <a href="#portfolio" class="btn btn-secondary">View Portfolio</a>
            </div>
            <p style="font-size: 0.9rem; color: var(--text-muted); margin-top: 0;"><i class="fa-solid fa-circle-check" style="color: var(--primary);"></i> 500+ Servers Launched</p>
        </div>
    </section>

    <section id="trust">
        <div class="container trust-grid">
            <div class="trust-item">
                <div class="stars">
                    <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                </div>
                <span>4.9/5 on Trustpilot</span>
            </div>
            <div class="trust-item">
                <i class="fa-solid fa-shield-halved" style="color: var(--secondary); font-size: 1.5rem;"></i>
                <span>100% Quality Guarantee</span>
            </div>
            <div class="trust-item">
                <i class="fa-solid fa-clock-rotate-left" style="color: var(--primary); font-size: 1.5rem;"></i>
                <span>24-72h Delivery</span>
            </div>
        </div>
    </section>

    <section id="services" class="section-padding">
        <div class="container">
            <div class="text-center">
                <h2>Our <span class="highlight">Build Services</span></h2>
                <p>Choose from our premium categories. Optimized for performance and player retention.</p>
            </div>
            <div class="grid-3">
                <div class="card">
                    <i class="fa-solid fa-chess-rook card-icon"></i>
                    <h3>Server Spawns</h3>
                    <p>High-FPS, visually stunning starting zones that give your players the perfect first impression.</p>
                    <div class="card-price">Starting at $29</div>
                    <a href="#pricing" class="btn btn-secondary">Browse Spawns</a>
                </div>
                <div class="card">
                    <i class="fa-solid fa-khanda card-icon"></i>
                    <h3>PvP & Minigame Maps</h3>
                    <p>Symmetrical, balanced arenas designed for competitive gameplay (Skywars, Bedwars, Duels).</p>
                    <div class="card-price">Starting at $19</div>
                    <a href="#pricing" class="btn btn-secondary">Browse Maps</a>
                </div>
                <div class="card">
                    <i class="fa-solid fa-hammer card-icon"></i>
                    <h3>Custom Commissions</h3>
                    <p>Have a unique vision? Our pro build team will construct it exactly to your server's specifications.</p>
                    <div class="card-price">Starting at $99</div>
                    <a href="#pricing" class="btn btn-primary">Open Ticket</a>
                </div>
            </div>
        </div>
    </section>

    <section id="portfolio" class="section-padding" style="background: var(--surface);">
        <div class="container">
            <div class="text-center">
                <h2>Recent <span class="highlight">Masterpieces</span></h2>
                <p>Don't just take our word for it. See the quality for yourself.</p>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item bg-1">
                    <div class="portfolio-overlay">
                        <h3>Cyberpunk Hub</h3>
                        <p>150x150</p>
                    </div>
                </div>
                <div class="portfolio-item bg-2">
                    <div class="portfolio-overlay">
                        <h3>Fantasy Skyblock</h3>
                        <p>200x200</p>
                    </div>
                </div>
                <div class="portfolio-item bg-3">
                    <div class="portfolio-overlay">
                        <h3>Medieval Factions</h3>
                        <p>300x300</p>
                    </div>
                </div>
                <div class="portfolio-item bg-4">
                    <div class="portfolio-overlay">
                        <h3>Gladiator PvP Arena</h3>
                        <p>100x100</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="how-it-works" class="section-padding">
        <div class="container">
            <div class="text-center">
                <h2>How It <span class="highlight">Works</span></h2>
                <p>A frictionless process to get your server online faster.</p>
            </div>
            <div class="step-grid">
                <div class="step">
                    <div class="step-num">1</div>
                    <h3>Choose Your Build</h3>
                    <p>Browse our catalog of premium pre-mades or select a custom commission tier.</p>
                </div>
                <div class="step">
                    <div class="step-num">2</div>
                    <h3>Specify Details</h3>
                    <p>Tell us your server version, required NPCs spots, and color preferences via Discord.</p>
                </div>
                <div class="step">
                    <div class="step-num">3</div>
                    <h3>Instant Delivery</h3>
                    <p>Download your schematic or world file instantly, ready to be pasted into your server.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="pricing" class="section-padding" style="background: var(--surface);">
        <div class="container">
            <div class="text-center">
                <h2>Simple, Transparent <span class="highlight">Pricing</span></h2>
                <p>No hidden fees. Full ownership rights included.</p>
            </div>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>Pre-Made Map</h3>
                    <div class="price">$29</div>
                    <p>Perfect for new servers on a budget.</p>
                    <ul class="features">
                        <li><i class="fa-solid fa-check"></i> Instant Download</li>
                        <li><i class="fa-solid fa-check"></i> Schematic + World File</li>
                        <li><i class="fa-solid fa-check"></i> 1.8 to 1.20+ Support</li>
                        <li><i class="fa-solid fa-xmark" style="color: var(--text-muted);"></i> Custom Modifications</li>
                    </ul>
                    <a href="#" class="btn btn-secondary">Browse Store</a>
                </div>
                <div class="pricing-card popular">
                    <div class="badge">Best Value</div>
                    <h3>Semi-Custom</h3>
                    <div class="price">$79</div>
                    <p>A premium pre-made, edited to fit your brand.</p>
                    <ul class="features">
                        <li><i class="fa-solid fa-check"></i> Delivery in 24 Hours</li>
                        <li><i class="fa-solid fa-check"></i> Custom Logo Integration</li>
                        <li><i class="fa-solid fa-check"></i> Layout Adjustments</li>
                        <li><i class="fa-solid fa-check"></i> Dedicated Support Ticket</li>
                    </ul>
                    <a href="#" class="btn btn-primary">Start Order</a>
                </div>
                <div class="pricing-card">
                    <h3>Full Custom</h3>
                    <div class="price">$149+</div>
                    <p>Built from scratch exclusively for you.</p>
                    <ul class="features">
                        <li><i class="fa-solid fa-check"></i> 100% Unique Design</li>
                        <li><i class="fa-solid fa-check"></i> Unlimited Revisions</li>
                        <li><i class="fa-solid fa-check"></i> Progress Updates</li>
                        <li><i class="fa-solid fa-check"></i> Exclusive Resell Rights</li>
                    </ul>
                    <a href="#" class="btn btn-secondary">Get a Quote</a>
                </div>
            </div>
        </div>
    </section>

    <section class="section-padding">
        <div class="container">
            <div class="text-center">
                <h2>Trusted by <span class="highlight">Creators</span></h2>
            </div>
            <div class="grid-3">
                <div class="testimonial-card">
                    <p>"InstantBuildsMC saved our launch. We needed a Factions spawn in 48 hours and they delivered a masterpiece. Player retention is up 20%."</p>
                    <div class="user-info">
                        <div class="avatar">V</div>
                        <div>
                            <h4>VoidNetwork</h4>
                            <p style="font-size: 0.9rem; margin: 0;">500+ CCU Server</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"Tired of getting scammed on Fiverr. These guys are the real deal. Clean file formats, no lag, and the neon aesthetics are crazy."</p>
                    <div class="user-info">
                        <div class="avatar" style="background: var(--primary); color: var(--bg);">S</div>
                        <div>
                            <h4>SkyblockPro</h4>
                            <p style="font-size: 0.9rem; margin: 0;">Server Owner</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"Used them for my YouTuber SMP. The custom spawn point they made was the highlight of episode 1. Highly recommend!"</p>
                    <div class="user-info">
                        <div class="avatar" style="background: #3b82f6;">J</div>
                        <div>
                            <h4>JPlayz</h4>
                            <p style="font-size: 0.9rem; margin: 0;">Content Creator</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="faq" class="section-padding" style="background: var(--surface);">
        <div class="container">
            <div class="text-center">
                <h2>Frequently Asked <span class="highlight">Questions</span></h2>
            </div>
            <div class="faq-container">
                <details open>
                    <summary>How long does delivery take?</summary>
                    <p>Pre-made maps are delivered <strong>instantly</strong> via automated email and dashboard download. Custom commissions typically take between 24 to 72 hours depending on the size and complexity.</p>
                </details>
                <details>
                    <summary>What file formats do I receive?</summary>
                    <p>You will receive both a `.schematic` (or `.schem`) file for WorldEdit/FAWE, and a standard Minecraft world save folder. This ensures compatibility with any setup.</p>
                </details>
                <details>
                    <summary>Are these builds optimized for servers?</summary>
                    <p>Yes. All our builds are created void-world, block-optimized, and checked to ensure there are no entities or lag-inducing blocks that could hurt your server's TPS.</p>
                </details>
                <details>
                    <summary>Do you offer refunds?</summary>
                    <p>Due to the digital nature of the files, pre-mades are non-refundable. However, for custom builds, we offer unlimited revisions during the building phase to ensure you are 100% satisfied before final delivery.</p>
                </details>
            </div>
        </div>
    </section>

    <section id="cta" class="section-padding">
        <div class="container text-center">
            <h2 style="font-size: clamp(2.5rem, 4vw, 3.5rem);">Ready to Level Up Your Server?</h2>
            <p style="max-width: 500px; margin: 0 auto 2rem; color: var(--text);">Join hundreds of successful server owners who trust InstantBuildsMC.</p>
            <a href="#" class="btn btn-primary" style="font-size: 1.25rem; padding: 1.2rem 3rem;">
                <i class="fa-brands fa-discord"></i> Open a Ticket Now
            </a>
            <p style="margin-top: 1rem; font-size: 0.9rem; font-weight: 700; color: var(--primary);">⚠️ Only 3 custom build slots remaining this week.</p>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <a href="#" class="logo" style="margin-bottom: 1rem;"><i class="fa-solid fa-cube"></i> InstantBuildsMC</a>
                    <p style="font-size: 0.9rem;">Premium Minecraft architecture. Built for performance, designed for players.</p>
                </div>
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#portfolio">Portfolio</a></li>
                        <li><a href="#pricing">Pricing</a></li>
                        <li><a href="#faq">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Legal</h4>
                    <ul>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Refund Policy</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Connect</h4>
                    <ul>
                        <li><a href="#"><i class="fa-brands fa-discord"></i> Discord Server</a></li>
                        <li><a href="#"><i class="fa-brands fa-twitter"></i> Twitter / X</a></li>
                        <li><a href="#"><i class="fa-brands fa-youtube"></i> YouTube</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2026 InstantBuildsMC. Not affiliated with Mojang AB or Microsoft.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth FAQ Accordion Behavior (Closes others when one is opened)
        const detailsElements = document.querySelectorAll("details");
        detailsElements.forEach((targetDetail) => {
            targetDetail.addEventListener("click", () => {
                detailsElements.forEach((detail) => {
                    if (detail !== targetDetail) {
                        detail.removeAttribute("open");
                    }
                });
            });
        });

        // Header Scroll Effect
        const header = document.getElementById('header');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                header.style.background = 'rgba(9, 9, 11, 0.95)';
                header.style.boxShadow = '0 4px 30px rgba(0, 0, 0, 0.5)';
            } else {
                header.style.background = 'rgba(9, 9, 11, 0.8)';
                header.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>
