<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yoseph Trifosa Zega - TKJ Professional Portfolio</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html, body {
            height: 100%;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #0a0a0a;
            color: #fff;
        }

        /* ===========================================
                NAVBAR 5 HEAD BAR - TKJ STYLE
        =========================================== */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            height: 80px;
            background: rgba(10,10,10,0.95);
            backdrop-filter: blur(20px);
            z-index: 1000;
            border-bottom: 1px solid rgba(102,126,234,0.3);
            transition: all 0.3s ease;
        }
        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 50px;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .logo i { font-size: 2.2rem; animation: spin 3s linear infinite; }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .nav-menu {
            display: flex;
            list-style: none;
            gap: 10px;
        }
        .nav-item {
            position: relative;
        }
        .nav-link {
            color: #fff;
            text-decoration: none;
            padding: 15px 25px;
            font-weight: 600;
            border-radius: 25px;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }
        .nav-link:hover {
            background: linear-gradient(45deg, #667eea, #764ba2);
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(102,126,234,0.4);
        }
        .nav-link.active {
            background: linear-gradient(45deg, #f093fb, #f5576c);
            box-shadow: 0 5px 15px rgba(240,147,251,0.5);
        }

        /* ===========================================
                HERO SECTION - FULLSCREEN TKJ VIBE
        =========================================== */
        .hero-section {
            height: 100vh;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow: hidden;
        }
        .hero-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120,119,198,0.3) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255,119,198,0.3) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120,219,255,0.2) 0%, transparent 50%);
            animation: bgShift 15s ease-in-out infinite;
        }
        @keyframes bgShift {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.1) rotate(180deg); }
        }
        .hero-content {
            z-index: 10;
            max-width: 1000px;
            position: relative;
        }
        .profile-img {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            margin: 0 auto 40px;
            border: 5px solid transparent;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb) padding-box,
                        linear-gradient(45deg, #667eea, #764ba2, #f093fb) border-box;
            box-shadow: 
                0 0 50px rgba(102,126,234,0.5),
                inset 0 0 50px rgba(255,255,255,0.1);
            animation: float 4s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        .hero-title {
            font-size: 4.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #fff, #f0f0f0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 30px rgba(255,255,255,0.5);
        }
        .hero-subtitle {
            font-size: 1.6rem;
            margin-bottom: 30px;
            color: rgba(255,255,255,0.9);
            font-weight: 400;
        }
        .hero-contact {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .contact-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            padding: 20px 35px;
            border-radius: 50px;
            border: 2px solid rgba(255,255,255,0.2);
            transition: all 0.4s ease;
            cursor: pointer;
            font-weight: 600;
        }
        .contact-card:hover {
            background: rgba(102,126,234,0.3);
            border-color: #667eea;
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 20px 40px rgba(102,126,234,0.4);
        }

        /* ===========================================
                SECTIONS - FULLSCREEN SCROLL
        =========================================== */
        .section {
            min-height: 100vh;
            padding: 120px 50px;
            display: flex;
            align-items: center;
            position: relative;
        }
        .container {
            max-width: 1400px;
            margin: 0 auto;
            width: 100%;
        }
        .section-title {
            font-size: 4rem;
            text-align: center;
            margin-bottom: 60px;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 800;
        }

        /* About Section */
        .about-section {
            background: linear-gradient(135deg, rgba(26,26,46,0.8) 0%, rgba(22,33,62,0.8) 100%);
        }
        .about-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.5rem;
            line-height: 1.8;
            color: rgba(255,255,255,0.9);
        }

        /* Skills Section */
        .skills-section {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 50px;
        }
        .skill-card {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(20px);
            padding: 50px;
            border-radius: 25px;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }
        .skill-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            transition: left 0.5s;
        }
        .skill-card:hover::before {
            left: 100%;
        }
        .skill-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 60px rgba(0,0,0,0.5);
            border-color: #667eea;
        }
        .skill-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 30px;
        }
        .skill-icon {
            width: 70px;
            height: 70px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            background: linear-gradient(45deg, #667eea, #764ba2);
        }
        .skill-title {
            font-size: 1.8rem;
            font-weight: 700;
        }
        .skill-level {
            color: #f093fb;
            font-weight: 600;
        }
        .skill-list {
            list-style: none;
        }
        .skill-item {
            padding: 15px 0;
            font-size: 1.2rem;
            color: rgba(255,255,255,0.9);
            position: relative;
            padding-left: 40px;
        }
        .skill-item::before {
            content: "⚡";
            position: absolute;
            left: 0;
            font-size: 1.4rem;
        }

        /* Positions Section */
        .positions-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .positions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        .position-card {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(25px);
            padding: 50px 30px;
            border-radius: 20px;
            text-align: center;
            border: 2px solid rgba(255,255,255,0.2);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .position-card:hover {
            transform: translateY(-20px) rotateX(5deg);
            box-shadow: 0 40px 80px rgba(0,0,0,0.4);
            border-color: rgba(255,255,255,0.4);
        }
        .position-icon {
            font-size: 4rem;
            margin-bottom: 25px;
            display: block;
        }
        .position-title {
            font-size: 1.6rem;
            font-weight: 700;
            margin-bottom: 15px;
        }

        /* Career Section */
        .career-section {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }
        .career-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        .career-goal {
            background: rgba(255,255,255,0.15);
            padding: 40px;
            margin: 30px 0;
            border-radius: 20px;
            backdrop-filter: blur(20px);
            font-size: 1.5rem;
        }

        /* Final Contact */
        .contact-section {
            background: linear-gradient(135deg, #000 0%, #1a1a2e 100%);
            text-align: center;
        }
        .contact-hero {
            font-size: 3.5rem;
            margin-bottom: 40px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .cta-buttons {
            display: flex;
            gap: 30px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .btn-cta {
            padding: 25px 50px;
            font-size: 1.4rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 15px;
            transition: all 0.4s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        .btn-whatsapp {
            background: linear-gradient(45deg, #25D366, #128C7E);
            color: white;
            box-shadow: 0 10px 30px rgba(37,211,102,0.4);
        }
        .btn-email {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            box-shadow: 0 10px 30px rgba(102,126,234,0.4);
        }
        .btn-cta:hover {
            transform: translateY(-10px) scale(1.1);
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-container { padding: 0 20px; }
            .nav-menu { 
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: rgba(10,10,10,0.98);
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                padding-top: 50px;
                transition: left 0.3s ease;
            }
            .nav-menu.active { left: 0; }
            .hero-title { font-size: 3rem; }
            .section { padding: 100px 20px; }
            .section-title { font-size: 2.8rem; }
            .skills-grid { grid-template-columns: 1fr; }
            .cta-buttons { flex-direction: column; align-items: center; }
        }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }
        .hamburger span {
            width: 30px;
            height: 4px;
            background: #fff;
            border-radius: 3px;
            transition: 0.3s;
        }
        @media (max-width: 768px) {
            .hamburger { display: flex; }
            .nav-menu { display: flex; }
        }
    </style>
</head>
<body>
    <!-- NAVBAR 5 HEAD BAR -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-network-wired"></i>
                Yoseph Zega
            </div>
            <ul class="nav-menu">
                <li class="nav-item"><a href="#home" class="nav-link active"><i class="fas fa-home"></i> Home</a></li>
                <li class="nav-item"><a href="#about" class="nav-link"><i class="fas fa-user"></i> About</a></li>
                <li class="nav-item"><a href="#skills" class="nav-link"><i class="fas fa-tools"></i> Skills</a></li>
                <li class="nav-item"><a href="#positions" class="nav-link"><i class="fas fa-briefcase"></i> Positions</a></li>
                <li class="nav-item"><a href="#career" class="nav-link"><i class="fas fa-rocket"></i> Career</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section">
        <div class="hero-content">
            <img src="yosep.jpg" alt="Jika tulisan ini muncul artinya file tidak ditemukan" style="border: 5px solid red; width: 200px;">
            <h1 class="hero-title">Yoseph Trifosa Zega</h1>
            <div class="hero-subtitle">
                Teknisi Jaringan & Web Developer<br>
                <small>TKJ SMKS YPPI TUALANG [Perawang] | Lulusan 2027</small>
            </div>
            <div class="hero-contact">
                <div class="contact-card">
                    <i class="fas fa-map-marker-alt"></i> JL. Niaga Gg. Rukun
                </div>
                <div class="contact-card">
                    <i class="fas fa-phone"></i> 0853-6322-1253
                </div>
                <div class="contact-card">
                    <i class="fas fa-envelope"></i> yosepz07@gmail.com
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section about-section">
        <div class="container">
            <h2 class="section-title">📋 Tentang Saya</h2>
            <div class="about-content">
                Saya adalah lulusan <strong>Teknik Komputer dan Jaringan (TKJ)</strong> dengan pengalaman praktik di bidang networking, hardware maintenance, dan web development. Passion saya adalah membangun infrastruktur jaringan yang stabil dan aplikasi web yang responsif.
            </div>
        </div>
    </section>

    <!-- Positions Section -->
    <section id="positions" class="section positions-section">
        <div class="container">
            <h2 class="section-title">🎯 Siap Kerja Di Posisi</h2>
            <div class="positions-grid">
                <div class="position-card">
                    <i class="fas fa-network-wired position-icon"></i>
                    <div class="position-title">Junior Network Engineer</div>
                </div>
                <div class="position-card">
                    <i class="fas fa-headset position-icon"></i>
                    <div class="position-title">IT Support/Helpdesk</div>
                </div>
                <div class="position-card">
                    <i class="fas fa-code position-icon"></i>
                    <div class="position-title">Web Developer Frontend/Backend</div>
                </div>
                <div class="position-card">
                    <i class="fas fa-server position-icon"></i>
                    <div class="position-title">System Administrator</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section skills-section">
        <div class="container">
            <h2 class="section-title">🛠️ SKILLS TKJ YANG DIKUASAI</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-header">
                        <div class="skill-icon"><i class="fas fa-network-wired"></i></div>
                        <div>
                            <div class="skill-title">Networking</div>
                            <div class="skill-level">(80%)</div>
                        </div>
                    </div>
                    <ul class="skill-list">
                        <li class="skill-item">Konfigurasi Router Cisco/MikroTik</li>
                        <li class="skill-item">VLAN, Subnetting, DHCP Server</li>
                        <li class="skill-item">Instalasi Jaringan LAN/WAN</li>
                        <li class="skill-item">Wireless Access Point Setup</li>
                        <li class="skill-item">Packet Tracer Simulation</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <div class="skill-header">
                        <div class="skill-icon" style="background: linear-gradient(45deg, #ff6b6b, #f093fb);"><i class="fas fa-hammer"></i></div>
                        <div>
                            <div class="skill-title">Hardware & Troubleshooting</div>
                            <div class="skill-level">(90%)</div>
                        </div>
                    </div>
                    <ul class="skill-list">
                        <li class="skill-item">PC/Laptop Assembly & Upgrade</li>
                        <li class="skill-item">Diagnosa Motherboard & BIOS</li>
                        <li class="skill-item">Crimping Kabel UTP/STP</li>
                        <li class="skill-item">Instalasi Server & Printer</li>
                        <li class="skill-item">CCTV IP Camera Setup</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <div class="skill-header">
                        <div class="skill-icon" style="background: linear-gradient(45deg, #4ecdc4, #44a08d);"><i class="fas fa-laptop-code"></i></div>
                        <div>
                            <div class="skill-title">Web Development</div>
                            <div class="skill-level">(75%)</div>
                        </div>
                    </div>
                    <ul class="skill-list">
                        <li class="skill-item">Frontend: HTML5, CSS3, JavaScript, Bootstrap, Tailwind</li>
                        <li class="skill-item">Backend: PHP, MySQL, XAMPP</li>
                        <li class="skill-item">Framework: CodeIgniter Dasar</li>
                        <li class="skill-item">Responsive Web Design</li>
                        <li class="skill-item">WordPress Customization</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Career Section -->
    <section id="career" class="section career-section">
        <div class="container">
            <h2 class="section-title">🎯 TARGET KARIR</h2>
            <div class="career-content">
                <div class="career-goal">
                    <strong>Short-term:</strong> IT Support di perusahaan PT. INDAH KIAT
                </div>
                <div class="career-goal">
                    <strong>Long-term:</strong> Network Engineer CCNA Certified | Fullstack Developer
                </div>
            </div>
        </div>
    </section>

    <!-- Final Contact -->
    <section class="section contact-section">
        <div class="container">
            <h2 class="contact-hero">📞 HUBUNGI SAYA</h2>
            <div style="font-size: 1.6rem; margin-bottom: 50px; opacity: 0.9;">
                Siap troubleshoot masalah jaringan 24/7 dan coding website sampai subuh!
            </div>
            <div class="cta-buttons">
                <a href="https://wa.me/6285363221253" target="_blank" class="btn-cta btn-whatsapp">
                    <i class="fab fa-whatsapp"></i> WhatsApp Sekarang
                </a>
                <a href="mailto:yosepz07@gmail.com" class="btn-cta btn-email">
                    <i class="fas fa-envelope"></i> Kirim Email
                </a>
            </div>
        </div>
    </section>

    <script>
        // Smooth scroll & active nav
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                
                // Active nav
                document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
                this.classList.add('active');
            });
        });

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.background = 'rgba(10,10,10,0.98)';
                navbar.style.boxShadow = '0 5px 25px rgba(0,0,0,0.5)';
            } else {
                navbar.style.background = 'rgba(10,10,10,0.95)';
                navbar.style.boxShadow = 'none';
            }
        });

        // Mobile menu toggle
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');
        hamburger.addEventListener('click', () => {
            navMenu.classList.toggle('active');
            hamburger.classList.toggle('active');
        });
    </script>
</body>
</html>
