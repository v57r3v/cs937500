java c
Commerce 2KA3 
Information Systems in Business (Winter 2025) 
Hands-on Using Microsoft Access Purpose: The purpose of   this assignment is to learn   how   to   create   a   database by using   Microsoft   Access.   In this   assignment, you will   create tables,   and make   queries   for   course   registration   from   the   perspective   of a   system   administrator.   This   assignment   has   two   parts:   (1)   completion   of the   hands-on and (2) development of   an   E-R model.
Total Marks: This assignment is scored out of 100 marks, which is worth   10% of   your final grade.Late Penalty:   Late   submissions will   incur   a   20%   (i.e.,   20 marks) penalty per   day,   meaning   that   after 5 days past the due date, late submissions receive zero marks.   Due to unexpected   difficulties   that may arise, please start and finish the assignment   as   soon   as possible.Submission Instructions: You are required to follow the steps described in this document as well   as submitting the materials described on page   12.   The submissions   (i.e.,   Access   file   and   a pdf   file   must be uploaded to the Dropbox   for Access   assignment   (assignment   1)   on   the pertinent   Avenue   account   under Assessments   >   Assignments   >   Assignment    1).   Please   note   that   any   other   form   of   submission will not be accepted.Submitting your assignment to the Dropbox on Avenue is a two-step process. One step is uploading your document to the Dropbox folder for Access Assignment on Avenue; next step is actually submitting your document to be marked. Make sure you actually submit your assignment (and not just upload it). 
Send an email to TA – Ms. Fatemeh Navazi (navazif@mcmaster.ca), for any questions that you may have about this assignment. (mention 2KA3 in the title of your email) In this assignment MS Access Software will be used. Windows users can use MS Access installed on the laptop/PC, Microsoft 365 or Vlab to access MS Access. Mac users need to use Vlab to access MS Access. 
To use Microsoft Access on Vlab, Please Connect to McMaster VPN First.   Instructions on how to connect to McMaster VPN from out   of   campus   are available   at:
https://mcmasteru365.sharepoint.com/:u:/r/sites/UTS- 
NetSoft/SitePages/All%20Software/McMasterVPN.aspx?csf=1web=1e=efDKakTo use Microsoft Access on Vlab,   please   choose   the   document   that   matches   the   operating   system of   your computer between the following two documents and follow   the   instructions.   Both documents are shared   on Avenue.
Windows Instructions:
Avenue-> COMMERCE 2KA3:Information Systems in Business-> Content-> Assignments-> Assignment #1 -> vlab-Virtual-Applications-Instructions-Windows 
Mac Instructions:
Avenue-> COMMERCE 2KA3:Information Systems in Business-> Content-> Assignments-> Assignment #1 -> vlab-Virtual-Applications-Instructions-OSX1 
You may access MS Access   Software through the   "Access" icon on VLAB Resources.

For any issues related to Vlab, please Contact DSB IT department   at
dsbhelp@mcmaster.caand   make   sure   to   include   your   full   name, your   MacID, and   the   course number in your request.
Part 1 
1. Getting started 
Before starting the assignment, make yourself   familiar with the Microsoft   Access Interface.
2. Creating tables (20 Marks) 
From the Access file menu, select New, then:
a. Select the Blank Desktop Database icon in the main panel. Name your database   file Assign and   click   the   folder   icon   next   to   the   FileName

b. From the opened window, select Desktop and click   OK.

c. Finally,   click on Create button. 
Data   are   stored   in   tables   in   Access.   A   table   consists   of columns,   called   fields,   and   rows,   called   records.   To   store data   for   course registration processing you need to   create   four   tables: Courses, Registrations, RegistrationLn,    and Students.      The Courses table      is      used      to      store      course   information; the Registration table is used to store student registration; the RegistrationLn table   is used to   store   detailed registration   lines   for   each   registration;   and the Students table   is   used   to   store detailed student information. Their structures are   shown   as   follows:
Table 1. The Structure of Four Tables 
Table Name 
Field Name 
Key 
Data Type 
Field Size 


Courses 
Course_ID 
Course_Name Course_Days Prof_Name 
* Short Text Short Text Short Text Short Text 
4 
25 
20 
15 



Registration 
Registration_Number Student_ID 

Registration_Date 
* 
Number Number 

Date/Time 
Integer Integer 

Current date as 
the default 
value 
RegistrationLn 
Registration_Number Course_ID 
* * 
Number ShortText 
Integer 4 


