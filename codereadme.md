# AI_project
just edit the location of the the csv file if the code is not working 
========================================================
code in txt format
===========================================================
from tkinter import*
from tkinter import messagebox
import csv
root = Tk()
root["padx"] = 40
root["pady"] = 40
label = Label(root, text="Choose any catagory : ")
label.pack()
########################################phones#####################################
def phoneram(frame):
	label = Label(frame, text="Enter a size of RAM : ")
	label.pack()
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text="Look up", command=lambda:search_ram(phone.get(),frame))
	b.pack()
def phonerom(frame):
	label = Label(frame, text="Enter a size of ROM : ")
	label.pack()
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text=  "Look up", command=lambda:search_rom(phone.get(),frame))
	b.pack()
def phonecamera(frame):
	label = Label(frame, text="Enter camera size : type 'mp' after size like 16mp ")
	label.pack()
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text=  "Look up", command=lambda:search_camera(phone.get(),frame))
	b.pack()
def search_camera(ram,lop):
    csv_file=csv.reader(open('D:/mycsv.csv','r'))
    Label(lop, text="[ PhoneName ] [RAM] [ROM] [CAMERA] ").pack()
    for row in csv_file:
        if ram==row[4]:#row[1] means row of my ram in excel row 0 is fro name of phones
            Label(lop, text=row).pack() 

def search_ram(ram,lop):
    csv_file=csv.reader(open('D:/mycsv.csv','r'))
    Label(lop, text="[ PhoneName ] [RAM] [ROM] [CAMERA] ").pack()
    for row in csv_file:
        if ram==row[1]:#row[1] means row of my ram in excel row 0 is fro name of phones
            Label(lop, text=row).pack()
def search_rom(rom,lop):
    csv_file=csv.reader(open('D:/mycsv.csv','r'))
    Label(lop, text="[ PhoneName ] [RAM] [ROM] [CAMERA] ").pack()
    for row in csv_file:
        if rom==row[2]:
            Label(lop, text=row).pack()
def es():
    lop=Tk()
    lop["padx"] = 40
    lop["pady"] = 40
    btn_eas = Button(lop, text=" SORT by RAM ",width=15,bg="#6B69D6",fg="#FFFFFF", command =lambda: phoneram(lop))
    btn_reload = Button(lop, text=" SORT BY ROM  ",width=15,bg="#6B69D6",fg="#FFFFFF", command =lambda: phonerom(lop))
    btn_rela = Button(lop, text=" SORT BY Camera  ",width=15,bg="#6B69D6",fg="#FFFFFF", command =lambda: phonecamera(lop))
    btn_rela.pack(side =BOTTOM)
    btn_reload.pack(side =BOTTOM)
    btn_eas.pack(side = BOTTOM)
btn_submit = Button(root, text=" Phones ",width=15,bg="#6B69D6",fg="#FFFFFF", command = es)
btn_submit.pack(side =RIGHT)
#########################phone###############################################################
#===========================================================================================
#==========================================================================================
###########################TV###############################################################
def tvinches(frame):
	label = Label(frame, text="Inches : ")
	label.pack()
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text="Look up", command=lambda:search_inches(phone.get(),frame))
	b.pack()
def tvquality(frame):
	label = Label(frame, text="4k|8k|hd : ")
	label.pack() 
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text="Look up", command=lambda:search_quality(phone.get(),frame))
	b.pack()
def tvcolour(frame):
	label = Label(frame, text="red|black|white|yellow |blue| ")
	label.pack() 
	phone = Entry(frame)
	phone.pack()
	b = Button(frame, text="Look up", command=lambda:search_colour(phone.get(),frame))
	b.pack()
def search_colour(col,win):
    csv_file=csv.reader(open('D:/tvcsv.csv','r'))
    Label(win, text="[ TVname ] [Inches] [Quality] [Colour] ").pack()
    for row in csv_file:
        if col==row[3]:
            Label(win, text=row).pack()

def search_inches(inc,win):
    csv_file=csv.reader(open('D:/tvcsv.csv','r'))
    Label(win, text="[ TVname ] [Inches] [Quality] [Colour] ").pack()
    for row in csv_file:
        if inc==row[1]:
            Label(win, text=row).pack()
def search_quality(qua,win):
    csv_file=csv.reader(open('D:/tvcsv.csv','r'))
    Label(win, text="[ TVname ] [Inches] [Quality] [Colour] ").pack()
    for row in csv_file:
        if qua==row[2]:
            Label(win, text=row).pack()
def ess():
    win=Tk()
    win["padx"] = 40
    win["pady"] = 40
    btn_eas = Button(win, text=" TV  SIZE ",width=15,bg="#D20000",fg="#FFFFFF",command =lambda: tvinches(win))
    btn_reload = Button(win, text="SCREEN Quality  ",width=15,bg="#D20000",fg="#FFFFFF", command =lambda: tvquality(win))
    btn_re = Button(win, text="COLOUR  ",width=15,bg="#D20000",fg="#FFFFFF", command =lambda: tvcolour(win))
    btn_re.pack(side = TOP)
    btn_reload.pack(side = TOP)
    btn_eas.pack(side =TOP)
    
btn_submit = Button(root, text="TV",width=15,bg="#D20000",fg="#FFFFFF",command = ess)
btn_submit.pack(side=LEFT)
###########################TV###############################################################

############################################################################################
root.mainloop()
===========================================
