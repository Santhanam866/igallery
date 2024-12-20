# Ex.08 Design of Interactive Image Gallery
## Date:17\12\2024

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
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BIKES Showcase</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: rgb(10, 233, 233);
            font-family: 'Roboto', sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
        }

        header {
            font-size: 2.5rem;
            margin-top: 30px;
            color: #222;
        }

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 16px;
            padding: 20px;
            max-width: 1300px;
            width: 100%;
        }

        .photo-item {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
        }

        .photo-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease-in-out, filter 0.3s ease;
        }

        .photo-item:hover img {
            transform: scale(1.1);
            filter: brightness(0.7);
        }

        .photo-item .label {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            text-align: center;
            padding: 12px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .photo-item:hover .label {
            opacity: 1;
        }

        .viewer {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
            z-index: 10000;
        }

        .viewer img {
            max-width: 95%;
            max-height: 95%;
        }

        .close-btn {
            position: absolute;
            top: 30px;
            right: 30px;
            font-size: 35px;
            color: white;
            cursor: pointer;
        }

        footer {
            background-color: #444;
            color: #fff;
            padding: 12px 30px;
            text-align: center;
            width: 100%;
            position: fixed;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>Bikes Showcase</header>

<div class="photo-grid">
    <div class="photo-item">
        <img src="GT650🚀.jpg" alt="gt 650">
        <div class="label">GT650</div>
    </div>
    <div class="photo-item">
        <img src="Kawasaki Ninja H2R.jpg" alt="NinjaH2R">
        <div class="label">NinjaH2R</div>
    </div>
    <div class="photo-item">
        <img src="Kawasaki Z900 in the sunset 4K.jpg" alt="z900">
        <div class="label">z900</div>
    </div>
    <div class="photo-item">
        <img src="Ducati bike.jpg" alt="Euro 5">
        <div class="label">euro 5</div>
    </div>
    <div class="photo-item">
        <img src="BMW motorcycle Super bikes  Latest motorbike 2022.jpg" alt="1000r">
        <div class="label">1000rr</div>
    </div>
</div>

<div class="viewer">
    <span class="close-btn">&times;</span>
    <img src="" alt="Large View">
</div>

<footer>
    <p>Designed and Developed by Santa's</p>
</footer>

<script>
    const allPhotos = document.querySelectorAll('.photo-item img');
    const viewer = document.querySelector('.viewer');
    const viewerImage = viewer.querySelector('img');
    const closeBtn = viewer.querySelector('.close-btn');

    allPhotos.forEach((img) => {
        img.addEventListener('click', function() {
            viewer.style.display = 'flex';
            viewerImage.src = this.src;
        });
    });

    closeBtn.addEventListener('click', () => {
        viewer.style.display = 'none';
    });

    viewer.addEventListener('click', (e) => {
        if (e.target === viewer) {
            viewer.style.display = 'none';
        }
    });
</script>

</body>
</html>



```

## OUTPUT:
![alt text](<Screenshot (55).png>)
![alt text](<Screenshot (56).png>)
![alt text](<Screenshot (57).png>)
![alt text](<Screenshot (58).png>)
![alt text](<Screenshot (59).png>)
![alt text](<Screenshot (60).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
