# Cake

import java.util.Scanner;

public class P57_Cake {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int width = Integer.parseInt(scanner.nextLine());
        int length = Integer.parseInt(scanner.nextLine());
        int countPieces = 0;

        int numAllPieces = width * length;

        while (countPieces <= numAllPieces) {
            try {
                int takePieces = Integer.parseInt(scanner.nextLine());
                countPieces += takePieces;
            } catch (Exception e) {
                System.out.printf("%d pieces are left.", numAllPieces - countPieces);
                return;
            }
        }
        System.out.printf("No more cake left! You need %d pieces more.", countPieces - numAllPieces);
    }
}
