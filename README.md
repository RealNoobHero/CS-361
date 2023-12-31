# CS-361

Communication Contract
This contract is not legally binding or enforcable, it is not actually a contract.

To request data from the blood_sample microservice, either use or integrate the included ui. For that simply start the ui.py script
and follow the instructions provided by the CLI. Simply type the collection unit, start, and stop dates in the format indicated by the ui interface.

The ui then writes the information to a text file, date_range.txt, this info is recieved by the blood_sample microservice which then
accesses the database provided as dp_for_partner.py. Using the info from date_range, blood_sample microservice reads the dict in dp_for_partner,
and finds the requested dates for the requested collection unit, pulls the numbers for total blood samples and contaminated samples for each 
  date. Then those numbers are summed to provide a total number of contaminated samples from the date range, and the total number of samples
  collected by the collection unit.

The blood_sample microservice then outputs the total numbers needed, contaminated samples first, to blood_sample.txt. The ui monitors
blood_sample.txt for this information. Then formats it as human readable and prints this information directly into the CLI interface.

![uml diagram](/CS-361/Assignment 9/Screenshot (54).png?raw=true "UML diagram title")
![uml diagram](https://github.com/RealNoobHero/CS-361/blob/main/Assignment%209/Screenshot%20(54).png)
