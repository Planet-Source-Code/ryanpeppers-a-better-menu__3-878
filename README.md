<div align="center">

## A Better Menu


</div>

### Description

This is my example of a quick and simple menu. This is a good method of simple menus, better then telling someone to enter 1 or 2 or 3 then hit enter to do this and that and i also think thats so boring. All you gotta do is just press the button it tells you then the operation will execute
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[ryanpeppers](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/ryanpeppers.md)
**Level**          |Beginner
**User Rating**    |3.3 (30 globes from 9 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/ryanpeppers-a-better-menu__3-878/archive/master.zip)

### API Declarations

stdio,conio,stdlib


### Source Code

```
#include <stdio.h> // for printf
#include <conio.h> // clrscr,getch
#include <stdlib.h> //exit function
// i like using this method of menus better then telling someone to enter 1 or 2 or 3 to do this and that
// all you gotta do is just press the button it tells you then the operation will execute
//******function proto-types*****
void sayabout();
void function1();
void function2();
void function3();
void yesorno();
void main()
{
int key = 0; // this is the varible that the keycode will be stored in
sayabout(); // call sayabout
getch(); // wait for key to be pressed
clrscr(); // clears screen
printf("Menu\n\r"); // displays the menu
printf("1: call function 1\n\r");
printf("2: call function 2\n\r");
printf("3: call function 3\n\r");
printf("ESC to exit.\n\r");
do // does a loop while they ESC key is not pressed
{
// if any key other then 1 2 3 or ESC is pressed it will do nothing and just keep looping until one of those keys is pressed
key = getch(); // keycode stored into key
// if 1 is pressed
if (key==49)
{
function1(); // call function1
break; // stop the loop
}
else
// if 2 is pressed
if (key==50)
{
function2();
break;
}
else
// if 3 is pressed
if (key==51)
{
function3();
break;
}
} while (key != 27); // if ESC is pressed then stop the loop
key = 0;
printf("press any key to continue....\n\r");
getch();
}
// *****declaranation of functions****
void sayabout()
{
clrscr();
printf("This is my example of A Better Menu.\n\r");
printf("This menu uses the getch function insted of the cin function.\n\r");
printf("In my personal opinion this is better then using cin =]\n\r");
printf("press any key to continue.......\n\r");
}
void function1()
{
printf("You've choosed option 1\n\r");
yesorno(); // call yesorno function
}
void function2()
{
printf("You've choosed option 2\n\r");
yesorno();
}
void function3()
{
printf("You've choosed option 3\n\r");
yesorno();
}
void yesorno() // the function name says it all
{
int keyy = 0; // keycode stored in varible
printf("Would you like to try again? (Y/N) \n\r");
do
{
keyy = getch();
// if y or Y is pressed then call the main function
if (keyy == 98 || keyy == 121)
main();
else
// if n or N is pressed then exit the program completely
if (keyy == 110 || keyy == 78) {
keyy = 0;
exit(-1); // exit function ends the program completely ((love this function))
}
} while (1);
}
```

