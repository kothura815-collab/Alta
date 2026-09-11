    <div class="modal-content">
      <h3 style="margin-top:0; color:#f59e0b;">Payout Request</h3>
      <label style="font-size: 12px; color: #94a3b8;">Telegram Username</label>
      <input type="text" id="username" placeholder="Telegram Username">
      
      <label style="font-size: 12px; color: #94a3b8;">Amount (PTF)</label>
      <input type="number" id="amount" placeholder="Amount (PTF)">
      
      <label style="font-size: 12px; color: #94a3b8;">TON Wallet Address</label>
      <input type="text" id="wallet" placeholder="TON Wallet Address">
      
      <button class="btn" onclick="submitWithdrawal()" style="background:#22c55e; margin-top:15px;">SUBMIT REQUEST</button>
      <p style="text-align: center; cursor: pointer; color: #94a3b8; margin-top: 15px; font-size: 14px;" onclick="closeModal()">Cancel</p>
    </div>
  </div>

  <script>
    let points = 3.10;
    const tg = window.Telegram.WebApp;
    tg.expand();

    function minePoint() {
      points += 0.10;
      document.getElementById('balance').innerText = points.toFixed(2);
    }

    function openModal() { document.getElementById('withdrawModal').style.display = 'block'; }
    function closeModal() { document.getElementById('withdrawModal').style.display = 'none'; }

    function submitWithdrawal() {
      const username = document.getElementById('username').value;
      const amount = document.getElementById('amount').value;
      const wallet = document.getElementById('wallet').value;

      if(!username || !amount || !wallet) {
        alert("ကျေးဇူးပြု၍ အချက်အလက်များကို ပြည့်စုံစွာဖြည့်ပါ။");
        return;
      }

      alert("Withdrawal Request Sent Successfully!");
      closeModal();
    }
  </script>
</body>
</html>
# Alta
