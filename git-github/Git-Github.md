# Aprendizado sobre o Git e Github



​	:star: Controle de versão

​	:star: Armazenamento em nuvem

​	:star: Trabalho em equipe

​	:star: Melhora de código 

​	:star: Reconhecimento



## Comandos para o Git :comet:



​	:small_blue_diamond: **dir** - abrir todas as pastas do local

​	:small_blue_diamond: **cd** - navegar para um local específico

​	:small_blue_diamond:**cd ..** - retroceder 

​	:small_blue_diamond:**ctrl + l** - limpar o terminal

​	:small_blue_diamond:**tab** - reconhece algo

​	:small_blue_diamond:**mkdir** - criar uma pasta

​	:small_blue_diamond: **echo** - para escrever algo ou criar uma documento de texto (echo > hello.txt)

​	:small_blue_diamond: **delete** - deleta o conteúdo **não deleta o repositório**

​	:small_blue_diamond:**rmdir** - exlcui o repositório.



## SHA1 - O que é e como funciona :desktop_computer:





**SHA1** é um modo de encriptação projetada pela Agência de Segurança Nacional dos Estados Unidos. O **SHA1** implementa um algoritmo de hash sem chave, que pega uma mensagem de até 264 bits e produz um resumo da mensagem de 160-bits e assim é utilizado para a verificação de integridade da mensagem. Ele é baseado nos princípios de projeto dos algoritmos de hash MD4 e MD5.



## Blob, Trees and Commits :information_source:



![Git Object Model | Online Video Tutorial by thoughtbot](https://thoughtbot-images.s3.amazonaws.com/upcase/git-course/git-base-object-model.png)

## Chave SSH :key:



O objetivo da chave SSH é permitir que desenvolvedores ou outros usuários realizem alterações em sites e servidores utilizando uma  <font color="green">conexão simples e segura</font>.



#### Como criar uma chave SSH 



:one: **Primeiro execute o seguinte comando:**



``  ssh-keygen - C "seu-email"  `` (Neste exemplo o tipo da criptografia será atribuída automaticamente, por padrão o tipo RSA)

 ou 

``ssh-keygen -t ed25519 -C "seu-email"`` (Neste exemplo usa o parâmetro -t para especificar o tipo da criptografia que nesse caso é ed255190.

A chave pública e privada será gerada dentro da pasta oculta .ssh que por padrão estará alocada dentro da sua pasta pessoal,  no diretório home (Linux) ou Users (Windows).

:label: **Exemplo:** Caso utilize o Windows, sua chave será criada no diretório  /c/Users/seu-nome-de-usuário, a pasta oculta será encontrada lá. Caso utilize o Linux, sua chave será criada no diretório  /home/seu-nome-de-usuário, a pasta oculta será encontrada lá.

:bulb: **Dica:** Você pode consultar o caminho atual utilizando o comando pwd

A chave SSH foi criada, agora você precisa inicializar o agente.



:two: **Inicializando o agente:** 



Primeiro você irá navegar até o diretório .ssh, utilizando o comando cd /especifique Caminho

Estando no diretório irá executar o seguinte comando: 

``eval $(ssh-agent -s)``

O agente foi criado, agora é necessário atribuir a chave ao agente. 



:three: **Atribuindo a chave ao agente**



Do diretório .ssh, execute o comando ``ls`` para listar o arquivo das chaves públicas e privadas.

Caso tiver criado com o tipo RSA, os arquivos apareceram como id_rsa e id_rsa.pub 

Caso tiver criado com o tipo ed25519, os arquivos apareceram como id_ed25519 e id_ed25519.pub



Execute o comando: 

``ssh-add id_rsa`` (no caso do tipo RSA)

ou

``ssh-add id_ed25519`` (no caso do tipo ed25519)
