TODO-CASERO
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="Todo Casero - Rotisería con los mejores sándwiches, hamburguesas, pizzas y pastas caseras. Abierto de Lun-Dom: 20:00-23:45">
  <title>Todo Casero - Rotisería | Campana</title>
  <style>
    :root {
      --primary-color: #e67e22;
      --secondary-color: #f39c12;
      --light-color: #fffbe6;
      --dark-color: #333;
      --accent-color: #25d366;
      --shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
   
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
   
    body {
      font-family: 'Segoe UI', 'Roboto', sans-serif;
      line-height: 1.6;
      background-color: var(--light-color);
      color: var(--dark-color);
    }
   
    header {
      background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
      padding: 1.5rem;
      text-align: center;
      box-shadow: var(--shadow);
      position: relative;
      z-index: 100;
    }
   
    .logo {
      font-size: 2.5rem;
      font-weight: bold;
      color: white;
      margin-bottom: 0.5rem;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
      animation: microEffect 1s infinite alternate;
    }
   
    @keyframes microEffect {
      from { transform: scale(1); }
      to { transform: scale(1.05); }
    }
   
    .tagline {
      color: white;
      font-style: italic;
      margin-bottom: 1rem;
    }
   
    nav {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 1rem;
      flex-wrap: wrap;
    }
   
    nav a {
      text-decoration: none;
      color: white;
      font-weight: bold;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      transition: background 0.3s;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
   
    nav a:hover {
      background-color: rgba(255,255,255,0.2);
    }
   
    .hero {
      background: url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover;
      height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      position: relative;
    }
   
    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.5);
    }
   
    .hero-content {
      position: relative;
      z-index: 1;
      color: white;
      max-width: 800px;
      padding: 2rem;
    }
   
    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
   
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
    }
   
    .btn {
      display: inline-block;
      background-color: var(--primary-color);
      color: white;
      padding: 0.8rem 1.5rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: bold;
      transition: all 0.3s;
      border: none;
      cursor: pointer;
    }
   
    .btn:hover {
      background-color: #d35400;
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
   
    .btn-whatsapp {
      background-color: var(--accent-color);
    }
   
    .btn-whatsapp:hover {
      background-color: #128C7E;
    }
   
    .section {
      padding: 4rem 2rem;
      max-width: 1200px;
      margin: 0 auto;
    }
   
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
      font-size: 2rem;
      color: var(--primary-color);
      position: relative;
    }
   
    .section-title::after {
      content: '';
      display: block;
      width: 80px;
      height: 4px;
      background-color: var(--secondary-color);
      margin: 0.5rem auto 0;
    }
   
    .menu-section {
      background-color: white;
      border-radius: 8px;
      box-shadow: var(--shadow);
      padding: 2rem;
      margin-bottom: 2rem;
    }
   
    .category {
      margin-bottom: 2rem;
    }
   
    .category-header {
      background-color: var(--primary-color);
      color: white;
      padding: 1rem;
      border-radius: 4px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: all 0.3s;
    }
   
    .category-header:hover {
      background-color: #d35400;
    }
   
    .category-header h3 {
      margin: 0;
    }
   
    .products {
      display: none;
      padding: 1rem;
      background-color: #f9f9f9;
      border-radius: 0 0 4px 4px;
    }
   
    .product {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
      border-bottom: 1px solid #eee;
      transition: all 0.3s;
    }
   
    .product:last-child {
      border-bottom: none;
    }
   
    .product:hover {
      background-color: #f1f1f1;
    }
   
    .product-info {
      flex: 1;
    }
   
    .product-name {
      font-weight: bold;
      font-size: 1.1rem;
      margin-bottom: 0.3rem;
    }
   
    .product-description {
      color: #666;
      font-size: 0.9rem;
    }
   
    .product-price {
      font-weight: bold;
      color: var(--primary-color);
      font-size: 1.2rem;
      margin-left: 1rem;
      white-space: nowrap;
    }
   
    .product-stock {
      font-size: 0.9rem;
      color: #888;
      margin-left: 1rem;
    }
   
    .product-image {
      width: 80px;
      height: 80px;
      object-fit: cover;
      border-radius: 4px;
      margin-left: 1rem;
    }
   
    .add-to-cart {
      background-color: var(--secondary-color);
      color: white;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      border: none;
      cursor: pointer;
      margin-left: 1rem;
      transition: all 0.3s;
    }
   
    .add-to-cart:hover {
      background-color: #e67e22;
    }
   
    .offer-banner {
      background: linear-gradient(135deg, #e74c3c, #c0392b);
      color: white;
      padding: 1rem;
      text-align: center;
      border-radius: 4px;
      margin-bottom: 2rem;
      animation: pulse 2s infinite;
    }
   
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.02); }
      100% { transform: scale(1); }
    }
   
    .info-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }
   
    .info-card {
      background-color: white;
      border-radius: 8px;
      box-shadow: var(--shadow);
      padding: 2rem;
      text-align: center;
    }
   
    .info-card i {
      font-size: 2.5rem;
      color: var(--primary-color);
      margin-bottom: 1rem;
    }
   
    .info-card h3 {
      margin-bottom: 1rem;
      color: var(--primary-color);
    }
   
    .payment-info {
      background-color: #f8f9fa;
      padding: 1.5rem;
      border-radius: 4px;
      margin-top: 2rem;
      border-left: 4px solid var(--accent-color);
      transition: all 0.3s;
    }
   
    .payment-info:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
   
    .payment-method {
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
    }
   
    .payment-method input {
      margin-right: 1rem;
    }
   
    footer {
      background-color: var(--dark-color);
      color: white;
      text-align: center;
      padding: 2rem;
      margin-top: 3rem;
    }
   
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      text-align: left;
    }
   
    .footer-section h3 {
      margin-bottom: 1rem;
      color: var(--secondary-color);
    }
   
    .footer-section ul {
      list-style: none;
    }
   
    .footer-section ul li {
      margin-bottom: 0.5rem;
    }
   
    .footer-section ul li a {
      color: #ddd;
      text-decoration: none;
      transition: color 0.3s;
    }
   
    .footer-section ul li a:hover {
      color: var(--secondary-color);
    }
   
    .copyright {
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid #444;
    }
   
    .whatsapp-float {
      position: fixed;
      bottom: 2rem;
      right: 2rem;
      background-color: var(--accent-color);
      color: white;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      transition: all 0.3s;
      z-index: 99;
      text-decoration: none;
    }
   
    .whatsapp-float:hover {
      background-color: #128C7E;
      transform: translateY(-5px);
      box-shadow: 0 8px 16px rgba(0,0,0,0.3);
    }
   
    .cart-modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.7);
      z-index: 999;
      justify-content: center;
      align-items: center;
    }
   
    .cart-content {
      background-color: white;
      padding: 2rem;
      border-radius: 8px;
      max-width: 600px;
      width: 90%;
      max-height: 80vh;
      overflow-y: auto;
    }
   
    .cart-content h3 {
      margin-bottom: 1rem;
      color: var(--primary-color);
    }
   
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 0;
      border-bottom: 1px solid #eee;
    }
   
    .cart-item:last-child {
      border-bottom: none;
    }
   
    .cart-item span {
      flex: 1;
    }
   
    .cart-item button {
      background-color: #e74c3c;
      color: white;
      padding: 0.5rem;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
   
    .cart-total {
      margin-top: 1rem;
      font-weight: bold;
      text-align: right;
    }
   
    .cart-actions {
      margin-top: 1rem;
      display: flex;
      justify-content: space-between;
    }
   
    .customer-info input {
      width: 100%;
      padding: 0.8rem;
      margin-bottom: 1rem;
      border: 1px solid #ddd;
      border-radius: 4px;
    }
   
    .chat-widget {
      position: fixed;
      bottom: 80px;
      right: 2rem;
      width: 300px;
      background-color: white;
      border-radius: 8px;
      box-shadow: var(--shadow);
      z-index: 100;
      display: none;
    }
   
    .chat-header {
      background: var(--primary-color);
      color: white;
      padding: 1rem;
      border-radius: 8px 8px 0 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
   
    .chat-body {
      max-height: 300px;
      overflow-y: auto;
      padding: 1rem;
    }
   
    .chat-message {
      margin-bottom: 1rem;
      padding: 0.5rem;
      border-radius: 4px;
    }
   
    .chat-message.user {
      background-color: var(--light-color);
      text-align: right;
    }
   
    .chat-message.bot {
      background-color: #f1f1f1;
      text-align: left;
    }
   
    .chat-input {
      display: flex;
      padding: 1rem;
      border-top: 1px solid #eee;
    }
   
    .chat-input input {
      flex: 1;
      padding: 0.5rem;
      border: 1px solid #ddd;
      border-radius: 4px 0 0 4px;
    }
   
    .chat-input button {
      padding: 0.5rem 1rem;
      background-color: var(--primary-color);
      color: white;
      border: none;
      border-radius: 0 4px 4px 0;
      cursor: pointer;
    }
   
    .admin-panel {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: white;
      padding: 2rem;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
      z-index: 1000;
      width: 90%;
      max-width: 800px;
      max-height: 90vh;
      overflow-y: auto;
      border-radius: 8px;
    }
   
    .admin-panel h3 {
      color: var(--primary-color);
      margin-bottom: 1.5rem;
      text-align: center;
    }
   
    .admin-form {
      display: grid;
      gap: 1rem;
    }
   
    .admin-form label {
      font-weight: bold;
      color: var(--dark-color);
    }
   
    .admin-form input,
    .admin-form select,
    .admin-form textarea {
      padding: 0.8rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      font-family: inherit;
    }
   
    .admin-form button {
      padding: 0.8rem;
      background-color: var(--primary-color);
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s;
    }
   
    .admin-form button:hover {
      background-color: #d35400;
    }
   
    .close-admin {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background: none;
      border: none;
      font-size: 1.5rem;
      cursor: pointer;
      color: #666;
    }
   
    .image-preview {
      max-width: 150px;
      max-height: 150px;
      margin-top: 0.5rem;
      display: block;
    }
   
    .product-list {
      margin-top: 2rem;
    }
   
    .product-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
      border-bottom: 1px solid #eee;
    }
   
    .product-item button {
      margin-left: 1rem;
    }
   
    .offer-form {
      margin-top: 2rem;
      border-top: 1px solid #eee;
      padding-top: 1rem;
    }
   
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2rem;
      }
     
      .hero p {
        font-size: 1rem;
      }
     
      .section {
        padding: 2rem 1rem;
      }
     
      .product {
        flex-direction: column;
        align-items: flex-start;
      }
     
      .product-price {
        margin-left: 0;
        margin-top: 0.5rem;
      }
     
      .product-stock {
        margin-left: 0;
        margin-top: 0.5rem;
      }
     
      .product-image {
        margin-left: 0;
        margin-top: 1rem;
      }
     
      .add-to-cart {
        margin-left: 0;
        margin-top: 0.5rem;
      }
     
      .chat-widget {
        width: 90%;
        bottom: 70px;
        right: 1rem;
      }
    }
   
    .category-arrow {
      transition: transform 0.3s;
    }
   
    .category-header.active .category-arrow {
      transform: rotate(90deg);
    }
   
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.7);
      z-index: 999;
      justify-content: center;
      align-items: center;
    }
   
    .modal-content {
      background-color: white;
      padding: 2rem;
      border-radius: 8px;
      max-width: 500px;
      width: 90%;
      text-align: center;
    }
   
    .modal h3 {
      margin-bottom: 1rem;
      color: var(--primary-color);
    }
   
    .modal input {
      width: 100%;
      padding: 0.8rem;
      margin-bottom: 1rem;
      border: 1px solid #ddd;
      border-radius: 4px;
    }
   
    .modal button {
      margin-top: 1rem;
    }
  </style>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/js/all.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
