# mabani
#include<stdio.h>
#include<time.h>
#include<string.h>
#include<stdlib.h>
#include<ctype.h>
#include<conio.h>
 int cash=0;
boz
char order[10],food1[20];
char c[2][20];
struct costumer
{

int sign;

int timev;

int timew;

  int list[10];

};
struct costumer men[7];

struct food
{

char name[50];

int price;

char prime[20][20];

int timep;
int sign;
int capacity;
};
struct food food[100];

void rnd ()
{

int i, j, k,h=0;

for (i = 0; i < 7; i++)
    {

if (men[i].sign == 0)
	{
	memset(men[i].list,0,10);
	  srand((h++)+time(NULL));
men[i].sign = rand() % 2;

if (men[i].sign == 0)
	    {

}

	  else
	    {
	        printf("person number %d\n",i);

men[i].timev = time (NULL);

men[i].timew = rand() % 30 + 20;

for (j = 0; food[j].price; j++)
		{

srand (time (NULL)+(h++));

k = rand ();

if (k % 3 == 0 && food[j].sign!=0)
		    {

men[i].list[j] = 1;
printf("%s  ",food[j].name);
}

}
printf("\n%d\n",men[i].timew);
}

}

}

}
int sum(int a[])
{
int i,s=0;
for(i=0;i<100;i++){
    if(a[i]==1)
        s++;
}
if(s>0)
    return 0;
else
    return 1;
}
int check (char a[], struct food food[])
{

int i;

for (i = 0; food[i].price; i++)
    {

if (strcmp (food[i].name, a) == 0)

return i;
    }


}
void Sakht ()
{
char s[120];
int i,k;
for (i = 0; food[i].price; i++);
gets (food[i].name);
scanf ("%d", &food[i].price);
int j;
scanf("%d",&k);
if(k==1){
        food[i].timep=0;
for (j = 0;j<2; j++)
    {
gets (s);

if (s == '\0')
	break;

      else

strcpy (food[i].prime[j], s);
}

}
else{
scanf ("%d", &food[i].timep);
strcpy(food[i].prime[0],food[i].name);
}
}
void edit (void)
{

char s[20];

gets (s);

int i;

for (i = 0; food[i].price && strcmp (food[i].name, s)!=0; i++)
    {


}

scanf ("%d", &food[i].price);
int j;
if (food[i].sign==1){
for (j = 0;j<2; j++)
    {

gets (s);

if (s == '\0')
	break;

      else

strcpy (food[i].prime[j], s);
}
}
else {
scanf ("%d", &food[i].timep);
}
}
void change(char a[],struct food food[]){
int i,j;
int s=0;
memset(c[0],0,strlen(c[0]));
memset(c[1],0,strlen(c[1]));
for(i=0;food[i].price;i++){
        if (strstr(a,food[i].name)&&food[i].sign!=1){
            strcpy(c[s],food[i].name);
s++;
        }


}
if(s==1){
    strcpy(food1,c[0]);
}
else{
s=0;
int k;

for(i=0;food[i].price;i++){
    s=0;
    for (j=0;j<2;j++){
            for(k=0;k<10;k++){
        if (!strcmp(food[i].prime[k],c[j])){
            s++;
        }
        }

        }
        if(s==2)
        break;
}
strcpy(food1,food[i].name);
}
printf("qqqqqqqqqqq%sqqqqqqqqq",food1);

}


typedef struct Anbar *anbar;
struct Anbar
{

//      int timep;
char name[20];
int timeC;
int sign;
 anbar link;
};
void display(anbar first){
anbar ptr=first;
while(ptr->link!=NULL){
        ptr=ptr->link;
    printf("%s",ptr->name);
}
}

int hazine(struct costumer men[],int i){
int j,s=0;
for(j=0;j<10;j++){
        if(men[i].list[j])
    s+=food[j].price;
}
return s;
}
void read (anbar first, struct costumer men[], struct food food[]);
void save(struct food food[],struct costumer men[],anbar first,char food1[],char order[],int cash);
void load(struct food food[],struct costumer men[],anbar first,char food1[],char order[],int cash);

