In order to create a chat command and connect it to VioPaige's BetterChat mod, copy the uasset in this folder into the location Content/UI/Widgets/HUD/Chat/WBP_UI_HUD_Chat.uasset in your UE4.27 project folder

Do not actually include this blueprint in your mod, only include your own mod that connects to it there, then instruct your users to also get this mod. This way the better chat can be updated and patched where necessary.
In order to connect a command to this mod, get all widgets of the chat class (you will only get one), then bind a custom event (in your blueprint) to the "ChatCommandDispatcher" that exists in this blueprint, your custom event needs a string input, if it has that, the text that the player is currently typing will be passed there, then you can check whether that string/text corresponds to a command name you would like to add.

Note: Make sure to add a ~10 second delay before connecting as the chat does not load immediately when the heist starts