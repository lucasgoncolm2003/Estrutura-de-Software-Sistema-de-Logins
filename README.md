# Estrutura de Software de Sistema de Logins - [Desafio Coderbyte]
## Enunciado
Imagine que você é o(a) arquiteto(a) responsável pelo desenho de um sistema de logins para um site extremamente concorrido de ingressos de um mega show de Rock em Rio (got it?). Dado que o número de ingressos é limitado e muito inferior a quantidade de acessos no dia venda, você precisa garantir que o site só irá finalizar a venda para pessoas que realmente vão receber o ingresso, ou seja, você não pode deixar uma pessoa comprar um ingresso sem que haja mais disponíveis. Além disso, um cliente com internet mais lenta não ficaria feliz de não conseguir comprar seu ingresso pois uma pessoa com internet mais veloz passou sua frente. Desenhe uma estrutura de software que sustente esse serviço, pode ser um desenho simples, da maneira que você preferir, desde que o mesmo transmita a ideia da arquitetura que você teve para quem o lê.
## Solução
Um Cliente pede uma Requisição ao Software, caso não tenha um Login, ele é levado para um Cadastro; mas caso já o tenho, apenas o confirma para comprar seu Ingresso. Essa requisição faz com que os demais clientes tenham que aguardar a primeira ser concluída para que as próximas sejam atendidas. O Sistema irá verificar o número de ingressos; caso existam mais disponíveis, ele é levado para a página de Compra, de Finalização de Compra, e no fim, finaliza a sua Requisição e o Sistema solicita a próxima Requisição.
Porém, caso não existam mais Ingressos, o Cliente vai ser movido para a Solicitação de Aguardo, e quando a Empresa Responsável pelo Show fizer um Upload de Novos Ingressos, o mesmo Cliente será redirecionado para a página de Compra, de Finalização de Compra, e por fim, finalizar sua Requisição e solicitar a Próxima Requisição. Vale destacar que o Upload de Ingressos deve ter um número acima de 1 ingresso, pois não faria sentido prático que uma empresa disponibilizasse apenas 1 novo ingresso. A estrutura seria:
<div align="center">
  <img height="500" width="700" src="https://user-images.githubusercontent.com/112359793/216433542-b0b60e1b-7246-4362-a460-13ed8b33db2f.jpeg" />
</div>

