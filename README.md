# chrome-header-extension-bug
This is a way to reproduce a Chrome bug where an extension adds an extra header to each request and subsequently fails downloading images.

# Setup

1. Chrome 42
2. PC, Windows 8.1 Pro
3. Enable just one Chrome extension that can modify headers, for instance [Requestly](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa) or [ModHeader](https://chrome.google.com/webstore/detail/modheader/idgpnmonknjnojddfkpgkljpfnnfcklj).
4. Add a custom header, ie: `TerminalId = Vekt1-Oppe`

# How to reproduce

1. [Watch a video](http://youtu.be/2GH7hCzkVUI?hd=1) of how I reproduce the bug.
2. Start a local web server (I used [http-server](https://www.npmjs.com/package/http-server))
3. Open the index.html in Chrome and press and hold F5 for 10 seconds. Release and see if the images load or if they get stuck in "pending" mode. Repeat until images are stuck in "pending" mode.

# pages.github.io
I also put the test site on http://nitech.github.io/chrome-header-extension-bug/, but I can't reproduce the bug there. It seems the server has to have a very quick response time for us to trigger the bug. Try instead [http-server](https://www.npmjs.com/package/http-server) or similar. 
