# aaPanel Installation Guide for Ubuntu Server 22.04

![aaPanel](https://www.aapanel.com/images/logo.png)

![GitHub](https://img.shields.io/github/license/your-repo/your-project)
![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04-orange)
![aaPanel](https://img.shields.io/badge/aaPanel-Latest-brightgreen)

## Introduction
This guide provides step-by-step instructions to install **aaPanel**, a lightweight and user-friendly web hosting control panel, on Ubuntu Server 22.04.

## Prerequisites
Ensure your server meets the following requirements:
- Ubuntu Server 22.04 (fresh installation recommended)
- Root or sudo access
- A stable internet connection

## Installation Steps

### 1. Update & Upgrade System
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Required Packages
```bash
sudo apt install curl wget -y
```

### 3. Download and Install aaPanel
```bash
wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && sudo bash install.sh
```

### 4. Confirm Installation
During installation, confirm by typing `y` and pressing `Enter` when prompted.

### 5. Retrieve Login Credentials
Once installation is complete, you will see output similar to:
```
Congratulations! Installed successfully!
==================================================================
aaPanel Internet Address: http://your-server-ip:8888/8xxxxxxx
aaPanel Internal Address: http://your-server-ip:8888/8xxxxxxx
username: xxxxxx
password: xxxxxx
==================================================================
```
Save these credentials for logging in.

### 6. Access aaPanel
Open your web browser and go to:
```
http://your-server-ip:8888/8xxxxxxx
```
Replace `your-server-ip` with your actual server IP address.

### 7. Change Default Login Port (Optional)
For security reasons, change the default `8888` port:
```bash
bt 14
```
Enter a new port (e.g., `2087`), then access aaPanel with:
```
http://your-server-ip:2087/
```

### 8. Install Essential Software
Upon first login, aaPanel will prompt you to install:
- **LNMP (Nginx, MySQL, PHP)** or
- **LAMP (Apache, MySQL, PHP)**

Choose based on your requirements and wait for installation to complete.

## Uninstallation
If you need to remove aaPanel, use the following command:
```bash
wget http://www.aapanel.com/script/clean.sh && bash clean.sh
```

## How to Use This README on GitHub
To create a `README.md` file in your GitHub repository:

1. Go to your repository on GitHub.
2. Click on **Add file** > **Create new file**.
3. Name the file `README.md`.
4. Copy and paste the content of this guide into the file.
5. Click **Commit changes**.

## Conclusion
You have successfully installed aaPanel on Ubuntu Server 22.04. Enjoy managing your web hosting environment efficiently!

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

