<!DOCTYPE html>
<html lang="pt-br">

<head>

<meta charset="UTF-8">
<title>Ortopets: Cadeiras de Rodas para Cães</title>

<style>

body{
margin:0;
font-family:Arial;
background-color:#00aeff;
}

/* titulo */

.titulo{
text-align:center;
font-size:50px;
color:#0145ff;
margin-top:20px;
}

/* caixa principal */

#mae{
width:650px;
margin:auto;
background:linear-gradient(#0000ff,#001aff);
padding:25px;
border-radius:10px;
color:white;
}

/* cabeçalho */

#cabecalho{
background-color:#f2d9b3;
color:black;
padding:5px;
margin-bottom:20px;
text-align:center;
font-weight:bold;
}

/* imagem */

.imagem{
text-align:center;
margin-bottom:20px;
}

.imagem img{
width:200px;
border-radius:10px;
}

/* rodapé */

#rodape{
margin-top:20px;
text-align:center;
}

button{
padding:10px 20px;
font-size:16px;
margin:5px;
cursor:pointer;
}

</style>

</head>

<body>

<h1 class="titulo">Ortopets: Cadeiras de Rodas para Cães</h1>

<div id="mae">

<div id="cabecalho">
Informações Necessárias para Enviar à Maurício. Contato: (14)99709-2829
</div>

<div class="imagem">
<img src="./cachorro1.jpg.jpeg">
<img src="./cachorro2.jpg.jpeg">

</div>

<form id="formulario">

<label>Digite o seu Nome:</label><br>
<input type="text" id="nome" required><br><br>

<label>Digite o seu Telefone:</label><br>
<input type="text" id="telefone" required><br><br>

<label>Digite o Nome do Cão:</label><br>
<input type="text" id="cao"><br><br>

<label>Qual é o porte do seu cão?</label><br>

<input type="radio" name="porte" value="Grande"> Grande <br>
<input type="radio" name="porte" value="Médio"> Médio <br>
<input type="radio" name="porte" value="Pequeno"> Pequeno <br><br>

<label>Peso do cachorro:</label><br>
<input type="text" id="peso"><br><br>

<label>Envie uma foto do cachorro:</label><br>
<input type="file"><br><br>

<div id="rodape">

<button type="button" onclick="enviarWhats()">Enviar</button>

<button type="reset">Limpar</button>

</div>

</form>

</div>

<script>

function enviarWhats(){

let nome = document.getElementById("nome").value;
let telefone = document.getElementById("telefone").value;
let cao = document.getElementById("cao").value;
let peso = document.getElementById("peso").value;

let porte = document.querySelector('input[name="porte"]:checked');

if(porte){
porte = porte.value;
}else{
porte = "";
}

let mensagem =
`Pedido de Carrinho para Cão

Nome: ${nome}
Telefone: ${telefone}
Nome do Cão: ${cao}
Porte: ${porte}
Peso: ${peso}`;

let numero = "5514997092829";

let url = "https://wa.me/"+numero+"?text="+encodeURIComponent(mensagem);

window.open(url,"_blank");

}

</script>

</body>
</html>
