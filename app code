
import tkinter as tk


# Function to evaluate mathematical expressions
def evaluate_expression():
    try:
        expression = entry.get()
        result = str(eval(expression))
        entry.delete(0, tk.END)
        entry.insert(tk.END, result)
    except Exception as e:
        entry.delete(0, tk.END)
        entry.insert(tk.END, "Error")

# Function to update the entry widget with button clicks
def button_click(value):
    current_text = entry.get()
    entry.delete(0, tk.END)
    entry.insert(tk.END, current_text + str(value))

# Function to clear the entry widget
def clear_entry():
    entry.delete(0, tk.END)

# Create the main Tkinter window
window = tk.Tk()
window.title("Simple Calculator")

# Entry widget to display the current expression
entry = tk.Entry(window, width=20, font=('Arial', 16), bd=5, insertwidth=4, justify='right')
entry.grid(row=0, column=0, columnspan=4)

# Buttons for digits and operations
buttons = [
    ('7', 1, 0), ('8', 1, 1), ('9', 1, 2), ('/', 1, 3),
    ('4', 2, 0), ('5', 2, 1), ('6', 2, 2), ('*', 2, 3),
    ('1', 3, 0), ('2', 3, 1), ('3', 3, 2), ('-', 3, 3),
    ('0', 4, 0), ('.', 4, 1), ('=', 4, 2), ('+', 4, 3),
]

# Create buttons dynamically
for (text, row, col) in buttons:
    button = tk.Button(window, text=text, width=5, height=2, command=lambda value=text: button_click(value))
    button.grid(row=row, column=col, padx=5, pady=5)

# Clear button
clear_button = tk.Button(window, text='C', width=5, height=2, command=clear_entry)
clear_button.grid(row=5, column=0, padx=5, pady=5, columnspan=3)

# Equal button
equal_button = tk.Button(window, text='=', width=5, height=2, command=evaluate_expression)
equal_button.grid(row=5, column=3, padx=5, pady=5)

# Run the Tkinter event loop
window.mainloop()
