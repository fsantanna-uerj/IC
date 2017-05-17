Uma Avaliação Prática da Linguagem de Programação Céu para Sistemas Embarcados e Internet das Coisas
====================================================================================================

Introdução
----------

A programação de sistemas embarcados envolve leituras de sensores do
ambiente, processamento das informações recebidas, e ativação de atuadores como
resposta.
As leituras dos sensores devem ser processadas concorrentemente e em tempo 
real, de modo a obter as informações necessárias para determinar a próxima ação
do sistema embarcado dentro de um tempo limite aceitável de resposta.
Quando aplicadas no contexto de Internet das Coisas (IoT), os sistemas
embarcados possuem ainda o requisito de comunicação distribuída com
computadores ou outros sistemas embarcados.
Essa característica reativa, concorrente, distribuída, e de tempo real impõe
grandes desafios para os programadores de sistemas embarcados.

A linguagem C ainda é predominante no desenvolvimento de sistemas embarcados e
IoT.
Apesar de ser eficiente em termos de uso de recursos, C não oferece facilidades 
para o desenvolvimento de aplicações concorrentes ou garantias de respostas em 
tempo real.
Grande parte das aplicações são modeladas por máquinas de estados, que usam 
variáveis de estado globais, dificultando o entendimento e manutenção do 
código.

A linguagem Céu possui facilidades dedicadas a lidar com entradas do ambiente,
tais como sensores e temporizadores, assim como a controlar múltiplas linhas de
execução simultâneas.
Dessa maneira, Céu se mostra uma alternativa mais apropriada para o
desenvolvimento de sistemas embarcados e IoT.
Céu é uma linguagem reativa e concorrente desenvolvida na UERJ em conjunto com
o LabLua da PUC-Rio.

Objetivos
---------

- Exercitar o desenvolvimento de sistemas embarcados e IoT em Céu:
    - uso básico de sensores e atuadores
    - uso de transceivers para comunicação sem fio
    - desenvolvimento de aplicações para ambientes inteligentes

- Comparar os resultados com implementações em C sob os seguintes critérios:
    - facilidade de implementação e depuração
    - tamanho do código fonte (e.g., número de linhas)
    - tamanho do objeto (executável)
    - tempo de execução, processamento, e responsividade
    - consumo de energia

- Relatar o processo:
    - documentação
    - artigo acadêmico

Justificativas
--------------

A Internet das Coisas (IoT) é a interconexão de objetos, veículos, edificações,
e outros dispositivos físicos com eletrônicos embarcados.
Estima-se que em 2020 haverá 30 bilhões de dispositivos conectados.
Além de ser uma área emergente de pesquisa em computação, a IoT envole
múltiplas linhas de pesquisa, tais como linguagens de programação, sistemas
embarcados, redes e sistemas distribuídos, sistemas operacionais, e engenharia
de software.

Apesar de este projeto focar na linha de linguagens de programação, a proposta
de uma abordagem prática visa explorar outras áreas de maneira a fomentar a
cooperação com outros grupos de pesquisa da universidade.
Atualmente, a UERJ oferece três disciplinas com uma abordagem prática a IoT:
    - Sistemas Reativos, que adota Arduino e Céu;
    - Sistemas Distribuídos, que adota redes de sensores sem fio;
    - Projeto de Engenharia de Software, onde os alunos projetam ambientes inteligentes.

O uso de ambientes inteligentes como aplicação fim visa explorar demandas reais
do mundo universitário, tais como detecção de presença em sala de aula,
uso racional de luz e ar-condicionado, e permissão de acesso a salas e
laboratórios.

Metas
-----

- Aplicações simples
    - pelo menos 3 aplicações
    - integração entre pelo menos um sensor e um atuador

- Aplicações médias
    - pelo menos 2 aplicações
    - integração entre sensores, atuadores, e transceivers

- Aplicação complexa
    - pelo menos 1 aplicação
    - 

- Artigo acadêmico

Método
------

