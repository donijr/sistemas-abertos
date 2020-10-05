# Globing e Quoting

##  ;

- **;**

; entre dois comandos faz o shell fazer o comando1 depois o comando2. 

```shell
comando1;comando2
```

##  &&

- **&&** 

(E) entre dois comandos faz o shell executar o comando2 se o comando1 ter exit status = 0.

```shell
comando1 && comando2
```

## || 

- **||**

(OU) entre dois comandos faz o shell executar o comando2 se o comando1 dar exit status != 0.

```shell
comando1 || comando2
```

## *

- **\***
Antes ou depois de um termo expandirá a busca/seleção para qualquer termo a partir do asteriscos ou antes dele, dependendo da limitação de texto antes ou depois. Exemplos: 

```shell
cat *.txt
```
```
saída: mostraria todo o conteúdo de cada arquivo .txt de uma pasta.
```
```shell
cat text*.txt
```
```
saída: mostraria todo o conteúdo de todos os arquivos que tem o nome com   text(AlgumaCoisa).txt
```

## ?

- **?**
? antes ou depois de um termo irá expandir a buscar/selecionar o nº de caracteres correspondentes ao nº de ? digitados.

## [0-9]

- **[123]**

Antes ou depois de um termo irá expandir para buscar/selecionar arquivos onde o espaço que está substituindo sejam os números 1 ou 2 ou 3.

---

- **[1239]**

Antes ou depois de um termo irá expandir para buscar/selecionar arquivos onde o espaço que está substituindo sejam os números 1 ou 2 ou 3 ou 9.

---

- **[0-9]**

Antes ou depois de um termo irá expandir para buscar/selecionar arquivos onde o espaço que está substituindo sejam os números 0 ao 9.

**Nota**
`!` nega o comando. EX: `[!0-9]` -> retornaria coisas que não são nºs.

##  [a-z] ou [A-Z]

- **[a-z]** 

Antes ou depois de um termo irá expandir para buscar/selecionar arquivos onde o espaço que está substituindo sejam as letras de “a” a “z” minúsculas.

**Nota**

`!` nega o comando. EX: `[!a-z]` --> retornaria coisas que não são letras.

---

- **[A-Z]** 

Antes ou depois de um termo irá expandir para buscar/selecionar arquivos onde o espaço que está substituindo sejam as letras de “A” a “Z” maiúsculas.

## {...,...}

- **comando {primeiro*,segundo?}**

Vai buscar/selecionar resultados correspondentes ao `primeio*` e/ou ao `segundo?` ao mesmo tempo.

## \

- **\qualquerCoisa** 

Ao usar o \ antes de qualquer coisa isso indica para o bash que não queremos que essa coisa seja interpretada como normalmente seria.

## “...” ou ‘...’

- **echo ‘parametro’** 

Ao usa`‘` ou `“` no início e final de um parametro indica para o bash que o que está entre ‘ ou “ é um único parametro e não um comando. 