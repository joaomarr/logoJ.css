# logoJ.css
//That was my first animated css code, by using linear-gradient and cubic-bezier in animation-timing-function, the idea were roughly make a logo with "J" letter, my name's first letter.

//Html content
<!DOCTYPE html>
 <html>
  <head>
    <title>Teste de borda</title>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <div class="box">
      <h2>J</h2>
    </div>
  </body>
 </html>
 
//Css content
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap');
*{
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    display:flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: rgb(40, 64, 199);
}
.box{
    position:relative;
    width:300px;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center; 
    color: white;
    font-size: 8em;
    background: rgba(0, 0, 0, 0.5);
    z-index: 10;
    overflow: hidden;
    border-radius: 150px;
}
.box h2{
    z-index: 10000;
}
.box::before{
   content: "";
   position: absolute;
   width: 150px;
   height: 130%;
   background: linear-gradient(#006781,#d400d4);
   z-index: -1;
   animation:animation 4s linear infinite;
   animation-timing-function: cubic-bezier(0.445, 0.05, 0.55, 0.95);
}
.box::after{
    content:"";
    position: absolute;
    width: 200px;
    height: 300px;
    background: #050b29;
    border-radius: 160px;
    
}
@keyframes animation {
    0%{
      transform: rotate(0deg);
    }
    100%{
      transform: rotate(360deg);
    }
}
