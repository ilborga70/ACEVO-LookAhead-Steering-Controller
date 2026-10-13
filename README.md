# ACEVO-LookAhead-Steering-Controller
LookAhead Steering Controller is a lightweight, standalone suite that converts your steering wheel rotation into toward the inside of a corner, without needing to install or run OpenTrack.

🇬🇧 What's New in Version 0.9.0.0
- Dynamic Apex Roll Tilt: Added natural camera roll/tilt toward the corner apex when steering.
- UI Controls: Added an ON/OFF toggle for the roll tilt along with an intensity percentage adjustment slider/spinbox.
- Complete UDP Telemetry: Real-time display of both Yaw and Roll values sent to OpenTrack at 60Hz.
- JSON Configuration Save: Integrated automatic saving and loading for the Roll Tilt settings in the JSON configuration file.

<img width="1357" height="1386" alt="ACEVO LookAhead Steering Controller v0 9 0 0" src="https://github.com/user-attachments/assets/c19829b3-1904-4deb-af73-ea27cf1e47c3" />

🚀 Quick Installation (First Time Only)
1. Download the mod's .zip archive.
2. Extract ALL the contents of the ZIP directly into the game's root folder:
`...\SteamLibrary\steamapps\common\Assetto Corsa EVO\`
Note: The manual build will add the mod (`LookAhead Steering Controller.exe` and `dinput8.dll` and `AssettoCorsaEvoHeadTracking.asi`).

🛠️ Step-by-Step Setup Guide Without Mod (`LookAhead Steering Controller.exe` and `dinput8.dll` and `AssettoCorsaEvoHeadTracking.asi`)

0. **Download OpenTrack:**  
   Download and install OpenTrack from the official release page:  
   👉 [OpenTrack Releases](https://github.com/opentrack/opentrack)

1. **Configure OpenTrack (Universal Output Matrix):**
   * Open OpenTrack and set **Input** to *UDP over network* (Port `4242`).
   * Set **Output** to *freetrack 2.0 Enhanced*.
   * Go to **Options → Output** and configure the matrix as follows:
     * **Yaw:** Source ➡️ `Yaw`
     * **Pitch:** Source ➡️ `Roll`
     * **Roll:** Source ➡️ `Roll` + Enable **Post-Invert**
   * Click **Start**.

2. **Configure LookAhead Steering Controller:**
   * Extract the ZIP package and run `LookAhead Steering Controller.exe` as Administrator.
   * Set **Wheel Degrees (Lock-to-Lock)** to `1800°` inside the utility to establish a maximum linear baseline.
   * Adjust your physical steering lock degrees exclusively within your wheelbase driver software (e.g., Fanatec Fanalab, Simucube True Drive, Thrustmaster Control Panel).
   * Check the built-in diagnostic panel (**System Process Status**) to verify real-time connections for your wheel, OpenTrack, and the simulator.

🛠️ Technical Features
Direct UDP Protocol: Sends data directly to the game engine (zero latency).
No external programs: OpenTrack is not necessary.
Natural Movement Filter: Stabilizes the signal and avoids jerkiness during sudden steering inputs.

🎮 Windows Security & SimRacing: Why exclude the LookAhead Steering Controller? 🏎️💨
Have you noticed this file in the Windows Defender exclusions?
Let’s break down why adding lookahead steering controller.exe is essential for your setup! 👇

🛡️ 1. Preventing False Positives (Unjustified Blocks).
This program is a third-party utility designed to calculate wheel movements and camera angles for racing simulators.
Because it reads hardware data and shares it directly with other software (like OpenTrack), Windows Defender might mistake this behavior for malicious activity (like a keylogger).
Adding it to your exclusions stops Windows from blocking or deleting it by mistake!

⚡ 2. Eliminating Micro-Stuttering & Input Lag.
Windows Antivirus scans files in real-time.
As shown in the software window, this controller transmits data at a very high frequency (60Hz — 60 times per second).
If the antivirus analyzed every single data packet while you were driving, it would cause:

📈 Abnormal CPU spikes
⏱️ Delayed inputs (input lag)
🛑 Micro-stuttering during your races

📂 3. Why the Entire D:\ Drive is Excluded.
You can also see that the whole D:\ folder is listed.
Sim-racers often do this to prevent Microsoft Defender from constantly scanning heavy game files installed on a secondary HDD or SSD.
This significantly improves overall loading times and game fluidity!

🔬 Is this file 100% safe?
Yes! If you are worried about security, the file has been fully analyzed on Jotti's malware scan.
The results show 0/13 scanners reporting malware, meaning top antiviruses like Kaspersky, BitDefender, and Avast found absolutely nothing.

🔗 Check the full safety report here: https://virusscan.jotti.org/it-IT/filescanjob/g84ynyzizw

📜 Credits & Licenses
LookAhead Steering Controller by `ilborga70`
