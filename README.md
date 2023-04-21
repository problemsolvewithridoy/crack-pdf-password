
# Open PDF file without password using python.

This Python script provides a solution to open password-protected PDF files. It uses the PyPDF2 library to remove the password from the PDF file and then opens it in the default PDF viewer of your system. This can come in handy if you have forgotten the password of a PDF file that you urgently need to access. With just a few lines of Python code, you can easily open the PDF file without needing to enter the password.

let's start...............

To make this project you need to follow this step:-










## Installation

Install package with pip

```bash
  pip install pikepdf
  pip install colorama

```
    
## Deployment

To deploy this project run

```bash
#please subscribe "Problem Solve With Ridoy" youtube channel

import pikepdf
import time
from colorama import Fore

password_file = open("yourPasswordFileName.txt")

i = 0
start_time = time.time()
for password in password_file:
    i += 1
    print(Fore.RED+f"\r {i} Password is tested {password.strip()}", end = "")
    try:
        pikepdf.open("YourPDFFileNmae.pdf",password = password.strip("\n"))
        end_time = time.time()
        print("\n")
        print(Fore.GREEN+ f"password found in {str(end_time-start_time)[:4]} second \nPassword is: ", end = "")
        print(Fore.BLUE+ f" {password}")

        break
    except:
        pass
```


## 







## You can follow me

Facebook:- https://www.facebook.com/problemsolvewithridoy/

Linkedin:- https://www.linkedin.com/in/ridoyhossain/

YouTube:- https://www.youtube.com/@problemsolvewithridoy

Gmail:- entridoy2@gmail.com

If you have any confusion, please feel free to contact me. Thank you

