# Using-tools-like-John-the-Ripper-for-password-cracking
## AIM:
To crack the password of a ZIP file using John the Ripper on Kali Linux by
extracting the hash value

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).


### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:
Password Cracking with John the Ripper

## OUTPUT:
### Create an txt file 

• Right-click on the Desktop and choose Create Document → Empty Document.

• Name the file: anyname.txt

![alt text](<LAB-7 IMG-1.png>)

![alt text](<LAB-7 IMG-2.png>)

### Create a Password-Protected ZIP File 

• Right-click on name.txt → Create Archive → Select .zip format.

• Click Other Options, set a password (e.g., 1234), then click Create.

• A file named name.txt.zip will appear.

![alt text](<LAB-7 IMG-3.png>)

![alt text](<LAB-7 IMG-4.png>)




### Open John-The-Ripper Tool

• Click on the Kali menu or press the Super (Windows) key.


• Search for “john” and click it — this opens the terminal with John the
Ripper installed.

![alt text](<LAB-7 IMG-5.png>)

![alt text](<LAB-7 IMG-6.png>)

### Generate Hash Using zip2john

• Run: “ls” command to confirm whether zip file is present

![alt text](<LAB-7 IMG-7.png>)

and type the following command below
```
zip2john afshan.txt.zip > hash.txt
```
![alt text](<LAB-7 IMG-8.png>)


• Type the command cat hash.txt or Open the file hash.txt

```
cat hash.txt
```
![alt text](<LAB-7 IMG-10.png>)

#### or

• Open hash.txt file

![alt text](<LAB-7 IMG-9.png>)

### Start Cracking the Password
• Type the following command to crack the password:

```
john --format=zip --mask=?d?d?d?d hash.txt

```

![alt text](<LAB-7 IMG-11.png>)

### View the Cracked Password
• After cracking is complete, reveal the password using:
```
john --show hash.txt

```
![alt text](<LAB-7 IMG-12.png>)
## RESULT:
The password hashes were successfully cracked using John the Ripper.
