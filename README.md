# GdscProject1
It is an image slider made by using HTML and CSS only.
<!DOCTYPE html>
<html lang="en">
    <head> 
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Image Slider</title>
        <link href="style.CSS" type="text/CSS" rel="stylesheet" />
    </head>
    <body>
       
        <div class="slider" >
            
            <div class="images" >
                <input type="radio" name="slide" id="img1" checked>
                <input type="radio" name="slide" id="img2" >
                <input type="radio" name="slide" id="img3" >
                <img src="img1.jpg" class="m1" alt="img1">
                <img src="img2.jpg" class="m2" alt="img2">
                <img src="img3.jpg" class="m3" alt="img3">
            </div>
            <div class="dots">
                <label for="img1"></label>
                <label for="img2"></label>
                <label for="img3"></label>
            </div>
            
        </div>

    </body>
</html>
*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
body{
    height: 100vh;
    display:flex;
    justify-content: center;
    align-items: center;
    background-image: url('backImg.jpg');
    background-size: cover;
}
.slider{
    position:relative;
    width:500px;
    overflow:hidden;
    }
    .images{
        display: flex;
        width:100%;
        box-shadow: 5px 5px 10px 5px rgb(0,40,60);
     }
     .images img{
         height:400px;
         width:500px;
         transition:all 0.15s ease;
     }
     .images input{ 
         display:none;
     }
     .dots{
         display:flex;
         justify-content: center;
         margin:5px;
     }
     .dots label{
         height: 20px;
         width: 20px;
         border-radius: 50%;
         border:solid #fff 3px;
         cursor:pointer;
         transition: all 0.15s ease;
         margin: 5px;
     }
     .dots label:hover{background: #fff;}
     #img1:checked~.m1{
        margin-left:0%;
     }
     #img2:checked~.m2{
       margin-left:-100%;
    }
    #img3:checked~.m3{
       margin-left:-200%;
    }
