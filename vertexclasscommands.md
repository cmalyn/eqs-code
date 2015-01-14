# eqs-code

#class Vertex
	#function for external vertices conversion to list
def find_external(tree):
	externaltaxa=tree.replace('(','').replace(')','').replace(';','').split(',')
	return externaltaxa
		
#function for reading in a file and converting to a string
def open_file(string):
	with open (string,"r") as filename:
		newstring=filename.read().replace('\n','')
		return newstring

#function that does both

def file_to_taxa(string):
	with open (string, "r") as filename:
		newstring=filename.read().replace('\n','')
	externaltaxa=newstring.replace('(','').replace(')','').replace(';','').split(',')
	return externaltaxa
	print externaltaxa
	
#function to count beginning parentheses
def pcount(string):
	number1=string.count('(')
	number2=string.count(')')
	print number1
	print number2 

#function to count number of internal vertices *note not list
def icount(string):
	number1=string.count('(')
	number2=string.count(')')
	number3=(number1+number2)/2
	number4=number3-1
	print number4
	
#function that will do everything mentioned so far
def file_sac(string):
	with open (string, "r") as filename:
		newstring=filename.read().replace('\n','')
	externaltaxa=newstring.replace('(','').replace(')','').replace(';','').split(',')
	print "These are the taxa:"
	for i in externaltaxa:
		print i 
	
	number1=newstring.count('(')
	number2=newstring.count(')')
	number3=(number1+number2)/2
	number4=number3-1
	print "The total number of taxa is {}".format(number4)
	
	for i in externaltaxa:
		print "The character value for {} is {}.".format(i,newstring.find(i))



#just playing around, the %s means it applies to strings, %d means it applies to numbers

def trytaxa(listname):
	for i in listname:
		print "This is taxa %s" % i 
