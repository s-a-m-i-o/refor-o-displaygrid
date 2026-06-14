# 📚 Módulo 1 — Fundamentos do CSS Grid

## O que é CSS Grid?

CSS Grid é um sistema de layout bidimensional criado para organizar elementos em linhas e colunas ao mesmo tempo.

Diferente do Flexbox, que trabalha principalmente em uma única direção (linha ou coluna), o Grid foi projetado para controlar os dois eixos simultaneamente.

---

## display: grid

Para transformar um elemento em Grid, utilizamos:

```css
.container {
    display: grid;
}
```

Ao aplicar apenas `display: grid`, os elementos continuam empilhados verticalmente. O Grid só começa a criar colunas quando definimos sua estrutura.

---

## grid-template-columns

A propriedade `grid-template-columns` define quantas colunas existirão e qual será o tamanho de cada uma.

Exemplo:

```css
.container {
    display: grid;
    grid-template-columns: 200px 200px 200px;
}
```

Resultado:

```text
[1][2][3]
```

---

## Posicionamento Automático (Auto Placement)

Quando existem colunas disponíveis, o Grid distribui os elementos automaticamente.

Exemplo:

```css
grid-template-columns: repeat(3, 200px);
```

Com 5 elementos:

```text
[1][2][3]
[4][5]
```

O Grid preenche as colunas da esquerda para a direita e cria novas linhas quando necessário.

---

## repeat()

A função `repeat()` evita repetição de código.

Em vez de:

```css
grid-template-columns: 200px 200px 200px;
```

Podemos escrever:

```css
grid-template-columns: repeat(3, 200px);
```

Ambos produzem exatamente o mesmo resultado.

Vantagens:

* Código mais limpo
* Melhor manutenção
* Maior legibilidade

---

## Unidade fr (Fraction)

A unidade `fr` representa uma fração do espaço disponível.

Exemplo:

```css
grid-template-columns: 1fr 1fr 1fr;
```

O espaço será dividido igualmente entre as três colunas.

---

## Proporções com fr

O Grid trabalha com proporções.

Exemplo:

```css
grid-template-columns: 1fr 2fr 1fr;
```

O espaço será dividido em 4 partes:

```text
1 + 2 + 1 = 4
```

Distribuição:

```text
1 parte | 2 partes | 1 parte
```

A segunda coluna ficará maior porque recebe duas frações.

---

## Misturando px e fr

É possível combinar tamanhos fixos com tamanhos flexíveis.

Exemplo:

```css
grid-template-columns: 200px 1fr 1fr;
```

O Grid:

1. Reserva os 200px da primeira coluna.
2. Calcula o espaço restante.
3. Divide o restante entre as colunas com `fr`.

Regra mental:

> Primeiro o Grid resolve os tamanhos fixos. Depois distribui o espaço restante entre as frações.

---

## Conceitos Aprendidos

✔ display: grid

✔ grid-template-columns

✔ posicionamento automático

✔ repeat()

✔ unidade fr

✔ proporções com fr

✔ mistura de px e fr

✔ cálculo do espaço restante

---

## Conclusão

Neste módulo aprendemos a criar colunas utilizando CSS Grid, entender como o Grid posiciona elementos automaticamente e como distribuir espaço utilizando a unidade `fr`.

Esses conceitos formam a base para todos os módulos seguintes.
