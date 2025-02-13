# Weather Fetcher Script

This repository contains a simple Windows batch script that retrieves weather information for Gorakhpur using the `curl` command and displays it in the command prompt.

![image](https://github.com/user-attachments/assets/3472308b-021f-460a-b49b-adc40487cc33)


## Prerequisites

- Windows operating system
- `curl` installed (available by default in Windows 10 and later)
- Internet connection

## Usage

1. Clone or download the repository.
2. Save the following script as `weather.bat`:

   ```bat
   @echo off
   curl wttr.in/Gorakhpur
   pause
   ```

3. Double-click `weather.bat` to execute the script, or run it from the command prompt:

   ```cmd
   weather.bat
   ```

## Troubleshooting

If the script does not work, try the following:

- Run `cmd` and manually execute `curl wttr.in/Gorakhpur` to check if `curl` is working.
- Ensure the batch file is correctly saved as `weather.bat` (not `weather.bat.txt`).
- Run the script as an administrator.
- If the window closes too quickly, modify the script to include `pause` at the end.
- If `curl` is not recognized, use PowerShell instead:

   ```bat
   @echo off
   powershell -Command "& {Invoke-WebRequest -Uri 'http://wttr.in/Gorakhpur?format=3' -UseBasicParsing}"
   pause
   ```

## License

This project is licensed under the MIT License.

