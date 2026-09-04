<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Aditya Mamidala | Cybersecurity Portfolio</title>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">

    <!-- Icons -->
    <link rel="stylesheet"
          href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

    <style>

        /* =========================
           GLOBAL
        ========================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: "Inter", sans-serif;
            background: #05070d;
            color: #e6edf3;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ::selection {
            background: #58a6ff;
            color: #05070d;
        }


        /* =========================
           ANIMATED BACKGROUND
        ========================= */

        .background {
            position: fixed;
            inset: 0;
            z-index: -2;
            overflow: hidden;
            background:
                radial-gradient(circle at 15% 20%, rgba(88,166,255,.12), transparent 30%),
                radial-gradient(circle at 85% 70%, rgba(139,92,246,.12), transparent 30%),
                #05070d;
        }

        .grid {
            position: absolute;
            inset: 0;

            background-image:
                linear-gradient(rgba(88,166,255,.035) 1px, transparent 1px),
                linear-gradient(90deg, rgba(88,166,255,.035) 1px, transparent 1px);

            background-size: 45px 45px;

            animation: gridMove 15s linear infinite;
        }

        @keyframes gridMove {
            from {
                transform: translateY(0);
            }

            to {
                transform: translateY(45px);
            }
        }

        .orb {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            animation: float 8s ease-in-out infinite;
        }

        .orb.one {
            width: 300px;
            height: 300px;
            background: #1473e6;
            opacity: .12;
            top: 10%;
            left: -100px;
        }

        .orb.two {
            width: 350px;
            height: 350px;
            background: #7c3aed;
            opacity: .10;
            right: -100px;
            bottom: 10%;
            animation-delay: 2s;
        }

        @keyframes float {
            0%,100% {
                transform: translate(0,0);
            }

            50% {
                transform: translate(30px,-40px);
            }
        }


        /* =========================
           NAVBAR
        ========================= */

        nav {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);

            width: min(1100px, 92%);

            display: flex;
            justify-content: space-between;
            align-items: center;

            padding: 15px 22px;

            background: rgba(13,17,23,.75);
            border: 1px solid rgba(88,166,255,.15);

            backdrop-filter: blur(18px);

            border-radius: 16px;

            z-index: 1000;
        }

        .logo {
            font-family: "JetBrains Mono", monospace;
            font-weight: 600;
            color: #58a6ff;
        }

        .logo span {
            color: #8b5cf6;
        }

        nav ul {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        nav a {
            color: #9da7b3;
            font-size: 14px;
            transition: .3s;
        }

        nav a:hover {
            color: #58a6ff;
        }


        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;
            justify-content: center;

            padding: 120px 20px 60px;
        }

        .hero-container {
            max-width: 1100px;
            width: 100%;

            display: grid;
            grid-template-columns: 1.3fr .7fr;

            gap: 70px;
            align-items: center;
        }

        .terminal {
            font-family: "JetBrains Mono", monospace;
            color: #58a6ff;
            font-size: 14px;
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: clamp(45px, 7vw, 82px);
            line-height: 1;

            letter-spacing: -4px;

            margin-bottom: 20px;
        }

        .hero h1 span {
            color: transparent;

            background: linear-gradient(
                90deg,
                #58a6ff,
                #8b5cf6,
                #58a6ff
            );

            background-size: 200%;

            -webkit-background-clip: text;
            background-clip: text;

            animation: gradient 4s linear infinite;
        }

        @keyframes gradient {
            to {
                background-position: 200%;
            }
        }

        .typing {
            font-family: "JetBrains Mono", monospace;

            font-size: 18px;

            color: #8b5cf6;

            min-height: 28px;
            margin-bottom: 25px;
        }

        .hero p {
            color: #8b949e;

            max-width: 650px;

            line-height: 1.8;
            font-size: 16px;
        }

        .buttons {
            display: flex;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 13px 20px;

            border-radius: 10px;

            border: 1px solid rgba(88,166,255,.3);

            font-size: 14px;
            font-weight: 600;

            transition: .3s;
        }

        .btn.primary {
            background: #58a6ff;
            color: #05070d;
        }

        .btn.secondary {
            background: rgba(88,166,255,.05);
            color: #58a6ff;
        }

        .btn:hover {
            transform: translateY(-4px);

            box-shadow:
                0 10px 30px rgba(88,166,255,.15);
        }


        /* =========================
           CYBER CORE
        ========================= */

        .cyber-core {
            width: 280px;
            height: 280px;

            margin: auto;

            position: relative;

            display: flex;
            justify-content: center;
            align-items: center;
        }

        .ring {
            position: absolute;

            border-radius: 50%;

            border: 1px solid #58a6ff;
        }

        .ring.one {
            width: 280px;
            height: 280px;

            border-style: dashed;

            animation: rotate 12s linear infinite;
        }

        .ring.two {
            width: 220px;
            height: 220px;

            border-color: #8b5cf6;

            border-style: dotted;

            animation: rotateReverse 8s linear infinite;
        }

        .ring.three {
            width: 150px;
            height: 150px;

            box-shadow:
                0 0 40px rgba(88,166,255,.3);

            animation: pulse 2s infinite;
        }

        .core {
            width: 75px;
            height: 75px;

            border-radius: 50%;

            background:
                radial-gradient(circle, #58a6ff, #8b5cf6);

            box-shadow:
                0 0 50px rgba(88,166,255,.7);

            display: flex;
            justify-content: center;
            align-items: center;

            font-size: 30px;
        }

        @keyframes rotate {
            to {
                transform: rotate(360deg);
            }
        }

        @keyframes rotateReverse {
            to {
                transform: rotate(-360deg);
            }
        }

        @keyframes pulse {
            0%,100% {
                transform: scale(1);
                opacity: .7;
            }

            50% {
                transform: scale(1.12);
                opacity: 1;
            }
        }


        /* =========================
           SECTION
        ========================= */

        section {
            max-width: 1100px;

            margin: auto;

            padding: 110px 20px;
        }

        .section-label {
            font-family: "JetBrains Mono", monospace;

            color: #58a6ff;

            font-size: 13px;

            letter-spacing: 2px;

            margin-bottom: 10px;
        }

        section h2 {
            font-size: 38px;
            margin-bottom: 40px;
        }


        /* =========================
           ABOUT
        ========================= */

        .about-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 25px;
        }

        .card {
            background: rgba(13,17,23,.65);

            border: 1px solid rgba(88,166,255,.12);

            border-radius: 18px;

            padding: 30px;

            backdrop-filter: blur(12px);

            transition: .4s;
        }

        .card:hover {
            transform: translateY(-7px);

            border-color: rgba(88,166,255,.4);

            box-shadow:
                0 15px 45px rgba(0,0,0,.3),
                0 0 25px rgba(88,166,255,.05);
        }

        .card h3 {
            margin-bottom: 15px;
        }

        .card p {
            color: #8b949e;
            line-height: 1.8;
        }

        .terminal-box {
            font-family: "JetBrains Mono", monospace;

            background: #080b12;

            border-radius: 12px;

            padding: 20px;

            color: #8b949e;

            line-height: 2;
        }

        .terminal-box .blue {
            color: #58a6ff;
        }

        .terminal-box .purple {
            color: #8b5cf6;
        }

        .terminal-box .green {
            color: #3fb950;
        }


        /* =========================
           SKILLS
        ========================= */

        .skills {
            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 15px;
        }

        .skill {
            padding: 25px;

            text-align: center;

            background: rgba(13,17,23,.7);

            border: 1px solid rgba(88,166,255,.1);

            border-radius: 15px;

            transition: .3s;
        }

        .skill i {
            font-size: 32px;

            color: #58a6ff;

            margin-bottom: 12px;
        }

        .skill h4 {
            font-size: 14px;
        }

        .skill:hover {
            transform: translateY(-5px) scale(1.02);

            border-color: #58a6ff;

            box-shadow:
                0 0 25px rgba(88,166,255,.1);
        }


        /* =========================
           PROJECTS
        ========================= */

        .projects {
            display: grid;

            grid-template-columns:
                repeat(2, 1fr);

            gap: 25px;
        }

        .project {
            position: relative;

            overflow: hidden;
        }

        .project-number {
            font-family: "JetBrains Mono", monospace;

            color: #58a6ff;

            font-size: 12px;

            margin-bottom: 15px;
        }

        .project h3 {
            font-size: 22px;

            margin-bottom: 12px;
        }

        .project p {
            color: #8b949e;

            line-height: 1.7;

            margin-bottom: 20px;
        }

        .tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }

        .tag {
            padding: 6px 10px;

            border-radius: 6px;

            background: rgba(88,166,255,.08);

            color: #58a6ff;

            font-family: "JetBrains Mono", monospace;

            font-size: 11px;
        }


        /* =========================
           CONTACT
        ========================= */

        .contact {
            text-align: center;

            padding-bottom: 150px;
        }

        .contact p {
            max-width: 600px;

            margin: auto;

            color: #8b949e;

            line-height: 1.8;
        }

        .socials {
            margin-top: 30px;

            display: flex;

            justify-content: center;

            gap: 15px;
        }

        .social {
            width: 50px;
            height: 50px;

            display: flex;

            justify-content: center;
            align-items: center;

            border-radius: 12px;

            border: 1px solid rgba(88,166,255,.2);

            color: #8b949e;

            transition: .3s;
        }

        .social:hover {
            color: #58a6ff;

            border-color: #58a6ff;

            transform: translateY(-5px);
        }


        /* =========================
           FOOTER
        ========================= */

        footer {
            border-top: 1px solid rgba(88,166,255,.1);

            padding: 25px;

            text-align: center;

            color: #586069;

            font-family: "JetBrains Mono", monospace;

            font-size: 12px;
        }


        /* =========================
           RESPONSIVE
        ========================= */

        @media(max-width: 850px) {

            nav ul {
                display: none;
            }

            .hero-container {
                grid-template-columns: 1fr;

                text-align: center;
            }

            .hero p {
                margin: auto;
            }

            .buttons {
                justify-content: center;
            }

            .cyber-core {
                width: 220px;
                height: 220px;
            }

            .ring.one {
                width: 220px;
                height: 220px;
            }

            .ring.two {
                width: 170px;
                height: 170px;
            }

            .ring.three {
                width: 120px;
                height: 120px;
            }

            .about-grid,
            .projects {
                grid-template-columns: 1fr;
            }

            .skills {
                grid-template-columns:
                    repeat(2,1fr);
            }
        }

        @media(max-width: 450px) {

            .hero h1 {
                font-size: 45px;
            }

            section h2 {
                font-size: 30px;
            }

            .skills {
                grid-template-columns: 1fr;
            }
        }

    </style>
