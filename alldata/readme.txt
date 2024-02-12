
ReadMe file for USN Research Data Archive
ReadMe file generated on 2023-09-08 by Halvor Nybø Risto 


-------------------
GENERAL INFORMATION
------------------- 
Title of Dataset: Fixed-text keystroke dynamics authentication data set
Contact Information
  - Name: Halvor Nybø Risto
  - Institution: USN / Indra Navia
  - Email: halvor.n.risto@usn.no / halvor.risto@indra.no

H. N. Risto and O. H. Graven, “Collection and statistical analysis of a fixed-text keystroke dynamics authentication data set”, CSNET 2023

DATE(S) OF DATA COLLECTION AND/OR TIME PERIOD COVERED
[YYYYMMDD]
2023/02/01 - 2023/04/01

GEOGRAPHIC LOCATION(S) OF DATA COLLECTION
USN - Hasbergsvei 36, Krona, Hasbergs vei 36, 3616


TYPE OF DATA:
Keystroke timing logs, comma-separated values

LANGUAGE
English

------------
METHODOLOGY
------------

A C++ keylogger with a console application input window was developed to record keystroke with millisecond resolution, using a desktop computer with a PS/2 keyboard. The choice to not use a typical USB keyboard was due to the polling frequency limiting timing resolution, while PS/2 keyboards issues interrupts rather than polling.
The data set can be divided into two parts; 5 selected individuals typing each of the 6 password 200 times (referred to as the defence set), and approximately 100 passerby individuals typing 2 of the passwords on a cycle 10 times for each password (referred to as the attack set).
The defence set was collected in one session for each password, and typically two sessions for all passwords per individual.
The attack set was collected next to the staffed "servicetorget" at USN in Kongsberg. Each completion of 20 password typings was rewarded with a unique code which could be exchanged for a small chocolate at servicetorget. The staff was instructed to cross out each code as they were exchanged, and that each participant could only participate once. The collection was done on an unattended semi-supervised computer with efforts taken to prohibit interference by participants by disabling specific keyboard keys and ensuring that fullscreen could not be exited without an abort code.

The raw data was first collected as a sequence of key presses and releases, then processed to list the times between key presses and releases (hold times, times between subsequent key presses, and times between key release and key press of subsequent keys) using another C++ program.

----------------
FILE INFORMATION
----------------


The data sets consist of 6 passwords: flying automatic monster, Gigab!t R3ceiver, gigabit receiver, Ob$erv3r, observer, repetition learn machine thinker
There is one file for each 5 of the defence set participant and per password, and one file per password for the attack set, giving a total of 6x6 = 36 files.

The first row of each file defines the columns as three types of time measurements for the keys; the hold time of the given key (defined as the time between key press and release of the same key), down to down time (defined as the time between a key press and the key press of the subsequent key), and up to down time (defined as the time between a key release and the key press of the subsequent key, this value may be negative). Each file lists these measurements for each subsequent keyboard key used to type the password.

Time is listed in seconds with 3 decimal points. The values are separated by commas, and a period is used for decimal points.

For the sake of avoiding special characters in the filenames, ! and $ are replaced with "-dollar-" and "-exclm-".
List of files:
"attack - flying automatic monster.csv"
"attack - Gigab-exclm-t R3ceiver.csv"
"attack - gigabit receiver.csv"
"attack - Ob-dollar-erv3r.csv"
"attack - observer.csv"
"attack - repetition learn machine thinker.csv"
"participant1 - flying automatic monster.csv"
"participant1 - Gigab-exclm-t R3ceiver.csv"
"participant1 - gigabit receiver.csv"
"participant1 - Ob-dollar-erv3r.csv"
"participant1 - observer.csv"
"participant1 - repetition learn machine thinker.csv"
"participant2 - flying automatic monster.csv"
"participant2 - Gigab-exclm-t R3ceiver.csv"
"participant2 - gigabit receiver.csv"
"participant2 - Ob-dollar-erv3r.csv"
"participant2 - observer.csv"
"participant2 - repetition learn machine thinker.csv"
"participant3 - flying automatic monster.csv"
"participant3 - Gigab-exclm-t R3ceiver.csv"
"participant3 - gigabit receiver.csv"
"participant3 - Ob-dollar-erv3r.csv"
"participant3 - observer.csv"
"participant3 - repetition learn machine thinker.csv"
"participant4 - flying automatic monster.csv"
"participant4 - Gigab-exclm-t R3ceiver.csv"
"participant4 - gigabit receiver.csv"
"participant4 - Ob-dollar-erv3r.csv"
"participant4 - observer.csv"
"participant4 - repetition learn machine thinker.csv"
"participant5 - flying automatic monster.csv"
"participant5 - Gigab-exclm-t R3ceiver.csv"
"participant5 - gigabit receiver.csv"
"participant5 - Ob-dollar-erv3r.csv"
"participant5 - observer.csv"
"participant5 - repetition learn machine thinker.csv"


-------
SHARING 
-------

ALL UPLOADED DATASETS HAVE THEIR OWN CITE AND SHARING SECTION IN USN RESEARCH DATA ARCHIVE

Acknowledgements. 
This README file template is adapted from DataverseNO's general README file Template Version: 2.1. Available at: https://drive.google.com/file/d/1RHl-D79tZWC3nJJPrnvcgIQDHgmuH2Mk/view
