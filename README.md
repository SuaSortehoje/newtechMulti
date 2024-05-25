<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CENTENA_10h_horas</title>
    <style>
    
        body {
            font-family: Arial, sans-serif;
            background-color: black;
            color: white;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        h1{
            text-align: center;
            color: black;
            font-size:22px;  
        }
      h2{ display:flex;
           flex-direction:row;
           justify-content:center;
           text-align:center;
           margin:auto;      
        }
        .container {
            background-color: green;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="text"]{
            width: 50%;
            padding: 10px;
            margin-bottom: 6px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        input[type="number"]{
            width: 30%;
            padding: 10px;
            margin-bottom: 6px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        select {
            width: 45%;
            padding: 10px;
            margin-bottom: 6px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        input[type="tel"]{
            width: 18%;
            padding: 10px;
            margin-bottom: 6px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        button {
            padding: 10px 20px;
            background-color: #00d0ff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #00aacc;
        }
        button:disabled {
            background-color: #888;
            cursor: not-allowed;
        }
        #modal {
            display: none;
            background-color: rgba(0, 0, 0, 0.5);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            justify-content: center;
            align-items: center;
        }
        #modal-content {
            background-color: black;
            color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        h {
          color:red;
          border-radius:10px;
          border:5px;
          font-weight:bold;
      }
      h {
          animation:h 1s infinite;
      }
       @keyframes h{
           10%{background-color:blue;}
           80% {background-color:yellow}
       }
        git {
            color:white;
        }  
       #valorInput{
            width: 28%;
            padding: 10px;
            margin-bottom: 6px;
            border-radius: 5px;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
           .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <div class="container">
     <h1>RIFA CENTENA <h>10:00h</h><br><git> R$ 1.00 </git>GANHA<git> R$ 700.00</git></h1>
<h2> MULTIJOGO </h2><br>
        <input type="tel" id="valorInput" placeholder="Digite o valor" maxlength="2"><br>
        <input type="text" id="nomeInput" placeholder="Digite seu nome">
        <select id="premioInput">
            <option value="premio">1º Prêmio</option>
            <option value="1a5premio">1º ao 5º Prêmio</option>
            <option value="1a10premio">1º ao 10º Prêmio</option>
        </select>
        <br>
      <input type="tel" id="milharInput1" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput2" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput3" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput4" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput5" placeholder="  Centena" maxlength="3">
         <input type="tel" id="milharInput6" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput7" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput8" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput9" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput10" placeholder="  Centena" maxlength="3">
         <input type="tel" id="milharInput11" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput12" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput13" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput14" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput15" placeholder="  Centena" maxlength="3">
         <input type="tel" id="milharInput16" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput17" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput18" placeholder=" Centena" maxlength="3">
        <input type="tel" id="milharInput19" placeholder="  Centena" maxlength="3">
        <input type="tel" id="milharInput20" placeholder="  Centena" maxlength="3">
        <br>
        <button id="botaoAdicionar" onclick="adicionarMilhar()">Adicionar Milhar</button>
        <button id="botaoCalcular" onclick="calcular()" disabled>Calcular</button>
    </div>

    <div id="modal">
        <div id="modal-content">
            <h2>Detalhes do Jogo</h2>
             <span class="close" onclick="closeModal()">&times;</span>  
            <p>Nome: <span id="nomePix"></span></p>
            <p>Horário: <span id="horarioPix"></span></p>
            <p>Milhares: <span id="milharesPix"></span></p>
            <p>Total a Pagar: R$ <span id="totalPagar"></span></p>
            <p>Total a Receber: R$ <span id="totalReceber"></span></p>
            <p>Código PIX: <span id="codigoPix"></span></p>
            <button onclick="copyPix()">Copiar PIX</button>
            <button onclick="enviarWhatsApp()">Enviar por WhatsApp</button>
        </div>
    </div>

    <script>
        var milhares = [];

        function adicionarMilhar() {
    for (var i = 1; i <= 20; i++) {
        var milharInput = document.getElementById('milharInput' + i);
        if (milharInput.value.length === 3) {
            milhares.push(milharInput.value);
        }
    }
    if (milhares.length > 0) {
        document.getElementById('botaoCalcular').disabled = false;
    }
    alert('Milhares adicionados com sucesso!');
}
   function calcular() {
    var valor = document.getElementById('valorInput').value;
    var nome = document.getElementById('nomeInput').value;
    var premio = document.getElementById('premioInput').value;

    var agora = new Date();
    var horaAtual = agora.getHours();
    var minutosAtual = agora.getMinutes();

    if (horaAtual > 9 || (horaAtual === 9 && minutosAtual > 50)) {
        document.getElementById('botaoCalcular').disabled = true;
        alert('O tempo limite para JOGAR foi Excedido ATE 9:50.');
        return;
    }

    if (nome && valor) {
        valor = parseInt(valor);
        if (!isNaN(valor)) {
            var total;
            if (premio === "1a5premio") {
                total = valor * 700 / 5;
            } else if (premio === "1a10premio") {
                total = valor * 700 / 10;
            } else {
                total = valor * 700;
            }
            var totalPagar = valor * milhares.length;
            showModal(nome, totalPagar, total);
        } else {
            alert('Por favor, digite um valor válido.');
        }
    } else {
        alert('Por favor, preencha pelo menos o nome e o valor.');
    }
}


        function showModal(nome, totalPagar, totalReceber) {
            var modal = document.getElementById('modal');
            var nomePix = document.getElementById('nomePix');
            var totalPagarElement = document.getElementById('totalPagar');
            var totalReceberElement = document.getElementById('totalReceber');
            var codigoPix = document.getElementById('codigoPix');

            nomePix.textContent = nome;
            totalPagarElement.textContent = totalPagar.toFixed(2);
            totalReceberElement.textContent = totalReceber.toFixed(2);

            codigoPix.textContent = '71992290058';

            modal.style.display = 'flex';
        }

        function copyPix() {
            var codigoPix = document.getElementById('codigoPix');
            var range = document.createRange();
            range.selectNode(codigoPix);
            window.getSelection().removeAllRanges();
            window.getSelection().addRange(range);
            document.execCommand('copy');
            window.getSelection().removeAllRanges();
            alert('Código PIX copiado!');
        }

        function enviarWhatsApp() {
            var nome = document.getElementById('nomeInput').value;
            var valor = document.getElementById('valorInput').value;
            var premio = document.getElementById('premioInput').value;
            var milharesString = milhares.join(', ');
            var totalPagar = document.getElementById('totalPagar').textContent;
            var totalReceber = document.getElementById('totalReceber').textContent;
            var codigoPix = document.getElementById('codigoPix').textContent;

            var selecionado = document.getElementById('premioInput');
            var premioText = selecionado.options[selecionado.selectedIndex].text;
        var multijogo = "MULTIJOGO CENTENA DAS 10:00 HORAS";

const chavePagamento = "https://multijogo.github.io/Link-de-pagamento-pix/";
    
  const  titulo = "https://multijogo-38.webnode.page/centenas/";
    
    const horaLimite =  "HORA LIMITE 09:55";

    // Gerar o código de 6 dígitos
    const codigo = Math.floor(100000 + Math.random() * 900000);
    
    
   const responsabilidade = "E de Responsabilidade do Apostador Conferir sua pule antes da Extracao";

            var mensagem = `${titulo}
            *${multijogo}*
            
       *Olá* , ${nome}!
    
               DATA E HORA ATUAL
  *Data: ${new Date().toLocaleDateString()}*       *Hora: ${new Date().toLocaleTimeString()}*
              *${horaLimite }*
             
            *Segue o código PIX*: ${chavePagamento}
         
            *Valor a  Pagar* : R$ ${totalPagar}
            
            *Valor a Receber* : R$ ${totalReceber}
        
             *Prêmio* : ${premioText}
         
             *Centena* : ${milharesString}
         
      *Nº Controle da Aposta* : *${codigo}*
 
*${responsabilidade}*`;

            const linkWhatsApp = `https://wa.me/5571992290058?text=${encodeURIComponent(mensagem)}`;
    window.open(linkWhatsApp, '_blank');
}

function closeModal() {
    var modal = document.getElementById('modal');
    modal.style.display = 'none';
}

    </script>
</body>
</html>