</head>

<body>

<!-- Animated Background -->

<div class="background">

    <div class="grid"></div>

    <div class="orb one"></div>

    <div class="orb two"></div>

</div>


<!-- NAVIGATION -->

<nav>

    <div class="logo">
        ADITYA<span>_</span>
    </div>

    <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>

</nav>


<!-- HERO -->

<header class="hero">

    <div class="hero-container">

        <div>

            <div class="terminal">
                &gt; initializing_profile...
            </div>

            <h1>
                ADITYA<br>
                <span>MAMIDALA</span>
            </h1>

            <div class="typing">
                <span id="typing"></span><span>|</span>
            </div>

            <p>
                B.Tech Computer Science student focused on
                cybersecurity, programming, networking and
                Linux. Learning, building and exploring technology
                one project at a time.
            </p>

            <div class="buttons">

                <a class="btn primary"
                   href="https://aditya-mamidala.github.io/aditya-portfolio/"
                   target="_blank">
                    <i class="fa-solid fa-globe"></i>
                    View Portfolio
                </a>

                <a class="btn secondary"
                   href="https://www.linkedin.com/in/aditya-mamidala-487410428/"
                   target="_blank">
                    <i class="fa-brands fa-linkedin"></i>
                    LinkedIn
                </a>

            </div>

        </div>


        <!-- CYBER CORE -->

        <div class="cyber-core">

            <div class="ring one"></div>

            <div class="ring two"></div>

            <div class="ring three"></div>

            <div class="core">
                <i class="fa-solid fa-shield-halved"></i>
            </div>

        </div>

    </div>

