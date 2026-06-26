# JAPTECH Fleet Management System

A Windows Forms desktop application for managing a vehicle fleet — built as a university group project by a team of five. The system supports multiple user roles, vehicle and trip administration, booking management, timesheets, job sheets, and emergency logging.

> **Team project** — developed collaboratively with 4 teammates. Primary contributions: backend C# class design and XML/resource file configuration.

---

## Overview

The application is designed for an organisation that needs to manage a fleet of vehicles across different operational roles. Depending on their role, users see a tailored view of the system:

- **Vehicle Admin** — manage vehicles and their availability
- **Trip Manager** — plan and oversee trips
- **Office Manager** — handle bookings, delegations, and records
- **Service Manager** — manage maintenance and job sheets
- **Timesheet Manager** — log and view driver timesheets
- **Employees / Customers** — register and make bookings

---

## Tech Stack

| Layer | Technology |
|---|---|
| Application Type | Windows Forms Desktop App |
| Framework | .NET Framework 4.7.2 |
| Language | C# |
| UI | Windows Forms (`System.Windows.Forms`) |
| Data | `System.Data` + `System.Xml` |
| Directory Services | `System.DirectoryServices` |
| IDE | Visual Studio |
| Solution | `JAPTECH FLEET MANAGEMENT SYSTEM.sln` |

---

## Application Windows & User Controls

The `.csproj` distinguishes between full **Forms** (standalone windows) and **UserControls** (embedded panels within a form).

### Forms (Windows)

| Form | Purpose |
|---|---|
| `login` | User authentication and role-based routing |
| `HomePage` | Main dashboard after login |
| `EmpRegistration` | Employee registration |
| `VehicleAdmin` | Vehicle management and availability |
| `TripManager` | Trip planning and oversight |
| `OfficeManager` | Central office operations hub |
| `ServiceManager_FirstScreen` | Maintenance and service entry point |
| `TimesheetManager` | Timesheet creation and management |
| `JobSheet_Window` | Job sheet logging for vehicle maintenance |
| `Bookings` | Create new bookings |
| `ViewBookings` | View existing bookings |
| `UpdateBooking` | Edit or update a booking |

### User Controls (Embedded Panels)

| Control | Purpose |
|---|---|
| `custRegcs` | Customer registration panel |
| `Delegations` | Trip delegation management |
| `Emergencies` | Emergency incident logging |
| `Recordings` | Vehicle usage recordings |
| `Records` | General records view |
| `TripBookings` | Trip-specific booking panel |
| `UpdateTimesheet` | Edit timesheet entries |
| `ViewTimesheet` | View timesheet records |

---

## Project Structure

```
JAPTECH-FLEET-MANAGEMENT-SYSTEM/
├── Program.cs                          # Entry point — launches login form
├── login.cs / .Designer.cs             # Login form
├── HomePage.cs / .Designer.cs          # Main dashboard
├── VehicleAdmin.cs / .Designer.cs      # Vehicle management
├── TripManager.cs / .Designer.cs       # Trip management
├── OfficeManager.cs / .Designer.cs     # Office operations
├── ServiceManager_FirstScreen.cs       # Service/maintenance entry
├── TimesheetManager.cs                 # Timesheet form
├── JobSheet_Window.cs                  # Job sheet form
├── Bookings.cs / ViewBookings.cs       # Booking forms
├── UpdateBooking.cs                    # Edit booking form
├── EmpRegistration.cs                  # Employee registration form
├── custRegcs.cs                        # Customer registration control
├── Delegations.cs                      # Delegation control
├── Emergencies.cs                      # Emergency logging control
├── Recordings.cs / Records.cs          # Recording/record controls
├── TripBookings.cs                     # Trip booking control
├── ViewTimesheet.cs / UpdateTimesheet.cs # Timesheet controls
├── Properties/                         # Assembly info, resources, settings
├── App.config                          # Application config
└── JAPTECH FLEET MANAGEMENT SYSTEM.sln
```

---

## Prerequisites

- Visual Studio 2019 or later
- .NET Framework 4.7.2
- A database backend (SQL Server recommended — connection configured via `App.config`)

---

## Running the Application

1. Clone the repository:
   ```bash
   git clone https://github.com/thorstore-ong/Fleet-management-system.git
   ```

2. Open `JAPTECH FLEET MANAGEMENT SYSTEM.sln` in Visual Studio.

3. Update `App.config` with your database connection string if the application uses a local SQL Server instance.

4. Press `Ctrl + B` to build the solution.

5. Press `F5` or click **Start** to run. The application will open at the `login` form.

---

## My Contributions

This was a team project (5 members). Personal contributions included:

- Designing and implementing backend C# classes for the core domain objects
- Configuring XML/resource (`.resx`) files used across the Windows Forms components
- Contributing to the overall backend logic shared across the forms

---

## Context

Built as a university group project to practise object-oriented design, Windows Forms development, and multi-person collaboration on a shared C# codebase.
