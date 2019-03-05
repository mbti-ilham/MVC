#coding:-utf8
from modeleAnnuaire import *
import cmdControleurAnnuaire as cmd



from tkinter import *
application = Tk()
application.title("Application")
application.geometry("500x150")

def insert ():
	pass
"""
	if len(entry_nom.get()) == 0 or len(entry_prenom.get()) == 0 or len(entry_ville.get()) == 0 or len(entry_nb_telephone.get()) == 0:
		afficheWarning("Merci de specifier toute les informations.")
	strIn
"""
def reshear ():
	pass
	
"""
	if len(entry_nom) == 0 :
		afficheWarning("donné le nom de la personne rechercher")
	pass # cmd [...] 
"""
	
def show_data ():
	txtnom = entry_nom.get()
	txtprenom = entry_prenom.get()
	txtville = entry_ville.get()
	txtnb_telephone = entry_nb_telephone.get()

	print(txtnom,txtprenom,txtadresse,txtnb_telephone);
	print("nom : {} \nprenom : {} \nville : {} \nn°tel : {} \n" 
	.format(txtnom,txtprenom,txtville,txtnb_telephone));



def create_wid():
# Label

	lab_nom = Label(application,text="Nom")
	lab_prenom = Label(application,text="Prenom")
	lab_ville = Label(application,text="Ville")
	lab_nb_telephone = Label(application,text="numero de telephone")

	lab_nom.grid(row=2,sticky=W)
	lab_prenom.grid(row=3,sticky=W)
	lab_ville.grid(row=4,sticky=W)
	lab_nb_telephone.grid(row=5,sticky=W)

# Entry
	

	application.varNom = StringVar(application)
	
	entry_nom = Entry(application,textvariable=application.varNom)
	entry_prenom = Entry(application,textvariable=application.varNom)
	entry_ville = Entry(application,textvariable=application.varNom)
	entry_nb_telephone = Entry(application,textvariable=application.varNom)

	entry_nom.grid(row=2,column=1)
	entry_prenom.grid(row=3,column=1)
	entry_ville.grid(row=4,column=1)
	entry_nb_telephone.grid(row=5,column=1)
		
	

# Button

	but_insert = Button(application, text=' insert ',command=insert)
	but_del= Button(application, text=' reshear',command=reshear)
	but_quit= Button(application, text=' quit ',command=application.quit)

	but_insert.grid(row=6,column=1,columnspan=2, padx=1, pady=1)
	but_del.grid(row=6,column=2,columnspan=1, padx=1, pady=1)
	but_quit.grid(row=6,column=4,columnspan=2, padx=1, pady=1)

if __name__ == '__main__':
	repertoire = ModeleAnnuaire()
	create_wid()
	insert()
	application.mainloop()
	entry_nom= Entry(application)
	

