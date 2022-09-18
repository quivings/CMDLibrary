# CMDLibrary
my first ui library 

#Documentation

```local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/quivings/CMDLibrary/main/src"))()```

#Creating the window
```local Window = Library:Create({Title = "CMD"})```

#UI Elements

```
local Tab = Window:CreateTab({
    Icon = "rbxassetid://" -- Roblox Icon Id's go here; there are no tab titles.
)}
```

**Toggles**
```
local Toggle = Tab:CreateToggle({
    Title = "Toggle"
    callback = function(v) -- Returns true or false
    end
})
```
local Dropdown = Tab:CreateDropdown({
    Title = "Dropdown",
    KeepValue = true -- If you have KeepValue on, it will Keep the option selected. If KeepValue is off, the dropdown option will still work as normal. More of a visual thing.
})

local DropdownOption = Dropdown:MakeOption({
    Text = "Option",
    callback = function(v) -- Returns the Dropdown option
    end
})
```
**Sliders**
```
local Slider = Tab:CreateSlider({
    Title = "Slider",
    callback = function(v) -- Returns the value of the slider
    end
})
```

**Buttons**
```local Button = Tab:CreateButton({
      Title = "Button"
      callback = function()
      end
   })

   Button:SetText("Text")
   
   Button:SetCallback(function()
      print("Button clicked")
   end)
```

#Chat commands

```
Library:CreateChatCommand(";", "print", "p", function(msg) -- Prefix, Command Name, Command Alias, and the command function. can take up to a maximum of three args
    print(msg)
end)
```
