<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Behailu Yifru · CS profile</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts: Inter + Fira Code -->
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&family=Inter:ital,opsz,wght@0,14..32,400..700;1,14..32,400..700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #0a0c10 0%, #1a1e24 100%);
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 2rem 1.5rem;
            color: #e9edf2;
            line-height: 1.6;
        }

        .readme-card {
            max-width: 1100px;
            width: 100%;
            background: rgba(18, 22, 28, 0.9);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(66, 153, 225, 0.15);
            border-radius: 2.5rem;
            box-shadow: 0 30px 60px -15px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(0, 255, 255, 0.05) inset;
            overflow: hidden;
            padding: 2.8rem 2.8rem;
            transition: all 0.3s ease;
        }

        /* floating accent line */
        .readme-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 10%;
            width: 80%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #3b82f6, #8b5cf6, #3b82f6, transparent);
            border-radius: 100%;
            filter: blur(1px);
        }

        .relative {
            position: relative;
        }

        /* header section — name + titles */
        .name-title {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2.2rem;
            border-bottom: 1px dashed rgba(100, 150, 255, 0.25);
            padding-bottom: 1.8rem;
        }

        .name-section h1 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(to right, #ffffff, #b4d0ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1.2;
            text-shadow: 0 2px 5px rgba(0,40,100,0.5);
        }

        .badge-container {
            display: flex;
            gap: 0.75rem;
            flex-wrap: wrap;
            margin-top: 0.5rem;
        }

        .badge {
            background: rgba(15, 25, 40, 0.8);
            border: 1px solid #2a3a55;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            color: #cbd5e0;
            backdrop-filter: blur(4px);
        }

        .badge i {
            color: #3b82f6;
            font-size: 0.9rem;
        }

        .status-pulse {
            display: flex;
            align-items: center;
            gap: 10px;
            background: #0e1a28;
            padding: 0.6rem 1.4rem;
            border-radius: 60px;
            border: 1px solid #2d4a7a;
            box-shadow: 0 0 12px #1e3a5f;
        }

        .pulse-dot {
            width: 12px;
            height: 12px;
            background: #22c55e;
            border-radius: 50%;
            box-shadow: 0 0 10px #22c55e;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.6; transform: scale(1.2); }
            100% { opacity: 1; transform: scale(1); }
        }

        /* tagline matrix style */
        .matrix-tagline {
            font-family: 'Fira Code', monospace;
            font-size: 1.2rem;
            margin: 1.5rem 0 2rem 0;
            padding: 0.9rem 1.5rem;
            background: #0b1017;
            border-radius: 20px;
            border-left: 6px solid #3b82f6;
            border-right: 1px solid #2d4a7a;
            color: #a3c8ff;
            box-shadow: 0 6px 14px rgba(0,10,30,0.8);
            word-break: break-word;
        }

        .matrix-tagline i {
            color: #f97316;
            margin-right: 10px;
        }

        .matrix-tagline .cursor {
            background: #3b82f6;
            width: 10px;
            height: 1.4rem;
            display: inline-block;
            margin-left: 5px;
            animation: blink 1s infinite;
            vertical-align: middle;
        }

        @keyframes blink {
            0%,100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* 3 column stats / connect */
        .quick-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 1.5rem;
            margin: 2.5rem 0 2.8rem;
        }

        .info-cell {
            background: rgba(10, 18, 28, 0.7);
            border: 1px solid #253549;
            border-radius: 28px;
            padding: 1.2rem 0.8rem;
            text-align: center;
            backdrop-filter: blur(8px);
            transition: 0.2s;
        }

        .info-cell:hover {
            border-color: #3b82f6;
            transform: translateY(-3px);
            background: #0f1a29;
        }

        .info-cell i {
            font-size: 2rem;
            background: linear-gradient(145deg, #60a5fa, #a78bfa);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 8px;
        }

        .info-cell .label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #94a3b8;
        }

        .info-cell .value {
            font-size: 1.6rem;
            font-weight: 600;
            color: white;
        }

        /* social / contact strip */
        .social-orbit {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 2rem 0 2.5rem;
            justify-content: center;
        }

        .social-button {
            background: rgba(21, 31, 46, 0.8);
            border: 1px solid #2f405b;
            color: #dbecff;
            width: 48px;
            height: 48px;
            border-radius: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: 0.25s;
            backdrop-filter: blur(6px);
            text-decoration: none;
        }

        .social-button:hover {
            border-color: #3b82f6;
            color: #ffffff;
            background: #1e2a3a;
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 0 15px #3b82f6;
        }

        .contact-email {
            background: linear-gradient(135deg, #1e2b3c, #0f1a28);
            border-radius: 40px;
            padding: 0.6rem 1.8rem;
            border: 1px solid #3b82f6;
            color: white;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-size: 1.1rem;
            transition: 0.2s;
        }

        .contact-email i {
            color: #f97316;
        }

        .contact-email:hover {
            background: #1e3448;
            border-color: #f97316;
        }

        /* project highlights / github metrics */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.8rem;
            margin: 2.8rem 0 2.2rem;
        }

        .project-item {
            background: rgba(10, 18, 28, 0.5);
            border: 1px solid #2b384b;
            border-radius: 1.8rem;
            padding: 1.5rem 1.2rem;
            backdrop-filter: blur(8px);
            transition: 0.15s;
        }

        .project-item:hover {
            border-color: #3b82f6;
            background: #0f1b2b;
        }

        .project-icon {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .project-title a {
            color: white;
            text-decoration: none;
        }

        .project-title a:hover {
            text-decoration: underline;
            color: #90caf9;
        }

        .project-desc {
            color: #a0b8d1;
            font-size: 0.95rem;
            margin: 0.6rem 0;
        }

        .lang-stack {
            display: flex;
            gap: 12px;
            margin-top: 12px;
            font-size: 0.8rem;
            color: #7b98b9;
            flex-wrap: wrap;
        }

        .lang-stack span i {
            color: #eab308;
        }

        /* contribution section / activity */
        .activity-log {
            background: #0c131f;
            border-radius: 1.8rem;
            padding: 1.8rem 2rem;
            border: 1px solid #2d405a;
            margin: 2rem 0 1.5rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .activity-text {
            font-family: 'Fira Code', monospace;
            color: #b3d2ff;
        }

        .activity-text i {
            color: #3b82f6;
            margin-right: 8px;
        }

        .contribution-graph {
            display: flex;
            gap: 4px;
            align-items: center;
            flex-wrap: wrap;
        }

        .graph-box {
            width: 18px;
            height: 18px;
            background: #1b2a41;
            border-radius: 4px;
        }

        .graph-box.active {
            background: #3b82f6;
            box-shadow: 0 0 8px #3b82f6;
        }

        .graph-box.medium {
            background: #1d4a7a;
        }

        /* footer quote */
        .footer-quote {
            margin-top: 3rem;
            text-align: center;
            font-size: 1rem;
            color: #7f9bc0;
            border-top: 1px dashed #2a3f60;
            padding-top: 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .footer-quote .left {
            font-style: italic;
        }

        .footer-quote .right {
            font-family: 'Fira Code', monospace;
            font-size: 0.9rem;
            background: #0e1b2b;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            border: 1px solid #3b82f6;
        }

        /* responsiveness */
        @media (max-width: 700px) {
            .readme-card { padding: 1.8rem; }
            .name-section h1 { font-size: 2.4rem; }
            .status-pulse { margin-top: 15px; }
            .name-title { flex-direction: column; align-items: start; }
        }

        /* custom glitch effect for name */
        .glitch {
            position: relative;
        }
    </style>
</head>
<body>
    <div class="readme-card relative">
        <!-- small decorative -->
        <div style="position: absolute; top: 10px; right: 25px; opacity: 0.2; font-size: 1.8rem;">{CS}</div>

        <!-- HEADER: name + active status -->
        <div class="name-title">
            <div class="name-section">
                <h1 class="glitch">BEHAILU YIFRU</h1>
                <div class="badge-container">
                    <span class="badge"><i class="fas fa-terminal"></i> compsci · undergraduate</span>
                    <span class="badge"><i class="fas fa-location-dot"></i> Addis Ababa / remote</span>
                    <span class="badge"><i class="fas fa-code"></i> full‑stack builder</span>
                </div>
            </div>
            <div class="status-pulse">
                <span class="pulse-dot"></span>
                <span style="font-weight: 500; letter-spacing: 0.5px;">#OpenToIntern · fall 2025</span>
                <i class="fas fa-arrow-up-right-from-square" style="color:#6b9eff; font-size:0.9rem;"></i>
            </div>
        </div>

        <!-- matrix style tagline / intro -->
        <div class="matrix-tagline">
            <i class="fa-solid fa-chevron-right"></i> 
            <span style="color:#ffffff;">Behailu Yifru</span> · computer science student 
            <span style="color:#60a5fa;">&nbsp;&&&nbsp;</span>  problem solver 
            <span style="color:#f97316;">⚡</span> 
            <span style="color:#8b9dc3;">"code, learn, disrupt"</span>
            <span class="cursor"></span>
        </div>

        <!-- quick stats: years, projects, coffee, etc (professional) -->
        <div class="quick-info">
            <div class="info-cell">
                <i class="fa-regular fa-calendar"></i>
                <div class="label">experience</div>
                <div class="value">3+ years</div>
                <div style="font-size:0.8rem; color:#9ab0d1;">academic & personal</div>
            </div>
            <div class="info-cell">
                <i class="fa-regular fa-file-lines"></i>
                <div class="label">repos</div>
                <div class="value">24+</div>
                <div style="font-size:0.8rem; color:#9ab0d1;">public contributions</div>
            </div>
            <div class="info-cell">
                <i class="fa-solid fa-mug-hot"></i>
                <div class="label">commit fuel</div>
                <div class="value">∞</div>
                <div style="font-size:0.8rem; color:#9ab0d1;">caffeine & algorithms</div>
            </div>
            <div class="info-cell">
                <i class="fa-regular fa-star"></i>
                <div class="label">hackathons</div>
                <div class="value">5</div>
                <div style="font-size:0.8rem; color:#9ab0d1;">2x finalist</div>
            </div>
        </div>

        <!-- Connect / social / email - international style -->
        <div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 1rem;">
            <div class="social-orbit">
                <a href="#" class="social-button"><i class="fab fa-github"></i></a>
                <a href="#" class="social-button"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-button"><i class="fab fa-x-twitter"></i></a>
                <a href="#" class="social-button"><i class="fab fa-dev"></i></a>
                <a href="#" class="social-button"><i class="fab fa-discord"></i></a>
                <a href="#" class="social-button"><i class="fab fa-medium"></i></a>
            </div>
            <div class="contact-email">
                <i class="fa-regular fa-envelope"></i> behailu.yifru@cs.student
                <span style="background: #1e3a5f; border-radius: 20px; padding: 2px 8px; font-size:0.8rem;">GPG · 0xBEHA</span>
            </div>
        </div>

        <!-- featured projects / pin repos (advanced visual) -->
        <div style="margin: 2.8rem 0 1.2rem;">
            <div style="display: flex; gap: 0.8rem; align-items: center; margin-bottom: 1.8rem;">
                <i class="fa-solid fa-diagram-project" style="color: #3b82f6; font-size: 2rem;"></i>
                <span style="font-weight: 500; letter-spacing: 1px; font-size: 1.2rem; border-left: 2px solid #3b82f6; padding-left: 1rem;">Pinned repositories — innovation in progress</span>
            </div>
            <div class="project-grid">
                <!-- project 1 -->
                <div class="project-item">
                    <div class="project-icon"><i class="fa-regular fa-cube" style="color: #f97316;"></i></div>
                    <div class="project-title">
                        <a href="#">nexus-ds</a> <span style="color:#6b9eff; font-size:0.9rem;">★ 43</span>
                    </div>
                    <div class="project-desc">declarative data structures lib in Rust & Python · zero‑copy, ergonomic API.</div>
                    <div class="lang-stack">
                        <span><i class="fa-brands fa-rust"></i> Rust</span>
                        <span><i class="fa-brands fa-python"></i> Python</span>
                        <span>🔥 23 forks</span>
                    </div>
                </div>
                <!-- project 2 -->
                <div class="project-item">
                    <div class="project-icon"><i class="fa-regular fa-compass" style="color: #3b82f6;"></i></div>
                    <div class="project-title">
                        <a href="#">ethio‑learn</a> <span style="color:#6b9eff; font-size:0.9rem;">★ 67</span>
                    </div>
                    <div class="project-desc">localized DSA visualizer for Ethiopian students · Amharic / English.</div>
                    <div class="lang-stack">
                        <span><i class="fa-brands fa-js"></i> Next.js</span>
                        <span><i class="fa-regular fa-chart-scatter"></i> TS</span>
                        <span>⚡ 12 contributors</span>
                    </div>
                </div>
                <!-- project 3 -->
                <div class="project-item">
                    <div class="project-icon"><i class="fa-regular fa-gem" style="color: #a78bfa;"></i></div>
                    <div class="project-title">
                        <a href="#">zk‑vault</a> <span style="color:#6b9eff; font-size:0.9rem;">★ 21</span>
                    </div>
                    <div class="project-desc">minimal zero‑knowledge proof circuit for identity (academic research).</div>
                    <div class="lang-stack">
                        <span><i class="fa-regular fa-circle"></i> Circom</span>
                        <span><i class="fa-brands fa-ethereum"></i> Solidity</span>
                        <span>🧪 audit in progress</span>
                    </div>
                </div>
                <!-- project 4 -->
                <div class="project-item">
                    <div class="project-icon"><i class="fa-regular fa-cloud"></i></div>
                    <div class="project-title">
                        <a href="#">gridlock</a> <span style="color:#6b9eff;">★ 18</span>
                    </div>
                    <div class="project-desc">distributed task scheduler with Go + Redis, used for course project.</div>
                    <div class="lang-stack">
                        <span><i class="fa-brands fa-golang"></i> Go</span>
                        <span><i class="fa-regular fa-database"></i> Redis</span>
                        <span>⏱️ low‑latency</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Contribution / activity section (realistic github like) -->
        <div class="activity-log">
            <div class="activity-text">
                <i class="fa-regular fa-calendar-check"></i> 417 contributions in the last year
            </div>
            <div class="contribution-graph">
                <div class="graph-box active"></div><div class="graph-box active"></div><div class="graph-box medium"></div><div class="graph-box"></div><div class="graph-box active"></div>
                <div class="graph-box medium"></div><div class="graph-box active"></div><div class="graph-box active"></div><div class="graph-box"></div><div class="graph-box medium"></div>
                <div class="graph-box active"></div><div class="graph-box"></div><div class="graph-box medium"></div><div class="graph-box active"></div><div class="graph-box active"></div>
                <div class="graph-box medium"></div><div class="graph-box"></div><div class="graph-box active"></div><div class="graph-box active"></div>
                <span style="color:#94a3b8; font-size:0.8rem; margin-left:8px;">🔥 23 day streak</span>
            </div>
        </div>

        <!-- github metrics and current learning -->
        <div style="display: flex; gap: 1.2rem; flex-wrap: wrap; margin: 1.5rem 0 2rem;">
            <div style="background: #0e1724; border-radius: 50px; padding: 0.5rem 1.5rem; border:1px solid #2b405e;">
                <i class="fa-regular fa-brain" style="color:#f97316;"></i> currently: distributed systems · zk proofs
            </div>
            <div style="background: #0e1724; border-radius: 50px; padding: 0.5rem 1.5rem; border:1px solid #3b82f6;">
                <i class="fa-regular fa-code-pull-request"></i> 7 PRs merged (2025)
            </div>
            <div style="background: #0e1724; border-radius: 50px; padding: 0.5rem 1.5rem; border:1px solid #6b21a8;">
                <i class="fa-regular fa-award"></i> ICPC regional participant
            </div>
        </div>

        <!-- Footer / quote + visitor -->
        <div class="footer-quote">
            <div class="left">
                <i class="fa-solid fa-quote-left" style="opacity:0.6;"></i> 
                make it work, make it right, make it fast – then teach it.
            </div>
            <div class="right">
                <i class="fa-regular fa-eye"></i> profile visits: 1.8k 
                <span style="background:#2e4a7a; width:8px; height:8px; display:inline-block; border-radius: 50%; margin-left: 10px;"></span>
            </div>
        </div>

        <!-- hidden signature: always Behailu Yifru, CS student with international vibe -->
        <div style="margin-top: 1.5rem; font-size: 0.7rem; color: #3b5577; display: flex; justify-content: center; gap: 30px;">
            <span><i class="fa-regular fa-copyright"></i> behailu yifru · 2k25</span>
            <span>📍 addis ababa · san francisco (virtual)</span>
            <span><i class="fa-regular fa-shield-halved"></i> pgp available</span>
        </div>
    </div>
</body>
</html>
