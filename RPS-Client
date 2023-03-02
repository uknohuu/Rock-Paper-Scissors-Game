// Program: Rock, Paper, Scissors Game
// Written by: Andrew Nguyen
// Description: User will be asked if they want to play Rock, Paper, or Scissors and then they'll verse the computer best out of 3.
// Challenges::Understanding play() method.
// Time Spent: 4 hours
//
//                   Revision History
// Date:                   By:               Action:
// ---------------------------------------------------
// 05/31/2018         (initals)       Created
 
 
/* filename must be: Anyname.java */
import javax.swing.JOptionPane; //to use gui
import java.util.Random; // for computer generated outcome
public class RPS 
{ 
    static String r = "rock";   //--------------
    static String p = "paper";  //             ----  static Rock, Paper, Scissors
    static String s = "scissors";   //----------
    enum Status {WIN, LOSE, TIE}    //enum for WIN, LOSE, TIE
    
public static void main(String args [ ] ) 
{ 
// Your Java statements here
    // prompting user for a game of RPS
    String answer;
    while(true)
    {
        answer = JOptionPane.showInputDialog("Would you like to play Rock, Paper, Scissors best 2/3? Yes or No?");
        if(answer.equals("Yes") || answer.equals("yes")) //starts game
        {
            play(); // calling the play() method
            answer = JOptionPane.showInputDialog("Would you like to play again?");  //prompting if user wants to play again
            for(int i = 0; i < 10; i++)
            {
                if(answer.equals("Yes") || answer.equals("yes"))
                {
                    play();// calling play() method for replay
                    break;
                }
                if(answer.equals("No") || answer.equals("no")) //allows user to leave
                {
                    break;
                }
            }    
        }
        if(answer.equals("No") || answer.equals("no")) //allows user to leave
        {
            break;
        }
        if(answer != "no" || answer != "No" || answer != "Yes" || answer != "yes")
        {
            JOptionPane.showMessageDialog(null, "Be sure to enter Yes or No."); //making sure users only type yes or no
        }
    }
    
}/*end main method */ 
public static void play() // the play method
{
    String playerMove;
    int resultPlayer = 0;   //holds round results for player
    int resultComputer = 0; //holds round results for computer
    Status w = Status.WIN;  //enum win
    Status l = Status.LOSE; //enumlose
    Status t = Status.TIE;  //enum tie
    for(int i = 0; i < 3; i++)  //loops rounds of the game
    {
        //generates computer random choice of rps
        String[] rps = {"rock", "paper", "scissors"};
        String computerMove = rps[new Random().nextInt(rps.length)];
        //once either player or computer has won two round the game ends
        if(resultPlayer == 2 || resultComputer == 2)
        {
            break;
        }
        //loops around if player doesn't type either rock, paper, or scissors
        while(true)
        {
            playerMove = JOptionPane.showInputDialog("Please enter rock, paper, or scissors.");
            if(playerMove.equals("rock") || playerMove.equals("paper") || playerMove.equals("scissors"))
            {
             break;
            }
            JOptionPane.showMessageDialog(null, "Be sure to enter rock, paper, or scissors.");
        }
        JOptionPane.showMessageDialog(null, "Computer said: " +computerMove);   //displaying computers choice
        //results of each round depending on who picks what
        if(playerMove.equals(computerMove))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Round "+t);
            i--; // increment -- because if player and computer draw same then the game will redo that round until someone wins or loses
        }
        if(playerMove.equals(r)&computerMove.equals(s))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Player "+w);
            resultPlayer++;
        }
        else if(playerMove.equals(r)&computerMove.equals(p))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Computer Wins, round "+l);
            resultComputer++;
        }
        if(playerMove.equals(p)&computerMove.equals(r))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Player "+w);
            resultPlayer++;
        }
        else if(playerMove.equals(p)&computerMove.equals(s))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Computer Wins, round "+l);
            resultComputer++;
        }
        if(playerMove.equals(s)&computerMove.equals(p))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Player "+w);
            resultPlayer++;
        }
        else if(playerMove.equals(s)&computerMove.equals(r))
        {
            JOptionPane.showMessageDialog(null, "Player move: "+ playerMove+". Computer move: " +computerMove+"."+"\n Computer Wins, round "+l);
            resultComputer++;
        }
        JOptionPane.showMessageDialog(null, "Player won "+ resultPlayer+" rounds."+"\n Computer won "+resultComputer+" rounds.");
    }
    //if player wins 2 rounds or resultPlayer value is 2 then player wins and displays the game results
    if(resultPlayer == 2)
    {
        JOptionPane.showMessageDialog(null, "Player won the game!"+"\n Player won "+resultPlayer+" rounds."+"\n Computer won "+resultComputer+" rounds.");
    }
    //if computer wins 2 rounds or resultComputer value is 2 then computer wins and displays the game results
    if(resultComputer == 2)
    {
        JOptionPane.showMessageDialog(null, "Computer won the game!"+"\n Player won "+resultPlayer+" rounds."+"\n Computer won "+resultComputer+" rounds.");
    }
}
}/*end class Anyname*/
