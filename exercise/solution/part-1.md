# Logging in

The following are producers for logging in to the COARCE HPC via the following OS: Windows, Mac, and Linux.

## Table of Contents

- [For Windows](#for-windows)
  - [PuTTY](#putty)
  - [Command Prompt (for Windows 10 only)](#command-prompt-for-windows-10-only)
- [For Mac / Linux](#for-mac--linux)

## For Windows

For Windows, users have two options to use in logging in: PuTTY or Command Prompt.

## PuTTY

1. Download and run **PuTTY** application.
   - [32-bit:](https://the.earth.li/~sgtatham/putty/latest/w32/putty.exe)
   - [64-bit:](https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe)
2. Set port number **22** and the **Host Name** to **saliksik.asti.dost.gov.ph**.
   ![PuTTY Configuration 1 ](images/putty_2.png)

3. On the left panel under Category, collapse the **Connection** option and select the **SSH** option, and then click **Auth**. Select **Browse** to attach your **private key** (.ppk file) for authentication. Then click **Open**.
   ![PuTTY Configuration 2](images/putty_3.png)

4. Select **Yes** when prompted by a PuTTY Security Alert Window.
   ![PuTTY Security Alert](images/putty_4.png)
5. When the terminal opens, enter your COARE credentials that should have been sent to your email.
6. You are now inside the HPC frontend if you see this (see image below) on your terminal.
   ![HPC frontend](images/putty_6.png)

   NOTES:

   - Accessing HPC must be passwordless unless you have a passphrase during the generating of keys.
   - If you want to use your key (generated using PuTTY) in OpenSSH, check this tutorial on [converting PuTTY (.ppk) key to SSH Key](https://www.simplified.guide/putty/convert-ppk-to-ssh-key)
   - You cannot use your OpenSSH keys to PuTTY and vice versa.

## Command Prompt (for Windows 10 only)

1. Open **Command Prompt** or **Windows PowerShell**.
2. Type command:

   ```
   ssh <username>@saliksik.asti.dost.gov.ph
   ```

   Useful options:

   | Flag               | Description                                                  |
   | ------------------ | ------------------------------------------------------------ |
   | -i \<private-keys> | Indicate the private key to be used                          |
   | -v                 | Increase verbosity                                           |
   | -vv, -vvv          | Enable additional verbosity for even more debugging messages |

3. Type **Yes** to add the host in your known hosts.

   ![CMD3](images/cmd_3.png)

4. You should now be inside the HPC frontend.

   ![CMD3](images/cmd_4.png)
   NOTES:

   - Logging in must be passwordless unless you have a passphrase during the generating of keys.
   - If you want to use your key (generated using PuTTY) in OpenSSH, check this tutorial on [converting PuTTY (.ppk) key to SSH Key](https://www.simplified.guide/putty/convert-ppk-to-ssh-key).
   - You cannot use your PuTTY keys to OpenSSH and vice versa.

## For Mac / Linux

1. Launch your Terminal application and type:

   ```
   ssh <username>@saliksik.asti.dost.gov.ph
   ```

   Useful options:
   |Flag |Description |
   | -------- | -------- |
   | -i \<private-keys> | Indicate the private key to be used |
   | -v | Increase verbosity |
   | -v, -vvv | Enable additional versobisity for even more debugging messages

2. Type **Yes** to add the host in your known hosts.

   ![mac](images/mac-linux_2.png)

3. You are now inside the HPC Frontend

   ![mac1](images/mac-linux_3.png)

   NOTE: Logging in must be passwordless unless you have a passphrase during generating of keys.
