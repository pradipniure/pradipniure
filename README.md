TITLE: IMPLEMENTATION OF DYNAMIC MEMORY ALLOCATION
Program:List the marks of n students in C in Descending order using DMA. Find the third highest and second lowest marks.
#include <stdio.h>
#include <conio.h>
#include <std lib.h>
void main(){
	float *marks, temp;
	int n,i,j;
	clrscr();
	printf("How many marks?");
	scanf(" %d", &n);
	marks = (*float) malloc(n*sizeof(float));
	printf("Enter %d marks:\n",n);
	for(i=0;i<n;i++){
		printf("marks %d: ",i+1);
		scanf(" %f", marks+i);
	}
	
	//Sorting in Descending order
	for(i=0;i<n-1;i++){
		for(j=i+1;j<n;j++){
			if(*(marks+i) < *(marks+j){
				temp = *(marks+i);
				*(marks+i) = *(marks+j);
				*(marks+j) = temp;
			}
		}
	}
	
	printf("\nMarks in Descending order:\n");
	for(i=0;i<n;i++){
		printf("%.2f  ", *(marks+i));
	}
	
	printf("\nThird highest marks: %.2f",*(marks+2));
	printf("\nSecond lowest marks: %.2f",*(marks+n-2);
	
	getch();
}
