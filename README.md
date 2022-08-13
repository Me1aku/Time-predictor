# Time-predictor
# A code me and @SaimonAlam001 made to predict the end of a meeting or gathering.

hour = int(input("Starting time (hours): "))
mins = int(input("Starting time (minutes): "))
A_or_P = str(input("Was the event in the am or pm? "))
dura = int(input("Event duration (minutes): "))
if hour <12 and A_or_P == "pm":
    hour = hour + 12
elif hour == 12 and A_or_P == "am":
    hour = 0
elif hour == 12 and A_or_P == "pm":
    hour = 12
else:
    hour = hour
mins = (dura + mins) # find a total of all minutes
hour = (hour + mins // 60) # find a number of hours hidden in minutes and update the hour
mins = (mins % 60) # correct minutes to fall in the (0..59) range
hour = (hour % 24) # correct hours to fall in the (0..23) range
if hour == 13:
    hour = 1
    A_or_P = "pm"
elif hour == 14:
    hour = 2
    A_or_P = "pm"
elif hour == 15:
    hour = 3
    A_or_P = "pm"
elif hour == 16:
    hour = 4
    A_or_P = "pm"
elif hour == 17:
    hour = 5
    A_or_P = "pm"
elif hour == 18:
    hour = 6
    A_or_P = "pm"
elif hour == 19:
    hour = 7
    A_or_P = "pm"
elif hour == 20:
    hour = 8
    A_or_P = "pm"
elif hour == 21:
    hour = 9
    A_or_P = "pm"
elif hour == 22:
    hour = 10
    A_or_P = "pm"
elif hour == 23:
    hour = 11
    A_or_P = "pm"
elif hour == 0:
    hour = 12
    A_or_P = "am"
elif hour == 12:
    A_or_P = "pm"
else:
    hour = hour
if mins == 0:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 1:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 2:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 3:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 4:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 5:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 6:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 7:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 8:
    print(hour, ":", "0", mins, A_or_P, sep='')
elif mins == 9:
    print(hour, ":", "0", mins, A_or_P, sep='')
else:
    print(hour, ":", mins, A_or_P, sep='')
 
