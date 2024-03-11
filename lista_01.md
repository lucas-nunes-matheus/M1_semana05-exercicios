# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

<mark> a) Imprime os números pares de 1 a 10. </mark>


b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

<mark>A) let carro = new Carro("Toyota");</mark>

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

<mark>A) 18

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

<mark>A) ![Uma imagem](assets/ex04_1.PNG)

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

<mark>A) ![Uma imagem](assets/ex05_1.PNG)

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

<mark>A) "Olá, meu nome é João. Olá, meu nome é Maria."

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

*Resposta*:
```javascript
class Animal {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  descrever(){
    console.log(`Exemplo de animal: ${this.nome} com ${this.idade} anos de idade.`)
  }
}

var cachorro = new Animal("cachorro", 8);
var gato = new Animal("gato", 3);

cachorro.descrever();
gato.descrever();
```
______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

*Resposta:*
```javascript
// Definição da classe Animal
class Animal {
  // Método construtor da classe, recebe nome e idade como parâmetros
  constructor(nome, idade) {
    // Atribui o nome recebido ao atributo nome do objeto atual
    this.nome = nome;
    // Atribui a idade recebida ao atributo idade do objeto atual
    this.idade = idade;
  }

  // Método descrever, imprime uma mensagem descrevendo o animal
  descrever() {
    // Imprime uma mensagem com o nome e a idade do animal
    console.log(`Exemplo de animal: ${this.nome} com ${this.idade} anos de idade.`);
  }
}

// Definição da classe Gato, que estende a classe Animal
class Gato extends Animal {
  // Método construtor da classe, recebe nome, idade e cor como parâmetros
  constructor(nome, idade, cor){
    // Chama o construtor da classe pai (Animal) com nome e idade
    super(nome, idade);
    // Atribui a cor recebida ao atributo cor do objeto atual (gato)
    this.cor = cor;
  }
  
  // Método miar, imprime o som característico de um gato
  miar() {
    // Imprime "Miaaau!"
    console.log("Miaaau!")
  }
}

// Cria uma instância da classe Animal com nome "cachorro" e idade 6, atribuindo à variável cachorro
var cachorro = new Animal("cachorro", 6);
// Cria uma instância da classe Gato com nome "gato", idade 4 e cor "preto", atribuindo à variável gato
var gato = new Gato("gato", 4, "preto");

// Chama o método descrever do objeto cachorro, que imprime uma mensagem descrevendo o cachorro
cachorro.descrever();
// Chama o método descrever do objeto gato, que imprime uma mensagem descrevendo o gato
gato.descrever();
// Chama o método miar do objeto gato, que imprime o som característico de um gato
gato.miar();

```
______

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

*Resposta:*
``` javascript
// Definição da classe SomadorDeNotas
class SomadorDeNotas {
  // Método construtor da classe, é chamado quando uma nova instância da classe é criada
  constructor(){
    // Inicializa o atributo total com o valor zero
    this.total = 0;
  }

  // Método para adicionar uma nota ao total
  adicionarNota(nota){
    // Soma a nota ao total existente
    this.total += nota;
  }

  // Método para exibir o total das notas
  verTotal(){
    // Imprime uma mensagem com o total das notas
    console.log(`A soma total das notas é: ${this.total}`);
  }
}

// Cria uma nova instância da classe SomadorDeNotas e atribui à variável somador
var somador = new SomadorDeNotas();

// Adiciona algumas notas ao somador
somador.adicionarNota(9.0);
somador.adicionarNota(4.0);
somador.adicionarNota(6.5);

// Exibe o total das notas
somador.verTotal();




```
______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

*Resposta:*
``` javascript
// Criando classe "Funcionario" com informações essenciais do colaborador
class Funcionario{
  constructor(nome, idade, salarioBase){
    // Cada objeto da classe terá os atributos "nome", "idade" e "salarioBase", fornecidos pelo usuário
    this.nome = nome;
    this.idade = idade;
    this.salarioBase = salarioBase;
  }

  // Declarando função de calcular salário: "Vazia, pois cada funcionário terá o salário calculado diferentemente"
  calcularSalario(){}
}


// Criando classe "Professor", que herda atributos e métodos da classe pai "Funcionario"
class Professor extends Funcionario{
  constructor(nome, idade, salarioBase, disciplina, horasDeAulaSemana){
    // "super" acessa as propriedades "nome", "idade" e "salarioBase" da classe pai "Funcionario"
    super(nome, idade, salarioBase);
    this.disciplina = disciplina;
    this.horasDeAulaSemana = horasDeAulaSemana;
  }

  // Declarando função calcularSalario() para objetos da classe "Professor", a partir do atributo "horasDeAulaSemana" e do parâmetro "valorHoraAula"
  calcularSalario(valorHoraAula){
    this.salarioBase = this.horasDeAulaSemana*valorHoraAula;
    // Impressão do nome e do salário do professor
    console.log(`O salário de ${this.nome} é: ${this.salarioBase}.`)
  }
}


// Criando dois objetos da classe "Professor": Lucas e Alessandra
var Lucas = new Professor("Lucas", 27, 1320, "Comunicação Não-Violenta", 18);
var Alessandra = new Professor("Alessandra", 33, 1320, "Empreendedorismo", 30)

// Chamando as funções calcularSalario() para os professores "Lucas" e "Alessandra", com parâmetro "valorHoraAula = 200"  
Lucas.calcularSalario(200);
Alessandra.calcularSalario(200);

```