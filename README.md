# javad
javaj


//자료구조 구조체 실습

#include <stdio.h>
#include <math.h>
#define MAX_SIZE 101
#define SWAP(x,y,t) ((t)=(x), (x)=(y), (y)=(t))
void sort(int [ ], int); // selection sort
void main(void)
{
int i, n, list[MAX_SIZE];
  printf("Enter the number of numbers to generate: ");
  scanf("%d", &n);
  if (n<1 || n>MAX_SIZE) {
    fprintf(stderr, "Improper value of n\n");
    exit(1);
  }
  for (i=0; i<n; i++) {
    list[i] = rand() % 1000;
    printf(%d  ", list[i]);
}

           sort(list, n);   // sort 함수를 호출. 인자는 배열과 정수의 개수
           printf("\n Sorted array:\n ");
             for (i=0; i<n; i++) // 정렬된 정수를 출력
                  printf("%d  ", list[i]);
             printf("\n");
           }
            
           void sort(int list[], int n)
           {
             int i, j, min, temp;
             for (i=0; i<n-1; i++) {  // list[i]부터 list[n-1]까지 정렬.
                  min = i;  // i 위치에 들어갈 최소값의 초기화
                  for (j=i+1; j<n; j++)
                        if (list[j]<list[min])
                     min = j; // 더 작은 것이 있으면 최소값을 이 곳으로…
                  SWAP(list[i], list[min], temp);  // 최소값과 i의 내용을 교체
             }
           }
