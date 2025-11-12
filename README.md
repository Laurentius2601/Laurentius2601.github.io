<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Laurence Cornejo | Professional Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
        }

        h1, h2, h3, h4 {
            margin-bottom: 20px;
            color: var(--primary);
        }

        p {
            margin-bottom: 15px;
        }

        a {
            text-decoration: none;
            color: var(--secondary);
            transition: var(--transition);
        }

        a:hover {
            color: var(--accent);
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--secondary);
            color: white;
            border-radius: 4px;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            margin: 15px auto;
        }

        /* Header & Navigation */
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
            padding: 20px 0;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--dark);
            font-weight: 500;
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            bottom: -5px;
            left: 0;
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: white;
        }

        .hero-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: var(--light);
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .hero-btns .btn {
            background-color: transparent;
            border: 2px solid white;
        }

        .hero-btns .btn:hover {
            background-color: white;
            color: var(--primary);
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

        .about-img {
            flex: 1;
            text-align: center;
        }

        .about-img img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        /* Skills Section */
        .skills {
            background-color: white;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background-color: var(--light);
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        .skill-category:hover {
            transform: translateY(-10px);
        }

        .skill-category h3 {
            color: var(--secondary);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-item {
            margin-bottom: 15px;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }

        .skill-bar {
            height: 8px;
            background-color: #ddd;
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-level {
            height: 100%;
            background-color: var(--secondary);
            border-radius: 4px;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .project-img {
            height: 200px;
            background-color: var(--gray);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .project-info {
            padding: 20px;
        }

        .project-info h3 {
            margin-bottom: 10px;
        }

        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        /* Contact Section */
        .contact {
            background-color: white;
        }

        .contact-container {
            display: flex;
            gap: 50px;
        }

        .contact-info {
            flex: 1;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: var(--secondary);
            font-size: 20px;
        }

        .contact-form {
            flex: 1;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            padding: 40px 0;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .social-link {
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-link:hover {
            background-color: var(--secondary);
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 20px;
            color: rgba(255,255,255,0.7);
            font-size: 14px;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .contact-container {
                flex-direction: column;
            }
        }

        @media (max-width: 768px) {
            .navbar {
                flex-wrap: wrap;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                margin-top: 20px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 10px 0;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .hero-btns .btn {
                width: 100%;
                max-width: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">Laurence<span>Benedict</span></a>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Hi, I'm Laurence</h1>
                <p>I'm a professional specializing in Microsoft technologies, data analytics, and business solutions. I create efficient systems that help businesses thrive.</p>
                <div class="hero-btns">
                    <a href="#projects" class="btn">View My Work</a>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Who I Am & What I Do</h3>
                    <p>I'm a technology professional with expertise in Microsoft platforms, data analytics, and business process optimization. With over 5 years of experience, I've helped numerous organizations streamline their operations and leverage data for better decision-making.</p>
                    <p>My approach combines technical expertise with a deep understanding of business needs, ensuring that solutions not only work technically but also deliver real value.</p>
                    <p>I'm currently looking for new opportunities where I can apply my skills to solve complex business challenges and contribute to organizational success.</p>
                    <a href="#" class="btn">Download Resume</a>
                </div>
                <div class="about-img">
                    <!-- Placeholder for profile image -->
                    <div style="width: 100%; height: 400px; background-color: #ddd; border-radius: 10px; display: flex; align-items: center; justify-content: center;">
                        <img src="wbW7SU7k.jpg" style="width: 100%; height: 400px; background-color: #ddd; border-radius: 10px; display: flex; align-items: center; justify-content: center;">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-desktop"></i> Microsoft Technologies</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Microsoft 365</span>
                            <span>Expert</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 95%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Power Platform</span>
                            <span>Expert</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Azure</span>
                            <span>Advanced</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 80%"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-chart-bar"></i> Data Analytics</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Power BI</span>
                            <span>Expert</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Excel Analytics</span>
                            <span>Expert</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 95%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>SQL</span>
                            <span>Intermediate</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 75%"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-cogs"></i> Business Solutions</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Process Automation</span>
                            <span>Expert</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Workflow Design</span>
                            <span>Advanced</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 85%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Project Management</span>
                            <span>Intermediate</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-level" style="width: 70%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img" style="background-color: #3498db;">
                        Project Screenshot
                    </div>
                    <div class="project-info">
                        <h3>Sales Dashboard</h3>
                        <p>Interactive Power BI dashboard that provides real-time sales analytics and performance metrics for a retail company.</p>
                        <div class="project-links">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img" style="background-color: #e74c3c;">
                        Project Screenshot
                    </div>
                    <div class="project-info">
                        <h3>Automated Reporting System</h3>
                        <p>Power Automate workflow that automatically generates and distributes weekly performance reports to stakeholders.</p>
                        <div class="project-links">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-img" style="background-color: #2ecc71;">
                        Project Screenshot
                    </div>
                    <div class="project-info">
                        <h3>Inventory Management App</h3>
                        <p>Custom Power Apps solution with SharePoint integration for tracking inventory levels and automating reordering.</p>
                        <div class="project-links">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Contact Information</h3>
                    <p>Feel free to reach out to me for collaboration or any inquiries.</p>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h4>Email</h4>
                            <p>your.email@example.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h4>Phone</h4>
                            <p>+1 (123) 456-7890</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h4>Location</h4>
                            <p>Your City, Country</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" placeholder="Your Message" required></textarea>
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
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
            </div>
            <p class="copyright">&copy; 2023 Your Name. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    document.querySelector('.nav-links').classList.remove('active');
                }
            });
        });
        
        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });
    </script>
</body>
</html>
