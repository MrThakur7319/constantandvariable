# constantandvariable
/**
 * Demonstration of different types of variables in Java
 * Shows instance variables, static variables, constants, and local variables
 */
public class Main {
    // Instance variable - belongs to each object instance
    // Each object of Main class will have its own copy of this variable
    int instanceVariable = 10;
    
    // Static variable - belongs to the class, shared among all instances
    // Only one copy exists regardless of how many objects are created
    static int staticVar = 50;
    
    // Final variable - constant that cannot be changed after initialization
    // Must be initialized when declared or in constructor
    final int CONSTANT_VAR = 100;
    
    /**
     * Method to demonstrate variable access and modification
     */
    public void show() {
        // Local variable - exists only within this method scope
        // Created when method is called, destroyed when method ends
        int localVar = 10;
        
        // Print initial values of all variable types
        System.out.println("local variable: " + localVar);
        System.out.println("instance variable: " + instanceVariable);
        System.out.println("static variable: " + staticVar);
        System.out.println("constant variable: " + CONSTANT_VAR);
        
        // Modify local variable - only affects this method's execution
        localVar = 20;
        System.out.println("updated local variable: " + localVar);
        
        // Modify instance variable - affects this specific object instance
        instanceVariable = 30;
        System.out.println("updated instance variable: " + instanceVariable);
        
        // Modify static variable - affects the class variable shared by all instances
        staticVar = 60;
        System.out.println("updated static variable: " + staticVar);
        
        // Note: CONSTANT_VAR cannot be modified as it's declared as final
        // Attempting to do: CONSTANT_VAR = 200; would cause a compilation error
    }
    
    /**
     * Main method - entry point of the program
     * @param args command line arguments
     */
    public static void main(String[] args) {
        // Create an instance of Main class to access instance variables and methods
        Main obj = new Main();
        
        // Call the show method to demonstrate variable behavior
        obj.show();
    }
}
