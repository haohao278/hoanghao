
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc mừng ngày 8/3</title>
    <style>
        :root {
            --primary-color: #ff4d6d;
            --bg-color: #fff0f3;
        }

        body {
            margin: 0;
            padding: 0;
            background: var(--bg-color);
            font-family: 'Arial', sans-serif;
            overflow-x: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* Hiệu ứng tiêu đề */
        .header {
            text-align: center;
            margin-top: 50px;
            color: var(--primary-color);
            z-index: 10;
        }

        h1 {
            font-size: 3rem;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.1);
            animation: heartBeat 1.5s infinite;
        }

        @keyframes heartBeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* Khu vực 4 ảnh */
        .photo-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            max-width: 600px;
            padding: 20px;
            z-index: 5;
        }

        .photo-card {
            background: white;
            padding: 10px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            border-radius: 10px;
            transition: transform 0.3s;
            cursor: pointer;
        }

        .photo-card:hover {
            transform: translateY(-10px) rotate(3deg);
        }

        .photo-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 5px;
        }

        /* Lời chúc */
        .message {
            margin: 30px;
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            max-width: 500px;
            text-align: center;
            line-height: 1.6;
            color: #555;
            z-index: 5;
        }

        /* Hiệu ứng cánh hoa rơi */
        .petal {
            position: fixed;
            top: -10%;
            color: #ff4d6d;
            font-size: 20px;
            user-select: none;
            z-index: 1;
            animation: fall linear forwards;
        }

        @keyframes fall {
            to {
                transform: translateY(110vh) rotate(360deg);
            }
        }

        @media (max-width: 600px) {
            h1 { font-size: 2rem; }
            .photo-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>Happy Women's Day 8/3! 🌷</h1>
        <p>Gửi đến chị Nga nghi ngờ</p>
    </div>

    <div class="photo-grid">
    
        <div class="photo-card">
            <img src="111.jpg" alt="Ảnh 1"> <h3>chụp lúc nào không biết luôn tạm được</h3>
        </div>
        <div class="photo-card">
            <img src="222.jpg" alt="Ảnh 2"> <h3>đề nghị nên chụp mấy tấm xinh như vầy</h3>
        </div>
    </div>

    <div class="message">
        <p>Chúc chị Nga một ngày 8/3 tràn đầy niềm vui, hạnh phúc và luôn rạng rỡ như những đóa hoa. Và mong chị nga năm nay có nhiều ảnh hơn để em còn làm mấy cái như nì(´▽`ʃ❤️ƪ)</p>
    </div>

    <script>
        // Hiệu ứng hoa rơi
        function createPetal() {
            const symbols = ['🌸', '💖', '🌹', '✨', '🌷'];
            const petal = document.createElement('div');
            petal.classList.add('petal');
            petal.innerHTML = symbols[Math.floor(Math.random() * symbols.length)];
            petal.style.left = Math.random() * 100 + 'vw';
            petal.style.animationDuration = Math.random() * 3 + 2 + 's';
            petal.style.opacity = Math.random();
            petal.style.fontSize = Math.random() * 20 + 10 + 'px';
            
            document.body.appendChild(petal);

            setTimeout(() => {
                petal.remove();
            }, 5000);
        }

        setInterval(createPetal, 300);
    </script>
</body>
</html>