</head>
<body>

<header>
  <div class="logo">Todo Casero</div>
  <div class="tagline">Auténtica comida casera en Campana</div>
  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#menu">Menú</a>
    <a href="#pedidos">Cómo Pedir</a>
    <a href="#contacto">Contacto</a>
    <a href="#" id="viewCart"><i class="fas fa-shopping-cart"></i> Carrito (<span id="cartCount">0</span>)</a>
  </nav>
</header>

<section class="hero" id="inicio">
  <div class="hero-content">
    <h1>Los sabores más caseros de Campana</h1>
    <p>Delicias recién hechas todos los días de 19:30 a 23:45</p>
    <a href="#menu" class="btn">Ver Menú</a>
    <a href="#" class="btn btn-whatsapp" onclick="toggleChat()">Chatear con María</a>
  </div>
</section>

<section class="section" id="menu">
  <h2 class="section-title">Nuestro Menú</h2>
 
  <div class="offer-banner" id="offerBanner">
    <h3>¡Ofertas Especiales!</h3>
    <p id="offerText"></p>
  </div>
 
  <div class="menu-section">
    <div id="categoriesContainer"></div>
  </div>
</section>

<section class="section" id="pedidos">
  <h2 class="section-title">Cómo Hacer tu Pedido</h2>
 
  <div class="info-cards">
    <div class="info-card">
      <i class="fas fa-utensils"></i>
      <h3>Elige tu comida</h3>
      <p>Selecciona entre nuestra variedad de sándwiches, pizzas, pastas y más.</p>
    </div>
   
    <div class="info-card">
      <i class="fas fa-comment"></i>
      <h3>Haz tu pedido</h3>
      <p>Chatea con nuestra asistente María o usa WhatsApp al +54 348 9358998.</p>
    </div>
   
    <div class="info-card">
      <i class="fas fa-store"></i>
      <h3>Recoge en local</h3>
      <p>Retira tu pedido en nuestro local en el horario acordado.</p>
    </div>
  </div>
