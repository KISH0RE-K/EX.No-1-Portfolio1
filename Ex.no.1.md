# Ex01 Portfolio
## Date:29.08.2025
## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kishore K - Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #4dd0e1;
            --secondary-color: #26a69a;
            --accent-color: #ffb74d;
            --text-color: #e0e0e0;
            --light-bg: #212121;
            --dark-bg: #121212;
            --white: #ffffff;
            --shadow-light: 0 4px 8px rgba(0, 0, 0, 0.15);
            --shadow-medium: 0 6px 12px rgba(0, 0, 0, 0.25);
        }

        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.7;
            margin: 0;
            padding: 0;
            background-color: var(--dark-bg);
            color: var(--text-color);
            scroll-behavior: smooth;
        }

        header {
            background: linear-gradient(135deg, #1f1f1f, #2b2b2b);
            color: var(--white);
            padding: 2.5rem 0 1.5rem;
            text-align: center;
            position: relative;
            box-shadow: var(--shadow-medium);
        }

        .profile-pic {
            width: 160px;
            height: 160px;
            border-radius: 50%;
            border: 6px solid var(--primary-color);
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
            margin-bottom: 1rem;
            object-fit: cover;
            object-position: center;
            transition: transform 0.3s ease-in-out;
        }

        .profile-pic:hover {
            transform: scale(1.05) rotate(2deg);
        }

        header h1 {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            font-size: 3rem;
            font-weight: 700;
            letter-spacing: 1.5px;
            animation: fadeInDown 1s ease-out;
        }

        header p {
            font-size: 1.3rem;
            opacity: 0.95;
            margin-top: 0.5rem;
            animation: fadeInUp 1s ease-out 0.3s;
        }

        main {
            padding: 1.5rem 1rem;
            max-width: 960px;
            margin: auto;
            display: grid;
            gap: 1rem;
        }

        section {
            background: var(--light-bg);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: var(--shadow-medium);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            margin-bottom: 0.5rem;
        }

        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }

        h2 {
            font-family: 'Montserrat', sans-serif;
            color: var(--primary-color);
            border-bottom: 3px solid var(--secondary-color);
            padding-bottom: 0.75rem;
            margin-top: 0;
            margin-bottom: 1.5rem;
            font-size: 2.2rem;
            font-weight: 700;
        }

        .skills-container ul {
            list-style-type: none;
            padding: 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .skills-container li {
            background: #333;
            padding: 1rem 1.25rem;
            border-radius: 8px;
            border: 1px solid #444;
            transition: all 0.3s ease-in-out;
            display: flex;
            align-items: center;
        }

        .skills-container li:hover {
            background-color: var(--secondary-color);
            color: var(--white);
            border-color: var(--secondary-color);
            transform: scale(1.02);
        }

        .skills-container li strong {
            margin-right: 0.5rem;
            color: var(--primary-color);
        }

        .skills-container li:hover strong {
            color: var(--white);
        }

        .project-card,
        .hackathon-entry {
            border-left: 5px solid var(--primary-color);
            padding: 1.5rem;
            margin-bottom: 1rem;
            background: var(--dark-bg);
            border-radius: 8px;
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
            box-shadow: var(--shadow-light);
        }

        .project-card:last-of-type,
        .hackathon-entry:last-of-type {
            margin-bottom: 0;
        }

        .project-card:hover,
        .hackathon-entry:hover {
            transform: translateX(5px);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }

        .project-card h3,
        .hackathon-entry h3 {
            font-family: 'Montserrat', sans-serif;
            margin-top: 0;
            color: var(--primary-color);
            font-size: 1.6rem;
            margin-bottom: 0.75rem;
        }

        .project-card p,
        .hackathon-entry p {
            margin-bottom: 0.75rem;
        }

        a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease-in-out, text-decoration 0.3s ease-in-out;
        }

        a:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }

        #contact ul {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }

        #contact li {
            flex: 1 1 auto;
            max-width: 280px;
            text-align: center;
        }

        hr {
            border: 0;
            height: 1px;
            background-image: linear-gradient(to right, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.3), rgba(255, 255, 255, 0));
            margin: 1.5rem 0;
        }

        footer {
            text-align: center;
            padding: 1.5rem;
            background: #1f1f1f;
            color: var(--text-color);
            margin-top: 1.5rem;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            header p {
                font-size: 1rem;
            }
            h2 {
                font-size: 1.8rem;
            }
            .skills-container ul {
                grid-template-columns: 1fr;
            }
            #contact ul {
                flex-direction: column;
                align-items: center;
            }
            #contact li {
                max-width: 100%;
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <header>
        <img src="kishore.jpg" alt="Profile Picture of Kishore" class="profile-pic"> 
        <h1>KISHORE K</h1>
        <p>Software Developer | Data Enthusiast | Saveetha Engineering College, Chennai</p>
    </header>
    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>
                A passionate and results-driven individual with a strong foundation in computer science. I am enthusiastic about solving complex problems and building impactful applications. I am currently a student at **Saveetha Engineering College** in **Chennai, Tamil Nadu, India**. My expertise lies in full-stack development and machine learning, and I am always eager to learn new technologies.
            </p>
        </section>
        <hr>
        <section id="skills">
            <h2>Skills</h2>
            <div class="skills-container">
                <ul>
                    <li><strong>Programming Languages:</strong> Python, C, Java, JavaScript</li>
                    <li><strong>Web Technologies:</strong> HTML, CSS</li>
                    <li><strong>Databases:</strong> SQL</li>
                    <li><strong>Machine Learning:</strong> Scikit-learn, Pandas, TensorFlow</li>
                </ul>
            </div>
        </section>
        <hr>
        <section id="projects">
            <h2>Projects</h2>
            <div class="project-card">
                <h3>Smart Traffic Management System</h3>
                <p>Developed a real-time traffic prediction system for urban areas using machine learning algorithms and IoT sensor data to optimize traffic flow. A relevant project for **Chennai's** traffic challenges!</p>
                <p><strong>Technologies:</strong> Python (TensorFlow, Keras), Flask, JavaScript, PostgreSQL</p>
                <a href="https://github.com/yourusername/smart-traffic-system" target="_blank">View on GitHub</a>
            </div>
            <div class="project-card">
                <h3>E-commerce Product Recommender</h3>
                <p>Built a personalized product recommendation engine for an e-commerce platform, improving user engagement and sales using collaborative filtering and content-based filtering techniques.</p>
                <p><strong>Technologies:</strong> Python, Pandas, Scikit-learn, Django, HTML/CSS</p>
                <a href="https://github.com/yourusername/ecommerce-recommender" target="_blank">View on GitHub</a>
            </div>
        </section>
        <hr>
        <section id="hackathons">
            <h2>Hackathons</h2>
            <div class="hackathon-entry">
                <h3>Rajalakshmi Engineering College (Chennai) - "Innovate Chennai" Hackathon</h3>
                <p><strong>Project:</strong> A web-based application to track food waste in college canteens, providing analytics and suggesting optimization strategies.</p>
                <p><strong>Role:</strong> Led the backend development and database design using Python (Flask) and SQL.</p>
            </div>
            <div class="hackathon-entry">
                <h3>SRM Institute of Science and Technology (Chennai) - "Tech-Sparks" Hackathon</h3>
                <p><strong>Project:</strong> An AI-powered chatbot designed to assist students with campus information, course details, and event schedules, enhancing the student experience.</p>
                <p><strong>Role:</strong> Contributed to the natural language processing (NLP) model training and integration using Python.</p>
            </div>
            <div class="hackathon-entry">
                <h3>Anna University (Chennai) - "Smart City Solutions" Hackathon</h3>
                <p><strong>Project:</strong> A mobile-first web app for real-time traffic updates in Chennai, offering alternative routes and public transport information to commuters.</p>
                <p><strong>Role:</strong> Focused on front-end development and user interface design using HTML, CSS, and JavaScript, ensuring a smooth user experience.</p>
            </div>
        </section>
        <hr>
        <section id="contact">
            <h2>Contact</h2>
            <p>Feel free to connect with me! I'm always open to discussing new projects, creative ideas, or opportunities.</p>
            <ul>
                <li><strong>Email:</strong> <a href="mailto:kishore212010@gmail.com">kishore212010@gmail.com</a></li>
                <li><strong>Contact:</strong> <a href="tel:+919876543210">+91 98765 43210</a></li>
            </ul>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 Kishore K. All rights reserved. Made with ❤️ in Chennai.</p>
    </footer>
</body>
</html>
```

## OUTPUT
<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/31f4ad53-7977-443e-8f3d-1d5a276f3077" />
<img width="1920" height="1080" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/0db0711b-6ccc-425b-b060-f89bdb987544" />
<img width="1920" height="1080" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/57ac9355-04fd-4ef3-8517-82cc84cf2cdd" />
<img width="1920" height="1080" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/a26ce53e-b21a-4265-a31f-4fa719bf8d6f" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
