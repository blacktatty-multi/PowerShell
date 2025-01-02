# PowerShell

PowerShell is a scripting language developed by Microsoft for automating Windows tasks.

## Installation

### Windows

1. Download the latest stable release from the [PowerShell GitHub releases page](https://github.com/PowerShell/PowerShell/releases).
2. Run the downloaded `.msi` installer and follow the installation prompts.

### macOS

1. Open a terminal.
2. Run the following command to install via Homebrew:
    ```sh
    brew install --cask powershell
    ```

### Linux

#### Ubuntu

1. Open a terminal.
2. Run the following commands:
    ```sh
    sudo apt-get update
    sudo apt-get install -y wget apt-transport-https software-properties-common
    wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-bionic-prod bionic main"
    sudo apt-get update
    sudo apt-get install -y powershell
    ```

#### CentOS

1. Open a terminal.
2. Run the following commands:
    ```sh
    sudo yum install -y wget
    sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    wget https://packages.microsoft.com/config/rhel/7/prod.repo
    sudo mv prod.repo /etc/yum.repos.d/microsoft.repo
    sudo yum install -y powershell
    ```

### Verify Installation

1. Open a terminal or PowerShell prompt.
2. Run the following command to verify the installation:
    ```sh
    pwsh --version
    ```

## Security Verification

To ensure the integrity and security of the downloaded files, you can verify the checksums:

1. Download the checksum file from the [PowerShell GitHub releases page](https://github.com/PowerShell/PowerShell/releases).
2. Use the following command to verify the checksum (replace `<checksum-file>` and `<downloaded-file>` with the appropriate file names):
    ```sh
    shasum -a 256 -c <checksum-file>
    ```

This will verify that the downloaded file matches the checksum provided by the PowerShell team.

---

Save and commit the changes to your repository. If you need further assistance, please let me know.
