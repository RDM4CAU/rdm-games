<!--

author:   Britta Petersen
email:    b.petersen@rz.uni-kiel.de
version:  0.1
language: en
narrator: English female

icon:     

comment: Exploring online computer games on RDM topics in a playful manner.

-->

# Escape the PLAYplex 🤹

<script>
if (!window.globalTimerStarted) {

  window.globalTimerStarted = true;

  // Timer-Container erzeugen
  const timerDiv = document.createElement("div");
  timerDiv.id = "globalTimer";
  timerDiv.style.position = "fixed";
  timerDiv.style.top = "10px";
  timerDiv.style.right = "20px";
  timerDiv.style.fontSize = "20px";
  timerDiv.style.fontWeight = "bold";
  timerDiv.style.background = "white";
  timerDiv.style.padding = "10px 14px";
  timerDiv.style.borderRadius = "8px";
  timerDiv.style.boxShadow = "0 0 8px rgba(0,0,0,0.2)";
  timerDiv.style.zIndex = "9999";
  timerDiv.innerHTML = "⏳ Time left: 20:00";

  document.body.appendChild(timerDiv);

  let duration = 20 * 60; // 20 Minuten

  const timer = setInterval(function () {

    let minutes = Math.floor(duration / 60);
    let seconds = duration % 60;
    seconds = seconds < 10 ? "0" + seconds : seconds;

    timerDiv.innerHTML = "⏳ Time left: " + minutes + ":" + seconds;

    if (--duration < 0) {
      clearInterval(timer);
      timerDiv.innerHTML = "⛔ Time is up!";
      timerDiv.style.background = "#ffcccc";
    }

  }, 1000);
}
</script>

>**Welcome, data enthusiast!**<!-- style="font-size:32px" -->

>> You have been appointed **Gamification Officer** and are expected to present a RDM-related game at an upcoming online meeting.
>
> - You are supposed to fill a gap of about 20-30 minutes with an **online game** between two presentations. Thus, there won't be much time for playing. You need an online game that can be played through in **5 to 15 minutes**, or from which a meaningful part can be played through in 5-15 minutes.
>
> - You don't know exactly what kind of device the participants will be using. You have been told that there will also be tablet and smartphone users.
>
> - Unfortunately, a suitable game has not yet been selected.
> 
>>***Fortunately, you are here now!*** :-)

---

## 🗣️ System Log

> *“Gamification increases engagement of learners, right?!”*  
>
> *“Games are fun, right?”*  
>
> *“So, now you'll have fun and learn about some RDM-related games at the same time.”*
>
> **“Have some fun!”** :-)

---

To exit the system, you must **visit some existing RDM games**  
and feed the system with some *reflection*.

▶️ *We have 20 min, including this introduction.*  

▶️ *There is no single correct path.*

▶️ *There may be wrong or not fully correct answers.*

▶️ *Wrong or not fully correct answers cost time.*

▶️ *You may ***only select one checkbox at a time***, even if the system allows you to select multiple checkboxes simultaneously.*

# Start

>**TASK 💡🤹**
>
>**To select a game for your session, you need to know where to look for such a game... How do you proceed?**

- [ ] I know everything and don't need any further information.
- [ ] I will check forschungsdaten.info.
- [ ] I will use Google.
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## All right. Go on here:

