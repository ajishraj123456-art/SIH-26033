<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Farm Connect</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h2>🌱 Smart Farm Connect</h2>
    <nav>
        <a href="#home">Home</a>
        <a href="#market">Marketplace</a>
        <a href="#farmer">Farmers</a>
        <a href="#smart">AI Tools</a>
    </nav>
    <button onclick="showCart()">🛒 Cart (<span id="cartCount">0</span>)</button>
</header>

<section class="hero" id="home">
    <div>
        <h1>Farm Fresh.<br><span>Direct to You.</span></h1>
        <p>Connecting farmers directly with consumers.
           Better prices for farmers and fresh products for everyone.</p>
        <a href="#market" class="btn">Explore Marketplace</a>
    </div>
    <div class="hero-image">🌾 🚜 🥬</div>
</section>

<section class="stats">
    <div><h2>Direct</h2><p>Farmer Connection</p></div>
    <div><h2>Fair</h2><p>Product Pricing</p></div>
    <div><h2>Smart</h2><p>AI Technology</p></div>
</section>

<section id="market">
    <h2>Fresh Products</h2>
    <p>Buy directly from farmers.</p>

    <input type="text" id="search" placeholder="Search products..."
           oninput="displayProducts()">

    <div class="filters">
        <button onclick="filterProducts('All')">All</button>
        <button onclick="filterProducts('Vegetables')">Vegetables</button>
        <button onclick="filterProducts('Fruits')">Fruits</button>
        <button onclick="filterProducts('Grains')">Grains</button>
    </div>

    <div class="products" id="productList"></div>
</section>

<section id="farmer">
    <h2>Farmer Product Registration</h2>
    <p>Farmers can add their agricultural products here.</p>

    <form id="farmerForm">
        <input id="productName" placeholder="Product Name" required>
        <input id="farmerName" placeholder="Farmer Name" required>

        <select id="category">
            <option>Vegetables</option>
            <option>Fruits</option>
            <option>Grains</option>
        </select>

        <input id="price" type="number" min="1"
               placeholder="Price per kg (₹)" required>
        <input id="quantity" type="number" min="1"
               placeholder="Available Quantity (kg)" required>

        <button type="submit">Add Product</button>
    </form>
    <p id="message"></p>
</section>

<section id="smart">
    <h2>Smart AI Tools</h2>

    <div class="tools">
        <div class="tool-card">
            <h3>📊 Demand Forecasting</h3>
            <p>Estimate future agricultural product demand.</p>

            <select id="crop">
                <option>Tomato</option>
                <option>Rice</option>
                <option>Onion</option>
                <option>Potato</option>
            </select>

            <button onclick="forecast()">Predict Demand</button>
            <h3 id="prediction"></h3>
        </div>

        <div class="tool-card">
            <h3>🚚 Logistics Support</h3>
            <p>View a sample delivery route.</p>
            <button onclick="planRoute()">Plan Route</button>
            <p id="route"></p>
        </div>
    </div>
</section>

<footer>
    <h2>🌱 Smart Farm Connect</h2>
    <p>Empowering Farmers | Connecting Consumers</p>
    <p>Smart India Hackathon – SIH 26033</p>
    <p>Developed by AJISHRAJ.B</p>
</footer>

<div id="cartModal" class="modal">
    <div class="modal-content">
        <button class="close" onclick="closeCart()">Close ×</button>
        <h2>Shopping Cart</h2>
        <div id="cartItems"></div>
        <h3 id="total">Total: ₹0</h3>
        <button onclick="checkout()">Place Demo Order</button>
        <p id="orderMessage"></p>
    </div>
</div>

<script src="script.js"></script>
</body>
</html>
