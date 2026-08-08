import java.util.Scanner;

public class ShoppingCart {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String[] products = {"Laptop Bag", "Headphones", "Mouse", "Keyboard"};
        double[] prices = {800, 1200, 500, 1000};

        System.out.println("===== MINI SHOPPING CART =====");

        for (int i = 0; i < products.length; i++) {
            System.out.println((i + 1) + ". " + products[i] + " - Rs." + prices[i]);
        }

        System.out.print("\nChoose a product: ");
        int choice = sc.nextInt();

        if (choice >= 1 && choice <= 4) {

            System.out.print("Enter quantity: ");
            int quantity = sc.nextInt();

            double total = prices[choice - 1] * quantity;

            System.out.println("\n----- BILL -----");
            System.out.println("Product  : " + products[choice - 1]);
            System.out.println("Price    : Rs." + prices[choice - 1]);
            System.out.println("Quantity : " + quantity);
            System.out.println("Total    : Rs." + total);

            System.out.println("\nThank you for shopping!");

        } else {
            System.out.println("Invalid product choice!");
        }

        sc.close();
    }
}