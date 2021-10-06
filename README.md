#  演算法Sort

###  選擇排序(Select Sort)
選擇排序是一個簡單基礎排序演算法，工作步驟大約是將排序之數組分成兩區:未排序和已排序，自未排序中找出最大的數，放入已排序區，再尋找次大的數依序放入以排序區，以此類推，在n個數字排序中至多只會形成(n-1)次排序 平均時間複雜度О(n²)

以下有示例程式碼 (C++)
``` c++=
#include<bits/stdc++.h>
using namespace std;
int main(){
	void selection_sort(int a[], int n) {
    int i,j,temp;

	for (i = 0 ; i < n - 1 ; i++) {
		int min = i;
		for (j = i + 1; j < n; j++)     //走訪未排序的元素{
			if (a[j] < a[min])    //找到目前最小值{
				min = j;    //紀錄最小值
			}
		}
		if(min != i){
		  temp=a[min];  //交換兩個變數
		  a[min]=a[i];
		  a[i]=temp;
		}
		//或是以 swap(&a[min], &a[i]); 替代
        //若要使用這個 則需定義以下之函式
	}
}

/*
void swap(int *a,int *b){ //這團交換兩個變數函式
    int temp = *a;
    *a = *b;
    *b = temp;
}
```
