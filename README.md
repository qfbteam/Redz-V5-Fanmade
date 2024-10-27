# Redz-V5-Fanmade
This documentation was made by a fan, the original documentation is here: https://github.com/REDzHUB/RedzLibV5
## Library
```lua
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV5/main/Source.Lua"))()
```
## Window
```lua
local Window = redzlib:MakeWindow({
  Title = "redz Hub : fanmade",
  SubTitle = "by redz9999 lib",
  SaveFolder = "testando | redz lib v5.lua"
})
```
## Tab
```Lua
local Tab1 = Window:MakeTab({"Example", "cherry"}) -- Icons Comming Soon
```

## Section
```lua
local Section = Tab2:AddSection({"Section"})
```

## Button
```lua
Tab1:AddButton({"Dark Purple", function()
-- code here
end})
```

## Toggle
```lua
local Toggle1 = Tab2:AddToggle({
  Name = "Toggle 1",
  Description = "This is a <font color='rgb(88, 101, 242)'>Toggle</font> Example",
  Flag = "Toggle1",
  Default = false
})
```
## Dropdown
```lua
local Dropdown = Tab2:AddDropdown({
  Name = "Players List",
  Description = "Select a random Number",
  Options = {"One", "Two", "Three", "Four", "Five"},
  Default = {"Two", "Four"},
  Flag = "Dropdown Teste 2",
  MultiSelect = true
})

-- Dropdown:Set("All", false)
-- Dropdown:Set("All", true)

Dropdown:Callback(function(Value)
  -- table.foreach(Value, print)
  -- print(Value, typeof(Value))
end)
```
## Slider
```lua
local Slider = Tab2:AddSlider({
  Name = "This is a Slider",
  -- Flag = "Slider Teste"
  Default = 40
})

Slider:Callback(function(Value)
  game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
end)

--[[Button:Callback(function()
  Dropdown:Set(Players:GetPlayers())
  Dropdown:Remove(Player.Name)
end

Dropdown:Remove(Player.Name)
Dropdown:Select(1)]]
```

## Textbox
```lua
local TextBox = Tab2:AddTextBox({
  Name = "Textbox",
  Description = "Walk Speed",
  PlaceholderText = "Number: 25/100",
  Callback = function(Value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
  end
})

TextBox.OnChanging = function(Text)
  local Number = tonumber(Text)
  if Number then
    return math.clamp(Number, 25, 100)
  end
  return 25
end
```
## Discord Invite Button
```
Tab3:AddDiscordInvite({
  Name = "redz Hub | Community",
  Description = "Join our discord community to receive information about the next update",
  Logo = "rbxassetid://15298567397",
  Invite = "https://discord.gg/7aR7kNVt4g"
})
```
