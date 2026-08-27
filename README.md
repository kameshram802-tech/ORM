# Ex01 Django ORM Web Application
# Date: 27-08-2026
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 cars

# PROGRAM

## admim.py

```
from django.contrib import admin
from django.contrib.auth.models import User, Group
from .models import Student

@admin.register(Student)
class StudentAdmin(admin.ModelAdmin):

    list_display = (
        'name',
        'register_no',
        'department',
        'year',
        'email',
        'mobile',
        'date_of_birth',
    )

    search_fields = (
        'name',
        'register_no',
        'department',
        'email',
    )


    admin.site.unregister(User)
    admin.site.unregister(Group)
```

## Model.py

```
from django.db import models

class Student(models.Model):
    name = models.CharField(max_length=100)
    register_no = models.IntegerField()
    department = models.CharField(max_length=100)
    year = models.IntegerField()
    email = models.EmailField()
    mobile = models.CharField(max_length=15)
    date_of_birth = models.DateField()

    def __str__(self):
        return self.name
```

# OUTPUT
![alt text](<Screenshot 2026-08-27 085251.png>)
# RESULT
Thus the program for creating a database using ORM hass been executed successfully
