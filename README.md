# Introduction to CSS

## Objectives
Link an external CSS file to an HTML document.
Apply basic styling using selectors.
Use colors, fonts, and spacing effectively.

## Instructions

Create a style.css file.
Apply CSS to a HTML page.
Style elements using:
Classes and IDs.
Color and typography.
Margins, paddings, and borders.

>[!NOTE]
>  - Include at least:
>  - Use of 3 selectors
>  - Style an image
>  - Margin, Padding & Borders
>  - Different font

# Tasks
 - Link an external CSS file.
 - Apply at least 3 different selectors.
 - Improve readability and aesthetics.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Samuel Service</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&family=Roboto+Slab:wght@700&display=swap" rel="stylesheet">
</head>
<body>
    <header id="main-header">
        <div class="container">
            <h1>Samuel Service</h1>
            <p class="tagline">Professional multimedia solutions</p>
        </div>
    </header>

    <nav class="main-nav">
        <div class="container">
            <ul>
                <li><a href="#services">Services</a></li>
                <li><a href="#multimedia">Multimedia</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <main class="container">
        <section id="hero">
            <img src="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg" alt="Nature scene" class="hero-image">
            <h2>Quality Multimedia Services</h2>
        </section>

        <section id="services" class="content-box">
            <h2>Our Services</h2>
            <ul class="service-list">
                <li>Audio Production</li>
                <li>Video Editing</li>
                <li>Web Development</li>
            </ul>
        </section>

        <section id="multimedia" class="content-box">
            <h2>Multimedia Showcase</h2>
            <div class="media-container">
                <audio controls class="media-element">
                    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
                </audio>
                <video controls class="media-element">
                    <source src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4" type="video/mp4">
                </video>
            </div>
        </section>

        <section id="contact" class="content-box">
            <h2>Contact Us</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message:</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </section>
    </main>

    <footer id="main-footer">
        <div class="container">
            <p>&copy; 2024 Samuel Service. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>

CSS
/* Base Styles */
body {
    font-family: 'Open Sans', sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    color: #333;
    background-color: #f5f5f5;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Typography */
h1, h2, h3 {
    font-family: 'Roboto Slab', serif;
    color: #2c3e50;
}

h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

h2 {
    font-size: 2rem;
    margin-bottom: 1.5rem;
    border-bottom: 2px solid #3498db;
    padding-bottom: 0.5rem;
}

/* Header Styles */
#main-header {
    background-color: #2c3e50;
    color: white;
    padding: 2rem 0;
    text-align: center;
}

.tagline {
    font-style: italic;
    font-size: 1.2rem;
    margin: 0;
}

/* Navigation */
.main-nav {
    background-color: #3498db;
    padding: 1rem 0;
}

.main-nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.main-nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    transition: background-color 0.3s;
}

.main-nav a:hover {
    background-color: #2980b9;
}

/* Hero Section */
#hero {
    text-align: center;
    margin: 2rem 0;
}

.hero-image {
    width: 100%;
    max-height: 400px;
    object-fit: cover;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin-bottom: 1.5rem;
}

/* Content Boxes */
.content-box {
    background-color: white;
    padding: 2rem;
    margin-bottom: 2rem;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Services List */
.service-list {
    list-style-type: none;
    padding: 0;
}

.service-list li {
    padding: 0.75rem;
    margin-bottom: 0.5rem;
    background-color: #ecf0f1;
    border-left: 4px solid #3498db;
}

/* Media Elements */
.media-container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
}

.media-element {
    width: 100%;
    max-width: 500px;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Contact Form */
.contact-form {
    max-width: 600px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 1.5rem;
}

label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
}

input, textarea {
    width: 100%;
    padding: 0.75rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: inherit;
    font-size: 1rem;
}

textarea {
    min-height: 150px;
    resize: vertical;
}

.btn {
    background-color: #3498db;
    color: white;
    border: none;
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #2980b9;
}

/* Footer */
#main-footer {
    background-color: #2c3e50;
    color: white;
    text-align: center;
    padding: 1.5rem 0;
    margin-top: 2rem;
}
