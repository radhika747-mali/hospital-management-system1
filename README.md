# hospital-management-system1
patients = [
    {"name": "Radha", "age": 30},
    {"name": "Abhi", "age": 25},
    {"name": "Dh", "age": 40}
]
appointments = []
medical_records = []

# --- Menu Program —

while True:
    print("\n=====Hospital  Management System =====")
    print("1. Appointments")
    print("2. Schedule Appointment")
    print("3. Add Patient")
    print("4. Add Medical Record")
    print("5. View Bill")
    print("6. Discharge patient")
    print("7. Display All Patients")
    print("8. Exit")

    choice = input("Enter choice: ")

# 1. Appointment.

    if choice == "1":
        name = input("Enter patient name: ")
        problem = input("Enter the your problem: ")
        date = input("Enter appoinment date: ")
        appointments.append({"name": name, "Problem": problem, "Date": date})
        print(f"Appointment: {name}, ({problem}), ({date})")

    # 2. Schedule Appointment

    elif choice == "2":
        name = input("Enter patient name: ")
        time = input("Enter the schedule time: ")
        drname = input("Enter doctor name: ")
        room = input("Enter room no: ")
        appointments.append({"Name" : name, "Time": time})
        appointments.append({"Name": name, "Time": time, "Doctor": drname, "Room": room})
        print(f"\nAppointment: {name} at {time}\nMeet Dr.{drname} in room {room}")
#add patient.

    elif choice == "3":

        name = input("Enter patient name: ")
        age = int(input("Enter patient age: "))
        address = input("Enter your address: ")
        patients.append({"name": name, "age": age, "Address": address})
        print(f"Added patient: {name}, ({age} years old), ({address})")

    # 4. Add Medical Record

    elif choice == "4":
        record = input("Enter medical record: ")
        room = input("Enter room no.: ")
        medical_records.append({"record": record, "room.no": room})   
        print(f"Record added:Go to {room} room no.for {record}.")

#5. Bill

    elif choice == "5
       print("\n---- Patient Bill Record ----")
       bed_charge = int(input("Enter bed charge: "))
       electric_charge = int(input("Enter electric charge: "))
       medical_charge = int(input("Enter medical charge: "))
       total_amount = bed_charge + electric_charge + medical_charge
       print(f"Total Amount is: {total_amount}")
       
    # 6. Discharge patient

    elif choice == "6":
        name = input("Enter patient name: ")
        day =  input("Enter the patient discharge day: ")
        date = input("Enter patient discharge date: ")
        time = input("Enter the patient discharge time: ")
        room = input("Enter room no.: ")
        appointments.append({"Name" : name, "Day": day, "Date": date, "Time": time, "Room no": room})
        print(f"Discharge scheduled for: {name} was discharged on,({day}),({date}), at({time}),from room no.({room})")

# 7. Display Patients

    elif choice == "7":
        print("\n--- Patients List ---")
        for p in patients:
            print(f" * {p['name']}, {p['age']} years old")

    # 8. Exit

    elif choice == "8":
        print(" Exiting system.Thank You!")
        break

    else:
        print("Invalid choice. Try again.")
