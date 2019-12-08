# project-calculator-tkinter

from tkinter import*

root = Tk()

root.title("Simple Calculator")

e= Entry(root,width=40)
e.grid(row=0,column=0,columnspan=3,padx=10,pady=10)

def buttonClick(number):
	e.delete(0,END)
	e.insert(0,str(e.get())+str(number))

def add():
	f_number = e.get()
	global f_num
	global math
	math="addition"
	f_num = int(f_number)
	e.delete(0,END)

def mult():
	f_number = e.get()
	global f_num
	global math
	math="multiplication"
	f_num = int(f_number)
	e.delete(0,END)

def sub():
	f_number = e.get()
	global f_num
	global math
	math="subtraction"
	f_num = int(f_number)
	e.delete(0,END)

def div():
	f_number = e.get()
	global f_num
	global math
	math="division"
	f_num = int(f_number)
	e.delete(0,END)

def clear():
	e.delete(0,END)

def equal():
	s_number = e.get()
	e.delete(0,END)
	if(math == "addition"):
		e.insert(0,f_num + int(s_number))
	if(math == "subtraction"):
		e.insert(0,f_num - int(s_number))
	if(math == "multiplication"):
		e.insert(0,f_num * int(s_number))
	if(math == "division"):
		e.insert(0,f_num /int(s_number))

myButton0 = Button(root, text="0",padx=50,pady=20,command=lambda:buttonClick(0))
myButton1 = Button(root, text="1",padx=50,pady=20,command=lambda:buttonClick(1))
myButton2 = Button(root, text="2",padx=50,pady=20,command=lambda:buttonClick(2))
myButton3 = Button(root, text="3",padx=50,pady=20,command=lambda:buttonClick(3))
myButton4 = Button(root, text="4",padx=50,pady=20,command=lambda:buttonClick(4))
myButton5 = Button(root, text="5",padx=50,pady=20,command=lambda:buttonClick(5))
myButton6 = Button(root, text="6",padx=50,pady=20,command=lambda:buttonClick(6))
myButton7 = Button(root, text="7",padx=50,pady=20,command=lambda:buttonClick(7))
myButton8 = Button(root, text="8",padx=50,pady=20,command=lambda:buttonClick(8))
myButton9 = Button(root, text="9",padx=50,pady=20,command=lambda:buttonClick(9))
ButtonClear= Button(root,text="Clear",padx=100,pady=20,command=clear)
ButtonEqual= Button(root,text="=",padx=110,pady=20,command=equal)
ButtonAdd = Button(root,text="+",padx=50,pady=20,command=add)
ButtonMult = Button(root,text="*",padx=50,pady=20,command=mult)
ButtonSub = Button(root,text="-",padx=50,pady=20,command=sub)
ButtonDiv = Button(root,text="/",padx=50,pady=20,command=div)

myButton0.grid(row=4,column=0)
myButton1.grid(row=3,column=0)
myButton2.grid(row=3,column=1)
myButton3.grid(row=3,column=2)
myButton4.grid(row=2,column=0)
myButton5.grid(row=2,column=1)
myButton6.grid(row=2,column=2)
myButton7.grid(row=1,column=0)
myButton8.grid(row=1,column=1)
myButton9.grid(row=1,column=2)
ButtonClear.grid(row=4,column=1,columnspan=2)
ButtonAdd.grid(row=5,column=0)
ButtonSub.grid(row=6,column=0)
ButtonMult.grid(row=6,column=1)
ButtonDiv.grid(row=6 ,column=2)
ButtonEqual.grid(row=5,column=1,columnspan=2)

root.mainloop()
