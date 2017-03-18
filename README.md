/*
 Let's develop the pseudocode, flowchart, and C++ source code 
 for the following problem:
 
 * Write a program that prompts the user to enter their total assignment 
 percentage, their total quiz percentage, their total discussion board 
 percentage, and their final exam percentage. 
 
 * The program should output the final course grade based on the weights 
 on Professor Conrad's syllabus. 
 
 * You should have four named constants for the weights of the categories, e.g. 
 ASSIGNMENT_WEIGHT should be 0.40 (for 40%), QUIZ_WEIGHT should be 0.20 (for 20%), etc.

At this time, keep the program simple (do not concern output actual letter 
grades to the terminal screen - this could be a future continuation assignment;) 

The program when running should look something similar to:
 */

/* 
 * File:   main.cpp
 * Author: yeseniareyesamado
 *
 * Created on March 18, 2017, 12:29 PM
 */

#include <iostream>
#include<iomanip>
#include<cmath>
using namespace std;

int main()
{
//Constants of student's grades
    const double ASSIGNMENT_WEIGHT = 0.40;
    const double QUIZ_WEIGHT = 0.20;
    const double DISCUSSION_WEIGHT = 0.10; 
    const double FINAL_WEIGHT = 0.30;
    
    //Course inputs
    float assignment,
          quiz,
          discussion,
          final;  
        
    double final_assignment,    //All assignments
           final_quiz,          //All quizzes
           final_discussion,    //All discussions
           final_finale,        //All finals
           FGP;                 //Final grade percentage
    
    cout<< "Please enter the total assignment percentage. \n";
    cin>>assignment;
    cout<< "Please enter the total quiz percentage. \n";
    cin>>quiz;
    cout<< "Please enter the total discussion percentage. \n";
    cin>>discussion;
    cout<< "Please enter the total final percentage. \n";
    cin>>final;
    
           final_assignment = (assignment * ASSIGNMENT_WEIGHT);
           final_quiz = (quiz * QUIZ_WEIGHT);
           final_discussion = (discussion * DISCUSSION_WEIGHT);
           final_finale = (final * FINAL_WEIGHT);
    
         FGP = (final_assignment+final_quiz+final_discussion+final_finale);
         
    cout<<"The final grade percentage for the course was "<<FGP<<endl<<endl;
    
    return 0;
}

