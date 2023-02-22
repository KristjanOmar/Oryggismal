# Öryggismál

## 13.2.3.7 Bitlocker and Bitlocker To Go
### Why is it important to save a BitLocker recovery key?

* So if you forget your log-in information, you can still access the file

### What is the function of a TPM in relation to Bitlocker?

* It is to ensure that nobody has tampered with the computer while offline and also holds the keys for encryption

---

## 13.3.2.5 Configure Windows Local Security Policy

| Policy                                      | Security Setting |
|---------------------------------------------|------------------|
| Enforce password history                    | 8                |
| Maximum password age                        | 90               |
| Minimum password age                        | 1                |
| Minimum password length                     | 8                |
| Password must meet complexity requirements  | Enabled          |
| Store passwords using reversible encryption | Disabled         |

### According to the security policy in Step 1, how many times is a user allowed to attempt to login before the account is locked?

* 5 times

### How long should the user have to wait before attempting to log back in?

* 5 minutes

### Are there any you would recommend changing? Why? [Local Security Policy > Local Policies > User Rights Assignment]

I would change the security setting for *Change the time zone* so that only administrators and the LOCAL SERVICE can change that and the security setting *Access this computer from the network* so that not *Everyone* can access the computer

| Policy                                                              | Security Setting                                                    |
|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Interactive logon: Machine inactivity limit                         | 1800 seconds                                                        |
| Devices: Allow undock without having to log on                      | Disabled                                                            |
| Interactive logon: Message title for users attempting to log on     | Caution:                                                            |
| Interactive logon: Message text for users attempting to log on      | Your activity is monitored. This computer is for business use only. |
| Interactive logon: Prompt user to change password before expiration | 7 days                                                              |

---

## 13.3.3.6 Configure Users and Groups in Windows
### What are the names of the accounts listed? [in *Computer Management*]

* Administrator
* DefaultAccount
* Guest
* Kristján
* WDAGUtilityAccount

### Select the **Groups** folder. Name five groups from the list.

* Backup Operators
* Device Owners
* Event Log Readers
* Power Users
* Replicator

### Which group does your account belong to?

* Administrators

### What is Student01 required to do when logging in the first time? [creating a user]

* They must change their password

### What group does Student01 belong to?

* Users

### From the description, can the members of the Users group make system wide changes? What can the Users group do on the computer?

* No, members of the group can *not* make system wide changes. They can, however, run most applications

### Who are the group members?

* NT AUTHORITY\Authenticated Users (S-1-5-11)
* NT AUTHORITY\INTERACTIVE (S-1-5-4)
* Staff01
* Staff02
* Student01
* Student02

### Were you successful in creating a new account? Explain. [as oone of the users you created]

* No, I wasn't as I was denied access due to the account not having the required permissions (administrative permissions)

### Were you able to navigate to **www.cisco.com**? Explain.

Yes, I was. I had internet access and the required permissions to access the internet

### With the group **ITEStaff** highlighted, what can the members do in this folder?

* They can *Read & execute*, *List folder contents*, and *Read*

### Which additional checkbox would you select? [to give the group ITEStudent full control of the folder]

* Full control

### Were you successful? Explain. [in creating a folder inside the Students folder and a text document inside]

* Yes, I was as I had the appropriate permissions to carry out such an action

### Were you successful? Explain. [in creating a folder inside the Staff folder and a text document inside]

* No, I wasn't as I lacked the required permissions to perfom such a task

### Navigate to **C:\**. Can you place a text file in the **Staff** folder? Can you modify the text file in folder **Student02**? Explain.

* No, I don't have the permissions to do that. Yes, I can, as I have full control over that folder.

### Are you able to access the content in the **Student01** and **Student02** folders? Explain.

* I am able to access the Student02 folder but not the Student01 folder as I have permissions to access the Student02 folder but not those for the Student01 folder

### Were you able to access the content in the folders Staff, Student\Student01 and Student\Student02? Explain.

* Yes, I was as the user Staff01 is in the group ITEStaff, which has access to all of those folders

### Can you log on as **Staff02**? Explain. [after disabling Staff02]

No, I can not as *Staff02* is not available to log on as because I disabled the account

### Reflection Questions
### 1. How would you give administrative privileges to the local computer to all the members of ITEStaff?

By adding all members of ITEStaff to the *Administrators* group

### 2. How would you deny access to a file for everyone except the owner?

By denying full control to every user except the owner

---

## 13.3.4.6 Lab - Configure Windows Firewall
### Under PC-1, are you able to see the shared folder **Cisco**?

* Yes, I am

### What are the benefits of Windows Firewall?

* It can help prevent hackers or malicious software from gaining access to one's PC through the Internet or a network

### Describe a negative consequence of having too many exceptions.

* It will take up more bandwidth, leaving less bandwidth for legitimate services

### Can you connect to PC-1 and view the Cisco shared folder?

* No, I can't due to an error

### Did you receive an error message on PC-2? If so, what was the Error message?

* Yes, I did. It reads: Windows can not access \\PC-1

### Can you connect to computer 1? Explain.

* Yes, now I can since PC-1 can now share files due to *File and Printer Sharing* being turned on

### List the short name of four services that are available in the **Customize Service Settings** window.

* AJRouter
* ALG
* Appinfo
* AppXSvc

### List four of the specific ICMP types.

* Source Quench
* Router Advertisement
* Time Exceeded
* Timestamp Request

### What are some possible reasons you may need to make firewall changes?

* You may need to block access for harmful services or to allow access for services that you need to use

---