Anotações das aulas sobre GIT e GITHUB

Estarei aqui realzando anotações que julgar relevante para essas aulas.


- Comandos básicos de navegação são eles cd, dir e ls, mkdir e del / rmdir e rm -rf;
- Comando dir (windows) e ls (linux), serve para listar tudo que existe dentro do diretório;
- Comando cd (windows e linux), serve para navegar nas pastas tem que vir acompanhado de /;
- Comando cd.. (windows e linux), serve para retroceder nas pastas;
- Comando cls (windows) e clear (linux), serve para limpar a tela;
- Comando tab (windows) completa o comando;
- Comando mkdir (windows e linux), serve para criar uma pasta;
- Comando echo (windows) printa um texto;
- Comando/símbolo > é um redirecionador, ele vai pegar o que foi printado na tela ou criado e jogar num arquivo. Trata-se de comandos para criação de um arquivo 
  sem usar o modelo tradional, cria através de comandos; 
- Forma de deletar o arquivo, comando del (windows), esse comando deleta apenas o arquivo, não a pasta mesmo que tenhamos dado o comando, como na aula 
  de "de teste", que foi a pasta que criei;
- Comando Î (seta pra cima), navega entre comandos anteriores utilizados;
- O comando para remover a pasta é rmdir (windows), ele remove a pasta/repositório/diretório e tudo que há dentro, ele deve vir acompanhado dos 
  comando /s e /q, o /s é para excluir todas os arquivos e o /q executa o trabalho sem a pergunta de confirmação (sim ou não)
  No linux usamos apenas o rm com as flags -rf, o r é para apagar tudo e o f para não perguntar (sim ou não);
- Iremos usar o GIT BASH, pois atenderá a ambos os sistemas no que se refere a comandos;
- SHA1 é um comando de encriptação dos arquivos, é uma codificação única para cada arquivo;
- Para passar o arquivo para o algoritmo de encriptação, o SHA1, o comando utilizado é o openssl sha1 e o nome do arquivo que deseja encriptar;
- Os objetos do GIT resposnáveis por versionamento do código, são BLOBS, TREES e COMMIT;
- Versionamento, é um gerenciamento de versões diferentes dos arquivos, documentos, software;
- O objeto BLOB (bolhas), armazena metadados, tamanos dos arquivos, as características;
- O obejto TREE (árvores), armazenam os BLOB;
- O objeto COMMIT é o que junta tudo, quando o arquivo é alterado, o SHA1 é modificado e toda a estrutura também é alterada, é possível ver todo o histórico 
  de alterações através do histórico de COMMIT;
- Comando no GIT, para iniciar o repositório no GIT usaremos o git init, mover arquivos git add e o git commit para comitar as alterações do arquivo local para 
  o GITHUB;
- Então eu criei uma nova pasta para rodar o GIT nela para poder exercitar os comandos, para que o GIT possa gerencia-la, e o comando para isso é o git add, 
  ao dar esse comando, retorna a mensagem que o GIT criou uma pasta chamada .git/, mas não aparece mesmo dando o comando de listar (ls ou dir), pois é uma pasta oculta, 
  é uma pasta gerencial, é onde o GIT versiona, para ver essa pasta temos que usar um comando/flag específico que é o -a, ela mostra arquivos ocultos;
- O comando git add, adiciona todos os arquivos que estão na pasta selecionada ao GIT Após o comando de git add *, faremos o commit do arquivo, e o comando 
  é git commit -m "" é importante usar um string para referenciar o commit que está realizando, como por exemplo "commit inicial", para referenciar que foi o 
  primeiro commit do arquivo, este comando pode ser com git add + nome do arquivo ou git add * e git add . que adiciona todos os arquivos;
- Ao usar o git init nós criamos de fato um repositório(pasta gerenciável pelo GIT) no GIT;
- Os arquivos gerenciados pelo GIT são Tracked (monitorados) e Untracked (não monitorados), Tracked são arquivos conhecidos pelo GIT e Untracked não;
- Os arquivos Tracked podem ser de 3 tipos diferentes, modified (modificado), unmodified (não modificado) e o staged é um arquivo que saiu de untracked através do
  comando git add e se torna tracked, ele fica aguardando para ser comitado, através do comando git commit -m, para ser tonar um repositório gerenciável pelo GIT
  Então sempre que o arquivo é modificado, ele precisa ser adicionado (git add) e comitado (git commit -m);
- O comando git status, mostra qual o status do arquivo, se está tracked, untracked ou staged;
- Criei uma pasta (musicas), para guardar o arquivo musicas_que_curto, para mover o arquivo para dentro da pasta, usamos o comando mv + o nome do arquivo + ./com o
  nome da pasta que será movido;
- Para "empurrar" um arquivo do GIT local para o servidor, que é o GITHUB que vou usar, temos que adicionar o destino, ou seja, um local no GITHUB que foi criado em novo repositório, o comando utilizado é o git remote add origin + o link que foi criado no GITHUB. Ao efetuar este comando, podemos dar um comando git remote -v, para listar os arquivos remotos que tenho na pasta;
- Para enviar "empurrar" os arquivos para o repositório remoto, o comando é git push origin master, o (origin foi o nome que dei ao arquivo, cada arquivo tem que ter um nome diferente) , para traçar o caminho que o arquivo ficará no GITHUB (ou seja, as ações que fiz conforme tópico anterior);
- Caso sejam feitas alterações no repositório remoto, é preciso baixar esta versão do GITHUB, através do comando git pull + o nome dado (como origin ou origin1) + master.
- Quando o repositório é criado diretamente no GitHub, usamos o comando git clone + colar o link do repositório criado no GitHub;