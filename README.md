This filter list was created 2015 and is under MIT license by CHEF-KOCH and contains all the advertising domains which are hard-coded within Spotify (free account). <br/>

The project is unofficial and not in any relationship with [Spotify AB](https://en.wikipedia.org/wiki/Spotify). <br/>

# Project is closed and merged within [CK's-FilterList](https://github.com/CHEF-KOCH/CKs-FilterList) ([mirror](https://gitlab.com/CHEF-KOCH/cks-filterlist))!

[![GitHub release](https://img.shields.io/github/release/CHEF-KOCH/Spotify-Ad-free.svg?label=Latest%20Release&style=popout)](https://github.com/CHEF-KOCH/Spotify-Ad-free/releases/latest)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/fold_left.svg?style=social&label=Follow%20%40CHEF-KOCH)](https://twitter.com/CKsTechNews)
[![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/CHEF-KOCH)
[![Discord](https://discordapp.com/api/guilds/418256415874875402/widget.png)](https://discord.me/CHEF-KOCH)


### Project Overview 

You can easily import the "blocker" (filters) list into any Ad-blocker or download the pre-made Ad-Free versions. A HOSTS file is not a "crack". 


### Official client(s) & download information

* [Android Alpha Google Group](https://groups.google.com/forum/#!forum/spotify-android-alpha/join)
* [Android Beta Google Group](https://groups.google.com/forum/#!forum/spotify-android-beta/join)
* [Android App Testing Page](https://play.google.com/apps/testing/com.spotify.music)
* [Official Play Store link](https://play.google.com/store/apps/details?id=com.spotify.music)
* [Unofficial Linux Mint Link](http://packages.linuxmint.com/search.php?release=any&section=any&keyword=spotify)
* [Official MacOS Link](https://download.scdn.co/Spotify.dmg)
* [Official Linux Link](https://www.spotify.com/de/download/linux/)

I provide untouched official mirrors as they come, in case someone wants to manually up-/downgrade. Spotify itself in fact does keep backups of all their client releases but they don't post the links public.


### Bypassing ToS (_needs confirmation_)

* The current ToS (see link below) only affects America and Europe, Swiss is not affected. My advice is to setup a Proxy/VPN for Spotify which connects to Swiss in order to _bypass_ (needs confirmation) the ToS in case you're account get banned you can then win this case and the swiss server in general have less ads.

An additional advice is to set this:

- Edit - Preferences (CTRL + P) - Privacy _Block all cookies..._ (enable it)
- Edit - Preferences (CTRL + P) - Advertisement - Change advertising preferences (disable everything here on the Spotify website)
- Manually delete the Spotify cache folder and mark it as _read-only_so that Spotify won't get access tp it, which prevents to store meta-data and ads in it. 

This helps to get rid of cookie leftover(s) tracker(s) and reduces the chance to see banner ads (it does not remove them!). 


### How to capture ads on Windows?

* Flush your DNS cache `ipconfig /flushdns`, then run [DNSQuerySniffer](http://www.nirsoft.net/utils/dns_query_sniffer.html) and your Spotify Client
* After an audio Ads appears save domains list via DNSQuerySniffer. 
* In order to provide a useful _Pull request_ or _Bug report_ ensure you're use the latest Spotify version. 


### How to capture ads on Android?

* Install AdGuard, ensure HTTPS filtering is globally activated and enabled for the Spotify application. 
* Enable DNS filtering.
* Go to filter log and export the list. You can click on the domains and block them and export the list in order to provide a useful Pull Request.


### How to enable the Spotify Audio Routing function?

* Using _--enable-audio-graph_ at the end of the Spotify shortcut target address will enable the Playback device selection box!


### How to disable Spotify auto update (without blocking domains in HOSTS)?

```
// Open Command Prompt with Admin rights:
icacls "%localappdata%\Spotify\Update" /reset /T

del /s /q "%localappdata%\Spotify\Update"

mkdir "%localappdata%\Spotify\Update"

icacls "%localappdata%\Spotify\Update" /deny "%username%":W
```

### How to get Spotify premium for ~ 2 €/Dollars

- Use a VPN and use one of the following locations: Argentina, Vietnam, Philippine, Brazil
- The url is always the same `http://spotify.com/ph/signup` only the `/ph/` part changes which points to the location in this example it points to the philippines. 
- Some countries censorship the spotify content e.g. India, so don't use such countries.


### Release & RePack information

I do _not officially maintain this project_ which means every work I still do is for the community only and entirely for free. I spent a lot of time debugging and inspecting Spotify's traffic. 

No one is forced to download something from the [release tab](https://github.com/CHEF-KOCH/Spotify-Ad-free/releases) nor do I support something illegal here. Repacking the installer is not illegal, however modifying the files itself is because it's against ToS (which I respect) but including several additional patches and a HOSTS file seems pretty much okay because Spotify does include already anti-blocking debugging techniques to prevent all of this. Abusing "holes" is illegal. 

In this repo I provide:
* Ad-Free mods for Desktops and the Android OS. MacOS is official not supported because I don't use any Apple products.
* Filter lists in order to block ads (via hosts).


### Spotify updating mechanism
The UWP Spotify app gets updates _quicker_ since they are automatically compiled (which explains the strange [versions scheme](https://en.wikipedia.org/wiki/Software_versioning) which means the Win32 apps are uploaded around 4-10 days later (depending how fast Spotify rolls them out).

### Preventing updates on MacOS (untested)
The user [julionc](https://github.com/julionc) wrote a small script to prevent updates on MacOS.

* Uninstall all old Spotify versions on your MacOS.
* Install a Spotify MacOS version [below 1.0.80](https://mac.filehorse.com/download-spotify/10400/). 
* Open and [copy the file](https://github.com/julionc/dotfiles/blob/9990859cf4de0536d0d2b4351c3f19dec9fdfd48/osx/doNotUpdateSpotify.sh) to `whatever.sh`. 
* Save the file on your desktop and open the MacOS terminal, enter `cd desktop` and then execute `sudo sh whatever.sh`.

The script will block Spotify from updating itself. Alternative _solutions_ are [Spotifree](https://github.com/simonmeusel/MuteSpotifyAds#alternatives) & [MuteSpotify Ads](https://github.com/simonmeusel/MuteSpotifyAds). If all of it fails, uBlock is still working (Spotify Web) on all systems without any need for installing third-party software on your OS.

### Reference
* [Spotify Downloader (github.com)](https://github.com/ritiek/spotify-downloader) - Download Spotify playlists with albumart and meta-tags.
* [Spytify (github.com)](https://github.com/jwallet/spy-spotify) - Records Spotify without ads while it plays and includes media tags to the recorded files
* [abertschi/ad-free (github.com)](http://adfree.abertschi.ch) - A modularized Ad Blocker for Spotify on Android.  
* ~~[BlockTheSpot](https://github.com/master131/BlockTheSpot/) - Spotify injection (for the Windows Desktop version only) which blocks video, audio & banner~~
* [Spotify Terms and Conditions of Use](https://www.spotify.com/us/legal/end-user-agreement/#s9)
* [Proof that Spotify collects everything](https://twitter.com/steipete/status/1025024813889478656) + they [sell your private data](https://betanews.com/2016/07/22/spotify-sells-user-data-to-advertisers/)
* [SpotMyBackup](https://github.com/secuvera/SpotMyBackup) - Backup your playlist & tracks.
* [Yay for Bloatware: Samsung to Pre-Install Spotify on Its Smartphones](https://news.softpedia.com/news/yay-for-bloatware-samsung-to-pre-install-spotify-on-its-smartphones-525250.shtml)
* [Spicetify-cli](https://github.com/khanhas/spicetify-cli) - Commandline tool to customize Spotify client.

### Block Spotify updates
* [spotify_version_keeper (github.com)](https://github.com/SrMordred/spotify_version_keeper) - A small app which prevents Spotify updates on Windows. 


### Anti-debugger protection in Spotify 
* [Spotify vs OllyDbg (2009) (web.archive.org)](https://web.archive.org/web/20130417061130/http://www.steike.com/code/spotify-vs-ollydbg/) 


### Browser extension (for Spotify Web)
* [Spotify Crack Chrome App (github.com)](https://github.com/sooxiaotong/spotify-crack-chrome-app) - Basically an app for Chrome in case you nver heard of uBlock/AdGuard & Co. 


### Criticism of Spotify
- The spotify clients aren't open source
- [Spotify now requiring users to share location data to prevent abuse of family plan](https://9to5mac.com/2019/09/12/spottily-family-plan-location/)
- other [stuff mentioned on WIkipedia](https://en.wikipedia.org/wiki/Criticism_of_Spotify)


### Spotify Alternatives
* [Audius](https://audius.co/)
* [Qobuz](https://www.qobuz.com/gb-en/discover)
* [Deezer](https://www.deezer.com/en/)


