# Zoo Database Project
## Zoo Garden
This database represents a management model of a zoo, having a relational structure, based on interconnected tables through primary and foreign keys. Thus, we can store and manage data about: the zoo, employees, animals, species, cages, locations, shows, tickets, connections, visitors, schedule, care.
### ZOO_GARDEN Table:
- stores information about the zoo such as its size and the city it belongs to. It is in a one to many relationship with the EMPLOYEE table, one to many with the ANIMAL table, one to many with the SHOW table, one to one with the SCHEDULE table, and one to many with the VISITOR table.
### EMPLOYEE Table: 
- stores information about employees such as name, first name, age, gender, and salary. It is in a many to one relationship with the ZOO_GARDEN table and many to one with the CARE table.
### ANIMAL Table:
- stores information about the animals in the zoo such as: their category, number, and names. It is in a many to one relationship with the ZOO_GARDEN table, many to one with the CONNECTION table, one to many with the SPECIES table, and many to one with the CARE table.
### TICKET Table:
- stores information about tickets for the zoo's shows such as: the price and category. It is in a many to one relationship with the SHOW table.
### SHOW Table:
- stores information about the shows taking place in the zoo such as: the time and the maximum number of seats. It is in a one to many relationship with the TICKET table, many to one with the CONNECTIONS table, many to one with the ZOO_GARDEN table, and one to one with the TIME table.
### CONNECTION Table:
- links the ANIMAL table and the SHOW table to turn a many to many relationship into two, one being one to many between the CONNECTION table and the ANIMAL table and the other being many to one between the SHOW table and the CONNECTION table.
### SPECIES Table:
- stores information about animal species such as: their breed and the number of families. It is in a one to many relationship with the ANIMAL table.
### CAGE Table:
- stores information about animal cages such as: their material and size. It is in a many to one relationship with the LOCATION table and many to one with the CARE table.
### LOCATION Table:
- stores information about the locations in the zoo where each cage is such as: their positions and distance from the entrance to the zoo. It is in a one to many relationship with the CAGE table.
### VISITOR Table:
- stores information about the zoo's visitors such as: their age category. It is in a many to one relationship with the ZOO_GARDEN table.
### SCHEDULE Table:
- stores information about the zoo's schedule such as: the day of the week, opening hour, and closing hour. It is in a one to one relationship with the ZOO_GARDEN table.
### CARE Table:
- links the ANIMAL table, the EMPLOYEE table, and the CAGE table to turn 3 many to many relationships into 3, one being one to many between the EMPLOYEE table and the CARE table, one to many between the CAGE table and the CARE table, and another one to many between the ANIMAL table and the CARE table.
### TIME Table:
- stores information about the time when the show is scheduled such as: the hour. It is in a one to one relationship with the SHOW table.
