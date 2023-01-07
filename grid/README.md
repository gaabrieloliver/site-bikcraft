# Anotações sobre grid 

## grid-column: 1 
- Seleciona a coluna 1
<br>

## grid-column: 2 
- Seleciona a coluna 2 
<br>
<br>
## grid-column: 1 / 2 
- Da primeira coluna à segunda
<br> 

## grid-column: 1 / 3 
- Da primeira coluna à terceira
<br> 
<br>

## grid-column: span 1 
- Expande até a 1° coluna
## grid-column: span 2 
- Expande até a 2° coluna
## grid-column: 1 / span 3 
- Comece da linha 2 e expanda 3 colunas
<br>
<br>

# Tem diferenças do alinhamento do conteúdo e da caixa que está envolvendo ele, exemplo:
<br>

## justify-items: end 
- Alinha caixa à direita
<br>

## text-align: right; 
- Alinha texto à direita

<br>
<br>

# Grid template rows

## grid-template-rows: 100px auto;
Define o tamanho das linhas.
<br>

## grid-auto-rows:
Linhas são adicionadas automaticamente com o valor de auto.
<br>

## grid-rows: 2
Define a linha do item, funciona da mesma forma que o grid-column.
<br>

## grid-template-rows: auto auto;
Define o tamanho das linhas (força linha nova se possível)

<br>
<br>

## grid-auto-rows: 200px;
Cada linha nova que surgir vai definir o tamanho de 200px

## Imagine a situação:

A 1° linha quero que tenha o tamanho de 300px, a 2° auto e depois todas as próximas que ele for criar, no tamanho de 200px, então:

~~~css
.grid {
  grid-template-rows: 300px auto;
  grid-auto-rows: 200px;
}
~~~
podemos também agilizar com o código:

~~~css
.grid {
  grid-template-columns: repeat(2, 1fr); /* (qntdColunas, espaçamentoDisponível) */
  grid-template-rows: repeat(4, 200px);  /* (qntdLinhas, tamanhoLinha) */
}
~~~