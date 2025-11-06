# ANNIVERSARY v1.2
                           
## INSTRUCTIONS

ANN provides a way of maintaining a list of annual appointments and
anniversaries, with tracking of a person's age.

Run ANN to start it up.

The software is fairly self explanatory - it follows the standard PSION
interface fairly closely. When you enter it, it creates a file ANNAPP on A. If
you enter it with some anniversaries in the file it will display the next one to
occur after the current system time.  It gives an indication of how far away the
appointment is (In days if it is under 2 weeks).  Use MODE to access the menu

`Find, Goto, Soonest, Add, Delete, Export`

Here are some notes on each option:

Find
: Will only find the first occurrence of the search string.

Goto
: Sets the date the program scans from for the next appointment

Soonest
: Resets the scan date to the system date.

Add
: Add an anniversary - use a standard date selector (Courtesy of David C. Jones)
  routine to select the day and month of the anniversary.  If you set the year 
  to the persons year of birth and answer Y to the following question the prog 
  will keep track of their age for you. Answer N for things like new years day!

Delete
: Gives you the option of deleting the current entry.

Export
: Creates a file on A which is in diary format and can be merged into your 
  diary.  The appointment is set with no alarm at midnight on the day of the 
  anniversary. It's duration is 15 mins.

## FILES

Files created:

  `A:ANNAPP`	The annual appointments file (Anniversary)
  
  This file is maintained in sorted order by the program so A: is the only 
  practical drive for it.
  
Procedure Filenames:
```
ANN		Anniversary
ANEXPORT
ANSELECT
ANADDIT
ANADD
ANDISP%

DATEIN		David's DATIN$ modified to return the no of days since 1/1/1900 
		and to allow the user to escape (returns -1)
MONTH%		Find the month from a no of days from 1/1/1900
DAY%		Find the day from a no of days from 1/1/1900
YEAR%		Find the year from a no of days from 1/1/1900
		The above three are from Collected algorithms from CACM no 199.

TOPLINE		This puts a clock+icon on the top line of the display
PRINTC		Print a string in the centre of the screen
BATT		Check for battery low error
ZERPREF$	Preface a number with zeros - ie ZERPREF$(9,2)="09"
```