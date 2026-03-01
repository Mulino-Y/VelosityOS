--- FILE: D:\Window Tuning\Velosity_site\index.html ---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velocity - Windows Optimization Simplified</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <a href="index.html" class="navbar-logo">Velocity</a>
        <div class="nav-links">
            <a href="index.html" class="nav-button">Home</a>
            <a href="how-to-use/index.html" class="nav-button">How to use</a>
            <a href="how-to-install/index.html" class="nav-button">How to install</a>
            <a href="download/index.html" class="nav-button">Download</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <h1>Optimize Your Windows Experience</h1>
            <p>Velocity is your ultimate solution for optimizing your Windows system. Clean, boost, and optimize your computer for peak performance with professionally-designed tools.</p>
            <button class="download-btn" onclick="downloadFile()">Download Now</button>
        </div>
    </section>

    <script>
        function downloadFile() {
            const fileUrl = 'https://github.com/Mulino-Y/Velocity/releases/download/v4.2/velocity_setup.exe';
            const link = document.createElement('a');
            link.href = fileUrl;
            link.download = 'Velocity.exe';
            link.click();
        }
    </script>
</body>
</html>



--- FILE: D:\Window Tuning\Velosity_site\style.css ---
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #f7f9fc 0%, #eef2f7 100%);
    color: #1a202c;
    line-height: 1.6;
}

/* Navigation Bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 24px 64px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar-logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2563eb;
    text-decoration: none;
}

.nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
}

.nav-button {
    background: none;
    border: none;
    font-size: 1rem;
    font-weight: 500;
    color: #4b5563;
    cursor: pointer;
    text-decoration: none;
    padding: 8px 16px;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.nav-button:hover {
    color: #2563eb;
    background: rgba(37, 99, 235, 0.1);
}

/* Hero Section */
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 85vh;
    padding: 60px 24px;
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -10%;
    width: 500px;
    height: 500px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    animation: float 6s ease-in-out infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(30px); }
}

.hero-content {
    position: relative;
    z-index: 1;
    max-width: 700px;
}

.hero h1 {
    font-size: 3.5rem;
    font-weight: 700;
    color: white;
    margin-bottom: 24px;
    letter-spacing: -2px;
}

.hero p {
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 0.9);
    margin-bottom: 40px;
}

.hero .download-btn {
    background: white;
    color: #2563eb;
    border: none;
    padding: 16px 48px;
    font-size: 1.1rem;
    font-weight: 600;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease;
}

.hero .download-btn:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 32px rgba(0, 0, 0, 0.2);
}

/* Content Sections */
.content {
    max-width: 1000px;
    margin: 0 auto;
    padding: 80px 24px;
}

.section {
    background: white;
    border-radius: 16px;
    padding: 60px 48px;
    margin-bottom: 40px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

.section h2 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 24px;
    text-align: center;
}

.section p {
    font-size: 1.1rem;
    color: #4b5563;
    line-height: 1.8;
    margin-bottom: 16px;
}

.steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 32px;
    margin-top: 32px;
}

.step {
    text-align: center;
    padding: 24px;
    background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
    border-radius: 12px;
}

.step-number {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 48px;
    height: 48px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    font-weight: 700;
    font-size: 1.3rem;
    border-radius: 50%;
    margin-bottom: 16px;
}

.step h3 {
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 8px;
}

.step p {
    margin: 0;
    font-size: 0.95rem;
}

