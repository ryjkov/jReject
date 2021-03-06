[jReject](http://jreject.turnwheel.com/) - jQuery Browser Rejection Plugin
================================

Created by Steven Bower
TurnWheel Designs 2009-2011

Concept based on "IE6 Upgrade Warning" library.

Visit [jreject.turnwheel.com](http://jreject.turnwheel.com/) for full documentation

Default Options:
-----------------
	options = {
		reject : { // Rejection flags for specific browsers
			all: false, // Covers Everything (Nothing blocked)
			msie5: true,msie6: true // Covers MSIE 5-6 (Blocked by default)
			/*
				Possibilities are endless...

				msie: false,msie5: true,msie6: true,msie7: false,msie8: false, // MSIE Flags (Global, 5-8)
				firefox: false,firefox1: false,firefox2: false,firefox3: false, // Firefox Flags (Global, 1-3)
				konqueror: false,konqueror1: false,konqueror2: false,konqueror3: false, // Konqueror Flags (Global, 1-3)
				chrome: false,chrome1: false,chrome2: false,chrome3: false,chrome4: false, // Chrome Flags (Global, 1-4)
				safari: false,safari2: false,safari3: false,safari4: false, // Safari Flags (Global, 1-4)
				opera: false,opera7: false,opera8: false,opera9: false,opera10: false, // Opera Flags (Global, 7-10)
				gecko: false,webkit: false,trident: false,khtml: false,presto: false, // Rendering Engines (Gecko, Webkit, Trident, KHTML, Presto)
				win: false,mac: false,linux : false,solaris : false,iphone: false, // Operating Systems (Win, Mac, Linux, Solaris, iPhone)
				unknown: false // Unknown covers everything else
			*/
		},
		display: ['firefox','chrome','msie','safari','opera','gcf'], // What browsers to display and their order
		browserInfo: { // Settings for which browsers to display
			firefox: {
				text: 'Firefox 3.5+', // Text below the icon
				url: 'http://www.mozilla.com/firefox/' // URL For icon/text link
			},
			safari: {
				text: 'Safari 4',
				url: 'http://www.apple.com/safari/download/'
			},
			opera: {
				text: 'Opera 10.5',
				url: 'http://www.opera.com/download/'
			},
			chrome: {
				text: 'Chrome 5',
				url: 'http://www.google.com/chrome/'
			},
			msie: {
				text: 'Internet Explorer 8',
				url: 'http://www.microsoft.com/windows/Internet-explorer/'
			},
			gcf: {
				text: 'Google Chrome Frame',
				url: 'http://code.google.com/chrome/chromeframe/',
				allow: { all: false, msie: true } // This browser option will only be displayed for MSIE
			}
		},
		header: 'Did you know that your Internet Browser is out of date?', // Header of pop-up window
		paragraph1: 'Your browser is out of date, and may not be compatible with our website. A list of the most popular web browsers can be found below.', // Paragraph 1
		paragraph2: 'Just click on the icons to get to the download page', // Paragraph 2
		close: true, // Allow closing of window
		closeMessage: 'By closing this window you acknowledge that your experience on this website may be degraded', // Message displayed below closing link
		closeLink: 'Close This Window', // Text for closing link
		closeURL: '#', // Close URL
		closeESC: true, // Allow closing of window with esc key
		closeCookie: false, // If cookies should be used to remmember if the window was closed (see cookieSettings for more options)
		// Cookie settings are only used if closeCookie is true
		cookieSettings: {
			path: '/', // Path for the cookie to be saved on (should be root domain in most cases)
			expires: 0 // Expiration Date (in seconds), 0 (default) means it ends with the current session
		},
		imagePath: '/images/', // Path where images are located
		overlayBgColor: '#000', // Background color for overlay
		overlayOpacity: 0.8, // Background transparency (0-1)
		fadeInTime: 'fast', // Fade in time on open ('slow','medium','fast' or integer in ms)
		fadeOutTime: 'fast' // Fade out time on close ('slow','medium','fast' or integer in ms)
	}

Run On load (Default Options):
	$(function() {
		$.reject();
	});
