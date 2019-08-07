
 // PROJECT.
 // bill(name,class bill to store ),delete stock if stock==0.
 // make braces in conditions from 1331.


 #include<iostream.h>
 #include<conio.h>
 #include<stdio.h>
 #include<fstream.h>
 #include<process.h>
 #include<string.h>
 #include<dos.h>
 #include<graphics.h>

 //--------------------------------Global Variable----------------------------

 int flag=0;

 //------------------------General Functions------------------------------------------

 void kart();        // Function to Draw kart logo.
 void arrow();       // Function to display instruction on the bottom of screen.
 void box();         // To make the box.
 void bill();        //Function to Display bill.

 void mainmenu();   // Fumction of Main Menu.
 //-------------------------------------------------------------------------
 void plist();      // Function to view kart.
 int dplist(int h);     // Function to display kart.
 int  pcheck(char a[]); // Function to check purchase code.
 void delp();       // Function to delete item from kart.
 void user();       // Function to access the web without login.
 void nuser(int);   // Function to buy.
 void search();     // Function to search for given product.
 void ustock();     // Function to update stock.
 //void stock();      // Function to delete Garment if stock==0.
 void ser(char b[]);
 void serbox();

 //------------------------------------------------------------------------
 void login(){};    // Function to Login in the account.
 void signup(){};   // Function to make new account.
 void tc(){};       // Function to display Terms & Condition.
 void admin();      // Function of Administrator.


 //--------------------Functions related to Garments---------------------------------

 void garments();    // Function to access all the manipulation with garmnet.
 void ginput();    // Function to Input New garment.
 void gdisplay(int);  // Function to Display garment.
 void gmodify();   // Function to Modify Garment.
 void gdelete();   // Function to Delete Garment.
 void cdisp();      // Function to display all garment codes.
 int gcheck(char code[]); // Function to Check the garment code.

  //-------------------Function related to gadgets----------------------------

 void gadgets(); // Function to access all the manipulation with gadgets,
   void gdinput();    // Function to Input New gadgets.
   void gddisplay(int);  // Function to Display gadgets.
   void gdmodify();   // Function to Modify Gadgets.
   void gddelete();   // Function to Delete Gadgets.
   void cddisp();      // Function to display all gadgets codes.
   int gdcheck(char code[]); // Function to Check the gadget code.
//----------------------Function related to storing bill-----------------






//---------------------------------------------------------------------------
struct code{
	       char code[50][5];
	       int n;
	       code()
	       {
		n=0;
	       }
	     } s;

//--------------------------------------------------------------------------
 void kart()
  {
  int gdriver = DETECT, gmode, errorcode;
  initgraph(&gdriver, &gmode, "");
  int x=500,y=20;
  line(x,y,x+3,y+13);
  line(x+3,y+13,x+19,y+13);
  line(x+19,y+13,x+22,y+2);
  line(x,y,x+21,y+2);
  line(x+1,y+5,x+20,y+6);
  line(x+3,y+10,x+19,y+10);
  line(x+1,y,x-1,y-10);
  line(x-1,y-10,x-8,y-10);
  circle(x+5,y+17,2.5);
  circle(x+16,y+17,2.5);
  closegraph();
  }
 //--------------------------------------------------------------------------
 void arrow()
 {
  clrscr();
  int x=40,y=43;
  char a=280,b=281;
  gotoxy(x+3,y);
  y=y+2;
  cout<<"Use "<<a<<" "<<b<<" to goto your option.";
  gotoxy(x+2,y);
  cout<<"Press 'BACKSPACE' to go back.";
  gotoxy(x,y+2);
  cout<<"Press 'ENTER' To select your Option.";
 }
 //--------------------------------------------------------------------------

  class gadget {
		  public:

		  char code[5];
		  char cmp[30];
		  char type[15];
		  char model[30];
		  float price;
		  int stock;

		  int input();
		  void display(int);
		  int modify();
	       };

  int gadget::modify()
 {
  char c[5],t[10],cm[15],mn[10];
  int st;
  float p;
  cout<<"\n\n ENTER NEW CODE: ";
  gets(c);
  int k=gdcheck(c);
  if(k==1)
  {
   cout<<" ENTER NEW TYPE: ";
   gets(t);
   cout<<" ENTER NEW COMPANY: ";
   gets(cm);
   cout<<" ENTER NEW MODEL : ";
   gets(mn);
   cout<<" ENTER NEW PRICE: ";
   cin>>p;
   cout<<" ENTER NEW STOCK: ";
   cin>>st;


   if(strcmp(c,".")!=0)
     strcpy(code,c);
   if(strcmp(t,".")!=0)
     strcpy(type,t);
   if(strcmp(cm,".")!=0)
     strcpy(cmp,cm);
   if(strcmp(mn,".")!=0)
     strcpy(model,mn);
   if(st!=-1)
     stock=st;
   if(p!=-1)
     price=p;
  }

  return k;

 }

 int gadget::input()
  {
   cout<<"\n\t\tENTER CODE : ";
   gets(code);
   int k=gdcheck(code);
   if(k==0)
   {
    cout<<"\n\n\t\t CODE ALREADY PRESENT !!!\n\n";
    sound(900);
    delay(300);
    nosound();
   }

   else
   {
   cout<<"\t\tENTER TYPE : ";
   gets(type);
   cout<<"\t\tENTER COMPANY : ";
   gets(cmp);
   cout<<"\t\tENTER MODEL : ";
   gets(model);
   cout<<"\t\tENTER PRICE : ";
   cin>>price;
   cout<<"\t\tENTER STOCK : ";
   cin>>stock;

   }
   return k;
  }


   void gadget::display(int k)
  {
   int x=7,y=10;
   y=y+(k*2);
   if(k!=1)
    x=x+k-1;
   if(k==1)
   { gotoxy(x-k,y-4);
     cout<<"CODE       TYPE       COMPANY       MODEL      PRICE      STOCK";
   }
   x=x-k;
   gotoxy(x,y);     cout<<code;

   int l=strlen(type);
   l=l/2;
   x=x+13;
   gotoxy(x-l,y);
   cout<<type;

   int l1=strlen(cmp);
   l1=l1/2;
   x=x+13;
   gotoxy(x-l1-1,y);
   cout<<cmp;

   x=x+12;
   int l2=strlen(model);
   l2=l2/2;
   gotoxy(x-l2,y);
   cout<<model;

   x=x+9;
   gotoxy(x,y);
   cout<<price;

   x=x+13;
   gotoxy(x,y);
   cout<<stock;
   if(::flag==0)
    delay(150);
  }