/* Responsive */
@media (max-width: 768px) {
    .navbar {
        padding: 16px 24px;
        flex-direction: column;
        gap: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .hero h1 {
        font-size: 2.2rem;
    }

    .hero p {
        font-size: 1.1rem;
    }

    .section {
        padding: 32px 24px;
    }

    .section h2 {
        font-size: 1.8rem;
    }
}



--- FILE: D:\Window Tuning\Velosity_site\download\index.html ---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download - Velocity</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <a href="../index.html" class="navbar-logo">Velocity</a>
        <div class="nav-links">
            <a href="../index.html" class="nav-button">Home</a>
            <a href="../how-to-use/index.html" class="nav-button">How to use</a>
            <a href="../how-to-install/index.html" class="nav-button">How to install</a>
            <a href="../download/index.html" class="nav-button">Download</a>
        </div>
    </nav>

    <main class="content">
        <section class="section">
            <h2>Download Velocity</h2>
            <p>Get the latest version of Velocity and start optimizing your Windows system today. Fast, secure, and completely free!</p>
            <div style="margin-top: 40px; text-align: center;">
                <button class="download-btn" onclick="downloadFile()">
                    Download Velocity v4.2
                </button>
                <p style="margin-top: 20px; color: #4b5563;">Windows 10/11 вЂў 64-bit вЂў ~100MB</p>
                <div style="margin-top:30px; text-align:left; max-width:500px; margin-left:auto; margin-right:auto; background:#f9fafb; padding:20px; border-radius:8px; box-shadow:0 2px 8px #0001;">
                    <h3 style="margin-top:0;">How to Download & Install</h3>
                    <ol style="padding-left:20px;">
                        <li>Click the <b>Download Velocity v4.2</b> button above.</li>
                        <li>Save <b>velocity_setup.exe</b> to your computer.</li>
                        <li>Double-click <b>velocity_setup.exe</b> to start the installer.</li>
                        <li>Follow the on-screen instructions to complete installation.</li>
                        <li>After installation, launch <b>Velocity</b> from your desktop or Start menu.</li>
                    </ol>
                </div>
            </div>
        </section>
    </main>

    <script>
        function downloadFile() {
            const fileUrl = 'https://github.com/Mulino-Y/Velocity/releases/download/v4.2/velocity_setup.exe';
            const link = document.createElement('a');
            link.href = fileUrl;
            link.download = 'velocity_setup.exe';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
    </script>
</body>
</html>



--- FILE: D:\Window Tuning\Velosity_site\download\style.css ---
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #f7f9fc 0%, #eef2f7 100%);
    color: #1a202c;
    line-height: 1.6;
}

/* Navigation Bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 24px 64px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar-logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2563eb;
    text-decoration: none;
}

.nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
}

.nav-button {
    background: none;
    border: none;
    font-size: 1rem;
    font-weight: 500;
    color: #4b5563;
    cursor: pointer;
    text-decoration: none;
    padding: 8px 16px;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.nav-button:hover {
    color: #2563eb;
    background: rgba(37, 99, 235, 0.1);
}

/* Content Sections */
.content {
    max-width: 1000px;
    margin: 0 auto;
    padding: 80px 24px;
}

.section {
    background: white;
    border-radius: 16px;
    padding: 60px 48px;
    margin-bottom: 40px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

.section h2 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 24px;
    text-align: center;
}

.section p {
    font-size: 1.1rem;
    color: #4b5563;
    line-height: 1.8;
    margin-bottom: 16px;
    text-align: center;
}

.download-btn {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    border: none;
    padding: 16px 48px;
    font-size: 1.1rem;
    font-weight: 600;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0 8px 24px rgba(102, 126, 234, 0.3);
    transition: all 0.3s ease;
}

.download-btn:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 32px rgba(102, 126, 234, 0.4);
}

