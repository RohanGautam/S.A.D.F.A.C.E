## Inspiration

S.A.D.F.A.C.E. stands for Sentiment Analysis Data For A Computer-vision Extension and has been designed for YouTube. In this data driven age, it is imperative for content creators as well as companies to get more metrics on how audiences perceive their content. S.A.D.F.A.C.E. does just that through live recording and analysis of viewer emotions.
YouTube is definitely not at its prime now as it once used to be. Videos can fail to target the right audience or flat out get demonetized because they happened to break even a single one of YouTube’s stringent content policies. This leads to unhappy creators that stop taking creative risks in order to avoid having their only source of living being snatched away from them. S.A.D.F.A.C.E. can help them tailor their content to their audience and adapt to changing opinions.

## What it does

Our project is a chrome extension that is integrated with a python backend which runs scripts for detecting emotions. The extension allows the users to record their face and their reactions while watching a YouTube video. The backend then splits the video into various frames and performs the machine learning scripts on them to find the dominant emotion in each frame. This information is then collated in the form of graphs in a user-friendly dashboard for the YouTube creators to analyze. This allows ![chromeExtension](https://user-images.githubusercontent.com/17317792/51651212-0b97e380-1fc6-11e9-9efc-f5b725724fd4.jpg)
![contentCreatorDashboard](https://user-images.githubusercontent.com/17317792/51651214-0dfa3d80-1fc6-11e9-9883-7b62c0f754bb.jpg)


## How we built it

### Chrome Extension:

1. Chrome Developer Dashboard was used to publicly list the extension on the Chrome Web Store.
2. Various Chrome APIs were called such as ActiveTab and VideoCapture to give the extension the required features.
3. ES6, JavaScript and JQuery was used to manipulate the DOM structure of the extension popup. 

### Front-end:

1. The front end is built using React and Material UI. 
2. Axios is used to listen for video searches and query the MongoDB database hosted on MLab.
3. Chart.js is used to display the data retrieved from the database.


## Challenges we ran into

1. We were unable to use “fetch()” to make AJAX requests to the database as it always returned an undefined value. Axios was used as a more robust alternative.
2. Due to may async requests, the front-end was very prone to errors which could cripple the system. Thus, it was necessary to add error handling for situations such as when the entered video doesn’t exist in the database.
3. We were unable to print the current timestamps from a YouTube video to the extension popup because the DOM loaded slower than the code was processed even though they were being logged into the console.
4. Figuring out which requests to send to what environment so that a particular API worked in the chrome extension was a complicated process.


## What we learned

1. How to make asynchronous requests to remote MongoDB databases using axios
2. How to display data in a succinct and comprehensible format using Chart.js
3. How to manage a vast amount of data through states and props in react via component lifecycle methods.
4. How to send requests between the various environments of a chrome extension.
5. How to query information from YouTube videos into the extension.


## What's next for S.A.D.F.A.C.E.

1. Partner with sites like YouTube to add a reward program to incentivise viewers to record their emotions.
2. Enabling crowdsourcing of data instead of taking the data from only one user per video as it is now.
3. Build our extension so that it can run 100% online (for instance, webcam works offline for now).
4. Synchronize the reactions video perfectly with the actual video and allow pausing of the video (we have it working with Selenium but not with the actual extension).

#### DevpostLink: https://devpost.com/software/cz-s-a-d-f-a-c-e
