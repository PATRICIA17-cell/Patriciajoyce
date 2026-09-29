def calculate_average(score1, score2, score3):
    return (score1 + score2 + score3) / 3


number_of_students = int(input("How many students? "))

while number_of_students < 3:
    print("The program must process at least 3 students.")
    number_of_students = int(input("How many students? "))

for student_number in range(1, number_of_students + 1):
    print("\nStudent", student_number)

    name = input("Enter name: ")

    activity1 = float(input("Activity 1: "))
    activity2 = float(input("Activity 2: "))
    activity3 = float(input("Activity 3: "))

    average = calculate_average(activity1, activity2, activity3)

    if average >= 90:
        status = "Excellent"
    elif average >= 80:
        status = "Very Good"
    elif average >= 75:
        status = "Passed"
    else:
        status = "Failed"

    print("\nAverage:", round(average, 2))
    print("Status:", status)