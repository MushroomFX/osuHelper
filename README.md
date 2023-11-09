# **osuHelper**
This project is supposed to help osu-players get some **QOL-features** without **osu-suppoerter**

## **Features:**
- [Auto-Map download](#auto-map-download)
- [Auto-Map installer](#auto-map-installer)

- - -

## Auto-Map download
For downloading maps automatically, use the following script with a web injector like [User JavaScript and CSS](https://chromewebstore.google.com/detail/nbhcbdghjpllgmfilhnhkllmkecfmpld).

### Code:
```js
var downloadInterval = setInterval(function() {
	if(window.location.hash !== ''){
		window.location.href =  window.location.href.replaceAll(window.location.hash,'') + '/download';
		clearInterval(downloadInterval);
		setTimeout(function() {
			window.close();
		}, 1000);
	}
}, 100);
```
### URL:
https://osu.ppy.sh/beatmapsets

- - -

## Auto-Map installer
For installing maps automatically, you can use any programming/scripting-language to scan for **.osz** files and exectute them.
### Batch-Code example:
```bat
:rl
for %%i in (*.osz) do start "" "%%~i"
timeout 5
goto rl
```
*(can be found in the repo under **./files/osuMapInstaller.bat**)*

- - -
