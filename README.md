# Task-1---Digital-Clock-
import tkinter as tk
import time

def update_time():
    current_time = time.strftime("%H:%M:%S")
    label.config(text=current_time)
    root.after(1000, update_time)  # Update every 1000ms (1 second)

root = tk.Tk()
root.title("Digital Clock")
root.geometry("500x300")

label = tk.Label(root, font=("Helvetica", 40), bg="black", fg="white")
label.pack(expand=True)

update_time()

root.mainloop()
