import tkinter as tk
from time import strftime

# Create the main window
root = tk.Tk()
root.title("Digital Clock")

# Function to update the time
def update_time():
    current_time = strftime('%H:%M:%S %p')  # Time format: Hour:Minute:Second AM/PM
    time_label.config(text=current_time)
    time_label.after(1000, update_time)  # Update the time every 1000 milliseconds (1 second)

# Create a label for displaying the time
time_label = tk.Label(root, font=('calibri', 40, 'bold'), background='black', foreground='cyan')
time_label.pack(anchor='center')

# Call the function to update the time
update_time()

# Run the application
root.mainloop()
