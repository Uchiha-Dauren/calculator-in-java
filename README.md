import java.util.Scanner;
import java.util.Random;
public class GuessGame{
    public static  void main(String[] args ){
        Scanner reader = new Scanner(System.in);
        Random random = new Random();

        int secretNumber = random.nextInt(100) + 1;
        int guess = 0;
        int attempts = 0;
        System.out.println("1ден  100ге дейіңгі санды тап");
        while(guess != secretNumber){
            System.out.print("сенің нұсқаң:");
            guess = reader.nextInt();
            attempts++;
            if(guess < secretNumber){
                System.out.println("үлкенірек сан жаз");
            }else if(guess > secretNumber){
                System.out.println("кішірек сан жаз");
            }else{
                System.out.println("құттықтаймын! сен\t" + attempts + "\tмүмкіндікте  таптың!");
            }
        }
