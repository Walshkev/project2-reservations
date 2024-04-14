# reservations

is a file that can reserve a seat free a seat and count taken seats with multiple threads at the same time.

## building

Type make into the command line while you are in the same directory that the file is in and the make file will be created with the same name as the c file.

## files

reservations.c

## data

an array that hold n amount of seats
an intager that hold the amount of used seats
a temparay count that is used to see if the taken seats is acuurate.

## functions

int verify_seat_count(void)
checks to see if a specific seat is taken.

int is_free(int n)

    checks to see if the current count of taken seats is accurate.

int free_seat(int n)

    changes a specific seat form taken(1) to free(0)\
    or raises a error (returns -1 ) if already free (0)

int reserve_seat(int n)
changes a specific seat from free(0) to taken (1) or
raises an error ( returns -1 ) if that seat is already taken.

## notes

the only part that was complicated is to make sure that the bool return form the verify_seat_count was inside of the lock so that the other treads changing the available count would not mess up this function.
# project2-reservations
#   p r o j e c t 2 - r e s e r v a t i o n s  
 