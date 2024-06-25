This is a fork, updated for my personal use. I cannot recommend it, but I do use it on my iPad 5th Gen and Windows.

## Requirements:

- Windows
- iTunes and iCloud (not from the Microsoft Store), [see here for links](https://faq.altstore.io/getting-started/how-to-install-altstore-windows).
- Python [latest](https://www.python.org/downloads/) version.

## Environment

1. **Launch PowerShell as an Administrator.**
2. Navigate with `cd ~\Desktop`.
3. Clone the repository: `git clone https://github.com/RobThePCGuy/SideJITServer.git`.
4. Change directory with `cd SideJITServer`.
5. Create and activate a virtual environment with Python:

   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

   You should now see `(venv) PS` indicating that the virtual environment is activated.

6. Install required packages:

   ```powershell
   pip install -r requirements.txt
   pip install SideJITServer
   pip install pymobiledevice3==4.10.11
   ```

7. Check the version of the server with `SideJITServer --version`.

   **Expected output:** `pymobiledevice3: 4.10.11` and `SideJITServer: 1.3.1`.

## Pairing

1. Connect your iPad to the PC and run `SideJITServer --pair`, then type in `y` at the prompt.
   - You may have to hit the 'Trust' button on the Apple device a couple times during this step.
   - You will be given three different IP addresses if the server starts successfully.
2. Open the default web browser on your Apple device and type that IP into the address bar, i.e., `http://192.168.1.164:8080/`.
   - Acknowledge any popups on this page.
3. Copy or write down your UUID, which is the 24 characters at the end, including the hyphen.

   ```json
   {"usbmux-########-################-USB":"########-################"}
   ```

## Follow Through

1. On your Apple device, go to my repo: https://github.com/RobThePCGuy/SideJITServer
2. Click [here](https://www.icloud.com/shortcuts/b0ffc9c3f0e74e7a8f8052c89fa322cf) to install the Shortcut.
3. Select `Set Up Shortcut`
4. You will be asked for your device UUID, the 24 characters noted previously, similar to: `00001111-000A1100A11101A`.
5. Next, you will need to enter the IP address for the SideJITServer.
   - This is the same IP we used in the browser to get the UUID, i.e., `http://192.168.1.164:8080/`.
     - You MUST enter the `http://` at the beginning as well as the `/` at the very end.
6. Save it or press Done.
7. Search for the new Shortcut via the name 'SideJIT'.
8. Press the play button to run the Shortcut, or just say, `"Hey Siri, SideJIT"`.
9. Either way, you will need to pick an application. If none appear, then you do not have any installed that support JIT.
