# Bachelors-FinalYearProject
Final Year Project Title: "Format Checking of FYP Reports (Word files)". 
•	This repository contains source code of my bachelors final year project and also Report of it. 
•	This repository is only created to demonstrate source code for admission in masters in Germany.
•	As, I'll get my degree and complete transcript in end of June or on earliest of July, so this fyp is not yet evaluated on transcript I uploaded on the time of admission in University of Passau but the defence of FYP has been conducted and passed, also the documentation is not yet countersigned by university officials as it is due in the mid of June. 

ABSTRACT:
Purpose of this final year project is to streamline the evaluation process for the National University of Modern Languages (NUML). 
This is done by developing a web application that automatically verifies all necessary criteria in student’s final year project reports, such as heading’s font size and style, alignments, logos, static words, chapter names and paragraph headings, sub-headings, referrences, tables & diagrams, minimum word counts in specific paragraphs, table of contents and figures etc. 
I’ve also introduced SMTP services in my project, so the Final Year Project Report's FILE CONTAINING RED HIGHLIGHTED ERRORS and also a LOG FILE which contains each and every validation in text file is sent to the provided email automatically.
So Now Teachers no longer need to assess each report manually my application will go through the initial phase of checking requirements and format of provided content in FYP reports. It is created using .NET development and validates all required fields by going through each word from the Word file.
NOW, the frontend is being refreshed when there will be portal for students and administration. The previous work that has been done is that when student inserts his FYP Report and provide his email in portal, he gets an email with 2 validation files discused above and also he can download by clicking on them in portal. Now we have to add 1 more functionality which is when user validates his FYP REPORT, he also gets a automatically generated TOKEN. This token can be used in administration portal where administration just Searches that provided token and he can see which students have validated final year project report.  

FYP Evaluation time period: 
•	The Defence of my Final year project was successfully passed in May but the final marking will appear in my final transcript on end of June / start of July 2023. 

•	To perform this functionality .NET development is used both console and ASP.NET development. To fetch the data from Word file (.doc) I have used library named "SpireDoc".

•	For the validation of student's first 7 pages of FYP REPORT, I defined the rules in database by "Regular Expression" in some cases and by static words(like font, bold, unbold, alignment) in some case because there are so many static keywords in first 7 pages of FYP REPORTS like dates, names, specific format etc. Code of these can be found in Business Layer, So there is separate file for every page as every page has its own name like certificate page, abstract page and so on

•	After 7 pages, there is a check whether TABLE OF CONTENT, LIST OF FIGURES and LIST OF TABLES are AUTOGENERATED or not.

•	Then comes the main part which is CHAPTERS. In chapters, chapters name, chapters headings and sub-headings are directly compared with corresponding chapters name, headings, sub-headings which are present in TABLE OF CONTENT in SEQUENCE. Also, more details are checked like: bold/unbold, fort size, font style, alignment, word count of main paragraph and its sub-paragraphs, availability of diagrams and tables as they are mentioned in "List of Figures" & "List of Tables". Code of this can be found in ManagementLayer.cs file inside Business Layer. At the end References are validated.


