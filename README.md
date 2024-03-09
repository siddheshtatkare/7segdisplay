# 7segdisplay

#include<reg51.h>
void delay(unsigned int t);
void main()
{
unsigned int ch[]={0xC0,0xF9,0xA4,0xB0,0x99,0x92,0x82,0xF8,0x80,0x90,0x88};
unsigned int i;
P2=0x00;

while(1)
{	
for(i=0;i<11;i++)
{
P2=ch[i];
delay(100);
}
}
}
void delay(unsigned int t)
{
unsigned int i,j;
for(i=0;i<t;i++)
for(j=0;j<1275;j++);
}
