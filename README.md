# Sistema supervisório na web para CLP Siemens S7 1200 com utilização de JavaScript e Ajax


- Projeto de simulação de um Web Server rodando em um CLP modelo S7 1200 da Siemens, com dados de variáveis do próprio programa do CLP. O projeto baseou-se em uma funcionalidade
específica do modelo de CLP da Siemens da linha S7 1200, onde possibilita a inclusão de uma página web no seu sistema que pode conter tanto amostragem das variáveis do CLP, 
como também alterar o valor das variáveis a partir da página gerada. 

## CLP Simatic Siemens S7 1200

- O modelo de CLP S7 1200 da marca Siemens é um aprelho amplamente utilizado no setor de automação industrial. Existem inúmeras vantagens de utilizar esse tipo de hardware, no entanto, sua aplicação em sistemas supervisórios é de suma importância, principalmente com a funcionalidade de Web Server, que permite a criação de telas em formato de páginas na web, evitando assim o custo de aquisição de outros hardwares tais como as IHM's. A imagem a seguir ilustra o hardware utilizado nesse projeto. 

![WhatsApp Image 2022-08-26 at 19 34 25](https://user-images.githubusercontent.com/35776840/187011040-d0e08a5b-46fe-4b24-bad2-b5088f9cd6c2.jpeg)

## Configurações iniciais no CLP

- Como mencionado anteriormente, o modelo de CLP S7 1200, possibilita a ligação de um web servidor, que nada mais é que uma funcionalidade própria do modelo de CPU. A imagem a seguir, elucida como fazer tal configuração através do TIA Portal. Desse modo nas configurações do PLC deve-se ativar a função web server e posteriormente apontar o arquivo a qual deverá ser carregado no endereçod e IP do PLC, ou seja, a página web criada. As duas figuras a seguir elucidam esses dois passos.


![EnableWebserver](https://user-images.githubusercontent.com/35776840/187011433-75cb1c7d-7786-4b92-bcba-29e89bc406ad.png)

![fig5](https://user-images.githubusercontent.com/35776840/187011432-efaab0cb-06c7-498f-871f-e5e7c5aa1b70.png)

## Simulação de um valor variável ao longo do tempo

- Para esse projeto, o intuito é simular um valor variável ao longo do tempo uma vez que deve-se utilizar atualizações de telas simuntâneas na página web. Desse modo, uma lógica na Linguagem Ladder foi desenvolvida para simular um contador de 1 até 36 que retorna ao valor 1 ao chegar no seu limite superior. A Figura a seguir elucida tal lógica no TIA PORTAL.

![fig4](https://user-images.githubusercontent.com/35776840/187011430-ed27af22-c204-4207-9377-171ee01e3413.png)

## A página Web do projeto 

- Nesse projeto, foi utilizado vários testes para uma amostragem completa, ou seja, foi testado o envio de uma única variável por vez e posteriormente um conjunto de variáveis diferentes. O que foi possível observar é que os dados devem ser enviados no formato JSON para a aplicação em um arquivo HTML e no mesmo, pode-se executar algumas funções com JavaScript, como no caso a requisição do JSON via JQuery. Além disso, a página foi estilizada com algumas bibliotecas do JS: Highcharts de forma que todas as amostragens deveriam ser dinâmicas e auto atualizáveis. Para a amostragem em tempo real foi feito o uso da tecnolgia AJAX no script da página. Os resultados podem ser observados a seguir:


![as](https://user-images.githubusercontent.com/35776840/187365041-b747d16f-7f87-4887-8af5-0f75d1214ae7.png)


![sada](https://user-images.githubusercontent.com/35776840/187365043-2b9daa18-446d-42e6-801d-472f445d7a5c.png)


![saddada](https://user-images.githubusercontent.com/35776840/187365047-d404b263-2386-4df0-a66b-3d579f1911bb.png)