//----------------------------------------------------------------------------

void gadgets()
 {
   ::flag=0;

   arrow();
   box();
   int x=30,y=18;
   int y1=y;
   gotoxy(x,y1);
    cout<<"  INPUT NEW GADGET";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  DELETE GADGET ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  VIEW ALL GADGET ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  MODIFY GADGET ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  BACK ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  EXIT ";

   gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for(i=0;;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==6)
   {
     cout<<"\b  ";
     x=30;
     y=18;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<6)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=28;
    gotoxy(x,y);
    cout<<"";
    k=6;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }

   if(a==13)
    break;
   if(a==8)
    admin();
  }

  if(k==1)
   gdinput();
  else if(k==2)
   gddelete();
  else if(k==3)
   gddisplay(1);
  else if(k==4)
   gdmodify();
  else if(k==5)
   admin();
  else
   exit(0);
 }
  void cddisp()
 {
  gadget g;
  ifstream f;
  for(int i=1;i<=50;i++)
  { gotoxy(70,i);
    cout<<"|";  }

  int x=73,y=6;
  gotoxy(x-1,y-3);
  cout<<"GADGETS";
  gotoxy(x,y-2);
  cout<<"CODE";
  f.open("GADGET",ios::in | ios::binary);
  f.seekg(0);
  while(!f.eof())
  {
   f.read((char *)&g,sizeof(g));
   if(!f.eof())
    {
     gotoxy(x,y);
     cout<<g.code;
     y++;
    }
  }
  if(y==6)
  {
   gotoxy(x-2,y);
   cout<<"NO GADGET";
  }
  f.close();
 }

 int gdcheck(char code[])
 {
   gadget g;
   ifstream f;
   int k=1;
   f.open("GADGET",ios::in|ios::binary);
   while(!f.eof())
   {
     f.read((char*)&g,sizeof(g));
      if(strcmp(g.code,code)==0)
      {
       k=0;
       break;
      }
   }
   f.close();
   return k;
  }


   //-------------------------------------------------------------------------

 void gdinput()
 {
  clrscr();
  ofstream f;
  gadget g;
  char opt='y';
  f.open("GADGET",ios::out|ios::app|ios::binary);
  while(opt=='y'||opt=='Y')
  {
   int k=g.input();
   if(k==1)
    f.write((char *)&g,sizeof(g));
   cout<<"\nDO YOU WANT TO ENTER MORE(Y/N): ";
   cin>>opt;
  }

  f.close();
  getch();
  gadgets();
 }
 //--------------------------------------------------------------------------
 void gddisplay(int c)
 {
  //stock();
  clrscr();
  ifstream f;
  gadget g;
  f.open("GADGET",ios::in|ios::binary);
  int k=1;
  if(::flag==0)
   delay(300);
  while(!f.eof())
  {
   f.read((char *)&g,sizeof(g));
   if(!f.eof())
    {
     g.display(k);
     k++;
    }
  }
  if(k==1)
   {
    cout<<"\n\n\n\n\t\t\tNO GADGETS FOUND !!!!! ";
    sound(900);
    delay(300);
    nosound();
   }
  f.close();
  ::flag++;
  if(c==1)
  {
   getch();
   gadgets();
  }
  else
  nuser(2);
 }
 //----------------------------------------------------------------------------

 void gddelete()
 {
  clrscr();
  cddisp();
  gadget g;
  ifstream f;
  ofstream f1;
  f.open("GADGET",ios::in|ios::binary);
  f1.open("GAD",ios::out|ios::binary);
  char code[5];
  gotoxy(2,4);
  int y=0;
  cout<<"ENTER THE CODE TO DELETE:-  ";
  gets(code);
  if(strcmp(code,"back")==0 || strcmp(code,"Back")==0 || strcmp(code,"BACK")==0)
  {
   f.close();
   f1.close();
   gadgets();
  }

  while(!f.eof())
  {
   f.read((char*)&g,sizeof(g));
   if(!f.eof())
   {
    if(strcmp(g.code,code)!=0)
    {
     f1.write((char*)&g,sizeof(g));
     }
    else
    {
     y++;
     cout<<"\n  YOUR GADGET IS: ";
     g.display(1);
     cout<<"\n\n\n\t ARE YOU SURE YOU WANT TO DELETE GADGET (Y/N):";
     char a;
     cin>>a;
     if(a!='y')
      f1.write((char *)&g,sizeof(g));
    }

   }
  }

  if(y==0)
  {
   cout<<"\n\n\n\t\t CODE NOT FOUND!!!!";
   sound(900);
   delay(300);
   nosound();
  }
  f.close();
  f1.close();
  remove("GADGET");
  rename("GAD","GADGET");

  char a;
  cout<<"\n\n\t DO YOU WANT TO DELETE ANYMORE (Y/N): ";
  cin>>a;
  if(a=='y'||a=='Y')
   gddelete();
  else
   gadgets();
 }

 //--------------------------------------------------------------------------

 void gdmodify()
 {
  clrscr();
  gadget g;
  fstream f;
  f.open("GADGET",ios::in | ios::out| ios::binary);
  char c[5],opt;
  int g1,y=0;
  cout<<"\n\tENTER THE CODE YOU WANT TO MODIFY: ";
  cddisp();
  gotoxy(45,2);
  gets(c);
  f.seekg(0);
  while(!f.eof())
  {
   g1=f.tellg();
   f.read((char *)&g , sizeof(g));
   if(!f.eof())
   {
    if(strcmp(c,g.code)==0)
    {
     gotoxy(3,5);
     y++;
     cout<<"YOUR GADGET IS: ";
     g.display(1);
     cout<<"\n\n    ARE YOU SURE YOU WANT TO MODIFY(Y/N): ";
     cin>>opt;
     if(opt=='y')
     {
      int k=g.modify();
      if(k==1)
      {
       f.seekg(g1);
       f.write((char *)&g,sizeof(g));
      }
      else
       {
	cout<<"\n\n GADGET CODE ALREADY PRESENT !!!! ";
	sound(900);
	delay(300);
	nosound();
       }
     }
     break;
    }
   }
  }

  if(y==0)
   {
    cout<<"\n\n\t\tGADGET NOT FOUND !!!!";
    sound(900);
    delay(300);
    nosound();
   }
  f.close();

  cout<<"\n\n\t DO YOU WANT TO MODIFY MORE(Y/N): ";
  cin>>opt;

  if(opt=='y')
   gdmodify();
  else
   gadgets();
 }



 //--------------------------------------------------------------------------
  class garment {
		  public :

		  char code[5];
		  char gender;
		  char type[10];
		  char cmp[15];
		  char size;
		  int stock;
		  float price;

		  int input();
		  void display(int);
		  int modify();
		 };


 int garment::modify()
 {
  char c[5],g,t[10],cm[15],s;
  int st;
  float p;
  cout<<"\n\n ENTER NEW CODE: ";
  gets(c);
  int k=gcheck(c);
  if(k==1)
  {
   cout<<" ENTER NEW GENDER: ";
   cin>>g;
   cout<<" ENTER NEW TYPE: ";
   gets(t);
   cout<<" ENTER NEW COMPANY: ";
   gets(cm);
   cout<<" ENTER NEW SIZE: ";
   cin>>s;
   cout<<" ENTER NEW PRICE: ";
   cin>>p;
   cout<<" ENTER NEW STOCK: ";
   cin>>st;


   if(strcmp(c,".")!=0)
     strcpy(code,c);
   if(g!='.')
     gender=g;
   if(strcmp(t,".")!=0)
     strcpy(type,t);
   if(strcmp(cm,".")!=0)
     strcpy(cmp,cm);
   if(s!='.')
     size=s;
   if(st!=-1)
     stock=st;
   if(p!=-1)
     price=p;
  }

  return k;

 }


 int garment::input()
  {
   cout<<"\n\t\tENTER CODE : ";
   gets(code);
   int k=gcheck(code);
   if(k==0)
    cout<<"\n\n\t\t CODE ALREADY PRESENT !!!\n\n";
   else
   {
   cout<<"\t\tENTER GENDER : ";
   cin>>gender;
   cout<<"\t\tENTER TYPE : ";
   gets(type);
   cout<<"\t\tENTER COMPANY: ";
   gets(cmp);
   cout<<"\t\tENTER SIZE : ";
   cin>>size;
   cout<<"\t\tENTER PRICE : ";
   cin>>price;
   cout<<"\t\tENTER STOCK : ";
   cin>>stock;

   }
   return k;
  }


  void garment::display(int k)
  {
   int x=7,y=10;
   y=y+(k*2);

   if(k==1)
     cout<<"\n\n\n      CODE   GENDER     TYPE        COMPANY     SIZE   PRICE   STOCK ";

   gotoxy(x,y);     cout<<code;  x=x+9;
   gotoxy(x,y);   cout<<gender;
   int l=strlen(type);
   l=l/2;
   x=x+11;
   gotoxy(x-l,y);
   cout<<type;

   int l1=strlen(cmp);
   l1=l1/2;
   x=x+14;
   gotoxy(x-l1-1,y);
   cout<<cmp;

   x=x+10;
   gotoxy(x,y);
   cout<<size;

   x=x+5;
   gotoxy(x,y);
   cout<<price;

   x=x+9;
   gotoxy(x,y);
   cout<<stock;
   if(::flag==0)
   delay(150);
    }
  //--------------------------------------------------------------------------
 void cdisp()
 {
  garment g;
  ifstream f;
   for(int i=1;i<=50;i++)
  { gotoxy(70,i);
    cout<<"|";  }
  int x=73,y=6;
  gotoxy(x-1,y-3);
  cout<<"GARMENT";
  gotoxy(x,y-2);
  cout<<"CODE";
  f.open("GARMENT",ios::in | ios::binary);
  f.seekg(0);
  while(!f.eof())
  {
   f.read((char *)&g,sizeof(g));
   if(!f.eof())
    {
     gotoxy(x,y);
     cout<<g.code;
     y++;
    }
  }
  if(y==6)
  {
   gotoxy(x-2,y);
   cout<<"NO GARMENT";
  }
  f.close();
 }

 //--------------------------------------------------------------------------

 int gcheck(char code[])
 {
   garment g;
   ifstream f;
   int k=1;
   f.open("GARMENT",ios::in|ios::binary);
   while(!f.eof())
   {
     f.read((char*)&g,sizeof(g));
      if(strcmp(g.code,code)==0)
      {
       k=0;
       break;
      }
   }
   f.close();
   return k;
  }

 //--------------------------------------------------------------------------

 void garments()
 {
   ::flag=0;
   arrow();
   box();
   int x=30,y=18;
   int y1=y;
   gotoxy(x,y1);
    cout<<"  INPUT NEW GARMENT";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  DELETE GARMENT ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  VIEW ALL GARMENT ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  MODIFY GARMENT ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  BACK ";
   y1+=2;
   gotoxy(x,y1);
    cout<<"  EXIT";

   gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for(i=0;;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==6)
   {
     cout<<"\b  ";
     x=30;
     y=18;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<6)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=28;
    gotoxy(x,y);
    cout<<"";
    k=6;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
   if(a==8)
    admin();
  }

  if(k==1)
   ginput();
  else if(k==2)
   gdelete();
  else if(k==3)
   gdisplay(1);
  else if(k==4)
   gmodify();
  else if(k==5)
   admin();
  else
   exit(0);
 }
 //-------------------------------------------------------------------------

 void ginput()
 {
  clrscr();
  ofstream f;
  garment g;
  char opt='y';
  f.open("GARMENT",ios::out|ios::app|ios::binary);
  while(opt=='y'||opt=='Y')
  {
   int k=g.input();
   if(k==1)
    f.write((char *)&g,sizeof(g));
   cout<<"\nDO YOU WANT TO ENTER MORE(Y/N): ";
   cin>>opt;
  }

  f.close();
  getch();
  garments();
 }
 //--------------------------------------------------------------------------
 void gdisplay(int c)
 {
  //stock();
  clrscr();
  ifstream f;
  garment g;
  f.open("GARMENT",ios::in|ios::binary);
  int k=1;
  cout<<"\n\n\n\n";
  if(::flag==0)
  delay(300);
  while(!f.eof())
  {
   f.read((char *)&g,sizeof(g));
   if(!f.eof())
    {
     g.display(k);
     k++;
    }
  }
  if(k==1)
   {
    cout<<"\n\n\n\n\t\t\tNO GARMNETS FOUND !!!!! ";
    sound(900);
    delay(300);
    nosound();
   }
  f.close();
  ::flag++;
  if(c==1)
   {
    getch();
    garments();
   }
  else
   nuser(1);
 }
 //----------------------------------------------------------------------------

 void gdelete()
 {
  clrscr();
  cdisp();
  garment g;
  ifstream f;
  ofstream f1;
  f.open("GARMENT",ios::in|ios::binary);
  f1.open("GAR",ios::out|ios::binary|ios::trunc);
  char code[5];
  gotoxy(2,4);
  int y=0;
  cout<<"ENTER THE CODE TO DELETE:-  ";
  gets(code);
  if(strcmp(code,"back")==0 || strcmp(code,"Back")==0 || strcmp(code,"BACK")==0)
  {
   f.close();
   f1.close();
   garments();
  }

  while(!f.eof())
  {
   f.read((char*)&g,sizeof(g));
   if(!f.eof())
   {
    if(strcmp(g.code,code)!=0)
      f1.write((char*)&g,sizeof(g));
    else
    {
     y++;
     cout<<"\n YOUR GARMENT IS: ";
     g.display(1);
     cout<<"\n   ARE YOU SURE YOU WANT TO DELETE GARMENT(Y/N):";
     char a;
     cin>>a;
     if(a!='y')
     f1.write((char *)&g,sizeof(g));
    }
   }
  }

  if(y==0)
  {
   cout<<"\n\n\t\tCODE NOT FOUND!!!!";
   sound(900);
   delay(300);
   nosound();
  }

  f.close();
  f1.close();
  remove("GARMENT");
  rename("GAR","GARMENT");

  char a;
  cout<<"\n\n  DO YOU WANT TO DELETE ANYMORE (Y/N): ";
  cin>>a;
  if(a=='y'||a=='Y')
   gdelete();
  else
   garments();
 }

 //--------------------------------------------------------------------------

 void gmodify()
 {
  clrscr();
  garment g;
  fstream f;
  f.open("GARMENT",ios::in | ios::out| ios::binary);
  char c[5],opt;
  int g1,y=0;
  cout<<"\n\tENTER THE CODE YOU WANT TO MODIFY: ";
  cdisp();
  gotoxy(45,2);
  gets(c);
  f.seekg(0);
  while(!f.eof())
  {
   g1=f.tellg();
   f.read((char *)&g , sizeof(g));
   if(!f.eof())
   {
    if(strcmp(c,g.code)==0)
    {
     y++;
     cout<<"\n\nYOUR GARMENT IS: ";
     g.display(1);
     cout<<"\n\n\t ARE YOU SURE YOU WANT TO MODIFY(Y/N): ";
     cin>>opt;
     if(opt=='y')
     {
      int k=g.modify();
      if(k==1)
      {
       f.seekg(g1);
       f.write((char *)&g,sizeof(g));
      }
      else
       {
	cout<<"\n\n GARMENT CODE ALREADY PRESENT !!!! ";
	sound(900);
	delay(300);
	nosound();
       }
     }
     break;
    }
   }
  }

  if(y==0)
   {
    cout<<"\n\n\t\tGARMENT NOT FOUND !!!!";
    sound(900);
    delay(300);
    nosound();
   }

  f.close();

  cout<<"\n\n\n\n DO YOU WANT TO MODIFY MORE(Y/N): ";
  cin>>opt;

  if(opt=='y')
   gmodify();
  else
   garments();
 }


 //--------------------------------------------------------------------------
 void admin()
  {
   ::flag=0;

   arrow();
   box();
   int x=31,y=19;
   int y1=y;
   gotoxy(x,y1);
    cout<<" GARMENTS ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" GADGETS ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" BACK ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" EXIT";

   x=x-1;
  gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for(i=0; ;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==4)
   {
     cout<<"\b  ";
     x=30;
     y=19;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<4)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=25;
    gotoxy(x,y);
    cout<<"";
    k=4;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
   if(a==8)
    mainmenu();
  }
  if(k==1)
   garments();
  else if(k==2)
   gadgets();
  else if(k==3)
   mainmenu();
  else
   exit(0);

 }

