# Notify Manager
<p align="center">
<a href="javascript:void(0)">
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=10000&color=DB33F7&center=true&vCenter=true&width=435&lines=Notify+Manager">
</a>
</p>
<p align="center">
Create beautiful and functional notifications on electron
</p>

# Info
You can test the library with `npm run test`. And also see the source code of [test.js](https://github.com/fydne/Notify-Manager-electron/tree/main/files/test.js)

#### Approximate result:
<a href="javascript:void(0)">
<img src="https://cdn.scpsl.store/another/kvrfintgaflc/image.png">
</a>

> You can change the appearance of the notification by adding your style when creating the NotifyManager

You can use your own sounds when showing a notification.

https://user-images.githubusercontent.com/121295212/219909789-5f343998-814b-4c2a-814b-d290ea1fe3a2.mp4


# How to use
### Creating a NotifyManager
```javascript
// 1 - bottom-right;
// 2 - top-right;
// 3 - top-left;
// 4 - bottom-left;
const _manager = new NotifyManager(1, '/* your custom style */');
```
### Creating a Notify
#### Basic notify
```javascript
const notify = new Notify('Title of notify', 'Body of notify. HTML allowed.');

// show notify
_manager.show(notify);
```
#### Notification with image & custom duration
Recommended image size - 55x55px
```javascript
const duration = 30; // in seconds
const notify = new Notify('Your App', 'Your beautiful message', duration, 'https://github.com/favicon.ico');

// show notify
_manager.show(notify);
```
#### Notify with sound
##### Attention: It is not recommended to use music playing for a long time. Instead, use sounds up to 10 seconds long. The example below uses music for demonstration purposes only.
```javascript
// url, volume
const sound = new NotifySound('https://cdn.fydne.dev/another/rgq05ekp8k4k/sneg.mp3', 50);

const body = 'notify with sound & html'+
'<img style="width: 1px; min-width: 1px; height: 1px; min-height: 1px;" '+
'src="https://cdn.fydne.dev/another/j7jtku7ebf86/1px.svg" '+
'onload="window.open(`https://soundcloud.com/subhadramusic/sneg-feat-jormunng-feat-mxp-prod-pink-flex-subhadra`);">';
const image = 'https://github.com/fydne/SoundCloud-Desktop/raw/main/icons/appLogo.png';

const notify = new Notify('Notify', body, 60, image, sound);

// show notify
_manager.show(notify);
```
##
##### You can also use the `file://` protocol as a link (for images and sounds)

<p align="center">
<a href="javascript:void(0)">
<img src="https://profile-counter.glitch.me/notify-manager-electron/count.svg" width="200px" />
</a>
