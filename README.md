<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>EarnHub PH - Shopee Deals</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  min-height: 100vh;
  background: linear-gradient(135deg, #ff512f, #dd2476);
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #fff;
}

header {
  padding: 30px 15px;
  font-size: 28px;
  font-weight: 700;
  text-align: center;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
}

.container {
  width: 100%;
  max-width: 420px;
  padding: 15px;
}

/* Voucher Cards */
.card {
  background: linear-gradient(145deg, #ffffff, #f9f9f9);
  color: #333;
  border-radius: 20px;
  padding: 25px;
  margin-bottom: 25px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.25);
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.3);
}

.card h2 {
  margin-bottom: 12px;
  font-size: 22px;
  color: #ff512f;
}

.card p {
  margin: 10px 0;
  font-size: 15px;
}

.coins {
  font-size: 18px;
  font-weight: 600;
  color: #ff9800;
}

/* Buttons */
.btn {
  display: inline-block;
  margin-top: 15px;
  padding: 14px 28px;
  background: #ee4d2d;
  color: white;
  text-decoration: none;
  border-radius: 12px;
  font-weight: 600;
  transition: 0.3s;
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.btn:hover {
  background: #c7371b;
  transform: scale(1.05);
}

/* Admin Panel */
#adminPanel {
  background: rgba(255,255,255,0.95);
  padding: 20px;
  border-radius: 15px;
  margin-bottom: 25px;
  color: #333;
}

#adminPanel h3 {
  margin-bottom: 15px;
  text-align: center;
  color: #ff512f;
}

#adminPanel input, #adminPanel button {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 15px;
}

#adminPanel button {
  background: #ee4d2d;
  color: #fff;
  border: none;
  font-weight: 600;
  cursor: pointer;
  transition: 0.3s;
}

#adminPanel button:hover {
  background: #c7371b;
}

/* Footer */
footer {
  margin-top: auto;
  padding: 20px;
  font-size: 13px;
  opacity: 0.9;
  text-align: center;
}
</style>
</head>

<body>

<header>
🔥 EarnHub PH 🔥
</header>

<div class="container">

  <!-- Existing Vouchers -->
  <div class="card">
    <h2>50% OFF Flash Sale</h2>
    <p>Limited time Shopee promo!</p>
    <p class="coins">+100 Bonus Coins</p>
    <a href="ILAGAY_MO_DITO_AFFILIATE_LINK_MO" target="_blank" class="btn">
      Shop Now
    </a>
  </div>

  <div class="card">
    <h2>Free Shipping Deals</h2>
    <p>Grab today before stocks run out!</p>
    <p class="coins">+50 Bonus Coins</p>
    <a href="ILAGAY_MO_DITO_AFFILIATE_LINK_MO" target="_blank" class="btn">
      View Deals
    </a>
  </div>

  <!-- Admin Panel -->
  <div id="adminPanel">
    <h3>Add New Promo Code</h3>
    <form id="adminForm">
      <input type="text" id="voucherTitle" placeholder="Promo Title" required>
      <input type="text" id="voucherDesc" placeholder="Description" required>
      <input type="number" id="voucherCoins" placeholder="Bonus Coins" required>
      <input type="text" id="voucherLink" placeholder="Affiliate Link" required>
      <button type="submit">Add Promo</button>
    </form>
  </div>

</div>

<footer>
© 2026 EarnHub PH | Shopee Affiliate Promo
</footer>

<script>
const container = document.querySelector('.container');
const adminForm = document.getElementById('adminForm');

adminForm.addEventListener('submit', function(e) {
  e.preventDefault();

  const title = document.getElementById('voucherTitle').value;
  const desc = document.getElementById('voucherDesc').value;
  const coins = document.getElementById('voucherCoins').value;
  const link = document.getElementById('voucherLink').value;

  // Create new voucher card
  const card = document.createElement('div');
  card.className = 'card';
  card.innerHTML = `
    <h2>${title}</h2>
    <p>${desc}</p>
    <p class="coins">+${coins} Bonus Coins</p>
    <a href="${link}" target="_blank" class="btn">Get Promo</a>
  `;

  // Insert new card above admin panel
  const adminPanel = document.getElementById('adminPanel');
  container.insertBefore(card, adminPanel);

  // Reset form
  adminForm.reset();
});
</script>

</body>
</html>