/* Responsive */
@media (max-width: 768px) {
    .navbar {
        padding: 16px 24px;
        flex-direction: column;
        gap: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .section {
        padding: 32px 24px;
    }

    .section h2 {
        font-size: 1.8rem;
    }

    .download-btn {
        font-size: 1rem;
        padding: 12px 32px;
    }
}



--- FILE: D:\Window Tuning\Velosity_site\home\index.html ---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home - Velocity</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <a href="../index.html" class="nav-button">Home</a>
        <a href="../how-to-use/index.html" class="nav-button">How to use</a>
        <a href="../how-to-install/index.html" class="nav-button">How to install</a>
    </nav>

    <main class="content">
        <section class="intro">
            <h1>Welcome to Velocity</h1>
            <p>Velocity is your ultimate solution for optimizing your Windows system. With just a few clicks, you can clean, boost, and optimize your computer for peak performance.</p>
        </section>

        <section class="download-section">
            <button class="download-btn" onclick="downloadFile()">Download Now</button>
        </section>
    </main>

    <script>
        function downloadFile() {
            const fileUrl = 'https://github.com/Mulino-Y/Velocity/releases/download/v4.2/velocity_setup.exe';
            const link = document.createElement('a');
            link.href = fileUrl;
            link.download = 'Velocity.exe';
            link.click();
        }
    </script>
</body>
</html>



--- FILE: D:\Window Tuning\Velosity_site\home\style.css ---
body {
    font-family: 'Inter', 'Roboto', Arial, sans-serif;
    background: #f7f8fa;
    color: #181c32;
    margin: 0;
    padding: 0;
    min-height: 100vh;
}

.navbar {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    background: #fff;
    padding: 32px 64px 0 64px;
    gap: 24px;
    border: none;
    box-shadow: none;
}

.nav-button {
    background: none;
    border: none;
    color: #181c32;
    font-size: 1.1rem;
    font-weight: 500;
    padding: 8px 20px;
    border-radius: 24px;
    text-decoration: none;
    transition: background 0.2s, color 0.2s;
}

.nav-button:hover {
    background: #f0f4ff;
    color: #2563eb;
}

.content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 80vh;
    padding: 0 24px;
}

.intro {
    margin-top: 60px;
    margin-bottom: 40px;
    text-align: center;
}

.intro h1 {
    font-size: 3.2rem;
    font-weight: 700;
    margin-bottom: 18px;
    letter-spacing: -1px;
}

.intro p {
    font-size: 1.35rem;
    color: #4b5563;
    max-width: 600px;
    margin: 0 auto;
}

.download-section {
    margin: 40px 0 0 0;
    display: flex;
    flex-direction: row;
    gap: 18px;
    justify-content: center;
}

.download-btn {
    background: #2563eb;
    color: #fff;
    border: none;
    padding: 18px 44px;
    font-size: 1.25rem;
    border-radius: 32px;
    cursor: pointer;
    font-weight: 600;
    box-shadow: 0 4px 24px 0 rgba(37,99,235,0.10);
    transition: background 0.2s, transform 0.2s;
}

.download-btn:hover {
    background: #1d4ed8;
    transform: translateY(-2px) scale(1.04);
}

@media (max-width: 700px) {
    .navbar {
        padding: 24px 10px 0 10px;
        gap: 10px;
    }
    .intro h1 {
        font-size: 2rem;
    }
    .intro p {
        font-size: 1rem;
    }
    .download-btn {
        font-size: 1rem;
        padding: 12px 24px;
    }
}



--- FILE: D:\Window Tuning\Velosity_site\how-to-install\index.html ---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How to Install - Velocity</title>
    <link rel="stylesheet" href="../style.css">
</head>
<body>
    <nav class="navbar">
        <a href="../index.html" class="navbar-logo">Velocity</a>
        <div class="nav-links">
            <a href="../index.html" class="nav-button">Home</a>
            <a href="../how-to-use/index.html" class="nav-button">How to use</a>
            <a href="../how-to-install/index.html" class="nav-button">How to install</a>
            <a href="https://github.com/Mulino-Y/Velocity/releases/download/v4.2/velocity_setup.exe" class="nav-button">Download</a>
        </div>
    </nav>

    <main class="content">
        <section class="section">
            <h2>How to Install Velocity</h2>
            
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Download the File</h3>
                    <p>Click the Download button and save the installer to your computer</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Extract zip</h3>
                    <p>Locate the file and extract exe file to any folder you want</p>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <h3>Launch & Enjoy</h3>
                    <p>Installation complete - open Velocity and start optimizing</p>
                </div>
            </div>
        </section>
    </main>
</body>
</html>



--- FILE: D:\Window Tuning\Velosity_site\how-to-install\style.css ---
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #f7f9fc 0%, #eef2f7 100%);
    color: #1a202c;
    line-height: 1.6;
}

/* Navigation Bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 24px 64px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar-logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2563eb;
    text-decoration: none;
}

.nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
}

.nav-button {
    background: none;
    border: none;
    font-size: 1rem;
    font-weight: 500;
    color: #4b5563;
    cursor: pointer;
    text-decoration: none;
    padding: 8px 16px;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.nav-button:hover {
    color: #2563eb;
    background: rgba(37, 99, 235, 0.1);
}

/* Content Sections */
.content {
    max-width: 1000px;
    margin: 0 auto;
    padding: 80px 24px;
}

