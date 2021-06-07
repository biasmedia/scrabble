# Scrabble

Learning React Native with a Scabble Help App

## Design Goals

Create an mobile application which will act as a Scrabble dictionary.

- [ ] Allow "Starts with" word searches
- [ ] Display a page of all the 2 letter word variants
- [ ] Expand "Starts with" word searches
    - Thinking the least cheater version would be I have "1 unknown letter" after this "starts with" section plus these n letters to work with and filtering words by that
- [ ] Handle wild letters?
- [ ] Rename things to be not a trademark word "Scrabblee"/"Scrabbly"/etc.

After that we could do:

- "cheater mode" features
- Port to web
- Other: Clone the game networking
- Other: Computer vision fun

### "Cheater Mode"

- [ ] Allow a "cheater mode" lock where the person you're versing in Scrabble could lock out the "cheater mode" features for say "1 hour" with a password to release early
- [ ] Allow "contains" word searches
- [ ] Allow "best possible word" searches for ultimate memes
- [ ] Allow toggling of Scrabble word databases

### Port to Web

Recreate the core functionality as a hosted webpage and try to share as much of the logic as possible.

### Other Stretch

- Build a Scrabble clone so we could challenge people in the applicaiton?
    - Would allow the team to experiement with networking and distributed state
- Find best move on board option
    - Have a vision of the current Scrabble board state within the app. Combine this with the current letters in the players hand. The app will "search" for the highest point plays and show them to you.
    - This requires building a fully working local scrabble game (~half the work of the Scrabble clone). Then implementation of a clasification and search algorithm to do the points calculations.
- Build a computer vision pipeline to "take image of scrabble board" and parse the board into vertual Scrabble board to run through the above cheater options quicker
- Build a Scrabble help keyboard/display over widget for usage with "Words with Friends" or the other Scrabble apps instead of having to app switch

## Technology

We want to use React Native because:

- Targets easily both Android and iOS
- Allows development on Windows and MacOS
- Has good industry adoption
- Empowers our existing React experience

Other technologies considered:

- Native (iOS and Android)
    - Con: Adds extra development work with no added business benefit. There aren't performance concerns with our envisioned views.
- Flutter
    - Pro: David Soller (@3ygun) thought it was nicer to get started with last demo application he built.
    - Con: Less industry addoption then React Native so long term learning benefits were percieved as less valuable.

## Research and Prior Art

How do we get a Scrabble dictionary?

- [Has the dictionary and is Apache 2](https://github.com/edlerd/scrabble)
- [Supposedly this is the Scrabble list](https://en.wikipedia.org/wiki/Collins_Scrabble_Words)
    - [pdf version](https://www.wespa.org/csw19ik.pdf)
    - Found from [Dart Scrabble](https://github.com/pohara60/dart-scrabble)

Other apps?

- [Marriam Webster's Website Verson](https://scrabble.merriam.com/words/start-with/an)
    - Doesn't seem mobile friendly
- [Word Cheats (for Scrabble)](https://apps.apple.com/us/app/word-cheats-for-scrabble/id1479634673)
- [Descrambler](https://apps.apple.com/us/app/descrambler-word-game-cheat/id352148853)
    - This is the application with the cheat mode that Julia uses

## Troubleshooting

### Failures During `npx react-native run-ios`

> The following build commands failed: PhaseScriptExecution [CP-User]\ Generate\ Specs /Users/3ygun/Library/Developer/Xcode/DerivedData/Scrabblee-agevzmqjmpvvahdfnozdcrxikbsd/Build/Intermediates.noindex/Pods.build/Debug-iphonesimulator/FBReactNativeSpec.build/Script-7FB7093881F8ED55A76C2B4940D47D19.sh

[My StackOverflow Comment](https://stackoverflow.com/a/67865377/6480404)
