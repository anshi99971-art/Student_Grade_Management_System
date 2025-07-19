def calculate_grade(avg):
    if avg >= 90:
        return 'A+'
    elif avg >= 80:
        return 'A'
    elif avg >= 70:
        return 'B'
    elif avg >= 60:
        return 'C'
    elif avg >= 50:
        return 'D'
    else:
        return 'F'

students = []

n = int(input("Enter number of students: "))

for i in range(n):
    print(f"\nEnter details for Student {i+1}")
    name = input("Name: ")
    marks = []

    for j in range(3):
        mark = int(input(f"Enter marks for Subject {j+1}: "))
        marks.append(mark)

    total = sum(marks)
    avg = total / 3
    grade = calculate_grade(avg)

    student_data = {
        "name": name,
        "marks": marks,
        "total": total,
        "average": avg,
        "grade": grade
    }

    students.append(student_data)

print("\n=== Student Report ===")
for stu
