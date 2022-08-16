# logic-gates
#include<stdio.h>
#include<conio.h>
void main()
{
int a[20],b[20],c[20],i,n,choice;
printf("Enter the choice");
printf("\n1-for not\n2-for or\n3-for and\n4-for nor\n5-for nand\n");
scanf("%d",&choice);

switch(choice)

case 1:
{
   printf("your choice is not gate\n");
   printf("formula is a!\n");
printf("enter the number of bits: ");
scanf("%d",&n);
read:
printf("enter the inputs in binary(0,1 only)\n");
for(i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
for(i=0;i<n;i++)
{
if(a[i]>1)
goto read;}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto write;

write:
printf("input is\n");

for(i=0;i<n;i++)
{
printf("%d\t",a[i]);}
printf("\n");
for(i=0;i<n;i++)
{
if(a[i]==1)
c[i]=0;
if(a[i]==0)
c[i]=1;
}
printf("output is\n");
for(i=0;i<n;i++){
printf("%d\t",c[i]);}
break;

case 2:
{
printf("your choice is or gate\n");
   printf("formula is (a+b)\n");
printf("enter the number of bits: ");
scanf("%d",&n);
read1:
printf("\nenter the inputs for a in binary (0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&a[i]);

for(i=0;i<n;i++)
{
if(a[i]>1){
printf("\ninput is wrong re-enter it");
goto read1;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto write1;

write1:
printf("\nenter the inputs for b in binary (0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&b[i]);


for(i=0;i<n;i++)
{
if(b[i]>1){
printf("\ninput is wrong re-enter it");
goto write1;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto list1;
list1:
for(i=0;i<n;i++)
{
if(a[i]+b[i]==0)
c[i]=0;
else
c[i]=1;
}
printf("input for a is\n");
for(i=0;i<n;i++)
printf("%d\t",a[i]);
printf("\n");
printf("input for b is\n");
for(i=0;i<n;i++)
printf("%d\t",b[i]);
printf("\n");
printf("output is\n");
for(i=0;i<n;i++)
printf("%d\t",c[i]);
break;
}


case 3:
{
printf("your choice is and gate\n");
   printf("formula is (a•b)\n");
printf("enter the number of bits: ");
scanf("%d",&n);

read2:
printf("\nenter the inputs for a in binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&a[i]);

for(i=0;i<n;i++)
{
if(a[i]>1){
printf("\ninput is wrong re-enter it");
goto read2;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto write2;
write2:
printf("\nenter the inputs for bin binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&b[i]);

for(i=0;i<n;i++)
{
if(b[i]>1){
printf("\ninput is wrong re-enter it");
goto write2;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto list2;
list2:

for(i=0;i<n;i++)
{
if(a[i]+b[i]==2)
c[i]=1;
else
c[i]=0;
}
printf("input for a is\n");
for(i=0;i<n;i++)
printf("%d\t",a[i]);
printf("input for b is\n");
for(i=0;i<n;i++)
printf("%d\t",b[i]);
printf("\n");
printf("output is\n");
for(i=0;i<n;i++)
printf("%d\t",c[i]);
break;
}

case 4:
{
printf("your choice is nor gate\n");
   printf("formula is (a+b)!\n");
printf("enter the number of bits: ");
scanf("%d",&n);
read3:
printf("\nenter the inputs for a in binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&a[i]);
for(i=0;i<n;i++)
{
if(a[i]>1){
printf("\ninput is wrong re-enter it");
goto read3;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto write3;
write3:
printf("enter the inputs for b in binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&b[i]);
for(i=0;i<n;i++)
{
if(b[i]>1){
printf("\ninput is wrong re-enter it\n");
goto write3;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto list3;
list3:
for(i=0;i<n;i++)
{
if(a[i]+b[i]==0)
c[i]=1;
else
c[i]=0;
}
printf("input for a is\n");
for(i=0;i<n;i++)
printf("%d\t",a[i]);
printf("\n");
printf("input for b is\n");
for(i=0;i<n;i++)
printf("%d\t",b[i]);
printf("\n");
printf("output is\n");
for(i=0;i<n;i++)
printf("%d\t",c[i]);
break;
}

case 5:
{
printf("your choice is nand gate\n");
   printf("formula is (a•b)!\n");
printf("enter the number of bits: ");
scanf("%d",&n);
read4:
printf("enter the inputs for a in binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&a[i]);
for(i=0;i<n;i++)
{
if(a[i]>1){
printf("\ninput is wrong re-enter it");
goto read4;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto write4;

write4:
printf("enter the inputs for b in binary(0,1)\n");
for(i=0;i<n;i++)
scanf("%d",&b[i]);
for(i=0;i<n;i++)
{
if(b[i]>1){
printf("\ninput is wrong re-enter it\n");
goto write4;}}
for(i=0;i<n;i++)
if(a[i]==0||1)
goto list4;
list4:
for(i=0;i<n;i++)
{
if(a[i]+b[i]==2)
c[i]=0;
else
c[i]=1;
}
printf("input for a is\n");
for(i=0;i<n;i++)
printf("%d\t",a[i]);
printf("\n");
printf("input for b is\n");
for(i=0;i<n;i++)
printf("%d\t",b[i]);
printf("\n");
printf("output is\n");
for(i=0;i<n;i++)
printf("%d\t",c[i]);
break;
}
default:
{printf("invalid option");}
}
}
