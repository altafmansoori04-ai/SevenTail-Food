<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seven Tail | Fine Dining Experience</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #e74c3c;
            --secondary: #2c3e50;
            --accent: #f39c12;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --text: #333;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        body {
            color: var(--text);
            line-height: 1.6;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .section-title p {
            color: #777;
            max-width: 700px;
            margin: 0 auto;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--primary);
            margin: 15px auto;
            border-radius: 2px;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .btn:hover {
            background: #c0392b;
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }

        /* Header Styles */
        header {
            background-color: var(--secondary);
            color: white;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-container {
            display: flex;
            align-items: center;
            text-decoration: none;
            
        }

        .circular-logo img {
        
            width: 80px;
            height: 65px;
            border-radius: 50%;
        justify-content: flex-start;
        border: #c11f0d solid 2px;
        
                }

        .logo-text {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            margin-left: 15px;
            
        }

        .logo-text span {
            color: var(--primary);
            margin-left: 5px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            bottom: -5px;
            left: 0;
            transition: width 0.3s;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url(SEVENTAIL_PL\ 2025\ \(1\)_page-0007.jpg);
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .about-text p {
            margin-bottom: 20px;
        }

        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* Menu Section */
        .menu {
            background-color: var(--light);
        }

        .menu-categories {
            display: flex;
            justify-content: center;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .category-btn {
            padding: 10px 25px;
            margin: 0 10px 10px;
            background: white;
            border: 2px solid var(--primary);
            color: var(--primary);
            border-radius: 30px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }

        .category-btn.active, .category-btn:hover {
            background: var(--primary);
            color: white;
        }

        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .menu-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }

        .menu-item:hover {
            transform: translateY(-10px);
        }

        .menu-item-image {
            height: 200px;
            overflow: hidden;
        }

        .menu-item-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .menu-item:hover .menu-item-image img {
            transform: scale(1.1);
        }

        .menu-item-content {
            padding: 20px;
        }

        .menu-item-title {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .menu-item-title h3 {
            font-size: 1.3rem;
            color: var(--secondary);
        }

        .menu-item-title span {
            color: var(--primary);
            font-weight: 700;
        }

        .menu-item p {
            color: #777;
            font-size: 0.9rem;
        }

        /* Specials Section */
        .specials-content {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
        }

        .special-item {
            flex: 1;
            min-width: 300px;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .special-item-image {
            height: 200px;
            overflow: hidden;
        }

        .special-item-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .special-item-content {
            padding: 20px;
        }

        .special-item-content h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }

        .special-item-content p {
            margin-bottom: 15px;
            color: #777;
        }

        /* Testimonials Section */
        .testimonials {
            background-color: var(--light);
        }

        .testimonials-container {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }

        .testimonial {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--shadow);
            text-align: center;
            display: none;
        }

        .testimonial.active {
            display: block;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .testimonial-author img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }

        .testimonial-author h4 {
            font-size: 1.1rem;
            color: var(--secondary);
        }

        .testimonial-author p {
            color: #777;
            font-size: 0.9rem;
        }

        .testimonial-nav {
            display: flex;
            justify-content: center;
            margin-top: 30px;
        }

        .testimonial-dot {
            width: 12px;
            height: 12px;
            background: #ccc;
            border-radius: 50%;
            margin: 0 5px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .testimonial-dot.active {
            background: var(--primary);
        }

        /* Contact Section */
        .contact-content {
            display: flex;
            gap: 50px;
            flex-wrap: wrap;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .contact-info i {
            margin-right: 10px;
            color: var(--primary);
            width: 20px;
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        .form-group textarea {
            height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
            margin-bottom: 30px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background: var(--primary);
        }

        .footer-column p {
            margin-bottom: 15px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #bbb;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .about-image {
                order: -1;
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: var(--secondary);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: left 0.3s;
            }
            
            nav ul.active {
                left: 0;
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .logo-text {
                font-size: 1.5rem;
            }
            
            .circular-logo {
                width: 40px;
                height: 40px;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
            
            .menu-items {
                grid-template-columns: 1fr;
            }
            
            .logo-text {
                font-size: 1.3rem;
            }
            
            .circular-logo {
                width: 35px;
                height: 35px;
                margin-right: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo-container">
                    <div class="circular-logo">
                    <img src="logo121.jpeg" alt="">
                    </div>
                    <div class="logo-text">Seven<span>Tail</span></div>
                </a>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#menu">Menu</a></li>
                        <li><a href="#specials">Specials</a></li>
                        <li><a href="#testimonials">Testimonials</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Experience Culinary Excellence</h1>
                <p>“We export premium natural products like honey, spices, organic seeds, peanut butter, olive oil, coconut oil, and coconut milk worldwide.”</p>
                <a href="#menu" class="btn">View Our Menu</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>Our Story</h2>
                <p>Discover the passion and dedication behind every Experience we serve</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Creating Memorable Dining Experiences Since 2005</h3>
                <p> <b>Trust & Quality Focus</b>
“Seven Tail is your trusted partner in global exports of premium natural products. We bring you the finest honey, spices, organic seeds, peanut butter, olive oil, coconut oil, and coconut milk, carefully sourced to ensure purity and quality. Our vision is simple — to share the goodness of nature with the world.”</p>


---

✨<p> <b> Global Reach Focus</b>
“At Seven Tail, we export a diverse range of natural and organic products to international markets. From healthy spreads and oils to rich spices and seeds, every product we deliver reflects our commitment to excellence. We believe in building lasting relationships through quality, reliability, and a global approach.”</p>


---

✨ <b>Health & Lifestyle Focus</b>
“Seven Tail stands for health taste, and authenticity. With a portfolio that includes honey, spices, organic seeds, peanut butter, olive oil, coconut oil, and coconut milk, we aim to enhance everyday living with natural products. Our promise is to bring you closer to nature — one product at a time.”</p>
                    <a href="#contact" class="btn">Visit Us</a>
                </div>
                <div class="about-image">
                    <img src="SEVENTAIL_PL 2025 (1)_page-0003.jpg" alt="Restaurant Interior">
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="menu">
        <div class="container">
            <div class="section-title">
                <h2>Our Product</h2>
                <p>Explore our carefully crafted selection of culinary delights</p>
            </div>
                        <div class="menu-items">
                <!-- Starters -->
                <div class="menu-item" data-category="starters">
                    <div class="menu-item-image">
                        <img src="organic1.jpg" alt="Bruschetta">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Organic seed & Grains</h3><br>
                            
                            
                        </div>
                        <p>We provide high-quality organic seeds and grains, carefully sourced to ensure purity and nutrition. Perfect for healthy living and global food industries.</p>
                    </div>
                </div>
                
                <div class="menu-item" data-category="starters">
                    <div class="menu-item-image">
                        <img src="organic2.jpg" alt="Calamari">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Spices</h3>
                        
                            
                        </div>
                        <p>From black pepper to aromatic herbs, Seven Tail exports premium spices that add authentic flavor and richness to cuisines worldwide.</p>
                    </div>
                </div>
                
                <!-- Main Courses -->
                <div class="menu-item" data-category="mains">
                    <div class="menu-item-image">
                        <img src="organic3.jpg" alt="Steak">
                        
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Olis & Herbs</h3>
                            
                            
                        </div>
                        <p>Our range includes olive oil, coconut oil, and other natural extracts—pure, healthy, and ideal for both cooking and wellness.</p>
                    </div>
                </div>
                
                <div class="menu-item" data-category="mains">
                    <div class="menu-item-image">
                        <img src="honey.jpg" alt="Pizza">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Honey</h3>
                            
                        </div>
                        <p>Honey is a sweet, golden liquid made by bees from flower nectar. It is nutritious, has natural healing properties, and is used in food, drinks, and medicine.</p>
                    </div>
                </div>
                
                <!-- Desserts -->
                <div class="menu-item" data-category="desserts">
                    <div class="menu-item-image">
                        <img src="pea nut.jpg" alt="Chocolate Cake">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Pea Nut Butter</h3>
                            
                        </div>
                        <p> Peanut butter is a creamy or crunchy spread made from ground roasted peanuts. It is rich in protein, healthy fats, and energy, and is commonly used on bread, in desserts, or as a snack.</p>
                    </div>
                </div>
                
                <div class="menu-item" data-category="desserts">
                    <div class="menu-item-image">
                        <img src="oilive oil.jpg" alt="Cheesecake">
                    </div>
                    <div class="menu-item-content">
                        <div class="menu-item-title">
                            <h3>Oilive Oil</h3>
                            
                        </div>
                        <p>Olive oil is a healthy oil extracted from olives. It is rich in monounsaturated fats and antioxidants, commonly used in cooking, salads, and for its health benefits.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Specials Section -->
    <section id="specials">
        <div class="container">
            <div class="section-title">
                <h2>Our Specials Product</h2>
                <p>Discover our  exclusive creations available for a lifetime</p>
            </div>
            <div class="specials-content">
                <div class="special-item">
                    <div class="special-item-image">
                        <img src="organic seed.jpg" alt="Special Dish">
                    </div>
                    <div class="special-item-content">
                        <h3>Real Organic Seed</h3>
                        <p>Organic seeds are natural seeds grown without chemical fertilizers or pesticides. They are healthy, nutritious, and used for planting or as a food source.</p>
                        
                    </div>
                </div>
                <div class="special-item">
                    <div class="special-item-image">
                        <img src="coconut oil.jpg" alt="Special Dish">
                    </div>
                    <div class="special-item-content">
                        <h3>Coconut Oil And Milk</h3>
                        <p>Coconut oil and coconut milk come from the coconut fruit. Coconut oil is a healthy fat used in cooking, skincare, and hair care, while coconut milk is a creamy liquid used in cooking and beverages for its rich flavor and nutrients.</p>

                    </div>
                </div>
                <div class="special-item">
                    <div class="special-item-image">
                        <img src="Spices factry.jpg" alt="Special Dish">
                    </div>
                    <div class="special-item-content">
                        <h3>Spices Factory</h3>
                        <p>Spices are natural substances from seeds, bark, roots, or fruits, used to add flavor, aroma, and color to food. They also have medicinal and preservative properties.</p>
                        
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Customers Say</h2>
                <p>Hear from our delighted patrons about their experiences</p>
            </div>
            <div class="testimonials-container">
                <div class="testimonial active">
                    <p class="testimonial-text">I am impressed with the quality of your products and the professionalism of your service. The products are reliable, effective, and meet expectations, while the staff is responsive, helpful, and attentive to customer needs. Overall, your company delivers a satisfying experience and demonstrates commitment to excellence.</p>
                    <div class="testimonial-author">
                        <img src="dp2.jpg" alt="Customer">
                        <div>
                            <h4>Sarah Johnson</h4>
                            <p>Client From Philippines</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">"I am very satisfied with the service. The team is professional, responsive, and ensures a smooth and pleasant experience.""</p>
                    <div class="testimonial-author">
                        <img src="port-img.jpeg" alt="Customer">
                        <div>
                            <h4>Altaf </h4>
                            <p> Client From India </p>
                        </div>
                    </div>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">"The products are high-quality and practical, showing attention to detail and customer needs. The service is prompt, courteous, and professional, making the overall experience smooth and enjoyable. I am satisfied with both the products and the support provided by your team."</p>
                    <div class="testimonial-author">
                        <img src="dp1.jpg" alt="Customer">
                        <div>
                            <h4>Elena Rodriguez</h4>
                            <p>client from U.S.A</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-nav">
                    <div class="testimonial-dot active" data-index="0"></div>
                    <div class="testimonial-dot" data-index="1"></div>
                    <div class="testimonial-dot" data-index="2"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>We'd love to hear from you. Visit us or get in touch</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Noida Uttar Pradesh India</p>
                    <p><i class="fas fa-phone"></i> 7982208363</p>
                    <p><i class="fas fa-envelope"></i> natalia@seventail.in</p>
                    <p><i class="fas fa-clock"></i> Monday-Friday: 9AM - 10PM</p>

                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-tripadvisor"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Send Us a Message</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Your Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Seven Tail</h3>
                    <p>Experience culinary excellence in the heart of the Country. We're committed to creating memorable export experiences with our innovative ideas and experience service.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#menu">Menu</a></li>
                        <li><a href="#specials">Specials</a></li>
                        <li><a href="#testimonials">Testimonials</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <p><i class="fas fa-map-marker-alt"></i>Noida Uttar Pradesh India</p>
                    <p><i class="fas fa-phone"></i> 7982208363</p>
                    <p><i class="fas fa-envelope"></i> natalia@seventail.in</p>
                </div>
                <div class="footer-column">
                    <h3>Newsletter</h3>
                    <p>Subscribe to our newsletter to receive updates on special offers and new menu items.</p>
                    <form id="newsletterForm">
                        <div class="form-group">
                            <input type="email" placeholder="Your Email" required>
                        </div>
                        <button type="submit" class="btn">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 sevenTail. All Rights Reserved. |  
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('active');
        });

        // Smooth Scrolling for Navigation Links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetSection.offsetTop - 70,
                    behavior: 'smooth'
                });
                
                // Close mobile menu after clicking a link
                document.querySelector('nav ul').classList.remove('active');
            });
        });

        // Menu Category Filter
        document.querySelectorAll('.category-btn').forEach(button => {
            button.addEventListener('click', function() {
                // Remove active class from all buttons
                document.querySelectorAll('.category-btn').forEach(btn => {
                    btn.classList.remove('active');
                });
                
                // Add active class to clicked button
                this.classList.add('active');
                
                const category = this.getAttribute('data-category');
                const menuItems = document.querySelectorAll('.menu-item');
                
                menuItems.forEach(item => {
                    if (category === 'all' || item.getAttribute('data-category') === category) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });

        // Testimonial Slider
        const testimonials = document.querySelectorAll('.testimonial');
        const dots = document.querySelectorAll('.testimonial-dot');
        let currentTestimonial = 0;

        function showTestimonial(index) {
            testimonials.forEach(testimonial => {
                testimonial.classList.remove('active');
            });
            
            dots.forEach(dot => {
                dot.classList.remove('active');
            });
            
            testimonials[index].classList.add('active');
            dots[index].classList.add('active');
            currentTestimonial = index;
        }

        dots.forEach(dot => {
            dot.addEventListener('click', function() {
                const index = parseInt(this.getAttribute('data-index'));
                showTestimonial(index);
            });
        });

        // Auto-rotate testimonials
        setInterval(() => {
            currentTestimonial = (currentTestimonial + 1) % testimonials.length;
            showTestimonial(currentTestimonial);
        }, 5000);

        // Form Submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });

        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for subscribing to our newsletter!');
            this.reset();
        });

        // Header background on scroll
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(44, 62, 80, 0.95)';
            } else {
                header.style.backgroundColor = 'var(--secondary)';
            }
        });
    </script>
</body>
</html>