</section>

<section class="section" id="contacto">
  <h2 class="section-title">Contacto</h2>
 
  <div class="info-cards">
    <div class="info-card">
      <i class="fas fa-map-marker-alt"></i>
      <h3>Ubicación</h3>
      <p>Campana, Buenos Aires</p>
    </div>
   
    <div class="info-card">
      <i class="fas fa-clock"></i>
      <h3>Horario</h3>
      <p>Lunes a Domingo<br>19:30 - 23:45</p>
    </div>
   
    <div class="info-card">
      <i class="fab fa-whatsapp"></i>
      <h3>Teléfono</h3>
      <p>+54 348 9358998</p>
      <a href="#" class="btn btn-whatsapp" style="margin-top: 1rem;" onclick="toggleChat()">
        <i class="fab fa-whatsapp"></i> Chatea con María
      </a>
    </div>
  </div>
</section>

<div id="chatWidget" class="chat-widget">
  <div class="chat-header">
    <span>Chat con María de Todo Casero</span>
    <button onclick="toggleChat()">×</button>
  </div>
  <div class="chat-body" id="chatBody"></div>
  <div class="chat-input">
    <input type="text" id="chatInput" placeholder="Escribe tu consulta...">
    <button onclick="sendChatMessage()">Enviar</button>
  </div>
</div>

<footer>
  <div class="footer-content">
    <div class="footer-section">
      <h3>Todo Casero</h3>
      <p>Auténtica comida casera preparada con los mejores ingredientes y mucho amor.</p>
    </div>
   
    <div class="footer-section">
      <h3>Menú</h3>
      <ul>
        <li><a href="#menu">Sándwiches</a></li>
        <li><a href="#menu">Pizzas</a></li>
        <li><a href="#menu">Pastas</a></li>
        <li><a href="#menu">Hamburguesas</a></li>
      </ul>
    </div>
   
    <div class="footer-section">
      <h3>Contacto</h3>
      <ul>
        <li><i class="fas fa-map-marker-alt"></i> Campana, BA</li>
        <li><i class="fas fa-phone"></i> +54 348 9358998</li>
        <li><i class="fas fa-clock"></i> Lun-Dom: 19:30-23:45</li>
      </ul>
    </div>
  </div>
 
  <div class="copyright">
    © 2025 Todo Casero - Todos los derechos reservados |
    <span id="adminLink" style="cursor:pointer; text-decoration:underline;">Acceso Administrador</span>
  </div>
</footer>

<a href="#" class="whatsapp-float" onclick="toggleChat()">
  <i class="fas fa-comment"></i>
</a>

<div id="cartModal" class="cart-modal">
  <div class="cart-content">
    <h3>Tu Carrito</h3>
    <div id="cartItems"></div>
    <div class="cart-total" id="cartTotal"></div>
    <div class="customer-info">
      <h4>Datos del Cliente</h4>
      <input type="text" id="customerName" placeholder="Nombre" required>
      <input type="tel" id="customerPhone" placeholder="Celular" required>
    </div>
    <div class="payment-info">
      <h4>Métodos de Pago</h4>
      <div class="payment-method">
        <input type="radio" id="cartEfectivo" name="payment" value="Efectivo" checked>
        <label for="cartEfectivo">Efectivo al retirar</label>
      </div>
      <div class="payment-method">
        <input type="radio" id="cartTransferencia" name="payment" value="Transferencia">
        <label for="cartTransferencia">Transferencia bancaria</label>
      </div>
      <p id="cartTransferenciaInfo" style="display:none; background-color: white; padding: 1rem; border-radius: 4px; margin-top: 1rem;">
        <strong>Alias:</strong> Adri.roti<br>
        <strong>Titular:</strong> Adriana Basilia Enrique
      </p>
    </div>
    <div class="cart-actions">
      <button class="btn" onclick="closeCart()">Cerrar</button>
      <button class="btn btn-whatsapp" id="sendOrder">Enviar Pedido por WhatsApp</button>
    </div>
  </div>
</div>

<div id="adminPanel" class="admin-panel">
  <button class="close-admin" onclick="closeAdmin()">×</button>
  <h3>Panel de Administración</h3>
  <form id="productForm" class="admin-form">
    <div>
      <label for="categorySelect">Categoría</label>
      <select id="categorySelect" required>
        <option value="">Seleccione una categoría</option>
        <option value="Sándwiches">Sándwiches</option>
        <option value="Pizzas">Pizzas</option>
        <option value="Pizzas Individuales">Pizzas Individuales</option>
        <option value="Pastas">Pastas</option>
        <option value="Hamburguesas">Hamburguesas</option>
        <option value="Acompañamientos">Acompañamientos</option>
        <option value="Empanadas">Empanadas</option>
        <option value="Postres">Postres</option>
        <option value="Al Plato">Al Plato</option>
      </select>
    </div>
   
    <div>
      <label for="productName">Nombre del Producto</label>
      <input type="text" id="productName" required placeholder="Ej: Sándwich de Bondiola">
    </div>
   
    <div>
      <label for="productPrice">Precio (ARS)</label>
      <input type="number" id="productPrice" required placeholder="Ej: 9000">
    </div>
   
    <div>
      <label for="productStock">Stock</label>
      <input type="number" id="productStock" required placeholder="Ej: 10">
    </div>
   
    <div>
      <label for="productDescription">Descripción</label>
      <textarea id="productDescription" rows="3" placeholder="Descripción del producto"></textarea>
    </div>
   
    <div>
      <label for="productImage">Subir Imagen del Producto</label>
      <input type="file" id="productImage" accept="image/*">
    </div>
   
    <div>
      <label for="productImageUrl">O ingrese URL de la Imagen</label>
      <input type="url" id="productImageUrl" placeholder="Ej: https://example.com/image.jpg">
    </div>
   
    <div>
      <img id="previewImage" class="image-preview" style="display:none;">
    </div>
   
    <button type="submit">Agregar/Editar Producto</button>
    <button type="button" id="saveChanges" style="margin-top: 1rem;">Guardar Modificaciones</button>
  </form>
  <div class="product-list" id="productList"></div>
