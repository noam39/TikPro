<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TikPro - קידום בטיקטוק</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f5f6fa;
      margin: 0;
      padding: 0;
      direction: rtl;
      color: #333;
    }
    header {
      background-color: #2f3640;
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 24px;
      font-weight: bold;
      letter-spacing: 1.5px;
    }
    main {
      display: flex;
      flex-wrap: wrap;
      max-width: 1200px;
      margin: 30px auto;
      gap: 30px;
      padding: 0 15px;
    }
    .products {
      flex: 3;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }
    .product-card {
      background: white;
      border-radius: 12px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
      padding: 20px;
      text-align: center;
      transition: box-shadow 0.3s ease;
    }
    .product-card:hover {
      box-shadow: 0 6px 15px rgba(0,0,0,0.15);
    }
    .product-card h3 {
      margin-top: 0;
      font-size: 20px;
      color: #2f3640;
    }
    .product-card p {
      font-size: 18px;
      margin: 10px 0 15px 0;
      color: #44bd32;
      font-weight: 600;
    }
    .product-card button {
      background-color: #44bd32;
      border: none;
      padding: 12px 20px;
      color: white;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .product-card button:hover {
      background-color: #2e8b1a;
    }
    .cart {
      flex: 1;
      background: white;
      border-radius: 12px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
      padding: 20px;
      max-height: 650px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .cart h2 {
      margin-top: 0;
      font-size: 22px;
      border-bottom: 2px solid #44bd32;
      padding-bottom: 10px;
      color: #2f3640;
    }
    .cart-items {
      flex-grow: 1;
      overflow-y: auto;
      margin-top: 15px;
      margin-bottom: 15px;
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
      padding-bottom: 8px;
      border-bottom: 1px solid #ddd;
    }
    .cart-item-name {
      font-weight: 600;
      color: #2f3640;
    }
    .cart-item-price {
      color: #44bd32;
      font-weight: 600;
    }
    .remove-btn {
      background: none;
      border: none;
      color: #e84118;
      font-weight: bold;
      cursor: pointer;
      font-size: 18px;
      padding: 0 5px;
    }
    .input-group {
      margin: 15px 0;
      display: flex;
      flex-direction: column;
    }
    label {
      margin-bottom: 6px;
      font-weight: 600;
      color: #2f3640;
    }
    input[type="text"], input[type="tel"] {
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 16px;
      outline: none;
      transition: border-color 0.3s ease;
    }
    input[type="text"]:focus, input[type="tel"]:focus {
      border-color: #44bd32;
    }
    .total {
      font-size: 20px;
      font-weight: 700;
      color: #2f3640;
      text-align: right;
      margin-bottom: 15px;
    }
    .order-btn {
      background-color: #273c75;
      color: white;
      padding: 14px 0;
      border: none;
      font-size: 18px;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      width: 100%;
    }
    .order-btn:disabled {
      background-color: #999;
      cursor: not-allowed;
    }
    .order-btn:hover:not(:disabled) {
      background-color: #192a56;
    }
    footer {
      text-align: center;
      padding: 15px 0;
      margin-top: 40px;
      background: #2f3640;
      color: white;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <header>
    TikPro - קידום בטיקטוק
  </header>

  <main>
    <section class="products">
      <div class="product-card" data-name="10 עוקבים" data-price="2.90">
        <h3>10 עוקבים</h3>
        <p>₪2.90</p>
        <button>הוסף לסל</button>
      </div>
      <div class="product-card" data-name="500 עוקבים" data-price="20">
        <h3>500 עוקבים</h3>
        <p>₪20</p>
        <button>הוסף לסל</button>
      </div>
      <div class="product-card" data-name="1000 עוקבים" data-price="80">
        <h3>1000 עוקבים</h3>
        <p>₪80</p>
        <button>הוסף לסל</button>
      </div>
    </section>

    <aside class="cart">
      <h2>סל קניות</h2>

      <div class="cart-items">
        <p>הסל שלך ריק</p>
      </div>

      <div class="input-group">
        <label for="name">שם מלא:</label>
        <input type="text" id="name" placeholder="הקלד את שמך המלא" />
      </div>

      <div class="input-group">
        <label for="phone">מספר טלפון:</label>
        <input type="tel" id="phone" placeholder="הקלד את מספר הטלפון" />
      </div>

      <div class="total">סה"כ: ₪0.00</div>
      <button class="order-btn" disabled>הזמן עכשיו</button>
    </aside>
  </main>

  <footer>
    © 2025 TikPro. כל הזכויות שמורות.
  </footer>

  <script>
    const products = document.querySelectorAll('.product-card button');
    const cartItemsContainer = document.querySelector('.cart-items');
    const totalDisplay = document.querySelector('.total');
    const orderBtn = document.querySelector('.order-btn');
    const nameInput = document.getElementById('name');
    const phoneInput = document.getElementById('phone');

    let cart = [];

    function updateCartUI() {
      cartItemsContainer.innerHTML = '';
      if (cart.length === 0) {
        cartItemsContainer.innerHTML = '<p>הסל שלך ריק</p>';
        totalDisplay.textContent = 'סה"כ: ₪0.00';
        orderBtn.disabled = true;
        return;
      }

      let total = 0;
      cart.forEach((item, index) => {
        total += item.price;

        const itemDiv = document.createElement('div');
        itemDiv.classList.add('cart-item');

        const nameSpan = document.createElement('span');
        nameSpan.classList.add('cart-item-name');
        nameSpan.textContent = item.name;

        const priceSpan = document.createElement('span');
        priceSpan.classList.add('cart-item-price');
        priceSpan.textContent = '₪' + item.price.toFixed(2);

        const removeBtn = document.createElement('button');
        removeBtn.classList.add('remove-btn');
        removeBtn.textContent = '×';
        removeBtn.onclick = () => {
          cart.splice(index, 1);
          updateCartUI();
        };

        itemDiv.appendChild(nameSpan);
        itemDiv.appendChild(priceSpan);
        itemDiv.appendChild(removeBtn);

        cartItemsContainer.appendChild(itemDiv);
      });

      totalDisplay.textContent = 'סה"כ: ₪' + total.toFixed(2);
      checkOrderBtnState();
    }

    function checkOrderBtnState() {
      if (cart.length > 0 && nameInput.value.trim() !== '' && phoneInput.value.trim() !== '') {
        orderBtn.disabled = false;
      } else {
        orderBtn.disabled = true;
      }
    }

    products.forEach(button => {
      button.addEventListener('click', () => {
        const productCard = button.parentElement;
        const name = productCard.getAttribute('data-name');
        const price = parseFloat(productCard.getAttribute('data-price'));
        cart.push({ name, price });
        updateCartUI();
      });
    });

    nameInput.addEventListener('input', checkOrderBtnState);
    phoneInput.addEventListener('input', checkOrderBtnState);

    orderBtn.addEventListener('click', () => {
      if (cart.length === 0) return;
      if (nameInput.value.trim() === '' || phoneInput.value.trim() === '') {
        alert('אנא מלא שם מלא ומספר טלפון כדי להמשיך');
        return;
      }

      let orderDetails = 'הזמנה חדשה:\n';
      cart.forEach(item => {
        orderDetails += `${item.name} - ₪${item.price.toFixed(2)}\n`;
      });
      orderDetails += totalDisplay.textContent + '\n\n';
      orderDetails += `שם מלא: ${nameInput.value}\n`;
      orderDetails += `מספר טלפון: ${phoneInput.value}\n\n`;
      orderDetails += 'מזומן בלבד. לפרטים והמשך תשלום דברו איתנו בפרטי.\n';
      orderDetails += 'עמוד טיקטוק: @big.brother_.2025';

      alert(orderDetails);
    });
  </script>
</body>
</html># TikPro
