//滑动窗口问题
#include<stdio.h>
int a[2000010];
struct node
{
	int date, post;//定义数据，和相应下标
}sta[2000010];
int main()
{
	int n, m,i;
	scanf_s("%d%d", &n, &m);
	for (i = 0; i < n; i++)
	{
		scanf_s("%d", &a[i]);
	}
	int head = 0;//头
	int ans = 0;//尾
	sta[ans].date = a[0];
	sta[ans].post = 0;
	for (i = 0; i < n; i++)
	{
		while (head <= ans && sta[ans].date > a[i])
			ans--;
		sta[++ans].date = a[i];
		sta[ans].post = i;
		while (sta[head].post < i - m+1)
			head++;
		if(i+1>=m)printf("%d  ", sta[head].date);
	}
	printf("\n");
	head = 0;
	ans = 0;
	sta[ans].date = a[0];
	sta[ans].post = 0;
	for (i = 0; i < n; i++)
	{
		while (head <= ans && sta[ans].date < a[i])
			ans--;
		sta[++ans].date = a[i];
		sta[ans].post = i;
		while (sta[head].post < i - m + 1)
			head++;
		if (i+1 >= m)printf("%d  ", sta[head].date);
	}
	return 0;
}