C e Arduino são as plataformas de software e hardware mais populares para
ensino e pesquisa em sistemas embarcados.
A linguagem Céu já possui binding nativo para Arduino.
Além disso, todas as bibliotecas em C disponíveis para Arduino são compatíveis
com Céu.
O aluno já possui familiaridade com essas ferramentas.

O laboratório dispõe de diversos sensores, atuadores, e transceivers para o
desenvolvimento de ambientes inteligentes, tais como leitores de RFID; sensores
de luz, temperatura, umidade, e distância; motores e servo mecanismos; e rádios
RF e Bluetooth.

Inicialmente, os sensores, atuadores, e transceivers serão testados
isoladamente de maneira a comparar seus usos entre C e Céu.
Em seguida, estes serão integrados de maneira a se desenvolver pelo menos
três aplicações simples, duas médias, e uma complexa.

Para analisarmos os resultados em termos de processamento, uso de memória, 
tamanho de código e facilidade de programação usaremos a seguinte abordagem:
    - tempo médio entre a leitura de um sensor até a ativação dos atuadores
    - tamanho em bytes da região de código e dados dos programas
    - quantidade de linhas de código
    - uso de variáveis globais e máquinas de estado explícitas
Essa abordagem já foi adotada em artigos acadêmicos publicados no contexto de
redes de sensores sem fio.

Resultados Esperados
--------------------

- Protótipo funcional de uma aplicação de ambiente inteligente a ser instalada
  na universidade.
- Ganhos de facilidade de implementação com a adoção de Céu mantendo
  performance e uso de memória comparável à C.
- Artigo acadêmico com os resultados obtidos.

Referências
-----------

- Brown, Eric (2016). "Who Needs the Internet of Things?". Linux.com.
- Nordrum, Amy (2016). "Popular Internet of Things Forecast of 50 Billion Devices by 2020 Is Outdated". IEEE.
- Augusto, Juan C; Callaghan, Vic (2013). "Intelligent Environments: a manifesto". Human-centric Computing and Information Sciences. Springer. doi:10.1186/2192-1962-3-12.
- Sant'Anna, Francisco (2013). "Safe system-level concurrency on resource-constrained nodes". In Proceedings of the 11th ACM Conference on Embedded Networked Sensor Systems (SenSys '13). ACM. doi:10.1145/2517351.2517360.

Cronograma
----------

    Descrição                                               1o  2o  3o  4o
    Levantamento de aplicações para robótica                x
    Classificação das aplicações (simples, médio, difícil)  x
    Implementação de aplicações simples                     x
    Implementação de aplicações médias                          x
    Implementação de aplicações difíceis                            x   x
    Redação de relatório e artigo científico                        x   x
    Apresentações sobre o andamento do projeto              x   x   x   x
    Análise das aplicações segundo metodologia              x   x   x   x

<!--
As seguintes características da linguagem Céu serão exploradas no processo de 
desenvolvimento:

* O conceito preciso de tempo:

"Céu is grounded on a precise definition of time as a discrete sequence of 
external input events: a sequence because only a single input event is handled 
at a time; discrete because reactions to events are guaranteed to execute in 
bounded time."

É interessante a ideia sequencial de tempo porque para cada input, o robô 
reagirá diretamente, desta forma, esperamos criar uma alternativa reativa a 
maquina de estados e ser discreto também é interessante por em muitos sistemas 
de robótica existirem tempos limites para determinadas ações.	

"The synchronous execution model of Céu is based on the hypothesis that 
internal reactions run infinitely faster in comparison to the rate of external 
events." 

Controle de tempo:

O controle de tempo em C é de dificil implementação e asserção.

"The await statement of Céu supports wall-clock time and handles deltas 
automatically, resulting in more robust applications."

* Eventos internos:
 Útil para tratar exceções.
 "Internal events also provide means for describing more elaborate control 
structures, such as exceptions."

A fim de analisar o reaproveitamento de codigo e tempo de depuração usaremos o 
git, para versionar o código e analisar sua evolução com o tempo, podendo ver 
erros interessantes e como foram solucionados.
-->

