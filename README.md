# Installing Microsoft SQL Server on Windows

## Prerequisites
- Windows 10/11 or Windows Server (2016 or later)
- At least 2 GB of free disk space
- Minimum 2 GB RAM (4 GB recommended)
- .NET Framework 4.6 or later

## Step-by-Step Installation Guide

### Step 1: Download Microsoft SQL Server
1. Visit the official Microsoft website: [Download SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
2. Choose the edition:
   - **SQL Server Express** (Free, lightweight)
   - **SQL Server Developer** (Free, full-featured for development)
   - **SQL Server Standard/Enterprise** (Paid versions for production)
3. Click the **Download** button and save the installer.

### Step 2: Run the SQL Server Installer
1. Locate the downloaded `.exe` file and double-click to run it.
2. Select **Basic Installation** or **Custom Installation**:
   - **Basic**: Installs with default configurations.
   - **Custom**: Allows you to choose features and installation directory.
3. Accept the license agreement and proceed.

### Step 3: Configure SQL Server
1. Choose the **SQL Server Edition** (Express, Developer, Standard, or Enterprise).
2. Select an installation directory (default: `C:\Program Files\Microsoft SQL Server`).
3. Click **Install** and wait for the installation to complete.

### Step 4: Configure SQL Server Authentication Mode
1. Choose **Mixed Mode** (SQL + Windows Authentication) or **Windows Authentication Mode**.
2. If using **Mixed Mode**, set a strong password for the `sa` (System Administrator) account.
3. Add the current user as an SQL Server administrator.

### Step 5: Install SQL Server Management Studio (SSMS) (Optional)
1. Download SSMS from: [Download SSMS](https://aka.ms/ssmsfullsetup)
2. Run the installer and follow the installation steps.
3. Once installed, launch SSMS and connect to your SQL Server instance.

### Step 6: Verify Installation
1. Open **SQL Server Configuration Manager**.
2. Ensure that the **SQL Server Service** is running.
3. Open SSMS and connect using:
   - Server Name: `localhost` or `127.0.0.1`
   - Authentication: Windows Authentication or SQL Authentication
4. Run the following query to test the connection:
   ```sql
   SELECT @@VERSION;
   ```

### Step 7: Enable Remote Connections (Optional)
1. Open **SQL Server Configuration Manager**.
2. Navigate to **SQL Server Network Configuration > Protocols for MSSQLSERVER**.
3. Enable **TCP/IP** and restart the SQL Server service.
4. Open **Windows Firewall** and allow inbound connections for **SQL Server TCP Port (1433)**.

### Step 8: Uninstalling SQL Server (If Needed)
1. Open **Control Panel > Programs & Features**.
2. Locate **Microsoft SQL Server** and click **Uninstall**.
3. Follow the prompts to remove the SQL Server instance.

## Conclusion
You have successfully installed Microsoft SQL Server on Windows. You can now create and manage databases using SQL Server Management Studio or command-line tools.

---


