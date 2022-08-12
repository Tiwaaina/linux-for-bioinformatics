# linux-for-bioinformatics
Bioinformatics for Biologists - An introduction to Linux, command line, and Bash

Conditional Expressions - Performing multiple comparisons

Using Bash syntax, comparisons can be combined using the '&&' and the '||' operators which represent AND and OR respectively.

Task 1:
Write a Bash script called temperature.sh that:

- reads in a command line argument into a variable called temperature

- has a variable called min_temperature and give it a variable of 10

- has a variable called max_temperature and give it a variable of 30

- returns “Too hot!” if temperature is greater than max_temperature

- returns “Too cold!” if temperature is less than min_temperature

- returns “Just right!” if temperature is greater than the min_temperature and less than max_temperature

Terminal:

nano temperature.sh

Script:

#!/usr/bin/env bash

echo "Please enter your temperature!"

read temperature

min_tem=10

max_tem=30

if [[ ${temperature} -gt ${max_tem} ]]

then

echo "Too hot!"

elif [[ ${temperature} -lt ${min_tem} ]]

then

echo "Too cold!"

elif [[ ${temperature} -ge ${min_tem} ]] && [[ ${temperature} -le ${max_tem} ]]

then

echo "Just right!"

fi

#save script (CTRL + O), click ENTER and exit script (CTRL + X)

#Now test Bash script on the terminal with the command:

./temperature.sh
