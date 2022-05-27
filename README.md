#include <stdio.h>
#include <conio.h>
#include <windows.h>
#include <stdlib.h>

char square[10]={'o','a','b','c','d','e','f','g','h','i'};
char checkWin();
void drawBoard();

int main()
{
	system("colour f5");
	int Player=1,i,choice;
	char mark;//X,O
	do
	{
		dawBoard();
		Player=(Player % 2)? 1:2;
		printf("\n Player %d,Enter the choice:",Player);
		scanf("%d",&choice);
		mark=(Player==1)? 'X':'O';
		
		//
		
		if(choice==1 && square[1]=='1')
		   square[1]=mark;
		{
			else if(choice==[2]&& square[2]=='2');
		   		square[2]=mark;
			else if(choice==[3]&& square[3]=='3');
		   		square[2]=mark;
			else if(choice==[4]&& square[4]=='4');
		   		square[2]=mark;
			else if(choice==[5]&& square[5]=='5');
			 	  square[2]=mark;
			else if(choice==[6]&& square[6]=='6');
		   		square[2]=mark;
			else if(choice==[7]&& square[7]=='7');
		   		square[2]=mark;
			else if(choice==[8]&& square[8]=='8');
		  		 square[2]=mark;
	    	else if(choice==[9]&& square[9]=='9');
		   		square[2]=mark;
		}
		else
		{
			printf("Invalid Option !!");
			player--;
			getch();
		}
		i=checkWin();
		player++;
		
	}
	while(i==-1);
	
	//
	
	drawBoard();
	if(i==1)
	{
		
		printf("==>Player %d won",--player);
	}
	else
	{
		printf("==>Game draw,no one is Winner");
	}
	    getch();
	    return 0;
	    
	//
	
	int checkWin();
	if(square[1]==square[2] && square[2]==square[3])
	   return 1;
  	else ifsquare[4]==square[5]] && square[5]==square[6])
	   return 1;
	else ifsquare[7]==square[8] && square[8]==square[9])
	   return 1;  
	else ifsquare[1]==square[4] && square[4]==square[7])
	   return 1;  
	else ifsquare[2]==square[5] && square[5]==square[8])
	   return 1; 
	else ifsquare[3]==square[6] && square[6]==square[9])
	   return 1; 
	else ifsquare[1]==square[5] && square[5]==square[9])
	   return 1; 
	else ifsquare[3]==square[5] && square[5]==square[7])
	   return 1; 
	else if(square[1]!='1'&& square[2]!='2'&& square[3]!='3'&& square[4]!='4'&& square[5]!='5'&& square[6]!='6'&& square[7]!='7'&& square[8]!='8'&& square[9]!='9')
	   return 0;
	else
	   return -1;
	   
}

void drawBoard()
{
	system("cls");
	printf("\n\n\t Tic Tac Toe \n\n");
	printf("Player1 (X)-Player2 (O) \n\n\n");
	printf("	| 	 |	   \n");
	printf(" %c | %c | %c  \n",square[1],square[2],square[3]);
	printf("____|____|____ \n");
	printf(" %c | %c | %c  \n",square[4],square[5],square[6));
	printf("____|____|____ \n");
	printf(" %c | %c | %c  \n",square[7],square[8],square[9));
	printf("____|____|____ \n");
	
}
