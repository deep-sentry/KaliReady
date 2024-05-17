# KaliReady
KaliReady is a comprehensive automation tool designed to simplify the process of setting up, configuring, and securing a fresh Kali Linux installation. Whether you're a security professional, a penetration tester, or a cybersecurity enthusiast, KaliReady helps you get your Kali Linux environment up and running quickly and securely.

<p align="center">
  <img width="460" height="460" src="https://github.com/deep-sentry/KaliReady/assets/7604466/992aac87-f0e9-4021-91e1-5abea3f3a011">
</p>

## Features

- **Automated Installation**: Install additional applications and tools with a single command.
- **System Configuration**: Configure system settings for optimal performance and usability.
- **Security Enhancements**: Apply security measures to harden your Kali Linux installation against threats.
- **Customizable Scripts**: Tailor the setup process to your specific needs with customizable scripts.

## Instructions

Clone the repository:

```bash
git clone https://github.com/deep-sentry/KaliReady.git
```

Execute the playbook:
```bash
ansible-playbook kaliready.yml --ask-become-pass
```

## Explanation
- The playbook begins by updating the package list and upgrading installed packages.
- It then installs necessary dependencies and **flameshot** using apt.
- **gitrob** is installed using RubyGems.
-  The **Sublist3r** and **SecLists** repositories are cloned from GitHub, and Sublist3r dependencies are installed via pip.
-  Symbolic links are created to make Sublist3r easily accessible from the command line.
-  Finally, the playbook verifies the installations by checking the versions of gitrob, sublist3r, and flameshot and outputs the versions using Ansible's debug module.

## Customization
KaliReady includes customizable scripts that allow you to tailor the setup process to your specific needs. Edit the configuration files in the config directory to add or remove applications, change system settings, or modify security measures.

## Contributing
We welcome contributions to KaliReady! If you have suggestions for new features, improvements, or bug fixes, please open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
