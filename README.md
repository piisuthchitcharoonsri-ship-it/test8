<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ร้านขายของ</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fdf6f0;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 { color: #ff6f91; }
    .product {
      background: #fff;
      border: 2px solid #ffb6b9;
      border-radius: 12px;
      padding: 15px;
      margin: 15px auto;
      max-width: 300px;
    }
    button {
      background-color: #ff6f91;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
    }
    button:hover { background-color: #ff4e78; }
    .cart-link {
      display: inline-block;
      margin-top: 20px;
      background: #6a5acd;
      padding: 10px 15px;
      border-radius: 8px;
      color: white;
      text-decoration: none;
    }
  </style>
  <script>
    function addToCart(product) {
      let cart = JSON.parse(localStorage.getItem("cart")) || [];
      cart.push(product);
      localStorage.setItem("cart", JSON.stringify(cart));
      alert(product + " ถูกเพิ่มเข้าตะกร้าแล้ว!");
    }
  </script>
</head>
<body>
  <h1>ร้านขายของ</h1>

  <div class="product">
    <h2>สินค้า A</h2>
    <p>ราคา 100 บาท</p>
    <button onclick="addToCart('สินค้า A')">หยิบใส่ตะกร้า</button>
  </div>

  <div class="product">
    <h2>สินค้า B</h2>
    <p>ราคา 200 บาท</p>
    <button onclick="addToCart('สินค้า B')">หยิบใส่ตะกร้า</button>
  </div>

  <a href="cart.html" class="cart-link">ไปที่ตะกร้า</a>
</body>
</html>