//---------------------------------------------------------------------------

 void mainmenu()
 {
  arrow();
  box();
  int x=31,y=19;
  gotoxy(x,y);
   cout<<" VISIT THE WEB ";
  int y1=y+2;
  gotoxy(x,y1);
   cout<<" TERMS & CONDITIONS ";
  y1+=2;
  gotoxy(x,y1);
   cout<<" ADMINISTRATOR";
  y1+=2;
  gotoxy(x,y1);
   cout<<" EXIT ";

  x=x-1;
  gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for( i=0; ;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==4)
   {
     cout<<"\b  ";
     x=30;
     y=19;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<4)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=25;
    gotoxy(x,y);
    cout<<"";
    k=4;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
  }
  if(k==1)
   user();
  else if(k==2)
   tc();
  else if(k==3)
   admin();
  else
   exit(0);
 }

//--------------------------------------------------------------------------
void user()
 {
   arrow();
   box();
   ::flag=0;
   int x=31,y=19;
   int y1=y;
   gotoxy(x,y1);
    cout<<" GARMENTS ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" GADGETS ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" SEARCH ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" KART ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" BACK ";
   y1+=2;
   gotoxy(x,y1);
    cout<<" EXIT";

   x=x-1;
  gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for(i=0; ;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==6)
   {
     cout<<"\b  ";
     x=30;
     y=19;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<6)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=29;
    gotoxy(x,y);
    cout<<"";
    k=6;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
   if(a==8)
    mainmenu();
  }

  if(k==1)
   gdisplay(2);
  else if(k==2)
   gddisplay(2);
  else if(k==3)
   search();
  else if(k==4)
   plist();
  else if(k==5)
   mainmenu();
  else
   exit(0);
 }
