<div align="center">
  <img alt="League Page logo" src="https://storage.googleapis.com/nfl-player-data/League%20Page.png" width="100px" />

  **[(Unofficial) Sleeper League Page Template](https://github.com/nmelhado/league-page/)**


Generate a custom league page for your Sleeper fantasy football league in just a few steps
  <br />

  ![GitHub](https://img.shields.io/github/license/nmelhado/league-page) [![node](https://img.shields.io/badge/node-%3E%3D14-brightgreen)](https://github.com/nmelhado/league-page) ![GitHub top language](https://img.shields.io/github/languages/top/nmelhado/league-page?color=ff3e00) ![Lines of code](https://img.shields.io/tokei/lines/github/nmelhado/league-page?label=lines%20of%20code) ![GitHub forks](https://img.shields.io/github/forks/nmelhado/league-page) ![GitHub pull requests](https://img.shields.io/github/issues-pr/nmelhado/league-page) ![GitHub issues](https://img.shields.io/github/issues-raw/nmelhado/league-page)
</div>

# Training Wheels Instructions
<div align="center">Keep this open in a separate tab, to make setup as easy as possible</div>

## I. Initial Setup

### 1. Fork This Repo to Your GitHub Account
- If you don't already have a Github account, [make a free account](https://github.com/join)
- Go to [League Page (https://github.com/nmelhado/league-page)](https://github.com/nmelhado/league-page)
- Click on the Fork button
![Fork](https://storage.googleapis.com/nfl-player-data/fork.png)
<br />

- You now have your own League Page!

### 2. Configure your League
- In your league page, go to `/src/lib/utils/helperFunctions/leagueData.js`
![src](https://storage.googleapis.com/nfl-player-data/src.png)
![lib](https://storage.googleapis.com/nfl-player-data/lib.png)
![utils](https://storage.googleapis.com/nfl-player-data/utils.png)
![helperFunctions](https://storage.googleapis.com/nfl-player-data/helperFunctions.png)
![leagueData](https://storage.googleapis.com/nfl-player-data/leagueData.png)
<br />

- Click the edit button
![editLeagueData](https://storage.googleapis.com/nfl-player-data/editLeagueData.png)
<br />

- Replace `your_league_name` and `your_league_id` with your Sleeper league name and ID *[(how to find your league ID)](https://support.sleeper.app/en/articles/4121798-how-do-i-find-my-league-id#:~:text=Go%20toward%20the%20bottom%20of,email%20support%40sleeper.app.)* in `/src/lib/utils/helperFunctions/leagueData.js`:
![league ID instructions](https://storage.googleapis.com/nfl-player-data/editLeagueID.jpg)
- Scroll down to the bottom of the page and commit your changes
<br />

![Commit your changes](https://storage.googleapis.com/nfl-player-data/commitLeagueID.png)
- Your league has been configured!
### 3. Deploy your League Page
- Go to Vercel, and [sign up using your GitHub account](https://vercel.com/signup)
- Now link your Github account to your Vercel account
![Link GitHub account](https://storage.googleapis.com/nfl-player-data/linkAccounts.png)
<br />

- `Import` League Page
![import league page](https://storage.googleapis.com/nfl-player-data/importLeaguePage.png)
<br />

- Skip the Create a Team step
- Leave all setting as they are, and click `Deploy`
![deploy](https://storage.googleapis.com/nfl-player-data/deploy.png)
<br />

- Wait for Vercel to deploy your League Page (should take about a minute)
- Click on `Go to Dashboard`
- Now click on `Visit` to visit your page (and then keep your league website open in that tab)
- You have officially built a website!

## II. Adding Managers and Changing the Homepage Text

### 1. Now that you have a league website, it's time to personalize your homepage
- Go back to GitHub and go to the root of you repo
![root](https://storage.googleapis.com/nfl-player-data/root.png)
<br />

- Go to `/src/routes/index.svelte`
![src](https://storage.googleapis.com/nfl-player-data/src.png)
![routes](https://storage.googleapis.com/nfl-player-data/routes.png)
![index](https://storage.googleapis.com/nfl-player-data/index.png)
<br />

- Click edit
![edit index](https://storage.googleapis.com/nfl-player-data/editIndex.png)
<br />

- Scroll down to lines 151-156
![scroll down](https://storage.googleapis.com/nfl-player-data/scrollDown.png)
<br />

- Each line (which is sandwiched by a `<p>` and a `</p>`) creates a new paragraph on your homepage. Replace those paragraphs with the text you want to use to introduce your league
- If you want fewer paragraphs, delete one of the lines. If you want more, copy a line and paste it below the last `<p>...</p>` in this area
![example text](https://storage.googleapis.com/nfl-player-data/exampleText.png)
<br />

- Scroll down to the bottom of the page when you're done and `Commit changes`
- Now go back to your league website, wait a minute or two, and then refresh!
![text preview](https://storage.googleapis.com/nfl-player-data/textRendered.png)


### 2. Add Managers
- You now have a functioning website, with a personalized homepage. But you're missing one of League Page's best features, Managers!
- Go back to GitHub and go to the root of you repo
![root](https://storage.googleapis.com/nfl-player-data/root.png)
<br />

- Go to `/src/routes/managers/managers.js`
![src](https://storage.googleapis.com/nfl-player-data/src.png)
![routes](https://storage.googleapis.com/nfl-player-data/routes.png)
![managers](https://storage.googleapis.com/nfl-player-data/managers.png)
![managersJs](https://storage.googleapis.com/nfl-player-data/managersJs.png)
<br />

- Click the edit button
- Highlight lines 3-68
![highlight](https://storage.googleapis.com/nfl-player-data/highlight.png)
<br />

- On Mac, click: `⌘ Command` + `/`, on Windows, click: `Ctrl` + `/`. This will remove the `// ` or, in coding terminology, `uncomment` these lines, so the code should now look like this:
![uncomment](https://storage.googleapis.com/nfl-player-data/uncomment.png)
<br />

- Each `object` (shown highlighted below) corresponds to one manager
![single manager](https://storage.googleapis.com/nfl-player-data/singleManager.png)
<br />

- Fill each one out as follows:
    - `"roster" :` give the roster ID for this manager
        - To find the roster ID for the manager, go back to your website and scroll down to the `Power Rankings` graph
        ![pRankings](https://storage.googleapis.com/nfl-player-data/pRankings.png)
        <br />

        - The roster ID is the order of the bar chart, the first bar is roster ID 1, the second is roster ID 2, etc.
    - `"name" :` The name of this manager
    - `"tookOver" :` If this manager took over an orphaned team in your league, give the year they took over. Otherwise set this to `null`
    - `"location" :` Where is this manager based out of (City, State, Country, whatever floats your boat)
    - `"bio" :` This manager's bio. If you don't have a bio yet, leave it as is and come back and edit this again when you have the bio.
    - `"bio" :` This manager's bio. If you don't have a bio yet, leave it as is and come back and edit this again when you have the bio.
    - `"photo" :` This manager's photo. To upload a photo:
        - Open up your repo's root in a new tab
        ![newTab](https://storage.googleapis.com/nfl-player-data/newTab.png)
        <br />

        - Got to `/static/managers/`
        ![static](https://storage.googleapis.com/nfl-player-data/static.png)
        ![managersDir](https://storage.googleapis.com/nfl-player-data/managersDir.png)
        <br />

        - Click on `Add file` then `Upload files`
        ![managersDir](https://storage.googleapis.com/nfl-player-data/upload.png)
        <br />

        - Add one or all of the manager photos
        - When you're done, click `Commit changes` at the bottom of the page
        - Back in `/src/routes/managers/managers.js` tab, use the filename to fill out the photo field. For the below file, you would fill out `"photo" : "/managers/nick.jpg",`
        ![managersDir](https://storage.googleapis.com/nfl-player-data/nickExample.png) (please note that this IS case sensitive)
    - `"fantasyStart" :` what year did the manager start playing fantasy
    - `"favoriteTeam" :` supply the lowercase shorthand for a manager's favorite NFL team (i.e. `"nyj"`, `"cle"`, `"sf"`, `"ne"`, etc.)
    - `"mode" :` There are two options: `"Win Now"` or `"Rebuild"`
    - `"rival" :` This has a nested object that should be filled out as follows:
        - `"name" :` The name of this manager's rival (can also be themselves, everyone, or nobody)
        - `"link" :` This corresponds to the other managers on this list. 
            - If the manager's rival is the first manager you created in this list, you would supply `0`, if their rival is the second manager, you would supply `1`, if it's the 10th manager, you would supply `9`, etc.
            - If the rival is nobody or everyone, then supply `null`
            - If the rival is themselves, and they are the third manager in this list, supply `2`
        - `"image" :` Fill this out the same way you did for the manger photo above (you can upload and use specific rival photos if you want) 
    - `"favoritePlayer" :` This is possibly the trickiest step
        - Go to [https://api.sleeper.app/v1/players/nfl](https://api.sleeper.app/v1/players/nfl) in a new tab
        - Use `⌘ Command` + `F` (on Mac), or `Ctrl` + `F` on Windows to search for the player you are looking for and then copy down that player's `player_id`
        ![player selection](https://storage.googleapis.com/nfl-player-data/playerSelection.jpg)
        <br />

        - Supply that number (i.e. `1426`)
    - `"favoritePlayer" :` This is possibly the trickiest step.
    - `"valuePosition" :` Does the manager prefer `"WR"`, `"RB"`, `"QB"`, `"TE"`, etc. for fantasy
    - `"rookiesOrVets" :` Two options, does the manager prefer `"Rookies"` or `"Vets"`
    - `"philosophy" :` The fantasy manager's fantasy football philosophy
    - `"tradingScale" :` a number 1-10 representing how much the manager likes to trade
    - `"preferredContact" :` `"Text"`, `"WhatsApp"`, and `"Carrier Pigeon"` are the only options supplied by default

- You have finished your first manager! Now repeat the process for each manager in your league. Here's [an example](https://github.com/nmelhado2/league-page/blob/master/src/routes/managers/managers.js) of a finished 12 team `managers.js`
- When you're done, scroll down and click `Commit changes`

## 3. Configure the roster to manager link
- Now for the final step
- Go to the root of your repo
- Go back to the root of you repo
![root](https://storage.googleapis.com/nfl-player-data/root.png)
<br />

- Go to `/src/lib/utils/rosterManagers.js`
![src](https://storage.googleapis.com/nfl-player-data/src.png)
![lib](https://storage.googleapis.com/nfl-player-data/lib.png)
![utils](https://storage.googleapis.com/nfl-player-data/utils.png)
![roster managers](https://storage.googleapis.com/nfl-player-data/rosterManagers.png)
<br />

- Click edit
- This links the different rosters to the correct manager. Each row corresponds to a different roster. For a 12 team league, it should look like this:
```
export const rosterManagers = {
    // the 1 here corresponds to the roster ID (roster 1)
    // the 0 is the manger
    (1st manager is manager 0, second is manager 1, etc.)
    1: 0,
  
    // the 2 here corresponds to the roster ID (roster 2)
    // the 1 is the manger
    (2nd manager is manager 1, third is manager 2, etc.)
    2: 1,
  
    // same for the below. Make sure that each roster
    // corresponds to the correct manager. If there are
    // co-managers for a team, choose one "primary" manager
    3: 2,
    4: 3,
    5: 4,
    6: 5,
    7: 6,
    8: 7,
    9: 8,
    10: 9,
    11: 10,
    12: 11,
};
```
- When you're done, scroll down and click `Commit changes`
- Go back to your league website tab, wait a minute or two, and then refresh. Now you'll have a Managers tab (located in `LEAGUE INFO` on desktop)
- Click on `Managers` and you'll see all the managers you just added

![managers preview](https://storage.googleapis.com/nfl-player-data/managersRendered.png)

## III. Wrapping up

- That's it. You've built out your own league website!
- If you and your league like League Page, please consider <b><a href="https://www.buymeacoffee.com/nmelhado" target="_blank">donating</a></b> (and encouraging your league-mates to too!)
<div align="center">
    <a href="https://www.buymeacoffee.com/nmelhado" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-green.png" alt="Buy Me A Coffee" style="height: 60px !important; width: 217px !important;" width="217px" height="60px" ></a>
</div>

- **If you run into any issues**, go back to [the original League Page repo](https://github.com/nmelhado/league-page) and click on [`Issues`](https://github.com/nmelhado/league-page/issues)

<br>
<br>