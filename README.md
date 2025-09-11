<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dhiraj Kumar - GitHub Profile</title>
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
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            margin-bottom: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            animation: fadeIn 1.5s ease-out;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45aaf2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        h2 {
            font-size: 2.2rem;
            margin: 40px 0 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #4ecdc4;
            color: #4ecdc4;
        }
        
        h3 {
            font-size: 1.8rem;
            margin: 30px 0 15px;
            color: #45aaf2;
        }
        
        .tagline {
            font-size: 1.4rem;
            color: #c9d1d9;
            margin-bottom: 20px;
        }
        
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: slideUp 1s ease-out;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
        }
        
        .full-width {
            grid-column: 1 / span 2;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
            overflow: hidden;
        }
        
        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        th {
            background: rgba(78, 205, 196, 0.2);
            color: #4ecdc4;
            font-weight: 600;
        }
        
        tr {
            transition: background 0.3s ease;
        }
        
        tr:hover {
            background: rgba(255, 255, 255, 0.05);
        }
        
        .status {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: 500;
            background: rgba(69, 170, 242, 0.2);
            color: #45aaf2;
            animation: pulse 2s infinite;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            border-left: 4px solid #4ecdc4;
        }
        
        .tech-item:hover {
            background: rgba(78, 205, 196, 0.1);
            transform: translateY(-3px);
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .stat-value {
            font-size: 2.5rem;
            font-weight: 700;
            color: #ff6b6b;
            margin: 10px 0;
        }
        
        .stat-label {
            color: #c9d1d9;
            font-size: 1.1rem;
        }
        
        .snake-container {
            margin-top: 50px;
            text-align: center;
            padding: 20px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 15px;
        }
        
        .snake-animation {
            height: 150px;
            background: #0d1b23;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            position: relative;
        }
        
        .snake {
            position: absolute;
            width: 300px;
            height: 30px;
            background: linear-gradient(90deg, #4ecdc4, #45aaf2, #ff6b6b);
            border-radius: 15px;
            animation: slither 8s infinite ease-in-out;
        }
        
        .snake::before, .snake::after {
            content: '';
            position: absolute;
            background: #ff6b6b;
            border-radius: 50%;
        }
        
        .snake::before {
            width: 30px;
            height: 30px;
            left: -15px;
            top: 0;
        }
        
        .snake::after {
            width: 20px;
            height: 20px;
            right: -10px;
            top: 5px;
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #8b949e;
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(30px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(69, 170, 242, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(69, 170, 242, 0); }
            100% { box-shadow: 0 0 0 0 rgba(69, 170, 242, 0); }
        }
        
        @keyframes slither {
            0% { transform: translateX(-300px) rotate(0deg); }
            25% { transform: translateX(300px) rotate(5deg); }
            50% { transform: translateX(-300px) rotate(-5deg); }
            75% { transform: translateX(300px) rotate(3deg); }
            100% { transform: translateX(-300px) rotate(0deg); }
        }
        
        /* Responsive design */
        @media (max-width: 900px) {
            .container {
                grid-template-columns: 1fr;
            }
            
            .full-width {
                grid-column: 1;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Dhiraj Kumar Sharma</h1>
        <p class="tagline">Data Science & Machine Learning Enthusiast</p>
        <p>Turning data into insights and coffee into code <i class="fas fa-coffee"></i></p>
    </header>
    
    <div class="container">
        <div class="card full-width">
            <h2><i class="fas fa-bullseye"></i> 2025 Goals</h2>
            <table>
                <thead>
                    <tr>
                        <th>Goal</th>
                        <th>Status</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Master Machine Learning</td>
                        <td><span class="status">In Progress</span></td>
                    </tr>
                    <tr>
                        <td>Complete 100+ ML practice problems</td>
                        <td><span class="status">In Progress</span></td>
                    </tr>
                    <tr>
                        <td>Contribute to open-source projects</td>
                        <td><span class="status">In Progress</span></td>
                    </tr>
                    <tr>
                        <td>Build a full Data Science portfolio</td>
                        <td><span class="status">In Progress</span></td>
                    </tr>
                </tbody>
            </table>
        </div>
        
        <div class="card">
            <h2><i class="fas fa-laptop-code"></i> Data Science & ML</h2>
            <div class="tech-grid">
                <div class="tech-item">PYTHON</div>
                <div class="tech-item">NUMPY</div>
                <div class="tech-item">PANDAS</div>
                <div class="tech-item">SCIKIT-LEARN</div>
                <div class="tech-item">TENSORFLOW</div>
                <div class="tech-item">JUPYTER</div>
            </div>
        </div>
        
        <div class="card">
            <h2><i class="fas fa-code"></i> Web Development</h2>
            <div class="tech-grid">
                <div class="tech-item">HTML5</div>
                <div class="tech-item">CSS3</div>
                <div class="tech-item">JAVASCRIPT</div>
                <div class="tech-item">REACT</div>
                <div class="tech-item">NODE.JS</div>
                <div class="tech-item">EXPRESS.JS</div>
                <div class="tech-item">MONGODB</div>
            </div>
        </div>
        
        <div class="card full-width">
            <h2><i class="fas fa-chart-line"></i> GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-value">56</div>
                    <div class="stat-label">Total Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">0</div>
                    <div class="stat-label">Total Stars Earned</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">0</div>
                    <div class="stat-label">Total PRs</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">0</div>
                    <div class="stat-label">Total Issues</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">74</div>
                    <div class="stat-label">Total Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">3</div>
                    <div class="stat-label">Longest Streak</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">1</div>
                    <div class="stat-label">Current Streak</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="snake-container">
        <h2><i class="fas fa-gamepad"></i> Contribution Snake</h2>
        <div class="snake-animation">
            <div class="snake"></div>
        </div>
        <p style="margin-top: 15px;">Animated visualization of my GitHub contributions</p>
    </div>
    
    <footer>
        <p>© 2023 Dhiraj Kumar Sharma | Made with <i class="fas fa-heart" style="color: #ff6b6b;"></i></p>
    </footer>

    <script>
        // Add slight delay to animations for better visual effect
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            cards.forEach((card, index) => {
                card.style.animationDelay = `${index * 0.1}s`;
            });
        });
    </script>
</body>
</html>
