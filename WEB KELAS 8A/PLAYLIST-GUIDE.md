# 🎵 Music Playlist Customization Guide

## **Quick Edits (5 mins)**

### 1. **Change/Add Songs** `music-tracks.js`
```
Replace the `tracks` array:
```js
const tracks = [
  {
    title: 'Your Song Name',
    artist: 'Artist Name',
    src: 'path/to/your-song.mp3',  // Upload MP3 here
    duration: '3:45',              // Format MM:SS
    art: 'path/to/album-art.jpg'   // 300x300px image
  }
];
```
**Demo tracks use free SoundHelix MP3s - replace `src` with local files.**

### 2. **Update Track List UI** `index.html` #track-list `<li>`
```
<li data-track="0">
  <span>Song Name - Artist</span>
  <span>3:45</span>
</li>
```
Add more `<li>` matching array index.

### 3. **Player Colors** `style.css` CSS vars
```
:root {
  --primary-color: #your-color;  // Player accent
  --glass-bg: rgba(...);         // Player background blur
}
```

## **Advanced (15 mins)**

### **Add Playlist Shuffle/Repeat** `script.js`
```js
// Add buttons in HTML, then:
shuffleBtn.addEventListener('click', shufflePlaylist);
repeatBtn.addEventListener('click', toggleRepeat);
```

### **Volume Control**
```html
<input type="range" id="volume-slider" min="0" max="1" step="0.1" value="0.5">
```
```js
volumeSlider.addEventListener('input', (e) => {
  audioPlayer.volume = e.target.value;
});
```

### **Real Audio Files**
1. Add MP3s to folder
2. Update `src: 'your-song.mp3'`
3. Upload album art JPG/PNG

## **Sections to Edit:**

| File | Line/Section | What to Change |
|------|--------------|---------------|
| `music-tracks.js` | `tracks` array | Song data (title/artist/src/duration/art) |
| `index.html` | `#track-list ul li` | Track list display |
| `style.css` | `.player, .playlist` | Player design/colors |
| `script.js` | Music Player functions | Add shuffle/volume/repeat |

**Live preview:** Open `index.html` → scroll to #playlist → play demo tracks!

**Pro tip:** Use Audacity (free) to convert/edit MP3s, Canva for album art.