* [No help needed](#No-help)
`)
  } else if (choice === 1) {
    send.liascript(`## Fine. Go on here:

* [forschungsdaten.info](#forschungsdaten.info)
`)
  } else if (choice === 2) {
    send.liascript(`## Why not? Go on here:

* [Google](#Google)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## No help

**You know everything! That is great! Let us move on.**

>**TASK 💡🤹**
>
>**Which statement best reflects your attitude right now?**

- [ ] I am bored.
- [ ] I hate games. 
<script output="tasks">"@input"</script>

<script style="width: 100%">
try {
  let task = @input(`tasks`) // interpret the output="tasks"

  if (task[0]) {
    send.liascript(`## You are bored. Okay...

You can play this little game, but there is no information on RDM games in it...

<iframe src="https://archive.org/embed/chenall_dyna" width="560" height="384" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" allowfullscreen></iframe>

You can also go back to

* [Start](#Start)

`)
  
  } else if (task[1]) {
    send.liascript(`## You hate games? May be, you want to read instead?

* [Read](#Read)

You can also go back to

* [Start](#Start)

  `)
  
  } else if (task[2]) {
    send.liascript(`## I will use Google.

Ok Cool. Go on here:

* [Google](#Google)`)
  
  } else {
    send.clear()
  }

} catch(e) { }
</script>

You can also go back to

* [Start](#Start)

## Read

Okay, you don´t like games...
---

***You may also read an interesting article on an rdm related games:***

- https://series.publisso.de/index.php/de/journals/mbi/volume24/mbi000607

- https://www.zbw-mediatalk.eu/de/2022/02/horror-forschungsdatenmanagement-4-best-practice-beispiele-fuer-gelungene-gamifications/

<br>

You can also go back to

* [Start](#Start)

## forschungsdaten.info

Nice! [forschungsdaten.info](https://forschungsdaten.info) is a good place to start.
---

However the overview of games related to FDM is a bit hidden. You can find it here:

- https://forschungsdaten.info/praxis-kompakt/spiele-mit-fdm-bezug/

>**TASK 💡🤹**
>
>Which of the games listed as **discipline-specific games** (Disziplinspezifische Spiele) is marked as **online game**?

- [ ] Daten im Fadenkreuz
- [ ] Digital Data Stories
- [ ] Research Data Scary Tales - Biodiversity Edition
- [ ] MaRDI Station: Data Quest
<script output="tasks">"@input"</script>

<script style="width: 100%">
try {
  let task = @input(`tasks`) // interpret the output="tasks"

  if (task[0]) {
    send.liascript(`## Daten im Fadenkreuz?

No. This is a concept for an interactive exhibition.`)

  } else if (task[1]) {
    send.liascript(`## Digital Data Stories?

That's not right. :-(`)

  } else if (task[2]) {
    send.liascript(`## Research Data Scary Tales - Biodiversity Edition?

Hmm, this game can be played online, but it is not labeled as an online game.`)

  } else if (task[3]) {
    send.liascript(`## MaRDI Station: Data Quest

That's right! You're looking for an online game. Here's one. Perfect! 🏆

[Have a closer look at the game here!](#mardi-data-quest)`)

  } else {
    send.clear()
  }

} catch(e) { }
</script>

## Google

Okay, than let us perform a Google search!

>**TASK 💡🤹**
>
>What is the hosting page of your first match when performing a Google search for `spiele mit fdm bezug`?

- [ ] [Deutsche Nationalbibliothek](https://www.dnb.de/DE/Home/home_node.html)
- [ ] [Forschungsdaten.org](https://www.forschungsdaten.org/)
- [ ] [Forschungsdaten.info](https://www.forschungsdaten.info/)
- [ ] [RDA Deutschland](https://www.rda-de.de/)
<script output="tasks">"@input"</script>

<script style="width: 100%">
try {
  let task = @input(`tasks`) // interpret the output="tasks"

  if (task[0]) {
    send.liascript(`## Deutsche Nationalbibliothek?

No. ❌`)

  } else if (task[1]) {
    send.liascript(`## Forschungsdaten.org?

Close, but that's still not right. :-(`)

  } else if (task[2]) {
    send.liascript(`## Forschungsdaten.info?

That's right! You will find a list of rdm related games there. Perfect! 🏆

Go on here: 
[forschungsdaten.info](#forschungsdaten.info).`)

  } else if (task[3]) {
    send.liascript(`## RDA Deutschland?

That is not the right solution. Try again!`)

  } else {
    send.clear()
  }

} catch(e) { }
</script>

## MaRDI Data Quest

All right. Let us have a look at this game. It may be a good choice for your session!

Try the game here: [MaRDI Data Quest](https://datalove.imaginary.org/) and answer the quiz:

>**TASK 💡🤹**
>
>Can you play through the game or a meaningful portion of it in a maximum of 15 minutes?

- [ ] No
- [ ] No clue
- [ ] Yes
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No?

* Start the game again! What time limit does it have?
`)
  } else if (choice === 1) {
    send.liascript(`## No clue?

* Start the game! What time limit does it have?
`)
  } else if (choice === 2) {
    send.liascript(`## Yes?

* Right :-) Great! You are a hero! 🏆

[Have a closer look at MaRDI Data Quest](#mardi-data-quest-II)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## MaRDI Data Quest II

>**TASK 💡🤹**
>
>You need a game with little technical requirements. What are the technical requirements of the [MaRDI Data Quest](https://datalove.imaginary.org/) game?

- [ ] No technical requirements at all
- [ ] The game needs to be installed
- [ ] Just a browser needed
- [ ] Browser and a keyboard needed
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No technical requirements at all?

* How do you play the game? Have a look again.
`)
  } else if (choice === 1) {
    send.liascript(`## Installation needed?

* This version is running in the browser without a need to install, isn´t it?
`)
  } else if (choice === 2) {
    send.liascript(`## Just a browser?

* Really? Try to play the game with your smartphone. Does it work?
`)
  } else if (choice === 3) {
    send.liascript(`## Browser and keyboard?

* That is right. You are a hero! 🏆
* Check out some other game: [RDM Adventures](#rdm-adventures)
* Go to [Finish](#Finish)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## RDM Adventures

**Now, let us have a look at** [**RDM Adventures**](https://rdm-games.gitlab.io/rdm-adventure/)

It may be a good choice for your session!

Skip the introduction and play straight away here! 

[**RDM Adventures**](https://rdm-games.gitlab.io/rdm-adventure/)

>**TASK 💡🤹**
>
>Can you play through the game or a meaningful portion of it in a maximum of 15 minutes?

- [ ] No
- [ ] No clue
- [ ] Yes
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No?

* It will not be possible to play through the entire game within 15 Min, but you could choose one chapter as a meaningful portion to play during your session.
`)
  } else if (choice === 1) {
    send.liascript(`## No clue?

* Start the game and just try one chapter of the game!
`)
  } else if (choice === 2) {
    send.liascript(`## Yes?

* You can choose a meaningful chapter to play during your session! So, yes is correct. :-)  You are a hero! 🏆

[Go on checking out RDM Adventures](#rdm-adventures-II)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## RDM Adventures II

>**TASK 💡🤹**
>
>What are the technical requirements for playing [**RDM Adventures**](https://rdm-games.gitlab.io/rdm-adventure/)?

- [ ] No technical requirements at all
- [ ] The game needs to be installed
- [ ] Just a browser needed
- [ ] Browser and a keyboard needed
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No technical requirements at all?

* How do you play the game? Have a look again.
`)
  } else if (choice === 1) {
    send.liascript(`## Installation needed?

* The game is running in the browser, isn´t it?
`)
  } else if (choice === 2) {
    send.liascript(`## Just a browser?

* That is right. You are a hero! 🏆
* You still have time? Check out some other game: [Data Management - The Game](#Data-Management---The-Game)
* Go to [Finish](#Finish)
`)
  } else if (choice === 3) {
    send.liascript(`## Browser and keyboard?

* Try to play the game with your smartphone. It should work. Doesn´t it?
* You may check out some other game: [Data Management - The Game](#Data-Management---The-Game)
* Go to [Finish](#Finish)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## Data Management - The Game

**Now, let us have a look at** [**Data Management - The Game**](https://sites.google.com/view/data-management-the-game/home)

It may be a good choice for your session!

Try one of the two possible options and play straight away here:

[**Data Management - The Game**](https://sites.google.com/view/data-management-the-game/home)

>**TASK 💡🤹**
>
>Can you play through the game or a meaningful portion of it in a maximum of 15 minutes?

- [ ] No
- [ ] No clue
- [ ] Yes
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No?

* Start the game and try one option of the game!
`)
  } else if (choice === 1) {
    send.liascript(`## No clue?

* Start the game and try one option of the game!
`)
  } else if (choice === 2) {
    send.liascript(`## Yes?

* Yes this is correct. Both options are playable is a short time. :-)  You are a hero! 🏆

[Go on checking out Data Management - The Game](#data-management---the-game-ii)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

## Data Management - The Game II

>**TASK 💡🤹**
>
>What are the technical requirements for playing [**Data Management - The Game**](https://sites.google.com/view/data-management-the-game/home)?

- [ ] No technical requirements at all
- [ ] The game needs to be installed
- [ ] Just a browser needed
- [ ] Browser and a keyboard needed
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## No technical requirements at all?

* How do you play the game? Have a look again.
`)
  } else if (choice === 1) {
    send.liascript(`## Installation needed?

* The game is running in the browser, isn´t it?
`)
  } else if (choice === 2) {
    send.liascript(`## Just a browser?

* That is right. You are a hero! 🏆
* You still have time? May be you can read an article: [Read](#read)
* Go to [Finish](#Finish)
`)
  } else if (choice === 3) {
    send.liascript(`## Browser and keyboard?

* Try to play the game with your smartphone. It should work. Doesn´t it?
* You still have time? May be you can read an article: [Read](#read)
* Go to [Finish](#Finish)
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

# Finish

Okay, we playfully explored some RDM-related online games you could use for your session now.

Here is a reminder on the prerequisites:

1. You are looking for an online game.
2. You need a game with very little technical requirements.
3. You don´t have a lot of time. It must be possible to play the entire game or a chapter within aprox 15 Min.
4. You know that you will have smartphone/tablet users in your audience and everybody should be able to play the game individually.

>**TASK 💡🤹**
>
>**Which of the games do you choose for you session?**

- [ ] [MaRDI Data Quest](https://datalove.imaginary.org/)
- [ ] [Research Data Management Adventure](https://rdm-games.gitlab.io/rdm-adventure/)
- [ ] [Data Management - The Game](https://sites.google.com/view/data-management-the-game/home)
- [ ] Non of them. I´ll prepare something myself.
<script output="choice">"@input"</script>

<script style="width: 100%">
try {
  let choice = @input(`choice`).indexOf(true)

  if (choice === 0) {
    send.liascript(`## MaRDI Data Quest?

Well, it is a nice game and it does match quite some prerequisites, but you need a keyboard to be able to play it. Thus smartphone or tablet users will not be able to play.

`)
  } else if (choice === 1) {
    send.liascript(`## Research Data Management Adventure?

This seems to be a good choice! The game can be played in a browser and you don´t even need a keyboard. Thus the games can also be played by smartphone or tablet users.

In order to keep in time, you choose to play only one chapter of the game during your session.

`)
  } else if (choice === 2) {
    send.liascript(`## Data Management - The Game

* Text text tex
`)
  } else if (choice === 3) {
    send.liascript(`## You´ll prepare something yourself?

* That is cool, too. But be aware that this can eat a lot of your time!
`)
  } else {
    send.clear()
  }
} catch(e) {}
</script>

# Thank you 💝

Thank you very much for your participation!

🏆🏆🏆 You are a hero! 🏆🏆🏆