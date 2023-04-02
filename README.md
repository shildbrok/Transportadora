# Transportadora
Solução da Lista de exercicio

`````
Algoritmo "Transportadora"

//codigo para empresa de caminhão
// receber um numero entre 1 e 5
// 1 == 35% imposto
// 2 == 25%
// 3 == 15%
// 4 == 5%
// 5 == isento


// receber o kilo do caminhão


// receber o código da carga entre 10 e 40
// entre 10 e 20 == 100 * kilo
// entre 21 e 30 == 250 * kilo
// entre 31 e 40 == 340 * kilo


//mostrar o peso da carga do caminha em KG
//mostrar o preço da craga
//o valor do imposto sabendo que vc o imposto é cobrado por regiao
// valor total do caminhão


Var
imposto, peso, preco_Carga, preco_impo, prcFinal : real
codigo, codigo_carga: inteiro


Inicio
escreva(" Insira o código do estado da viagem : ")
leia(codigo)
//estrutura de repetição para receber o codigo entre
// 1 e 5
enquanto (codigo>5)ou(codigo<1) faca
         escreva(" Insira o código do estado da viagem : ")
         leia(codigo)
fimenquanto

se codigo = 1 entao
   imposto <- 0.35
fimse
se codigo = 2 entao
   imposto <- 0.25
fimse
se codigo = 3 entao
   imposto <- 0.15
fimse
se codigo = 4 entao
   imposto <- 0.05
fimse
se codigo = 5 entao
   imposto <- 0.00
fimse

//nesse trecho mudamos definimos o imposto da carga

escreva(" Insira o peso do caminhão (KG) : ")
leia(peso)


//pegando o código da carga para calcular o Preço.
escreva(" Insira o código da carga: ")
leia(codigo_carga)
enquanto (codigo_carga < 10) ou (codigo_carga > 40) faca
         escreval(" ")
         escreval(" Error :: Not Found : Insira um numero entre 10 e 40!")
         escreva(" Insira o código da carga: ")
         leia(codigo_carga)
fimenquanto

se (codigo_carga>9)e(codigo_carga<21) entao
       preco_carga <- 100
fimse
se (codigo_carga>20)e(codigo_carga<31) entao
       preco_carga <- 250
fimse
se (codigo_carga>30)e(codigo_carga<41) entao
       preco_carga <- 340
fimse

//agora vamos fazer os calculos.

//Tratamento de dados e calculos.
prcFinal <- preco_carga * peso

preco_impo <- prcFinal * imposto

escreval("Calulo de viagem: Peso(Kg):", peso," X Preço/Peso :",preco_carga," = R$",prcFinal)
escreval("Calculo de Imposto:",preco_impo)
escreval("Calculo final de Preço: R$", prcFinal + preco_impo)


Fimalgoritmo

`````
