# KeywordsSuggest - Version Alpha 0.0 Licence GPL 3
Anakeyn Keywords Suggest is a keywords suggestion tool for SEO and Web Maketing purpose.
This tool searches in the first  x pages responding to a given keyword in Google. 

Next the system will get the content of the pages in order to find popular and original  keywords/Expressions 
in the subject area. The system works  with a TF-IDF  algorithm.

TF-IDF means term frequency–inverse document frequency. TF-IDF is a numerical statistic that is intended to reflect 
how important a word is to a document in a collection or corpus.

In order to calculate a "global" TF-IDF value we calculate a mean of TF-IDF for each terms from all documents to 
find popular expressions and an non-zero mean of each term from all documents for original expressions.

The program is developed in Python in a Web format using Flask (web framework), Jinja2 (web template engine), 
SQLALchemy (Object-relational mapping for SQL databases),Bootstrap (front-end framework) ...

STRUCTURE (see in raw):
KeywordsSuggest
|   database.db
|   favicon.ico
|   keywordssuggest.py
|   license.txt
|   myconfig.py
|   __init__.py
|   
+---configdata
|       tldLang.xlsx
|       user_agents-taglang.txt
|       
+---static
|   |   Anakeyn_Rectangle.jpg
|   |   keywordssuggest.css
|   |   Oeil_Anakeyn.jpg
|   |   signin.css
|   |   starter-template.css
|   |   
|           
+---templates
|       index.html
|       keywordssuggest.html
|       login.html
|       signup.html
|       
+---uploads


By default the systeme works with a sqlite database calls database.db which is create the first time you use the program.
The main program is "keywordssuggest.py".

Default config variables are in the myconfig.py file including the 2 default users admin (pwd "adminpwd") 
and guest (pwd "guestpwd")

Other configuration data is available in the configdata subdiretory in 2 files :
tldlang.xlsx : parameters for Google Top Level domains and Search Engines Results Pages languages (358 combinations)
user_agents-taglang.txt :  a list of valid user agents to provide to Google randomly to avoid blocking. (4281)

Static directory contains images and .css files

Templates directory contains .html templates.

Uploads directory is dedicated to create/save all keywords files to download.

The system creates 7 "popular" keywords/expressions files : 1 file with all sizes expression in words, 
and one file for respectively 1, 2, 3, 4, 5 or 6 words expressions.
The same for "original"  keywords/expressions files. 
If available the system provides a maximum of 10.000 expressions for each file. This could be enough to get ideas :-) 





