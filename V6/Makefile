#------------------------------------------------------------------------------
#target: prerequisit
#       recipe
#Makefiles generally follow such a structure
#target: the name of a file generated by a program. Such as 
#       executables or object files.
#prerequisite: file that is used as input to create the target. Often 
#       several files.
#recipe: An action that make command carries out. A recipe can have more than
#       one command. Not all tagets have prereqs.
#rule: explains to the compiler how and when to remake certain files which
#       are targets of particular rule.

#VARIABLES---------------------------------------------------------------------
objects = main.o list.o
oFlags = -o -pthread

#NOTE: MUST ADD STUFF TO BE ABLE TO USE PTHREADS.

#Here the executable file is called talk. talk will depend on a number of
#object files, which will in turn depend on a number of .c files.
#talk: main.o keyboard.o screen.o list.o


#MAKEFILE---------------------------------------------------------------------
sim: $(objects) 
	gcc -o sim $(objects) 

main.o: main.c list.h
	gcc -c main.c

list.o: list.c list.h
	gcc -c list.c

#It is given to us, so...?
clean: 
	rm sim $(objects)
