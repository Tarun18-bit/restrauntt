<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tarun Foods</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        body {
            background: #fafafa;
            color: #333;
        }

        header {
            background: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            background: #34495e;
            padding: 10px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        section {
            padding: 40px;
            max-width: 1000px;
            margin: auto;
        }

        h2 {
            text-align: center;
            margin-bottom: 30px;
        }

        /* Menu cards */
        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 8px rgba(0,0,0,0.1);
            text-align: center;
        }

        .card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
        }

        /* Reservation */
        form {
            display: flex;
            flex-direction: column;
            gap: 15px;
            max-width: 450px;
            margin: auto;
        }

        input, textarea {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
        }

        button {
            padding: 10px;
            background: #2ecc71;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: #27ae60;
        }

        /* Reviews */
        .review {
            background: white;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 15px;
            box-shadow: 0 0 6px rgba(0,0,0,0.1);
        }

        footer {
            background: #2c3e50;
            color: white;
            padding: 15px;
            text-align: center;
            margin-top: 40px;
        }
    </style>
</head>
<body>

<header>
    <h1>Tarun Foods</h1>
    <p>Where Flavor Meets Creativity</p>
</header>

<nav>
    <a href="#menu">Menu</a>
    <a href="#reservation">Reservation</a>
    <a href="#reviews">Reviews</a>
</nav>

<!-- Menu Section -->
<section id="menu">
    <h2>Our Menu</h2>
    <div class="menu-items">
        <div class="card">
            <img src="https://source.unsplash.com/400x300/?pizza" alt="Pizza">
            <h3>Italian Pizza</h3>
            <p>₹350</p>
        </div>
        <div class="card">
            <img src="https://source.unsplash.com/400x300/?pasta" alt="Pasta">
            <h3>Cheese Pasta</h3>
            <p>₹280</p>
        </div>
        <div class="card">
            <img src="https://source.unsplash.com/400x300/?salad" alt="Salad">
            <h3>Healthy Salad</h3>
            <p>₹200</p>
        </div>
    </div>
</section>

<!-- Reservation Section -->
<section id="reservation">
    <h2>Online Reservation</h2>
    <form onsubmit="submitForm(event)">
        <input type="text" id="name" placeholder="Your Name" required>
        <input type="email" id="email" placeholder="Email" required>
        <input type="date" id="date" required>
        <input type="time" id="time" required>
        <textarea id="message" placeholder="Special request (optional)"></textarea>
        <button type="submit">Reserve Table</button>
    </form>
    <p id="response-msg" style="text-align:center; margin-top:15px;"></p>
</section>

<!-- Reviews Section -->
<section id="reviews">
    <h2>Customer Reviews</h2>

    <div class="review">
        <strong>Arjun:</strong>
        <p>Amazing ambiance and delicious food. Loved the pasta!</p>
    </div>

    <div class="review">
        <strong>Priya:</strong>
        <p>Best pizza in town. Must visit!</p>
    </div>

</section>

<footer>
    <p>© 2025 Gourmet Haven | All Rights Reserved</p>
</footer>

<script>
    function submitForm(event) {
        event.preventDefault();
        document.getElementById("response-msg").textContent = "✅ Reservation Submitted! We will contact you soon.";
    }
</script>

</body>
</html>
