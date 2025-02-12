<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Serás mi San Valentín?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        h1 {
            font-size: 2em;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        #contenedor {
            position: relative;
            margin-top: 20px;
        }

        .boton {
            font-size: 1.2em;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }

        #si {
            background-color: #ff4d79;
            color: white;
        }

        #si:hover {
            background-color: #ff1a4d;
        }

        #no {
            background-color: #666;
            color: white;
            position: absolute;
        }

        #mensaje {
            display: none;
            font-size: 1.5em;
            color: white;
            margin-top: 20px;
        }

        #gif {
            width: 250px;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>

    <h1>Gorda, ¿quieres ser mi San Valentín? ❤️</h1>

    <div id="contenedor">
        <button id="si" class="boton">Sí</button>
        <button id="no" class="boton">No</button>
    </div>

    <div id="mensaje">
        ¡Sabía que dirías que sí, mi amor! 💕  
        <br>  
        Eres lo mejor que me ha pasado, gracias por estar conmigo.  
    </div>

    <img id="gif" src="https://media.giphy.com/media/3oz8xKaR836UJOYeOc/giphy.gif" alt="Pareja feliz">

    <script>
        let botonNo = document.getElementById("no");
        let botonSi = document.getElementById("si");
        let mensaje = document.getElementById("mensaje");
        let gif = document.getElementById("gif");

        botonNo.addEventListener("mouseover", function () {
            let x = Math.random() * (window.innerWidth - botonNo.clientWidth);
            let y = Math.random() * (window.innerHeight - botonNo.clientHeight);
            botonNo.style.left = `${x}px`;
            botonNo.style.top = `${y}px`;
        });

        botonSi.addEventListener("click", function () {
            mensaje.style.display = "block";
            gif.style.display = "block";
            document.getElementById("contenedor").style.display = "none";
        });
    </script>

</body>
</html>

