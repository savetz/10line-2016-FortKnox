# 10line-2016-FortKnox
Fort Knox game in Turbo BASIC XL for Atari 8-bit. Entry for 2016 10-line BASIC contest

My second entry in the 2016 10-line BASIC program contest is FORTKNOX, in which you steal treasure away from robot guards.

Move the joystick to collect the diamonds, avoiding the robot guards. When your timer runs out, the game ends. Touching a guard decreases your timer dramatically; getting a diamond increases it a little. Your final score is the maximum amount the timer attained during the game. There are 9 levels: as they increase, the guards do more damage (decreasing your time more dramatically) and there are fewer prizes to increase your time.

I was having a lot of trouble with TurboBasic XL’s tokenizer on very long lines - for both this program and CABBAGE before it. This isn’t a problem I remember having in previous years of doing this contest. If I understand it correctly, TBXL can choke on very compacted, but long program lines. Even though a line is under the limit of 120 characters, if the number of tokens it takes to store that line exceeds some internal limit, TBXL freaks out with a crash or by scrambling the program in memory. I mentioned this program on the AtariAge forum, and someone pointed me to [TurboBasic XL parser tool](https://atariage.com/forums/topic/238422-my-basic-parsing-and-transformation-tool/), a program (which runs on a modern computer) that parses and tokenizes TBXL programs. There wasn’t a Mac version, so someone made a binary for me. (The Atari community is pretty incredible.) So I was able to write this program in BBEDIT, let TurboBasic XL parser tool create the tokenized BAS file, and import that into Atari800MacX for testing.

Not only does this program let me avoid the TBXL tokenizing bug, it produces more compact BASIC programs than I’ve been able to (making smart use of abbreviations, for instance), allowing me to squeeze in more features than I’d be able to with it, and taking away the tedious task of compressing programs by hand.

Update: Turns out that the parse tool can create extra-long BASIC lines (up to 256 characters) and does so by default – so I accidently made this game with 256-line characters instead of the usual 120-character limitation. Which is fine, it just puts the game in a different category for the contest. It also explains why I was able to pack in so much, so easily. Next time I’ll know to use the -s option to force shorter BASIC lines. If I so choose :)

Line-by-line code breakdown at https://atariaction.tumblr.com/post/138055691187/fortknox
