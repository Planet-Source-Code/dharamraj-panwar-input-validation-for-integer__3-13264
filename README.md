<div align="center">

## input validation for integer


</div>

### Description

This Code Validate The Input provided by You Within The Integer Range -32768 to 32767

at Run Time. It checks each character and shows on the screen if it is valid .
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dharamraj Panwar](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dharamraj-panwar.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Validation/ Processing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/validation-processing__3-16.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dharamraj-panwar-input-validation-for-integer__3-13264/archive/master.zip)





### Source Code

```
#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<stdlib.h>
void main()
{
	int n,i,l;
	int MAX = 4;
	char s[7],ch;
	clrscr();
	printf("\nEnter the Integer Value within -32768 and 32767: ");
	i=0;
	while((ch = getch())!='\r'||i==0 || (MAX==5&&i==1))
	{
	  if(ch == '\b' && i >0)
	  {
		printf("%c",'\b');
		printf("%c",' ');
		printf("%c",'\b');
		i--;
		if(s[i] == '-')
		{
		  --MAX;
		}
	  }
	  else if( i == 0 && ch == '-')
	  {
	    s[i++] = ch;
	    putch(ch);
	    ++MAX;
	  }
	  else if(i== MAX)
	  {
	    s[i] = '\0';
	    n=atoi(s);
	    if(s[0] == '-' && (n > -3276 || (n == -3276 && ch <= '8')))
	    {
		 s[i++] = ch;
		 putch(ch);
	    }
	    else if(s[0] != '-' && (n < 3276 || (n == 3276 && ch <= '7')))
	    {
		 s[i++] = ch;
		 putch(ch);
	    }
	  }
	  else if(i < MAX && ch >= '0' && ch <='9')
	  {
	    s[i++] = ch;
	    putch(ch);
	  }
	}
	s[i] = '\0';
	n=atoi(s);
	printf("\n\nThe Value, You have Entered is: %d",n);
	getch();
}
```

