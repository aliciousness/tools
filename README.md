Here’s the full markdown-formatted README you can now copy:

# Script: Setup Python Virtual Environment and Install Dependencies

This Bash script automates the setup of a Python virtual environment, installation of dependencies, and updating the `requirements.txt` file. Additionally, it provides an option to install the dependencies globally and configure the script for global access.

## Functionality

1. **Navigate to Script Directory**: Automatically moves to the directory where the script is located.
2. **Remove Old Virtual Environment**: Deletes any existing Python virtual environment (`venv/`) to ensure a fresh setup.
3. **Create a New Virtual Environment**: Initializes a new virtual environment in the current directory.
4. **Activate Virtual Environment**: Activates the newly created environment.
5. **Install Dependencies**: Installs required Python packages specified in `requirements.txt`.
6. **Update `requirements.txt`**: After installation, the `requirements.txt` is updated with the latest installed packages.

## Option 1: Install with Virtual Environment (Recommended)

### Steps:

1. Clone the repository or download the script.
2. Ensure you have Python 3 installed on your system.
3. Run the script:

   ```bash
   ./pip-env.sh
   ```

This will create a virtual environment, install the dependencies, and activate the environment.

## Option 2: Install Requirements Globally

If you prefer to install the dependencies globally and make the script available system-wide, follow these steps:

### Steps:

1. **Install Dependencies Globally**:

   Instead of using a virtual environment, you can install the dependencies globally by running:

   ```bash
   pip install -r requirements.txt
   ```

2. **Add Script to Global PATH**:

   Add the `bin` directory of this repository to your system's `PATH` to run the script globally from anywhere.

   - Edit your shell configuration file (e.g., `~/.bashrc`, `~/.zshrc`) and add the following line:

     ```bash
     export PATH="/path/to/your/repo/bin:$PATH"
     ```

     Replace `/path/to/your/repo/bin` with the full path to the `bin` directory in your repository.

3. **Reload your shell**:

   After updating the `PATH`, run:

   ```bash
   source ~/.bashrc   # for Bash users
   source ~/.zshrc    # for Zsh users
   ```

Now you can run the script globally by simply typing the script name from any location in your terminal.

## Prerequisites

- **Python 3**: Ensure that Python 3 is installed.
- **boto3**: Add `boto3` to your `requirements.txt` if not already present.

## Notes

- This script assumes that `requirements.txt` is in the same directory as the script.
- For the virtual environment option, the script regenerates the environment each time it is run, deleting the old one.
- For the global installation option, make sure you have the necessary permissions to install global Python packages.

Now you should be able to copy it easily from here!