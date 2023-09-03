import tkinter as tk
import random

# Create a function to generate a random background color
def generate_random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    return f'#{r:02X}{g:02X}{b:02X}'  # Convert RGB values to hexadecimal

# Create a function to update the background color
def update_background():
    color = generate_random_color()
    root.configure(bg=color)

# Create the main application window
root = tk.Tk()
root.title("Random Background Generator")

# Create a button to change the background color
button = tk.Button(root, text="Change Background", command=update_background)
button.pack(pady=20)

# Initialize the background color
update_background()

# Start the main event loop
root.mainloop()

# Background-Generator
