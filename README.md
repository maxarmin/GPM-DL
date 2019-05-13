# GPM-DL
**Experimental** Tool written in Python to download tracks from Google Play Music for Windows.
Sister of [Qo-DL](https://github.com/Sorrow446/Qo-DL) and [Ti-DL](https://github.com/Sorrow446/Ti-DL).

Latest versions:

Windows:   
GPM-DL: 12th May 19 - Release 1 - [DOWNLOAD - x64](https://thoas.feralhosting.com/sorrow/GPM-DL/Latest%20Build/GPM-DL_x64.exe)   
No x86 build at the moment as a needed lib is having issues working with it.   

![](https://thoas.feralhosting.com/sorrow/GPM-DL/b1.jpg)

# Setup
## Mandatory ##
The following field values need to be inputted into the config file:
- email
- password - **must be app password. Must have 2-step auth.** See: https = //myaccount.google.com/apppasswords
- quality - 1 = MP3 128, 2 = MP3 160, 3 = MP3 320
- namingSscheme - 1 = "01. ", 2 = "01 -"
- soundNotifVol - volume of sound notification. 0-1. I don't advise going over 0.5.
- checkForUpdates - you will still be able to use GPM-DL without having the latest version.

- All tags under "[Tags]" and "[Playlist]" except comment.

**You can't download ANY tracks with a free account.**
## Optional ##
- comment - write custom comment to comment field. Special chars will be escaped.
- downloadDir - where to download tracks to. Make sure you wrap this up in double quotes. "" = %CD%\GPM-DL Downloads.
- soundNotif - play audio file of your choice. Specify the filename of your audio file. Must be in GPM-DL's directory and must be either MP3 or WAV format.

# Usage
Fill in your config file first.

### Windows ###
Run the exe.   
**Streaming on another device while using GPM-DLs will cause 403s.**

GPM-DL can also be used via command line.   
**Make sure you cd to GPM-DL's dir before calling it or it won't not be able to read your config file.**   
```
usage: GPM-DL.py [-h] [-url URL] [-q Q] [-p P] [-s S] [-comment COMMENT]
                 [-list LIST]

optional arguments:
  -h, --help        show this help message and exit
  -url URL          Google Play Music URL.
  -q Q              Download quality. 1 = MP3 128, 2 = MP3 160, 3 = MP3 320.
  -p P              Where to download tracks to. Make sure you wrap this up in
                    double quotes.
  -s S              File naming scheme. 1 = "01. ", 2 = "01 -".
  -comment COMMENT  Write custom comment to comment field in track tags. Make
                    sure you wrap this up in double quotes.
  -list LIST        Download from a list of URLs. -list <txt file filename>.
                    Accepted URL types: album, track, playlist.
```
# Update Log #
### 12th May 19 - Release 1 ###

# Misc Info
- Written around Python v3.6.7.    
- If there are required empty or missing fields in your config file, GPM-DL will notify you and write any missing fields to your config file.
- Any special characters that Windows doesn't support in filenames are replaced with "-".    
- Filename clashes are handled inside of album folders. If a clash occurs inside an album folder, the previous file will be deleted.     
- id3 v2.3 is used for tags.

If you need to get in touch: Sorrow#5631, [Reddit](https://www.reddit.com/user/Sorrow446)

# Disclaimer
GPM-DL does NOT contain code to decrypt encrypted tracks from Google Play Music.    
I will not be responsible for how you use GPM-DL.    
Google brand and name is the registered trademark of its respective owner.    
GPM-DL has no partnership, sponsorship or endorsement with Google.    
