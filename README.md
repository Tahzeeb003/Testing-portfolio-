<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tahzeeb - Manual QA Portfolio</title>
    <style>
        /* Basic Reset & Fonts */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: #ffffff;
            color: #333;
            line-height: 1.6;
        }

        /* Navigation Bar */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #1e3a8a;
        }
        .nav-links a {
            text-decoration: none;
            color: #4b5563;
            margin-left: 20px;
            font-weight: 600;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #1e3a8a;
        }

        /* Hero Section */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 60px 20px;
            max-width: 900px;
            margin: 0 auto;
        }
        .hero-text h1 {
            color: #1e3a8a;
            font-size: 48px;
            margin: 10px 0;
        }
        .hero-text h3 {
            color: #6b7280;
            font-size: 20px;
            font-weight: 600;
        }
        .hero-text p {
            color: #6b7280;
            max-width: 600px;
            margin: 15px auto;
        }
        .profile-img {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
            margin-top: 30px;
            border: 5px solid #fff;
        }

        /* Blue Stats Box */
        .stats-box {
            display: flex;
            justify-content: space-around;
            background-color: #3B82F6;
            border-radius: 15px;
            width: 100%;
            max-width: 700px;
            margin: 40px auto;
            padding: 20px;
            color: white;
        }
        .stat-item {
            text-align: center;
            flex: 1;
            border-right: 1px solid rgba(255,255,255,0.4);
        }
        .stat-item:last-child {
            border-right: none;
        }
        .stat-item h2 {
            font-size: 36px;
            margin-bottom: 5px;
        }
        .stat-item p {
            font-size: 12px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Skills Section */
        .skills-section {
            background-color: #f3f4f6;
            padding: 60px 20px;
            text-align: center;
        }
        .skills-section h2 {
            color: #1e3a8a;
            font-size: 32px;
            margin-bottom: 30px;
        }
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            max-width: 800px;
            margin: 0 auto;
        }
        .skill-tag {
            background-color: #fff;
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: 600;
            color: #1e3a8a;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        /* Projects Section */
        .projects-section {
            padding: 60px 20px;
            text-align: center;
            max-width: 900px;
            margin: 0 auto;
        }
        .projects-section h2 {
            color: #1e3a8a;
            font-size: 32px;
            margin-bottom: 40px;
        }
        .project-card {
            background: #fff;
            border: 1px solid #e5e7eb;
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            text-align: left;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        .project-card:hover {
            transform: translateY(-5px);
        }
        .project-card h3 {
            color: #1e3a8a;
            font-size: 24px;
            margin-bottom: 10px;
        }
        .project-card .role {
            color: #6b7280;
            font-size: 14px;
            margin-bottom: 15px;
            font-weight: 600;
        }
        .project-card ul {
            margin-left: 20px;
            color: #4b5563;
            margin-bottom: 20px;
        }
        .project-card li {
            margin-bottom: 8px;
        }
        .tags span {
            background-color: #eff6ff;
            color: #2563eb;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 12px;
            font-weight: 600;
            margin-right: 5px;
            display: inline-block;
            margin-bottom: 5px;
        }

        /* Contact Section */
        .contact-section {
            background-color: #1e3a8a;
            color: white;
            text-align: center;
            padding: 50px 20px;
        }
        .contact-section h2 {
            margin-bottom: 20px;
        }
        .contact-btn {
            display: inline-block;
            background-color: #3B82F6;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            margin: 10px;
            transition: background 0.3s;
        }
        .contact-btn:hover {
            background-color: #2563eb;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            nav { padding: 15px 20px; }
            .nav-links { display: none; } /* Mobile menu hidden for simplicity */
            .hero-text h1 { font-size: 36px; }
            .stats-box { flex-direction: column; gap: 20px; }
            .stat-item { border-right: none; border-bottom: 1px solid rgba(255,255,255,0.4); padding-bottom: 20px; }
            .stat-item:last-child { border-bottom: none; padding-bottom: 0; }
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <div class="logo">Tahzeeb.</div>
        <div class="nav-links">
            <a href="#skills">Skills Acquired</a>
            <a href="#projects">My Projects</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <!-- Main Hero Section -->
    <section class="hero">
        <div class="hero-text">
            <h3>Hi, my name is</h3>
            <h1>Tahzeeb Anwar</h1>
            <p>I have earned many skills and built industry grade projects using them. Explore my projects below.</p>
        </div>
        
        <!-- Profile Photo (Apna working link yahan daalein) -->
        <img src="https://drive.google.com/thumbnail?id=1MP9ny_f5rdGP3Jl7Z3qwTjeEjNMJrTwb&sz=w1000" alt="Tahzeeb" class="profile-img">

        <!-- Stats Box -->
        <div class="stats-box">
            <div class="stat-item">
                <h2>8</h2>
                <p>Verified<br>Skills</p>
            </div>
            <div class="stat-item">
                <h2>4</h2>
                <p>Professional<br>Projects</p>
            </div>
            <div class="stat-item">
                <h2>500+</h2>
                <p>Test Cases<br>Executed</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills-section" id="skills">
        <h2>Skills Acquired</h2>
        <div class="skills-grid">
            <div class="skill-tag">Manual Testing</div>
            <div class="skill-tag">UI Testing</div>
            <div class="skill-tag">Payment Testing</div>
            <div class="skill-tag">Regression Testing</div>
            <div class="skill-tag">Excel</div>
            <div class="skill-tag">Google Sheets</div>
            <div class="skill-tag">Google Drive</div>
            <div class="skill-tag">JIRA</div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects-section" id="projects">
        <h2>My Projects</h2>

        <!-- Project 1 -->
        <div class="project-card">
            <h3>🧾 QK Bills — Multi-Domain Billing Software</h3>
            <p class="role">Role: Freelance Manual Tester | Client: Codbos Software Pvt Ltd | Duration: 1+ Year</p>
            <ul>
                <li>Tested restaurant, pharmacy, and retail billing modules from project inception.</li>
                <li>Performed UI, payment, functional, retesting, and regression testing.</li>
                <li>Identified 50+ defects including 15+ critical payment-related issues.</li>
            </ul>
            <div class="tags">
                <span>Payment Testing</span>
                <span>Regression Testing</span>
                <span>Excel</span>
            </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
            <h3>🏫 Takshashila Vidyapith — School Website</h3>
            <p class="role">Role: Freelance Manual Tester | Client: Codbos Software Pvt Ltd | Duration: 2 Months</p>
            <ul>
                <li>A government school website tested across 5 roles: Admin, Super Admin, HOD, Teacher, Student.</li>
                <li>Performed role-based access, functional, UI, and regression testing.</li>
                <li>Ensured data privacy and verified that each role sees only authorized features.</li>
            </ul>
            <div class="tags">
                <span>Role-Based Testing</span>
                <span>UI Testing</span>
                <span>Google Sheets</span>
            </div>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
            <h3>📱 Quartros — Restaurant Android App</h3>
            <p class="role">Role: Freelance Manual Tester | Client: Codbos Software Pvt Ltd | Duration: 3 Months</p>
            <ul>
                <li>Tested a multi-branch restaurant app (launched on Play Store).</li>
                <li>Performed complete payment method testing and retesting.</li>
                <li>Currently involved in iOS testing to ensure cross-platform stability.</li>
            </ul>
            <div class="tags">
                <span>Mobile Testing</span>
                <span>Payment Testing</span>
                <span>Retesting</span>
            </div>
        </div>

        <!-- Project 4 -->
        <div class="project-card">
            <h3>🏡 Dream Plots — Real Estate Web Application</h3>
            <p class="role">Role: Manual QA Engineer | Duration: 3 Months</p>
            <ul>
                <li>Performed end-to-end testing of property listing, search, and booking workflows.</li>
                <li>Designed and executed 300+ test cases for login, filters, and dashboards.</li>
                <li>Conducted regression and cross-browser testing to ensure application stability.</li>
            </ul>
            <div class="tags">
                <span>Cross-Browser</span>
                <span>Test Case Design</span>
                <span>Bug Reporting</span>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section" id="contact">
        <h2>Connect With Me</h2>
        <p>Feel free to reach out for freelance projects or job opportunities.</p>
        <br>
        <!-- Apne actual links yahan daalein -->
        <a href="https://linkedin.com/in/YOUR_LINKEDIN" class="contact-btn" target="_blank">LinkedIn Profile</a>
        <a href="mailto:YOUR_EMAIL@gmail.com" class="contact-btn">Send an Email</a>
    </section>

</body>
</html>
