## James Wright
## _Project Proposal_

#### Section 1

The propsed app is called _Beat the Count_.  The app is based on the game 21 or BlackJack.  The user can choose the number of decks in the shoe (1, 2, or 6) and a difficulty (easy, medium, or hard).  The difficulty determines the "count" or the ratio of high cards to low cards where the game provides less and less hints (as to the count) per succesive turns.  Apps such as _Card Counter_  is available on IOS and Android  ([Card Counter](https://games.tmsoft.com/cardcounter/)).

#### Section 2

##### Section 2.1

The app will feature three screens.  The first screen is the main menu.  This screen contains buttons for a new game,  to a resume game, and to navigate to highscores screen.  the second screen is the table.  This screen is where the game takes place.  Cards are dealt to the player (first person view) and the dealer (opposed to the player).  Buttons to hit, stand, double, split, count, and quit are at the bottom of the screen.  The third screen is a highscores screen connected to the apps server.  This screen will be a scrollable list where the top scores are listed and the user position will be listed at the bottom of the screen.

##### Section 2.2

The app will use an SQLite database to store relevant data. For example, if is a game is terminated, current play state can be saved or resumed through a variety of methods.  Data can also be retrieved from the database to be posted to the highscores page once the game is completed.

##### Section 2.3

The app will be connected to another SQL Database on a server that will update highscores viewable via a list through the app.

#### Section 3
##### View  - Model - Controller

##### Screen 1

Model: 

>Database Class (contains game data)
Blackjack Class (contains games mechanics algorithms)
Highscores Class (contains list of highscores updated via game completion)

View:

>TextView Buttons for New Game, Resume Game, and High Score
ImageView for Main Menu Logo

Controller:

>setOnClickListener for new game to delete previous games data and to access view for screen 2 (game table)
setOnClickListner for resume game to access view for screen 2 (game table)
setOnClickListner for view for screen 3 (high score)

#### Screen 2
Model:
>enums for suit, rank
class for cards
class for decks
class for hands
class for blackjack
deck(s) made of arraylist of cards
methods to shuffle, dealCard, hit, stand, canDouble, canSplit, double, split, hiOrLow, highscore etc.

View
> TextView Button for hit, stand, double(linked to canDouble), split(linked to canSplit, count, and quit
ImageView image of card being dealt  (way to deal with dealers unrevealed card to be determined)
ImageView image of poker table with dealer

Controller
>setOnClickListner for hit, stand, etc 
setOnClickListner for Quit to save data and return to main menu view

#### Screen 3

Model
>SQL database on external server updates player data if new High Score reached

View
> recyclerList of high score database
TextView of users high score on bottom of screen
TextView of button to exit to menu

Controller
>  onScrollListner for recyclerView
> ImageView for Player high score