int
main ()
{

anbar first;
first=(Anbar*)malloc(sizeof(Anbar));
first->link=NULL;

int i;
for(i=0;i<100;i++){
    food[i].price=0;
}
memset(men[0].list,0,100);
memset(men[1].list,0,100);
memset(men[2].list,0,100);
memset(men[3].list,0,100);
memset(men[4].list,0,100);
memset(men[5].list,0,100);
memset(men[6].list,0,100);
    strcpy(food[0].name,"sandwich morgh");
    food[0].price=10;
    food[0].timep=0;
food[0].sign=1;
    strcpy(food[0].prime[0],"morgh");
    strcpy(food[0].prime[1],"nan");
    strcpy(food[1].name,"sandwich goosht");
    food[1].price=14;
    food[1].sign=1;
    food[1].timep=0;
    strcpy(food[1].prime[0],"goosht");
    strcpy(food[1].prime[1],"nan");
    strcpy(food[2].name,"morgh");
    food[2].price=8;
    food[2].timep=10;
    food[2].capacity=3;
    food[2].sign=0;
    strcpy(food[2].prime[0],"morgh");
    strcpy(food[3].name,"goosht");
    food[3].price=12;
    food[3].sign=0;
    food[3].timep=3;
    food[3].capacity=3;
    strcpy(food[3].prime[0],"goosht");
    strcpy(food[4].name,"nan");
    food[4].price=2;
    food[4].timep=1;
    food[4].capacity=4;
    food[4].sign=2;
    strcpy(food[4].prime[0],"nan");
    strcpy(food[5].name,"nushabe");
    food[5].price=3;
    food[5].sign=2;
    food[5].timep=1;
    food[5].capacity=3;
    strcpy(food[5].prime[0],"nushabe");
    strcpy(food[6].name,"dugh");
    food[6].price=2;
    food[6].timep=1;
    food[6].capacity=3;
    food[6].sign=2;
    strcpy(food[6].prime[0],"dugh");
for(i=0;i<7;i++){
    men[i].sign=0;
}
  for(;;){
   read(first,men,food);
  }
}
void
read (anbar first, struct costumer men[], struct food food[])
{
gets (order);
  rnd();
anbar ptr=first;
if(strstr(order,"save")){
  save(food,men,first,food1,order,cash);
}
else if(strstr(order,"load")){
  load(food,men,first,food1,order,cash);
}
else if(strstr(order,"check")){
    display(first);
    printf("%d",cash);
}
else if (strstr(order,"put")){
        int i, j, k, s = 0,t=0,l;
change(order,food);
ptr=ptr->link;
while (ptr!=NULL)
	{
if (ptr->sign==0)
	    {
for (j = 0; strcmp (food[j].name, ptr->name); j++);
if (time (NULL) - (ptr->timeC) > food[j].timep)
ptr->sign = 1;
	    }
if (strstr (order, ptr->name) && ptr->sign == 0)
	    {
printf ("not ready");
t++;
}
ptr = ptr->link;
}
anbar before=first;
if (t == 0)
	{
ptr = first;
while (ptr->link!=NULL)
	    {
ptr = ptr->link;
if (strstr (order, ptr->name) && ptr->sign == 1)
		{
before->link = ptr->link;
free (ptr);
ptr = before;
}
}
	}
}
else if (strstr (order, "give"))
    {

int i, j, k, s = 0,t=0,l;
for (i = 0; i < 7; i++)
	    {
if (strchr (order, i+'0'))
break;
}

s=0;
for(j=0;j<10;j++){
    if(!strcmp(food[j].name,food1)&&men[i].list[j]){
        s++;
        break;
    }
}
if (s>0)
		{

		    if (time(NULL)-men[i].timev>men[i].timew){
                    printf("tof tu rut");
                cash-=hazine(men,i);
                men[i].sign=0;
		    }
		    else{
		    men[i].list[j]=0;
		    men[i].timew+=10;
int k;
l=0;
for(k=0;k<10;k++){
    if(men[i].list[k]==1)
        l++;
}

if(l==0){
		   printf("thanks");
		   cash+=hazine(men,i);
men[i].sign = 0;
}
}
    }
	      else
		{
printf ("*****haji jooon!*****");
men[i].sign = 0;


}

}







  else if (strstr (order, "cook"))
    {

int i,g;

for (i = 0; food[i].price; i++)
	{

if (strstr (order, food[i].name))
	    {

anbar node;
node = (Anbar *) malloc (sizeof (Anbar));
anbar ptr=first;
g=0;
while (ptr->link!=NULL)
		{
ptr = ptr->link;
if(!strcmp(food[i].name,ptr->name))
    g++;
}
if(g<food[i].capacity){
strcpy (node->name, food[i].name);
node->timeC = time (NULL);
node->sign = 0;
node->link=NULL;
ptr->link=node;
}
else
    printf("haji Pore !");
//Check-capacity(node->name,)
break;
}

}

}

}
void save(struct food food[],struct costumer men[],anbar first,char food1[],char order[],int cash){
    FILE *fp;
    register int i;
    fp=fopen("file.text","wb");
    if(!fp){
        printf("\n haji save nemishe");
        getch();
        return;
    }
    fwrite(&cash,sizeof(int),1,fp);
  //  fwrite(&time,sizeof(int),1,fp);
   for(i=0;i<7;i++){
    fwrite(&men[i],sizeof(struct costumer),1,fp);
   }
   fwrite(&order,sizeof(char),1,fp);
   fwrite(&food1,sizeof(strlen(food1)),1,fp);
   anbar ptr=first;

   while(ptr->link){
        fwrite(&ptr,sizeof(struct Anbar),1,fp);
   ptr=ptr->link;

   }
   fclose(fp);
    printf("save gardid!");
}
void load(struct food food[],struct costumer men[],anbar first,char food1[],char order[],int cash){
 FILE *fp;
    register int i;
    fp=fopen("file.text","rb");
    if(!fp){
        printf("\n haji load nemishe");
        getch();
        return;
    }
    fread(&cash,sizeof(int),1,fp);
  //  fwrite(&time,sizeof(int),1,fp);
   for(i=0;i<7;i++){
    fread(&men[i],sizeof(struct costumer),1,fp);
   }
   fread(&order,sizeof(char),1,fp);
   fread(&food1,sizeof(strlen(food1)),1,fp);
   anbar ptr=first;

   while(ptr->link){
        fread(&ptr,sizeof(Anbar),1,fp);
   ptr=ptr->link;

   }
printf("load gardid ! ");
}

