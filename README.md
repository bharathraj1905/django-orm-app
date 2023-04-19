# Django ORM Web Application

## AIM

To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:

Create a django application

### STEP 2:

write your code in models.py and admin.py

### STEP 3:

End of the program

## PROGRAM

### models.py
```python
from django.db import models
from django.contrib import admin

# Create your models here.

class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    department=models.CharField(max_length=30)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','department')
```

### admin.py
```python
from django.contrib import admin
from.models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```

## OUTPUT

### serveroutput
![so](https://user-images.githubusercontent.com/121490575/232955473-61bcce5d-0ad4-43c2-bbbe-a50c77a52eb6.png)

### clientoutput
![co](https://user-images.githubusercontent.com/121490575/232955497-772d5646-10a1-4746-b2b1-eec559bce404.png)

## RESULT
Thus the code has been executed successfully.
