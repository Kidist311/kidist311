<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kidist Alemayehu | Software Engineering Student</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #6C63FF;
            --secondary: #4A44C6;
            --accent: #FF6584;
            --dark: #2D2B55;
            --light: #F5F5F7;
            --gray: #8A8AA3;
            --gradient: linear-gradient(135deg, #6C63FF 0%, #4A44C6 100%);
            --card-shadow: 0 10px 30px rgba(108, 99, 255, 0.15);
        }

        body {
            background-color: #FAFAFF;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Hero Section */
        header {
            background: var(--gradient);
            color: white;
            padding: 100px 0;
            text-align: center;
            border-radius: 0 0 40px 40px;
            position: relative;
            overflow: hidden;
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        .header-decoration {
            position: absolute;
            width: 300px;
            height: 300px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            top: -150px;
            right: -100px;
        }

        .header-decoration:nth-child(2) {
            width: 200px;
            height: 200px;
            top: auto;
            bottom: -100px;
            left: -50px;
            right: auto;
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: white;
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: var(--primary);
            border: 5px solid rgba(255, 255, 255, 0.3);
            box-shadow: var(--card-shadow);
        }

        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .subtitle {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 20px;
        }

        .location {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 20px;
            border-radius: 30px;
            margin-top: 15px;
            font-size: 0.95rem;
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: white;
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .social-link:hover {
            transform: translateY(-5px);
            background: var(--primary);
            color: white;
        }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--dark);
            font-size: 2.2rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--gradient);
            margin: 10px auto;
            border-radius: 2px;
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .tech-item {
            background: white;
            border-radius: 12px;
            padding: 20px 15px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #eee;
        }

        .tech-item:hover {
            transform: translateY(-10px);
            box-shadow: var(--card-shadow);
            border-color: var(--primary);
        }

        .tech-icon {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--primary);
        }

        .tech-name {
            font-weight: 600;
            color: var(--dark);
        }

        /* GitHub Stats */
        .stats-container {
            background: white;
            border-radius: 20px;
            padding: 40px;
            box-shadow: var(--card-shadow);
            margin-top: 30px;
        }

        .trophy-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .trophy {
            background: var(--gradient);
            color: white;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            box-shadow: 0 5px 15px rgba(108, 99, 255, 0.3);
        }

        .trophy span {
            font-size: 0.7rem;
            margin-top: 5px;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 40px 0;
            border-radius: 40px 40px 0 0;
            margin-top: 60px;
        }

        .footer-text {
            opacity: 0.8;
            margin-top: 20px;
            font-size: 0.9rem;
        }

        .visit-counter {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 30px;
            display: inline-block;
            margin-top: 20px;
            font-weight: 600;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.1rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
            
            section {
                padding: 50px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Hero -->
    <header>
        <div class="header-decoration"></div>
        <div class="header-decoration"></div>
        <div class="container header-content">
            <div class="avatar">
                <i class="fas fa-laptop-code"></i>
            </div>
            <h1>Kidist Alemayehu</h1>
            <p class="subtitle">Software Engineering Student at AASTU</p>
            <div class="location">
                <i class="fas fa-map-marker-alt"></i>
                <span>Addis Ababa, Ethiopia</span>
            </div>
            
            <!-- Social Links -->
            <div class="social-links">
                <a href="https://linkedin.com/in/kidist-alemayehu" class="social-link" target="_blank">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="mailto:kidistdev@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://github.com/kidist311" class="social-link" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </div>
    </header>

    <!-- Tech Stack Section -->
    <section id="tech-stack">
        <div class="container">
            <h2 class="section-title">Tech Stack & Skills</h2>
            <div class="tech-grid">
                <!-- Programming Languages -->
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-cuttlefish"></i></div>
                    <div class="tech-name">C++</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-python"></i></div>
                    <div class="tech-name">Python</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-java"></i></div>
                    <div class="tech-name">Java</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-js"></i></div>
                    <div class="tech-name">JavaScript</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-php"></i></div>
                    <div class="tech-name">PHP</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-dart"></i></div>
                    <div class="tech-name">Dart</div>
                </div>
                
                <!-- Web Development -->
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-html5"></i></div>
                    <div class="tech-name">HTML5</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-react"></i></div>
                    <div class="tech-name">React</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-bootstrap"></i></div>
                    <div class="tech-name">Bootstrap</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-css3-alt"></i></div>
                    <div class="tech-name">Tailwind</div>
                </div>
                
                <!-- Mobile & Backend -->
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-flutter"></i></div>
                    <div class="tech-name">Flutter</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fas fa-database"></i></div>
                    <div class="tech-name">MySQL</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fas fa-database"></i></div>
                    <div class="tech-name">SQLite</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fas fa-fire"></i></div>
                    <div class="tech-name">Firebase</div>
                </div>
                
                <!-- Tools -->
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-git-alt"></i></div>
                    <div class="tech-name">Git</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fab fa-github"></i></div>
                    <div class="tech-name">GitHub</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fas fa-rocket"></i></div>
                    <div class="tech-name">Vercel</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon"><i class="fas fa-server"></i></div>
                    <div class="tech-name">Apache</div>
                </div>
            </div>
        </div>
    </section>

    <!-- GitHub & Achievements -->
    <section id="github-stats">
        <div class="container">
            <h2 class="section-title">GitHub Achievements</h2>
            <div class="stats-container">
                <p style="text-align: center; margin-bottom: 20px; color: var(--gray);">
                    Proudly showcasing my coding journey and contributions
                </p>
                
                <div class="trophy-container">
                    <div class="trophy">
                        <i class="fas fa-trophy"></i>
                        <span>Gold</span>
                    </div>
                    <div class="trophy">
                        <i class="fas fa-trophy"></i>
                        <span>Silver</span>
                    </div>
                    <div class="trophy">
                        <i class="fas fa-trophy"></i>
                        <span>Bronze</span>
                    </div>
                    <div class="trophy">
                        <i class="fas fa-star"></i>
                        <span>Stars</span>
                    </div>
                    <div class="trophy">
                        <i class="fas fa-code-branch"></i>
                        <span>Forks</span>
                    </div>
                    <div class="trophy">
                        <i class="fas fa-heart"></i>
                        <span>Support</span>
                    </div>
                </div>
                
                <div style="text-align: center; margin-top: 30px;">
                    <a href="https://github.com/kidist311" class="social-link" target="_blank" style="display: inline-flex; text-decoration: none;">
                        <i class="fab fa-github"></i> 
                        <span style="margin-left: 10px; font-weight: 600;">Visit My GitHub</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <h3 style="font-size: 1.8rem; margin-bottom: 20px;">Let's Connect!</h3>
            <p>Always open to new opportunities, collaborations, and interesting tech discussions.</p>
            
            <div class="social-links" style="margin: 30px 0;">
                <a href="https://linkedin.com/in/kidist-alemayehu" class="social-link" target="_blank">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="mailto:kidistdev@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://github.com/kidist311" class="social-link" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
            </div>
            
            <div class="visit-counter">
                <i class="fas fa-eye"></i> 
                <span id="visitCount">0</span> Visits
            </div>
            
            <p class="footer-text">
                &copy; 2023 Kidist Alemayehu. Software Engineering Student at AASTU.<br>
                Built with passion and dedication to technology.
            </p>
        </div>
    </footer>

    <script>
        // Simple visit counter simulation
        document.addEventListener('DOMContentLoaded', function() {
            // Generate a random visit count between 50 and 200
            const visitCount = Math.floor(Math.random() * 150) + 50;
            document.getElementById('visitCount').textContent = visitCount.toLocaleString();
            
            // Add hover effects to tech items
            const techItems = document.querySelectorAll('.tech-item');
            techItems.forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px)';
                });
                
                item.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });
        });
    </script>
</body>
</html>