//--------------------------------------------------------------------------
void search()
  {
   clrscr();
   char a;
   char b[30]={""};
   int x=22,y=13,k=22;
   for(int i=0;i<20;i++)
   {
   if(x<22)
    {
     x=22;
     i=0;
     gotoxy(x,y);
    }
    serbox();
    gotoxy(k,y);
    cout<<b;
    gotoxy(x,y);
    a=getch();
    if(a==13)
      break;

    if(a==8)
    {
     b[i-1]='\0';
     x--;
     i-=2;
    }
    else
    {
     b[i]=a;
     b[i+1]='\0';
     x++;
    }
    ser(b);
   }
   user();
  }
//--------------------------------------------------------------------------
void ser(char b[])
 {
   clrscr();
   int flag=0;
   int x=20,y=20;
   ifstream f;
   garment g;
   f.open("GARMENT",ios::in||ios::binary);
   while(!f.eof())
   {
    int k=0,k1=0,k2=0;
    f.read((char *)& g,sizeof(g));
    if(!f.eof())
    {
     for(int j=0;b[j]!='\0';j++)
	if( b[j]==g.code[j]  ||  b[j]==g.code[j]+32  ||  b[j]==g.code[j]-32 )   k++;
	else
	 {
	   k=0;
	   break;
	 }
     for(j=0;b[j]!='\0';j++)
	if(b[j]==g.cmp[j]||b[j]==g.cmp[j]-32||b[j]==g.cmp[j]+32)    k1++;
	else
	 {
	   k1=0;
	   break;
	 }

     for(j=0;b[j]!='\0';j++)
	if(b[j]==g.type[j]||b[j]==g.type[j]+32||b[j]==g.type[j]-32)    k2++;
	else
	 {
	   k2=0;
	   break;
	 }

     if(k>0 || k1>0 ||k2>0)
      {
       flag++;
       int u=x;
       x+=5;
       gotoxy(x,y);     cout<<g.code;  x=x+9;
       int l=strlen(g.type);
       l=l/2;
       gotoxy(x-l,y);
       cout<<g.type;

       int l1=strlen(g.cmp);
       l1=l1/2;
       x=x+14;
       gotoxy(x-l1-1,y);
       cout<<g.cmp;

       x=x+9;
       gotoxy(x,y);
       cout<<g.price<<" RS.";

	x=u;
	y+=2;
      }
    }
  }
  y++;
  f.close();
  gadget gd;
  f.open("GADGET",ios::in||ios::binary);
  while(!f.eof())
   {
    int k=0,k1=0,k2=0,k3=0;
    f.read((char *)& gd,sizeof(gd));
    if(!f.eof())
    {
     for(int j=0;b[j]!='\0';j++)
	if(b[j]==gd.code[j]||b[j]==gd.code[j]-32||b[j]==gd.code[j]+32)   k++;
	else
	 {
	   k=0;
	   break;
	 }
     for(j=0;b[j]!='\0';j++)
	if(b[j]==gd.cmp[j]||b[j]==gd.cmp[j]+32||b[j]==gd.cmp[j]-32)    k1++;
	else
	 {
	   k1=0;
	   break;
	 }

     for(j=0;b[j]!='\0';j++)
	if(b[j]==gd.model[j]||b[j]==gd.model[j]+32||b[j]==gd.model[j]-32)    k2++;
	else
	 {
	   k2=0;
	   break;
	 }

     for(j=0;b[j]!='\0';j++)
	if(b[j]==gd.type[j] || b[j]==gd.type[j]-32 || b[j]==gd.type[j]+32)    k3++;
	else
	 {
	   k3=0;
	   break;
	 }

     if(k>0 || k1>0 ||k2>0 ||k3>0)
      {
	flag++;
	int  u=x;
	x-=3;
	gotoxy(x,y);
	cout<<gd.code;
	int l=strlen(gd.type);
	l=l/2;
	x=x+13;
	gotoxy(x-l,y);
	cout<<gd.type;

	int l1=strlen(gd.cmp);
	l1=l1/2;
	x=x+13;
	gotoxy(x-l1-1,y);
	cout<<gd.cmp;

	x=x+12;
	int l2=strlen(gd.model);
	l2=l2/2;
	gotoxy(x-l2,y);
	cout<<gd.model;

	x=x+9;
	gotoxy(x,y);
	cout<<gd.price<<" RS.";

	x=u;
	y+=2;
      }
    }
  }
  f.close();
  if(flag==0 && b[0]!='\0')
  {
  gotoxy(x-1,y);
  cout<<"___________________NO RESULT__________________";
  }

 }
