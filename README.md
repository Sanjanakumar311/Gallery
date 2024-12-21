# Ex.08 Design of Interactive Image Gallery
# Date:12.12.2024
# AIM:To design a web application for an inteactive image gallery with minimum five images.
# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
``` python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IMAGE GALLERY</title>
    <link rel="stylesheet" href=""
</head>

<style>

    body {
    margin: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100vh;
    background: rgb(68, 60, 60);
    overflow: hidden;
  }
  .image-container {
    position: relative;
    width: 200px;
    height: 200px;
    transform-style: preserve-3d;
    transform: perspective(1000px) rotateY(0deg);
    transition: transform 0.9s;
  }
  .image-container span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px);
  }
  .image-container span img {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
  }
  .btn-container {
    position: relative;
    width: 80%;
  }
  .btn {
    position: absolute;
    bottom: -250px;
    background: rgb(162, 28, 28);
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  #prev {
    left: 20%;
  }
  #next {
    right: 20%;
  }
  .btn:hover {
    filter: brightness(1);
  }

</style>

<body>

    <div class="image-container">

        <span style="--i:1">
            <img src="nn.jpg" width="260" height="300">
        </span>

        <span style="--i:2">
            <img src="k.jpg" width="220" height="300">
        </span>

        <span style="--i:3">
            <img src="s.webp" width="220" height="300">
        </span>

        <span style="--i:4">
            <img src="i.jpg" width="220" height="300">
        </span>

        <span style="--i:5">
            <img src="jj.jpg" width="220" height="300">
        </span>

        <span style="--i:6">
            <img src= "mi.jpg" width="220" height="300">
        </span>

        <span style="--i:7">
            <img src="sak.jpg" width="220" height="300">
        </span>

        <span style="--i:8">
            <img src=" hi.jpg" width="220" height="300">
        </span>


    </div>

    <div class="btn-container">
        <button class="btn" id="prev">PREV</button>
        <button class="btn" id="next">NEXT</button>
    </div>

    <script>

      const imageContainer = document.querySelector('.image-container');
      const prevBtn = document.getElementById('prev');
      const nextBtn = document.getElementById('next');
      
      let x=0;
      prevBtn.addEventListener('click',( ) => {


          x=x+45
          rotate()
      })
      nextBtn.addEventListener('click',( ) => {


          x=x-45
          rotate()
      })
      function rotate() {
          imageContainer.style.transform=`perspective(1000px) rotateY(${x}deg)`;

      }
      
    </script>

</body>
</html>
```
# OUTPUT:

![Screenshot (92)](https://github.com/user-attachments/assets/48f0752e-10e1-4934-b85e-dedb1fb2f101)

![Screenshot (98)](https://github.com/user-attachments/assets/0f8f0bcb-a4a9-401c-a831-5ddfa2cb661a)

![Screenshot (97)](https://github.com/user-attachments/assets/cb32b433-4a54-4a5a-a3aa-2c6130b1ffbb)

![Screenshot (96)](https://github.com/user-attachments/assets/470a9503-e717-421e-9544-bde7939810b5)

![Screenshot (95)](https://github.com/user-attachments/assets/06d411e8-3f20-460b-b762-a751c705ddfa)

![Screenshot (94)](https://github.com/user-attachments/assets/e0cfc3b3-e80c-4b13-98d6-6cb791cbca36)

![Screenshot (93)](https://github.com/user-attachments/assets/34728573-7355-4864-8338-56730e11c613)



# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
