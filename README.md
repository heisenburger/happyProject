The Happy Project :)
====================

Happy Project was initiated as a part of the first iteration of WellyHack. It currently contains a welcome screen and the beginnings of a game screen. It is the first app that we have worked on so it is quite rudimentary!

Proposed Structure
------------------

MainActivity
+ Checks if this is the first time the app has been started. If it is, go to TutorialActivity. If not, show homeFragment
+ homeFragment contains:
  + infoFragment - A happyface icon that pops up app info on tap
  + graphFragment - An (interactive?) graph of your previous scores
  + inspireFragment - An inspirational happy quote :)
  + startNewGame button - go to GameActivity
  
GameActivity
+ Starts gameFragment, which contains:
  + timerFragment, which starts and ends with gameFragment
  + pictureFragment, which creates a randomised grid containing 1 random happyface in a random location and 8 other random sadfaces. Generates new grid every time happyface is tapped, until after 8 iterations when which it ends gameFragment and starts endFragment
  + endFragment, which displays the number of the stopped timer, save the result, and has links to:
    + restart GameActivity
    + go back to MainActivity
    
TutorialActivity
+ Starts when MainActivity calls it (on first time user opens app). Displays welcome message "Find the happy face!" with start button, which starts
  + timerFragment
  + tutorialFragment, which has 4 preset grids with helper color overlays, that get more transparent with each new grid
  + endFragment
  