//--------------------------------------------------------------------------

 void serbox()
 {
  int x=19,y=11;
  gotoxy(x,y);
  cout<<"ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿";  y++;
  gotoxy(x,y);
  cout<<"³                                            ³";  y++;
  gotoxy(x,y);
  cout<<"³                                            ³";  y++;
  gotoxy(x,y);
  cout<<"³                                            ³";  y++;
  gotoxy(x,y);
  cout<<"ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ";
 }


//---------------------------------------------------------------------------
 void nuser(int l)
 {
  char c[5];
  ::flag++;
  cout<<"\n\n  ENTER THE CODE TO ADD TO KART: ";
  cin>>c;
  if(strcmp(c,"back")==0 || strcmp(c,"Back")==0 || strcmp(c,"BACK")==0 )
   user();
  int d=pcheck(c);

  if(d==0)
  {
  ifstream f;
  garment g;

  f.open("GARMENT",ios::in|ios::binary);
  int k=1;                  // to check for presence of code.
  while(!f.eof())
  {
   f.read((char *)&g,sizeof(g));
   if(strcmp(g.code,c)==0)
    {
     k++;
     cout<<" \n\n\tYOUR GARMENT HAVE BEEN ADDED TO KART !!!! ";
     getch();
     strcpy(s.code[s.n],g.code);
     s.n++;
     break;
    }
  }
  f.close();

  gadget gd;
  f.open("GADGET",ios::in|ios::binary);
  f.seekg(0);
  while(!f.eof())
  {
   f.read((char *)&gd,sizeof(gd));
   if(!f.eof())
   if(strcmp(gd.code,c)==0)
    {
     k++;
     cout<<"\n\n\n\n\t YOUR GADGET HAVE BEEN ADDED TO KART!!!! ";
     getch();
     strcpy(s.code[s.n],gd.code);
     s.n++;
     break;
    }
  }
  f.close();
  if(k==1)
   {
    cout<<"\n\n\n\t\t\tCODE NOT FOUND !!!!! ";
    sound(900);
    delay(200);
    nosound();
    getch();
   }
  }
  else
  { cout<<"\n\n\n\n\t\t  YOUR KART ALREADY CONTAIN THIS ITEM";
   sound(900);
   delay(200);
    nosound();
   getch();
  }
  if(l==1)
   gdisplay(2);
  else
   gddisplay(2);
 }
