# tool-kit

Passo 1 - Adicionar botão e input
Vamos criar um input e um botão. Quando a pessoa clicar no botão, a lista deverá ser incrementada com o valor digitado no input.

Passo 2 - Criando um estado para a lista toolKit
A partir de então, vamos adicionar novos valores à lista. Dessa forma, é importante que ela seja dinâmica e que suas atualizações reflitam na interface. Assim, é necessário que nossa lista esteja no estado do componente.

Vamos criar um novo estado chamado toolList que inicializará com o valor da lista toolKit. Também vamos atualizar todas as nossas referências de toolKit para o estado toolList.

Passo 3 - Criando um estado para armazenar o valor do input
Precisamos armazenar o valor digitado no input. Felizmente, conhecemos a ferramenta perfeita para armazenar dados em uma aplicação: o estado! Então, criaremos um estado para armazenar tudo que está sendo digitado no input, alterando o estado diretamente no atributo onChange do input:input.
Quando adicionamos o event handler no evento onChange, sempre que o input sofrer alguma alteração, ele irá armazenar o seu value no novo estado inputValue.

Passo 4 - Implementando a funcionalidade de adicionar itens à lista
É necessário criar uma função para o botão Adicionar. Assim, é preciso que, quando clicado, ele adicione o valor armazenado no estado inputValue. Como explicado anteriormente, não podemos simplesmente adicionar o valor à lista com um Array.push por exemplo, mas podemos reatribuir uma nova lista a esse estado, utilizando o spread operator.

Com essa finalidade, criaremos a função handleAddClick() da seguinte forma:

Primeiramente, o spread operator fará a verificação para descobrir se existe algo digitado no input;
Caso exista, ele irá setar o estado toolList com uma lista (setToolList([])) que contém todos os valores que estão armazenados no estado toolList e, ainda, acrescentar o valor armazenado no estado inputValue (...toolList, inputValue).
Com essa função criada, deve-se adicioná-la no evento de clique do botão.
Pronto! A pessoa usuária poderá adicionar novos valores à lista de ferramentas.

Passo 5 - Renderizando uma lista com todos os valores do toolList
Por fim, vamos renderizar uma lista contendo todos os valores do estado toolList:
