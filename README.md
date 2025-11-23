[bakery.html.html](https://github.com/user-attachments/files/23697067/bakery.html.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Cake Delights</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #fffdf7;
            color: #5a3e2b;
            overflow-x: hidden;
        }
        header {
            background: #f7d774;
            padding: 20px;
            text-align: center;
            animation: fadeIn 1.2s ease;
        }
        header h1 {
            margin: 0;
            font-size: 2.5rem;
        }
        nav {
            background: #fbe9a1;
            padding: 10px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: #5a3e2b;
            font-weight: bold;
            transition: color 0.3s ease;
        }
        nav a:hover {
            color: #c59b28;
        }
        .hero {
            padding: 80px 20px;
            text-align: center;
            background-image: url('https://images.unsplash.com/photo-1541783018529-1f0b0c56f053');
            background-size: cover;
            background-position: center;
            color: #5a3e2b;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
            animation: slideIn 1.3s ease;
        }
        .hero h2 {
            font-size: 3rem;
        }
        .section {
            padding: 40px 20px;
            text-align: center;
        }
        .cakes {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        .cake-card {
            background: #ffffff;
            padding: 20px;
            border-radius: 12px;
            width: 260px;
            box-shadow: 0 4px 10px rgba(90, 62, 43, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeUp 1s ease;
        }
        .cake-card:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 14px rgba(0,0,0,0.15);
        }
        .cake-card img {
            width: 100%;
            border-radius: 10px;
        }
        footer {
            background: #f7d774;
            padding: 20px;
            text-align: center;
            margin-top: 40px;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes slideIn {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        @keyframes fadeUp {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        /* Mobile responsive */
        @media (max-width: 600px) {
            header h1 {
                font-size: 1.8rem;
            }
            .hero h2 {
                font-size: 2rem;
            }
            .cake-card {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Cake Delights</h1>
        <p>Sweetness Baked Fresh Every Day</p>
    </header>

    <nav>
        <a href="#menu">Menu</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>

    <section class="hero">
        <h2>Freshly Baked Cakes</h2>
        <p>Handcrafted with love and the finest ingredients</p>
    </section>

    <section id="menu" class="section">
        <h2>Our Cakes</h2>
        <div class="cakes">
            <div class="cake-card">
                <img src="https://i.pinimg.com/1200x/fd/9e/c1/fd9ec12ea9c0287f551537da3dc75605.jpg" alt="Chocolate Cake" />
                <h3>Chocolate Brownies</h3>
                <p>Rich, moist, and irresistible.</p>
            </div>
            <div class="cake-card">
                <img src="https://images.unsplash.com/photo-1563805042-7684c019e1cb" alt="Strawberry Cake" />
                <h3>Chocolate Mint</h3>
                <p>Fresh Chocolate & Delicious Mint</p>
            </div>
            <div class="cake-card">
                <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587" alt="Vanilla Cake" />
                <h3>Classic Chocolate Cake</h3>
                <p>Simple, elegant, and delicious</p>
            </div>
        </div>
    </section>

    <section id="about" class="section">
        <h2>About Us</h2>
        <p>We are a small artisan bakery dedicated to making fresh, homemade cakes with premium ingredients. Every cake is made with passion and a sprinkle of love.</p>
    </section>

    <section id="contact" class="section">
        <h2>Contact Us</h2>
        <p>Email: hello@cakedelights.com<br>Phone: 555-123-456</p>
    </section>

    <footer>
        © 2025 Cake Delights. All Rights Reserved.
    </footer>

    <footer>
        <h3>Quick Links</h3>
        <p>
            <a href="#store-location">Store Location</a> |
            <a href="#terms">Terms of Use</a> |
            <a href="#about">About Us</a> |
            <a href="#disclaimer">Disclaimer</a> |
            <a href="#contact">Contact Us</a> |
            <a href="#faq">FAQ</a> |
            <a href="#privacy">Privacy Policy</a>
        </p>
    </footer>

<script>
// Smooth fade-in on scroll
const cards = document.querySelectorAll('.cake-card');
const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.style.opacity = 1;
            entry.target.style.transform = "translateY(0)";
        }
    });
});
cards.forEach(card => {
    card.style.opacity = 0;
    card.style.transform = "translateY(30px)";
    observer.observe(card);
});
</script>
    
    <section id="store-location" class="section">
        <h2>Store Location</h2>
        <p>123 Sweet Street, Dessert City, CA 90210</p>
    </section>

    <section id="terms" class="section">
        <h2>Terms of Use</h2>
        <p>By using this website, you agree to our terms and conditions for service and purchases.</p>
    </section>

    <section id="disclaimer" class="section">
        <h2>Disclaimer</h2>
        <p>All cake images are for illustration purposes. Actual products may vary slightly.</p>
    </section>

    <section id="faq" class="section">
        <h2>Frequently Asked Questions</h2>
        <p>
            <strong>Q: Do you make custom cakes?</strong><br>
            A: Yes, we do! Contact us for details.<br><br>
            <strong>Q: Do you offer delivery?</strong><br>
            A: Yes, local delivery is available.
        </p>
    </section>

    <section id="privacy" class="section">
        <h2>Privacy Policy</h2>
        <p>We respect your privacy and do not share your personal information with third parties.</p>
    </section>

</body>
</html>
