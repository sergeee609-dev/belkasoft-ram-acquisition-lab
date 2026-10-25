# Windows RAM Acquisition Using Belkasoft RAM Capturer

## Project Overview
This project documents a hands-on digital forensics lab involving the acquisition of volatile memory (RAM) from a Windows system using Belkasoft Live RAM Capturer. Following acquisition, I calculated a SHA-256 hash of the resulting memory image using Windows PowerShell.

The lab demonstrates memory acquisition, forensic evidence preparation, and initial integrity documentation.

## Tools and Technologies
- Belkasoft Live RAM Capturer
- Windows
- Windows PowerShell
- Get-FileHash cmdlet
- SHA-256 hashing

## Lab Workflow

### 1. Tool Preparation
Downloaded the instructor-provided Belkasoft RAM Capturer archive, extracted its contents into an evidence directory, and prepared the executable to run with administrator privileges.

### 2. Memory Acquisition
Used Belkasoft Live RAM Capturer to acquire the system's volatile memory. The application displayed a completed memory dump, reporting approximately 35,328 MB of memory captured.

### 3. Memory Image Documentation
Saved the acquired memory image as a `.mem` file in the designated evidence directory. The resulting image served as the input for SHA-256 hashing.

### 4. SHA-256 Hash Calculation
Used PowerShell's `Get-FileHash` cmdlet with the SHA-256 algorithm to calculate a cryptographic hash of the acquired memory image.

```powershell
Get-FileHash "C:\Evidence\RamCapturer\x64\20261022.mem" -Algorithm SHA256
```

### 5. Evidence Integrity Considerations
Recorded a SHA-256 hash for the acquired memory image. This provides a reference value for future integrity comparisons. The lab does not document a subsequent comparison against an independently recorded hash.

## Skills Demonstrated
- Acquiring volatile memory from a Windows system
- Using Belkasoft Live RAM Capturer
- Preparing and organizing forensic evidence files
- Using PowerShell for file hashing
- Understanding the purpose of SHA-256 in evidence integrity documentation
- Recording technical procedures with screenshots

## Project Documentation
[View the Belkasoft RAM Acquisition Portfolio (PDF)](Belkasoft_RAM_Acquisition_Portfolio_Polished.pdf)

## Project Scope
This educational lab documents a completed RAM acquisition and SHA-256 hash calculation. It does not include analysis of the memory image with tools such as Volatility or independent verification of the hash against a trusted reference. The memory dump itself is not included because RAM images may contain sensitive data.
