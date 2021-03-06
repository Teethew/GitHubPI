# Usando Git e GitHub (básico) <!--GIT--><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Git_icon.svg/1024px-Git_icon.svg.png" width="30" height="30"> <img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg" width="30" height="30">

>Inspirado no lendário .txt do [Daniel Cardoso](https://github.com/daniel-cardoso) e complementado pelo esclarecedor guia do [Roger Dudler](https://github.com/rogerdudler)

# Glossário 📖  

### Os principais termos abordados serão:

- [Repositórios](https://github.com/Teethew/GitHubPI/blob/master/README.md#reposit%C3%B3rios)
- [Git bash](https://github.com/Teethew/GitHubPI/blob/master/README.md#git-bash)
- [Branches](https://github.com/Teethew/GitHubPI/blob/master/README.md#branches)
- [Comandos do Git](https://github.com/Teethew/GitHubPI/blob/master/README.md#comandos-do-git)

## Repositórios

Os repositórios são onde estão armazenados os arquivos de cada projeto do GitHub, eles podem parecer meio confusos no começo mas aos poucos vai ficando mais fácil de entendê-los.
Cada repositório geralmente conta com um arquivo chamado **_README.md_**, que funciona como um arquivo de texto com formatação _Markdown_ que pode ser usado de inúmeras formas e por diversas razões, mas as mais comuns são:
- Descrever um projeto, desde sua utilidade até sobre as melhores formas de implementação
- Dar informações sobre o andamento do projeto
- Listar regras para as pessoas que desejam colaborar para o projeto

###### Nota:  no futuro, eu pretendo detalhar melhor as funcionalidades de um repositório no GitHub, mas por enquanto isso já é o suficiente para quem está atrás do básico.

##  _Git bash_
É  como um terminal do Git, basicamente o lugar onde você executa linhas de comandos para fazer alterações tanto no seu repositório local quanto _commits_, criações de novas _branches_ e _pushes_.

Para iniciar o _**bash**_ em alguma pasta do seu computador você pode simplesmente clicar com o lado direito do mouse e escolher a opção de **_Git Bash here_** ou "iniciar Git bash aqui", se você preferir.

![Abrindo o Git bash na pasta desejada](https://github.com/Teethew/GitHubPI/blob/master/img/git%20bash%20here.png?raw=true)
>Abrindo o Git bash na pasta desejada

Dentro do bash, você pode não só executar comandos relacionados ao Git em si, como também comando básicos de manipulação de arquivos e diretórios, como:

- `cd pastaDestino` - _cd_ ou _change directory_ (mudar diretório) é um comando para mudar o local onde os comandos do bash serão executados. Exemplos de uso:
```
cd ../pastaAtual/pastaDestino/projeto
```
> ./ antes refere-se à pasta atual e . ./ antes refere-se à uma pasta acima da atual

- `dir` - *dir* ou *directory* exibe os diretórios no local

- `mkdir nomeDaPasta` - _mkdir_ ou _make directory_ (criar diretório) cria uma pasta com o nome escolhido no local.  
- `rm nomeDoArquivo` - _rm_ ou _remove_ exclui um arquivo da sua escolha
- `rmdir nomeDaPasta` - _rmdir_ ou _remove directory_ (remover diretório) exclui a pasta escolhida do local

![comandos de movimentação de arquivos e diretórios no bash](https://github.com/Teethew/GitHubPI/blob/master/img/cd%20bash.png?raw=true)
>Exemplo dos comandos sendo executados no terminal do Linux (aposto que você notou a semelhança com o Git Bash no Windows).

Nessa imagem eu naveguei até uma pasta na minha área de trabalho chamada GitHub com o `cd`, listei os diretórios usando `dir`, fiz uma nova pasta chamada teste usando `mkdir teste` e depois a removi usando `rmdir teste` .

## _Branches_
O conceito de branches durante o desenvolvimento de um projeto pode ser entendido como uma ramificação em uma **linha do tempo**, onde existe a linha **principal** que costuma ser chamada de _**master**_ e suas respectivas **divisões** ou ramificações (branches) que tem por objetivo final enviar alterações feitas separadamente para a linha principal (master).
Esse recurso possibilita que várias pessoas colaborem em um mesmo projeto de diversos locais do mundo inteiro como uma "equipe", cada uma fazendo pequenas alterações que somadas trazem uma evolução gigantesca para o projeto como um todo.
![Exemplificação do conceito de branches](https://github.com/Teethew/GitHubPI/blob/master/img/Diagrama%20de%20Branches.png?raw=true)
>Conceito de branches aplicado à uma linha do tempo. (Fonte: draw.io)
 
## Comandos do Git

## `git checkout`
Muda para outra **branch**. Deve ser utilizado junto com um **-b** (build) à direita quando se pretende **criar uma branch nova**.
```
git checkout -b branchNova
```
## `git clone`
"Clona" ou faz o download dos arquivos contidos no repositório **remoto** para o seu repositório **local** (que fica na sua máquina).
```
git clone https://github.com/usuario/repositorio
```
## `git commit`
Envia e comenta suas alterações para o _HEAD_, local de onde serão enviadas para o repositório **remoto** (que fica no seu GitHub) através de um push.
```
git commit -m "comentario sobre alterações feitas"
```
## `git init`
Inicializa um repositório **local** na pasta **atual** (vale lembrar que é necessário associar um repositório do GitHub ao repositório local para fazer seus pushes).
## `git merge`
**Faz uma junção** entre os arquivos situados na **branch atual** com os da **branch de destino** (normalmente a **master**).
## `git pull`
Atualiza seu repositório **local** com os arquivos que estão no repositório **remoto** (é bem comum ter que realizar um **pull** para enviar suas alterações para uma branch se seu repositório **local** não estiver atualizado (ou _up to date_).
## `git push`
Envia as alterações commitadas para o repositório **remoto**, na branch desejada.
É importante lembrar que antes de realizar um push para um branch que ainda não está no GitHub, você primeiro precisa "publicar" ela, através do seguinte comando:
```
git push -u origin suaBranch
```
Neste caso o **-u** equivale a `--set-upstream`.
## `git status`
Exibe os arquivos prontos para um **push** e os que ainda não foram adicionados ou commitados.

## Inicializando nosso repositório
### Pra isso, existem duas formas de se realizar esse procedimento:
- `git init`
- `git clone`









> Written with [StackEdit](https://stackedit.io/).
