# Hotel Management System

A role-based console application for managing hotel operations, built with C# and the .NET Framework 4.7.2.

The system provides separate workflows for managers and receptionists, with user authentication, staff management, room monitoring, resident records, and income tracking. Data is stored in local text files.

## Features

### Authentication
- Register manager or receptionist accounts
- Login using a username and password
- Role-based access to system operations

### Manager tools
- Add, edit, delete, and view workers
- View resident information
- Monitor room availability and occupancy
- Track recorded hotel income

### Receptionist tools
- Add, edit, and delete residents
- Assign rooms
- Calculate resident costs by room type and boarding plan

### Pricing

| Room type | Daily room cost |
|---|---:|
| Single | $100 |
| Double | $150 |
| Triple | $200 |

| Boarding plan | Daily boarding cost |
|---|---:|
| Full Board | $50 |
| Half Board | $30 |
| Bed and Breakfast | $20 |

**Total cost** = (room cost + boarding cost) × duration in days

## Tech stack

- C#
- .NET Framework 4.7.2
- Console application
- File-based persistence (`.txt` files)
- Visual Studio/MSBuild project format

## Getting started

### Prerequisites

- Windows
- Visual Studio 2017 or later
- .NET Framework 4.7.2 Developer Pack

### Run the application

1. Clone the repository:

   ```bash
   git clone https://github.com/faragelyan/Hotel-Management-System-.git
   ```

2. Open `H_M_S.csproj` in Visual Studio.

3. Build the solution with **Build > Build Solution**.

4. Run with **Debug > Start Without Debugging**.

> The application currently initializes and accesses data files in `C:\Users\MOHAMED\Desktop\DP_FILES`. Update the file paths in `Program.cs` if you use another environment.

## Default accounts

| Username | Password | Role |
|---|---|---|
| `admin` | `admin123` | Manager |
| `receptionist1` | `pass123` | Receptionist |
| `receptionist2` | `pass123` | Receptionist |
| `receptionist3` | `pass123` | Receptionist |

> Change default credentials before using this project beyond local demonstration or development.

## Data files

The application uses the following text files:

| File | Purpose |
|---|---|
| `users.txt` | Login credentials and roles |
| `workers.txt` | Employee records |
| `rooms.txt` | Room types and availability |
| `residents.txt` | Resident bookings and boarding plans |
| `income.txt` | Income records |

Running the application recreates the initial sample data at startup.

## Project structure

```text
Hotel-Management-System-/
├── App.config          # .NET runtime configuration
├── H_M_S.csproj        # Visual Studio project file
├── Program.cs          # Application logic and menu workflows
└── Properties/
    └── AssemblyInfo.cs # Assembly metadata
```

## Current limitations

- Uses hard-coded Windows file paths
- Stores credentials and records in plain-text CSV-style files
- Has no database or password encryption
- Reinitializes users and sample data every time it starts
- Uses a single-file console architecture
- Intended primarily as a learning or demonstration project

## Possible improvements

- Replace text-file storage with SQL Server or SQLite
- Move configuration and data paths to `App.config`
- Hash passwords and add secure authentication
- Improve input validation and error handling
- Add automated unit tests
- Split classes into separate source files
- Migrate to a modern .NET console project

## License

No license has been specified for this repository. Please contact the repository owner before using or distributing the project.

## Author

**Farag Elyan**

- GitHub: [@faragelyan](https://github.com/faragelyan)
