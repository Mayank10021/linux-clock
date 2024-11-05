# Digital Clock using Fedora

## Overview
This Bash script displays a **simple digital clock** in the terminal, refreshing every second to show the current time. The time is displayed in a colored format for better visibility.

## Prerequisites
Ensure that you are running **Fedora Linux** or any Linux distribution with `bash` and `date` command support.

## How It Works
- The script runs an infinite loop to continuously display the current time.
- The `date` command is used to fetch the current time in `HH:MM:SS` format.
- The `clear` command refreshes the terminal before each update.
- The time is shown in green text for better visibility.

## Usage
1. **Download or Create the Script**:
    Create a new file called `digital_clock.sh` and paste the following code:

    ```bash
    #!/bin/bash

    Red='\e[1;31m'
    green='\e[1;32m'
    blue='\e[1;34m'

    while true; do
        clear
        echo -e "$green$(date +%T)"
        sleep 1s
    done
    ```

2. **Make the Script Executable**:
    Run the following command to make the script executable:

    ```bash
    chmod +x digital_clock.sh
    ```

3. **Run the Script**:
    Execute the script using:

    ```bash
    ./digital_clock.sh
    ```

## Customization
- **Color Change**: Modify the `green` variable to use `Red` or `blue` for different display colors.
- **Format Change**: Modify `date +%T` to include the date with `date "+%Y-%m-%d %T"` if desired.

## Troubleshooting
- Ensure that the script has execution permissions.
- If colors do not display correctly, check terminal compatibility for ANSI color codes.

