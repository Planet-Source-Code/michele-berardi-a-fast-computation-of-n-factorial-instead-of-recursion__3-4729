<div align="center">

## A fast Computation of N\! \( Factorial\) instead of recursion\.\.\.


</div>

### Description

Quickly you can obtain your factorial number, and of course this code explain the theory you can optimize more and more this.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[michele berardi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/michele-berardi.md)
**Level**          |Advanced
**User Rating**    |3.3 (10 globes from 3 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/michele-berardi-a-fast-computation-of-n-factorial-instead-of-recursion__3-4729/archive/master.zip)





### Source Code

```
/*
 Quick Factorial Computation
 (you can use any types instead of long!)
 (C) 2002 Berardi Michele
 http://web.tiscali.it/mberardi
 E-Mail(s): 03473192000@vizzavi.it
 mfxaub@tin.it
*/
#include <stdio.h>
void main()
 {
 	long N , b , c , p ; // use int for fast calculation and small range of calculation..
							// use double for factor bigger than 12!
 Restart:
 	printf("Enter N!: ");
 	scanf("%d", &N);
		if(N < 0)
 	{
 		printf("\t\n R.estart, I.nvalid P.arameter! (N > -1)\n");
 		goto Restart;
 	}
 	else
	c = N - 1;
	p = 1;
	while(c>0)
	{
		p = 0;
		b = c;
			while(b>0) {
					if ( b & 1 )
					{
					p += N; // p = p + N;
					}
			// if you would like to use double choose the alternative forms instead shifts
		 // the code is fast even!
			// you can use the same tips on double or 64 bit int etc.... but you must... ;-)
			b >>=1; // b/=2; (b = b / 2;) ( b >> 1; a.s.r. is more efficent for int or long..!)
			N <<=1; // N += N; N = N + N; N = N * 2; (N <<=1; a.s.l. is more efficent for int or long..!)
			} // end of: while(b>0)
			N = p;
			c--; // c = c - 1;
	} // end of: while(c > 0)
	printf("[%d] is the factorial! \n", p);
}
//p.s.
//using recursion is much slower!
//for example:
//
//int fact(int);
//void main()
//{
// int N;
// printf("Enter the number: ");
// do
// { scanf("%d",&N);}
// while(N<0);
// printf("\n %d", fact(N));
// }
// int fact(int N)
// {
// int f;
// if(N==0)f=1;
// else f=N*(fact(N-1));
// return f;
// }
```

