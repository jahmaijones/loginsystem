# loginsystem

users = {}
status = " "

def displayMenu():
  status = input("Are you a registered user? y/n Press q to quit")
  if status == "y":
  		olduser=()
  elif status == "n":
  		newUser()


def newUser():
		createLogin = input("Create login name: ")

		if createLogin in users: 
			print ("\nLogin name already exists!\n")
		else:
			createPassw = input("Create a new password: ")	
			users[createLogin] = createPassw
			print("\n User Created\n")

def oldUser():
		login = input("Enter login name: ")
		passw = input("Enter password: ")

		if login in users and users [login] == passw:
			print ("\nLogin Succesful\n")

		else:
			print("\nUser doesn't exist or wrong password\n")

while status != "q":
	displayMenu()

