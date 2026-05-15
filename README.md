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

Remove the directory "my-folder"

<img width="1920" height="111" alt="image" src="https://github.com/user-attachments/assets/cd901a99-87b2-42c7-bec4-43728e80a6df" />


## COMMAND AND OUTPUT

Create the file Rose.txt

<img width="1920" height="102" alt="image" src="https://github.com/user-attachments/assets/084e0419-0f82-4b30-8479-0dcaf64f9984" />

## COMMAND AND OUTPUT

Create the file hello.txt using echo and redirection


<img width="1920" height="105" alt="image" src="https://github.com/user-attachments/assets/ae64019a-e1b1-4575-ab16-98b0bffebb08" />


## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt


<img width="1920" height="113" alt="image" src="https://github.com/user-attachments/assets/07fa769f-3b9e-493d-b433-c11437b722bc" />


## COMMAND AND OUTPUT

Remove the file hello1.txt

<img width="1920" height="131" alt="image" src="https://github.com/user-attachments/assets/cd12801b-13b2-47de-a705-cf4233086de9" />

## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory

<img width="1920" height="105" alt="image" src="https://github.com/user-attachments/assets/6b985d43-ab22-4bd5-84bd-9dd80aa964ea" />

## COMMAND AND OUTPUT

List out all the associated file extensions 

<img width="1920" height="250" alt="image" src="https://github.com/user-attachments/assets/34531980-bc13-4b16-a743-4031860cd840" />

## COMMAND AND OUTPUT

Compare the file hello.txt and rose.txt

<img width="1920" height="773" alt="image" src="https://github.com/user-attachments/assets/5ef9baea-ff77-4f97-972a-313837556ce9" />

## COMMAND AND OUTPUT

<img width="1920" height="210" alt="image" src="https://github.com/user-attachments/assets/6360fcc0-37c1-4af9-891d-d4deb8c75490" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".


## PROGRAM
```
@echo off
set name=John
echo Hello, %name%
pause
```


## OUTPUT


<img width="445" height="80" alt="Screenshot 2026-05-15 111246" src="https://github.com/user-attachments/assets/4f430daa-deb4-4739-ba7c-760713b1ff13" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

## PROGRAM
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

set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid Input
goto START

:END
echo Thank You
pause
```

## OUTPUT

<img width="635" height="204" alt="Screenshot 2026-05-15 111556" src="https://github.com/user-attachments/assets/d24edc05-af62-4cf1-ad2f-ce32e0ee6d46" />

Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.


## PROGRAM
```
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```

## OUTPUT


<img width="511" height="172" alt="Screenshot 2026-05-15 111836" src="https://github.com/user-attachments/assets/7661832e-ce5d-4ab0-9850-8a92191f9db7" />


Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## PROGRAM
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


<img width="831" height="227" alt="Screenshot 2026-05-15 112954" src="https://github.com/user-attachments/assets/870ac80a-eca8-42b6-87ce-408dcc9a65b1" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## PROGRAM
```
@echo off

:MENU
echo ====================
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo ====================

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid Choice
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File Created
pause
goto MENU

:EXIT
echo Goodbye
pause
exit
```

## OUTPUT


<img width="524" height="398" alt="Screenshot 2026-05-15 113239" src="https://github.com/user-attachments/assets/cb9a3331-e909-4d29-bc1b-1c031d04ca6f" />


# RESULT:
The commands/batch files are executed successfully.

