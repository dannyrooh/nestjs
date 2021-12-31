#Introdução ao NestJS
<hr>

##Requisitos

* [Node] <https://nodejs.org/pt-br/download/>
* NPM
* [Git] <https://git-scm.com/download/win>
* [VSCode] <https://code.visualstudio.com/download>


##Criando o projeto no Github

Entre no seu gibhub, e faça a criação de um novo repositório.

<https://docs.github.com/pt/repositories/creating-and-managing-repositories/creating-a-new-repository>


Este projeto deve ser criado como **public**, nome de **nestjs**. Em ***Initialize this repository with:*** marque as opções :
  * Add a README file
  * Add .gitignore  (.gitignore template: Node) 


##Clonando o repositório

O próximo passo é clonar o repositório do git na sua máquina,
para isso abra o cmd do windows, powerShel ou VSCode.
Se preferir o VSCode, execute os comandos a partir do terminal integrado, antes, abra um folder, (file/open folder), e  o terminal integrado (Terminal / New Terminal  (ctrl + shift + ')). 

No github, vá para o botão clone, na aba HTTPS, copie o link do seu projeto para clonar

~~~
git clone https://github.com/dannyrooh/nestjs.git
cd ./nestjs
git status
~~~

##🚀Criando o primeiro projeto  em NestJS

No terminal execute
~~~
npm i -g @nestjs/cli
nest new 1.hello-world
~~~

**caso você receba a mensagem de erro:**
~~~
nest : O arquivo C:\Users\...\AppData\Roaming\npm\nest.ps1 não pode ser carregado porque a execução de scripts foi desabilitada neste sistema. Para obter mais informações, 
consulte about_Execution_Policies em https://go.microsoft.com/fwlink/?LinkID=135170.
No linha:1 caractere:1
+ nest --version
+ 
    + CategoryInfo          : ErrodeSegurança: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
~~~

execute o seguinte comando no terminal, para habilitar a permissão de execução de script para o usuário corrente

~~~
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
nest new 1.hello-world
~~~

## configurando o git na máquina local

Vamos atualizar o projeto no git, para isso vamos voltar para o diretório do projeto 

>**Obs**: *caso você ainda não tenha configurado os dados para enviar os arquivos para o GitHub, execute os comandos abaixo.*
>
>*Não esqueca de mudar para o **seu nome** e **seu email** da conta criada no GitHub*

~~~
git config --global user.name "SEU NOME"
git config --global user.email "SEU@EMAIL.COM"
~~~

Agora vamos gerar uma chave ssh para quando for feito o upload não seja necessário ficar informando usuário e senha 

~~~
ssh-keygen -t rsa -C "SEU@EMAIL.COM" -b 4096
~~~

Caso não tenha o ssh, instalado você deve instalar. Ao rodar o comando ele solicitará o arquivo e uma frase para identificação, eu deixei o padrão e cliquei enter 

Será mostrado onde foi gerada a sua chave rsa, abra este arquivo para obter o rsa

~~~
Your public key has been saved in C:\Users\[SEU DIRETORIO]/.ssh/id_rsa.pub.
~~~

Para ver o conteúdo da chave, execute
~~~
type C:\Users\[SEU DIRETORIO]/.ssh/id_rsa.pub
~~~

No projeto no github, vá no menu Settings, e no lado esquerdo em Deploy keys, clique no botão Add deploy key. Informe um título, copie a chave gerada e salve. Com essa chave informada, quando você fizer um push, ele não pedirá mais a senha


## Fazendo o primeiro push

Vamos para o diretório raiz  "/nestjs" para adicionar o diretorio criado para o primeiro exemplo *1.hello-world*

~~~
git add .
git commit -m "criado hello-world"
git push origin main
~~~

 
## Executando o hello-world

No terminal, vá para o diretório e execute 

~~~
cd .\1.hello-world\
npm run start
~~~

###Abra seu browse e navegue para

**http://localhost:3000/**



>[NestJS](https://docs.nestjs.com)
>
>documentação: <https://docs.nestjs.com>










