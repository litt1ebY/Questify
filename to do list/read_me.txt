
# Simple To-Do List for Beginners

# Create an empty list to store tasks
tasks = []

print("Welcome to Your To-Do List!")

while True:
    # Show menu
    print("\n--- MENU ---")
    print("1. Add a task")
    print("2. View tasks")
    print("3. Remove a task")
    print("4. Exit")

    # Get user choice
    choice = input("\nWhat would you like to do? (1-4): ")

    # Add a task
    if choice == "1":
        task = input("Enter your task: ")
        tasks.append(task)
        print(f"Added: {task}")

    # View all tasks
    elif choice == "2":
        if len(tasks) == 0:
            print("No tasks yet!")
        else:
            print("\nYour Tasks:")
            for i in range(len(tasks)):
                print(f"{i + 1}. {tasks[i]}")

    # Remove a task
    elif choice == "3":
        if len(tasks) == 0:
            print("No tasks to remove!")
        else:
            print("\nYour Tasks:")
            for i in range(len(tasks)):
                print(f"{i + 1}. {tasks[i]}")

            task_number = int(input("Which task number to remove? "))
            if task_number > 0 and task_number <= len(tasks):
                removed = tasks.pop(task_number - 1)
                print(f"Removed: {removed}")
            else:
                print("Invalid task number!")

    # Exit
    elif choice == "4":
        print("Goodbye!")
        break

    # Invalid choice
    else:
        print("Invalid choice! Please enter 1-4.")