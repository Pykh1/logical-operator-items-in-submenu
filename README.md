# logical-operator-items-in-submenu

#Here we create program with logical operator items in submenu[New,open,Save....]

import tkinter as tk
def Menu_New():
    print("here menu new ")

def Menu_open():
    print("here menu open ")
def Menu_save():
    print("here menu save")

def Menu_save_as():
    print("here menu save as  ")

def Menu_Exit():
        print("here menu exit ")

my_window=tk.Tk()
my_menubar=tk.Menu(my_window)
my_dropdown_menu=tk.Menu(my_menubar)
my_dropdown_menu.add_command(label="New",command=Menu_New)
my_dropdown_menu.add_command(label="Open",command=Menu_open)
my_dropdown_menu.add_separator()
my_dropdown_menu.add_command(label="Save",command=Menu_save)
my_dropdown_menu.add_command(label="Save_as",command=Menu_save_as)
my_dropdown_menu.add_separator()
my_dropdown_menu.add_command(label="Exit",command=Menu_Exit)
my_menubar.add_cascade(label="File",menu=my_dropdown_menu)
my_window.config(menu=my_menubar)
my_window.mainloop()
