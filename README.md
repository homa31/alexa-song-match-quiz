# Alexa "Song Match" Quiz
![](images/ReadMeBanner.png)

Alexa quiz created using JavaScript and Node.js in the Alexa Developer Console

## Table of Contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Design Choice](#design-choice)
* [Supported Artists](#supported-artist)
* [Bonus](#bonus)

## General info
This quiz matches the user to a song of their artist of choice based on their selections in the Alexa environment.

## Technologies
Project is created with:
* JavaScript
* Node.js
* Alexa Developer Console

## Setup
* Open Alexa Developer Console and paste lambda/custom/index.js into the corresponding file, other files were unchanged.
* Set up the necessary intents shown in models/en-US.json.

## Features
* Starts a "Song Match" quiz.
* Asks another artist if the artist provided is not supported.
* Asks a series of questions and matches a song.
* Provides a list of commands.
* Repeats the last statement.
* Stops the quiz.

## Design Choice
* The instructions are not automatically provided in the beginning since many people know the rules already.
* Alexa will respond differently to the same utterances depending on whether in quiz or not.
* AMAZON.Musician was not used due to many unwanted utterance conflicts.
* ArtistAnswerIntentHandler takes into account QuizAnswerIntent because it priortises QuizAnswerIntent when an unknown musician is heard.
* AMAZON.NavigateHomeIntent not implemented because restarting game yield similar results and instruction can be get at anytime.
* The output of FallBackIntentHandler won't be repeated by the RepeatIntent because it isn't helpful to get the user back on track.

## Supported Artists
* Ariana Grande
* Jason Mraz
* Train
* Pentatonix
* Bon Jovi
* More to be added...

## Bonus
* Try saying "Volley, volley, volley"!
