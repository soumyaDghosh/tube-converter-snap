\# Tube Converter
<img src="https://github.com/nlogozzo/NickvisionTubeConverter/raw/main/NickvisionTubeConverter.Shared/Resources/org.nickvision.tubeconverter.png" width="100" height="100"/>

**An easy-to-use YouTube video downloader**

# Features
- A basic yt-dlp frontend
- Supports downloading videos in multiple formats (mp4, webm, mp3, opus, flac, and wav)
- Run multiple downloads at a time
- Supports downloading metadata and video subtitles

# Disclaimer
The authors of Nickvision Tube Converter are not responsible/liable for any misuse of this program that may violate local copyright/DMCA laws. Users use this application at their own risk.

# Installation
<p><a href="https://snapcraft.io/tube-converter"><img width='150' alt="Get it from the Snap Store" src="https://snapcraft.io/static/images/badges/en/snap-store-black.svg" /></a></p>

# Chat
<a href='https://matrix.to/#/#nickvision:matrix.org'><img width='140' alt='Join our room' src='https://user-images.githubusercontent.com/17648453/196094077-c896527d-af6d-4b43-a5d8-e34a00ffd8f6.png'/></a>

# Screenshots
![MainWindow](https://github.com/soumyaDghosh/tube-converter-snap/raw/main/Screenshots/Screenshot%20from%202023-03-27%2000-17-20.png)
![AddDownloadDialog](https://github.com/soumyaDghosh/tube-converter-snap/raw/main/Screenshots/Screenshot%20from%202023-03-27%2000-20-53.png)
![Downloading](https://raw.githubusercontent.com/soumyaDghosh/tube-converter-snap/main/Screenshots/Screenshot%20from%202023-03-27%2000-21-00.png)
![Done](https://raw.githubusercontent.com/soumyaDghosh/tube-converter-snap/main/Screenshots/Screenshot%20from%202023-03-27%2000-21-14.png)
![LightMode](https://github.com/soumyaDghosh/tube-converter-snap/raw/main/Screenshots/Screenshot%20from%202023-03-27%2000-17-34.png)
![AboutPage](https://raw.githubusercontent.com/soumyaDghosh/tube-converter-snap/main/Screenshots/Screenshot%20from%202023-03-27%2000-17-54.png)

# Translating
Everyone is welcome to translate this app into their native or known languages, so that the application is accessible to everyone.

To translate the app, fork the repository and clone it locally. Make sure that `meson` is installed. Run the commands in your shell while in the directory of repository:
```bash
meson build
cd build
meson compile org.nickvision.tubeconverter-pot
```
Or, if you are using GNOME Builder, build the app and then run in the Builder's terminal:
```bash
flatpak run --command=sh org.gnome.Builder
cd _build
meson compile org.nickvision.tubeconverter-pot
```
This would generate a `NickvisionTubeConverter/po/org.nickvision.tubeconverter.pot` file, now you can use this file to translate the strings into your target language. You may use [Gtranslator](https://flathub.org/apps/details/org.gnome.Gtranslator) or [poedit](https://poedit.net) if you do not know how to translate manually in text itself. After translating (either through tools or directly in text editor), make sure to include the required metadata on the top of translation file (see existing files in `NickvisionTubeConverter/po/` directory.)

One particular thing you should keep in mind is that some strings in this project are bifurcated into multiple strings to cater to responsiveness of the application, like:
```
msgid ""
"If checked, the currency symbol will be displayed on the right of a monetary "
"value."
```
You should use the same format for translated strings as well. But, because all languages do not have the same sentence structure, you may not need to follow this word-by-word, rather you should bifurcate the string in about the same ratio. (For examples, look into translations of languages which do not have a English-like structure in `NickvisionTubeConverter/po/`)

Put your translated file in `NickvisionTubeConverter/po` directory in format `<LANG>.po` where `<LANG>` is the language code.

Put the language code of your language in `NickvisionTubeConverter/po/LINGUAS` (this file, as a convention, should remain in alphabetical order.)

Add information in `NickvisionTubeConverter/po/CREDITS.json` so your name will appear in the app's About dialog:
```
"Jango Fett": {
    "lang": "Mandalorian",
    "email": "jango@galaxyfarfar.away"
}
```
If you made multiple translations, use an array to list all languages:
```
"C-3PO": {
    "lang": ["Ewokese", "Wookieespeak", "Jawaese"],
    "url": "https://free.droids"
}
```

To test your translation in GNOME Builder, press Ctrl+Alt+T to open a terminal inside the app's environment and then run:
```
LC_ALL=<LOCALE> /app/bin/org.nickvision.tubeconverter
```
where `<LOCALE>` is your locale (e.g. `it_IT.UTF-8`.)

Commit these changes, and then create a pull request to the project.

As more strings may be added in the application in future, the following command needs to be ran to update all the `.po` files, which would add new strings to be translated without altering the already translated strings. But, because running this command would do this for all the languages, generally a maintainer would do that.

```bash
meson compile org.nickvision.tubeconverter-update-po
```

# Dependencies
- [.NET 7](https://dotnet.microsoft.com/en-us/)
- [ffmpeg (GNOME)](https://ffmpeg.org/)
- [python (GNOME)](https://python.org/)
- [yt-dlp as python module (GNOME)](https://github.com/yt-dlp/yt-dlp)

# Special Thanks
- [daudix-UFO](https://github.com/daudix-UFO) and [martin-desktops](https://github.com/martin-desktops) for our application icons

# Code of Conduct
This project follows the [GNOME Code of Conduct](https://wiki.gnome.org/Foundation/CodeOfConduct).

