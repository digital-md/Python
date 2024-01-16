<h1>Develop Algorithms for File Updates</h1>

<h2>Description</h2>

As a security professional, I am going to update a file for a healthcare company that identifies employees who can access restricted content. The content of the files is on a file called “allow_list.txt” listing the IP addresses. The employees are either restricted, allowed or removed based on their IP addresses. I will be using Python code to create an algorithm to check to see if any employees are to be removed from the allowed list. The # symbol indicates the comments made that direct the process. 


<b>Open the file that contains the allow list</b>

First, I will open “allow_list.txt” and assign it as a string to the import_file variable.

![image](https://github.com/digital-md/Python/assets/156498985/0d1553a9-2070-4545-85ec-bb4ef0a5e36c)

Second, I used the ‘with’ ‘open’ statements to open the allowed list file to read it and view the IP addresses stored in the file. I used  with open(“import_file”, “r”) as file:  , there are two parameters, one locates the file to import and the other in this case is the “r” which is for me to read the file.  Additionally, as is used to assign a new variable named file. This file will store the output of open() while I work with it.  

![image](https://github.com/digital-md/Python/assets/156498985/30307214-231c-42bf-b6bb-74a1127a7c23)

<b>Read the file contents</b>

![image](https://github.com/digital-md/Python/assets/156498985/7798f33e-d29e-431b-93e7-a5107f34f998)

When I use the open() function that includes “r” for read. The read() method will convert the file IP addresses into a string and allow me to use it. I used read() to the file variable in the with statement then assigned a string output to the IP addresses variable. This code will allow reading of the allowed_list.txt file and allow me to read and extract data later. 

<b>Convert the string into a list</b>

For me to remove the IP addresses from the allowed_list. I needed to parse it by using .split() to convert the string IP addresses into a list.

![image](https://github.com/digital-md/Python/assets/156498985/60815e47-ff0c-4d64-bef2-c30b90f24957)

 When .split() is used it appends and converts the contents of that string to a list. The reason we split IP addresses into this list is because it will make it easier to remove IP addresses in the alllowed_list. The algorithm .split() function will take data stored in IP addresses and convert the string into list of IP addresses. Then I will reassign it back to the variable IP addresses. 

<b>Iterate through the remove list</b>

Iterating through the IP addresses in this algorithm is key to reviewing remove_list. Therefore, I needed to create a for loop

![image](https://github.com/digital-md/Python/assets/156498985/122bd3f6-f39b-499d-a527-100eb16ad8b7)

In for loop it will repeat the code by applying specific statements to all elements in sequence. 
It starts the loop with for and is followed by a loop variable named element. The in keyword directs the iterate through sequences of the IP addresses and assigns a value to the variable element. 

<b>Remove IP addresses that are on the remove list</b>

The algorithm I made requires removing the IP addresses from the allow list, which is also in the remove list. I used this code to achieve this. 

![image](https://github.com/digital-md/Python/assets/156498985/0adf2928-fab6-46df-9d43-92ceed9ef45a)

First in the for loop I needed to create a conditional to evaluate if the loop variable element would be found in the list of IP addresses. I applied .remove() to IP addresses and passed the loop to element as the argument so that the IP addresses in the remove list would be removed from IP addresses. 

<b>Update the file with the revised list of IP addresses </b>

I updated the allow list file with the revised list of IP addresses. First I had to convert the list back into a string. I used .join() for this.

![image](https://github.com/digital-md/Python/assets/156498985/292ab303-841d-43dc-86b5-880ad6088a63)

When using .join() it combines all items in an iterable into a string. When it is applied to a string containing characters it will separate the elements in the iterable once it has joined a string. In the algorithm, I used .join()to create the string from the list in ip_addresses so it passes as an argument to the .write() method when writing to this file "allow_list.txt". I used ("\n") a string to be a separator that instructs the code to place the elements on a new line. Then, I used the with statement and .write()to update the file.

![image](https://github.com/digital-md/Python/assets/156498985/8c5d2dfc-af82-4b3d-8fed-5e02493e66ee)

In this instance, I employed the “w” argument in conjunction with the open() function within my with statement. This argument signifies my intention to overwrite a file’s contents. When the “w” argument is used, the .write() function can be invoked within the with statement’s body. The .write() function overwrites a specified file with string data, replacing any pre-existing content.
In this scenario, my goal was to overwrite the “allow_list.txt” file with the updated allow list in string format. Consequently, any IP addresses removed from the allow list will no longer have access to restricted content. To overwrite the file, I attached the .write() function to the file object, identified as ‘file’ in the with statement. I input the ip_addresses variable as the argument, indicating that the data in this variable should replace the contents of the file specified in the with statement.

<b>Summary</b>

I created an algorithm that eliminates IP addresses listed in a variable named remove_list from the “allow_list.txt” file, which contains approved IP addresses. This process involves opening the file, transforming its content into a string for reading, and then converting this string into a list that is stored in the ip_addresses variable.
Next, I loop through the IP addresses in remove_list. During each iteration, I check if the current IP address exists in the ip_addresses list. If it does, I use the .remove() method to delete it from ip_addresses.
Finally, I use the .join() method to convert ip_addresses back into a string. This allows me to overwrite the “allow_list.txt” file with the updated list of IP addresses.

```
--!>
