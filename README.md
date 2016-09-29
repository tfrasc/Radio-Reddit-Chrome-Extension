# Reddit-Continuous-Music-Extension
*This is currently in development*
- Originally, the goal of this extension was to build on top of the Reddit Enhancement Suite (RES). Unfortunately, the iFrame's provided by RES don't allow Cross-Origin events to allow me to trigger starting the music player/video. Through a bit of trial, error, and research this project evolved into a dynamic music player that automatically cycles through the links on a music subreddit, independent (or on top of) of RES.

## Goal
The Goal of this extension is to simulate a radio-type streaming experience on music subreddits. Just click play on the extension pop-up in Chrome's menu bar and let the music play!

## Branches
- soundcloud_api: This branch now loads Soundcloud links through their api and detects an end event when the music is over and cycles to next video. Youtube and Mixcloud links play, however they don't currently have an end event (you have to manually click next). Mixcloud links don't play automatically.
- iframe_no_api: This branch opens up each link in an iframe that plays on the subreddit page itself. This is currently only compatible with youtube videos as those can simply use a different link to play in iframes. However, this will allow to use the youtube iframe api and souncloud player widget that will allow detecting end of song, therefore allowing easy navigation to next link.
- message_api: This branch opens up a new tab by grabbing the url from each thread title. Some controls have been implemented through the extension's popup icon.  
- no_chrome_api: This branch opens up a new tab by grabbing the url from each thread title.

## TODO
- Integrate Youtube, Bandcamp, Mixcloud, and other API's to fire music end events and automatically continue to next song (I plan to submit version 1.0 to Chrome Web Store after Youtube integration)
- Integrate Play/Pause commands from popup attached to button
- Add fancier CSS to popup attached to button
- Create icon for button
