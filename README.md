ALX TEAM PROJECT (printf)
team members - Temiede Emmanuel 
		David Grace
Customizing printf

The GNU C Library lets you define your own custom conversion specifiers for printf template strings, to teach printf clever ways to print the important data structures of your program.
The way you do this is by registering the conversion with the function register_printf_function; see Registering New Conversions. One of the arguments you pass to this function is a pointer to a handler function that produces the actual output; see Defining the Output Handler, for information on how to write this function.

You can also install a function that just returns information about the number and type of arguments expected by the conversion specifier. See Parsing a Template String, for information about this.
The facilities of this section are declared in the header file printf.h.
:
Portability Note: The ability to extend the syntax of printf template strings is a GNU extension. ISO standard C has nothing similar. When using the GNU C compiler or any other compiler that interprets calls to standard I/O functions according to the rules of the language standard it is necessary to disable such handling by the appropriate compiler option. Otherwise the behavior of a program that relies on the extension is undefined.
