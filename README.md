# goalkicker is a website with programming books (pdf)
https://goalkicker.com/
- This repo contains all 47 books from the website.
- You can download by yourself also using this script below.
```python
import requests
import re

PDF_URLS = [
    "https://goalkicker.com/DotNETFrameworkBook/DotNETFrameworkNotesForProfessionals.pdf",
    "https://goalkicker.com/AlgorithmsBook/AlgorithmsNotesForProfessionals.pdf",
    "https://goalkicker.com/AndroidBook/AndroidNotesForProfessionals.pdf",
    "https://goalkicker.com/Angular2Book/Angular2NotesForProfessionals.pdf",
    "https://goalkicker.com/AngularJSBook/AngularJSNotesForProfessionals.pdf",
    "https://goalkicker.com/BashBook/BashNotesForProfessionals.pdf",
    "https://goalkicker.com/CBook/CNotesForProfessionals.pdf",
    "https://goalkicker.com/CPlusPlusBook/CPlusPlusNotesForProfessionals.pdf",
    "https://goalkicker.com/CSharpBook/CSharpNotesForProfessionals.pdf",
    "https://goalkicker.com/CSSBook/CSSNotesForProfessionals.pdf",
    "https://goalkicker.com/EntityFrameworkBook/EntityFrameworkNotesForProfessionals.pdf",
    "https://goalkicker.com/ExcelVBABook/ExcelVBANotesForProfessionals.pdf",
    "https://goalkicker.com/GitBook/GitNotesForProfessionals.pdf",
    "https://goalkicker.com/HaskellBook/HaskellNotesForProfessionals.pdf",
    "https://goalkicker.com/HibernateBook/HibernateNotesForProfessionals.pdf",
    "https://goalkicker.com/HTML5Book/HTML5NotesForProfessionals.pdf",
    "https://goalkicker.com/HTML5CanvasBook/HTML5CanvasNotesForProfessionals.pdf",
    "https://goalkicker.com/iOSBook/iOSNotesForProfessionals.pdf",
    "https://goalkicker.com/JavaBook/JavaNotesForProfessionals.pdf",
    "https://goalkicker.com/JavaScriptBook/JavaScriptNotesForProfessionals.pdf",
    "https://goalkicker.com/jQueryBook/jQueryNotesForProfessionals.pdf",
    "https://goalkicker.com/KotlinBook/KotlinNotesForProfessionals.pdf",
    "https://goalkicker.com/LaTeXBook/LaTeXNotesForProfessionals.pdf",
    "https://goalkicker.com/LinuxBook/LinuxNotesForProfessionals.pdf",
    "https://goalkicker.com/MATLABBook/MATLABNotesForProfessionals.pdf"
    "https://goalkicker.com/MicrosoftSQLServerBook/MicrosoftSQLServerNotesForProfessionals.pdf",
    "https://goalkicker.com/MongoDBBook/MongoDBNotesForProfessionals.pdf",
    "https://goalkicker.com/MySQLBook/MySQLNotesForProfessionals.pdf",
    "https://goalkicker.com/NodeJSBook/NodeJSNotesForProfessionals.pdf",
    "https://goalkicker.com/ObjectiveCBook/ObjectiveCNotesForProfessionals.pdf",
    "https://goalkicker.com/OracleDatabaseBook/OracleDatabaseNotesForProfessionals.pdf",
    "https://goalkicker.com/PerlBook/PerlNotesForProfessionals.pdf",
    "https://goalkicker.com/PHPBook/PHPNotesForProfessionals.pdf",
    "https://goalkicker.com/PostgreSQLBook/PostgreSQLNotesForProfessionals.pdf",
    "https://goalkicker.com/PowerShellBook/PowerShellNotesForProfessionals.pdf",
    "https://goalkicker.com/PythonBook/PythonNotesForProfessionals.pdf",
    "https://goalkicker.com/RBook/RNotesForProfessionals.pdf",
    "https://goalkicker.com/ReactJSBook/ReactJSNotesForProfessionals.pdf",
    "https://goalkicker.com/ReactNativeBook/ReactNativeNotesForProfessionals.pdf",
    "https://goalkicker.com/RubyBook/RubyNotesForProfessionals.pdf",
    "https://goalkicker.com/RubyOnRailsBook/RubyOnRailsNotesForProfessionals.pdf",
    "https://goalkicker.com/SpringFrameworkBook/SpringFrameworkNotesForProfessionals.pdf",
    "https://goalkicker.com/SQLBook/SQLNotesForProfessionals.pdf",
    "https://goalkicker.com/SwiftBook/SwiftNotesForProfessionals.pdf",
    "https://goalkicker.com/TypeScriptBook2/TypeScriptNotesForProfessionals.pdf",
    "https://goalkicker.com/VBABook/VBANotesForProfessionals.pdf",
    "https://goalkicker.com/VisualBasic_NETBook/VisualBasic_NETNotesForProfessionals.pdf",
    "https://goalkicker.com/XamarinFormsBook/XamarinFormsNotesForProfessionals.pdf"
]

for URL in PDF_URLS:
    filename = URL.split('/')[-1]
    r = requests.get(URL, stream=True)
    with open(filename, 'wb') as f:
        for chunk in r.iter_content(chunk_size=1024):
            if chunk:
                f.write(chunk)
                f.flush()
        f.close()
```
