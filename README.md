<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SoundMarket - Grammy-winning music. Zero copyright strikes. Completely free.</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --coral: #FF6B47;
            --purple: #6B46C1;
            --neutral: #F7F5F3;
            --teal: #0F766E;
            --gold: #F59E0B;
            --white: #FFFFFF;
            --charcoal: #1F1F1F;
            --gray: #666666;
            --light-gray: #E5E5E5;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--charcoal);
            overflow-x: hidden;
        }
        
        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 1px 0 rgba(0,0,0,0.1);
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 72px;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--charcoal);
            text-decoration: none;
        }
        
        .nav-links {
            display: flex;
            gap: 32px;
            align-items: center;
        }
        
        .nav-links a {
            color: var(--charcoal);
            text-decoration: none;
            font-size: 16px;
            transition: color 0.2s;
        }
        
        .nav-links a:hover {
            color: var(--coral);
        }
        
        .nav-cta {
            background: var(--coral);
            color: white;
            padding: 10px 24px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.2s;
        }
        
        .nav-cta:hover {
            background: #E5532F;
            transform: translateY(-1px);
            box-shadow: 0 4px 12px rgba(255, 107, 71, 0.3);
        }
        
        /* Hero Section */
        .hero {
            padding: 120px 24px 80px;
            background: linear-gradient(135deg, var(--neutral) 0%, rgba(255, 107, 71, 0.05) 100%);
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 56px;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
            color: var(--charcoal);
        }
        
        .hero-highlight {
            color: var(--coral);
        }
        
        .hero-subhead {
            font-size: 22px;
            color: var(--gray);
            margin-bottom: 40px;
            line-height: 1.5;
        }
        
        .hero-ctas {
            display: flex;
            gap: 16px;
            justify-content: center;
            margin-bottom: 16px;
        }
        
        .btn-primary {
            background: var(--coral);
            color: white;
            padding: 16px 32px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: all 0.2s;
            display: inline-block;
        }
        
        .btn-primary:hover {
            background: #E5532F;
            transform: translateY(-2px);
            box-shadow: 0 8px 24px rgba(255, 107, 71, 0.3);
        }
        
        .btn-secondary {
            background: transparent;
            color: var(--purple);
            padding: 16px 32px;
            border: 2px solid var(--purple);
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: all 0.2s;
            display: inline-block;
        }
        
        .btn-secondary:hover {
            background: var(--purple);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 8px 24px rgba(107, 70, 193, 0.3);
        }
        
        .hero-meta {
            font-size: 14px;
            color: var(--gray);
            margin-bottom: 8px;
        }
        
        .why-free-link {
            font-size: 14px;
            color: var(--purple);
            text-decoration: none;
            transition: color 0.2s;
        }
        
        .why-free-link:hover {
            color: var(--coral);
            text-decoration: underline;
        }
        
        /* Trust Strip */
        .trust-strip {
            background: white;
            padding: 40px 24px;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .trust-container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            text-align: center;
        }
        
        .trust-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
        }
        
        .trust-icon {
            width: 40px;
            height: 40px;
            background: var(--gold);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
        }
        
        .trust-label {
            font-weight: 600;
            color: var(--charcoal);
        }
        
        .trust-sublabel {
            font-size: 14px;
            color: var(--gray);
        }
        
        /* How It Works */
        .how-it-works {
            padding: 80px 24px;
            background: var(--neutral);
        }
        
        .section-header {
            text-align: center;
            max-width: 600px;
            margin: 0 auto 60px;
        }
        
        .section-header h2 {
            font-size: 40px;
            margin-bottom: 16px;
            color: var(--charcoal);
        }
        
        .section-header p {
            font-size: 18px;
            color: var(--gray);
        }
        
        .steps-container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }
        
        .step {
            background: white;
            padding: 40px 32px;
            border-radius: 12px;
            text-align: center;
            position: relative;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .step:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }
        
        .step-number {
            width: 48px;
            height: 48px;
            background: var(--coral);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 20px;
            margin: 0 auto 24px;
        }
        
        .step h3 {
            font-size: 24px;
            margin-bottom: 12px;
            color: var(--charcoal);
        }
        
        .step p {
            color: var(--gray);
            line-height: 1.6;
        }
        
        /* Content Fit */
        .content-fit {
            padding: 80px 24px;
            background: white;
        }
        
        .playlists-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 24px;
        }
        
        .playlist-card {
            background: var(--neutral);
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
            transition: all 0.2s;
            text-align: center;
        }
        
        .playlist-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }
        
        .playlist-cover {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--purple) 0%, var(--coral) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
        }
        
        .playlist-info {
            padding: 20px;
        }
        
        .playlist-title {
            font-weight: 600;
            margin-bottom: 4px;
            color: var(--charcoal);
        }
        
        .playlist-count {
            font-size: 14px;
            color: var(--gray);
        }
        
        /* Music Quality */
        .music-quality {
            padding: 80px 24px;
            background: linear-gradient(135deg, rgba(107, 70, 193, 0.05) 0%, rgba(255, 107, 71, 0.05) 100%);
        }
        
        .award-badge {
            position: absolute;
            top: 12px;
            right: 12px;
            background: var(--gold);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .music-grid {
            max-width: 1200px;
            margin: 0 auto 60px;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 24px;
        }
        
        .track-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            transition: all 0.2s;
            cursor: pointer;
            position: relative;
        }
        
        .track-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }
        
        .track-artwork {
            width: 100%;
            height: 180px;
            background: linear-gradient(135deg, var(--purple) 0%, var(--coral) 100%);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .play-button {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: all 0.2s;
        }
        
        .track-card:hover .play-button {
            transform: scale(1.1);
            background: white;
        }
        
        .track-info {
            padding: 20px;
        }
        
        .track-title {
            font-weight: 600;
            margin-bottom: 4px;
            color: var(--charcoal);
        }
        
        .track-artist {
            color: var(--gray);
            font-size: 14px;
            margin-bottom: 8px;
        }
        
        .track-feature {
            font-size: 12px;
            color: var(--purple);
            font-weight: 500;
        }
        
        .featured-in {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }
        
        .featured-in h3 {
            font-size: 18px;
            color: var(--gray);
            margin-bottom: 24px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .tv-logos {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 48px;
            flex-wrap: wrap;
            opacity: 0.7;
            filter: grayscale(100%);
            transition: all 0.3s;
        }
        
        .tv-logos:hover {
            opacity: 1;
            filter: grayscale(0%);
        }
        
        .tv-logo {
            height: 40px;
            font-size: 24px;
            font-weight: 700;
            color: var(--gray);
        }
        
        /* Agencies & Brands */
        .agencies-brands {
            padding: 80px 24px;
            background: white;
        }
        
        .enterprise-features {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .feature-card {
            text-align: center;
            padding: 40px;
        }
        
        .feature-icon {
            width: 64px;
            height: 64px;
            background: var(--teal);
            color: white;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            margin: 0 auto 24px;
        }
        
        .feature-card h3 {
            font-size: 24px;
            margin-bottom: 12px;
            color: var(--charcoal);
        }
        
        .feature-card p {
            color: var(--gray);
            line-height: 1.6;
        }
        
        .enterprise-cta {
            text-align: center;
            margin-top: 48px;
        }
        
        /* Pricing */
        .pricing-section {
            padding: 80px 24px;
            background: var(--neutral);
        }
        
        .pricing-container {
            max-width: 800px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 32px;
        }
        
        .pricing-card {
            background: white;
            padding: 48px 40px;
            border-radius: 12px;
            text-align: center;
            position: relative;
            transition: all 0.2s;
        }
        
        .pricing-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 16px 32px rgba(0,0,0,0.1);
        }
        
        .plan-name {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 8px;
            color: var(--charcoal);
        }
        
        .plan-price {
            font-size: 20px;
            color: var(--gray);
            margin-bottom: 24px;
        }
        
        .plan-features {
            list-style: none;
            margin-bottom: 32px;
            text-align: left;
        }
        
        .plan-features li {
            padding: 12px 0;
            color: var(--charcoal);
            position: relative;
            padding-left: 28px;
        }
        
        .plan-features li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--teal);
            font-weight: 700;
        }
        
        .popular-badge {
            position: absolute;
            top: -12px;
            right: 24px;
            background: var(--gold);
            color: white;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
        }
        
        /* Success Stories */
        .success-stories {
            padding: 80px 24px;
            background: white;
        }
        
        .testimonials-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 32px;
        }
        
        .testimonial {
            background: var(--neutral);
            padding: 32px;
            border-radius: 12px;
            position: relative;
        }
        
        .quote {
            font-size: 18px;
            color: var(--charcoal);
            margin-bottom: 24px;
            line-height: 1.6;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 16px;
        }
        
        .author-avatar {
            width: 48px;
            height: 48px;
            background: var(--purple);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
        }
        
        .author-info {
            flex: 1;
        }
        
        .author-name {
            font-weight: 600;
            color: var(--charcoal);
        }
        
        .author-channel {
            font-size: 14px;
            color: var(--gray);
        }
        
        /* CTA Section */
        .cta-section {
            padding: 100px 24px;
            background: var(--charcoal);
            color: white;
            text-align: center;
        }
        
        .cta-content {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .cta-content h2 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .cta-content p {
            font-size: 20px;
            margin-bottom: 40px;
            opacity: 0.9;
        }
        
        .cta-button {
            background: var(--coral);
            color: white;
            padding: 20px 48px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 20px;
            display: inline-block;
            transition: all 0.2s;
        }
        
        .cta-button:hover {
            background: #E5532F;
            transform: translateY(-2px);
            box-shadow: 0 12px 32px rgba(255, 107, 71, 0.4);
        }
        
        /* Footer */
        footer {
            background: var(--neutral);
            padding: 60px 24px 40px;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h4 {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 16px;
            color: var(--charcoal);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column li {
            margin-bottom: 12px;
        }
        
        .footer-column a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.2s;
        }
        
        .footer-column a:hover {
            color: var(--coral);
        }
        
        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            padding-top: 40px;
            border-top: 1px solid var(--light-gray);
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--gray);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 40px;
            }
            
            .hero-subhead {
                font-size: 18px;
            }
            
            .hero-ctas {
                flex-direction: column;
                align-items: center;
            }
            
            .btn-primary, .btn-secondary {
                width: 100%;
                max-width: 300px;
            }
            
            .section-header h2 {
                font-size: 32px;
            }
            
            .tv-logos {
                gap: 24px;
            }
            
            .footer-bottom {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">SoundMarket</a>
            <div class="nav-links">
                <a href="#">Browse Music</a>
                <a href="#">How It Works</a>
                <a href="#">Pricing</a>
                <a href="#">Login</a>
                <a href="#" class="nav-cta">Get Started Free</a>
            </div>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Grammy-winning music.<br><span class="hero-highlight">Zero copyright strikes.</span><br>Completely free.</h1>
            <p class="hero-subhead">The same tracks licensed by Netflix and Fortune 500 companies.<br>Now available to every creator with full commercial rights.</p>
            <div class="hero-ctas">
                <a href="#" class="btn-primary">Start Creating - It's Free</a>
                <a href="#" class="btn-secondary">Browse Music</a>
            </div>
            <p class="hero-meta">No credit card required • Full commercial rights included</p>
            <a href="#" class="why-free-link">Why free? We believe great music shouldn't limit great content →</a>
        </div>
    </section>
    
    <!-- Trust Strip -->
    <section class="trust-strip">
        <div class="trust-container">
            <div class="trust-item">
                <div class="trust-icon">🏆</div>
                <div class="trust-label">Grammy Winners</div>
                <div class="trust-sublabel">In our catalog</div>
            </div>
            <div class="trust-item">
                <div class="trust-icon">🏢</div>
                <div class="trust-label">Fortune 500</div>
                <div class="trust-sublabel">Companies trust us</div>
            </div>
            <div class="trust-item">
                <div class="trust-icon">✓</div>
                <div class="trust-label">Zero Strikes</div>
                <div class="trust-sublabel">Guaranteed safe</div>
            </div>
            <div class="trust-item">
                <div class="trust-icon">🎵</div>
                <div class="trust-label">300,000+</div>
                <div class="trust-sublabel">Tracks available</div>
            </div>
        </div>
    </section>
    
    <!-- How It Works -->
    <section class="how-it-works">
        <div class="section-header">
            <h2>How It Works</h2>
            <p>Start using professional music in your content in minutes</p>
        </div>
        <div class="steps-container">
            <div class="step">
                <div class="step-number">1</div>
                <h3>Find Your Sound</h3>
                <p>Browse 300,000+ tracks from Grammy and Emmy-winning artists. Filter by mood, genre, or energy.</p>
            </div>
            <div class="step">
                <div class="step-number">2</div>
                <h3>Download & Create</h3>
                <p>Every track includes full commercial rights. Use on YouTube, TikTok, podcasts, or any platform.</p>
            </div>
            <div class="step">
                <div class="step-number">3</div>
                <h3>Publish Confidently</h3>
                <p>No copyright strikes. Ever. Upgrade to Pro for Content ID protection if you monetize.</p>
            </div>
        </div>
    </section>
    
    <!-- Content Fit -->
    <section class="content-fit">
        <div class="section-header">
            <h2>Music for Every Type of Content</h2>
            <p>Curated playlists for your specific creative needs</p>
        </div>
        <div class="playlists-grid">
            <div class="playlist-card">
                <div class="playlist-cover">💪</div>
                <div class="playlist-info">
                    <div class="playlist-title">Workout & Wellness</div>
                    <div class="playlist-count">12,450 tracks</div>
                </div>
            </div>
            <div class="playlist-card">
                <div class="playlist-cover">⚽</div>
                <div class="playlist-info">
                    <div class="playlist-title">Sports & Action</div>
                    <div class="playlist-count">8,320 tracks</div>
                </div>
            </div>
            <div class="playlist-card">
                <div class="playlist-cover">🌿</div>
                <div class="playlist-info">
                    <div class="playlist-title">Nature & Outdoors</div>
                    <div class="playlist-count">6,890 tracks</div>
                </div>
            </div>
            <div class="playlist-card">
                <div class="playlist-cover">✈️</div>
                <div class="playlist-info">
                    <div class="playlist-title">Travel & Adventure</div>
                    <div class="playlist-count">9,760 tracks</div>
                </div>
            </div>
            <div class="playlist-card">
                <div class="playlist-cover">🎮</div>
                <div class="playlist-info">
                    <div class="playlist-title">Gaming & Tech</div>
                    <div class="playlist-count">7,230 tracks</div>
                </div>
            </div>
            <div class="playlist-card">
                <div class="playlist-cover">🎬</div>
                <div class="playlist-info">
                    <div class="playlist-title">Cinematic & Drama</div>
                    <div class="playlist-count">15,890 tracks</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Music Quality with Preview -->
    <section class="music-quality">
        <div class="section-header">
            <h2>Award-Winning Music from Industry Leaders</h2>
            <p>Grammy and Emmy winners. Featured in your favorite shows.</p>
        </div>
        <div class="music-grid">
            <div class="track-card">
                <div class="award-badge">Grammy Winner</div>
                <div class="track-artwork">
                    <div class="play-button">▶</div>
                </div>
                <div class="track-info">
                    <div class="track-title">Electric Dreams</div>
                    <div class="track-artist">Marcus Johnson • 2x Grammy Winner</div>
                    <div class="track-feature">Featured in: The Crown (Netflix)</div>
                </div>
            </div>
            <div class="track-card">
                <div class="award-badge">Emmy Winner</div>
                <div class="track-artwork">
                    <div class="play-button">▶</div>
                </div>
                <div class="track-info">
                    <div class="track-title">Midnight Symphony</div>
                    <div class="track-artist">Sarah Chen • Emmy Award 2023</div>
                    <div class="track-feature">Featured in: Succession (HBO)</div>
                </div>
            </div>
            <div class="track-card">
                <div class="award-badge">Billboard #1</div>
                <div class="track-artwork">
                    <div class="play-button">▶</div>
                </div>
                <div class="track-info">
                    <div class="track-title">Rise Above</div>
                    <div class="track-artist">The Midnight Collective</div>
                    <div class="track-feature">Featured in: Apple Keynote 2024</div>
                </div>
            </div>
            <div class="track-card">
                <div class="award-badge">Platinum</div>
                <div class="track-artwork">
                    <div class="play-button">▶</div>
                </div>
                <div class="track-info">
                    <div class="track-title">Ocean Waves</div>
                    <div class="track-artist">Luna Park • 3x Platinum</div>
                    <div class="track-feature">Featured in: Nike Campaign</div>
                </div>
            </div>
        </div>
        <div class="featured-in">
            <h3>As Featured In</h3>
            <div class="tv-logos">
                <span class="tv-logo">NETFLIX</span>
                <span class="tv-logo">HBO</span>
                <span class="tv-logo">Apple TV+</span>
                <span class="tv-logo">Disney+</span>
                <span class="tv-logo">Amazon</span>
            </div>
        </div>
    </section>
    
    <!-- Agencies & Brands -->
    <section class="agencies-brands">
        <div class="section-header">
            <h2>Built for Scale</h2>
            <p>From individual creators to global agencies, we've got you covered</p>
        </div>
        <div class="enterprise-features">
            <div class="feature-card">
                <div class="feature-icon">📋</div>
                <h3>Flexible Licensing</h3>
                <p>Commercial use, broadcast distribution, and worldwide rights. One license covers everything your agency needs.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">👥</div>
                <h3>Team Management</h3>
                <p>Multi-seat access with role-based permissions. Add or remove team members instantly.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🔧</div>
                <h3>API Access</h3>
                <p>Integrate our catalog directly into your workflow. Automated licensing and usage tracking.</p>
            </div>
        </div>
        <div class="enterprise-cta">
            <a href="#" class="btn-secondary">Learn About Enterprise Solutions</a>
        </div>
    </section>
    
    <!-- Pricing -->
    <section class="pricing-section">
        <div class="section-header">
            <h2>Simple, Transparent Pricing</h2>
            <p>Start free or protect your monetization with Pro</p>
        </div>
        <div class="pricing-container">
            <div class="pricing-card">
                <div class="popular-badge">Most Popular</div>
                <h3 class="plan-name">Creator</h3>
                <p class="plan-price">Free Forever</p>
                <ul class="plan-features">
                    <li>Full catalog access (300,000+ tracks)</li>
                    <li>Commercial use license</li>
                    <li>All platforms supported</li>
                    <li>Unlimited downloads</li>
                    <li>No copyright strikes</li>
                </ul>
                <a href="#" class="btn-primary">Start Creating</a>
            </div>
            <div class="pricing-card">
                <h3 class="plan-name">Creator Pro</h3>
                <p class="plan-price">$15/month</p>
                <ul class="plan-features">
                    <li>Everything in Creator</li>
                    <li><strong>Content ID whitelist</strong></li>
                    <li>Priority customer support</li>
                    <li>Early access to new releases</li>
                    <li>Advanced search filters</li>
                </ul>
                <a href="#" class="btn-secondary">Protect Your Revenue</a>
            </div>
        </div>
    </section>
    
    <!-- Success Stories -->
    <section class="success-stories">
        <div class="section-header">
            <h2>Creators Making It Happen</h2>
            <p>Join thousands of creators using SoundMarket</p>
        </div>
        <div class="testimonials-grid">
            <div class="testimonial">
                <p class="quote">"I can't believe this quality is free. The Grammy-winning tracks give my videos a professional edge that my audience loves."</p>
                <div class="testimonial-author">
                    <div class="author-avatar">JT</div>
                    <div class="author-info">
                        <div class="author-name">Jake Thompson</div>
                        <div class="author-channel">Travel Vlogger • 125K subs</div>
                    </div>
                </div>
            </div>
            <div class="testimonial">
                <p class="quote">"Content ID protection saved my channel. I keep 100% of my ad revenue while using amazing music. Worth every penny."</p>
                <div class="testimonial-author">
                    <div class="author-avatar">MC</div>
                    <div class="author-info">
                        <div class="author-name">Maria Cruz</div>
                        <div class="author-channel">Fitness Creator • 450K subs</div>
                    </div>
                </div>
            </div>
            <div class="testimonial">
                <p class="quote">"Our agency switched from [competitor] and saved $10K/year. Same quality music, better licensing terms."</p>
                <div class="testimonial-author">
                    <div class="author-avatar">BS</div>
                    <div class="author-info">
                        <div class="author-name">Brad Stevens</div>
                        <div class="author-channel">Creative Director • Agency</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section class="cta-section">
        <div class="cta-content">
            <h2>Ready to level up your content?</h2>
            <p>Join thousands of creators using Grammy-winning music in their videos.</p>
            <a href="#" class="cta-button">Get Started Free →</a>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <h4>Product</h4>
                <ul>
                    <li><a href="#">Browse Music</a></li>
                    <li><a href="#">Pricing</a></li>
                    <li><a href="#">How It Works</a></li>
                    <li><a href="#">Success Stories</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>Company</h4>
                <ul>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Our Artists</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Press Kit</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>Support</h4>
                <ul>
                    <li><a href="#">Help Center</a></li>
                    <li><a href="#">Contact</a></li>
                    <li><a href="#">Legal/Terms</a></li>
                    <li><a href="#">Privacy</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>Connect</h4>
                <ul>
                    <li><a href="#">Newsletter</a></li>
                    <li><a href="#">Twitter</a></li>
                    <li><a href="#">Instagram</a></li>
                    <li><a href="#">hello@soundmarket.com</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <div>© 2024 SoundMarket. All rights reserved.</div>
            <div>Made with ❤️ for creators</div>
        </div>
    </footer>
</body>
</html>
