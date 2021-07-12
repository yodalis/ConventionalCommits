# Conventional Commits

Created: July 11, 2021 8:17 PM

Created By: Thais Calazans

# Overview

Por que implementar o conventional commits no time? Isso é realmente necessário?

### O que é o Conventional Commits?

O Conventional Commits é uma convenção no topo das mensagens de commit. Fornece um conjunto fácil de regras para a criação de um histórico de commits explícito, o que facilita a comunicação entre devs em uma aplicação automatizada. 

Se encaixa com o **[SemVer](https://semver.org/)** descrevendo os recursos, correções e alterações importantes feitas nas mensagens de confirmação. 

Informações retiradas da documentação do **Conventional Commits.**

### Por que usar o Conventional Commits?

- Geração de CHANGELOGs automaticamente.
- Maior e melhor comunicação da equipe sobre mudanças realizadas.
- Históricos de commits mais bem estruturados.
- Possibilidade de determinar automaticamente um aumento de versão semântica (com base nos tipos de commits recebidos).

### Estrutura do commit

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(14).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(14).png)

### **Elementos estruturais que compõem seu commit**

**fix :** *um commit do tipo **fix** corrige um bug na sua base de código* (**PATCH** do **[Semantic Versioning](https://semver.org/)**).

**feat :** *um commit do tipo* ***feat** adiciona uma nova feature no seu código **(*MINOR ***no [Semantic Versioning](https://semver.org/)***)**

**BREAKING CHANGE :** *Quando um commit possui um footer com **BREAKING CHANGE**, ou um ! depois do tipo, todas as mudanças a partir daquele commit, começarão a ser incompatíveis com versões anteriores do projeto. Uma **BREAKING CHANGE** pode ser um footer de qualquer tipo de commit.*

**build :** *o commit **build** é usado quando há alguma mudança na parte de desenvolvimento relacionado ao sistema de construção. **Exemplos:** dependências de pacotes, configurações, scripts, etc.*

**ci:** *commits do tipo **ci** são usados quando uma mudança de desenvolvimento que é relacionada a parte de integração contínua e sistema de integração. **Exemplos:** scripts, configurações ou ferramentas.*

**docs :** *o commit **docs** é usado quando há uma alteração na documentação do projeto.*

**refactor :** *o commit **refactor** é usado quando há alterações em desenvolvimento relacionadas à modificação da base de código, que não adiciona um recurso nem corrige um bug, como remover código redundante, simplificar o código, renomear variáveis, etc.*

### Exemplos

### **Utilizando feat e BREAKING CHANGE no footer**

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(13).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(13).png)

### Utilizando ! para redobrar a atenção no BREAKING CHANGE

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(12).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(12).png)

### Utilizando ! e BREAKING CHANGE no footer

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(11).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(11).png)

### **Commit sem corpo**

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(10).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(10).png)

### Commit com escopo

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(9).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(9).png)

### Commit com múltiplos parágrafos no corpo e múltiplos footers

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(8).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(8).png)

# Projetos que utilizam Conventional Commits

Aqui estão alguns projetos famosos que utilizam a padronização do Conventional Commits.

- **Jenkins X :** Jenkins X fornece automação de pipeline, GitOps integrado e ambientes de visualização para ajudar as equipes a colaborar e acelerar a entrega de software em qualquer escala.
- **electron :** Tecnologia usada para criação de aplicativos de plataforma cruzada para desktop com JavaScript, HTML e CSS.
- **Angular :** Framework baseado em Typescript, voltado principalmente para o desenvolvimento web e que por coincidência também inspirou a criação do Conventional Commits.

## Husky & CommitLint

### **CommitLint**

O CommitLint é uma biblioteca do Javascript que verifica se o seu commit segue as regras do Conventional Commits, com todas as regras e padronizações exigidas.

PS. Não se preocupe, o CommitLint existe para vários tipos de linguagens de programação, então você não fica preso ao JS. Legal,né? :)

### **Husky**

Já o Husky é também uma biblioteca do JS que nos permite usar Git Hooks em nossos commits.

Git Hooks? Sim! Git Hooks é uma funcionalidade que nos permite executar scripts personalizados antes de uma ação definitiva, como um push ou um commit.

O Husky e o CommitLint em conjunto irão verificar se os nossos commits seguem os padrões requiridos no arquivo de configuração do CommitLint antes de subir o commit.

Então vamos instalar? **Bora lá! 😉**

## **Instalando o CommitLint**

Vamos instalar o CommitLint e seu CLI no seu repositório. 

E não esqueça de deixá-lo como uma dependência de desenvolvimento, ok?

**Vamo lá!**

### **Windows/**Mac/Linux

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(7).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(7).png)

**Após a instalação, você precisará configurar o CommitLint para seguir as regras do Conventional Commits.**

Você deverá criar um arquivo chamado commitlint.config.js, onde será setado as regras de acordo com o padrão que você deseja seguir. 

Como este:

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(6).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(6).png)

Ps. Segundo o artigo 'Improve your commits with Conventional Commits' escrito pelo Gabriel Nascimento Costa, você pode usar a própria CLI do CommitLint para verificar os seus commits, mas nesse caso iremos fazer essa integração com o Husky.

## **Instalando o Husky**

Como padrão vamos instalar o Husky como dependência de desenvolvimento assim como o CommitLint, então bora lá no terminal e digita isso aí ;)

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(5).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(5).png)

Ativando o Git Hooks...

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(4).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(4).png)

Adicionando o commit-msg hook:

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(3).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(3).png)

Fácil, né?

Agora no arquivo **commit-msg**  adicione esses comandos:

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(1).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(1).png)

E tá pronto o sorvetinho!

## 1,2,3 testando... 🤓

Agora para testarmos, vamos adicionar um commit sem seguir os padrões ConventionalCommits, esse foi o nosso resultado:

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(2).png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon_(2).png)

Agora um certo!

![Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon.png](Conventional%20Commits%20bd0392b786874e759ddb68a3dd474cbd/carbon.png)

### Referências

Antes de tudo, quero agradecer a esses gênios que me auxiliaram em toda a construção desse artigo e que eu espero que cada pessoa que tire um tempinho para ler o meu artigo, tire um tempo pra ler o deles também, obrigada amigos!

- [**How to lint Git commit messages](https://remarkablemark.org/blog/2019/05/29/git-husky-commitlint/#test) - [https://remarkablemark.org/](https://remarkablemark.org/)**
- [**Improve your commits with Conventional Commits](https://medium.com/linkapi-solutions/improve-your-commits-with-conventional-commits-72134a852d19) - Gabriel Nascimento Costa**
- Conventional Commits Documentation - **[https://www.conventionalcommits.org/en/v1.0.0/](https://www.conventionalcommits.org/en/v1.0.0/)**

**Espero que não tenha esquecido ninguém, obrigada amigos, bom divertimento! 🤓**