//--------------------------------pcheck--------------------------------------
int pcheck(char a[])
{
  for(int i=0;i<s.n;i++)
    if(strcmp(s.code[i],a)==0)
      return 1;
  return 0;
}
//----------------------------Function of Purchase list------------------------------

 void plist()
 {
  clrscr();
  arrow();
  box();
  int x=31,y=19;
  int y1=y;
  gotoxy(x,y1);
   cout<<" VIEW KART";
  y1+=2;
  gotoxy(x,y1);
   cout<<" DELETE FROM KART";
  y1+=2;
  gotoxy(x,y1);
   cout<<" BACK";
  y1+=2;
  gotoxy(x,y1);
   cout<<" EXIT";

  x=x-1;
  gotoxy(x,y);
  cout<<"";

  int k=1,i;

  for(i=0; ;i++)
  {
   char a;
   a=getch();
   if(a==80 && k==4)
   {
     cout<<"\b  ";
     x=30;
     y=19;
     gotoxy(x,y);
     cout<<"";
     k=1;
   }
   else
   if(a==80 && k<4)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k==1)
   {
    cout<<"\b ";
    x=30; y=25;
    gotoxy(x,y);
    cout<<"";
    k=4;
   }
   else
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
   if(a==8)
    user();
  }

  if(k==1)
   dplist(0);
  else if(k==2)
   delp();
  else if(k==3)
   user();
  else
   exit(0);

 }


//--------------------------Display Purchase List----------------------------------------

 int dplist(int h)
 {
  clrscr();
   char cmp[20],type[15];
   float price;
   ifstream f;
   float tot=0;
   int x=25,y=9;
  for(int i=0;i<s.n;i++)
  {
     garment g;
     f.open("GARMENT",ios::in|ios::binary);

    while(!f.eof())
    {
     f.read((char *)&g,sizeof(g));
     if(!f.eof())
     {
     if(strcmp(g.code,s.code[i])==0)
     {
      strcpy(cmp,g.cmp);
      strcpy(type,g.type);
      price=g.price;
       break;
     }
     }
    }
    f.close();

    gadget gd;
    f.open("GADGET",ios::in|ios::binary);
    while(!f.eof())
    {
     f.read((char *)&gd,sizeof(gd));
     if(strcmp(gd.code,s.code[i])==0)
     {
      strcpy(cmp,gd.cmp);
      strcpy(type,gd.type);
      price=gd.price;
       break;
     }
    }
    f.close();
   if(i==0)
    {
    cout<<"  \n\n\t\tÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿ ";
    cout<<"\n\t\t³                 ³               ³              ³ ";
    cout<<"\n\t\t³     COMPANY     ³     TYPE      ³    PRICE     ³ ";
    cout<<"\n\t\t³                 ³               ³              ³ ";
    cout<<"\n\t\tÃÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÄÄÄÄÄÄ´ ";
    cout<<"\n\t\t³                 ³               ³              ³ ";
    }
   cout<<"\n\t\t³\n\t\t³";
   int l1=strlen(cmp);
   l1=l1/2;
   gotoxy(x-l1+1,y);
   cout<<cmp;
   gotoxy(35,y);
   cout<<"³";
   gotoxy(35,y+1);
   cout<<"³";
   x+=19;
   int l2=strlen(type);
   l2=l2/2;
   gotoxy(x-l2-1,y);
   cout<<type;
   x+=12;
   gotoxy(x,y);
   cout<<price;
   gotoxy(51,y);
   cout<<"³";
   gotoxy(51,y+1);
   cout<<"³";
   gotoxy(66,y);
   cout<<"³";
   gotoxy(66,y+1);
   cout<<"³";
   tot=tot+price;
   if(i==s.n-1)
   {
    cout<<"\n\t\tÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÄÄÄÄÄÄ´ ";
    cout<<"\n\t\t                  ³     TOTAL  :  ³              ³ ";
    cout<<"\n\t\t                  ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÁÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ ";
   gotoxy(56,y+3);
   cout<<tot;
   }

   y+=2;
   x=25;

 }
 if(s.n==0)
   cout<<"\n\n\n\n\n\t\tYOU HAVE NOT PURCHASE ANY ITEM YET !!!";

 else if(h==0)
  {
   cout<<"\n\n\n\n\n\n\n\n\n\t\t\t PAY YOUR BILL";
   cout<<"              \n\n\t\t\t BACK";
  int x=24,y=(s.n*2)+19;
  gotoxy(x,y);
  cout<<"";
  int k=1,i;

  for(i=0; ;i++)
  {
   char a;
   a=getch();
   if(a==80 && k<2)
   {
    cout<<"\b ";
    y+=2;
    gotoxy(x,y);
    cout<<"";
    k++;
   }
   if(a==72 && k>1)
   {
    cout<<"\b  ";
    y-=2;
    gotoxy(x,y);
    cout<<"";
    k--;
   }
   if(a==13)
    break;
   if(a==8)
    plist();
  }

  if(k==1)
   bill();
  else if(k==2)
   plist();
  }
  if(h==0)
  {
   getch();
   plist();
  }
  if(h==1 && s.n==0)
  return 0;
  else
  return 1;
}

