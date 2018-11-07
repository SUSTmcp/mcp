# mcp
日常练习
#变量交换
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int a = 10, b = 20;
	int tmp;
	tmp= a;
	a = b;b
	b = tmp;
	printf("%d %d\n", a, b);
	system("pause");
    return 0;		
}

#无临时变量交换
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int a = 10, b = 20;
	a = a ^ b;
	b = a ^ b;
	a = a ^ b;
	printf("%d %d\n", a, b);
	system("pause");
	return 0;
}

#求最大值
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int arr[10] = { 2, 3, 4, 6, 8, 9, 5, 1, 0, 7 };
	int i = 0;
	int max = arr[0];
	for ( i = 0; i < 10; i++)
	{
		if (arr[i] > max)
		{
			max = arr[i];
		}
	}
	printf("%d\n", max);
	system("pause");
	return 0;
}

#从小到大输出
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int a = 10; 
	int b = 20; 
	int c = 30;
    int tmp = 0;
	if (a < b)
	{
		tmp = a;
		a = b;
		b = tmp;
	}
    if (a < c)
    {
		tmp = a;
		a = c;
		c = tmp;
    }
	if (b < c)
	{
		tmp = b;
		b = c;
		c = tmp;
	}
	printf("%d %d %d\n", a, b, c);
	system("pause");
	return 0;
}

#求最大公约数
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int a, b, c;
	while (1)
	{
		printf("输入两个数求最大公约数:");
		scanf("%d %d", &a, &b);
		c = a % b;
		while (c != 0)
		{
			a = b;
			b = c;
			c = a % b;
		}
		printf("%d\n", b);
		system("pause");
		return 0;
	}
}
