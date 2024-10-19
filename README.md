<!DOCTYPE html>
<html lang="es">
<head>    
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta de Amor Interactiva</title>
    <style>    
        /* Estilos principales y románticos */
        body {    
            font-family: 'Comic Sans MS', sans-serif;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #FFF0F5; /* Fondo amoroso en color lavanda */
            color: #FF1493;      
        }
        .card {    
            width: 350px;
            height: 350px; /* Incrementé la altura para la imagen */
            background-color: #FFB6C1; /* Color rosado claro */
            border-radius: 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            transition: background-color 0.5s ease;
        }
        .card h1 {  
            font-size: 24px;
            color: white;
        }
        .card img {  
            width: 200px; /* Tamaño de la imagen */
            border-radius: 10px;
            margin-bottom: 10px;
        }
        .buttons {
            margin-top: 20px;
            display: flex;
            justify-content: space-between;
            width: 350px;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s ease;
        }
        .open-btn {
            background-color: #FF1493; /* Color rosa fuerte */
            color: white;
        }
        .open-btn:hover {
            background-color: #D402C7; /* Color púrpura oscuro al pasar el ratón */
        }
        .close-btn {
            background-color: #FF4500; /* Color naranja */
            color: white;
        }
        .close-btn:hover {
            background-color: #FF6347; /* Color rojo claro al pasar el ratón */
        }
        .next-btn {  
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #FF69B4; /* Color rosa fuerte */
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            display: none; /* Se muestra solo al abrir */
        }
        .next-btn:hover {  
            background-color: #D402C7; /* Color púrpura oscuro */
        }
        .hearts {  
            position: absolute;
            bottom: 10px;
            font-size: 30px;
            color: #FF69B4;                                                                  
        }
    </style>                                                                  
</head>                                                                  
<body>                                                                        

<!-- Carta que cambia su contenido al abrir y cerrar -->
<div class="card" id="card">
    <div id="message">
        <h1>Te amo mi amor 💖</h1>
    </div>                                                                                                
    <div class="hearts">💖💖💖</div>
</div>                                                                                                

<!-- Botones de abrir y cerrar -->
<div class="buttons">
    <button class="open-btn" id="open-btn">Abrir</button>
    <button class="close-btn" id="close-btn">Cerrar</button>
</div>                                                                                                        

<!-- Botón de siguiente -->
<button class="next-btn" id="next-btn">Siguiente</button>

<script>                                                                                                          
    const card = document.getElementById('card');
    const openBtn = document.getElementById('open-btn');
    const closeBtn = document.getElementById('close-btn');
    const nextBtn = document.getElementById('next-btn');  
    const message = document.getElementById('message');

    // Acción al hacer clic en "Abrir"  
    openBtn.addEventListener('click', function() {
        card.style.backgroundColor = '#FF69B4'; // Cambia a color rosa fuerte
        message.innerHTML = `
            <h1>Te amo mi amor 💖</h1>  
            <img src="https://example.com/imagen-romantica.jpg" alt="Imagen romántica">
         `;                                                                                           nextBtn.styl. display = 'block'; // Muestra el botón de "Siguiente"    
    });                                                                                                  
  
    // Acción al hacer clic en "Cerrar"
    closeBtn.addEventListener('click', function() {  
        card.style.backgroundColor = '#FF6347'; // Cambia a color rojo claro
        message.innerHTML = '<h1>Abrilo cada vez que dudes de mi amor 💔</h1>';
        nextBtn.style.display = 'none'; // Oculta el botón de "Siguiente"
    });                                                                                                        

    // Acción al hacer clic en "Siguiente"
    nextBtn.addEventListener('click', function() {
        card.style.backgroundColor = '#D402C7'; // Cambia a color púrpura
        message.innerHTML = '<h1>Te amo mucho Zahira, sos lo mejor que me pasó ❤️</h1>';  
    });                                                                                          
</script>                                                                

</body>                                                              
</html>                                                          
