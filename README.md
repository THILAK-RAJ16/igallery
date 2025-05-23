# Ex.08 Design of Interactive Image Gallery
## Date:17-05-2025

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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Animal Slider</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f0f0f0;
    }

    .slider {
      width: 100%;
      max-width: 1000px;
      margin: 40px auto;
      overflow: hidden;
      position: relative;
    }

    .slides {
      display: flex;
      transition: transform 0.5s ease-in-out;
      width: max-content;
    }

    .slide-item {
      min-width: 300px;
      margin: 0 10px;
      background: #fff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .slide-item img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .caption {
      padding: 10px;
      text-align: center;
      font-weight: bold;
    }

    .nav-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: rgba(0,0,0,0.5);
      color: #fff;
      border: none;
      font-size: 24px;
      padding: 10px;
      cursor: pointer;
      z-index: 10;
    }

    .prev {
      left: 0;
    }

    .next {
      right: 0;
    }
  </style>
</head>
<body>

<div class="slider">
  <button class="nav-btn prev" onclick="moveSlide(-1)">&#10094;</button>
  <div class="slides" id="slides">
    <div class="slide-item">
      <img src="/static/images5%20gal.jpeg" alt="Lion & Cub">
      <div class="caption">Lion & Cub</div>
    </div>
    <div class="slide-item">
      <img src="/static/imsge2%20gal.jpeg" alt="Elephant & Calf">
      <div class="caption">Elephant & Calf</div>
    </div>
    <div class="slide-item">
      <img src="/static/tiger%20web.jpg" alt="Tiger & Cub">
      <div class="caption">Tiger & Cub</div>
    </div>
    <div class="slide-item">
      <img src="/static/bear%20web.jpg" alt="Bear & Cub">
      <div class="caption">Bear & Cub</div>
    </div>
    <div class="slide-item">
      <img src="/static/penguin%20web.jpeg" alt="Penguin & Chick">
      <div class="caption">Penguin & Chick</div>
    </div>
    <div class="slide-item">
      <img src="/static/images4%20gal.jpeg" alt="Giraffe & Calf">
      <div class="caption">Giraffe & Calf</div>
    </div>
  </div>
  <button class="nav-btn next" onclick="moveSlide(1)">&#10095;</button>
</div>

<script>
  let slideIndex = 0;
  const slideWidth = 320; 
  const slides = document.getElementById('slides');

  function moveSlide(direction) {
    const totalItems = slides.children.length;
    slideIndex += direction;

    if (slideIndex < 0) slideIndex = 0;
    if (slideIndex > totalItems - 3) slideIndex = totalItems - 3;

    slides.style.transform = `translateX(-${slideIndex * slideWidth}px)`;
  }
</script>

</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2025-05-17 143810.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
