# Ex.08 Design of Interactive Image Gallery
## Date:23-12-2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Interactive Image Gallery</title>

<style>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 20px;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
}

/* GALLERY */
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    max-width: 900px;
    margin: auto;
}

.gallery img {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 10px;
    cursor: pointer;
    transition: transform 0.3s;
}

.gallery img:hover {
    transform: scale(1.05);
}

/* LIGHTBOX */
.lightbox {
    display: none;
    position: fixed;
    inset: 0;
    background-color: rgba(0,0,0,0.85);
    text-align: center;
}

.lightbox img {
    max-width: 90%;
    max-height: 90%;
    margin-top: 3%;
    object-fit: contain;   /* FULL IMAGE */
}

.lightbox span {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 35px;
    color: white;
    cursor: pointer;
}

/* FOOTER CREDIT */
footer {
    margin-top: 30px;
    font-size: 16px;
    color: #555;
}
</style>
</head>

<body>

<h1>Interactive Image Gallery</h1>

<div class="gallery">
    <img src="img1.jpg" onclick="openImage(this.src)">
    <img src="img2.jpg" onclick="openImage(this.src)">
    <img src="img3.jpg" onclick="openImage(this.src)">
    <img src="img4.jpg" onclick="openImage(this.src)">
    <img src="img5.jpg" onclick="openImage(this.src)">
</div>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
    <span onclick="closeImage()">&times;</span>
    <img id="lightbox-img">
</div>

<footer>
    <p><b>Done by RIHAB ZH</b></p>
</footer>

<script>
function openImage(src) {
    document.getElementById("lightbox").style.display = "block";
    document.getElementById("lightbox-img").src = src;
}

function closeImage() {
    document.getElementById("lightbox").style.display = "none";
}
</script>

</body>
</html>



```
## OUTPUT:
![alt text](<Screenshot 2025-12-23 105144.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
