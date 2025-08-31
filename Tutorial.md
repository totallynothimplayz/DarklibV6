 # Getting Started
To begin, you need to declare a loadstring to access the library.
```luau
local DarkLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/totallynothimplayz/DarklibV6/refs/heads/main/Source.txt", true))()
```
## Make a Window
```luau
local Window = DarkLib:CreateWindow({
	Name = "You Hub Name (Give space at the end)", 
	Subtitle = "Idk ", 
	LogoID = "10734897102", 
	Size = UDim2.new(0.95, 0, 0.8, 0),
	LoadingEnabled = true, 
	LoadingTitle = "DarkMoon X", 
	LoadingSubtitle = "Loading...", 

	ConfigSettings = {
		RootFolder = nil, 
		ConfigFolder = "ScriptFolderName" 
	},

KeySystem = false, 
	KeySettings = {
		Title = "Hub Name ",
		Subtitle = " Key System",
		Note = "Enter the Key Obtained for the Hub Name",
		SaveInRoot = false, 
		SaveKey = true, 
		Key = {"You Key" --[[ if you want to make a loadstring contaning the key just put it here without " " ]] }, 
		SecondAction = {
			Enabled = false, 
			Type = "Discord", 
			Parameter = "You Discord Invite" 
		}
	}
})
```
**Argument 1: UI Title (type: string)**

**Argument 2: UI SubTitle (type: string)**

**Argument 3: UI LogoId (type: string);**

**Argument 4: UI Size (type: UDim2.new)**

**Argument 5: UI LoadingEnabled (type: Bool)**

**Argument 1: LoadingTitle (type: String)**

**Argument 2: LoadingSubtitle (type: string)**

**SubArgument 3: KeySystem (type: Bool)**

**Argument 4: Key System Keys (type: table)**

## Create Notifications
```luau
DarkLib:Notification({
	Title = "Made By (Your Name)",
	Icon = "check_circle",
	ImageSource = "Material", --You Can Use Custom if you want
	Content = "Credits To (Your Name)",
	Duration = 7 --Notification Duration in seconds
})
```
**Argument 1: Notification Title (type: string)**

**Argument 2: Notification Description (type: string)**

**Argument 3: Notification Duration (type: number)**
## Create Tab
```luau
local Tab1 = Window:CreateTab({
	Name = "TabName",
	Icon = "info",
	ImageSource = "Material", --if you want To use it instead By ID set to Custom
	ShowTitle = true
})
```
**Argument 1: Tab Name (type: string)**

**Argument 2: Tab Icon Name (type: string)**

**Argument 3: Tab ImageSource (type: string)** **Material or Custom**

**----------------------------------------------------------------------**

## Add a Section
```luau
Tab1:CreateSection("Section")
```
**Argument 1: Section Text (type: string)**

## Add a TextLabel
```luau
Tab1:CreateLabel({
	Text = "Text",
	Style = 1 -- style 1 is a message, 2 is a success and 3 is a warning/error
})
```
**Argument 1: TextLabel Text (type: string)**

**Argument 2: Style (type: Number)**

## Add a Paragraph
```luau
Tab1:CreateParagraph({
	Title = "Title",
	Text = "Text"
})
```
**Argument 1: Paragraph Title (type: string)**

**Argument 2: Paragraph Content(Description) (type: string)**

## Add a Button
```luau
local Button1 = Tab1:CreateButton({
	Name = "Button With Desc",
	Description = "Description is optional, if you dont want use nil",
	Callback = function()
		--Function Here
		print("Hi")
	end
})
```
**Argument 1: Button Text (type: string)**

**Argument 2: Button Desc (type: string)**

**Argument 3: Button Function On Clicked (type: func)**

## Add a Toggle
```luau
local Toggle = Tab1:CreateToggle({
	Name = "Text",
	Description = "Optional",
	CurrentValue = false,
	Callback = function(Value)
		--Function Here
		print(Value)
	end
}, "Flag")
```
**Argument 1: Toggle Text (type: string)**

**Argument 2: Toggle Desc (type: string)**

**Argument 3: Toggle State (type: bool)**

**Argument 3: Toggle Function (type: func)**

## Add a TextBox
```luau
local TextBox = Tab_1:CreateInput({
	Name = "Text",
	Description = "Optional",
	PlaceholderText = "PlaceHolder",
	CurrentValue = "",
	Numeric = false, -- Numebers Only
	MaxCharacters = 700, --Max Chars
	Enter = false, --Need press Enter for works or send in mobile
	Callback = function(Text)
		--Function Here
		print(Text)
	end
}, "Flag") 
```
**Argument 1: TextBox Text(Title) (type: string)**

**Argument 2: TextBox Desc (type: string)**

**Argument 3: TextBox Default Text (type: string)**

**Argument 4: TextBox AutoClear (type: bool)**

**Argument 5: TextBox PlaceHolder Text (type: string)**

**Argument 6: CurrentValue (type: string)**

**Argument 7: Numeric (type: Bool)**

**Argument 8: Need To Enter (type: Bool)**

**Argument 9: TextBox Function (type: func)**

## Add a Slider
```luau
local Slider = Tab_1:CreateSlider({
	Name = "Text",
	Range = {1, 100}, --Min, Max
	Increment = 1,
	CurrentValue = "1",
	Callback = function(Value)
		--Function Here
		print(Value)
	end
}, "Flag")
```
**Argument 1: Slider Text (type: string)**

**Argument 2: Slider Range (type: number)**

**Argument 3: Slider Max Value (type: number)**

**Argument 4: Slider Increase Value (type: number)**

**Argument 5: Slider Default Value (type: string)**

**Argument 6: Slider Function (type: func)**

## Add a Dropdown
```luau
local DropDown = Tab_1:CreateDropdown({
	Name = "Text",
	Description = "Optional",
	Options = {"Option 1", "Option 2", "Option 3"},
	CurrentOption = {"Option 1"},
	MultipleOptions = false, --Select Multiple Options 
	Callback = function(Option)
		--Function Here
		print(Option)
	end
}, "Flag")
```
**Argument 1: Dropdown Text (type: string)**

**Argument 2: Dropdown Desc (type: string)**

**Argument 2: Dropdown Options (type: table)**

**Argument 3: Dropdown Default Option (type: String)**

**Argument 4: Dropdown Multiple Option (type: Bool)**

**Argument 5: Dropdown Function (type: function)**

# Functions
All Library Functions!

## Library
1. SettingsTab:BuildConfigSection() --optional
2. SettingsTab:BuildThemeSection() --Optional

3. Window:CreateHomeTab({
	 SupportedExecutors = {}, 
	 DiscordInvite = "Invite", -- dont put discord.gg
	Icon = 1, 
 })

**----------------------------------------------------------------------**

Thats All ;)
