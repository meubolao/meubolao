# TRABALHO 01:  Meu Bolão
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Ian Zanon Pessoa:ianzanon2@gmail.com<br>
Lucas Emanuel Pereira das Posses:posses.lucas@hotmail.com<br>
...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
Este documento contém a especificação do projeto do banco de dados Meu Bolão
<br>e motivação da escolha realizada. <br>

> O projeto "Meu Bolão" se fundamenta em um aplicativo que será responsivo, podendo ser aberto em qualquer aparelho e tem como intuito facilitar as interações envolvendo jogos de apostas, e entreter os usuários durante premiações de filmes, músicas e séries, e outros eventos, gerando um clima de competição saudavel. Surgiu como uma forma de agilizar os jogos de apostas já existentes, a fim de trazer mais praticidade e organização. O projeto não possui fins lucrativos, e qualquer tipo de envolvimento com bens financeiros é de total responsabilidade dos usuários.
 

### 3.MINI-MUNDO Novo<br>
> Um jogo de apostas é responsável por fazer apostas entre usuários acerca dos resultados de premiações de filmes, músicas e séries. O sistema mantém um cadastro de todos os usuários com as seguintes informações: nome,código, e-mail, senha e assinatura do termo de compromisso. Caso o usuário deseje se conectar com o Facebook, esses dados serão herdados do Facebook, tendo somente que acessar o termo de compromisso.Todos os usuários possuirão um perfil contendo:  nome, amigos (no caso de estar conectado com o Facebook, os amigos serão os amigos do Facebook que entraram no jogo pela rede social) , seu nível de Experiência no jogo,número de bolão de apostas que o usuário participou, que ganhou e uma relação(fração) entre bolão de apostas ganhos e que fez parte. No jogo haverão várias salas de apostas, criadas pelo própria pessoa que efetuou registro ou não. Cada sala do usuário terá: nome, tipo de premiação (premiação de filmes, premiações de músicas ou premiações de séries), membros, tempo de duração, data de início da premiação, foto e nível de segurança. Os níveis de segurança de uma sala podem ser público ou privado. Caso for público mantém os atributos anteriores. Se for privada, ela recebe uma senha além dos atributos anteriores. O jogo já possuirá para cada categoria da premiação uma lista de opções pré-definidas com base em categorias das premiações.Exemplo: Se a premiação escolhida for o Oscar, o sistema exibirá todas as categorias pertinentes ao Oscar. Para cada categoria receberão uma quantidade de nomes(indicados) informados pelo usuário. O usuário que não for dono da sala podem entrar em salas informando a senha e o nome dela e realizar apostas. Cada aposta constituirá de uma seleção dos indicados que o usuário acha que ganhará a categoria. Por exemplo, se a categoria for melhor diretor , indicados podem ser: Steven Spielberg, Stanley Kubrick, Ingmar Bergman e Woody Allen. Quem irá definir quem mais acertou as apostas será o próprio sistema com o atributo resultado. O resultado é digitado pelo criador da sala e comparado com todos as apostas dos jogadores.  O jogo gerará uma notificação para cada sala de aposta encerrada contendo: experiência que o jogador adquiriu nessa sala e quantas apostas ele acertou. As experiências adquiridas serão divididas proporcionalmente com a quantidade de acertos de cada jogador. O jogo também possuirá uma tabela com a colocação do jogador e de seus amigos em ordem de maior experiência para a menor.

### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/meubolao/meubolao/blob/master/Bolao_Balsamiq.pdf)
![Arquivo PDF do Protótipo Balsamiq feito para o Bolão](https://github.com/meubolao/meubolao/blob/master/Bolao_Balsamiq.pdf)


#### 4.1 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    e deve ser criada antes do modelo conceitual
    c) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
    
    
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 10 principais relatórios que poderão ser obtidos por meio do sistema proposto!
   1) O sistema exibirá qual indicado numa premiação é a aposta do usuário para vencer determinada categoria.
   2) O sistema exibirá uma lista de usuários organizada por nível que um usuário está jogando, funcionando como um ranking entre jogadores mais antigos e mais velhos.
   3) Caso o usuário deseje conectar/ fazer login na sua conta do bolão com o Facebook, todos os dados como: nome, e-mail e senha serão herdados dessa rede social.
   4) O sistema exibirá informações pertinente as apostas de cada usuário, como: número de bolões que participou, número de bolões que ganhou e uma relação entre o número de bolões que ganhou e que participou.
   5) O sistema exibirá, para cada usuário, quais salas de apostas estão disponíveis para acessar.
   6) Em cada sala de aposta, os usuários participantes terão direito a um chat integrado com o Facebook Messenger, no qual poderão se comunicar durante o tempo da premiação.
   7) Quando um usuário desejar criar uma sala de uma determinada premiação, o sistema indicará sugestões das categorias dessa premiação para que o dono da sala de apostas possa incluir em seu bolão. Exemplo: Se a premiação escolhida for o Oscar, o sistema exibirá todas as categorias pertinentes ao Oscar; caso for o Grammy Awards, o sistema exibirá todas as categorias do Grammy.
   8) Em cada sala de aposta, os jogadores terão direito a visualizar as apostas dos outros participantes dessa sala.
   9) Após o término da premiação, o sistema exibirá dentre as apostas presentes na sala, qual foi o usuário que mais pontuou, que mais acertou quem venceria em cada categoria por meio de uma notificação a todos os participantes da sala.
   10)  A experiência (XP) adquirida em cada sala de apostas será convertido para uma barra de progresso, indicando qual o nível do usuário no sistema. Será exibido a todos os usuários e seus amigos.Por exemplo: Se numa determinada premiação o usuário acertou 15 das 25 categorias, ele receberá uma experiência pré estabelecida à porcentagem de acertos em relação ao total de categorias: 2 XP caso acertado 4% (equivalente a um acerto). 10 XP caso acertado 100%.
  
>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
    A) NOTACAO ENTIDADE RELACIONAMENTO 
        * Para nosso prótótipo limitaremos o modelo conceitual nas 5 principais entidades do escopo
        * O protótipo deve possui no mínimo duas relações N para N
        * o mínimo de entidades do modelo conceitual será igual a 5
        
![Modelo Conceitual](https://github.com/meubolao/meubolao/blob/master/PremiacaoConceitual%20(1).brM3 "Modelo Conceitual")
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    C) QUALIDADE 
        Garantir que a semântica dos atributos seja clara no esquema
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]
## Marco de Entrega 01 em: (20/04/2018)<br>
#### 5.2 DECISÕES DE PROJETO
    [atributo]: [descrição da decisão]
    
    EXEMPLO:
    a) Campo endereço: em nosso projeto optamos por um campo multivalorado e composto, pois a empresa 
    pode possuir para cada departamento mais de uma localização... 
    b) justifique!

#### 5.3 DESCRIÇÃO DOS DADOS 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>

>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..)          
        [Modelo Fisico](https://github.com/meubolao/meubolao/blob/master/TrabalhoPremiacao.mwb)
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
>## Marco de Entrega 04/Entrega Final em: (Data definida no cronograma)<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


        
        


    





