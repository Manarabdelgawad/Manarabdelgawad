<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manar AbdElgawad - AI Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #f0f6fc;
            line-height: 1.6;
            padding: 2rem;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 3rem 0;
            position: relative;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(90deg, #ffa116, #ffd166, #06d6a0);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            position: relative;
            display: inline-block;
        }
        
        h1::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #ffa116, #06d6a0);
            border-radius: 2px;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: #c9d1d9;
        }
        
        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transition: transform 0.5s ease;
            margin: 0 auto 2rem;
            display: block;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
        }
        
        .section {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: #ffa116;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            font-size: 1.5rem;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .contact-item:hover {
            background: rgba(255, 255, 255, 0.12);
            transform: translateY(-3px);
        }
        
        .contact-item i {
            color: #ffa116;
            font-size: 1.2rem;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 12px;
            color: #f0f6fc;
            font-size: 1.8rem;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .social-link:hover::before {
            left: 100%;
        }
        
        .social-link.linkedin:hover {
            background: #0a66c2;
        }
        
        .social-link.leetcode:hover {
            background: #ffa116;
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 1.5rem;
        }
        
        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            padding: 1.5rem 1rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .skill-icon {
            font-size: 2.5rem;
            color: #ffa116;
        }
        
        .skill-name {
            font-size: 0.9rem;
            text-align: center;
        }
        
        .specialization-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .specialization-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 2rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .specialization-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
        }
        
        .cv-card::before {
            background: linear-gradient(90deg, #ff6b6b, #ffa116);
        }
        
        .nlp-card::before {
            background: linear-gradient(90deg, #4ecdc4, #06d6a0);
        }
        
        .specialization-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .specialization-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .specialization-title i {
            font-size: 1.8rem;
        }
        
        .cv-title {
            color: #ffa116;
        }
        
        .nlp-title {
            color: #06d6a0;
        }
        
        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 1rem;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            transition: all 0.3s ease;
        }
        
        .tech-item:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: scale(1.05);
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .stat-title {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: #ffa116;
        }
        
        .stat-img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        footer {
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #8b949e;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .contact-info {
                flex-direction: column;
            }
            
            .skills-container {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
            
            .specialization-container {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="https://i.pinimg.com/564x/d4/ba/b7/d4bab77b22ad2499b69b534f74f32bc4.jpg" alt="Manar AbdElgawad" class="profile-img">
            <h1>Hi, I'm Manar AbdElgawad</h1>
            <p class="tagline">AI Engineer | Specialized in Computer Vision & NLP</p>
        </header>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-envelope"></i> Reach Me</h2>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>manarabdelgawad11@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fab fa-kaggle"></i>
                    <span>kaggle.com/manarabdelgawad</span>
                </div>
            </div>
            <div class="social-links">
                <a href="https://linkedin.com/in/manar-abdelgawad" target="_blank" class="social-link linkedin">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://leetcode.com/u/Manar_Hammad/" target="_blank" class="social-link leetcode">
                    <i class="fas fa-code"></i>
                </a>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-brain"></i> AI Specializations</h2>
            <div class="specialization-container">
                <div class="specialization-card cv-card">
                    <h3 class="specialization-title cv-title"><i class="fas fa-eye"></i> Computer Vision</h3>
                    <p>Developing intelligent systems that can interpret and understand visual data from the world.</p>
                    <div class="tech-list">
                        <div class="tech-item">OpenCV</div>
                        <div class="tech-item">YOLO</div>
                        <div class="tech-item">CNN</div>
                        <div class="tech-item">Image Processing</div>
                        <div class="tech-item">Object Detection</div>
                        <div class="tech-item">Image Segmentation</div>
                    </div>
                </div>
                <div class="specialization-card nlp-card">
                    <h3 class="specialization-title nlp-title"><i class="fas fa-language"></i> Natural Language Processing</h3>
                    <p>Building systems that understand, interpret, and generate human language.</p>
                    <div class="tech-list">
                        <div class="tech-item">Transformers</div>
                        <div class="tech-item">BERT</div>
                        <div class="tech-item">NLTK</div>
                        <div class="tech-item">spaCy</div>
                        <div class="tech-item">Text Classification</div>
                        <div class="tech-item">Sentiment Analysis</div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-tools"></i> Languages & Tools</h2>
            <div class="skills-container">
                <div class="skill-item">
                    <i class="fab fa-python skill-icon"></i>
                    <span class="skill-name">Python</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-java skill-icon"></i>
                    <span class="skill-name">Java</span>
                </div>
                <div class="skill-item">
                    <i class="fas fa-plus skill-icon"></i>
                    <span class="skill-name">C++</span>
                </div>
                <div class="skill-item">
                    <i class="fas fa-cube skill-icon"></i>
                    <span class="skill-name">NumPy</span>
                </div>
                <div class="skill-item">
                    <i class="fas fa-table skill-icon"></i>
                    <span class="skill-name">Pandas</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-google skill-icon"></i>
                    <span class="skill-name">TensorFlow</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-php skill-icon"></i>
                    <span class="skill-name">PHP</span>
                </div>
                <div class="skill-item">
                    <i class="fas fa-database skill-icon"></i>
                    <span class="skill-name">MySQL</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-html5 skill-icon"></i>
                    <span class="skill-name">HTML5</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-css3-alt skill-icon"></i>
                    <span class="skill-name">CSS3</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-android skill-icon"></i>
                    <span class="skill-name">Android</span>
                </div>
                <div class="skill-item">
                    <i class="fab fa-pytorch skill-icon"></i>
                    <span class="skill-name">PyTorch</span>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-chart-line"></i> My Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <h3 class="stat-title">GitHub Statistics</h3>
                    <img src="https://github-readme-stats.vercel.app/api?username=ManarAbdelgawad&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&locale=en&hide_border=false&order=1&theme=dark" alt="GitHub Stats" class="stat-img">
                </div>
                <div class="stat-card">
                    <h3 class="stat-title">Top Languages</h3>
                    <img src="https://github-readme-stats.vercel.app/api/top-langs?username=ManarAbdelgawad&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=6&hide_border=false&order=2&theme=dark" alt="Top Languages" class="stat-img">
                </div>
            </div>
        </section>
        
        <footer>
            <p>© 2023 Manar AbdElgawad | AI Engineer Specializing in Computer Vision & NLP</p>
        </footer>
    </div>
</body>
</html>
