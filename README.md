<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        @font-face{
         font-family: "ceviche";
         src: url("/fonts/CevicheOne-Regular.ttf");
        }
        @font-face{
         font-family: computo ;
         src: url("/fonts/ComputoMonospace-p73xO.ttf");
        }
        @font-face{
         font-family: cursed;
         src: url("/fonts/CursedTimerUlil-Aznm.ttf");
        }
        @font-face{
         font-family: lcd;
         src: url("/fonts/LcdSolid-VPzB.ttf");
        }
        body{
            background-color: rgb(65, 83, 30);
        }
        h1{
            font-family:computo;
            color: rgb(0, 0, 0);
            font-size: 36pt;
            text-align: center;
            text-shadow: grey 1px 6px 8px;
        }
        div{
            border-radius: 20px;
            box-shadow: 2px 2px 2px 2px grey;
            width: 420px;
            height: 600px;
            background-color: rgb(5, 20, 5);
            margin: auto;
        }
        #resposta{
            background-color: rgb(110, 110, 110);
            box-shadow: 1px 1px 8px 3px rgb(0, 0, 0);
            width: 400px;
            height: 100px;
            margin: auto;
            border: solid rgb(36, 22, 22) 5px;
            font-family: lcd;
            color: white;
            font-size: 20pt;
            text-align: center;    
        }
        #resposta:hover{
            background-color: rgba(153, 205, 50, 0.753);
        }
        #entrada{
            position: relative;
            display: block;
            border-radius: 5px;
            margin: auto;
            background-color: rgba(90, 31, 31, 0.644);
            color: white;
            font-family: lcd;
        }
        #entrada:hover{
            background-color: rgb(56, 56, 56);
        }
        #entrada2{
            position: relative;
            display: block;
            border-radius: 5px;
            margin: auto; 
            background-color: rgba(90, 31, 31, 0.644);
            color: white;
            font-family: lcd;
        }
        #entrada2:hover{
            background-color: rgb(56, 56, 56) ;
        }
        .botão{
            background-color: tomato;
            margin-top: 60px;
            border-radius: 10px;
            font-family: lcd;
            color: black;
        }
        .botão:hover{
            background-color: yellow;
        }
        footer{
            color: white;
            margin-top: 45px; 
            
        }
        span{
           font-family: lcd; 
        }
    </style>
</head>
<body>
    <h1>Calculadora</h1>

    <div>
        
        <input type="number" name="entrada" id="entrada" onmouseenter="cor()"> <br>
        <input type="number" name="entrada2" id="entrada2"><br> <br>
        
        <section id="resposta"> &shy;</section><br><br>

        <input type="button" value="Somar +" onclick="soma()" class="botão">
        <input type="button" value="Subtrair -" onclick="sub()" class="botão">
        <input type="button" value="Multiplicar X" onclick="mult()" class="botão">
        <input type="button" value="Dividir /" onclick="divi()" class="botão">
        <br> <br>

       <footer> &copy; <span> Nalbert Bastos dos Santos</span></footer>
    </div>
    <script>
        function soma(){
            let num1 = document.getElementById('entrada');
            let num2 = document.getElementById('entrada2');
            let n1 = Number(num1.value);
            let n2 = Number(num2.value);
            let res = document.getElementById('resposta');
 
            if(num1.value.length == 0){
                alert('[ERRO] Sem primeiro valor')
            }else if(num2.value.length == 0){
                alert('[ERRO] Sem segundo valor')
            }else{
                res.innerHTML = n1 + n2
            }
        }
        function sub(){
            let num1 = document.getElementById('entrada');
            let num2 = document.getElementById('entrada2');
            let n1 = Number(num1.value);
            let n2 = Number(num2.value);
            let res = document.getElementById('resposta');
            
            if(num1.value.length == 0){
                alert('[ERRO] Sem primeiro valor')
            }else if(num2.value.length == 0){
                alert('[ERRO] Sem segundo valor')
            }else{
                res.innerHTML = n1 - n2 
            } 
            /*if(res.value.length >= 9 && res.value.length <=14 ){
                document.getElementById('resposta').style.fontSize = '15pt'
                
            } else if(res.value.length >=15){
                document.getElementById('resposta').style.fontSize = '10pt'
            }
            res.innerHTML = n1 - n2*/
        }
        function mult(){
            let num1 = document.getElementById('entrada');
            let num2 = document.getElementById('entrada2');
            let n1 = Number(num1.value);
            let n2 = Number(num2.value);
            let res = document.getElementById('resposta');

            if(num1.value.length == 0){
                alert('[ERRO] Sem primeiro valor')
            }else if(num2.value.length == 0){
                alert('[ERRO] Sem segundo valor')
            }else{
                res.innerHTML = n1 * n2;
            }
        }
        function divi(){
            let num1 = document.getElementById('entrada');
            let num2 = document.getElementById('entrada2');
            let n1 = Number(num1.value);
            let n2 = Number(num2.value);
            let res = document.getElementById('resposta');
            if(num1.value.length == 0){
                alert('[ERRO] Sem primeiro valor')
            }else if(num2.value.length == 0){
                alert('[ERRO] Sem segundo valor')
            }else{
                res.innerHTML = n1 / n2 
            }    
        }
    </script>
</body>

</html>
