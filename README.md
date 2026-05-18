<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pastelería del Infinito</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body{
      background: linear-gradient(135deg, #d9f3ff, #e8d8ff);
      color:#222;
    }

    header{
      background: linear-gradient(90deg, #6ec6ff, #8a4fff, #ff5b6e);
      color:white;
      padding:25px;
      text-align:center;
      box-shadow:0 4px 10px rgba(0,0,0,0.2);
    }

    header h1{
      font-size:3rem;
      letter-spacing:2px;
    }

    header p{
      margin-top:10px;
      font-size:1.1rem;
    }

    nav{
      background:#ffffffcc;
      backdrop-filter: blur(5px);
      display:flex;
      justify-content:center;
      gap:20px;
      padding:15px;
      position:sticky;
      top:0;
      z-index:100;
    }

    nav a{
      text-decoration:none;
      color:#7a2cff;
      font-weight:bold;
      transition:0.3s;
    }

    nav a:hover{
      color:#ff3c5f;
      transform:scale(1.1);
    }

    .hero{
      height:70vh;
      display:flex;
      align-items:center;
      justify-content:center;
      flex-direction:column;
      text-align:center;
      background:url('https://images.unsplash.com/photo-1519864600265-abb23847ef2c?q=80&w=1200') center/cover;
      color:white;
      position:relative;
    }

    .hero::before{
      content:"";
      position:absolute;
      inset:0;
      background:rgba(0,0,0,0.45);
    }

    .hero-content{
      position:relative;
      z-index:2;
    }

    .hero h2{
      font-size:4rem;
      margin-bottom:15px;
    }

    .hero button{
      padding:15px 30px;
      border:none;
      border-radius:30px;
      background:#ff5b6e;
      color:white;
      font-size:1rem;
      cursor:pointer;
      transition:0.3s;
    }

    .hero button:hover{
      background:#8a4fff;
      transform:scale(1.05);
    }

    .productos{
      padding:60px 20px;
    }

    .productos h2{
      text-align:center;
      margin-bottom:40px;
      color:#7a2cff;
      font-size:2.5rem;
    }

    .grid{
      display:grid;
      grid-template-columns:repeat(auto-fit, minmax(250px, 1fr));
      gap:30px;
    }

    .card{
      background:white;
      border-radius:20px;
      overflow:hidden;
      box-shadow:0 6px 15px rgba(0,0,0,0.15);
      transition:0.3s;
    }

    .card:hover{
      transform:translateY(-10px);
    }

    .card img{
      width:100%;
      height:220px;
      object-fit:cover;
    }

    .card-content{
      padding:20px;
    }

    .card h3{
      color:#ff3c5f;
      margin-bottom:10px;
    }

    .precio{
      color:#7a2cff;
      font-size:1.3rem;
      font-weight:bold;
      margin-top:10px;
    }

    .btn-comprar{
      margin-top:15px;
      padding:10px 20px;
      border:none;
      border-radius:20px;
      background:#6ec6ff;
      color:white;
      cursor:pointer;
      transition:0.3s;
    }

    .btn-comprar:hover{
      background:#ff5b6e;
    }

    .contacto{
      padding:60px 20px;
      background:#ffffffaa;
      text-align:center;
    }

    .contacto h2{
      color:#7a2cff;
      margin-bottom:20px;
    }

    input, textarea{
      width:80%;
      max-width:500px;
      margin:10px 0;
      padding:15px;
      border-radius:10px;
      border:1px solid #ccc;
    }

    .contacto button{
      padding:12px 25px;
      border:none;
      background:#8a4fff;
      color:white;
      border-radius:20px;
      cursor:pointer;
      transition:0.3s;
    }

    .contacto button:hover{
      background:#ff5b6e;
    }

    footer{
      background:#7a2cff;
      color:white;
      text-align:center;
      padding:20px;
      margin-top:30px;
    }

    .mensaje{
      margin-top:15px;
      font-weight:bold;
      color:#ff3c5f;
    }
  </style>
</head>

<body>

  <header>
    <h1>Pastelería del Infinito</h1>
    <p>Dulces que parecen infinitos ✨</p>
  </header>

  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#productos">Productos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <section class="hero" id="inicio">
    <div class="hero-content">
      <h2>Postres mágicos y deliciosos</h2>
      <button onclick="mostrarMensaje()">Descubrir más</button>
      <p class="mensaje" id="mensaje"></p>
    </div>
  </section>

  <section class="productos" id="productos">
    <h2>Nuestros Productos</h2>

    <div class="grid">

      <div class="card">
        <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?q=80&w=1000" alt="Torta">
        <div class="card-content">
          <h3>Torta de Chocolate</h3>
          <p>Deliciosa torta rellena de chocolate premium.</p>
          <div class="precio">$45.000 COP</div>
          <button class="btn-comprar">Comprar</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1486427944299-d1955d23e34d?q=80&w=1000" alt="Cupcakes">
        <div class="card-content">
          <h3>Cupcakes Especiales</h3>
          <p>Decorados con crema y sabores únicos.</p>
          <div class="precio">$18.000 COP</div>
          <button class="btn-comprar">Comprar</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1551024601-bec78aea704b?q=80&w=1000" alt="Macarons">
        <div class="card-content">
          <h3>Macarons Franceses</h3>
          <p>Suaves, coloridos y llenos de sabor.</p>
          <div class="precio">$28.000 COP</div>
          <button class="btn-comprar">Comprar</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1563729784474-d77dbb933a9e?q=80&w=1000" alt="Cheesecake">
        <div class="card-content">
          <h3>Cheesecake de Fresa</h3>
          <p>Postre suave con cobertura de fresas.</p>
          <div class="precio">$38.000 COP</div>
          <button class="btn-comprar">Comprar</button>
        </div>
      </div>

    </div>
  </section>

  <section class="contacto" id="contacto">
    <h2>Contáctanos</h2>

    <input type="text" placeholder="Tu nombre">
    <br>

    <input type="email" placeholder="Tu correo">
    <br>

    <textarea rows="5" placeholder="Escribe tu mensaje"></textarea>
    <br>

    <button>Enviar</button>
  </section>

  <footer>
    <p>© 2026 Pastelería del Infinito | Bogotá, Colombia</p>
  </footer>

  <script>
    function mostrarMensaje(){
      document.getElementById("mensaje").innerHTML =
      "🍰 Bienvenido a Pastelería del Infinito 🍰";
    }

    const botones = document.querySelectorAll(".btn-comprar");

    botones.forEach(boton => {
      boton.addEventListener("click", () => {
        alert("Producto agregado al carrito 🛒");
      });
    });
  </script>

</body>
</html>
