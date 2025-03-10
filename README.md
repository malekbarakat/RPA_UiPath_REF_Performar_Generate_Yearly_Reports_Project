# RPA UiPath REF Performer - Generate Yearly Reports

## Project Overview
The **RPA_UiPath_REF_Performer_Generate_Yearly_Reports_Project** is an automation process developed by **[Your Name]** using **UiPath**. This performer process retrieves transaction items from **UiPath Orchestrator Queue**, processes them, and generates **Yearly Reports** based on the extracted data.

## Purpose
This performer process is responsible for:
- Fetching transaction items from **Orchestrator Queue**.
- Logging into the required application or web portal.
- Extracting, processing, and generating **Yearly Reports**.
- Downloading and saving reports to a specified location.
- Logging status updates and handling errors.

## Project Structure
This project follows the **UiPath Robotic Enterprise Framework (REF)** to ensure scalability, error handling, and modular automation.

### 1. **Init State (Initialization)**
- Loads configuration settings from **Config.xlsx**.
- Initializes required applications and system settings.
- Retrieves credentials from **UiPath Orchestrator Assets**.

### 2. **Get Transaction Data**
- Retrieves the next available transaction item from the **Orchestrator Queue**.
- If a transaction is found, moves to the processing stage.
- If no transactions are available, the process ends.

### 3. **Process Transaction**
- Logs into the target application (e.g., an internal system or web portal).
- Extracts relevant data required for generating reports.
- Processes and generates **Yearly Reports** based on transaction details.
- Downloads and saves reports in a designated folder.
- Updates the transaction status in **Orchestrator** (Success/Failure).

### 4. **End Process**
- Cleans up resources and logs the final execution status.
- Ensures all open applications are closed properly.

## Dependencies
- **UiPath Studio** (Compatible with version 2021.10 or later)
- **UiPath Orchestrator** (For queue transaction management)
- **UiPath REFramework**
- **Microsoft Excel** (For configuration settings)
- **Target Application/Web Portal** (Where reports are generated)

## Configuration
This process is configured using a **Config.xlsx** file, containing:
- **Orchestrator Queue Name**
- **Application URLs**
- **Report Storage Path**
- **Credentials** (Stored securely in Orchestrator Assets)
- **Logging and Retry Settings**

## Execution Steps
1. **Open the Project** in UiPath Studio.
2. **Update the Config.xlsx** file with necessary details.
3. **Publish the Performer Process** to UiPath Orchestrator.
4. **Schedule or Manually Run** the performer in **Orchestrator**.
5. **Monitor execution logs** in UiPath Orchestrator.

## Logging & Error Handling
- **Exception Handling:** Implements `try-catch` blocks for robustness.
- **Logging:** Uses UiPath’s built-in logging to track each execution step.
- **Retries:** Configured to retry transactions upon failure based on **Config.xlsx** settings.

## Future Enhancements
- Implement email notifications for report generation completion.
- Support additional report formats (e.g., PDF, CSV).
- Optimize report generation speed.

## Author
Developed by **[Malek AL Barakat]**, following UiPath best practices for automation.
