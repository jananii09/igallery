# Ex.08 Design of Interactive Image Gallery
## Date:25/12/2024

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
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #f0f0f0;
            background-image: url('bg\ image2.jpg'); /* Replace 'background.jpg' with your image path */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            height: 100vh;
        }

        .header {
            margin-top: 20px;
            text-align: center;
            font-size: 2em;
            font-weight: bold;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .gallery-item {
            border: 2px solid #ddd;
            overflow: hidden;
            border-radius: 10px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            width: 200px;
            height: 250px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background-color: rgba(255, 255, 255, 0.8); /* Background color for better readability */
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .gallery-item img {
            width: 200px;
            height: 200px;
            object-fit: cover;
        }

        .gallery-item .caption {
            text-align: center;
            margin-top: 10px;
            font-size: 1em;
            color: #333;
        }

        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .modal.show {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            position: relative;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            width: 400px;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .modal-content img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 24px;
            cursor: pointer;
            color: #000;
            background: #fff;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
    </style>
</head>
<body>
    <div class="header">FOODIE WORLD WELCOMES YOU</div>
    <div class="gallery">
        <div class="gallery-item">
            <img src="m1.jpg" alt="Image 1">
            <div class="caption">Bruschetta</div>
        </div>
        <div class="gallery-item">
            <img src="m2.jpg" alt="Image 2">
            <div class="caption">Stuffed Mushrooms</div>
        </div>
        <div class="gallery-item">
            <img src="m3.jpg" alt="Image 3">
            <div class="caption">Fried Calamari</div>
        </div>
        <div class="gallery-item">
            <img src="m7.jpg" alt="Image 4">
            <div class="caption">Tiramisu</div>
        </div>
        <div class="gallery-item">
            <img src="m8.jpg" alt="Image 5">
            <div class="caption">Cheesecake</div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const galleryItems = document.querySelectorAll('.gallery-item');

            galleryItems.forEach(item => {
                item.addEventListener('click', () => {
                    const img = item.querySelector('img');
                    const modal = document.createElement('div');
                    modal.classList.add('modal');
                    modal.innerHTML = `
                        <div class="modal-content">
                            <span class="close">&times;</span>
                            <img src="${img.src}" alt="${img.alt}">
                        </div>
                    `;

                    document.body.appendChild(modal);

                    // Show the modal with a transition
                    setTimeout(() => modal.classList.add('show'), 10);

                    const close = modal.querySelector('.close');
                    close.addEventListener('click', () => {
                        modal.classList.remove('show');
                        setTimeout(() => document.body.removeChild(modal), 300);
                    });
                });
            });
        });
    </script>
</body>
</html>
```
## OUTPUT:
![out 1](https://github.com/user-attachments/assets/adc2e7c0-5a50-4682-b006-b14897f7cf36)

![out 2](https://github.com/user-attachments/assets/06c4091b-44da-4e35-95bf-ca7432269f14)

![out 3](https://github.com/user-attachments/assets/cd9306fa-5ae5-4615-82d3-9a5fe63c2e42)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
