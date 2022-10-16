# Desafio de Projeto sobre Git e GitHub da DIO :book:

Repositório criado para p desafio de projeto

##  Introdução ao Git e GitHub

1. Comando básicos para um bom desempenho no terminal
2. Objetos do GIT
3. Chaves SSH e Tokens
4. Primeiros comandos com o GIT
5. Resolvendo conflitos



1. **Comandos:**

dir - visualiza todos os diretórios no Windows e ls para o Linux

cd/ +nome do diretório - para navegar entre as pastas

cd .. - para voltar

cls - para limpar o terminal no Windows e ctrl+l no Linux

mkdir +nome da pasta - para criar uma pasta

echo > +nome do arquivo-  para criar um arquivo

del +nome da pasta - deleta o arquivo dentro da pasta informada

rmdir +nome da pasta /s /q - deleta o diretório informado

pwd - mostra o caminho completo da pasta



**SHA1** - Significa Secure Hash Algorithm (Algoritmo de Hash Seguro) - faz a encriptação do arquivo - gera um conjunto de caracteres de 40 dígitos identificando os arquivos de forma segura e rápida. 

2. **Objetos**

***Blob***- tipo de objeto que armazena o conteúdo de cada arquivo em um repositório. Contém metadados do objeto como tipo, tamanho, entre outros. *Blobs* não armazenam o nome do arquivo. Gera uma SHA1.

***Tree***- armazena as *Blobs*, nome do arquivo, pode apontar para outras *Tree* e gera um SHA1 também.

***Commit***- o commit junta tudo (aponta para *Tree*, *Blob*, parente, autor, mensagem)- é um objeto do Git que dá significado para as alterações, e também gera um SHA1.

Se algo é alterado no arquivo, altera o SHA1 da *Blob* que por sua vez altera o SHA1 da *Tree*, que altera o SHA1 do *Commit*, ou seja, gera uma reação em cadeia.

3. **Chaves SSH** 

A Chave SSH é uma forma de estabelecer uma conexão segura encriptada entre duas máquinas (local e o Servidor do GitHub).

Para clonar um repositório do GitHub remoto para o computador local, deve-se selecionar o caminho SSH ao invés do HTTPS que aparece no início e para isso devemos criar uma senha SSH.

4. **Primeiros comandos com o GIT**

Nota: Todo comando GIT leva o nome git na frente.

Exemplo:

git init - cria um repositório;

git status - monitora o status do arquivo;

git add +nome do arquivo- adiciona a alteração  no arquivo

git add * ou git add . - adiciona todas as alterações dos arquivos

git remote add origin +endereço do repositório remoto - adiciona o repositório local no remoto

git commit -m "nome da alteração" - fazer um commit

git push origin master - subir as alterações no gitHub remoto

git clone +endereço do repositório

git remote -v mostra os repositórios remoto

5. **Resolvendo conflitos**

O conflito ocorre por conta de alterações simultâneas, onde um arquivo está em versão diferente do outro (duas pessoas mexendo no código ao mesmo tempo). 

Quando ocorre o conflito, é necessário fazer um pull (puxar o arquivo mais atualizado) para atualizar antes de subir o novo commit.

Ex: git pull origin master 

e depois sobe faz o commit git push origin master

