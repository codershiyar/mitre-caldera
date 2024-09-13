# CALDERA Installation Guide by Coder Shiyar

## What is CALDERA?

CALDERA is an automated adversary emulation system designed to test and improve network defenses. It is developed by MITRE and leverages the MITRE ATT&CK framework to simulate different attack techniques. CALDERA enables red teams to conduct advanced offensive operations, while blue teams can use it to test their defenses in realistic scenarios.

## System Requirements

- Ubuntu 20.04 or later
- Python 3
- Git
- GCC
- UPX (optional)
- Go 1.20.3 or later

This guide will show you how to install CALDERA on Ubuntu using command line.

## Step 1: System Update

Start by updating your system to ensure you have the latest packages installed. Open a terminal (`Ctrl + Alt + T`) and run the following commands:

```bash
sudo apt update -y
sudo apt upgrade -y
```
##  Step 2: Install Required Dependencies
Next, install Python3, Git, and other necessary tools:

```bash
sudo apt install -y python3 python3-pip git gcc python3-dev upx-ucl
```
## Step 3: Install Go
Download and install Go (version 1.20.3 is used in this example):
```bash
wget https://go.dev/dl/go1.20.3.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.20.3.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
source ~/.profile
```
##  Step 4: Install CALDERA
Clone the CALDERA repository and install the required Python packages:
```bash
https://github.com/codershiyar/mitre-caldera 
cd mitre-caldera
pip3 install -r requirements.txt
``` 
<!-- in case my version did not worked use this: git clone https://github.com/mitre/caldera.git --recursive --branch 4.1.0 -->

If you encounter an error related to myst-parser, install it manually:

```bash
sudo pip3 install myst-parser
``` 

##  Step 5: Running CALDERA
Once everything is installed, you can start CALDERA using the following command:

```bash
python3 server.py --insecure
``` 

If the installation is successful, you should see the message All systems ready. You can now access the CALDERA web app by visiting the following URL in your browser:

- localhost:8888
- 127.0.0.1:8888
- 0.0.0.0:8888

## Step 6: Default Credentials
Use the following default login credentials to access the CALDERA interface:

### Red Team

- Username: red
- Password: admin

### Blue Team
- Username: blue
- Password: admin

### Admin
- Username: admin
- Password: admin


## Additional Notes
- Ensure you have a working internet connection while installing dependencies.

- You can explore different plugins and features in CALDERA to run advanced attack scenarios or defensive simulations.
For more information, please refer to MITRE CALDERA documentation: https://caldera.readthedocs.io.

### Thank you for following this guide! If you encounter any issues or have suggestions, feel free to reach out.

This `README.md` file provides a clear step-by-step guide on installing CALDERA, explains what it is, and includes additional instructions on running and accessing the web interface. Let me know if you need further customization or details!
