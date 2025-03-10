# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como `` esta aqui com `  `` ou

````javascript
//esta aqui com ```
let a = "olá";
let b = 10;
print(a);
````

- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove.

# Questões objetivas

**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**

```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```

a) A saída será undefined seguido de erro [X]

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

Solução: A variável `x` é declarada com `var`, o que faz com que ela seja elevada para o topo do escopo, mas não inicializada. Portanto, a primeira saída será `undefined`. A variável `y` é declarada com `let`, o que não permite a elevação da variável para o topo do escopo, e por isso a segunda saída gera um erro.

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
  if (a || b === 0) {
    return "Erro: número inválido";
  }
  return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0) [X]

Solução: Uma resposta completa a esse problema requer mais contexto sobre o escopo em que a função está inserida. Caso a soma utilizando o número zero for algo inválido no escopo do que se está querendo alcançar, a verificação `if (a || b === 0)` deve ser substituída por `if (a === 0 || b === 0)`. Porém, tomando como escopo a consideração de que a função soma possui apenas como objetivo somar dois números, o ato de somar o número zero não trás nenhum caso de número inválido, assim tornando a remoção completa do `if` a melhor opção.

---

**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**

```javascript
function calcularPreco(tipo) {
  let preco;

  switch (tipo) {
    case "eletrônico":
      preco = 1000;
    case "vestuário":
      preco = 200;
      break;
    case "alimento":
      preco = 50;
      break;
    default:
      preco = 0;
  }

  return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200. [X]

c) O código imprime 50.

d) O código gera um erro.

Solucão: O código imprime 200. O erro está na falta de `break` após o `case "eletrônico"`. Sem o `break`, o código continua a execução e atribui o valor 200 à variável `preco`, que é o valor do `case "vestuário"`. O `break` é necessário para interromper a execução do `switch` após a atribuição correta do valor.

---

**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**

```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros
  .map((x) => x * 2)
  .filter((x) => x > 5)
  .reduce((a, b) => a + b, 0);

console.log(resultado);
```

a) 0

b) 6

c) 18

d) 24 [X]

Solução: O código acima utiliza os métodos `map`, `filter` e `reduce` para transformar, filtrar e reduzir os elementos do array `numeros`. Primeiramente, o método `map` multiplica cada elemento por 2, resultando em `[2, 4, 6, 8, 10]`. Em seguida, o método `filter` filtra os elementos maiores que 5, resultando em `[6, 8, 10]`. Por fim, o método `reduce` soma os elementos do array resultante, resultando em 24.

---

**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"] [X]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

Solucão: O método `splice` remove elementos de um array e, se necessário, adiciona novos elementos no lugar dos removidos. No código acima, o método `splice(1, 2, "abacaxi", "manga")` remove os elementos "maçã" e "uva" (a partir do índice 1, removendo 2 elementos) e adiciona "abacaxi" e "manga" no lugar. Portanto, o array resultante será `["banana", "abacaxi", "manga", "laranja"]`.

---

**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.

a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira. [X]

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

Solução: A primeira afirmação é verdadeira. A herança em JavaScript é utilizada para compartilhar métodos e propriedades entre classes, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código. A segunda afirmação também é verdadeira. Em JavaScript, a herança é implementada através da palavra-chave `extends`, que permite que uma classe filha herde de uma classe pai.

Sobre a justificativa, a alternativa correta é discutível. Olhando para a definição da palavra justificar, que é "Demonstrar, provar, tornar legítimo, verdadeiro; dar razão a;", a palavra `extends` não justifica a primeira afirmação, a palavra por si só não demonstra o conceito ou o torna verdadeiro, é apenas uma palavra-chave que implementa a funcionalidade de herança e remete a ideia de extensão.

---

**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```

I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras. [X]

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

Solucão: A alternativa correta é a letra `a`. A afirmação I é verdadeira, pois a classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente. A afirmação II também é verdadeira, pois o método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`. A afirmação III é falsa, pois o código funciona corretamente e Funcionario pode herdar de Pessoa como uma classe em JavaScript.

---

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

Solucão: A alternativa correta é a letra `b`. A asserção é verdadeira, pois o conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes. No entanto, a razão é falsa, pois em JavaScript, o polimorfismo não é implementado utilizando o método de sobrecarga de métodos em uma classe. Em JavaScript, o polimorfismo é implementado através da capacidade de um objeto de uma classe filha substituir um método de uma classe pai, permitindo que diferentes objetos respondam à mesma mensagem de maneiras diferentes.

---

# Questões dissertativas

9. O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {
  for (i = 0; i < numeros.size; i++) {
    soma = 2 * numeros[i];
  }
  return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

```javascript
function somaArray(numeros) {
  // Declara e inicializa a variável 'soma' com 0 para acumular o resultado
  let soma = 0;

  // Usa 'let' para declarar 'i' no escopo do loop e corrige 'size' para 'length'
  for (let i = 0; i < numeros.length; i++) {
    // Incrementa 'soma' com o dobro do elemento atual, em vez de sobrescrevê-la
    soma += 2 * numeros[i];
  }

  // Retorna o valor acumulado da soma
  return soma;
}

// Testa a função com o array [1, 2, 3, 4], que deve retornar 20 (2*1 + 2*2 + 2*3 + 2*4)
console.log(somaArray([1, 2, 3, 4])); // Saída: 20
```

---

10. Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

```javascript
// Classe base Produto
class Produto {
  constructor(nome, preco) {
    this.nome = nome; // Atributo para o nome do produto
    this.preco = preco; // Atributo para o preço do produto
  }

  // Método para calcular desconto fixo de 10%
  calcularDesconto() {
    const desconto = this.preco * 0.1; // 10% do preço
    return this.preco - desconto; // Retorna o preço com desconto
  }
}

// Classe Livro que herda de Produto
class Livro extends Produto {
  constructor(nome, preco) {
    super(nome, preco); // Chama o construtor da classe pai para inicializar nome e preco
  }

  // Sobrescreve o método calcularDesconto para aplicar 20% de desconto
  calcularDesconto() {
    const desconto = this.preco * 0.2; // 20% do preço
    return this.preco - desconto; // Retorna o preço com desconto
  }
}

// Testando as classes
const produtoGenerico = new Produto("Caneta", 10);
console.log(`Produto: ${produtoGenerico.nome}`);
console.log(`Preço com desconto: R$ ${produtoGenerico.calcularDesconto()}`); // 10% de desconto

const livro = new Livro("JavaScript Básico", 50);
console.log(`Livro: ${livro.nome}`);
console.log(`Preço com desconto: R$ ${livro.calcularDesconto()}`); // 20% de desconto
```

A herança nesse contexto permite que a classe `Livro` herde os atributos e métodos da classe `Produto`, evitando a repetição de código. Ao chamar `super(nome, preco)` no construtor da classe `Livro`, os atributos `nome` e `preco` são inicializados pela classe pai `Produto`. A modificação do método `calcularDesconto()` na classe `Livro` é feita sobrescrevendo o método original da classe `Produto`, permitindo que a classe `Livro` aplique um desconto de 20% em vez de 10%.
