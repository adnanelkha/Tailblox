# Tailblox

> Custom Theme styles, with theme functions!

## Tutorial
> First, require the module from anywhere in your game, this module works anywhere.
```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Tailblox = require(ReplicatedStorage.Tailblox)
```
> Secondly, create your brand-new theme using a table of properties and functions.
```lua
local myTheme = Tailblox({ 

	BackgroundColor3 = Color3.fromRGB(16,16,16),
	BorderColor3 = Color3.fromRGB(255,255,255),
	BorderSizePixel = 1,
	Size = UDim2.new(0.1, 0, 0.1, 0),
	AnchorPoint = Vector2.new(0.5, 0,.5),
	Position = UDim2.new(0.5, 0, 0.5 ,0),
	
	myFunction = function()
		print("Hello from DarkTheme!")
	end,

        myCoolPrintFunction = function(optionalArguments)
		print(table.unpack(optionalArguments)) -- Ensure to unpack the arguments if you provided any!
	end,

})
```
> Finally, apply your brand new theme to any `GuiObject` by utilising the `:apply()` function.
```lua
local myFrame = Instance.new("Frame")
myTheme:apply(myFrame)
```
> You can run functions in your theme by utilising the `:run()` function. You must provide the first argument as the functions name and the second argument may be additional arguments to provide to the theme's function.
```lua
myTheme:run(myFunction)
```
```lua
myTheme:run(myCoolPrintFunction, "Hello World")
```

## Footer
> Thank you for using this module, updates will come as I think of them and I'll continue to update this page.
> Feel free to contact me on discord if you need assistance! @waitforchild
