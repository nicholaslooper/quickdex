# QuickDex

QuickDex is a tool that helps you track every Pokemon species you have captured, including form variations. Can be used to track a Living Dex, Shiny Dex, Vivillon Patterns, Unown Letters, Alcremie Flavors, Regional Forms, and more!

Data is saved in local storage on the browser. Progress will not be saved if opened in an incognito or private window.

## Installation

There is nothing to install, simply download the files and open the HTML file in a browser. The project consists of only an HTML, CSS, and Javascript file and the sprites. That's it! No dependencies.

## Quick Guide

Simply click on a Pokemon you have caught and it will be marked as caught. The running count for the number of Pokemon captured is displayed at the top. Different categories/dexes can be accessed through the hamburger menu on the top right. 

To quickly mark all Pokemon within a category as caught or uncaught, click on the option button (...) and click on "Mark all Pokemon as caught" or "Mark all Pokemon as uncaught". 

The National Dex has a special option which allows you to mark a range as caught or uncaught. Type in the number you want to start on in the first box and the number you want to end on in the second box. Example: Typing 1 and 25 will toggle the caught status of every Pokemon #001-#025 (Bulbasaur through Pikachu).

You can filter the Pokemon in each category by their caught status by clicking on the "Caught" "Uncaught" or "All" buttons or by clicking the "Filter" button and selecting an option on mobile devices.

You can search for Pokemon by name using the search bar. This is especially useful for the National Dex. The search is NOT case sensitive and will return partial matches (Example: Searching "meow" will return Meowth, Glameow, and Meowstic).

QuickDex can be turned into a shiny dex by turning on the "Shiny Sprites" switch in the hamburger menu.

Spreadsheets of your progress can be downloaded by clicking on the "Export Spreadsheet" button in the hamburger menu and selecting the categories you want included in the spreadsheet.

You can clear your saved data by clicking the "Clear Data" button in the hamburger menu.

## Usage

In the script file, each category/dex consists of an array of objects with each object representing a Pokemon. Pokemon can be added to a category by following this format:
```
{name:"Pokemon Name", number:"000", caught: false, id: "pokemon-name", sprite: "pokemon-name.png"}
```
Example: 
```
{name:"Bulbasaur", number:"001", caught: false, id: "bulbasaur", sprite: "bulbasaur.png"}
```
The sprite value **MUST** match the file name of the sprite image to work.

The number should be a string, especially if it is less than 100 so that the leading zeroes will display. 

New Pokemon entries (objects) **MUST** be added to the end of the category/dex. The script will check the length of the category array saved in local storage (if any) against the array in the script. If the script array is longer, the extra entries will be pushed to the saved array. The array will then be sorted by number.

If you run into any problems or errors when adding new Pokemon entries, it may be helpful to clear the local storage data by clicking on the "Clear Data" button in the hamburger menu.

## Acknowlegments

In memory of my cat Monkey who would sleep near my desk while I was working on this project.

Pokemon sprites from [PokeSprite](https://github.com/msikma/pokesprite) by [msikma](https://github.com/msikma)

## License

Pokemon sprites, characters, and names are property of Nintendo/Creatures Inc./GAME FREAK Inc.
The code is open-source under the MIT license.