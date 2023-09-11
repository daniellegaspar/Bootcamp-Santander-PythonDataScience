
# **Python**

### Tipos de dados mais utilizados

Os tipos servem para definir as caracteristicas e comportamentos de um valor (objeto) para o interpretador.

### Tipos built-in:

- texto - str
- numérico - int, float, complex
- sequência - list, tuple, range
- mapa - dict
- coleção - set, frozenset
- booleano - bool
- binário - bytes, byrearray, memoryview

— Números inteiros: 1, 10, 100, -1, -10, -100…(idade, ano…)

— Números flutuantes: usado para representar os numeros racionais e sua implementação é feita pela classa float = 1.5, -10.543…(preço, altura, peso…)

— Booleanos usado para representar true ou false, é uma subclasse de int, onde qualquer número diferente de 0 representa verdadeiro e 0  falso.

— Strings usadas para representar valores alfanuméricos. “python”, ‘python’, ‘’’’’python’’’’’…

#### MODO INTERATIVO

O interpretador python pode executar em modo que possibilite o desenvolvedor a escrever código, e ver o resultado na hora. 

Duas formas de fazer isso:

chamando apenas o interpretador python (puthon)

ou executar o script com a flag  -i (python -i app.py)

---

**Váriáveis**

Em linguagens de programação podemos definir valores que podem sofrer alterações no decorrer a execução do programa. Elas recebem o nome de variáveis, pois nascem com um valor  e não necessariamente devem permancer com o mesmo.


```python
Ex.:
nome, idade = "Danielle", 28

print(nome, idade)

nome = "Lucca"
```

********************Constantes -********************
São utilizadaspara armazenar valores, ela nasce com um valor e permanece com ele até o final da execução do programa, é imutável.

```python
Ex.:
BRAZILIAN_STATES = ["SP", "RJ", "SC", "RS"]
print(BRAZILIAN_STATES)
```

> 💡 PYTHON NÃO TEM CONSTANTES, em python utilizamos a convenção que diz ao programador que a variável é constante, criando a variável com o nome todo em letras MAIÚSCULAS.
> 

**************************BOAS PRÁTICAS**************************

- padrão de nomes em snake case = Ex.: primeiro programa em python fica **primeiro_programa_em_python**
- escolher nomes sugestivos = se o código fala sobre saque bancário, o nome das variáveis deve condizer com o código
- Nome de constantes todo em maiúsculo

******************Conversão de Tipos******************

Em alguns momentos é necessário converter o tipo de uma variável para manipular de forma diferente. Ex.: variáveis do tipo *******string,******* que armazenam números e precisamos fazer alguma operação matemática com esse valor

```python
# int para float
preco = 10
print(preco)

preco = float(preco)
print (preco)

preco = 10 / 2
print(preco)
```

```python
# Exemplo de float para int
preco = 10.30
print(preco)

preco = int(preco)
print(preco)
```

```python
# conversão por divisão
preco = 10
print(preco)

print(preco / 2)
print(preco // 2)
```

```python
# string para numéro
preco = "10.50"
idade = "28"

print(float(preco))

print(float(idade))
```

Nem sempre é possível fazer a conversão por exemplo🔽 
```python
preco = "python"
print(float(preco)

# não dá para converter *string* em *float*
```

### **Funções de entrada e saída (input e output)**

*Receber e exibir informações para o usuário.*

**-Função ******input:******** a função builtin input é usada quando queremos ler dados de entrada padrao (**teclado**). Ela recebe um argumento do tipo string, que é exibido para o usuário na saída padrão (**tela**). A função lê a entrada, converte para *string* e retorna o valor.

```python
Ex.: nome= input("Informe o seu nome: ")
```

**-Função ******print:******** a função *print* é usada quando queremos exibir dados na saída padrao (*******tela*******). Ela recebe um argumento obrigatório do  tipo varargs de objetos e 4 argumentos opcionais (sep, end, file e flush). Todos os objetos são convertidos para *******string,******* separados por *sep* e terminados por ****end.**** A *******string******* final é exibida para o usuário.

```python
nome = "Danielle"
sobrenome = "Gaspar"

print(nome, sobrenome)
printo(nome, sobrenome, end="...\n")
print(nome, sobrenome, sep="#")
```

### OPERADORES ARITMÉTICOS

Executam operações matemáticas como: adição, subtração, divisão …