//-------------------------Delete from kart-----------------------------------

void delp()
{
 int k1=dplist(1);
 if(k1==0)
  {
   getch();
   plist();
  }
 char c[20],t[20],code[5];
 cout<<"\n\n\n\t ENTER INFORMATION OF DELETING ITEM: ";
 cout<<"\n\n\t ENTER COMPANY: ";
 gets(c);
 if(strcmp(c,"empty kart")==0 || strcmp(c,"Empty Kart")==0 || strcmp(c,"Empty kart")==0 ||strcmp(c,"empty Kart")==0 ||strcmp(c,"EMPTY KART")==0)
  {
   cout<<"\n\n\tARE YOU SURE YOU WANT TO EMPTY KART(Y/N): ";
   char opt;
   cin>>opt;
   if(opt=='y' || opt=='Y')
   {
    s.n=0;
    cout<<"\n\n\tYOUR KART HAVE BEEN EMPTIED";
    getch();
    plist();
   }
   else
   delp();
  }
 cout<<"\n\t ENTER TYPE: ";
 gets(t);
 int k=0;
 ifstream f("GARMENT",ios::in);
 garment g;
 while(!f.eof())
 {
  f.read((char*)&g,sizeof(g));
  if(strcmp(g.cmp,c)==0 && strcmp(g.type,t)==0)
  {k++;
   strcpy(code,g.code);
   break;}
 }
 f.close();

 if(k==0)
 {
 f.open("GADGET",ios::in);
 gadget gd;
 while(!f.eof())
 {
  f.read((char*)&gd,sizeof(gd));
  if(strcmp(gd.cmp,c)==0 && strcmp(gd.type,t)==0)
  {
   k++;
   strcpy(code,gd.code);
   break;
  }
 }
 }
 f.close();

 if(k==0)
  cout<<"\n\n\n\t\t ITEM DOES NOT PRESENT!!!! ";
 else
 {
 for(int i=0;i<s.n;i++)
 {
  if(strcmp(s.code[i],code)==0)
  {
    for(int j=i;j<s.n-1;j++)
     strcpy(s.code[j],s.code[j+1]);
   s.n--;
  }
 }
 }
 cout<<"\n\n\tDO YOU WANT TO DELETE ANY MORE(Y/N): ";
 char opt;
 cin>>opt;
 if(opt=='y'||opt=='Y')
 delp();
 else
  dplist(0);
}




