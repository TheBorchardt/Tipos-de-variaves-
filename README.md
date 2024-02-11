<br>

> [!NOTE] Alguns pontos antes de entender
> Escopo: O código que estiver com indentação, ou seja que tenha um espaçamento no começo, é um Escopo.
> 
> Bloco: O código que estiver entre chaves `{}`, é um bloco.
> 
> Output: quando tiver `Output` comentado, é a saída pois não consegui o plugin de executar aqui nesse arquivo ent fds.



<br>

# Tipos

### Em Javascript temos 3 formas de declarar uma variável, sendo elas:
<br>

# `var`
#### O tipo de variável `var` é chamada de "variável de escopo de função" ou "variável de escopo global". 

#### É um tipo de variável que como nome sugere, ao definir ela em qualquer lugar, seja em um loop ou estrutura condicional, ainda será acessível em outro local do código. 

```js:main.js
function exemplo(){
	if (true){
		var pika = "hello world";
	}
	var pika2 = "hello world";

	console.log(pika) // output: hello world
}

console.log(pika) // output: hello world
console.log(pika2) // output: hello world

```

#### Por isso do nome "variável de escopo global", pois pode ser acessada globalmente.

<br>

# `let`

#### Já a variável `let` é do tipo de escopo "bloco", ou seja, só funcionará dentro de um bloco.

#### obs: As chaves `{}` são os blocos, o que estiver dentro das chaves, está dentro de um bloco.

```js:main.js
function exemplo(){
	if (true){
		let pika = "hello world";
	}
	let pika2 = "hello world";

	console.log(pika) 
	// output: error: pika is not defined.
	
	console.log(pika2) // output: hello world 
}

console.log(pika) 
// output: error: pika is not defined.

console.log(pika2) 
// output: error: pika2 is not defined.
```

#### Esse exemplo mostra que a variável pika e pika2 do tipo `let` estão dentro de blocos diferentes, portanto para que o `console.log()` funcione, ele precisa estar dentro do mesmo bloco `{}`, caso contrário não vai retornar erro.

<br>

# `const`

#### Esse tipo de variável é usado para declarar valores que não serão alterados, ou seja, ao declarar ela, não poderá atribuir outro valor depois.

```js:main.js
const penis = "bct"

penis = "pika"
// Output: error: Assignment to const variable
// Erro: Atribuição a uma variável constante

```
<br>

# Escopo Global 

#### O escopo Global é o escopo onde, independentemente do tipo, `var`, `let` ou `const`, sempre será acessível, em qualquer lugar do código.

```js:main.js
// Este é o escopo global 

let pika1 = "messiano";
const pika2 = "cristialdo";

// Qualquer variável declarada aqui poderá ser chamada em qualquer lugar.

function exemplo(){
	if (true){
		console.log(pika1, pika2)
		// Output: messiano, cristialdo
	}
	console.log(pika1, pika2)
	// Output: messiano, cristialdo
	
}

console.log(pika1, pika2)
// Output: messiano, cristialdo

```

#### Portanto se você colocar a variável no começo do código, sem estar dentro de qualquer escopo ou bloco, essa variável é chamada de variável global.
