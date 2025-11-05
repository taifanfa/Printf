# 🖨️ `ft_printf` — 42 School Project  
> 🧮 Recreating the classic `printf` function from scratch, with precision and C mastery.  
> Recriando a função `printf` do zero — com domínio de formatação e manipulação em C.

---

## 🧠 🇧🇷 Descrição

O **`ft_printf`** é um dos projetos mais icônicos da **Escola 42**, e seu propósito é recriar a função padrão da linguagem C: `printf()`.

O desafio consiste em **imitar o comportamento real do `printf`**, incluindo o tratamento de diferentes tipos de variáveis, formatação de saída e controle de buffer — **sem usar a função original da biblioteca padrão**.

Neste projeto (sem bônus), a função cobre as principais conversões de formatação:
- `%c` → caractere  
- `%s` → string  
- `%p` → ponteiro (endereços em hexadecimal)  
- `%d` / `%i` → números inteiros  
- `%u` → números inteiros sem sinal  
- `%x` / `%X` → hexadecimal (minúsculo e maiúsculo)  
- `%%` → imprime o próprio caractere `%`

---

### 🧠 🇺🇸 Description

**`ft_printf`** is one of the cornerstone projects at **42 School**, aimed at recreating the standard C function `printf()` from scratch.

The challenge is to **replicate the real behavior of `printf`**, handling multiple data types, output formatting, and buffer control — **without using the original library function**.

In this (non-bonus) version, the implementation supports the following format specifiers:
- `%c` → character  
- `%s` → string  
- `%p` → pointer (address in hexadecimal)  
- `%d` / `%i` → signed integer  
- `%u` → unsigned integer  
- `%x` / `%X` → hexadecimal (lowercase and uppercase)  
- `%%` → prints a literal `%`

---

## ⚙️ 🇧🇷 Funcionamento

O `ft_printf` utiliza **funções variádicas (`<stdarg.h>`)** para lidar com um número indefinido de argumentos.  
A função principal percorre a *string de formatação*, identificando os símbolos `%` e chamando as funções auxiliares responsáveis por converter e imprimir o tipo correspondente.

Fluxo simplificado:
1. Ler o formato caractere por caractere.  
2. Detectar quando aparece `%`.  
3. Determinar o tipo (`c`, `s`, `d`, etc.).  
4. Recuperar o valor do argumento correspondente.  
5. Imprimir o valor com a formatação correta.  
6. Retornar o número total de caracteres impressos.

---

### ⚙️ 🇺🇸 How it Works

`ft_printf` uses **variadic functions (`<stdarg.h>`)** to handle a variable number of arguments.  
The main function iterates through the format string, identifying `%` symbols and calling helper functions to convert and print the corresponding data type.

Simplified flow:
1. Read the format string character by character.  
2. Detect each `%` occurrence.  
3. Identify the type (`c`, `s`, `d`, etc.).  
4. Retrieve the corresponding argument.  
5. Print it with proper formatting.  
6. Return the total number of printed characters.

---

## 🧪 🇧🇷 Compilação e uso

```bash
# Compilar biblioteca
make

# Incluir no seu programa
cc -Wall -Wextra -Werror main.c libftprintf.a -o my_printf
```
Exemplo de uso:

```bash
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s! The answer is %d.\n", "world", 42);
    return (0);
}
```

---

### 🧪 🇺🇸 Compilation and Usage

```bash
# Compile the library
make

# Link with your program
cc -Wall -Wextra -Werror main.c libftprintf.a -o my_printf
```
Usage example:

```bash
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s! The answer is %d.\n", "world", 42);
    return (0);
}
```

---

## 🧰 Estrutura de Arquivos / File Structure

📂 ft_printf/
-├── ft_printf.c
-├── ft_printf.h
-├── ft_print_char.c
-├── ft_print_str.c
-├── ft_print_num.c
-├── Makefile
-└── README.md

--- 

### 🏁 Resultado / Result

✅ Suporta múltiplos formatos (%c, %s, %p, %d, %i, %u, %x, %X, %%) |
✅ Retorna o número de caracteres impressos |
✅ 100% compatível com a Norma da 42 |
✅ Projeto limpo, modular e sem leaks


---

### 👩‍💻 Créditos / Credits

Autor: Tai Fanfa |
Projeto: ft_printf (42 School) |
Linguagem: C |
Licença: MIT |