//-----------------------Function to make bill--------------------------------

 void bill()
 {
  clrscr();
  struct date d;
  getdate(&d);
  int d1=d.da_day;
  int m1=d.da_mon;
  int y1=d.da_year;

  char n1[10],n2[10],ad[50],cty[10],st[10],id[30];
  long pc,pn;
   cout<<"\n\n ENTER YOUR INFORMATION: ";
   cout<<"\n\n\t FIRST NAME: ";
     gets(n1);
   cout<<"\n\t SECOND NAME: ";
     gets(n2);
   cout<<"\n\t ADDRESS: ";
     gets(ad);
   cout<<"\n\t CITY: ";
     gets(cty);
   cout<<"\n\t POSTAL CODE: ";
     cin>>pc;
   cout<<"\n\t STATE: ";
     gets(st);
   cout<<"\n\t EMAIL ID: ";
     gets(id);
   cout<<"\n\t CONTACT NUMBER: ";
     cin>>pn;

   cout<<"\n\nSELECT WAY OF PAYMENT: ";
    cout<<"\n\n\t CREDIT CARD";
    cout<<"\n\n\t CASH ON DELIVERY.";

   int x2=8,y2=24,t=1;
   char e;
   gotoxy(x2,y2);
     cout<<"";
   for(int u=0;;u++)
   {
   char a;
   a=getch();
    if(a==80 && t<2)
   {
    cout<<"\b ";
    y2+=2;
    gotoxy(x2,y2);
    cout<<"";
    t++;
   }
   if(a==72 && t>1)
   {
    cout<<"\b  ";
    y2-=2;
    gotoxy(x2,y2);
    cout<<"";
    t--;
   }
   if(a==13)
    break;
  }

  if(t==1)
   {
    char cc[25];
    cout<<"\n\n\n\nENTER CREDIT CARD NUMBER:(xxxx-xxxx-xxxx-xxxx-xxxx)\n\n\t\t\t  ";
    for(int i=1;i<=20;i++)
    {
     char a=getch();
     cout<<a;
     cc[i-1]=a;
     if(i==20)
      break;
     if(i%4==0)
      cout<<"-";
    }
    cc[i-1]='\0';
   }
   if(t==2)
    cout<<"\n\n\n\n    YOUR PAYMENT WILL BE TAKEN ON DELIVERY";

   int d2,m2,y3;
   d2=d1;
   m2=m1;
   y3=y1;
   d2=d2+3;
   if(d2>31)
   {

    d2=d2-31;
    m2++;
    if(m2>12)
    {
     m2=m2-12;
     y3++;
    }
   }
   cout<<"\n\n\n\t YOU WILL RECEIVE YOUR PRODUCT ON : "<<d2<<"/"<<m2<<"/"<<y3;
   cout<<"\n\n\n PRESS ANY KEY TO SEE YOUR BILL......>>>> ";
  getch();

  clrscr();

  //   Á Â º  Í ¼ Ä È À É  »   Å   Ù  Ú  ¿ ¶  Ç  ³

cout<<"\n\n\n\n\n\n      ÉÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍ»\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                 DATE:  /  /      º\n";
cout<<"      ÇÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄ¶\n";
cout<<"      º SR NO.³                COMPANY                  ³QUANTITY³ PRICE º\n";
cout<<"      ºÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄÄÅÄÄÄÄÄÄÄº\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      º       ³                                         ³        ³       º\n";
cout<<"      ÇÄÄÄÄÄÄÄÁÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÁÄÄÄÄÄÄÄÄÁÄÄÄÄÄÄÄ¶\n";
cout<<"      º                                                   TOTAL:         º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      º                                                                  º\n";
cout<<"      ÈÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍÍ¼\n";


  char cmp[20],type[15];
  float price;
  fstream f;
  garment g;
  gadget gd;

  int y=15,x=62;
  gotoxy(x,y);
   cout<<d1;
   x=x+3;
  gotoxy(x,y);
   cout<<m1;
   x=x+3;
  gotoxy(x,y);
   cout<<y1;

  x=11,y=21;
  long int totprice=0;

  for(int i=0;i<s.n;i++)
  {
  f.open("GARMENT",ios::in|ios::binary);
   while(!f.eof())
   {
    f.read((char *)&g,sizeof(g));
    if(strcmp(g.code,s.code[i])==0)
      {
       strcpy(cmp,g.cmp);
       strcpy(type,g.type);
       price=g.price;
       break;
      }
   }
  f.close();
  f.open("GADGET",ios::in|ios::binary);
  while(!f.eof())
  {
   f.read((char *)&gd,sizeof(gd));
   if(strcmp(gd.code,s.code[i])==0)
     {
      strcpy(cmp,gd.cmp);
      strcpy(type,gd.type);
      price=gd.price;
      break;
     }
  }
  f.close();
 gotoxy(x,y);
  cout<<i+1<<".";
 int l1=strlen(cmp);
 int l2=strlen(type);
 int l=l1+l2;
 x=x+24;
 l=l/2;
 gotoxy(x-l,y);
  cout<<cmp;
  cout<<" ("<<type<<")";
 x=x+26;
 gotoxy(x,y);
  cout<<"1";
 x=x+7;
 gotoxy(x,y);
  cout<<price;
 totprice+=price;
 y=y+2;
 x=11;
}
 gotoxy(67,39);
 cout<<totprice;
 ustock();
 s.n=0;
 getch();
 mainmenu();
}

//----------------------Function to make box----------------------------------

 void box()
 {
  gotoxy(19,12);
  cout<<"É";
  for(int i=0;i<44;i++)
   cout<<"Í";
   cout<<"»";
  for(int j=13;j<35;j++)
  {
   gotoxy(19,j);
   cout<<"º";
   for(int k=0;k<44;k++)
    cout<<" ";
   cout<<"º";
  }
  gotoxy(19,j);
  cout<<"È";
  for( i=0;i<44;i++)
   cout<<"Í";
  cout<<"¼";
 }
//----------------------------------------------------------------------------
 void stock()
 {
  garment g;
  ifstream f("GARMENT",ios::in|ios::binary);
  ofstream of("TEMP1",ios::out|ios::binary|ios::trunc);
  while(!f.eof())
  {
    f.read((char *)&g,sizeof(g));
    if(!f.eof())
    {
     if(g.stock>0)
     of.write((char*)&g,sizeof(g));
    }
  }
  remove("GARMENT");
  rename("TEMP1","GARMENT");
  f.close();
  of.close();

  gadget gd;
  f.open("GADGET",ios::in|ios::binary);
  of.open("TEMP2",ios::out|ios::binary|ios::trunc);
  while(!f.eof())
  {
    f.read((char *)&gd,sizeof(gd));
    if(!f.eof())
    {
     if(gd.stock>0)
     of.write((char*)&gd,sizeof(gd));
    }
  }
  remove("GADGET");
  rename("TEMP2","GADGET");
  f.close();
  of.close();
 }
//-----------------------------USTOCK-----------------------------------------
void ustock()
{
 fstream f,f1;
 garment g;
 gadget gd;
 int pos=0;
  for(int i=0;i<s.n;i++)
 {
 f.open("GARMENT",ios::in|ios::out|ios::binary);
 f1.open("GADGET",ios::in|ios::out|ios::binary);
 while(!f.eof())
 {
  pos=f.tellg();
  f.read((char*)&g,sizeof(g));
  if(!f.eof())
  {
   if(strcmp(g.code,s.code[i])==0)
   {
    g.stock--;
    f.seekg(pos);
    f.write((char*)&g,sizeof(g));
   }
  }
 }
 f.close();
 while(!f1.eof())
 {
  pos=f1.tellg();
  f1.read((char*)&gd,sizeof(gd));
  if(!f1.eof())
  {
   if(strcmp(gd.code,s.code[i])==0)
   {
    gd.stock--;
    f1.seekg(pos);
    f1.write((char*)&gd,sizeof(gd));
   }
  }
 }
 f1.close();
 }
}
//----------------------------VOID MAIN--------------------------------------

 void main()
 {
  clrscr();
  mainmenu();
  getch();
 }