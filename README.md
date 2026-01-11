# ValRes - VALORANT Resolution Manager

yeah so i made this thing to change valorant res without having to dig through files every time. also auto-downloads vibrancegui because why not.

## what it does

- changes your valorant resolution quickly
- **automatically closes valorant for you** so you don't have to
- has some presets for common stretched res ratios
- downloads and launches vibrancegui automatically 
- you can customize all the colors if you're into that
- finds your valorant config automatically (barley works not gunna lie)
- hides all the config files so your folder stays clean

## requirements

- windows 
- python 3.7+ if you're running the .py file
- valorant installed somewhere

## how to use

### if you have the .exe
just run it. that's it.

### if you're running from source
run `install.bat` first to get dependencies, then:
```bash
python ValRes.py
```

## first time setup

when you first run it:

1. it'll try to find your valorant config
   - if it finds it, just hit enter
   - if not, you gotta paste the path manually
   - path looks like: `C:\Users\YourName\AppData\Local\VALORANT\Saved\Config\whatever\WindowsClient\GameUserSettings.ini`

2. type in the resolution you want
   - width first (like 1280)
   - then height (like 960)

3. decide if you want vibrancegui to launch automatically
   - it'll download it for you if you say yes

## menu options

**[1] Apply Resolution**
apply whatever res you have set. if valorant is running, it'll close it for you automatically.

**[2] Presets**
quick access to common resolutions:
- 1280x960 - 4:3 stretched
- 1440x1080 - 4:3 stretched
- 1680x1050 - 16:10
- 1720x1080 - 16:9 stretched
- 1920x1080 - native

**[3] Change Path**
if you need to update where your config file is

**[4] Toggle VibranceGUI**
turn auto-launch on/off

**[5] Theme Editor**
change colors if the default cyan isn't your vibe. has live preview and everything.

**[6] Exit**
self explanatory

## color customization

the theme.config file lets you change every color in the program. 

### color codes you can use:
- 31 = red, 91 = bright red
- 32 = green, 92 = bright green  
- 33 = yellow, 93 = bright yellow
- 34 = blue, 94 = bright blue
- 35 = magenta, 95 = bright magenta
- 36 = cyan, 96 = bright cyan
- 37 = white, 97 = bright white
- 90 = gray

just edit theme.config or use the theme editor in the program.

## what gets created/downloaded

- `config.json` - your settings (auto-hidden)
- `theme.config` - your color preferences (auto-hidden)
- `VibranceGUI.exe` - auto-downloaded from vibrancegui.com and hidden
- temp zip file during vibrancegui download (gets deleted automatically)

all config files are hidden so you don't have to look at them. keeps your folder clean.

## troubleshooting

**"Config file not found"**
- make sure valorant is actually installed
- manually find GameUserSettings.ini and paste the path
- it's in `%LOCALAPPDATA%\VALORANT\Saved\Config\...`

**Valorant won't close automatically**
- might need to run ValRes as admin
- or just close it yourself manually


**VibranceGUI won't download**
- check internet connection
- or just download it yourself from vibrancegui.com
- put it in the same folder as ValRes

**Resolution not applying**
- the program should close valorant automatically now
- make sure the config path is right
- try running as admin if nothing works


## other stuff

- if you delete config.json or theme.config, they'll just regenerate with defaults
- vibrancegui gets downloaded from the official site, extracts, deletes readme, hides itself, then deletes the zip
- the program will auto-close valorant if it's running when you try to apply settings
- all files except ValRes.exe itself are hidden automatically

---

made by **Krozy**

disclaimer: this messes with valorant config files. use at your own risk. not affiliated with riot or anything.

ps: ill add the source code sometime in future im just lazy :)
