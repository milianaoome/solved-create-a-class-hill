Download Link: https://assignmentchef.com/product/solved-create-a-class-hill
<br>
You should make a copy of this file in a convenient directory on your M: drive. Then take a look at the file. A part from the initial header row, each row describes a hill in the following format:Number Name County Height (in metres) Latitude Longitude255 Ben Nevis Highland 1344.5 56.796849 -5.003525In each row, the six fields are separated by commas. You can assume that there are no other commas in the CSV file.

<strong>Part A [7%]</strong>

Create a class Hill that represents the data for one hill as in file hills.csv. Each Hill object should have six fields corresponding to the columns in that file:An integer numberA nameA county nameThe height (in metres)The latitudeThe longitudeThe class should also have:

A constructor with six arguments for initialising the six fields.An instance method toString() which returns a string in the same format as the rows in the CSV file:255,Ben Nevis,Highland,1344.5,56.796849,-5.003525Then create a class Exercise5 with the following method:public static void exercise5a() {Hill benNevis = new Hill(255, “Ben Nevis”, “Highland”, 1344.5, 56.796849, -5.003525);System.out.println(benNevis);}Add a main() method to class Exercise5 that invokes exercise5a(). Test your program by running the class.

<strong>Part B [6%]</strong>

In class Hill, write a methodpublic static List readHills() The method should read the hill data from file hills.csv. It should skip the header row. For each row thereafter, it should create a corresponding Hill object. The method should return a list containing these objects in the same order as they are in the file.

In class Exercise5, create a method:public static void exercise5b()This method should invoke readHills() and display the first 20 list elements on the <a href="http://www.justanswer.com/topics-console/">console</a>.Add an invocation of exercise5b() in the main() method and test your program.Hints:See Week 19 lecture notes for sample code for reading data from a CSV file.Remember that classes Double and Integer have methods to parse a number from a string.

<strong>Part C [5%]</strong>

In class Exercise5, write a methodpublic static void exercise5c()The method should read the hill data from file hills.csv into a list using method readHills(). It should then start an interactive loop. In each step of the loop, the program should:Request the user to enter the name of a hill.Respond by printing to the console the details of all matching hills. A hill is said to be matching if its name starts with the string entered by the user. Matching should be case-insensitive.The program should exit if the user enters quit. See a sample interaction below:




Please enter a hill name or quit to exit:Cadair1862,Cadair Berwyn,Powys,832.0,52.8806,-3.3809931863,Cadair Berwyn North Top,Denbighshire,827.0,52.883881,-3.3802351865,Cadair Bronwen,Denbighshire,783.4,52.901461,-3.3728991868,Cadair Bronwen NE Top,Denbighshire,700.0,52.906631,-3.3588021911,Cadair Idris – Penygadair,Gwynedd,893.0,52.699618,-3.9087924587,Cadair Fawr,Rhondda Cynon Taff,485.0,51.800059,-3.48363612140,Cadair Ifan Goch,Conwy,207.0,53.185429,-3.810762Please enter a hill name or quit to exit:sno1742,Snowdon – Yr Wyddfa,Gwynedd,1085.0,53.068496,-4.07623110028,Snougie of Long Hill,Shetland Islands,75.0,60.259782,-1.20855113597,Snokoe Hill,Northumberland,191.0,54.953663,-2.02850913802,Snoddle Hill,Rochdale,277.0,53.66063,-2.073073Please enter a hill name or quit to exit:quitGood-byeAdd an invocation of exercise5c() in the main() method and test your program.Part D [6%]Write a methodpublic static void exercise5d()The method should read the hill data from file hills.csv into a list using method readHills(). It should then:sort the list of hills by name in alphabetical order and print the first 20 elements of the list; and thenperform another sorting of the list of hills but this time by height in descending order (=highest hills first) and then print the first 20 elements of the list.Sorting should be performed by invoking method Collections.sort making use of appropriate implementations of interfaces Comparable and/ or Comparator which you will need to code.Part E [6%]In class Hill, write a methodpublic static Map&gt; hillsByCounty(List hills)Given a list of Hill objects, the method should return a map which associates each county with the set of hills in that county. The map entries should be sorted by county names and each of the sets of hills should be sorted by hill names.Then write a method:public static void exercise5e()The method should read the hill data from file hills.csv into a list using method readHills(). It should invoke method hillsByCounty with that list. This method invocation returns a map. For each of the first three counties in that map, the program should display:The name of the countyThe names and the height of the first three hills associated with the county in the map.