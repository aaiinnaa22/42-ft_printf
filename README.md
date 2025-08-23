# 42-ft_printf

Hive Helsinki project

☆ INFO ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆ ☆

This project is about understanding the core of the C printf() function, and implementing a custom version called ft_printf(). The goal is to mimic a set of specific conversions found in printf(), and to get an understanding of how variadic functions work. 

☆ KEY CONCEPTS ☆ ☆ ☆ ☆ ☆ ☆

- Variadic functions: using va_start, va_arg, va_copy and va_end to handle unknown amounts of function arguments
- Type conversions: handling and printing the following
  -  %c, single character
  -  %s, string
  -  %p void * pointer, printed in hexadecimal format
  -  %d decimal (base 10) number
  -  %i integer in base 10
  -  %u unsigned decimal (base 10) number
  -  %x number in hexadecimal (base 16) lowercase format.
  -  %X number in hexadecimal (base 16) uppercase format.
  -  %% Prints a percent sign.

☆ RUN THE PROJECT ☆ ☆ ☆ ☆

The ft_printf project is built as a library using the Makefile. You can use the function by compiling and linking the library in another C project. 

First download and compile the ft_printf():
```
git clone https://github.com/aaiinnaa22/42-ft_printf.git
cd 42-ft_printf
make
```
The library libftprintf.a will be created at the root of this repository.

Make code you want to run with it, and include the ft_printf header file. For example a main.c:
```
#include "ft_printf.h"
int main(void)
{
  ft_printf("hello\n");
  ft_printf("hello and %s", "good evening");
  return (0);
}
```

Compile and run

```
cc main.c -L. -lftprintf -o myTest
./myTest
```

