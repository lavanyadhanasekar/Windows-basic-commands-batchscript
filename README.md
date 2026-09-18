# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
```
 mkdir my-folder
```

Remove the directory "my-folder"
<img width="775" height="245" alt="image" src="https://github.com/user-attachments/assets/fe54dac9-0237-4955-931c-a32ec4faeec3" />


## COMMAND AND OUTPUT
```
type nul > Rose.txt

```
<img width="555" height="112" alt="image" src="https://github.com/user-attachments/assets/ba218a49-d81c-492b-8036-c4c99673062d" />

Create the file Rose.txt

## COMMAND AND OUTPUT
```
rmdir my-folder

```
<img width="545" height="137" alt="image" src="https://github.com/user-attachments/assets/fe82edbc-fcaa-4037-a3f6-fc6fb515976c" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
```
echo Hello World > hello.txt
copy hello.txt hello1.txt

```
<img width="700" height="158" alt="image" src="https://github.com/user-attachments/assets/56d6a57a-e930-4b98-b85f-cc58c65fdc5f" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
```
del hello1.txt

```
<img width="532" height="152" alt="image" src="https://github.com/user-attachments/assets/d43eb0c3-6bd6-4cf7-89e3-d1979d3eab15" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
```
dir hello1.txt

```
<img width="597" height="246" alt="image" src="https://github.com/user-attachments/assets/3b299c40-3cb0-4fcd-8d17-b5dceb876855" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

List out all the associated file extensions 

## COMMAND AND OUTPUT

  ```
assoc

```
![Uploading image.png…]()


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
```
fc hello.txt Rose.txt

```
<img width="777" height="217" alt="image" src="https://github.com/user-attachments/assets/198c1476-1a03-4c75-b8af-9a4009711bff" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```

@echo off
set name=John
echo Hello, %name%
pause

```



## OUTPUT

<img width="607" height="197" alt="image" src="https://github.com/user-attachments/assets/2e859feb-1c34-4434-b5b2-dc8b2163de3a" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off

:START
set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is Even
) else (
    echo The number is Odd
)

:ASK
set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid choice. Enter Y or N.
goto ASK

:END
echo Thank you
pause

```

## OUTPUT
<img width="542" height="293" alt="image" src="https://github.com/user-attachments/assets/32f3ce92-b786-4ed1-a5e1-cb0fc6442551" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```


@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause

```


## OUTPUT

<img width="747" height="232" alt="image" src="https://github.com/user-attachments/assets/1d3d37c8-94bb-4ec8-8ce2-d8903cce664e" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```

@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause

```
## OUTPUT
<img width="635" height="110" alt="image" src="https://github.com/user-attachments/assets/c36f8b2a-3474-43ff-a596-7b9804cc44f0" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off

:MENU
cls
echo ===== MENU =====
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid choice
pause
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File created successfully
pause
goto MENU

:EXIT
echo Goodbye
pause
exit

```

## OUTPUT

<img width="640" height="261" alt="image" src="https://github.com/user-attachments/assets/9cfff5d1-1f86-4dc3-9896-3bf504590506" />

## result
The commands/batch files are executed successfully.


# RESULT:
The commands/batch files are executed successfully.

