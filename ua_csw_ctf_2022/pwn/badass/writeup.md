# Badass Quotes

## First of all, I'm not an expert, so maybe my approach was random and lucky in most of the challenges

### Here's the code

```

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    char term[64];
    char quote[32];

    setbuf(stdout, NULL);
    setbuf(stdin, NULL);
    setbuf(stderr, NULL);

    memset(term, 0, 64);
	memset(quote, 0, 32);

    printf("\nI CaN HaS BaDaSs QuOtE?\n# ");
    gets(quote);

    if (strcmp(term, "BaDaSs I Am") == 0) {
        printf("\n");
        system("cat flag.txt");
    } else if(strlen(term) != 0) {    
	    printf("\nI haz a sad %s...\n\n", term);
    } else {
	    printf("\nI haz a sad...\n\n");
	}

	printf(" ,_     _\n");
	printf(" |\\_,-~/\n");
	printf(" / _  _ |    ,--.\n");
	printf("(  @  @ )   / ,-'\n");
	printf(" \  _T_/-._( (   \n");
	printf(" /         `. \  \n");
	printf("|         _  \ | \n");
	printf(" \ \ ,  /      | \n");
	printf("  || |-_\__   /  \n");
	printf(" ((_/`(____,-'   \n");
	
}


```

in these 2 lines 
```     
memset(term, 0, 64);
	memset(quote, 0, 32);
```

I don't konw what memset means, but I think it's a function that sets memory cells in a consecutive order. So, *memset(term, 0, 64);* would set the memory cells from 0 to 64 for the variable **term**.
And *memset(quote, 0, 32);* would set memor cells from 0 to 31 for **qoute**. So it'll be as 0 to 32 for **qoute** and 33-64 for **term**.

From the source code, we can see that it prints out the flag if term is equal to **"BaDaSs I Am"**. which is only done if the cells starting from 32 have this value. So, I printed 'a'*32 + "BaDaSs I Am", which is "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaBaDaSs I Am". That printed out the flag. 
:)
So, I typed 'a' 32 times and after it I wrote **BaDaSs I Am**. So, 
