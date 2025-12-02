"""GOALPARA COLLAGE"""
students = {}  

while True:
    print("\n===== Student Management System =====")
    print("1. Add Student")
    print("2. Update Student")
    print("3. Delete Student")
    print("4. View Students")
    print("5. Exit")

    choice = input("Enter your choice : ")

    if choice == '1':
        name = input("Enter student name: ")
        role = input("Enter student mark: ")
        students[name] = role
        print(f"✅ {name} added successfully with role: {role}")

    elif choice == '2':
        name = input("Enter student name to update: ")
        if name in students:
            new_role = input("Enter new role: ")
            students[name] = new_role
            print(f"🔄 {name}'s role updated to: {new_role}")
        else:
            print("⚠ Student not found!")

    elif choice == '3':
        name = input("Enter student name to delete: ")
        if name in students:
            del students[name]
            print(f"🗑 {name} deleted successfully.")
        else:
            print("⚠ Student not found!")

    elif choice == '4':
        if students:
            print("\n📋 Student List:")
            for name, role in students.items():
                print(f"→ Name: {name}, Role: {role}")
        else:
            print("📭 No students found.")

    elif choice == '5':
        print("👋 Exiting program. Goodbye!")
        break
   

    else:
        print("❌ Invalid choice! Please select between 1-5.")

 print("Goodbye")
