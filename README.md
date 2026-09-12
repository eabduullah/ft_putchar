# ft_putchar

## 📖 Description

`ft_putchar` is a simple C project (part of the 42 School curriculum) that
reimplements the standard `putchar` function from `<stdio.h>` using the
`write` system call.

The goal of this exercise is to understand:
- How low-level I/O works in C (`write` vs buffered `stdio` functions)
- How to write your own version of a standard library function
- Working with file descriptors (`STDOUT_FILENO` / `1`)

## 🛠️ Function prototype

```c
void ft_putchar(char c);
```

## ⚙️ How it works

The function takes a single character `c` and writes it directly to the
standard output (file descriptor `1`) using `write(1, &c, 1)`.

Unlike the standard `putchar`, this version is **unbuffered** — it writes
immediately instead of waiting for a buffer flush.

## 📂 Files

| File | Description |
|---|---|
| `ft_putchar.c` | Contains the implementation of `ft_putchar` |

## 🚀 Usage example

```c
#include "ft_putchar.h"

int main(void)
{
	ft_putchar('H');
	ft_putchar('i');
	ft_putchar('\n');
	return (0);
}
```

Output:
```
Hi
```

## 🧑‍💻 Compilation

```bash
gcc -Wall -Wextra -Werror -c ft_putchar.c
```

## 📌 Notes

- Only allowed function: `write`
- No use of `printf` or any `stdio` output functions
- Norm-compliant (42 School coding style)
