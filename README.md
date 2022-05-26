# calculadoraJavaScript
function calculadora (){
    const operaçao = Number(prompt('Escolha uma operação:\n 1 - soma (+)\n 2 - subtração (-)\n 3 - multiplicação (*)\n 4 - divisão real (/)\n 5 - divisão inteira (%)\n 6 - potenciação (**)'))

    if (!operaçao || operaçao >= 7){
        alert('Erro - Operação Invalida!')
        calculadora();
    }   else{
        let n1 = Number(prompt ('Digite o primeiro número:'));
        let n2 = Number(prompt ('Digite o segundo número:'));
        let resultado;

        if (! n1 || !n2 ){
            alert('Erro - Parametros invalidos!')
            calculadora();
        }else{
            
        function soma (){
            resultado = n1 + n2;
            alert(`${n1} + ${n2} = ${resultado}`)
            novaOperaçao();
        }
        function subtração (){
            resultado = n1 - n2;
            alert(`${n1} - ${n2} = ${resultado}`)
            novaOperaçao();
        }
        function multiplicação (){
            resultado = n1 * n2;
            alert(`${n1} * ${n2} = ${resultado}`)
            novaOperaçao();
        }
        function divisaoreal (){
            resultado = n1 / n2;
            alert(`${n1} / ${n2} = ${resultado}`)
            novaOperaçao();
        }
        function divisaointeira (){
            resultado = n1 + n2;
            alert(`O resto da divisão entre ${n1} e ${n2} é igual a ${resultado}`)
            novaOperaçao();
        }
        function potenciaçao (){
            resultado = n1 ** n2;
            alert(`${n1} elevado a ${n2} é igual a ${resultado}`)
            novaOperaçao();
        }

        function novaOperaçao (){
            let opçao = prompt('Deseja fazer outra operação?\n 1 - SIM\n 2 - NÃO')

            if (opçao == 1){
                calculadora()
            }   else if (opçao == 2){
                alert('Até Mais!')
            }   else{
                alert('Digite uma opção valida')
                novaOperaçao();
            }   
        }}

        
        if (operaçao == 1){
            soma();
        }   else if (operaçao == 2){
            subtração();
        }   else if (operaçao == 3){
            multiplicação();
        }   else if (operaçao == 4){
            divisaoreal();
        }   else if (operaçao == 5){
            divisaointeira();
        }   else if (operaçao == 6){
            potenciaçao();
        }   }

    
}

calculadora();