</div>

<div id="adminModal" class="modal">
  <div class="modal-content">
    <h3>Acceso Administrador</h3>
    <p>Ingrese la clave de acceso:</p>
    <input type="password" id="adminPassword" placeholder="Clave de acceso">
    <button class="btn" onclick="checkAdminPassword()">Ingresar</button>
  </div>
</div>

<script>
  const defaultProducts = [
    { id: 1, category: "Sándwiches", name: "Bondiola", price: 9000, description: "Delicioso sándwich de bondiola casera c/Fritas.", image: "https://raw.githubusercontent.com/NEXOar-art/Rotiser-a-Todo-Casero/main/BONDIOLA.jpeg"
, stock: 4 },
    { id: 2, category: "Sándwiches", name: "Bondiola Especial", price: 10000, description: "Bondiola con extras especiales c/Fritas.", image: "https://images.unsplash.com/photo-1565299503-7e5fcdb7d58e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 3, category: "Sándwiches", name: "Bondiola Premium", price: 11000, description: "Bondiola premium con ingredientes selectos c/Fritas.", image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 4, category: "Sándwiches", name: "Milanesa", price: 9500, description: "Clásico sándwich de milanesa con lechuga y tomate c/Fritas.", image: "https://images.unsplash.com/photo-1607013251379-e6eecfffe234?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 5, category: "Sándwiches", name: "Milanesa Especial", price: 10500, description: "Milanesa con extras especiales c/Fritas.", image: "https://images.unsplash.com/photo-1600891964599-f61ba0e24092?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 6, category: "Sándwiches", name: "Milanesa Completa", price: 11500, description: "Milanesa completa con todos los complementos c/Fritas.", image: "https://images.unsplash.com/photo-1579751626657-72bc17010498?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 7, category: "Sándwiches", name: "Tucumano", price: 14000, description: "Sándwich tucumano tradicional c/Fritas Doble.", image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 8, category: "Sándwiches", name: "Lomito Simple", price: 10000, description: "Lomito jugoso con tomate y lechuga c/Fritas.", image: "https://images.unsplash.com/photo-1565299503-7e5fcdb7d58e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 9, category: "Sándwiches", name: "Lomito Especial", price: 10500, description: "Lomito con extras especiales c/Fritas.", image: "https://images.unsplash.com/photo-1607013251379-e6eecfffe234?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 10, category: "Sándwiches", name: "Lomito Premium", price: 11000, description: "Lomito premium con ingredientes selectos c/Fritas.", image: "https://images.unsplash.com/photo-1600891964599-f61ba0e24092?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 11, category: "Hamburguesas", name: "Hamburguesa Completa", price: 8500, description: "Con lechuga, tomate, queso y mayonesa c/Fritas.", image: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 12, category: "Hamburguesas", name: "Hamburguesa Vegetariana", price: 8500, description: "Hamburguesa vegetariana deliciosa c/Fritas.", image: "https://images.unsplash.com/photo-1594219001565-31856e373dca?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 13, category: "Hamburguesas", name: "Hamburguesa Doble", price: 10500, description: "Doble carne y queso c/Fritas.", image: "https://images.unsplash.com/photo-1553979459-d2229ba7433b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 14, category: "Hamburguesas", name: "Hamburguesa Zapping", price: 25000, description: "Hamburguesa especial Zapping c/Fritas Doble.", image: "https://images.unsplash.com/photo-1550547660-d9450f859349?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 15, category: "Pizzas", name: "Muzzarella", price: 10000, description: "Pizza clásica con queso muzzarella, oregano, aceitunas.", image: "https://images.unsplash.com/photo-1513106580091-1d82408b8cd6?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 16, category: "Pizzas", name: "Fugaza", price: 11000, description: "Pizza fugaza tradicional.", image: "https://images.unsplash.com/photo-1604383898580-0f3b51d76a95?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 17, category: "Pizzas", name: "Napolitana", price: 11500, description: "Pizza napolitana con tomate, ajo y oregano.", image: "https://images.unsplash.com/photo-1593560708920-61dd98c36a39?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 18, category: "Pizzas", name: "Especial", price: 12000, description: "Pizza especial con jamon, morrones y aceitunas.", image: "https://images.unsplash.com/photo-1565299624946-baccd3051816?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 19, category: "Pizzas Individuales", name: "Muzzarella Individual", price: 5500, description: "Individual con queso muzzarella.", image: "https://images.unsplash.com/photo-1605477261677-455cbedde22c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 20, category: "Pizzas Individuales", name: "Fugaza Individual", price: 6000, description: "Individual fugaza tradicional.", image: "https://images.unsplash.com/photo-1604383898580-0f3b51d76a95?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 21, category: "Pizzas Individuales", name: "Napolitana Individual", price: 6500, description: "Individual napolitana con tomate y ajo.", image: "https://images.unsplash.com/photo-1593560708920-61dd98c36a39?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 22, category: "Pizzas Individuales", name: "Especial Individual", price: 7000, description: "Individual especial con jamon y morrones.", image: "https://images.unsplash.com/photo-1565299624946-baccd3051816?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 23, category: "Pastas", name: "Tallarines con Bolognesa", price: 8500, description: "Pasta fresca con salsa bolognesa casera.", image: "https://images.unsplash.com/photo-1608897013039-887f21d8c804?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 24, category: "Pastas", name: "Ñoquis con Bolognesa", price: 8500, description: "Ñoquis frescos con salsa bolognesa.", image: "https://images.unsplash.com/photo-1632778149848-d1e83ec03c34?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 25, category: "Pastas", name: "Ravioles con Bolognesa", price: 9500, description: "Ravioles frescos con salsa bolognesa.", image: "https://images.unsplash.com/photo-1603183138310-2b6b33a342e6?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 26, category: "Acompañamientos", name: "Porción de Fritas", price: 4500, description: "Porción grande de papas fritas.", image: "https://images.unsplash.com/photo-1630384060421-2a5d7752d2ad?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 27, category: "Acompañamientos", name: "Cono de Fritas", price: 3500, description: "Cono mediano de papas fritas.", image: "https://images.unsplash.com/photo-1576107491407-5e9e3e42e300?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 28, category: "Empanadas", name: "Empanadas", price: 17000, description: "Empanadas de Carne caseras x 12 unidades.", image: "https://images.unsplash.com/photo-1608507940435-c4a37d0d5411?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 29, category: "Empanadas", name: "Empanadas", price: 8500, description: "Empanadas de Carne caseras x 6 unidades.", image: "https://images.unsplash.com/photo-1608507940435-c4a37d0d5411?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 30, category: "Postres", name: "Flan", price: 3500, description: "Con crema o mixto (Dulce de Leche y Crema).", image: "https://images.unsplash.com/photo-1599999518758-3f7d0e8c6a3a?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 31, category: "Postres", name: "Torta Helada", price: 4500, description: "Crema Americana con Dulce de Leche.", image: "https://images.unsplash.com/photo-1578985545060-699c680dd0f8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 32, category: "Postres", name: "Panqueque", price: 4500, description: "Dulce de Leche, Chocolate y canela.", image: "https://images.unsplash.com/photo-1562706329-5864714d5e84?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 0 },
    { id: 33, category: "Al Plato", name: "Milanesa con Puré", price: 9500, description: "Milanesa acompañada de puré de papas.", image: "https://images.unsplash.com/photo-1613844237701-8c0e7b9e4b7e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 10 },
    { id: 34, category: "Al Plato", name: "Milanesa a Caballo", price: 10000, description: "Milanesa con dos huevos fritos encima.", image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 10 },
    { id: 35, category: "Al Plato", name: "Milanesa Napolitana", price: 10500, description: "Milanesa con salsa de tomate, jamón y queso.", image: "https://images.unsplash.com/photo-1600891964599-f61ba0e24092?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80", stock: 10 }
  ];

  const defaultOffers = [
    { id: 1, day: "Lunes", description: "Pastas 10% off los Lunes", discount: 10 },
    { id: 2, day: "Martes", description: "Hamburguesa Zapping 10% off los Martes", discount: 10 },
    { id: 3, day: "Miércoles", description: "Sándwich de Bondiola 10% off los Miércoles", discount: 10 }
  ];

  let cart = [];
  let products = JSON.parse(localStorage.getItem("products")) || defaultProducts;
  let offers = JSON.parse(localStorage.getItem("offers")) || defaultOffers;
  let editingProductId = null;
  let userName = null;

  function saveData() {
    localStorage.setItem("products", JSON.stringify(products));
    localStorage.setItem("offers", JSON.stringify(offers));
  }

  function checkAdminPassword() {
    const pass = document.getElementById("adminPassword").value;
    const hashed = CryptoJS.SHA256(pass).toString();
    const correctHash = CryptoJS.SHA256("0608").toString();
    if (hashed === correctHash) {
      document.getElementById("adminModal").style.display = "none";
      openAdmin();
    } else {
      alert("Clave incorrecta. Intente nuevamente.");
    }
    document.getElementById("adminPassword").value = "";
  }

  function renderCategories() {
    const container = document.getElementById("categoriesContainer");
    container.innerHTML = "";

    const categories = [...new Set(products.map(p => p.category))];

    categories.forEach(category => {
      const div = document.createElement("div");
      div.className = "category";
      div.innerHTML = `
        <div class="category-header">
          <h3>${category}</h3>
          <span class="category-arrow">▶</span>
        </div>
        <div class="products"></div>
      `;
     
      const header = div.querySelector(".category-header");
      const content = div.querySelector(".products");
      const arrow = div.querySelector(".category-arrow");

      header.addEventListener("click", () => {
        const isOpen = content.style.display === "block";
        document.querySelectorAll(".products").forEach(p => {
          p.style.display = "none";
          p.previousElementSibling.classList.remove("active");
        });
        if (!isOpen) {
          content.style.display = "block";
          header.classList.add("active");
        }
      });

      const filteredProducts = products.filter(p => p.category === category);
     
      filteredProducts.forEach(product => {
        const productDiv = document.createElement("div");
        productDiv.className = "product";
        productDiv.innerHTML = `
          <div class="product-info">
            <div class="product-name">${product.name}</div>
            <div Jaeger-LeCoultreclass="product-description">${product.description}</div>
          </div>
          <div class="product-price">$${product.price.toLocaleString('es-AR')}</div>
          <div class="product-stock">Stock: ${product.stock}</div>
          ${product.image ? `<img src="${product.image}" alt="${product.name}" class="product-image" loading="lazy">` : ""}
          <button class="add-to-cart" data-id="${product.id}" data-name="${product.name}" data-price="${product.price}">Añadir al Carrito</button>
        `;
        content.appendChild(productDiv);
      });

      container.appendChild(div);
    });

    const firstCategory = container.querySelector(".category");
    if (firstCategory) {
      firstCategory.querySelector(".products").style.display = "block";
      firstCategory.querySelector(".category-header").classList.add("active");
    }

    document.querySelectorAll(".add-to-cart").forEach(button => {
      button.addEventListener("click", () => {
        const id = button.getAttribute("data-id");
        const name = button.getAttribute("data-name");
        const price = parseInt(button.getAttribute("data-price"));
        addToCart(id, name, price);
      });
    });

    const today = new Date().toLocaleString('es-AR', { weekday: 'long' });
    const todayOffer = offers.find(offer => offer.day === today);
    document.getElementById('offerText').textContent = todayOffer ? todayOffer.description : '¡Consulta nuestras ofertas semanales!';
  }

  function addToCart(id, name, price) {
    const product = products.find(p => p.id === parseInt(id));
    if (product.stock <= 0) {
      alert("Lo siento, este producto está agotado.");
      return;
    }
    const existingItem = cart.find(item => item.id === id);
    if (existingItem) {
      if (product.stock < existingItem.quantity + 1) {
        alert("Lo siento, no hay suficiente stock para agregar más unidades de este producto.");
        return;
      }
      existingItem.quantity += 1;
    } else {
      if (product.stock < 1) {
        alert("Lo siento, este producto está agotado.");
        return;
      }
      cart.push({ id, name, price, quantity: 1 });
    }
    updateCartDisplay();
    document.getElementById("cartModal").style.display = "flex";
  }

  function updateCartDisplay() {
    const cartItems = document.getElementById("cartItems");
    const cartTotal = document.getElementById("cartTotal");
    const cartCount = document.getElementById("cartCount");
   
    cartItems.innerHTML = "";
    let total = 0;

    cart.forEach(item => {
      const itemTotal = item.price * item.quantity;
      total += itemTotal;
      const div = document.createElement("div");
      div.className = "cart-item";
      div.innerHTML = `
        <span>${item.quantity} x ${item.name}</span>
        <span>$${itemTotal.toLocaleString('es-AR')}</span>
        <button onclick="removeFromCart('${item.id}')">Eliminar</button>
      `;
      cartItems.appendChild(div);
    });

    cartTotal.textContent = `Total: $${total.toLocaleString('es-AR')}`;
    cartCount.textContent = cart.reduce((sum, item) => sum + item.quantity, 0);
  }

  function removeFromCart(id) {
    const itemIndex = cart.findIndex(item => item.id === id);
    if (itemIndex !== -1) {
      if (cart[itemIndex].quantity > 1) {
        cart[itemIndex].quantity -= 1;
      } else {
        cart.splice(itemIndex, 1);
      }
      updateCartDisplay();
    }
  }

  function generatePDF() {
    const { jsPDF } = window.jspdf;
    const doc = new jsPDF();
   
    doc.setFontSize(18);
    doc.text("Orden Todo Casero", 20, 20);
    doc.setFontSize(12);
    doc.text(`Fecha: ${new Date().toLocaleString('es-AR')}`, 20, 30);
    doc.text(`Cliente: ${document.getElementById("customerName").value.trim()}`, 20, 40);
    doc.text(`Celular: ${document.getElementById("customerPhone").value.trim()}`, 20, 50);
    doc.text("Dirección: Campana, Buenos Aires", 20, 60);
    doc.text("Teléfono: +543489358998", 20, 70);
   
    let y = 90;
    doc.text("Producto | Cantidad | Precio Unitario | Total", 20, y);
    y += 10;
   
    let total = 0;
    cart.forEach(item => {
      const itemTotal = item.price * item.quantity;
      total += itemTotal;
      doc.text(`${item.name} | ${item.quantity} | $${item.price} | $${itemTotal}`, 20, y);
      y += 10;
    });
   
    doc.text(`Total: $${total.toLocaleString('es-AR')}`, 20, y + 10);
   
    const payment = document.querySelector('input[name="payment"]:checked').value;
    y += 20;
    doc.text(`Método de Pago: ${payment}`, 20, y);
    if (payment === "Transferencia") {
      doc.text("Alias: Adri.roti", 20, y + 10);
      doc.text("Titular: Adriana Basilia Enrique", 20, y + 20);
    }
   
    doc.save(`order_${new Date().toISOString().replace(/[:.]/g, '')}.pdf`);
  }

  function generateWhatsAppMessage(customerName, customerPhone, lowStockProducts) {
    let message = `🍔 *Pedido de Todo Casero* 🍔\n\n`;
    message += `👤 *Cliente*: ${customerName}\n`;
    message += `📞 *Celular*: ${customerPhone}\n\n`;
    cart.forEach(item => {
      message += `• ${item.quantity} x ${item.name} - $${(item.price * item.quantity).toLocaleString('es-AR')} 💸\n`;
    });
    const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
    message += `\n💰 *Total*: $${total.toLocaleString('es-AR')} 🤑\n`;
    const payment = document.querySelector('input[name="payment"]:checked').value;
    message += `💳 *Pago*: ${payment} ${payment === 'Transferencia' ? '🏦' : '💵'}`;
    if (payment === "Transferencia") {
      message += `\nAlias: Adri.roti\nTitular: Adriana Basilia Enrique`;
    }
    if (lowStockProducts.length > 0) {
      message += `\n\n🔒 *Para la rotisería*: Usar código !0608 para ver alertas de stock bajo`;
    }
    return encodeURIComponent(message);
  }

  function generateStockMessage(lowStockProducts) {
    let message = `🔒 *Alerta de Stock Bajo* 🔒\n\n`;
    message += `Código: !0608\n`;
    message += `¡Atención! El stock de los siguientes productos ha llegado a 2 unidades:\n`;
    lowStockProducts.forEach(product => {
      message += `- ${product}: Quedan solo 2 unidades.\n`;
    });
    return encodeURIComponent(message);
  }

  function toggleChat() {
    const chatWidget = document.getElementById("chatWidget");
    chatWidget.style.display = chatWidget.style.display === "block" ? "none" : "block";
    if (chatWidget.style.display === "block" && !document.getElementById("chatBody").innerHTML) {
      const chatBody = document.getElementById("chatBody");
      const welcomeMessage = document.createElement("div");
      welcomeMessage.className = "chat-message bot";
      welcomeMessage.textContent = "¡Hola y buenas noches! Soy María, tu asistente en Todo Casero, donde comer bien es como en casa. 😊 ¿En qué puedo ayudarte hoy?";
      chatBody.appendChild(welcomeMessage);
    }
  }

  function sendChatMessage() {
    const input = document.getElementById("chatInput");
    const message = input.value.trim();
    if (!message) return;

    const chatBody = document.getElementById("chatBody");
    const userMessage = document.createElement("div");
    userMessage.className = "chat-message user";
    userMessage.textContent = message;
    chatBody.appendChild(userMessage);

    const lowerMessage = message.toLowerCase();

    const nameMatch = message.match(/mi nombre es (\w+)/i);
    if (nameMatch) {
      userName = nameMatch[1].charAt(0).toUpperCase() + nameMatch[1].slice(1);
    }

    const greeting = userName ? `¡Hola ${userName}!` : "¡Hola!";
    const closing = "¿Quieres agregar algo más? 😊";
    const paymentInfo = "Aceptamos efectivo al retirar 💵 o transferencia bancaria 🏦 (Alias: Adri.roti, Titular: Adriana Basilia Enrique).";

    let response = `${greeting} Gracias por elegir Todo Casero. `;

    if (lowerMessage.includes("generar pdf") || lowerMessage.includes("resumen pdf")) {
      if (cart.length > 0) {
        generatePDF();
        response += "¡Listo! He generado el resumen de tu pedido en PDF. 📄 ¿Quieres confirmar el pedido por WhatsApp o agregar algo más?";
      } else {
        response += "Tu carrito está vacío. 😔 Por favor agrega productos antes de generar un resumen.";
      }
    } else if (lowerMessage.includes("cancelar pedido")) {
      if (cart.length > 0) {
        cart = [];
        updateCartDisplay();
        response += "¡Pedido cancelado! 😊 ¿Quieres empezar un nuevo pedido?";
      } else {
        response += "No hay pedido para cancelar. 😔 ¿Quieres hacer un nuevo pedido?";
      }
    } else {
      const orderRegex = /(\d+)\s*(?:x\s*)?([^\d\s][^,]*?)(?=\s*(?:y|,|$))/gi;
      const orderMatches = [...message.matchAll(orderRegex)];
      if (orderMatches.length > 0) {
        let total = 0;
        let orderDetails = [];
        let unmatchedItems = [];
        let today = new Date().toLocaleString('es-AR', { weekday: 'long' });
        let todayOffer = offers.find(offer => offer.day === today);

        for (const match of orderMatches) {
          const quantity = parseInt(match[1]);
          const productName = match[2].trim();
          const product = products.find(p => p.name.toLowerCase() === productName.toLowerCase() || p.name.toLowerCase().includes(productName.toLowerCase()));

          if (product && product.price) {
            let price = product.price;
            let discountApplied = false;

            if (todayOffer && todayOffer.description.toLowerCase().includes(product.name.toLowerCase())) {
              const discount = todayOffer.discount / 100;
              price = Math.round(price * (1 - discount));
              discountApplied = true;
            }

            const itemTotal = price * quantity;
            total += itemTotal;
            orderDetails.push({
              name: product.name,
              quantity,
              price,
              itemTotal,
              discountApplied
            });
          } else {
            unmatchedItems.push(productName);
          }
        }

        if (orderDetails.length > 0) {
          response += "¡Perfecto! Aquí está el detalle de tu pedido:\n";
          orderDetails.forEach(item => {
            response += `• ${item.quantity} x ${item.name} - $${item.itemTotal.toLocaleString('es-AR')}`;
            if (item.discountApplied) {
              response += ` (con ${todayOffer.discount}% de descuento)`;
            }
            response += '\n';
          });
          response += `\n💰 *Total*: $${total.toLocaleString('es-AR')}\n`;
          response += `${paymentInfo} ¿Quieres confirmar este pedido por WhatsApp o agregar algo más?`;

          if (unmatchedItems.length > 0) {
            response += `\n⚠️ No pude encontrar: ${unmatchedItems.join(', ')}. Por favor verifica los nombres en el menú (ejemplo: 'Sándwich de Bondiola', 'Muzzarella').`;
          }

          orderDetails.forEach(item => {
            const existingItem = cart.find(cartItem => cartItem.id === products.find(p => p.name === item.name).id);
            if (existingItem) {
              existingItem.quantity += item.quantity;
            } else {
              cart.push({
                id: products.find(p => p.name === item.name).id,
                name: item.name,
                price: item.price,
                quantity: item.quantity
              });
            }
          });
          updateCartDisplay();
        } else {
          response += "No pude identificar los productos en tu pedido. 😔 Por favor escribe los nombres como aparecen en el menú de Todo Casero (ejemplo, 'Sándwich de Bondiola', 'Muzzarella'). ¿Puedes intentarlo de nuevo?";
        }
      } else if (lowerMessage.includes("hola") || lowerMessage.includes("buenas")) {
        response += "¡Bienvenido a Todo Casero, una rotisería con corazón casero! 🍔 ¿Cómo puedo ayudarte hoy?";
      } else if (lowerMessage.includes("horario") || lowerMessage.includes("hora")) {
        response += "Estamos abiertos de lunes a domingo de 19:30 a 23:45. 🕗 ¿Quieres hacer un pedido ahora?";
      } else if (lowerMessage.includes("ubicación") || lowerMessage.includes("campana")) {
        response += "Estamos en Campana, Buenos Aires. 📍 ¿Puedo ayudarte a armar tu pedido?";
      } else if (lowerMessage.includes("menú") || lowerMessage.includes("carta")) {
        response += "Nuestro menú incluye sándwiches, pizzas, pastas, hamburguesas, lomitos, bondiolas y acompañamientos como fritas. 😋 Puedes ver la sección 'Menú' o preguntarme por algo específico.";
      } else if (lowerMessage.includes("precio") || lowerMessage.includes("cuánto cuesta")) {
        const productName = lowerMessage.replace(/precio de|cuánto cuesta|el precio de/gi, "").trim();
        const product = products.find(p => p.name.toLowerCase().includes(productName));
        if (product) {
          response += `El precio de ${product.name} es $${product.price.toLocaleString('es-AR')}. ${product.description} ¿Quieres agregarlo al carrito?`;
        } else {
          response += "No encontré ese producto. 😔 ¿Puedes darme más detalles o revisar nuestro menú en la sección 'Menú'?";
        }
      } else if (lowerMessage.includes("sándwich") || lowerMessage.includes("sandwiches")) {
        const sandwiches = products.filter(p => p.category === "Sándwiches");
        response += "Tenemos sándwiches deliciosos como Bondiola ($9,000), Milanesa ($9,500), Lomito ($10,000), y Zapping Burger ($25,000). ¿Cuál te tienta?";
      } else if (lowerMessage.includes("pizza")) {
        const pizzas = products.filter(p => p.category === "Pizzas" || p.category === "Pizzas Individuales");
        response += "Ofrecemos pizzas clásicas como Muzzarella ($10,000) y pizzas individuales como Muzzarella Individual ($5,500). 🍕 ¿Cuál prefieres?";
      } else if (lowerMessage.includes("pasta")) {
        const pastas = products.filter(p => p.category === "Pastas");
        response += "Nuestras pastas caseras incluyen Tallarines con Bolognesa ($8,500). 🍝 ¿Te interesa?";
      } else if (lowerMessage.includes("hamburguesa")) {
        const burgers = products.filter(p => p.category === "Hamburguesas");
        response += "Tenemos hamburguesas como la Completa ($8,500). 🍔 ¿Quieres probarla?";
      } else if (lowerMessage.includes("acompañamiento") || lowerMessage.includes("fritas")) {
        const sides = products.filter(p => p.category === "Acompañamientos");
        response += "Ofrecemos acompañamientos como Porción de Fritas ($4,500) o Cono de Fritas ($3,500). 🍟 ¿Quieres agregar alguno?";
      } else if (lowerMessage.includes("oferta") || lowerMessage.includes("promoción")) {
        const today = new Date().toLocaleString('es-AR', { weekday: 'long' });
        const todayOffer = offers.find(offer => offer.day === today);
        if (todayOffer) {
          response += `¡Hoy ${today} tenemos una oferta especial! ${todayOffer.description}. ¿Quieres aprovecharla?`;
        } else {
          response += "No tenemos ofertas para hoy, pero puedes consultar nuestras promociones semanales en el menú. 😊 ¿En qué más puedo ayudarte?";
        }
      } else if (lowerMessage.includes("pago") || lowerMessage.includes("método de pago")) {
        response += `${paymentInfo} ¿Cómo prefieres pagar?`;
      } else if (lowerMessage.includes("pedido") || lowerMessage.includes("cómo pedir")) {
        response += "Puedes elegir tus platos desde el menú, agregarlos al carrito y enviar el pedido por WhatsApp desde nuestro sitio. También puedes decirme qué quieres pedir y te ayudo a armarlo. 😊 ¿Quieres empezar un pedido?";
      } else {
        response += "Entiendo, pero no estoy segura de qué necesitas. 😔 ¿Puedes darme más detalles o preguntarme sobre el menú, horarios o algo específico? También puedes contactarnos por WhatsApp al +54 348 9358998.";
      }
    }

    response += ` ${closing}`;

    const botMessage = document.createElement("div");
    botMessage.className = "chat-message bot";
    botMessage.textContent = response;
    chatBody.appendChild(botMessage);

    input.value = "";
    chatBody.scrollTop = chatBody.scrollHeight;
  }

  function openAdmin() {
    document.getElementById("adminPanel").style.display = "block";
    renderProductList();
  }

  function closeAdmin() {
    document.getElementById("adminPanel").style.display = "none";
    document.getElementById("productForm").reset();
    document.getElementById("previewImage").style.display = "none";
    document.getElementById("productImageUrl").value = "";
    editingProductId = null;
  }

  function renderProductList() {
    const productList = document.getElementById("productList");
    productList.innerHTML = "";
    products.forEach(product => {
      const div = document.createElement("div");
      div.className = "product-item";
      div.innerHTML = `
        <span>${product.name} - $${product.price} - Stock: ${product.stock}</span>
        <div>
          <button class="btn" onclick="editProduct(${product.id})">Editar</button>
          <button class="btn" style="background-color: #e74c3c;" onclick="deleteProduct(${product.id})">Eliminar</button>
        </div>
      `;
      productList.appendChild(div);
    });
  }

  function editProduct(id) {
    editingProductId = id;
    const product = products.find(p => p.id === id);
    document.getElementById("categorySelect").value = product.category;
    document.getElementById("productName").value = product.name;
    document.getElementById("productPrice").value = product.price;
    document.getElementById("productStock").value = product.stock;
    document.getElementById("productDescription").value = product.description;
    document.getElementById("productImageUrl").value = product.image || "";
    if (product.image) {
      document.getElementById("previewImage").src = product.image;
      document.getElementById("previewImage").style.display = "block";
    }
  }

  function deleteProduct(id) {
    if (confirm("¿Confirmar eliminación?")) {
      products = products.filter(p => p.id !== id);
      saveData();
      renderProductList();
      renderCategories();
    }
  }

  document.getElementById("viewCart").addEventListener("click", (e) => {
    e.preventDefault();
    document.getElementById("cartModal").style.display = "flex";
    updateCartDisplay();
  });

  function closeCart() {
    document.getElementById("cartModal").style.display = "none";
  }

  document.getElementById("cartTransferencia").addEventListener("change", function() {
    document.getElementById("cartTransferenciaInfo").style.display = this.checked ? "block" : "none";
  });

  document.getElementById("sendOrder").addEventListener("click", () => {
    const customerName = document.getElementById("customerName").value.trim();
    const customerPhone = document.getElementById("customerPhone").value.trim();

    if (cart.length === 0) {
      alert("El carrito está vacío. Por favor agrega productos antes de enviar el pedido.");
      return;
    }

    if (!customerName || !customerPhone) {
      alert("Por favor completa tus datos (nombre y celular).");
      return;
    }

    let lowStockProducts = [];
    cart.forEach(item => {
      const product = products.find(p => p.id === parseInt(item.id));
      product.stock -= item.quantity;
      if (product.stock === 2) {
        lowStockProducts.push(product.name);
      }
    });

    const phoneNumber = "+543489358998";
    const whatsappMessage = generateWhatsAppMessage(customerName, customerPhone, lowStockProducts);
    const whatsappUrl = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${whatsappMessage}`;
    window.open(whatsappUrl, '_blank');

    if (lowStockProducts.length > 0) {
      const stockMessage = generateStockMessage(lowStockProducts);
      const stockUrl = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${stockMessage}`;
      setTimeout(() => window.open(stockUrl, '_blank'), 500);
    }

    generatePDF();
    cart = [];
    updateCartDisplay();
    renderCategories();
    saveData();
    closeCart();
  });

  document.getElementById("adminLink").addEventListener("click", function(e) {
    e.preventDefault();
    document.getElementById("adminModal").style.display = "flex";
  });

  document.getElementById("productImage").addEventListener("change", function(e) {
    const file = e.target.files[0];
    if (file) {
      const reader = new FileReader();
      reader.onload = function(ev) {
        const preview = document.getElementById("previewImage");
        preview.src = ev.target.result;
        preview.style.display = "block";
        document.getElementById("productImageUrl").value = ""; // Clear URL input
      };
      reader.readAsDataURL(file);
    }
  });

  document.getElementById("productImageUrl").addEventListener("input", function(e) {
    const url = e.target.value.trim();
    if (url) {
      const preview = document.getElementById("previewImage");
      preview.src = url;
      preview.style.display = "block";
      document.getElementById("productImage").value = ""; // Clear file input
    }
  });

  document.getElementById("productForm").addEventListener("submit", function(e) {
    e.preventDefault();

    const name = document.getElementById("productName").value.trim();
    const price = parseInt(document.getElementById("productPrice").value);
    const stock = parseInt(document.getElementById("productStock").value);
    const description = document.getElementById("productDescription").value.trim();
    const category = document.getElementById("categorySelect").value;
    const imageInput = document.getElementById("productImage");
    const imageUrl = document.getElementById("productImageUrl").value.trim();
    const image = imageUrl || (imageInput.files.length > 0 ? URL.createObjectURL(imageInput.files[0]) : "");

    if (!name || isNaN(price) || isNaN(stock)) {
      alert("Por favor completa todos los campos requeridos.");
      return;
    }

    if (editingProductId) {
      products = products.map(p => p.id === editingProductId ? { ...p, category, name, price, stock, description, image } : p);
    } else {
      const id = products.length ? Math.max(...products.map(p => p.id)) + 1 : 1;
      products.push({ id, category, name, price, stock, description, image });
    }

    renderProductList();
    renderCategories();
    this.reset();
    document.getElementById("previewImage").style.display = "none";
    document.getElementById("productImageUrl").value = "";
    editingProductId = null;
    saveData();
  });

  document.getElementById("saveChanges").addEventListener("click", function() {
    saveData();
    alert("¡Cambios guardados exitosamente!");
  });

  document.addEventListener("DOMContentLoaded", function() {
    renderCategories();

    document.getElementById("cartModal").addEventListener("click", function(e) {
      if (e.target === this) {
        closeCart();
      }
    });

    document.getElementById("adminModal").addEventListener("click", function(e) {
      if (e.target === this) {
        this.style.display = "none";
      }
    });
  });
</script>

</body>
</html>
