# OIBSIP-task-1
task 1Online reservation system
import java.util.Scanner;

public class LoginSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Predefined user credentials
        String validUsername = "sarthak";
        String validPassword = "password123";

        // Ask user for login credentials
        System.out.println("Enter Username: ");
        String username = scanner.nextLine();
        
        System.out.println("Enter Password: ");
        String password = scanner.nextLine();

        // Check if the credentials are correct
        if (username.equals(validUsername) && password.equals(validPassword)) {
            System.out.println("Login Successful!");
            ReservationSystem(); // Proceed to reservation system
        } else {
            System.out.println("Invalid credentials. Please try again.");
        }
    }

    // Simple Reservation System
    public static void ReservationSystem() {
        Scanner scanner = new Scanner(System.in);

        // Collect reservation details from the user
        System.out.println("\nEnter your name: ");
        String name = scanner.nextLine();
        
        System.out.println("Enter the train number: ");
        String trainNumber = scanner.nextLine();

        System.out.println("Enter the date of journey (DD/MM/YYYY): ");
        String journeyDate = scanner.nextLine();
        
        System.out.println("Enter the departure station: ");
        String departure = scanner.nextLine();
        
        System.out.println("Enter the destination station: ");
        String destination = scanner.nextLine();

        System.out.println("Enter class type (e.g., Sleeper, First Class): ");
        String classType = scanner.nextLine();

        // Display reservation details
        System.out.println("\nReservation Details:");
        System.out.println("Name: " + name);
        System.out.println("Train Number: " + trainNumber);
        System.out.println("Journey Date: " + journeyDate);
        System.out.println("From: " + departure);
        System.out.println("To: " + destination);
        System.out.println("Class Type: " + classType);

        // Simple confirmation
        System.out.println("\nYour reservation has been made successfully!");
        System.out.println("Your PNR number is: 12345\n");
        
        // Call for cancellation after reservation
        CancellationSystem();
    }

    // Cancellation System
    public static void CancellationSystem() {
        Scanner scanner = new Scanner(System.in);

        // Ask for PNR number to cancel the ticket
        System.out.println("Do you want to cancel a ticket? (Yes/No): ");
        String cancelChoice = scanner.nextLine();

        if (cancelChoice.equalsIgnoreCase("Yes")) {
            System.out.println("Enter your PNR number: ");
            String pnr = scanner.nextLine();

            // Assuming PNR is correct (In a real system, it would be checked in a database)
            System.out.println("Cancelling ticket with PNR: " + pnr);
            System.out.println("Your ticket has been cancelled successfully.\n");
        } else {
            System.out.println("No cancellation made.\n");
        }
    }
}