.section {
    background: white;
    border-radius: 16px;
    padding: 60px 48px;
    margin-bottom: 40px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

.section h2 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 24px;
    text-align: center;
}

.section p {
    font-size: 1.1rem;
    color: #4b5563;
    line-height: 1.8;
    margin-bottom: 16px;
    text-align: center;
}

.steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 32px;
    margin-top: 32px;
}

.step {
    text-align: center;
    padding: 24px;
    background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
    border-radius: 12px;
}

.step-number {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 48px;
    height: 48px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    font-weight: 700;
    font-size: 1.3rem;
    border-radius: 50%;
    margin-bottom: 16px;
}

.step h3 {
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 8px;
}

.step p {
    margin: 0;
    font-size: 0.95rem;
}

/* Responsive */
@media (max-width: 768px) {
    .navbar {
        padding: 16px 24px;
        flex-direction: column;
        gap: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .section {
        padding: 32px 24px;
    }

    .section h2 {
        font-size: 1.8rem;
    }
}



--- FILE: D:\Window Tuning\Velosity_site\how-to-use\index.html ---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How to Use - Velocity</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <a href="../index.html" class="navbar-logo">Velocity</a>
        <div class="nav-links">
            <a href="../index.html" class="nav-button">Home</a>
            <a href="../how-to-use/index.html" class="nav-button">How to use</a>
            <a href="../how-to-install/index.html" class="nav-button">How to install</a>
            <a href="https://github.com/Mulino-Y/Velocity/releases/download/v4.2/velocity_setup.exe" class="nav-button">Download</a>
        </div>
    </nav>

    <main class="content">
        <section class="section">
            <h2>How to Use Velocity</h2>
            <p>Follow these simple steps to optimize your Windows system:</p>
            
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Disable Defender</h3>
                    <p>Disable Windows Defender or any third-party antivirus software before running Velocity to avoid conflicts.</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Launch Velocity</h3>
                    <p>Launch Velocity as an administrator and select the optimization tasks you want to run.</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Log in</h3>
                    <p>Log in to your Velocity account (email + licence) to unlock all features!</p>
                </div>
            </div>
        </section>
    </main>
</body>
</html>



--- FILE: D:\Window Tuning\Velosity_site\how-to-use\style.css ---
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #f7f9fc 0%, #eef2f7 100%);
    color: #1a202c;
    line-height: 1.6;
}

/* Navigation Bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 24px 64px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar-logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2563eb;
    text-decoration: none;
}

.nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
}

.nav-button {
    background: none;
    border: none;
    font-size: 1rem;
    font-weight: 500;
    color: #4b5563;
    cursor: pointer;
    text-decoration: none;
    padding: 8px 16px;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.nav-button:hover {
    color: #2563eb;
    background: rgba(37, 99, 235, 0.1);
}

/* Content Sections */
.content {
    max-width: 1000px;
    margin: 0 auto;
    padding: 80px 24px;
}

.section {
    background: white;
    border-radius: 16px;
    padding: 60px 48px;
    margin-bottom: 40px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

.section h2 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #1a202c;
    margin-bottom: 24px;
    text-align: center;
}

.section p {
    font-size: 1.1rem;
    color: #4b5563;
    line-height: 1.8;
    margin-bottom: 16px;
    text-align: center;
}

.steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 32px;
    margin-top: 32px;
}

.step {
    text-align: center;
    padding: 24px;
    background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
    border-radius: 12px;
}

.step-number {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 48px;
    height: 48px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    font-weight: 700;
    font-size: 1.3rem;
    border-radius: 50%;
    margin-bottom: 16px;
}

.step h3 {
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 8px;
}

.step p {
    margin: 0;
    font-size: 0.95rem;
}

/* Responsive */
@media (max-width: 768px) {
    .navbar {
        padding: 16px 24px;
        flex-direction: column;
        gap: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .section {
        padding: 32px 24px;
    }

    .section h2 {
        font-size: 1.8rem;
    }
}



