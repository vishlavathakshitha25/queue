#include <stdio.h>
#include <stdlib.h>
#define SIZE 100
int queue[SIZE];
int front=-1,rear=-1;
void enqueue(int value){
if (rear==SIZE-1)
{
printf("queue overflow!cannot insert %d\n",value);
return;
}
if(front==-1)front=0;
rear++;
queue[rear]=value;
print("%d enqueued to queue.\n",value);
}
int dequeue(){
if (front==-1// front>rear){
print("queue underflow!\n");
return-1;
}
int removed=queue[front];
front++;
return removed;
}
int peek(){
if(front==-1//front>rear){
printf("queue is empty!\n");
return-1;
}
return queue[front];
}
int display(){
if(front==-1//front>rear){
print("queue is empty!\n");
return;
}
printf("queue");
int i;
for (i=front;i<rear;i++)
{
printf("%d",queue[i]);
}
printf("\n");
}
int main(){
int choice,value;
while(1){
printf("\n--queue menu--\n");
printf("1.enqueue\n");
printf("2.dequeue\n");
printf("3.peek\n");
printf("4.display\n");
printf("5.exit\n");
printf("enter your choice:");
scanf("%d,$choice);
switch(choice){
case1:
printf("enter value to enqueue:");
scanf("%d",$value);
enqueue(value);
break;
case2:
value=dequeue();
if(value!=-1)
printf("dequeue value:%d\n",value);
break;
case3:
value=peek();
if(value!=-1)
printf("front element:%d\n",value);
brake;
case4:
display()
break;
case5:
printf("exiting---\n");
default:
printf("invalid choice!try agian.\n);
}
}
return 0;
}
