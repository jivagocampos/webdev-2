# Atividade 01 - Alexsandro Antônio Pohren

## Questões

### 1. Quais são as duas formas de se obter um repositorio git?

- git init: coloca o diretorio atual sobre o controle do git.
- git clone: Faz o clone de um repositorio existente.

### 2.Explique para que serve o comando git status. Use exemplo para complementar a resposta.

- Serve para mostrar o status atual do repositorio, tambem mostra arquivos que foram modificados, adicionados, removidos e/ou estão pendentes de commit.

Exemplo: o estado atual do nosso repositorio

```
$ git commit
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
        modified:   Atividade01/README.md
        deleted:    Banana
        modified:   app.js
        deleted:    ../CONTRIBUTING.md
        deleted:    ../contributing.md

no changes added to commit
```
Este  $ git status indica que o arquivo README.md que esta dentro do repositorio Atividade01 foi modificado e precisa ser comitado

### 3.Levando em consideração commits e branches criados com Git, explique o que representa a imagem abaixo e descreva quais comandos Git foram executados para se obter este estado.

A imagem representa dois branches e seus commits

```
$ git branch iss53
$ git commit -am "resposta da questão 3"
$ it checkout iss53
$ git status
$ git branch
$ git commit -am "vai dar pt"
```

### 4. A imagem a seguir representa um estado posterior à imagem apresentada na questão 3. Explique o que representa a imagem e descreva quais comandos Git foram executados para se obter este estado.

A imagem representa que foi juntado os dois branches usando o merge
```
$ git checkout master
$ git merge iss53
$ git add.
$ git commit -am "Resolvendo conflito entre os branches"
```
### 5. Em que situação acontece um conflito ao executar um merge entre dois branches com Git? E como resolvemos esse conflito? Em sua resposta cite os comandos envolvidos no processo de merge e se julgar necessário represente a situação de forma gráfica, assim como apresentado nas questões 3 e 4.

O conflito acontece quando é feito o merge entre os dois branches e exatamente na mesma linha de um possui alguma coisa no outro, com isso é disparado um conflito, que e resolvido deletando a parte que não precisa ter no codigo ou texto

```
Comandos:

$ git status
$ git merge iss53
$ git status
$ git add .
$ Git commit -m "Resolvendo conflito"

```

### 6. Usando a sintaxe da linguagem JavaScript, crie um objeto com um atributo que tenha um valor do tipo string, um atributo com valor do tipo number e um atributo com valor do tipo array. Atribua este objeto a uma constante.

```
'use strict';

 const foo = {
   chave: 'valor string',
   atributoInt: 50,
   atributoArray:[],
   atributoFunc: function () { }
 };

```
### 7. Usando a sintaxe da linguagem JavaScript, defina uma função que recebe como parâmetro dois valores e que retorna um objeto que armazena os valores recebidos nos atributos a e b. Execute esta função e imprima o resultado no console.

```
function questaosete(valor1, valor2) {
  var objetoDeRetorno ={
  a:valor1,
  b:valor2
};
  return objetoDeRetorno;
}

var valorRetorno = questaosete(5, "seis");
console.log(valorRetorno);

```

### 8. Descreva o funcionamento de um escopo em JavaScript.

O funcionamento do escopo em JavaScript, funciona da sequinte forma, existe o escopo global que pode ser utilizado em qualquer parte do programa e o escopo local que é utilizado apenas  dentro da sua função, mais se esta funcao possui outras funcões, ela pode ser acessada e pode ser manipulada dentro da funcao.

### 9. Veja o código a seguir, descreva o que está acontecendo e,em sua ordem correta,quais informações serão impressas na tela?


resposta
var1 esta recebendo o valor "impresso"
ctrlP esta recebendoo valor [function]
ctrlP passa a receber o nome val, que recebe o valor var1
ctrlP passa a receber o nome imp, que passa a receber a [funcion]
rt possui um valor vazio
imp retorna val que possui o valor { impresso: 'impresso' }
var1 passa a receber o valor "passou aqui"
var1 ira imprimir o valor impresso na tela


```
Ordem de Impressão do codigo

$ undefined
$ "ctrl"
$ "impresso"
$ "passou aqui"
$ { impresso: 'impresso' }

```
### 10. Ao acessar o atributo de um objeto, qual a diferença entre as sintaxes objeto.atributo e objeto[‘atributo’]. Quando deve-se utilizar a segunda opção?

- Não há diferença entre as sintaxes, porém para acessar um atributo que inicia com um numero deve-se usar a sintaxe 'objecto['atributo']'.
