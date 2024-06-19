# Basic-Landing-Page
I recently created a basic landing page using HTML and CSS. The HTML provided the structure and content of the page, while CSS was used for styling and layout.  In HTML, I defined the main components of the landing page such as the header, navigation menu, sections for content, and a footer.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delicious Recipes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            line-height: 1.6;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: #333;
            color: #fff;
            padding: 10px 0;
        }

        header h1 {
            text-align: center;
        }

        nav ul {
            list-style: none;
            text-align: center;
        }

        nav ul li {
            display: inline;
            margin: 0 10px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        #hero {
            background: url('hero-image.jpg') no-repeat center center/cover;
            color: #fff;
            text-align: center;
            padding: 100px 0;
        }

        #hero h2 {
            margin: 0;
            font-size: 2.5em;
        }

        .cta-button {
            display: inline-block;
            padding: 10px 20px;
            background: #ff6347;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
        }

        #about, #recipes, #subscribe {
            padding: 50px 0;
            text-align: center;
        }

        #recipes .recipe-grid {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }

        .recipe-item {
            width: 30%;
            margin-bottom: 20px;
        }

        .recipe-item img {
            width: 100%;
            border-radius: 5px;
        }

        .recipe-item h3 {
            margin-top: 10px;
        }

        footer {
            background: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }

        .social-media {
            list-style: none;
            padding: 0;
        }

        .social-media li {
            display: inline;
            margin: 0 10px;
        }

        .social-media li a {
            color: #fff;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Delicious Recipes</h1>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#recipes">Recipes</a></li>
                    <li><a href="#subscribe">Subscribe</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <section id="hero">
        <div class="container">
            <h2>Welcome to Delicious Recipes</h2>
            <p>Explore our collection of mouth-watering recipes.</p>
            <a href="#recipes" class="cta-button">Discover Our Recipes</a>
        </div>
    </section>
    <section id="about">
        <div class="container">
            <h2>About Us</h2>
            <p>Welcome to Delicious Recipes, your go-to source for the best recipes. Whether you are a novice cook or a seasoned chef, our recipes are designed to inspire and delight your taste buds.</p>
        </div>
    </section>
    <section id="recipes">
        <div class="container">
            <h2>Featured Recipes</h2>
            <div class="recipe-grid">
                <div class="recipe-item">
                    <img src= "images/recipe1.jpg" alt="Recipe 1">
                    <h3>Recipe 1</h3>
                    <p>Noodles are a versatile, popular food made from unleavened dough, enjoyed in various dishes like soups, stir-fries, and salads worldwide.</p>
                    <a href="#">Read More</a>
                </div>
                <div class="recipe-item">
                    <img src="images/Recipe2.jpg" alt="Recipe 2">
                    <h3>Recipe 2</h3>
                    <p>Fried rice is a flavorful dish of stir-fried cooked rice mixed with vegetables, eggs, and often meat or seafood, popular in many cuisines.</p>
                    <a href="#">Read More</a>
                </div>
                <div class="recipe-item">
                    <img src="images/Recipe3.jpg" alt="Recipe 3">
                    <h3>Recipe 3</h3>
                    <p>Chole Bhature is a popular North Indian dish consisting of spicy chickpea curry (Chole) served with fluffy deep-fried bread (Bhature).</p>
                    <a href="#">Read More</a>
                </div>
            </div>
        </div>
    </section>
    <section id="subscribe">
        <div class="container">
            <h2>Subscribe to Our Newsletter</h2>
            <p>Get the latest recipes delivered straight to your inbox.</p>
            <form id="subscribe-form">
                <input type="email" id="email" placeholder="Enter your email" required>
                <button type="submit">Subscribe</button>
            </form>
        </div>
    </section>
    <footer>
        <div class="container">
            <p>Contact us at <a href="mailto:info@deliciousrecipes.com">info@deliciousrecipes.com</a></p>
            <ul class="social-media">
                <li><a href="#">Facebook</a></li>
                <li><a href="#">Instagram</a></li>
                <li><a href="#">Twitter</a></li>
            </ul>
            <p>&copy; 2024 Delicious Recipes. All rights reserved.</p>
        </div>
    </footer>

    <script>
        document.getElementById('subscribe-form').addEventListener('submit', function(event) {
            event.preventDefault();
            const email = document.getElementById('email').value;
            if (validateEmail(email)) {
                alert('Thank you for subscribing!');
                // Add further logic for subscribing user, e.g., sending data to a server
            } else {
                alert('Please enter a valid email address.');
            }
        });

        function validateEmail(email) {
            const re = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
            return re.test(String(email).toLowerCase());
        }
    </script>
</body>
</html>
