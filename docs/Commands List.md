You can support the project on patreon: <https://patreon.com/nadekobot> or paypal: <https://paypal.me/Kwoth>

##Table Of Contents
- [Help](#help)
- [Administration](#administration)
- [ClashOfClans](#clashofclans)
- [CustomReactions](#customreactions)
- [Gambling](#gambling)
- [Games](#games)
- [Music](#music)
- [NSFW](#nsfw)
- [Permissions](#permissions)
- [Pokemon](#pokemon)
- [Searches](#searches)
- [Utility](#utility)


### Administration  
Command and aliases | Description | Usage
----------------|--------------|-------
`.resetperms` | Resets the bot's permissions module on this server to the default value. **Requires Administrator server permission.** | `.resetperms`
`.delmsgoncmd` | Toggles the automatic deletion of the user's successful command message to prevent chat flood. **Requires Administrator server permission.** | `.delmsgoncmd`
`.setrole` `.sr` | Sets a role for a given user. **Requires ManageRoles server permission.** | `.sr @User Guest`
`.removerole` `.rr` | Removes a role from a given user. **Requires ManageRoles server permission.** | `.rr @User Admin`
`.renamerole` `.renr` | Renames a role. The role you are renaming must be lower than bot's highest role. **Requires ManageRoles server permission.** | `.renr "First role" SecondRole`
`.removeallroles` `.rar` | Removes all roles from a mentioned user. **Requires ManageRoles server permission.** | `.rar @User`
`.createrole` `.cr` | Creates a role with a given name. **Requires ManageRoles server permission.** | `.cr Awesome Role`
`.rolecolor` `.rc` | Set a role's color to the hex or 0-255 rgb color value provided. **Requires ManageRoles server permission.** | `.rc Admin 255 200 100` or `.rc Admin ffba55`
`.ban` `.b` | Bans a user by ID or name with an optional message. **Requires BanMembers server permission.** | `.b "@some Guy" Your behaviour is toxic.`
`.softban` `.sb` | Bans and then unbans a user by ID or name with an optional message. **Requires KickMembers server permission.** **Requires ManageMessages server permission.** | `.sb "@some Guy" Your behaviour is toxic.`
`.kick` `.k` | Kicks a mentioned user. **Requires KickMembers server permission.** | `.k "@some Guy" Your behaviour is toxic.`
`.deafen` `.deaf` | Deafens mentioned user or users. **Requires DeafenMembers server permission.** | `.deaf "@Someguy"` or `.deaf "@Someguy" "@Someguy"`
`.undeafen` `.undef` | Undeafens mentioned user or users. **Requires DeafenMembers server permission.** | `.undef "@Someguy"` or `.undef "@Someguy" "@Someguy"`
`.delvoichanl` `.dvch` | Deletes a voice channel with a given name. **Requires ManageChannels server permission.** | `.dvch VoiceChannelName`
`.creatvoichanl` `.cvch` | Creates a new voice channel with a given name. **Requires ManageChannels server permission.** | `.cvch VoiceChannelName`
`.deltxtchanl` `.dtch` | Deletes a text channel with a given name. **Requires ManageChannels server permission.** | `.dtch TextChannelName`
`.creatxtchanl` `.ctch` | Creates a new text channel with a given name. **Requires ManageChannels server permission.** | `.ctch TextChannelName`
`.settopic` `.st` | Sets a topic on the current channel. **Requires ManageChannels server permission.** | `.st My new topic`
`.setchanlname` `.schn` | Changes the name of the current channel. **Requires ManageChannels server permission.** | `.schn NewName`
`.prune` `.clr` | `.prune` removes all Nadeko's messages in the last 100 messages. `.prune X` removes last `X` number of messages from the channel (up to 100). `.prune @Someone` removes all Someone's messages in the last 100 messages. `.prune @Someone X` removes last `X` number of 'Someone's' messages in the channel.  | `.prune` or `.prune 5` or `.prune @Someone` or `.prune @Someone X`
`.mentionrole` `.menro` | Mentions every person from the provided role or roles (separated by a ',') on this server. Requires you to have the mention everyone permission. **Requires MentionEveryone server permission.** | `.menro RoleName`
`.donators` | List of the lovely people who donated to keep this project alive.  | `.donators`
`.donadd` | Add a donator to the database. **Bot Owner Only** | `.donadd Donate Amount`
`.autoassignrole` `.aar` | Automaticaly assigns a specified role to every user who joins the server. **Requires ManageRoles server permission.** | `.aar` to disable, `.aar Role Name` to enable
`.languageset` `.langset` | Sets this server's response language. If bot's response strings have been translated to that language, bot will use that language in this server. Reset by using `default` as the locale name. Provide no arguments to see currently set language.  | `.langset de-DE ` or `.langset default`
`.langsetdefault` `.langsetd` | Sets the bot's default response language. All servers which use a default locale will use this one. Setting to `default` will use the host's current culture. Provide no arguments to see currently set language.  | `.langsetd en-US` or `.langsetd default`
`.languageslist` `.langli` | List of languages for which translation (or part of it) exist atm.  | `.langli`
`.logserver` | Enables or Disables ALL log events. If enabled, all log events will log to this channel. **Requires Administrator server permission.** **Bot Owner Only** | `.logserver enable` or `.logserver disable`
`.logignore` | Toggles whether the `.logserver` command ignores this channel. Useful if you have hidden admin channel and public log channel. **Requires Administrator server permission.** **Bot Owner Only** | `.logignore`
`.logevents` | Shows a list of all events you can subscribe to with `.log` **Requires Administrator server permission.** **Bot Owner Only** | `.logevents`
`.log` | Toggles logging event. Disables it if it is active anywhere on the server. Enables if it isn't active. Use `.logevents` to see a list of all events you can subscribe to. **Requires Administrator server permission.** **Bot Owner Only** | `.log userpresence` or `.log userbanned`
`.migratedata` | Migrate data from old bot configuration **Bot Owner Only** | `.migratedata`
`.setmuterole` | Sets a name of the role which will be assigned to people who should be muted. Default is nadeko-mute. **Requires ManageRoles server permission.** | `.setmuterole Silenced`
`.mute` | Mutes a mentioned user both from speaking and chatting. **Requires ManageRoles server permission.** **Requires MuteMembers server permission.** | `.mute @Someone`
`.unmute` | Unmutes a mentioned user previously muted with `.mute` command. **Requires ManageRoles server permission.** **Requires MuteMembers server permission.** | `.unmute @Someone`
`.chatmute` | Prevents a mentioned user from chatting in text channels. **Requires ManageRoles server permission.** | `.chatmute @Someone`
`.chatunmute` | Removes a mute role previously set on a mentioned user with `.chatmute` which prevented him from chatting in text channels. **Requires ManageRoles server permission.** | `.chatunmute @Someone`
`.voicemute` | Prevents a mentioned user from speaking in voice channels. **Requires MuteMembers server permission.** | `.voicemute @Someone`
`.voiceunmute` | Gives a previously voice-muted user a permission to speak. **Requires MuteMembers server permission.** | `.voiceunmute @Someguy`
`.rotateplaying` `.ropl` | Toggles rotation of playing status of the dynamic strings you previously specified. **Bot Owner Only** | `.ropl`
`.addplaying` `.adpl` | Adds a specified string to the list of playing strings to rotate. Supported placeholders: `%servers%`, `%users%`, `%playing%`, `%queued%`, `%time%`, `%shardid%`, `%shardcount%`, `%shardguilds%`. **Bot Owner Only** | `.adpl`
`.listplaying` `.lipl` | Lists all playing statuses with their corresponding number. **Bot Owner Only** | `.lipl`
`.removeplaying` `.rmpl` `.repl` | Removes a playing string on a given number. **Bot Owner Only** | `.rmpl`
`.antiraid` | Sets an anti-raid protection on the server. First argument is number of people which will trigger the protection. Second one is a time interval in which that number of people needs to join in order to trigger the protection, and third argument is punishment for those people (Kick, Ban, Mute) **Requires Administrator server permission.** | `.antiraid 5 20 Kick`
`.antispam` | Stops people from repeating same message X times in a row. You can specify to either mute, kick or ban the offenders. Max message count is 10. **Requires Administrator server permission.** | `.antispam 3 Mute` or `.antispam 4 Kick` or `.antispam 6 Ban`
`.antispamignore` | Toggles whether antispam ignores current channel. Antispam must be enabled.  | `.antispamignore`
`.antilist` `.antilst` | Shows currently enabled protection features.  | `.antilist`
`.slowmode` | Toggles slowmode. Disable by specifying no parameters. To enable, specify a number of messages each user can send, and an interval in seconds. For example 1 message every 5 seconds. **Requires ManageMessages server permission.** | `.slowmode 1 5` or `.slowmode`
`.adsarm` | Toggles the automatic deletion of confirmations for `.iam` and `.iamn` commands. **Requires ManageMessages server permission.** | `.adsarm`
`.asar` | Adds a role to the list of self-assignable roles. **Requires ManageRoles server permission.** | `.asar Gamer`
`.rsar` | Removes a specified role from the list of self-assignable roles. **Requires ManageRoles server permission.** | `.rsar`
`.lsar` | Lists all self-assignable roles.  | `.lsar`
`.togglexclsar` `.tesar` | Toggles whether the self-assigned roles are exclusive. (So that any person can have only one of the self assignable roles) **Requires ManageRoles server permission.** | `.tesar`
`.iam` | Adds a role to you that you choose. Role must be on a list of self-assignable roles.  | `.iam Gamer`
`.iamnot` `.iamn` | Removes a role to you that you choose. Role must be on a list of self-assignable roles.  | `.iamn Gamer`
`.fwmsgs` | Toggles forwarding of non-command messages sent to bot's DM to the bot owners **Bot Owner Only** | `.fwmsgs`
`.fwtoall` | Toggles whether messages will be forwarded to all bot owners or only to the first one specified in the credentials.json file **Bot Owner Only** | `.fwtoall`
`.connectshard` | Try (re)connecting a shard with a certain shardid when it dies. No one knows will it work. Keep an eye on the console for errors. **Bot Owner Only** | `.connectshard 2`
`.leave` | Makes Nadeko leave the server. Either server name or server ID is required. **Bot Owner Only** | `.leave 123123123331`
`.die` | Shuts the bot down. **Bot Owner Only** | `.die`
`.setname` `.newnm` | Gives the bot a new name. **Bot Owner Only** | `.newnm BotName`
`.setstatus` | Sets the bot's status. (Online/Idle/Dnd/Invisible) **Bot Owner Only** | `.setstatus Idle`
`.setavatar` `.setav` | Sets a new avatar image for the NadekoBot. Argument is a direct link to an image. **Bot Owner Only** | `.setav http://i.imgur.com/xTG3a1I.jpg`
`.setgame` | Sets the bots game. **Bot Owner Only** | `.setgame with snakes`
`.setstream` | Sets the bots stream. First argument is the twitch link, second argument is stream name. **Bot Owner Only** | `.setstream TWITCHLINK Hello`
`.send` | Sends a message to someone on a different server through the bot.  Separate server and channel/user ids with `|` and prefix the channel id with `c:` and the user id with `u:`. **Bot Owner Only** | `.send serverid|c:channelid message` or `.send serverid|u:userid message`
`.announce` | Sends a message to all servers' default channel that bot is connected to. **Bot Owner Only** | `.announce Useless spam`
`.reloadimages` | Reloads images bot is using. Safe to use even when bot is being used heavily. **Bot Owner Only** | `.reloadimages`
`.greetdel` `.grdel` | Sets the time it takes (in seconds) for greet messages to be auto-deleted. Set it to 0 to disable automatic deletion. **Requires ManageServer server permission.** | `.greetdel 0` or `.greetdel 30`
`.greet` | Toggles anouncements on the current channel when someone joins the server. **Requires ManageServer server permission.** | `.greet`
`.greetmsg` | Sets a new join announcement message which will be shown in the server's channel. Type `%user%` if you want to mention the new member. Using it with no message will show the current greet message. You can use embed json from <http://nadekobot.xyz/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.greetmsg Welcome, %user%.`
`.greetdm` | Toggles whether the greet messages will be sent in a DM (This is separate from greet - you can have both, any or neither enabled). **Requires ManageServer server permission.** | `.greetdm`
`.greetdmmsg` | Sets a new join announcement message which will be sent to the user who joined. Type `%user%` if you want to mention the new member. Using it with no message will show the current DM greet message. You can use embed json from <http://nadekobot.xyz/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.greetdmmsg Welcome to the server, %user%`.
`.bye` | Toggles anouncements on the current channel when someone leaves the server. **Requires ManageServer server permission.** | `.bye`
`.byemsg` | Sets a new leave announcement message. Type `%user%` if you want to show the name the user who left. Type `%id%` to show id. Using this command with no message will show the current bye message. You can use embed json from <http://nadekobot.xyz/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Requires ManageServer server permission.** | `.byemsg %user% has left.`
`.byedel` | Sets the time it takes (in seconds) for bye messages to be auto-deleted. Set it to `0` to disable automatic deletion. **Requires ManageServer server permission.** | `.byedel 0` or `.byedel 30`
`.voice+text` `.v+t` | Creates a text channel for each voice channel only users in that voice channel can see. If you are server owner, keep in mind you will see them all the time regardless. **Requires ManageRoles server permission.** **Requires ManageChannels server permission.** | `.v+t`
`.cleanvplust` `.cv+t` | Deletes all text channels ending in `-voice` for which voicechannels are not found. Use at your own risk. **Requires ManageChannels server permission.** **Requires ManageRoles server permission.** | `.cleanv+t`

###### [Back to ToC](#table-of-contents)

### ClashOfClans  
Command and aliases | Description | Usage
----------------|--------------|-------
`,createwar` `,cw` | Creates a new war by specifying a size (>10 and multiple of 5) and enemy clan name. **Requires ManageMessages server permission.** | `,cw 15 The Enemy Clan`
`,startwar` `,sw` | Starts a war with a given number.  | `,sw 15`
`,listwar` `,lw` | Shows the active war claims by a number. Shows all wars in a short way if no number is specified.  | `,lw [war_number]` or `,lw`
`,claim` `,call` `,c` | Claims a certain base from a certain war. You can supply a name in the third optional argument to claim in someone else's place.  | `,call [war_number] [base_number] [optional_other_name]`
`,claimfinish1` `,cf1` | Finish your claim with 1 star if you destroyed a base. First argument is the war number, optional second argument is a base number if you want to finish for someone else.  | `,cf1 1` or `,cf1 1 5`
`,claimfinish2` `,cf2` | Finish your claim with 2 stars if you destroyed a base. First argument is the war number, optional second argument is a base number if you want to finish for someone else.  | `,cf2 1` or `,cf2 1 5`
`,claimfinish` `,cf` | Finish your claim with 3 stars if you destroyed a base. First argument is the war number, optional second argument is a base number if you want to finish for someone else.  | `,cf 1` or `,cf 1 5`
`,endwar` `,ew` | Ends the war with a given index.  | `,ew [war_number]`
`,unclaim` `,ucall` `,uc` | Removes your claim from a certain war. Optional second argument denotes a person in whose place to unclaim  | `,uc [war_number] [optional_other_name]`

###### [Back to ToC](#table-of-contents)

### CustomReactions  
Command and aliases | Description | Usage
----------------|--------------|-------
`.addcustreact` `.acr` | Add a custom reaction with a trigger and a response. Running this command in server requires the Administration permission. Running this command in DM is Bot Owner only and adds a new global custom reaction. Guide here: <http://nadekobot.readthedocs.io/en/latest/Custom%20Reactions/>  | `.acr "hello" Hi there %user%`
`.listcustreact` `.lcr` | Lists global or server custom reactions (20 commands per page). Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions. Specifying `all` argument instead of the number will DM you a text file with a list of all custom reactions.  | `.lcr 1` or `.lcr all`
`.listcustreactg` `.lcrg` | Lists global or server custom reactions (20 commands per page) grouped by trigger, and show a number of responses for each. Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions.  | `.lcrg 1`
`.showcustreact` `.scr` | Shows a custom reaction's response on a given ID.  | `.scr 1`
`.delcustreact` `.dcr` | Deletes a custom reaction on a specific index. If ran in DM, it is bot owner only and deletes a global custom reaction. If ran in a server, it requires Administration privileges and removes server custom reaction.  | `.dcr 5`
`.crstatsclear` | Resets the counters on `.crstats`. You can specify a trigger to clear stats only for that trigger. **Bot Owner Only** | `.crstatsclear` or `.crstatsclear rng`
`.crstats` | Shows a list of custom reactions and the number of times they have been executed. Paginated with 10 per page. Use `.crstatsclear` to reset the counters.  | `.crstats` or `.crstats 3`

###### [Back to ToC](#table-of-contents)

### Gambling  
Command and aliases | Description | Usage
----------------|--------------|-------
`$raffle` | Prints a name and ID of a random user from the online list from the (optional) role.  | `$raffle` or `$raffle RoleName`
`$cash` `$$$` | Check how much currency a person has. (Defaults to yourself)  | `$$$` or `$$$ @SomeGuy`
`$give` | Give someone a certain amount of currency.  | `$give 1 "@SomeGuy"`
`$award` | Awards someone a certain amount of currency.  You can also specify a role name to award currency to all users in a role. **Bot Owner Only** | `$award 100 @person` or `$award 5 Role Of Gamblers`
`$take` | Takes a certain amount of currency from someone. **Bot Owner Only** | `$take 1 "@someguy"`
`$betroll` `$br` | Bets a certain amount of currency and rolls a dice. Rolling over 66 yields x2 of your currency, over 90 - x4 and 100 x10.  | `$br 5`
`$leaderboard` `$lb` | Displays the bot's currency leaderboard.  | `$lb`
`$race` | Starts a new animal race.  | `$race`
`$joinrace` `$jr` | Joins a new race. You can specify an amount of currency for betting (optional). You will get YourBet*(participants-1) back if you win.  | `$jr` or `$jr 5`
`$startevent` | Starts one of the events seen on public nadeko. **Bot Owner Only** | `$startevent flowerreaction`
`$roll` | Rolls 0-100. If you supply a number `X` it rolls up to 30 normal dice. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`. `Y` can be a letter 'F' if you want to roll fate dice instead of dnd.  | `$roll` or `$roll 7` or `$roll 3d5` or `$roll 5dF`
`$rolluo` | Rolls `X` normal dice (up to 30) unordered. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`.  | `$rolluo` or `$rolluo 7` or `$rolluo 3d5`
`$nroll` | Rolls in a given range.  | `$nroll 5` (rolls 0-5) or `$nroll 5-15`
`$draw` | Draws a card from the deck.If you supply number X, she draws up to 5 cards from the deck.  | `$draw` or `$draw 5`
`$shuffle` `$sh` | Reshuffles all cards back into the deck.  | `$sh`
`$flip` | Flips coin(s) - heads or tails, and shows an image.  | `$flip` or `$flip 3`
`$betflip` `$bf` | Bet to guess will the result be heads or tails. Guessing awards you 1.95x the currency you've bet (rounded up). Multiplier can be changed by the bot owner.  | `$bf 5 heads` or `$bf 3 t`
`$slotstats` | Shows the total stats of the slot command for this bot's session. **Bot Owner Only** | `$slotstats`
`$slottest` | Tests to see how much slots payout for X number of plays. **Bot Owner Only** | `$slottest 1000`
`$slot` | Play Nadeko slots. Max bet is 999. 3 seconds cooldown per user.  | `$slot 5`
`$claimwaifu` `$claim` | Claim a waifu for yourself by spending currency.  You must spend atleast 10% more than her current value unless she set `$affinity` towards you.  | `$claim 50 @Himesama`
`$divorce` | Releases your claim on a specific waifu. You will get some of the money you've spent back unless that waifu has an affinity towards you. 6 hours cooldown.  | `$divorce @CheatingSloot`
`$affinity` | Sets your affinity towards someone you want to be claimed by. Setting affinity will reduce their `$claim` on you by 20%. You can leave second argument empty to clear your affinity. 30 minutes cooldown.  | `$affinity @MyHusband` or `$affinity`
`$waifus` `$waifulb` | Shows top 9 waifus.  | `$waifus`
`$waifuinfo` `$waifustats` | Shows waifu stats for a target person. Defaults to you if no user is provided.  | `$waifuinfo @MyCrush` or `$waifuinfo`

###### [Back to ToC](#table-of-contents)

### Games  
Command and aliases | Description | Usage
----------------|--------------|-------
`>choose` | Chooses a thing from a list of things  | `>choose Get up;Sleep;Sleep more`
`>8ball` | Ask the 8ball a yes/no question.  | `>8ball should I do something`
`>rps` | Play a game of Rocket-Paperclip-Scissors with Nadeko.  | `>rps scissors`
`>rategirl` | Use the universal hot-crazy wife zone matrix to determine the girl's worth. It is everything young men need to know about women. At any moment in time, any woman you have previously located on this chart can vanish from that location and appear anywhere else on the chart.  | `>rategirl @SomeGurl`
`>linux` | Prints a customizable Linux interjection  | `>linux Spyware Windows`
`>leet` | Converts a text to leetspeak with 6 (1-6) severity levels  | `>leet 3 Hello`
`>acrophobia` `>acro` | Starts an Acrophobia game. Second argment is optional round length in seconds. (default is 60)  | `>acro` or `>acro 30`
`>cleverbot` | Toggles cleverbot session. When enabled, the bot will reply to messages starting with bot mention in the server. Custom reactions starting with %mention% won't work if cleverbot is enabled. **Requires ManageMessages server permission.** | `>cleverbot`
`>hangmanlist` | Shows a list of hangman term types.  | `> hangmanlist`
`>hangman` | Starts a game of hangman in the channel. Use `>hangmanlist` to see a list of available term types. Defaults to 'all'.  | `>hangman` or `>hangman movies`
`>pick` | Picks the currency planted in this channel. 60 seconds cooldown.  | `>pick`
`>plant` | Spend an amount of currency to plant it in this channel. Default is 1. (If bot is restarted or crashes, the currency will be lost)  | `>plant` or `>plant 5`
`>gencurrency` `>gc` | Toggles currency generation on this channel. Every posted message will have chance to spawn currency. Chance is specified by the Bot Owner. (default is 2%) **Requires ManageMessages server permission.** | `>gc`
`>poll` | Creates a poll which requires users to send the number of the voting option to the bot. **Requires ManageMessages server permission.** | `>poll Question?;Answer1;Answ 2;A_3`
`>publicpoll` `>ppoll` | Creates a public poll which requires users to type a number of the voting option in the channel command is ran in. **Requires ManageMessages server permission.** | `>ppoll Question?;Answer1;Answ 2;A_3`
`>pollstats` | Shows the poll results without stopping the poll on this server. **Requires ManageMessages server permission.** | `>pollstats`
`>pollend` | Stops active poll on this server and prints the results in this channel. **Requires ManageMessages server permission.** | `>pollend`
`>typestart` | Starts a typing contest.  | `>typestart`
`>typestop` | Stops a typing contest on the current channel.  | `>typestop`
`>typeadd` | Adds a new article to the typing contest. **Bot Owner Only** | `>typeadd wordswords`
`>typelist` | Lists added typing articles with their IDs. 15 per page.  | `>typelist` or `>typelist 3`
`>typedel` | Deletes a typing article given the ID. **Bot Owner Only** | `>typedel 3`
`>tictactoe` `>ttt` | Starts a game of tic tac toe. Another user must run the command in the same channel in order to accept the challenge. Use numbers 1-9 to play. 15 seconds per move.  | >ttt
`>trivia` `>t` | Starts a game of trivia. You can add `nohint` to prevent hints. First player to get to 10 points wins by default. You can specify a different number. 30 seconds per question.  | `>t` or `>t 5 nohint`
`>tl` | Shows a current trivia leaderboard.  | `>tl`
`>tq` | Quits current trivia after current question.  | `>tq`

###### [Back to ToC](#table-of-contents)

### Help  
Command and aliases | Description | Usage
----------------|--------------|-------
`-modules` `-mdls` | Lists all bot modules.  | `-modules`
`-commands` `-cmds` | List all of the bot's commands from a certain module. You can either specify the full name or only the first few letters of the module name.  | `-commands Administration` or `-cmds Admin`
`-help` `-h` | Either shows a help for a single command, or DMs you help link if no arguments are specified.  | `-h -cmds` or `-h`
`-hgit` | Generates the commandlist.md file. **Bot Owner Only** | `-hgit`
`-readme` `-guide` | Sends a readme and a guide links to the channel.  | `-readme` or `-guide`
`-donate` | Instructions for helping the project financially.  | `-donate`

###### [Back to ToC](#table-of-contents)

### Music  
Command and aliases | Description | Usage
----------------|--------------|-------
`!!next` `!!n` | Goes to the next song in the queue. You have to be in the same voice channel as the bot. You can skip multiple songs, but in that case songs will not be requeued if !!rcs or !!rpl is enabled.  | `!!n` or `!!n 5`
`!!stop` `!!s` | Stops the music and clears the playlist. Stays in the channel.  | `!!s`
`!!destroy` `!!d` | Completely stops the music and unbinds the bot from the channel. (may cause weird behaviour)  | `!!d`
`!!pause` `!!p` | Pauses or Unpauses the song.  | `!!p`
`!!fairplay` `!!fp` | Toggles fairplay. While enabled, the bot will prioritize songs from users who didn't have their song recently played instead of the song's position in the queue.  | `!!fp`
`!!queue` `!!q` `!!yq` | Queue a song using keywords or a link. Bot will join your voice channel. **You must be in a voice channel**.  | `!!q Dream Of Venice`
`!!soundcloudqueue` `!!sq` | Queue a soundcloud song using keywords. Bot will join your voice channel. **You must be in a voice channel**.  | `!!sq Dream Of Venice`
`!!listqueue` `!!lq` | Lists 15 currently queued songs per page. Default page is 1.  | `!!lq` or `!!lq 2`
`!!nowplaying` `!!np` | Shows the song that the bot is currently playing.  | `!!np`
`!!volume` `!!vol` | Sets the music playback volume (0-100%)  | `!!vol 50`
`!!defvol` `!!dv` | Sets the default music volume when music playback is started (0-100). Persists through restarts.  | `!!dv 80`
`!!shuffle` `!!sh` | Shuffles the current playlist.  | `!!sh`
`!!playlist` `!!pl` | Queues up to 500 songs from a youtube playlist specified by a link, or keywords.  | `!!pl playlist link or name`
`!!soundcloudpl` `!!scpl` | Queue a Soundcloud playlist using a link.  | `!!scpl soundcloudseturl`
`!!localplaylst` `!!lopl` | Queues all songs from a directory. **Bot Owner Only** | `!!lopl C:/music/classical`
`!!radio` `!!ra` | Queues a radio stream from a link. It can be a direct mp3 radio stream, .m3u, .pls .asx or .xspf (Usage Video: <https://streamable.com/al54>)  | `!!ra radio link here`
`!!local` `!!lo` | Queues a local file by specifying a full path. **Bot Owner Only** | `!!lo C:/music/mysong.mp3`
`!!remove` `!!rm` | Remove a song by its # in the queue, or 'all' to remove whole queue.  | `!!rm 5`
`!!movesong` `!!ms` | Moves a song from one position to another.  | `!!ms 5>3`
`!!setmaxqueue` `!!smq` | Sets a maximum queue size. Supply 0 or no argument to have no limit.  | `!!smq 50` or `!!smq`
`!!setmaxplaytime` `!!smp` | Sets a maximum number of seconds (>14) a song can run before being skipped automatically. Set 0 to have no limit.  | `!!smp 0` or `!!smp 270`
`!!reptcursong` `!!rcs` | Toggles repeat of current song.  | `!!rcs`
`!!rpeatplaylst` `!!rpl` | Toggles repeat of all songs in the queue (every song that finishes is added to the end of the queue).  | `!!rpl`
`!!save` | Saves a playlist under a certain name. Playlist name must be no longer than 20 characters and must not contain dashes.  | `!!save classical1`
`!!load` | Loads a saved playlist using its ID. Use `!!pls` to list all saved playlists and `!!save` to save new ones.  | `!!load 5`
`!!playlists` `!!pls` | Lists all playlists. Paginated, 20 per page. Default page is 0.  | `!!pls 1`
`!!deleteplaylist` `!!delpls` | Deletes a saved playlist. Works only if you made it or if you are the bot owner.  | `!!delpls animu-5`
`!!goto` | Goes to a specific time in seconds in a song.  | `!!goto 30`
`!!autoplay` `!!ap` | Toggles autoplay - When the song is finished, automatically queue a related Youtube song. (Works only for Youtube songs and when queue is empty)  | `!!ap`
`!!setmusicchannel` `!!smch` | Sets the current channel as the default music output channel. This will output playing, finished, paused and removed songs to that channel instead of the channel where the first song was queued in. **Requires ManageMessages server permission.** | `!!smch`

###### [Back to ToC](#table-of-contents)

### NSFW  
Command and aliases | Description | Usage
----------------|--------------|-------
`~hentai` | Shows a hentai image from a random website (gelbooru or danbooru or konachan or atfbooru or yandere) with a given tag. Tag is optional but preferred. Only 1 tag allowed.  | `~hentai yuri`
`~autohentai` | Posts a hentai every X seconds with a random tag from the provided tags. Use `|` to separate tags. 20 seconds minimum. Provide no arguments to disable. **Requires ManageMessages channel permission.** | `~autohentai 30 yuri|tail|long_hair` or `~autohentai`
`~hentaibomb` | Shows a total 5 images (from gelbooru, danbooru, konachan, yandere and atfbooru). Tag is optional but preferred.  | `~hentaibomb yuri`
`~yandere` | Shows a random image from yandere with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `~yandere tag1+tag2`
`~konachan` | Shows a random hentai image from konachan with a given tag. Tag is optional but preferred.  | `~konachan yuri`
`~e621` | Shows a random hentai image from e621.net with a given tag. Tag is optional but preferred. Use spaces for multiple tags.  | `~e621 yuri kissing`
`~rule34` | Shows a random image from rule34.xx with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `~rule34 yuri+kissing`
`~danbooru` | Shows a random hentai image from danbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `~danbooru yuri+kissing`
`~gelbooru` | Shows a random hentai image from gelbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `~gelbooru yuri+kissing`
`~cp` | We all know where this will lead you to.  | `~cp`
`~boobs` | Real adult content.  | `~boobs`
`~butts` `~ass` `~butt` | Real adult content.  | `~butts` or `~ass`

###### [Back to ToC](#table-of-contents)

### Permissions  
Command and aliases | Description | Usage
----------------|--------------|-------
`;verbose` `;v` | Sets whether to show when a command/module is blocked.  | `;verbose true`
`;permrole` `;pr` | Sets a role which can change permissions. Supply no parameters to see the current one. Default is 'Nadeko'.  | `;pr role`
`;listperms` `;lp` | Lists whole permission chain with their indexes. You can specify an optional page number if there are a lot of permissions.  | `;lp` or `;lp 3`
`;removeperm` `;rp` | Removes a permission from a given position in the Permissions list.  | `;rp 1`
`;moveperm` `;mp` | Moves permission from one position to another in the Permissions list.  | `;mp 2 4`
`;srvrcmd` `;sc` | Sets a command's permission at the server level.  | `;sc "command name" disable`
`;srvrmdl` `;sm` | Sets a module's permission at the server level.  | `;sm ModuleName enable`
`;usrcmd` `;uc` | Sets a command's permission at the user level.  | `;uc "command name" enable SomeUsername`
`;usrmdl` `;um` | Sets a module's permission at the user level.  | `;um ModuleName enable SomeUsername`
`;rolecmd` `;rc` | Sets a command's permission at the role level.  | `;rc "command name" disable MyRole`
`;rolemdl` `;rm` | Sets a module's permission at the role level.  | `;rm ModuleName enable MyRole`
`;chnlcmd` `;cc` | Sets a command's permission at the channel level.  | `;cc "command name" enable SomeChannel`
`;chnlmdl` `;cm` | Sets a module's permission at the channel level.  | `;cm ModuleName enable SomeChannel`
`;allchnlmdls` `;acm` | Enable or disable all modules in a specified channel.  | `;acm enable #SomeChannel`
`;allrolemdls` `;arm` | Enable or disable all modules for a specific role.  | `;arm [enable/disable] MyRole`
`;allusrmdls` `;aum` | Enable or disable all modules for a specific user.  | `;aum enable @someone`
`;allsrvrmdls` `;asm` | Enable or disable all modules for your server.  | `;asm [enable/disable]`
`;ubl` | Either [add]s or [rem]oves a user specified by a Mention or an ID from a blacklist. **Bot Owner Only** | `;ubl add @SomeUser` or `;ubl rem 12312312313`
`;cbl` | Either [add]s or [rem]oves a channel specified by an ID from a blacklist. **Bot Owner Only** | `;cbl rem 12312312312`
`;sbl` | Either [add]s or [rem]oves a server specified by a Name or an ID from a blacklist. **Bot Owner Only** | `;sbl add 12312321312` or `;sbl rem SomeTrashServer`
`;cmdcooldown` `;cmdcd` | Sets a cooldown per user for a command. Set it to 0 to remove the cooldown.  | `;cmdcd "some cmd" 5`
`;allcmdcooldowns` `;acmdcds` | Shows a list of all commands and their respective cooldowns.  | `;acmdcds`
`;srvrfilterinv` `;sfi` | Toggles automatic deletion of invites posted in the server. Does not affect the Bot Owner.  | `;sfi`
`;chnlfilterinv` `;cfi` | Toggles automatic deletion of invites posted in the channel. Does not negate the `;srvrfilterinv` enabled setting. Does not affect the Bot Owner.  | `;cfi`
`;srvrfilterwords` `;sfw` | Toggles automatic deletion of messages containing filtered words on the server. Does not affect the Bot Owner.  | `;sfw`
`;chnlfilterwords` `;cfw` | Toggles automatic deletion of messages containing filtered words on the channel. Does not negate the `;srvrfilterwords` enabled setting. Does not affect the Bot Owner.  | `;cfw`
`;fw` | Adds or removes (if it exists) a word from the list of filtered words. Use`;sfw` or `;cfw` to toggle filtering.  | `;fw poop`
`;lstfilterwords` `;lfw` | Shows a list of filtered words.  | `;lfw`

###### [Back to ToC](#table-of-contents)

### Pokemon  
Command and aliases | Description | Usage
----------------|--------------|-------
`>attack` | Attacks a target with the given move. Use `>movelist` to see a list of moves your type can use.  | `>attack "vine whip" @someguy`
`>movelist` `>ml` | Lists the moves you are able to use  | `>ml`
`>heal` | Heals someone. Revives those who fainted. Costs a NadekoFlower.   | `>heal @someone`
`>type` | Get the poketype of the target.  | `>type @someone`
`>settype` | Set your poketype. Costs a NadekoFlower. Provide no arguments to see a list of available types.  | `>settype fire` or `>settype`

###### [Back to ToC](#table-of-contents)

### Searches  
Command and aliases | Description | Usage
----------------|--------------|-------
`~weather` `~we` | Shows weather data for a specified city. You can also specify a country after a comma.  | `~we Moscow, RU`
`~youtube` `~yt` | Searches youtubes and shows the first result  | `~yt query`
`~imdb` `~omdb` | Queries omdb for movies or series, show first result.  | `~imdb Batman vs Superman`
`~randomcat` `~meow` | Shows a random cat image.  | `~meow`
`~randomdog` `~woof` | Shows a random dog image.  | `~woof`
`~image` `~img` | Pulls the first image found using a search parameter. Use `~rimg` for different results.  | `~img cute kitten`
`~randomimage` `~rimg` | Pulls a random image using a search parameter.  | `~rimg cute kitten`
`~lmgtfy` | Google something for an idiot.  | `~lmgtfy query`
`~shorten` | Attempts to shorten an URL, if it fails, returns the input URL.  | `~shorten https://google.com`
`~google` `~g` | Get a Google search link for some terms.  | `~google query`
`~magicthegathering` `~mtg` | Searches for a Magic The Gathering card.  | `~magicthegathering about face` or `~mtg about face`
`~hearthstone` `~hs` | Searches for a Hearthstone card and shows its image. Takes a while to complete.  | `~hs Ysera`
`~yodify` `~yoda` | Translates your normal sentences into Yoda styled sentences!  | `~yoda my feelings hurt`
`~urbandict` `~ud` | Searches Urban Dictionary for a word.  | `~ud Pineapple`
`~define` `~def` | Finds a definition of a word.  | `~def heresy`
`~#` | Searches Tagdef.com for a hashtag.  | `~# ff`
`~catfact` | Shows a random catfact from <http://catfacts-api.appspot.com/api/facts>  | `~catfact`
`~revav` | Returns a Google reverse image search for someone's avatar.  | `~revav "@SomeGuy"`
`~revimg` | Returns a Google reverse image search for an image from a link.  | `~revimg Image link`
`~safebooru` | Shows a random image from safebooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `~safebooru yuri+kissing`
`~wikipedia` `~wiki` | Gives you back a wikipedia link  | `~wiki query`
`~color` `~clr` | Shows you what color corresponds to that hex.  | `~clr 00ff00`
`~videocall` | Creates a private <http://www.appear.in> video call link for you and other mentioned people. The link is sent to mentioned people via a private message.  | `~videocall "@SomeGuy"`
`~avatar` `~av` | Shows a mentioned person's avatar.  | `~av "@SomeGuy"`
`~wikia` | Gives you back a wikia link  | `~wikia mtg Vigilance` or `~wikia mlp Dashy`
`~lolban` | Shows top banned champions ordered by ban rate.  | `~lolban`
`~mal` | Shows basic info from a MyAnimeList profile.  | `~mal straysocks`
`~anime` `~ani` `~aq` | Queries anilist for an anime and shows the first result.  | `~ani aquarion evol`
`~manga` `~mang` `~mq` | Queries anilist for a manga and shows the first result.  | `~mq Shingeki no kyojin`
`~yomama` `~ym` | Shows a random joke from <http://api.yomomma.info/>  | `~ym`
`~randjoke` `~rj` | Shows a random joke from <http://tambal.azurewebsites.net/joke/random>  | `~rj`
`~chucknorris` `~cn` | Shows a random Chuck Norris joke from <http://tambal.azurewebsites.net/joke/random>  | `~cn`
`~wowjoke` | Get one of Kwoth's penultimate WoW jokes.  | `~wowjoke`
`~magicitem` `~mi` | Shows a random magic item from <https://1d4chan.org/wiki/List_of_/tg/%27s_magic_items>  | `~mi`
`~memelist` | Pulls a list of memes you can use with `~memegen` from http://memegen.link/templates/  | `~memelist`
`~memegen` | Generates a meme from memelist with top and bottom text.  | `~memegen biw "gets iced coffee" "in the winter"`
`~osu` | Shows osu stats for a player.  | `~osu Name` or `~osu Name taiko`
`~osub` | Shows information about an osu beatmap.  | `~osub https://osu.ppy.sh/s/127712`
`~osu5` | Displays a user's top 5 plays.  | `~osu5 Name`
`~overwatch` `~ow` | Show's basic stats on a player (competitive rank, playtime, level etc) Region codes are: `eu` `us` `cn` `kr`  | `~ow us Battletag#1337` or  `~overwatch eu Battletag#2016`
`~placelist` | Shows the list of available tags for the `~place` command.  | `~placelist`
`~place` | Shows a placeholder image of a given tag. Use `~placelist` to see all available tags. You can specify the width and height of the image as the last two optional arguments.  | `~place Cage` or `~place steven 500 400`
`~pokemon` `~poke` | Searches for a pokemon.  | `~poke Sylveon`
`~pokemonability` `~pokeab` | Searches for a pokemon ability.  | `~pokeab overgrow`
`~hitbox` `~hb` | Notifies this channel when a certain user starts streaming. **Requires ManageMessages server permission.** | `~hitbox SomeStreamer`
`~twitch` `~tw` | Notifies this channel when a certain user starts streaming. **Requires ManageMessages server permission.** | `~twitch SomeStreamer`
`~beam` `~bm` | Notifies this channel when a certain user starts streaming. **Requires ManageMessages server permission.** | `~beam SomeStreamer`
`~liststreams` `~ls` | Lists all streams you are following on this server.  | `~ls`
`~removestream` `~rms` | Removes notifications of a certain streamer from a certain platform on this channel. **Requires ManageMessages server permission.** | `~rms Twitch SomeGuy` or `~rms Beam SomeOtherGuy`
`~checkstream` `~cs` | Checks if a user is online on a certain streaming platform.  | `~cs twitch MyFavStreamer`
`~translate` `~trans` | Translates from>to text. From the given language to the destination language.  | `~trans en>fr Hello`
`~autotrans` `~at` | Starts automatic translation of all messages by users who set their `~atl` in this channel. You can set "del" argument to automatically delete all translated user messages. **Requires Administrator server permission.** **Bot Owner Only** | `~at` or `~at del`
`~autotranslang` `~atl` | Sets your source and target language to be used with `~at`. Specify no arguments to remove previously set value.  | `~atl en>fr`
`~translangs` | Lists the valid languages for translation.  | `~translangs`
`~xkcd` | Shows a XKCD comic. No arguments will retrieve random one. Number argument will retrieve a specific comic, and "latest" will get the latest one.  | `~xkcd` or `~xkcd 1400` or `~xkcd latest`

###### [Back to ToC](#table-of-contents)

### Utility  
Command and aliases | Description | Usage
----------------|--------------|-------
`.rotaterolecolor` `.rrc` | Rotates a roles color on an interval with a list of supplied colors. First argument is interval in seconds (Minimum 60). Second argument is a role, followed by a space-separated list of colors in hex. Provide a rolename with a 0 interval to disable. **Requires ManageRoles server permission.** **Bot Owner Only** | `.rrc 60 MyLsdRole #ff0000 #00ff00 #0000ff` or `.rrc 0 MyLsdRole`
`.togethertube` `.totube` | Creates a new room on <https://togethertube.com> and shows the link in the chat.  | `.totube`
`.whosplaying` `.whpl` | Shows a list of users who are playing the specified game.  | `.whpl Overwatch`
`.inrole` | Lists every person from the provided role or roles, separated with space, on this server. You can use role IDs, role names (in quotes if it has multiple words), or role mention If the list is too long for 1 message, you must have Manage Messages permission.  | `.inrole Role` or `.inrole Role1 "Role 2" @role3`
`.checkmyperms` | Checks your user-specific permissions on this channel.  | `.checkmyperms`
`.userid` `.uid` | Shows user ID.  | `.uid` or `.uid "@SomeGuy"`
`.channelid` `.cid` | Shows current channel ID.  | `.cid`
`.serverid` `.sid` | Shows current server ID.  | `.sid`
`.roles` | List roles on this server or a roles of a specific user if specified. Paginated, 20 roles per page.  | `.roles 2` or `.roles @Someone`
`.channeltopic` `.ct` | Sends current channel's topic as a message.  | `.ct`
`.createinvite` `.crinv` | Creates a new invite which has infinite max uses and never expires. **Requires CreateInstantInvite channel permission.** | `.crinv`
`.shardstats` | Stats for shards. Paginated with 25 shards per page.  | `.shardstats` or `.shardstats 2`
`.shardid` | Shows which shard is a certain guild on, by guildid.  | `.shardid 117523346618318850`
`.stats` | Shows some basic stats for Nadeko.  | `.stats`
`.showemojis` `.se` | Shows a name and a link to every SPECIAL emoji in the message.  | `.se A message full of SPECIAL emojis`
`.listservers` | Lists servers the bot is on with some basic info. 15 per page. **Bot Owner Only** | `.listservers 3`
`.savechat` | Saves a number of messages to a text file and sends it to you. **Bot Owner Only** | `.savechat 150`
`.activity` | Checks for spammers. **Bot Owner Only** | `.activity`
`.calculate` `.calc` | Evaluate a mathematical expression.  | `.calc 1+1`
`.calcops` | Shows all available operations in the `.calc` command  | `.calcops`
`.scsc` | Starts an instance of cross server channel. You will get a token as a DM that other people will use to tune in to the same instance. **Bot Owner Only** | `.scsc`
`.jcsc` | Joins current channel to an instance of cross server channel using the token. **Requires ManageServer server permission.** | `.jcsc TokenHere`
`.lcsc` | Leaves a cross server channel instance from this channel. **Requires ManageServer server permission.** | `.lcsc`
`.serverinfo` `.sinfo` | Shows info about the server the bot is on. If no channel is supplied, it defaults to current one.  | `.sinfo Some Server`
`.channelinfo` `.cinfo` | Shows info about the channel. If no channel is supplied, it defaults to current one.  | `.cinfo #some-channel`
`.userinfo` `.uinfo` | Shows info about the user. If no user is supplied, it defaults a user running the command.  | `.uinfo @SomeUser`
`.repeatinvoke` `.repinv` | Immediately shows the repeat message on a certain index and restarts its timer. **Requires ManageMessages server permission.** | `.repinv 1`
`.repeatremove` `.reprm` | Removes a repeating message on a specified index. Use `.repeatlist` to see indexes. **Requires ManageMessages server permission.** | `.reprm 2`
`.repeat` | Repeat a message every `X` minutes in the current channel. You can have up to 5 repeating messages on the server in total. **Requires ManageMessages server permission.** | `.repeat 5 Hello there`
`.repeatlist` `.replst` | Shows currently repeating messages and their indexes. **Requires ManageMessages server permission.** | `.repeatlist`
`.listquotes` `.liqu` | `.liqu` or `.liqu 3`  | Lists all quotes on the server ordered alphabetically. 15 Per page.
`...` | Shows a random quote with a specified name.  | `... abc`
`.qsearch` | Shows a random quote for a keyword that contains any text specified in the search.  | `.qsearch keyword text`
`..` | Adds a new quote with the specified name and message.  | `.. sayhi Hi`
`.deletequote` `.delq` | Deletes a random quote with the specified keyword. You have to either be server Administrator or the creator of the quote to delete it.  | `.delq abc`
`.delallq` `.daq` | Deletes all quotes on a specified keyword. **Requires Administrator server permission.** | `.delallq kek`
`.remind` | Sends a message to you or a channel after certain amount of time. First argument is `me`/`here`/'channelname'. Second argument is time in a descending order (mo>w>d>h>m) example: 1w5d3h10m. Third argument is a (multiword) message.  | `.remind me 1d5h Do something` or `.remind #general 1m Start now!`
`.remindtemplate` | Sets message for when the remind is triggered.  Available placeholders are `%user%` - user who ran the command, `%message%` - Message specified in the remind, `%target%` - target channel of the remind. **Bot Owner Only** | `.remindtemplate %user%, do %message%!`
`.convertlist` | List of the convertible dimensions and currencies.  | `.convertlist`
`.convert` | Convert quantities. Use `.convertlist` to see supported dimensions and currencies.  | `.convert m km 1000`
