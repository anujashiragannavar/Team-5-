# Team-5-
import pypandoc

md = """# Parking – Vehicle Entry and Exit Management System

## Project Overview

The **Parking – Vehicle Entry and Exit Management System** is designed to manage vehicle entry, parking slot allocation, vehicle exit, parking duration, and parking fee calculation.

The system maintains vehicle details, parking slot information, entry and exit times, and parking records for future reference. It is intended to provide a simple, fast, accurate, secure, and reliable way to manage parking operations.

The project is based on the provided problem statement and includes four main parts: **Requirements, Algorithm, Flowchart, and ER Diagram**. The problem statement specifies vehicle details, parking slots, entry time, exit time, and parking fee as the main feature set. fileciteturn0file0L2-L9

---

## 1. Requirements

### Functional Requirements

The system should:

- Register vehicle details such as vehicle number, vehicle type, and owner details.
- Check the availability of parking slots.
- Assign an available parking slot when a vehicle enters.
- Record the vehicle entry time.
- Record the vehicle exit time.
- Calculate the parking duration.
- Calculate the parking fee based on parking duration.
- Display the parking fee when the vehicle exits.
- Mark the parking slot as available after the vehicle exits.
- Store parking records for future reference. fileciteturn0file0L10-L23

### Non-Functional Requirements

The system should provide:

- A simple and user-friendly interface.
- Accurate time and fee calculation.
- Fast vehicle entry and exit processing.
- Secure storage of vehicle and parking information.
- Reliable and consistent data management. fileciteturn0file0L24-L29

---

## 2. Algorithm

1. **Start**
2. Enter vehicle details.
3. Check available parking slots.
4. If a slot is available, assign the parking slot.
5. Record the vehicle entry time.
6. When the vehicle exits, enter or find the vehicle number.
7. Record the vehicle exit time.
8. Calculate the parking duration.
9. Calculate the parking fee.
10. Display the parking fee.
11. Free the parking slot.
12. Store or update the parking record.
13. **Stop**

The algorithm should use appropriate **IF/ELSE conditions**, especially when checking parking-slot availability. fileciteturn0file0L30-L48

---

## 3. Flowchart

The flowchart represents the complete vehicle entry and exit process.

### Standard Flowchart Symbols

| Symbol | Meaning |
|---|---|
| Oval | Start / End |
| Rectangle | Process |
| Parallelogram | Input / Output |
| Diamond | Decision |
| Arrows | Flow direction |

### Process Flow

**Start → Enter Vehicle Details → Check Parking Slot Availability → Is Slot Available?**

- **If No:** Display **"Parking Full"** → End
- **If Yes:** Assign Parking Slot → Record Entry Time → Vehicle Exit Request → Find Vehicle Record → Record Exit Time → Calculate Parking Duration → Calculate Parking Fee → Display Fee → Free Parking Slot → Update Parking Record → End

This follows the flowchart requirements given in the problem statement. fileciteturn0file0L49-L69

---

## 4. ER Diagram

The system contains the following main entities:

### VEHICLE

- **Vehicle_ID** — Primary Key
- Vehicle_Number
- Vehicle_Type
- Owner_Name
- Owner_Contact

### PARKING_SLOT

- **Slot_ID** — Primary Key
- Slot_Number
- Slot_Type
- Slot_Status

### PARKING_RECORD

- **Record_ID** — Primary Key
- Vehicle_ID — Foreign Key
- Slot_ID — Foreign Key
- Entry_Time
- Exit_Time
- Parking_Duration
- Parking_Fee

### Relationships

- One **VEHICLE** can have many **PARKING_RECORDS**.
- One **PARKING_SLOT** can be used in many **PARKING_RECORDS** over time.
- Each **PARKING_RECORD** is associated with one **VEHICLE** and one **PARKING_SLOT**. fileciteturn0file0L70-L98

---

## Project Output

The final project documentation consists of:

1. **Requirements**
2. **Algorithm**
3. **Flowchart**
4. **ER Diagram**

These are the four sections specified in the provided problem statement. fileciteturn0file0L99-L104

---

## Conclusion

The Parking – Vehicle Entry and Exit Management System provides a structured approach to handling vehicle parking operations. It manages vehicle information, parking-slot allocation, entry and exit times, parking duration, parking fees, and parking records in an organized manner.
"""

out = "/mnt/data/README.md"
pypandoc.convert_text(md, "md", format="md", outputfile=out, extra_args=["--standalone"])
print(f"Created: {out}")

