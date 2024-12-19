# Hotel-Billing-Code
package CHITTOOR;

import java.util.Scanner;
 class HotelManagementSystem {
    float balance = 0.0f;
    char ch;

    public static void main(String[] args) {
        HotelManagementSystem hotel = new HotelManagementSystem();
        hotel.run();
    }

    public void run() {
        System.out.println("-------Welcome to Chittoor Spicy hotel--------");
        do {
            System.out.println(" Menu \n 1.idli -10 rs \n 2.poori - 15 rs \n 3.vada - 8 rs \n 4. lemonrice - 50 rs");
            System.out.println(" select order");
            Scanner sc = new Scanner(System.in);
            int order = sc.nextInt();
            switch (order) {
                case 1:
                    idli();
                    break;
                case 2:
                    poori();
                    break;
                case 3:
                    vada();
                    break;
                case 4:
                    lemonrice();
                    break;
            }
            System.out.print("Do you want to continue ordering? (y/n): ");
            ch = sc.next().charAt(0);
        } while (ch == 'y' || ch == 'Y');
        bill();
    }

    public void idli() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of plates of Idli: ");
        int quantity = sc.nextInt();
        balance += quantity * 10; // Each Idli plate costs 10 Rs
        System.out.println(quantity + " plate(s) of Idli added to your bill.");
    }

    public void poori() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of plates of Poori: ");
        int quantity = sc.nextInt();
        balance += quantity * 15; // Each Poori plate costs 15 Rs
        System.out.println(quantity + " plate(s) of Poori added to your bill.");
    }

    public void vada() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of plates of Vada: ");
        int quantity = sc.nextInt();
        balance += quantity * 8; // Each Vada plate costs 8 Rs
        System.out.println(quantity + " plate(s) of Vada added to your bill.");
    }

    public void lemonrice() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of plates of lemonrice: ");
        int quantity = sc.nextInt();
        balance += quantity * 50; // Each lemonrice plate costs 50 Rs
        System.out.println(quantity + " plate(s) of lemonrice added to your bill.");
    }

    public void bill() {
        System.out.println("Your total bill is: Rs " + balance);
        System.out.println("Thank you for visiting Chittoor Spicy Hotel!");
    }
}


