# ProiectLP2

import random
from tkinter import *

root=Tk()
root.geometry("750x450")
root.title('Roll the Dice')

l1=Label(root,font=("times",150),fg="green")
l2=Label(root,font=("times",150),fg="red")
l3=Label(root,font=("times",150),fg="blue")

def roll1():
    number=['\u2680','\u2681','\u2682','\u2683','\u2684','\u2685']
    l1.config(text=f'{random.choice(number)}')
    l1.pack()

def roll2():
    number=['\u2680','\u2681','\u2682','\u2683','\u2684','\u2685']
    l2.config(text=f'{random.choice(number)}{random.choice(number)}')
    l2.pack()

def roll3():
    number=['\u2680','\u2681','\u2682','\u2683','\u2684','\u2685']
    l3.config(text=f'{random.choice(number)}{random.choice(number)}{random.choice(number)}')
    l3.pack()


b1=Button(root,text="Roll 1 dice",command=roll1)
b1.place(x=150,y=0)

b2=Button(root,text="Roll 2 dices",command=roll2)
b2.place(x=250,y=0)

b3=Button(root,text="Roll 3 dices",command=roll3)
b3.place(x=350,y=0)

root.mainloop()
