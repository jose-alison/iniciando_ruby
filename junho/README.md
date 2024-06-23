## Junho/2024

### Criando o primeiro arquivo

Os arquivo Ruby, possuem a extensão `.rb`.

`junho.rb`

## Tipos básicos de dados em Ruby

| Tipo   | Descrição         |
| ------ | ------------------- |
| int    | Números inteiros   |
| float  | Números decimais   |
| string | Textos              |
| bool   | Verdadeiro ou falso |

## Expressões aritméticas

| Operador | Operação                                              |
| -------- | ------------------------------------------------------- |
| +        | Adição                                                |
| -        | Subtração                                             |
| /        | Divisão => retorna apenas o quociente em forma de int  |
| *        | Multiplicação                                         |
| %        | Divisão => Retorna apenas o resto da divisão como int |

## Imprimindo dados no terminal

Os dados podem ser impressos no terminal usando `puts` ou `print`, tudo vai depender da nossa necessidade.

### Puts

Imprime os dados levando em consideração toda a lógica existente no código.

Exemplo:

```ruby
puts [[123], [4, 5, nil]]

>> 1
>> 2
>> 3
>> 4
>> 5
```

O código acima, exemplifica como o **puts** entende cada elemento passado no array (vamos ver em breve) e imprime cada um deles. Diferentemente, o código abaixo, usando **print**, considera todo ele como uma unica string e imprime-o em tela.

```ruby
print [[1, 2, 3], [4, 5, nil]]

>> [[1, 2, 3], [4, 5, nil]]
```

## Estruturas de decisões

### If,Elsif, Else

* **if**: Valida de uma condição é verdadeira.
* **elsif**: no caso de condição alternativa.
* **else**: última condição em caso de não adequação de nenhuma outra.

```ruby
if (condicao1)
    # execução caso a condição 1 seja atendida
elsif (condicao2)
    # execução caso a condição 2 seja atendida
else
    # execução caso nenhuma das condições anteriores sejam atendida
end
```

É necessário informar onde encerrar a repetição com o **end**.

### Operadores lógicos

| <br />Operador | Operação                    |
| -------------- | ----------------------------- |
| >              | Maior que                     |
| <              | Menor que                     |
| >=             | Maior ou igual                |
| <=             | Menor ou igual                |
| =              | Atribuição => (a = 1)       |
| ==             | Igualdade => (a == a => True) |
| !=             | Diferença                    |
| &&             | e                             |
| \|\|           | ou                            |

### **While**

    Operador usado para realizar repetição enquanto a condição for verdadeira.**Verifica primeiro e executa depois.**

```ruby
x = 0 

while x < 5 do
    puts "Valor de X:"
    puts x
    i = i + 1
end
```

### **Do While**

    Diferente do while, o do while executa a operação primeiro e só em seguida, verifica. O que significa que ele será executado ao menos uma vez.

```ruby
loop do # A estrutura deve começar com loop do
    puts "Valor de X:" # antes de verificar o if do código, esses puts serão impressos
    puts x
    x = x + 1
    if x == 5
        break # Break é uma estrutura lógica usada como condição de parada
    end # end relativo ao if
end # end relativo ao loop do, while
```

### **for**

    realiza alguma operação para cada iteração feita.

* ### range

  É uma lista criada pelo próprio compilador, e segue sempre nossa regra passada. No Ruby, o range será representado por um numero seguido de dois pontos e um segundo numero.
  Ex: 1..10  => Nesse caso, nosso programa criará uma lista iterável de 1 a 10, acrescentando de 1 a 1, ou seja, 1, 2, 3, 4 ... até 10.


  ```ruby
  for x in 1..10 do # para cada elemento do range
      puts "Valor de X:" 
      puts x # imprimirá o 1, depois o 2, depois o 3 ...
  end # fim do laço
  puts "Fim" # executará somente uma vez após concluir o loop
  ```

### **until**

**Não é recomendado seu uso, mas vale a pena saber que ela existe**.
    Age de forma oposta ao for ou do while, pois ele executa algo enquanto a condição for falsa. 
    Existem formar muito mais inteligentes de fazer isso com for ou do while.

```ruby
x = 0

until x == 5
    puts "Valor de X"
    puts x
    x = x + 1
end
puts "Terminou"

>> Valor de X
>> 0
>> Valor de X
>> 1
>> Valor de X
>> 2
>> Valor de X
>> 3
>> Valor de X
>> 4
>> Terminou
```