</header>


<!-- ABOUT -->

<section id="about">

    <div class="section-label">
        01 / ABOUT_ME
    </div>

    <h2>
        Who I Am
    </h2>

    <div class="about-grid">

        <div class="card">

            <h3>
                <i class="fa-solid fa-user"></i>
                About Me
            </h3>

            <p>
                I'm Aditya Mamidala, a B.Tech Computer Science
                student with a growing interest in cybersecurity.
                I'm developing my skills in programming,
                networking, Linux and security fundamentals.
            </p>

        </div>


        <div class="card">

            <h3>
                <i class="fa-solid fa-terminal"></i>
                Terminal
            </h3>

            <div class="terminal-box">

                <div>
                    <span class="blue">$ whoami</span>
                </div>

                <div>
                    aditya@cyber-lab
                </div>

                <br>

                <div>
                    <span class="blue">$ focus</span>
                </div>

                <div>
                    <span class="purple">
                        Cybersecurity
                    </span>
                </div>

                <br>

                <div>
                    <span class="blue">$ status</span>
                </div>

                <div>
                    <span class="green">
                        Learning & Building
                    </span>
                </div>

            </div>

        </div>

    </div>

</section>


<!-- SKILLS -->

<section id="skills">

    <div class="section-label">
        02 / TECH_STACK
    </div>

    <h2>
        Technical Skills
    </h2>

    <div class="skills">

        <div class="skill">
            <i class="fa-brands fa-python"></i>
            <h4>Python</h4>
        </div>

        <div class="skill">
            <i class="fa-solid fa-c"></i>
            <h4>C</h4>
        </div>

        <div class="skill">
            <i class="fa-brands fa-java"></i>
            <h4>Java</h4>
        </div>

        <div class="skill">
            <i class="fa-brands fa-linux"></i>
            <h4>Linux</h4>
        </div>

        <div class="skill">
            <i class="fa-solid fa-network-wired"></i>
            <h4>Networking</h4>
        </div>

        <div class="skill">
            <i class="fa-solid fa-shield-halved"></i>
            <h4>Cybersecurity</h4>
        </div>

        <div class="skill">
            <i class="fa-brands fa-git-alt"></i>
            <h4>Git</h4>
        </div>

        <div class="skill">
            <i class="fa-brands fa-github"></i>
            <h4>GitHub</h4>
        </div>

    </div>

</section>


<!-- PROJECTS -->

<section id="projects">

    <div class="section-label">
        