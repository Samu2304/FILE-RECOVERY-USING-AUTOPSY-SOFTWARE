# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:

![WhatsApp Image 2025-08-28 at 14 07 47_496fa16c](https://github.com/user-attachments/assets/501b5130-419e-450c-806a-468e0d0a998f)

![WhatsApp Image 2025-08-28 at 14 08 42_e1a02c27](https://github.com/user-attachments/assets/7fa89bcc-5a7b-479a-aefb-e5e55d71fee5)

![WhatsApp Image 2025-08-28 at 14 10 25_19da80dd](https://github.com/user-attachments/assets/f63582b7-5595-4785-8b91-8059a19f4366)

![WhatsApp Image 2025-08-28 at 14 51 27_63c3bb27](https://github.com/user-attachments/assets/4a8ad5dd-c921-4419-987f-666a1db1475c)

![WhatsApp Image 2025-08-28 at 14 51 40_ece408d5](https://github.com/user-attachments/assets/5a9aa326-6d42-4713-81ad-b0fc28df221e)


## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
