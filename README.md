#2Pwn4Me

Currently not useable as I'm trying to recover this project...

Plays music on a remote PC (Active Directory and SMB required!)

---
#####This tool uses the followig programs:

PsExec (Microsoft)<br>
mpg123<br>
nircmd<br>
youtube-dl<br>
ffmpeg

---
#####How it Works:

We make an SMB connection to the remote computer
We copy a mp3, mpg123 (cmd line mp3 player) and nircmd to the remote computer
We make a remote shell connection to the remote computer using PsExec
We use the remote shell to turn the volume to max with NirCMD (Which we put on the remote computer in step 2)
We now use mpg123 to play the music
How to use:

Make sure there is a file called song.mp3 in the same folder as the run.bat file
Run run.bat
follow on screen instructions
Profit?

---
#####How to stop?

Currently the tool does not allow to do this remotly, you can however connect to the remote computer yourself with "PsExec \\remotecomputername cmd", wait for it to start and when your on the remote shell use: "TASKKILL /im mp.exe /f"
On the remote computer itself, you'll either have to run the TASKKILL command from above, or turn off the computer. You could also turn down the volume, though that wouldn't stop the music from playing you wouldn't be able to hear it anymore.

---
#####Credits:

MrJPGames<br>
Microsoft (for PsExec)<br>
NirSoft (for NirCMD)<br>
http://www.mpg123.de/ (mpg123)<br>