```python 
# Adição
print(1 + 1)

# Subtração
print(10 - 2)

# Multiplicação
print(4 * 3)

# Divisão
print(12 / 3)

# Divisão inteira
print(12 // 2)

# Módulo = resto da divisão. 
print(10 % 3)

# Exponenciação
print(2 ** 3)
```
### Precedência dos Operadores

É a regra que indica quais operações devem ser executadas primeiro, pois dependendo da ordem que forem executadas o valor pode ser diferente.

x = 10 - 5 * 2

x é igual a 10 ou 0***?***

Ordem na matemática:

— Parêntesis

— Expoêntes

— Multiplicações e divisões (da esqueda para a direita)

— Soma e Subtrações (da esquerda para a direita)

### Operadores de Comparação

Operadores utilizados para comparar dois valores
```python
# igualdade
saldo = 450
saque = 200
print(saldo == saque)
>>> False

# diferença
saldo = 450
saque = 200
print(saldo != saque)
>>> True

# maior que/maior ou igual
saldo = 450
saque = 200
print(saldo > saque)
>>> True

print(saldo >= saque)
>>> True

# menor que/menor ou igual
saldo = 450
saque = 200
print(saldo < saque)
>>> False

print(saldo <= saque)
>>> False
```
### Operadores de atribuição

Utilizados para definir o valor inicial ou sobescrever o valor de uma variável.

```python
#Simples
saldo = 500
print(saldo)

#Com adição
saldo = 500
saldo += 200
print(saldo)

#Com subtração
saldo = 500
saldo -= 100
print(saldo)

#Com multiplicação
saldo = 500
saldo *= 2
print(saldo)

#Com divisão
saldo = 500
saldo /= 5
print(saldo)

saldo = 500
saldo //= 5
print(saldo)

#Com módulo
saldo = 500
saldo %= 40
print(saldo)

#Com exponenciação
saldo = 0
saldo **= 2
print(saldo)
```

### Operadores Lógicos

Utilizados em conjunto com operadores de comparação, para montar uma expressão lógica. Quando utilizado um operador de comparação o resultado é um booleano.

Ex.: op_comp + op_log + op_comp …N…

```python
# operador e
saldo = 1000
saque = 200
limite = 100

saldo >= saque and saque <= limite
>>> False
```

#### — operador ***and**  =*  e,as duas ou mais  expressões precisam ser verdadeiras para resultar em true.
```python 
Ex.: 
saldo = 1000
saque = 200
limite = 100

saldo >= saque and saque <= limite
>>> False
```

#### — operador or = ou
verdade e verdade = verdadeiro

verdade ou falso = verdadeiro

falso ou verdadeiro = verdade

falso ou falso = falso

É verdade se apenas uma expressão seja verdadeira.
```python
saldo = 1000
saque = 200
limite = 100

saldo >= saque or saque <= limite
>>> True
```

#### —operador de *****negação =***** not
```python
contatos_emergencia = []

not 1000 > 1500
>>> True

not contatos_emergencia
>>> True

not "saque 1500;"
>>> False

not ""
>>> True
```

#### —parênteses delimita a precedência de compração
```python
saldo = 1000
saque = 250
limite = 200
conta_especial = True

saldo >= saque and saque <= limite or conta_especial and saldo >= saque
>>> True

(saldo >= saque and saque <= limite) or (conta_especial and saldo >= saque)
>>> True
```

### Operadores de Identidade
Utilizado para comparar se os dois objetos testados ocupam a mesma posição na memória.
```python
curso = "Curso de Python"
nome_curso = curso
saldo, limite = 200, 200

curso is nome_curso
>>> True

curso is not nome_curso
>>> False

saldo is limite
>>> True
```

### Operadores de Associação
Utilizado para verificar se um objeto está presente em uma sequência. 
```python
curso = "Curso de Python"
frutas = ["laranja", "uva", "limão"]
saques = [1500, 100]

"Python" in curso
>>> True

"maçã" not in frutas
>>> True

200 in saques
>>> False
```

## ****Estruturas Condicionais e de Repetição em Python****

#### ****Indentação e blocos****

Identar o código é uma forma de manter o código fonte mais legível e manutenível. Através da indentação o interpretador consegue determinar onde um bloco de comando inicia  e onde ele termina.

#### Bloco de Comando em Python

É indicado utilizar 4 espaços em branco por nível de indentação, ou seja, a cada novo bloco adicionamos 4 novos espaços em branco.
