# **2025-OBJPROG-LAB008**
Week 03-04 - Conditional and Looping Statements

Laboratory # 08 - Guided Coding Exercise 2: Selection Statements

## **Instructions**

### **Step 1.1: Accept the Assignment**

   1. Click on the assignment link provided by your instructor.
   2. GitHub Classroom will create a **private repository** under your GitHub account.
   3. After the repository is created, click **"Go to Repository"** to view your assignment.

---

### **Step 1.2: Setup your Git Environment**
Only perform this if this is the first time you will setup your Git Environment

   1. Create a GitHub Account:
   ```bash
   https://github.com/signup?source=login
   ```
      
   2. Download and Install Git on your Laptop/Desktop:
   ```bash
   https://git-scm.com/downloads
   ```
   
   3. Create a Folder in your Laptop/Desktop
   4. Right-click anywhere in the created folder and select "Open Git Bash Here".
   5. In the Git Bash Terminal, set your git name, perform command:
   ```bash
   git config --global user.name "Your Name"
   ```
   
   6. In the Git Bash Terminal, set your git email, perform command:
   ```bash
   git config --global user.email "your.email@example.com"
   ```
   
   7. Create your SSH Key, just follow the instructions, no need to provide filename and passphrase. In the Git Bash Terminal, perform command:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   
   8. Copy your SSH Keys into clipboard. In the Git Bash Terminal, perform command:
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```
   
   9. Log in to your GitHub account.
   10. In the upper-right corner of GitHub, click your profile picture and select Settings.
   11. In the left sidebar, click on SSH and GPG keys.
   12. Click the New SSH key button.
   13. In the Title field, give the key a recognizable name (e.g., "My Windows Laptop").
   14. In the Key field, CTRL + V or paste the keys copied into your clipboard. Save the key.
   15. Go Back to terminal, use command:
   ```bash
   ssh -T git@github.com
   ```

### **Step 2: Clone the Repository to Your Local Machine**

   1. On your repository page, click the green **"Code"** button.
   2. Copy the repository URL (choose HTTPS for simplicity).
   3. Open your terminal (or Git Bash, Command Prompt, or PowerShell) and run:
   
   ```bash
   git clone <git_repo_url>
   ```
   
   4. Navigate into the cloned folder:
   
   ```bash
   cd <git_cloned_folder>
   ```

### **Step 3: Complete the Assignment**

**Laboratory # 08 - Guided Coding Exercise 2: Selection Statements**

   **Objective:**
   - Implement various forms of selection control.
   - Practice one-way if, two-way if-else, nested if, and multi-way if-else statements.

   **File Naming Convention:**
   - `SelectionStatementsDemo.java`

   **Desired Output (with score = 82):**
   ```txt
   You passed the exam!
   Keep improving!
   Grade: B
   Multi-way Grade: B
   ```

   **Notable Observations (to be discussed after completing the exercise):**
   - Pay attention to the different outputs produced by each type of if statement.
   - Notice how the nested if and the multi-way if-else chain achieve a similar grading result but use different logic structures.

   **Java Programming Best Practices:**
   - Use descriptive variable names.
   - Comment your code to explain the logic of the if statements.
   - Indent your code properly to clearly show the code blocks within the if, else, and nested structures.
      
   **Step-by-Step Instructions:**

   1. Setup Class and Main Method
      - Create a file named `SelectionStatementsDemo.java`.
      - Define the class `SelectionStatementsDemo` and its `main` method.
      ```Java
      public class SelectionStatementsDemo {
          public static void main(String[] args) {
      
          }
      }
      ```
            
   2. Declare Boolean Variables
      - Inside the main method, declare an integer variable named studentScore and initialize it to 82.
      ```Java
      int studentScore = 82;
      ```

   3. One-Way if Statement (Passing)
      - Write a one-way if statement. The condition should check if studentScore is greater than or equal to 60.
      - Inside the if block, print "You passed the exam!".
      ```Java
      if (studentScore >= 60) {
         System.out.println("You passed the exam!");
      }
      ```

   4. Two-Way if-else Statement (Basic Feedback)
      - Write a two-way if-else statement. The condition should check if studentScore is greater than or equal to 90.
      - Inside the if block, print "Excellent performance!".
      - Inside the else block, print "Keep improving!".
      ```Java
      if (studentScore >= 90) {
         System.out.println("Excellent performance!");
      } else {
         System.out.println("Keep improving!");
      }
      ```

   5. Nested if Statements (Detailed Grading)
      - Write a nested if structure. The outer if should check if studentScore is greater than or equal to 60.
      - Inside the outer if block:
         - Write another if to check if studentScore is greater than or equal to 90. If so, print "Grade: A".
         - Write an else block (still inside the outer if). Inside this else:
            - Write another if to check if studentScore is greater than or equal to 75. If so, print "Grade: B".
            - Write another else block (inside the previous else). Inside this one:
               - Print "Grade: C".
      - Write an else block for the very first (outer) if. Inside this else, - print "Grade: F".
      ```Java
      if (studentScore >= 60) {
         if (studentScore >= 90) {
            System.out.println("Grade: A");
         } else {
            if (studentScore >= 75) {
                  System.out.println("Grade: B");
            } else {
                  System.out.println("Grade: C");
            }
         }
      } else {
         System.out.println("Grade: F");
      }
      ```

   6. Multi-way if-else Chain (Alternative Grading)
      - Write a multi-way if-else chain.
      - The first if should check if studentScore is greater than or equal to 90. If so, print "Multi-way Grade: A".
      - The next else if should check if studentScore is greater than or equal to 80. If so, print "Multi-way Grade: B".
      - The next else if should check if studentScore is greater than or equal to 70. If so, print "Multi-way Grade: C".
      - The next else if should check if studentScore is greater than or equal to 60. If so, print "Multi-way Grade: D".
      - The final else block should print "Multi-way Grade: F".
      ```Java
      if (studentScore >= 90) {
         System.out.println("Multi-way Grade: A");
      } else if (studentScore >= 80) {
         System.out.println("Multi-way Grade: B");
      } else if (studentScore >= 70) {
         System.out.println("Multi-way Grade: C");
      } else if (studentScore >= 60) {
         System.out.println("Multi-way Grade: D");
      } else {
         System.out.println("Multi-way Grade: F");
      }
      ```

   7. Compile and Run
       - Save the file as `SelectionStatementsDemo.java`.
       - Compile the code using `javac SelectionStatementsDemo.java` in your terminal or command prompt.
       - Run the compiled code using `java SelectionStatementsDemo`.

   **Conclusion**
   This exercise demonstrates the different forms of selection control flow in Java: one-way if, two-way if-else, nested if, and multi-way if-else.  These structures are essential for creating programs that make decisions based on different conditions.  Understanding when to use each type of if statement allows you to write more efficient and readable code.  Always prioritize code clarity through proper indentation and comments.

### **Step 4: Push Changes to GitHub**
Once you've completed your changes, follow these steps to upload your work to your GitHub repository.

1. Check the status of your changes:
   Open the terminal and run:
   
   ```bash
   git status
   ```
   This command shows any modified or new files.
   
2. Stage the changes:
   Add all modified files to staging:
   
   ```bash
   git add .
   ```
   
3. Commit your changes:
   Write a meaningful commit message:
   
   ```bash
   git commit -m "Submitting OBJPROG Week 04 - Session 01 - Exercise 02"
   ```
   
4. Push your changes to GitHub:
   Upload your changes to your remote repository:
   
   ```bash
   git push origin main
   ```
