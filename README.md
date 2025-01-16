

### README:

```markdown
# Wi-Fi Password Viewer

This Python script allows you to view the saved Wi-Fi passwords on your Windows machine. The script retrieves the list of all Wi-Fi profiles stored in your system and attempts to extract the corresponding passwords. This can be useful if you've forgotten the password to a Wi-Fi network you've previously connected to.

## Features:
- Lists saved Wi-Fi profiles on your Windows machine.
- Displays the Wi-Fi profile name and the corresponding password.
- Simple and easy-to-use interface.

## Requirements:
- **Python 3.x**
- Windows OS (as it uses `netsh` to interact with the system)

Ensure you have Python installed. You can download it from [python.org](https://www.python.org/).

## Usage

### Running the Script

To run the script, follow these steps:

1. Clone the repository or download the script.
2. Open a terminal or command prompt.
3. Navigate to the directory containing the script.
4. Run the following command:

   python3 wifi_password_viewer.py
   ```

### Example Output

```bash
..:: Wi-Fi Passwords: 

Wi-Fi Profile                        |  Password
------------------------------------------------------------
HomeNetwork                          |  mypassword123
WorkNetwork                          |  workpassword456
GuestNetwork                         |  (No Password)
```

If a password is found, it will be displayed next to the corresponding Wi-Fi profile. If no password is set, the script will display "No Password."

## Code Explanation

### Main Script

- **Wi-Fi Profiles List**: The script first retrieves the list of saved Wi-Fi profiles on your machine using the `netsh wlan show profiles` command.
- **Password Retrieval**: For each profile, the script extracts the password by using the `netsh wlan show profile <profile_name> key=clear` command.
- **Output Display**: The script outputs the profile names and passwords in a simple, aligned table format.

### Error Handling

- **No Password**: If a profile does not have a password or the password is not retrievable, it will show "(No Password)".
- **Encoding Issues**: If there is an error retrieving the password for a profile, the script will print an encoding error message.

## Contributing

Contributions are welcome! If you have suggestions for new features or improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. This license permits anyone to use, modify, and distribute the software with minimal restrictions, ensuring flexibility for open-source development. See the [LICENSE](LICENSE) file for details.

---

**Note**: This script is intended for educational purposes only. Please use it responsibly.
```

---
