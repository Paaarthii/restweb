# Ex.07 Restaurant Website
## Date: 26/12/2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meat & Ember</title>
    <style>
        body {
            background-color: #FFF8F0;
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: #4B1D0F;
        }
        header {
            background-color: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 30px 10px 20px 10px;
        }
        nav {
            background-color: #F39237;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: #4B1D0F;
            text-align: center;
            padding: 16px 36px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            background-color: #FFD166;
            color: #B23A48;
        }
        .banner {
            width: 100%;
            height: 360px;
            background-image: url(bannerfood.jpg);
            background-size: cover;
            background-position: center;
        }
        .container {
            max-width: 1000px;
            margin: 40px auto;
            padding: 24px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 24px rgba(180,58,72,0.07);
        }
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 22px;
        }
        .menu-item {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            padding: 20px 12px;
            text-align: center;
        }
        .menu-item img {
            width: 90px;
            height: 70px;
            object-fit: cover;
            border-radius: 8px;
        }
        .admin-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
            margin-top: 18px;
        }
        .admin-card {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            text-align: center;
            padding: 24px 12px;
        }
        .admin-card img {
            width: 78px;
            height: 78px;
            border-radius: 50%;
            object-fit: cover;
        }
        footer {
            background: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 18px 0 8px 0;
            position: relative;
        }
        .active {
            background-color: #FFD166;
            color: #B23A48 !important;
        }
        @media (max-width: 800px) {
            .menu-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .admin-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        @media (max-width: 500px) {
            .menu-grid, .admin-grid {
                grid-template-columns: 1fr;
            }
            nav a {
                float: none;
                display: block;
            }
        }
    </style>
    <script>
        function showPage(pageId) {
            document.querySelectorAll('.container').forEach(c=>c.style.display='none');
            document.getElementById(pageId).style.display = 'block';
            document.querySelectorAll('nav a').forEach(a=>a.classList.remove('active'));
            document.getElementById('nav-' + pageId).classList.add('active');
        }
        window.onload = function() {
            showPage('home');
        }
    </script>
</head>
<body>
    <header>
        <div class="banner"></div>
        <h1>Meat & Ember</h1>
        <p>Grilled to Perfection</p>
    </header>
    <nav>
        <a id="nav-home" href="#" onclick="showPage('home');return false;">Home</a>
        <a id="nav-menu" href="#" onclick="showPage('menu');return false;">Menu</a>
        <a id="nav-admin" href="#" onclick="showPage('admin');return false;">Administration</a>
        <a id="nav-contact" href="#" onclick="showPage('contact');return false;">Contact Us</a>
    </nav>
    <div id="home" class="container">
        <h2>Welcome. Discover the soul of non-vegetarian cuisine!</h2>
        <p>A modern non-veg restaurant focused on slow-cooked meats, deep marinades, and charcoal grilling that brings out intense taste in every bite.</p>
    </div>
    <div id="menu" class="container" style="display:none;">
        <h2>Our Menu</h2>
        <div class="menu-grid">
            <div class="menu-item"><img src="roast chicken.jpg"><br>Ember Roast Chicken<br>₹199</div>
            <div class="menu-item"><img src="wings.jpg"><br>Fiery BBQ Wings<br>₹169</div>
            <div class="menu-item"><img src="fried chicken.webp"><br>Fried Chicken<br>₹149</div>
            <div class="menu-item"><img src="lollipop.webp"><br>Chicken lollipop<br>₹150</div>
            <div class="menu-item"><img src="muttongravy.jpg"><br>Classic Mutton Curry<br>₹245</div>
            <div class="menu-item"><img src="butter naan.jpg"><br>Butter Naan<br>₹35</div>
            <div class="menu-item"><img src="garlic naan.jpg"><br>Garlic Naan<br>₹35</div>
            <div class="menu-item"><img src="chickengravy.jpg"><br>Chicken Chettinad<br>₹229</div>
            <div class="menu-item"><img src="mutton kola urundai.webp"><br>Mutton Kola Urundai<br>₹170</div>
            <div class="menu-item"><img src="soup.jpg">Chicken Soup<br><br>₹119</div>
            
        </div>
    </div>
    <div id="admin" class="container" style="display:none;">
        <h2>Administration</h2>
        <div class="admin-grid">
            <div class="admin-card">
                <img src="vijay.webp">
                <b>Thalapathy</b><br>
                Manager
            </div>
            <div class="admin-card">
                <img src="sk.jpg">
                <b>Sanjeev Kapoor</b><br>
                Head Chef
            </div>
            <div class="admin-card">
                <img src="damu.avif">
                <b>K.Damodharan</b><br>
                Lead Cook
            </div>
            <div class="admin-card">
                <img src="sam.jpg">
                <b>Samantha</b><br>
                Marketing Head
            </div>
            <div class="admin-card">
                <img src="iman.png">
                <b>Iman Gadzhi</b><br>
                Finance Manager
            </div>
            <div class="admin-card">
                <img src="batman.jpg">
                <b>Batman</b><br>
                Customer Relations
            </div>
        </div>
    </div>
    <div id="contact" class="container" style="display:none;">
        <h2>Contact Us</h2>
        <p><b>Address:</b> 123 Street, Anna Nagar, Chennai-699855</p>
        <p><b>Phone:</b> +91-9876543210</p>
        <p><b>Email:</b> cc@meat&ember</p>
        <p>We welcome all your feedback and enquiries!</p>
    </div>
    <footer>
        &copy; 2025 Meat & Ember
    </footer>
</body>
</html>
```

## OUTPUT:
HOME PAGE

![alt text](<Screenshot (87).png>)

MENU

![alt text](<Screenshot (88).png>)

ADMINISTRATION

![alt text](<Screenshot (89).png>)

CONTACT 

![alt text](<Screenshot (90).png>)
## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
