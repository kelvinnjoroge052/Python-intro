 Python-intro
Python projects
Here's the Python code that performs all the steps you described:

# Create an empty list
my_list = []

# Append elements to the list
my_list.append(10)
my_list.append(20)
my_list.append(30)
my_list.append(40)

# Insert 15 at the second position (index 1)
my_list.insert(1, 15)

# Extend the list with another list
my_list.extend([50, 60, 70])

# Remove the last element
my_list.pop()

# Sort the list in ascending order
my_list.sort()

# Find and print the index of the value 30
index_of_30 = my_list.index(30)
print("Index of 30:", index_of_30)

WEEK 3 Assignment 
Here's a Python program that combines both the Read & Write Challenge and the Error Handling Lab into one neat solution. It asks the user for a filename, handles errors gracefully, and writes a modified version of the content into a new file.

def read_and_modify_file():
    try:
        filename = input("Enter the filename to read: ")
        with open(filename, 'r') as infile:
            content = infile.readlines()

        # Modify content: for example, convert to uppercase
        modified_content = [line.upper() for line in content]

        # Write to a new file
        new_filename = "modified_" + filename
        with open(new_filename, 'w') as outfile:
            outfile.writelines(modified_content)

        print(f"Modified file has been saved as '{new_filename}'.")

    except FileNotFoundError:
        print("Error: The file you entered does not exist.")
    except IOError:
        print("Error: The file could not be read or written.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

read_and_modify_file()

What This Program Does:

Prompts the user for a filename.

Tries to open and read it, handling if it doesn't exist.

Converts each line to uppercase as a simple "modification."

Writes the modified content to a new file.

Handles errors with clear messages.





