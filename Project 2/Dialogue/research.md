#### Getting dialogue into a game

- Assets and tools needed
- Gameplay systems for dialogue
- Dynamic dialogue systems -> Game state
- Localization



Dialogue is inherently interaced with gameplay. Programming dialogue is an iterative process, as with any other game mechanic. You should experiment with dialogue and ask yourself questions such as: "do I even need voice acting?".

##### Key concepts:

- Dialogue line: A single line of dialogue that a character can use. Indivisible unit.
- Dialogue database: A centralised database of all the dialogue lines in the game. This provides a ground truth for all the people involved in the game to pull from.
  - Each line should contain information for the character saying the line, the line text itself, audio, an ID to identify this line...
  - It's good to organize the database into game zones and cutscenes.
  - This database can be easily created using Google Sheets or similar alternatives.
  - It's a good idea to format line IDs so they are readable by humans as it can help developers when debugging. One good example is ```<scene code><line number><character code>```, which would produce IDs such as ```CASTLE01OSCAR```.
  - This database can then be loaded directly into the same as to not store data in code.
  - One good thing about using IDs as identifiers for lines is that localization is just a matter of storing the text for different languages and choosing the correct one on runtime.

##### How do we play a line?

A central 

##### Localization:

- You must make sure the fonts you are using contain all the characters for the language.
- Make sure you use the right encoding.
- Some language dialects differ very much between each other. Eg: A person from Portugal will probably rather play the English version of a game than the Brazilian Portuguese localized version.
- Account for languages with very long words as they may not fit all UI elements.
- Chinese, Japanese, Korean and Thai use different punctuation rules, be careful when implementing line breaks.
- For Chinese characters, only include the glyphs used in your game.



10:33



[1]: https://www.youtube.com/watch?v=0hMiPBe_VRc	"Dialogue Systems in Double Fine Games"