Students 
Student_ID 
Student_Name Email 
Address 
Phone_Number 
* Number ShortText ShortText ShortText Number 
Integer 20 
20 50 
Long Integer Now we want to create   a table for   Courses,   Registrations,   RegistrationLn,   and   Students.   To   create   a   table, under the Create tab,   select the Table Design icon.   You   need   to   specify   the 代 写Information Systems in Business (Winter 2025)SPSS
代做程序编程语言  field   Name,   the   Data   Type,   the   key,   and   field properties.   All   the   required   data   to   create   tables   is   shown   in   Table   1.   Give the table   a name when you   save it   (see   the   table   names   in   the   above   list).    Please   reference   the   following    figure    for    creating    each    of   your    new    tables.    The    specification    of    field    properties    is   straightforward. Learn the meanings of   field properties from Help and specify them   accordingly.
Note: To   specify   a   key   field,   click   the   cell   to   the   left   side   of a   field   name   and   then   right   click   and   select Primary Key or select the Primary Key icon under the Design tab. 
Figure 2. Use Design View to Create a Table 

Set the Default value of Registration_Date field as Date() by clicking the button of   the field Default
Value and building expression in the following window.
Figure 3. Build expression Date() 
Note: To       specify          a       concatenated       key          in       the RegistrationLn table,          select       both       the Registration_Number field and Course_ID field (hold    while   you left click them), and then   right click or push the icon to set both fields as   the   concatenated primary   key.
3. Specifying relationships and integrity control (20 Marks) Referential   Integrity   refers   to    ensuring   that   the   records   in   related   tables   in   our   database   are   consistent   with   one   another.    When    enforcement   of referential    integrity   is   in   effect,   Microsoft   Access   does   not   let   you   add   records   to   a   related   table   when   there   is   no   associated   record   in   the   primary table.   For example, in   the RegistrationLn table, there is a record Registration_Number which   should   also   exist   in the Registration table.    Referential   integrity   also   allows updating   and   deleting   data   in   related   tables.    For   example,   when   a Registration_Number is   deleted   from   the Registration table,    then       all      associated Registration_Numbers      are      also      deleted      from    the RegistrationLn table.
In Access, the relationships (the links created through foreign keys) between tables can be   explicitly specified. Integrity can then be defined based on these links.From    the    main    toolbar,    select      the Relationships icon      from      the Database Tools tab.       The Relationships window    will       emerge      and    the Show       Table window    will      popup.       Click    the Registration table,    and    the Add button.      Similarly,      add      the RegistrationLn, Courses and Students tables, so the fourstables appear in a row in the Relationships window.   Close the Show Table window.Click       and       drag       the Registration_Number field       in       the Registration field       list       to         the Registration_Number field   in   the RegistrationLn field   list.   An   Edit   Relationships   window   opens.   Then,   click   the Enforce Referential Integrity check   box.      Click   the Cascade Delete Related Records check box.    This means that, if   you   delete   a   registration,   the   system   will   delete   all    the    registration    lines    related    to    this    registration.       Click    the Create button    to    create    this   relationship.   The   Relationships   window   display   now   illustrates   that   you   have   created   a One to Many relationship from Registration to RegistrationLn.
Note - Ifyou receive a table locked error message, close the tables you are working on.
Figure 4.    Edit Relationships 
Click   and   drag   the Course_ID field   in   the Courses field   list   to   the Course_ID field   in   the RegistrationLn field list.    Click the Enforce Referential Integrity check box, and then click the Cascade Update Related Fields check box. This means that, if   you change the Course_ID in the Coursestable, the same Course_ID will be changed in all of   related records in the RegistrationLn table. Click the Create button to create this relationship.Click   and   drag   the Student_ID field   in   the Students field   list   to   the Student_ID field   in   the Registration field    list.    Click      the Enforce Referential Integrity check    box.Then      click      the Cascade Update Related Fields check   box.   This   means   that,   if you   change   the Student_ID in   the Students table,   the   same Student_ID will   be   changed   in   all   of related   order   records   in   the Registration table.
The Relationship dialogue box should appear as shown in   the   following   figure   (Figure   5).Note: If you   want   to   delete   or   edit   an   existing   relationship,   right   click   the   line joining   the   two   tables   of interest   and   select Edit Relationship.   After   finishing with your relationships,   click the X icon   in   the   upper   right   corner   of   the   Relationships   window   and Close this   window.      The   relationships you defined will be saved automatically.
Figure 5.    Define the Relationships between Four Tables 


         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
