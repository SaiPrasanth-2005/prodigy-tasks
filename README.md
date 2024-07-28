//Navigatio.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav id="navbar">
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Home Section</h1>
    </section>
    <section id="about">
        <h1>About Section</h1>
    </section>
    <section id="services">
        <h1>Services Section</h1>
    </section>
    <section id="contact">
        <h1>Contact Section</h1>
    </section>

    <script src="script.js"></script>
</body>
</html>


// script.js


window.addEventListener('scroll', function() {
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

//style.css

body, html {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

nav {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: #333;
    color: white;
    transition: background-color 0.3s;
}

nav.scrolled {
    background-color: #222;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-around;
}

nav ul li {
    padding: 14px 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #FFD700;
}

section {
    padding: 100px;
    height: 100vh;
    border-bottom: 1px solid #ddd;
}
