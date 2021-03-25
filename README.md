# Pre-work - _Follow That Tune_

**Follow That Tune** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **George Melek**

Time spent: **4** hours spent in total

Link to project: https://glitch.com/edit/#!/boggy-heavenly-truck?path=index.html%3A4%3A19

## Required Functionality

The following **required** functionality is complete:

- [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [x] "Start" button toggles between "Start" and "Stop" when clicked.
- [x] Game buttons each light up and play a sound when clicked.
- [x] Computer plays back sequence of clues including sound and visual cue for each button
- [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [x] User wins the game after guessing a complete pattern
- [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [x] Buttons use a pitch (frequency) other than the ones in the tutorial
- [x] More than 4 functional game buttons
- [x] Playback speeds up on each turn
- [x] Player only loses after 3 mistakes (instead of on the first mistake)
- [ ] Computer picks a different pattern each time the game is played
- [ ] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [ ] User has a limited amount of time to enter their guess on each turn


## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](https://i.imgur.com/zbTbdKN.gif)


## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.

I did not need to use any outside resources to help complete my submission for the required user stories thanks to Codepath's very useful and beginner-friendly instructions, but to alter the colors of the new buttons I added, I used this link as a reference for CSS colors: https://www.w3schools.com/cssref/css_colors.asp
Also, in an attempt to create a randomizePattern function I used this link to learn about Math.random: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random and this link to learn more about arrays in Javascript: https://www.w3schools.com/js/js_arrays.asp

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

When I thought I was complete with my webpage, I tested it in order to ensure it was production-quality code. I clicked 'Start' and listened to a variety of tones playing, with only the blue button lighting up. At first I believed it was a problem with solely the blue panel, but when I went back to watch the video displaying a successful submission with all requirements present, I realized my thinking was reversed. In reality, the blue button was working as intended - it was the other three buttons that were supposed to be lighting up and were not. Now that I found the issue, it came down to localizing the issue. My first approach was deciding which file of the three that affected the webpage (HTML/CSS/JS) I should be looking into. Using what I learned from Codepath's instructions, I knew the issue could not be in the index.html file - HTML only deals with the physical content of what's displayed, not the displaying thereof. As for the script.js file, I remembered writing functions that would light or clear a button, but I knew if at least one button was functioning properly, the problem could not be there, because the function took a general button as a parameter, not specific ones. Lastly, I was left with style.css file. How could I not realize this earlier? Of course the problem would be here - this file affects how contents located in the html file are displayed. I began by debugging process by commenting out pieces of code that I believed, with good reason, would not affect the lighting-up feature of the buttons. Finally, I was left with the CSS rules that began with "button2:active #button2.lit {". I compared my code for buttons 2-4 with that for button1 and realized the only issue was that I forgot a comma in between the two pseudo-classes. Once I added the comma for each button, the webpage was functioning as expected. And that is how a singular "," and the Software Development Life Cycle taught me a lesson on overcoming challenges.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

Actually, I have a bunch of questions about web development. The first would be: if vanilla Javascript is so useful, then what need is there for React.js? My understanding is that React.js is a sort of library of javascript functions that you could import in order to make your website more dynamic, is that correct? If so, does the same logic apply for the rest of the MERN (MongoDB, Express, React.js, Node.js) and similar Stacks? Another question I have is which languages do Front-End Developers primarily focus on compared to Back-End Developers? Where do UI/UX Designers come into play? Are they just niche Front-End Developers? How do web developers consistently have work? Does one website really need that much maintenance? Or do they have multiple projects at any given time from different clients? As for development itself, how do you implement common features as seen in Facebook and YouTube such as infinite scrolling, user authentication, tailoring a feed based on the specific user, etc.?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)

If I had a few more hours to work on this project, I would definitely spend them on successfully completing my randomizePattern function, as I can tell I'm very close, as well alter the HTML contents more to make it a more personal website. This would include adding images to the buttons, like popular and funny memes such as Pepe the Frog, Bad Luck Brian, and 'The Office' memes, to name a few. As for the audio, when you click the button, the sound you hear should be related to the image attached to it. For example, if you clicked on a button with 'The Office' picture, you would hear a very short clip of Dwight yelling at Jim (two main characters in the TV show). In an effort to make the User Experience more enjoyable, I would also attempt to make the background a cool wallpaper or picture rather than a plain color. Overall, I would want the webpage to be more personable and possibly even have ads for the effort of monetization.

## License

    Copyright George Melek

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.