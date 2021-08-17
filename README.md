Top Down and Bottom Up Parsing
=======

This is really good implementation of Parser. We know intuitively how these parsers work, but need to specify some things precisely. Shift operations merely push the indicated state on the stack. A reduce operation has two parts.

Anam Azam Khan - Coder at http://egoseoservices.com

 # include <iostream.h>
 # include   <string.h>
 # include    <conio.h>

 staticchar Stack[50][10]={NULL}; 
 staticint top=-1;
 staticint cit=0;

 // Input Grammarstaticint productions[6]={5,1,7,7,2,10};

 constchar Grammar[5][11][10]={
               {"S","E"},
               {"E","E+T","E-T","E*T","E/T","E%T","E^T","T"},
               {"T","T+F","T-F","T*F","T/F","T%F","T^F","F"},
               {"F","(E)","D"},
               {"D","0","1","2","3","4","5","6","7","8","9"}
             };

 // Input Statementconstint input_length=8;
 char Input[input_length][5]={"2","*","(","3","+","4",")","$"};


 /*************************************Push( ) ***********************/ 
 //--------------------void Push(constchar* Token)---/
 {
    top++;

    strcpy(Stack[top],Token);
 }

\
 {
    strset(Stack[top],NULL);

    top--;
 }

 items,constint index)
 {
    for(int i=0;i<items;i++)
       Pop( );

    Push(Grammar[index][0]);
 }
 {
    Push(Input[cit]);

    cit++;
 }
