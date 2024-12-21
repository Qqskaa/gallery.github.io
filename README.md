<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Личная галерея</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background-color: #6200ea;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 1rem;
            padding: 1rem;
            background-color: #eee;
        }
        nav a {
            text-decoration: none;
            color: #6200ea;
            font-weight: bold;
            cursor: pointer;
        }
        .container {
            padding: 1rem;
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
        }
        .gallery img {
            width: 100%;
            border-radius: 8px;
            transition: transform 0.3s;
        }
        .gallery img:hover {
            transform: scale(1.05);
        }
        footer {
            text-align: center;
            padding: 1rem;
            background-color: #6200ea;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Моя Личная Галерея</h1>
    </header>
    <nav>
        <a data-target="gallery">Галерея</a>
        <a data-target="about">Обо мне</a>
        <a data-target="contact">Контакты</a>
    </nav>
    <div class="container">
        <section id="gallery" class="section active">
            <h2>Галерея</h2>
            <div class="gallery">
                <img src="https://via.placeholder.com/150" alt="Пример работы 1">
                <img src="https://via.placeholder.com/150" alt="Пример работы 2">
                <img src="https://via.placeholder.com/150" alt="Пример работы 3">
                <img src="https://via.placeholder.com/150" alt="Пример работы 4">
            </div>
        </section>
        <section id="about" class="section">
            <h2>Обо мне</h2>
            <p>Привет! Я [Твое имя], художник и разработчик. Добро пожаловать в мою галерею!</p>
        </section>
        <section id="contact" class="section">
            <h2>Контакты</h2>
            <p>Свяжитесь со мной через Telegram: <a href="https://t.me/YourUsername">@YourUsername</a></p>
        </section>
    </div>
    <footer>
        <p>&copy; 2024 [Твое имя]. Все права защищены.</p>
    </footer>
    <script>
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                const targetId = link.getAttribute('data-target');
                document.querySelectorAll('.section').forEach(section => {
                    section.classList.remove('active');
                });
                document.getElementById(targetId).classList.add('active');
            });
        });
    </script>
</body>
</html>
