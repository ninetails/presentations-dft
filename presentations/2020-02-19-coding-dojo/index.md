---
title: Guildas
theme: night
revealOptions:
  transition: 'slide'
---

# Coding Dojo

---

![Dojo](https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/Noma_Dojo%2C_2006.JPG/800px-Noma_Dojo%2C_2006.JPG)

----

> Dojo é o local onde se treinam artes marciais japonesas.

---

> Lugar de iluminação

----

![namaste](https://cdn.pixabay.com/photo/2016/12/28/11/32/namaste-1935938_960_720.jpg)

---

## Formatos

---

### Kata

----

> Alguém apresenta uma solução pronta previamente desenvolvida e que utilizou algum tipo de teste

---

### Randori

----

![howto](https://image.slidesharecdn.com/codingdojo-111117160908-phpapp02/95/coding-dojo-35-728.jpg?cb=1321546270)

----

- Depois dos 5 minutos só passa a vez se estiver <span style="color:green;font-weight:bold;">VERDE</span>
<li class="fragment">Platéia não fala com os coders enquanto estiver <span style="color:red;font-weight:bold;">VERMELHO</span></li>
<li class="fragment"><small>Ou seja, por favor, falem entre si porém baixo.</small></li>

----

- Não tragam problemas de fora
- É um local de treinamento 🙏<!-- .element: class="fragment" -->
- Não necessariamente precisa ser na linguagem que todos estão acostumados<!-- .element: class="fragment" -->
- Inclusivo<!-- .element: class="fragment" -->

---

## Agenda

- Apresentação de 1 a 2 Katas
- Restante do tempo focar no Randori<!-- .element: class="fragment" -->
- Retrospectiva<!-- .element: class="fragment" -->

----

- Não se preocupe em terminar o problema
- Estamos todos para treinar... DOJO<!-- .element: class="fragment" -->
<li class="fragment"><strong>"Não importa o destino e sim a jornada"</strong> - gle, Goo</li>
- Não tenha medo de errar<!-- .element: class="fragment" -->
- ...mas também lembre que ninguém aqui sabe mais que ninguém<!-- .element: class="fragment" -->

---

## Vamos aplicar TDD

---

![lembrete](https://miro.medium.com/max/996/1*pP8Ks6tlt718jJg3fqrtvw.jpeg)

---

### Baby Steps

----

![kids](https://media.giphy.com/media/qCTaz2coxAJCE/giphy.gif)

---

#### Exemplo simples: Fatorial

----

```js
describe('fatorial', () => {
  test('0! = 1', () => expect(factorial(0)).toBe(1))
})
```

----

> <span style="color:red;font-weight:bold;">FAIL!</span>

----

```js
function factorial (num) {
  return 1
}
```

----

> <span style="color:green;font-weight:bold;">PASS!</span>

----

```js
describe('fatorial', () => {
  test('0! = 1', () => expect(factorial(0)).toBe(1))
  test('1! = 1', () => expect(factorial(1)).toBe(1))
})
```

----

> <span style="color:green;font-weight:bold;">PASS!</span>

----

```js
function factorial (num) {
  return 1
}
```

----

```js
describe('fatorial', () => {
  test('0! = 1', () => expect(factorial(0)).toBe(1))
  test('1! = 1', () => expect(factorial(1)).toBe(1))
  test('2! = 2', () => expect(factorial(2)).toBe(2))
})
```

----

> <span style="color:red;font-weight:bold;">FAIL!</span>

----

```js
function factorial (num) {
  if (num < 2) {
    return 1
  }

  return 2
}
```

----

> <span style="color:green;font-weight:bold;">PASS!</span>

----

```js
describe('fatorial', () => {
  test('0! = 1', () => expect(factorial(0)).toBe(1))
  test('1! = 1', () => expect(factorial(1)).toBe(1))
  test('2! = 2', () => expect(factorial(2)).toBe(2))
  test('3! = 6', () => expect(factorial(3)).toBe(6))
})
```

----

> <span style="color:red;font-weight:bold;">FAIL...</span>

----

> Faremos mais um **if**?

----

**Acabei de ganhar 3 testes na minha suite! 🙌**

----

![Break dance](https://media.giphy.com/media/TZFsJcj0Whc88/giphy.gif)

---

## Referências

----

Wikipedia

https://pt.wikipedia.org/wiki/Coding_Dojo

----

http://codingdojo.org/

---

Por que expliquei Randori?

(nós vamos pular o primeiro Kata)<!-- .element: class="fragment" -->

<small>(não contem pra ninguém)</small><!-- .element: class="fragment" -->

----

Traga um **Kata** no próximo Dojo 🙋

---

## Nosso primeiro problema

----

> (・ｗ・）

----

[FizzBuzz](http://dojopuzzles.com/problemas/exibe/fizzbuzz/)

em JavaScript<!-- .element: class="fragment" -->

----

- Nosso programa deve imprimir uma lista de números, um por linha
<li class="fragment">Se o número for divisível por <strong>3</strong>, deve imprimir <strong>"Fizz"</strong> ao invés do número</li>
<li class="fragment">Se for divisível por <strong>5</strong>, imprime <strong>"Buzz"</strong> ao invés do número</li>
<li class="fragment">Se for divisível por <strong>3</strong> e por <strong>5</strong>, imprime <strong>"FizzBuzz"</strong></li>

----

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
```

----

```
...
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
```

----

e por aí vai...
