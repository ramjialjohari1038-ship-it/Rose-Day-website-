<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rose Day Celebration</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #ffe6f2, #ffffff);
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ff69b4;
            color: white;
            text-align: center;
            padding: 20px;
        }
        section {
            padding: 20px;
            max-width: 800px;
            margin: 0 auto;
        }
        .rose-gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .rose {
            margin: 10px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .rose:hover {
            transform: scale(1.1);
        }
        form {
            background: #f9f9f9;
            padding: 20px;
            border-radius: 8px;
        }
        input, textarea, button {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 10px;
        }
        button {
            background-color: #ff69b4;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #ff1493;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #ff69b4;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Happy Rose Day!</h1>
        <p>Express your love with the gift of roses on February 7th.</p>
    </header>

    <section id="about">
        <h2>What is Rose Day?</h2>
        <p>Rose Day is the first day of Valentine's Week. It's a time to share roses and show affection. Different colors mean different things:</p>
        <ul>
            <li><strong>Red:</strong> Passion and love</li>
            <li><strong>Pink:</strong> Gratitude and admiration</li>
            <li><strong>Yellow:</strong> Friendship and joy</li>
            <li><strong>White:</strong> Purity and innocence</li>
        </ul>
    </section>

    <section id="gallery">
        <h2>Virtual Rose Gallery</h2>
        <p>Click on a rose to add it to your collection!</p>
        <div class="rose-gallery">
            <img src="https://via.placeholder.com/100/ff0000?text=Red+Rose" alt="Red Rose" class="rose" onclick="addRose('Red')">
            <img src="https://via.placeholder.com/100/ffc0cb?text=Pink+Rose" alt="Pink Rose" class="rose" onclick="addRose('Pink')">
            <img src="https://via.placeholder.com/100/ffff00?text=Yellow+Rose" alt="Yellow Rose" class="rose" onclick="addRose('Yellow')">
            <img src="https://via.placeholder.com/100/ffffff?text=White+Rose" alt="White Rose" class="rose" onclick="addRose('White')">
        </div>
        <p id="rose-count">Roses collected: 0</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" rows="4" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2023 Rose Day Website. Made with love.</p>
    </footer>

    <script>
        let count = 0;
        function addRose(color) {
            count++;
            document.getElementById('rose-count').textContent = `Roses collected: ${count}`;
            alert(`You added a ${color} rose!`);
        }
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We\'ll get back to you soon.');
        });
    </script>
</body>
</html>
