<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Abhishek Adapa</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        /* Base Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, sans-serif;
        }

        /* Background Image */
        body {
            background-image: url('photo.jpg'); /* Put your image in same folder */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;

            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            color: #2d3436;
        }

        /* Main Profile Card */
        .profile-card {
            background: #eff0f3f2;
            padding: 3rem;
            border-radius: 24px;
            box-shadow: 0 20px 40px hsla(240, 8%, 95%, 0.91);
            text-align: center;
            width: 90%;
            max-width: 450px;
            transition: transform 0.3s ease;
        }

        /* Logo */
        .logo-container {
            width: 150px;
            height: 150px;
            margin: 0 auto 1.5rem;
            background-color: #eee;
            border: 4px solid #ffffff;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            border-radius: 12px;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .logo-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        h1 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .subtitle {
            color: #636e72;
            margin-bottom: 2rem;
            font-size: 1rem;
        }

        /* Social Buttons */
        .social-links {
            display: grid;
            gap: 12px;
        }

        .profile-btn {
            display: block;
            padding: 14px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            border-radius: 10px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .linkedin { background-color: #0077b5; }
        .instagram { background-color: #E1306C; }
        .whatsapp { background-color: #25D366; }
        .twitter { background-color: #1DA1F2; }
        .snapchat { background-color: #FFFC00; color: #000; }

        .profile-btn:hover {
            transform: scale(1.03);
            filter: brightness(1.1);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .profile-btn:active {
            transform: scale(0.98);
        }
    </style>
</head>

<body>

    <div class="profile-card" id="mainCard">

        <div class="logo-container">
            <img src="pict.jpg.jpg" alt="Student Logo"> 
            <!-- Put your profile image in same folder -->
        </div>

        <h1>ABHISHEK ADAPA</h1>
        <p class="subtitle">Personal Portfolio & Socials</p>

        <div class="social-links">
            <button class="profile-btn linkedin" onclick="navigateTo('https://www.linkedin.com/in/abhishek-adapa-b333282b0')">LinkedIn</button>
            <button class="profile-btn instagram" onclick="navigateTo('https://www.instagram.com/___abhiii___0709')">Instagram</button>
            <button class="profile-btn whatsapp" onclick="navigateTo('https://wa.me/9121455477')">WhatsApp</button>
            <button class="profile-btn twitter" onclick="navigateTo('https://x.com/abhiadapa0709')">Twitter</button>
            <button class="profile-btn snapchat" onclick="navigateTo('https://www.snapchat.com/add/abhiadapa0709')">Snapchat</button>
        </div>

    </div>

    <script>
        function navigateTo(url) {
            window.open(url, '_blank');
        }

        window.onload = () => {
            const card = document.getElementById('mainCard');
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            
            setTimeout(() => {
                card.style.transition = 'all 0.8s ease-out';
                card.style.opacity = '1';
                card.style.transform = 'translateY(0)';
            }, 100);
        };
    </script>

</body>
</html>
