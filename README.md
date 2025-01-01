# SAP-1

Comecei o desenvolvimento do SAP 1 bem atrasado mas comecei.

1 - =Estudar e explorar o Flip Flops e a ferramenta "Digital" e entender o que eu podia fazer dentro dela.
Assim, consegui fazer um contador de 4 bits e expandir ele, acrescendo chaves de "Set" e "Reset";

2 - Refiz o contador;

3 - Uma espécie de Registrador, meu objetivo é criar cada componente e depois juntar tudo...;

4 - Quando fui criar a RAM não achei lógica criar sozinha então aproveitei pra juntar os dois componentes que eu já tinha posse com ela, assim já tenho as funções de contar, registrar em uma REM,
Fornecer um Endereço de 4 bits, um dado de 8 bits e gravar na memoria RAM, e também de ler esse registro em determinada posição e jogar no Barramento;

5 - Fiz um protótipo de um registrador de intrução pra poder acrescentar no Modelo do SAP-1 a posteriori;

6 - Consegui fazer os dois componentes (decodificador de instrução e contador em anel) do controlador/sequencializador e em seguida implementei este, para aí sim tentar junta-los no SAP-1;

7 - Resolvi que o melhor caminho era fazer cada componente separado e jutnar no final, pois assim conseguiria testar tudo e ver se estava funcionando. Tomei esta decisão porque fazendo um por um
e juntando aos pouco ficou meio sem setido para mim;

FINAL: Segue tudo que explicarei agora está dentro do arquivo .ZIP:

1 - apoós terminar a montagem percebi que dava pra criar circuitos integrados que ficava bem mais legível, não sabia ade dado isntante, que isso era possível. Após criar os circuitos e refazer o SAP-1 que ainda não era funcional, comecei a validação.

2 - Primeiro percebi que todos os registradores estavam errados, pois não guardavam os valores quando a comunicação com o barramento era cortada, então fiz uma retoralimentação com multiplexador para poder manter o valor dentro dele.

3 - Corrigido o problema dos registradores, percebi que o estado de alta impedância estava fazendo com que os registradores e até mesmo o contador geracem dados aleatórios por causa do ruído. Então resolvi acrescentando um resistor "PullDown" no barramento,
Ele faz com que o barramento fique forçado ao valor 0 caso não tenha nada gerando sinal, assim corta o estado de alta impedância, evitando geração de ruído.

4 - Em seguida tive que corrigir o controlador de sequencia que estava todo errado, desde a geração de intrução até de sinais. Fiz um mapeamento manual de todos as funções e saídas que deveriam ser apresentadas, pra conseguir concertar o controlador.

5 - por fim conectei tudo e testei algumas instruções, validando cada operação.

HORAS GASTAS: 21 HORAS

