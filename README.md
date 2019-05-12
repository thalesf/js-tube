<h1 align="center" > Youtube playlist duration in javascript</h1>

<p align="center">
<img src="https://user-images.githubusercontent.com/11466066/57586456-90066780-74cc-11e9-9f19-7411e3b7c74e.png"
width=150px>
</p>

## Usage :smile:
Access a youtube playlist:

https://<span></span>youtube.com/<strong>playlist?list</strong>=PLMC9KNkIncKtPzgY-5rmhvj7fax8fdxoj</p>

Open the developer console using <strong> F12 </strong>

Paste the code below.

## Code :zap:

```js
let date = new Date(null);
document
  .querySelectorAll("ytd-thumbnail-overlay-time-status-renderer")
  .forEach(video =>
    date.setSeconds(
      video.innerText
        .split(":")
        .reduce((accumulator, time) => 60 * accumulator + +time)
    )
  );
console.log(date.toISOString().substr(11, 8));

```
