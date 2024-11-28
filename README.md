<div align="center">

![](https://github.com/funtmaster/AchievementService/blob/3abaf995c03c670bdd45e2a9a4ede302532adbd4/Logo.png)

</div>

<div align="center"><h1>Achievement Service</h1></div>
<div align="center"><h3>Easily Manage and Award Badges</h3></div>
<div align="center"><a href="https://www.roblox.com/games/127054146251804/AchievementService">Game Example (Uncopylocked)</a></div>

<br>AchievementService is an open-source module designed to make managing and awarding achievements in your games easy and customizable. With built-in support for UI animations, haptics, audio, and more, you can create engaging achievement experiences for your players.

<h2>⭐ Features</h2>

<h4> 1. Awarding Badges</h4>
AchievementService makes it simple to award badges to players in your game.

```lua
AchievementService:Award(player, badgeName)
```
That’s it! No need to specify the `BadgeId` anymore. AchievementService uses **HTTPService** and Roblox APIs to automatically fetch all the available badges for your game, making the process much easier and more efficient. *Please note that issues may occur if there are two or more badges with the exact same name.*


<h4> 2. Customizable Animations</h4>
AchievementService provides an option to toggle customizable UI animations. It also includes a default animation for easy use. You can either use the default UI or design your own. <i>I recommend using the existing script in the default UI as a template if you decide to create your own.</i>

![](https://github.com/funtmaster/AchievementService/blob/2efe12046beb4afb46980db811b31e24255d179b/Animation.mov)

<h4> 3. Audio Support</h4>
AchievementService allows for customizable sounds, allowing you to toggle and add audios. I've also included a pack of 25 classic Roblox audios with the module. <sub>lol</sub>

<h4> 4. Haptic Feedback</h4>
AchievementService even allows for haptics, allowing for tactile response to mobile and possibly console players.

<h4> 5. Fully Open-Source</h4>
AchievementService is entirely open-source, allowing you to modify and extend the module as needed for your game.

<h2>🔨 Installation Guide</h2>
<h4>1. Import the Module and Enable HTTP Requests</h4>

* Copy the AchievementService module into your game.
* Enable `Allow HTTP Requests` in your game settings under the security tab.

<h4>2. Initialization</h4>

* In your script, require the module and initialize it:
```lua
local AchievementService = require(PATH_TO_MODULE.AchievementService)
AchievementService.init()
```

<h4>3. Awarding Badges</h4>

* To award an achievement to a player, simply call:
```lua
AchievementService:Award(player, badgeName)
```

<h4>4. Configuration</h4>

* AchievementService, as of **v1.0**, allows configuration/customization for the following:

  * Toggle animations
   * Animation Style (which type of animation)
   * Toggle sounds
  * Sound (which sound will play)
  * Speed Multiplier (how fast an animation plays)
  * Toggle haptics
  * Animation timeout

<h2>🧠 Example</h2>

```lua
local AchievementService = require(game.ReplicatedStorage.AchievementService)

-- Initialize the service
AchievementService.init()

game.Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function(character)
        -- Example: Award achievement when player enters the game
        AchievementService:Award(player, "Welcome")
    end)
end)
```

<h2>📜 Update Log</h2>


<details open>
<summary>v1.0 - November 28th, 2024 (Current)</summary>

  * Released
</details>

<h2>🌐 Miscellaneous</h2>

* Developed and created by @FuntMaster.
* One thing to note is that AchievementService uses **[RoProxy](https://devforum.roblox.com/t/roproxycom-a-free-rotating-proxy-for-roblox-apis/1508367)** to access Roblox Badge APIs. Although rare, I cannot control any downtime or slowdown that occur with this proxy. If you're worried about that, I'd recommend using your own self-hosted proxy or some other way to access Roblox Badge APIs. (If someone has a better way of accessing the API, lmk!)
* Lastly, please feel free to let me know of any bugs, issues, suggestions that you have!
<br><sub>P.S. this is my first time making a Github respository!</sub>
