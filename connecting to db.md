# this code is to connect python to mysql database

import mysql.connector

try:
    mydb= mysql.connector.connect(host="localhost", user="***", passwd="******",database="*****")

    mycursor=mydb.cursor()

    mycursor.execute("show databases")
    for i in mycursor:
        print(i)

except Exception as e:
    print("Error occured ",e)

else:
    print("Database Connected")

finally:
    print("program executed")
