<h1>Computer Forensics - Floppy Disk</h1>

<h3>Objective</h3>
The aim of this project is to analyze aa disk image of a woman called Emma. She is involved in an incident and we have to find evidence of it.
<br /> <br />
<h3>Skills Learned</h3>
● Data recovery <br />

<br />
<h3>Tools Used</h3>
● Scalpel <br />
● FreeWordExcel document password cracker <br />
● Autopsy <br />
<br />
<h3>Steps</h3>
Firstly, we unzipped the folder containing the disk image in Kali, getting its contents:
<br />
<img width="258" alt="floppy1" src="https://github.com/user-attachments/assets/c33c29fb-bf6d-47c1-8d5f-27039647408e">
<br />
*Ref 1: Extracted zip file of the disk image*
<br />
<br />
Then, 31 files were recovered using the Scalpel tool to recover the deleted data in the floppy disk.
<br />
<img width="439" alt="floppy2" src="https://github.com/user-attachments/assets/631ae098-4075-4a02-b02f-813f11f32529">
<br />
<img width="440" alt="floppy3" src="https://github.com/user-attachments/assets/dabce1c9-7442-4411-8fb2-7acbca1c9aea">
<br />
*Ref 2: Recovered data with Scalpel*
<br />
<br />
We moved the obtained files to a Windows machine for better manipulation.
<br />
The files that we got were organized in the following folders:
<br />
<img width="197" alt="floppy4" src="https://github.com/user-attachments/assets/8ebe7903-fbce-49d8-bf8b-2e6d3d4f98e9">
<br />
*Ref 3: Recovered data folder structure*
<br />
<br />
● Doc-22-0: seemed to contain word documents files. We’ll talk about this folder later.
<br />
<img width="407" alt="floppy5" src="https://github.com/user-attachments/assets/34e1a6cb-c5dc-40b9-80d0-9409518f4110">
<br />
*Ref 4: Recovered data Doc-22-0 folder*
<br />
<br />
● Doc-23-0: seemed to contain word documents file, same as the previous folder.
<br />
<img width="405" alt="floppy6" src="https://github.com/user-attachments/assets/6395313a-53a8-4323-abef-5f554f007d7a">
<br />
*Ref 5: Recovered data Doc-23-0 folder*
<br />
<br />
● Mov-16-0: seemed to contain video files, but when we tried to open them, nothing was displayed.
<br />
<img width="292" alt="floppy7" src="https://github.com/user-attachments/assets/d05866d8-bc04-4ba9-b2fe-105dd70cd807">
<br />
*Ref 6: Recovered data Mov-16-0 folder*
<br />
<br />
● Pgp-37-0: seemed to contain pgp files. When opening them with the notepad, we didn't find anything relevant.
<br />
<img width="302" alt="floppy8" src="https://github.com/user-attachments/assets/91bb6edf-57f8-4ffc-bf06-ed43492dc1e0">
<br />
*Ref 7: Recovered data Pgp-37-0 folder*
<br />
<br />
● Pgp-38-0: seemed to contain pgp files. When opening them with the notepad, we didn't find anything relevant.
<br />
<img width="320" alt="floppy9" src="https://github.com/user-attachments/assets/f39ea6d1-5516-4141-8d5f-3d326005120e">
<br />
*Ref 8: Recovered data Pgp-38-0 folder*
<br />
<br />
The important folder would be the doc-22-0 one. Once we opened it we noticed what appeared to be four word documents.
<br />
<img width="340" alt="floppy10" src="https://github.com/user-attachments/assets/004c8ed8-47ad-4a08-8f5f-87fe606a5754">
<br />
*Ref 9: Recovered data doc-22-0 folder*
<br />
<br />
The first file (with the number 19) was actually a word document, but did not contain relevant information.
<br />
<img width="706" alt="floppy11" src="https://github.com/user-attachments/assets/27defc0b-73f0-43a7-8542-ed2b1e484d00">
<br />
*Ref 10: Recovered data doc-22-0 folder file 19*
<br />
<br />
The same thing happened when opening the second document (with the number 20), it was a word document with not relevant information.
<br />
<img width="806" alt="floppy12" src="https://github.com/user-attachments/assets/3d1f9f49-6e75-4af4-8aaf-5c3f557f3c91">
<br />
*Ref 11: Recovered data doc-22-0 folder file 20*
<br />
<br />
The third document (with the number 21) was in fact the same as the previous one.
<br />
<img width="806" alt="floppy12" src="https://github.com/user-attachments/assets/3d1f9f49-6e75-4af4-8aaf-5c3f557f3c91">
<br />
*Ref 12: Recovered data doc-22-0 folder file 21*
<br />
<br />
However, when we tried to open the fourth file (the one with the 22) as well with Word, we got this pop up. Which indicated that it wasn’t actually a word document like the rest.
<br />
<img width="604" alt="floppy13" src="https://github.com/user-attachments/assets/8a2b099d-3939-4f09-9edf-38def6f67c28">
<br />
*Ref 13: Recovered data doc-22-0 folder file 22*
<br />
<br />
We then opened this file with the notepad to see some clues on what this file could be, and we saw something that looked like a spreadsheet.
<br />
<img width="452" alt="floppy14" src="https://github.com/user-attachments/assets/3865b7b8-0994-4ac1-aca1-0c0fde4596d0">
<br />
*Ref 13: Recovered data doc-22-0 folder file 22 opened with notepad*
<br />
<br />
So we converted the file to an excel document with the .xls extension. But when trying to open it, we were asked for a password.
<br />
<img width="382" alt="floppy15" src="https://github.com/user-attachments/assets/25bc4b0e-b1e4-4df8-a3d9-fc99058c1c1f">
<br />
*Ref 14: Recovered data doc-22-0 folder file 22 transformed to .xls*
<br />
<br />
We didn’t know the password, as in the other documents we couldn’t find any hints on what could it be.
<br />
So in order to get the password, we tried a brute-force attack to get the password, as we did not find it in any other file. For this we used the application FreeWordExcel.
<br />
<img width="662" alt="floppy16" src="https://github.com/user-attachments/assets/0d921708-c40b-4392-8871-73345d2fa260">
<br />
*Ref 15: FreeWordExcel document password cracker*
<br />
<br />
The password is “crook”.
<br />
By inserting the password, we could obtain the xls file content:
<br />
<img width="662" alt="floppy17" src="https://github.com/user-attachments/assets/df1f0ba1-b3d6-43ed-b124-44f832bf7791">
<br />
*Ref 15: Excel content*
<br />
<br />
In addition, we uploaded the floppy.dd into autopsy to get more information, and we saw Mss Crook there with the label “BYE-BYE”, plus the date of 15/9/2004 when the incident occurred.
<br />
<img width="665" alt="floppy18" src="https://github.com/user-attachments/assets/369ee727-e948-4a22-ac6d-379888f5b4cc">
<br />
*Ref 16: Autopsy evidences*
