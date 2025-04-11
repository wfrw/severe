# EACH FUNCTION ADDED THIS DOCUMENTATION WILL BE UPDATED

### == [ roblox lua information ] ==

### ! all "get" and "set" functions below are PascalCase for rlua support !

-# general properties:
-# .Data - returns the userdata
-# .Name - returns the name
-# .ClassName - returns the classname
-# .Parent - returns the parent

-# example:
-# print(game.Players:FindFirstChild("novice"))
-# game:FindService("UserInputService"):SetMouseLocation(0, 0)
-# print(game:FindService("Players").localPlayer.Name)
-# print(game:FindService("Players").localPlayer.Data) -- returns userdata
### == [ predefined globals ] ==

-# [return: userdata] <- Game - returns datamodel
-# [return: table] <- game - returns datamodel [rlua only]
### == [ misc functions ] ==

-# [returns: tuple - fields: x, y | boolean] <- worldtoscreenpoint -> [argument: table - vector3] - this function returns the screen points of the vector3 and whether this point is within the bounds of the screen.
-# [return: none] <- print -> [argument: string] - prints out in white text
-# [return: none] <- warn -> [argument: string] - prints out in yellow text
-# [return: none] <- wait -> [argument: [OPTIONAL] number] - yields the current thread with specified timeout
-# [return: none] <- spawn -> [argument: function] - spawns in a background thread that will execute the function.
-# [return: string] <- gethwid -> [argument: none] - returns the current user SID
-# [return: none] <- setclipboard -> [argument: string] - sets the string argument to your clipboard.
-# [return: number] <- tick -> [argument: none] - returns the amount of time in seconds since the Unix epoch according to this device's time.
-# [return: number] <- gcinfo -> [argument: none] - returns the total memory heap size in kilobytes.
-# [return: number] <- time -> [argument: none] - returns the amount of time, in seconds, that has elapsed since severe started running
-# [return: variant] <- loadstring -> [argument: string, [OPTIONAL] [CHUNK] string] - loads lua code from the string and return it as a function.
-# [return: boolean] <- isrbxactive -> [argument: none] - returns a boolean indicating if roblox is focused or not
-# [return: none] <- destroy -> [argument: userdata] - sets the userdata parent to nothing technically destroying it
-# [return: none] <- makefolder -> [argument: string - foldername] - creates a folder : C:\v2\data
-# [return: none] <- deletefolder -> [argument: string - foldername] - deletes the folder  : C:\v2\data
-# [return: none] <- deletefile -> [argument: string - filename] - deletes the file  : C:\v2\data
-# [return:  boolean] <- checkfolder -> [argument: string - foldername] - checks if the folder exists  : C:\v2\data
-# [return: boolean] <- checkfile -> [argument: string - filename] - checks if the file exists : C:\v2\data
-# [return: table] <- listfiles -> [argument: none] - lists all files in C:\v2\data
-# [return: none] <- writefile -> [argument: string - filename, string - data] - creates the file and write the data into it. : C:\v2\data
-# [return: string] <- readfile -> [argument: string - filename] - returns the contents from the filename. : C:\v2\data
-# [return: boolean] <- ismenuopened -> [argument: none] - returns a boolean indicating if severe menu is opened or not
-# [return: none] <- set_window_passthrough -> [argument: boolean] - makes it so mouse events works through severe overlay or not
-# [return: none] <- SET_SCHEDULER_TIMEOUT-> [argument: boolean] - makes it so the scheduler can timeout if frozen for 7 seconds or not-# [return: tuple - Vector3  - fields: x, y, z ] <- lerpvector3 -> [arguments: table - vector3, table - vector3, number - alpha] - returns a vector3 interpolated between arg 1 and arg2 by the fraction alpha
-# [return: tuple - CFrame - fields: lookvector - vector3, upvector - vector3, rightvector - vector3, position - vector3 ] <- lerpcframe -> [arguments: cframe, cframe, number - alpha] - returns a cframe interpolated between arg 1 and arg2 by the fraction alpha
-# [return: tuple - CFrame - fields: lookvector - vector3, upvector - vector3, rightvector - vector3, position - vector3 ] <- cframelookat -> [arguments: table - cframe, table - vector3] - returns a new CFrame with the position of arg 1 [cframe] and facing towards arg 2 [vector3]
-# [return: table] <- pointer_to_table_data -> [argument: number - pointer] - returns the pointer as a table you can use for internals functions [! use only for rlua !]
-# [return: userdata] <- pointer_to_user_data -> [argument: number - pointer] - returns the pointer as a userdata you can use for internals functions
### == [ get functions ] ==

-# [return: number or table or bool or int or string] <- getvalue -> [argument: userdata] - returns the value property of the userdata class name must include "Value"
-# [return: userdata] <- findfirstchild -> [arguments: userdata, string] - returns the first child of the userdata with the given name
-# [return: userdata] <- findfirstchildofclass -> [arguments: userdata, string] - returns the first child of the userdata whose classname is equal to the given classname
-# [return: userdata] <- findfirstancestorofclass -> [arguments: userdata, string] - returns the first ancestor of the userdata whose name is equal to the given name.
-# [return: string] <- getname -> [argument: userdata] - returns the name of the userdata
-# [return: string] <- getclassname -> [argument: userdata] - returns the classname of the userdata
-# [return: array] <- getchildren -> [argument: userdata] - returns an array containing all of the userdata direct children
-# [return: array] <- getdescendants [unsafe] -> [argument: userdata] - returns an array containing all children of the userdata and every child of that children
-# [return: userdata] <- getparent -> [argument: userdata] - returns the parent of the userdata
-# [return: boolean] <- isancestorof -> [arguments: userdata, userdata] - returns true if the first userdata is an ancestor of the given descendant [second userdata]
-# [return: boolean] <- isdescendantof -> [arguments: userdata, userdata] - returns true if the first userdata is a descendant of the given ancestor [second userdata]
-# [return: userdata] <- getlocalplayer -> [argument: none] - returns the localplayer
-# [return: userdata] <- getcharacter -> [argument: userdata -> Player] - returns the character of the given player
-# [return: userdata] <- findservice -> [arguments: userdata -> Game, string] - returns the service specified by the given classname.
-# [return: number] <- getuserid -> [argument: userdata -> Player] -  returns the player [userdata] userid
-# [return: number] <- getping -> [argument: none] - returns your roblox game ping
-# [returns: tuple - fields: x, y] <- getscreendimensions -> [argument: none] - returns the screen dimensions.-# [return: userdata] <- getadornee -> [argument: userdata -> BillboardGui] - returns the adornee of the billboardgui
-# [return: string] <- getdisplayname -> [argument: userdata -> Player] - returns the displayname of the player [userdata]
-# [return: userdata] <- getprimarypart -> [argument: userdata -> Model] - returns the primarypart of the model [userdata]
-# [return: number] <- gethealth -> [argument: userdata -> Humanoid] - returns the health of the humanoid [userdata]
-# [return: number] <- getmaxhealth -> [argument: userdata -> Humanoid] - returns the maxhealth of the humanoid [userdata]
-# [return: userdata] <- getteam -> [argument: userdata -> Player] - returns the team of the player [userdata]
-# [return: string] <- gettextureid -> [argument: userdata -> MeshPart] - returns the texture id of the meshpart [userdata]
-# [return: string] <- getmeshid -> [argument: userdata -> MeshPart] - returns the mesh id of the meshpart [userdata]
-# [return: number] <- getcamerafov -> [argument: userdata -> Camera] - returns the fov of the camera [userdata]
-# [return: tuple - fields: x, y, z] <- getposition -> [argument: userdata] - returns the position of the given part or camera
-# [return: tuple - fields: x, y, z] <- getlookvector -> [argument: userdata] - returns the lookvector of the given part or camera
-# [return: tuple - fields: x, y, z] <- getrightvector -> [argument: userdata] - returns the rightvector of the given part or camera
-# [return: tuple - fields: x, y, z] <- getupvector -> [argument: userdata] - returns the upvector of the given part or camera
-# [return: tuple - fields: x, y, z] <- getsize -> [argument: userdata] - returns the size of the given part
-# [return: tuple - fields: x, y, z] <- getvelocity -> [argument: userdata] - returns the velocity of the given part
-# [return: userdata] <- findfirstdescendant -> [arguments: userdata, string] - returns the first descendant found with the given name
-# [return: userdata] <- findfirstancestor -> [arguments: userdata, string] - returns the first ancestor of the userdata whose name is equal to the given name.
-# [return: userdata] <- waitforchild -> [arguments: userdata, string, [OPTIONAL] number] - returns the child of the userdata with the given name. If the child does not exist, it will pause the current thread until it does. If the timeout parameter is specified, this will time out after the specified number of seconds and return nil
-# [return: tuple - CFrame - fields: lookvector - vector3, upvector - vector3, rightvector - vector3, position - vector3 ] <- getcframe -> [argument: userdata] - returns the cframe of the given part or camera### == [ set functions ] ==

-# [return: none] <- setcframe -> [arguments: userdata, table - cframe] - sets the cframe from the userdata to the given cframe
-# [return: none] <- setlookvector -> [arguments: userdata, table - vector3] - sets the lookvector from the userdata to the given vector3
-# [return: none] <- setupvector -> [arguments: userdata, table - vector3] - sets the upvector from the userdata to the given vector3
-# [return: none] <- setrightvector -> [arguments: userdata, table - vector3] - sets the rightvector from the userdata to the given vector3
-# [return: none] <- setposition -> [arguments: userdata, table - vector3] - sets the position from the userdata to the given vector3
-# [return: none] <- setvelocity -> [arguments: userdata, table - vector3] - sets the velocity from the userdata to the given vector3
-# [return: none] <- setmouselocation -> [arguments: userdata -> MouseService, number - x, number - y] - sets roblox mouse location to specified x and y values
-# [return: none] <- setmouseiconenabled -> [arguments: userdata -> MouseService, bool] - sets roblox mouse icon [false = hide cursor, true = show cursor]
-# [return: none] <- setmousebehaviour -> [arguments: userdata -> MouseService, number] - sets roblox mouse behaviour [ 0 = Default, 1 = LockCenter, 2 = LockCurrentPosition ]
-# [return: none] <- setmousedeltasensitivity -> [arguments: userdata -> MouseService, number] - sets roblox mouse delta sensitivity
-# [return: none] <- setvalue -> [argument: userdata, int or number or table or bool or string] - set the value property of the userdata class name must include "Value" and second argument must match classname
-# [return: none] <- setcamerasubject -> [arguments: userdata -> Camera] - sets the camera subject### == [ keyboard functions ] ==

-# : IMPORTANT : https://docs.microsoft.com/en-us/windows/desktop/inputdev/virtual-key-codes  : IMPORTANT :

-# [return: none] <- keypress -> [argument: number - keycode] - simulates a key press for the given virtual keycode
-# [return: none] <- keyrelease -> [argument: number - keycode] - simulates a key release for the given virtual keycode
-# [return: string] <- getpressedkey -> [argument: none] - returns the last pressed key name
-# [return: array] <- getpressedkeys -> [argument: none] - returns a list of pressed keys name### == [ mouse functions ] ==

-# [return: boolean] <- isleftclicked -> [argument: none] - returns a boolean if left mouse clicked or not
-# [return: boolean] <- isrightclicked -> [argument: none] - returns a boolean if right mouse clicked or not
-# [return: boolean] <- isleftpressed -> [argument: none] - returns a boolean if left mouse is pressed or not
-# [return: boolean] <- isrightpressed -> [argument: none] - returns a boolean if right mouse is pressed or not
-# [return: none] <- mousemoverel -> [arguments: number - x, number - y] - moves the mouse to the x and y relative coordinates
-# [return: none] <- mousemoveabs -> [arguments: number - x, number - y] - moves the mouse to the x and y absolute coordinates
-# [return: none] <- mousescroll -> [argument: number - pixels] - scrolls your mouse by the given pixels
-# [return: none] <- mouse1click > [argument: none] - simulate a left mouse click
-# [return: none] <- mouse1press > [argument: none] - simulate a left mouse press
-# [return: none] <- mouse1release > [argument: none] - simulate a left mouse release
-# [return: none] <- mouse2click > [argument: none] - simulate a right mouse click
-# [return: none] <- mouse2press > [argument: none] - simulate a right mouse press
-# [return: none] <- mouse2release > [argument: none] - simulate a right mouse release
-# [return: tuple - fields: x, y] <- getmouseposition > [argument: none] - returns the default mouse position
-# [return: boolean] <- ismouseiconenabled -> [argument: userdata -> MouseService] - returns a boolean if the mouseicon is enabled or not
-# [return: tuple - fields: x, y] <- getmouselocation -> [argument: userdata -> MouseService] - returns the roblox mouse location
-# [return: number] <- getmousebehavior -> [argument: userdata -> MouseService] - returns a number for how the mouse is behaving [ 0 = Default, 1 = LockCenter, 2 = LockCurrentPosition ]
-# [return: number] <- getmousedeltasensitivity -> [argument: userdata -> MouseService] - returns the roblox mouse delta sensitivity
-# [return: tuple - fields: x, y] <- smoothmouse_exponential -> [argument: table - x | y [ORIGIN], table - x | y [POINT], number - speed] - returns the exponential smoothing mouse results [recommended for aimbot]
-# [return: tuple - fields: x, y] <- smoothmouse_linear -> [argument: table - x | y [ORIGIN], table - x | y [POINT], number - sensitivity, number - smoothness] - returns the linear smoothing mouse results [recommended for aimbot]

-# example - smoothmouse_linear:
-# local mouse = getmouseposition()
-# local point_to = {0, 0}
-# local sensitivity = 1
-# local smoothness = .5
-# local result = smoothmouse_linear({mouse.x, mouse.y}, point_to, sensitivity, smoothness)
-# print(result.x, result.y)

-# example - smoothmouse_exponential:
-# local mouse = getmouseposition()
-# local point_to = {0, 0}
-# local speed = .5
-# local result = smoothmouse_exponential({mouse.x, mouse.y}, point_to, speed)
-# print(result.x, result.y)### == [ network functions ] ==

-# websocket example:
-# local ws = websocket_connect("ws://severe-websocket-test.glitch.me") -- connects to the websocket
-# websocket_onmessage(ws, function(msg) warn(msg) end) -- fires when a message is recieved from the websocket
-# websocket_send(ws, "Hello World!") -- sends message to the websocket
-# wait(1) -- yields the thread for 1 second
-# websocket_close(ws) -- closes the connection to the websocket

-# [return: none] <- websocket_connect -> [argument: string - URL] - connects to the websocket [URL], errors if fails.
-# [return: none] <- websocket_onmessage -> [arguments: userdata - websocket, function] - executes the function when a new message from the websocket is recieved
-# [return: none] <- websocket_send -> [arguments: userdata - websocket, string] - sends a message [string] to the websocket
-# [return: none] <- websocket_close -> [arguments: userdata - websocket, string] - closes the connection with the websocket.
-# [return: string] <- httpget -> [argument: string] - returns the contents of the given url
-# [return: string] <- httppost -> [arguments: string - URL, string - DATA, string - CONTENT_TYPE, string - ACCEPT,  [OPTIONAL] string - COOKIE,  [OPTIONAL] string - REFERER,  [OPTIONAL] string - ORIGIN] - sends a post request to the given url and returns the result
### == [ drawing lib ] ==
-# [return: none] <- Drawing.clear -> [argument: none] - clears and deletes all created drawing objects
-# [return: object] <- Drawing.new -> [argument: string - TYPE] - creates a new drawing object and returns it.

-# TYPES
-# 1. Text
-# 2. Line
-# 3. Quad
-# 4. Triangle
-# 5. Circle
-# 6. Square
-# 7. Image

-# Default -  PROPERTIES
-# bool Visible
-# void Remove
-# vector3 Color

-# Text -  PROPERTIES
-# string Text
-# number Transparency
-# number Size
-# bool Center
-# bool Outline
-# Vector3 OutlineColor
-# Vector2 Position
-# Vector2 TextBounds [readonly]
-# number Font : 0 - 15

-# Line -  PROPERTIES
-# number Transparency
-# number Thickness
-# Vector2 From
-# Vector2 To

-# Circle -  PROPERTIES
-# number Transparency
-# number Thickness
-# number NumSides
-# number Radius
-# bool Filled
-# Vector2 Position

-# Square -  PROPERTIES
-# number Transparency
-# number Thickness
-# Vector2 Size
-# Vector2 Position
-# bool Filled

-# Triangle -  PROPERTIES
-# number Transparency
-# number Thickness
-# Vector2 PointA
-# Vector2 PointB
-# Vector2 PointC
-# bool Filled

-# Image -  PROPERTIES
-# string Url
-# bool Gif
-# number Delay [GIF Only]
-# Vector2 Position
-# Vector2 Size

-# Quad -  PROPERTIES
-# Vector2 PointA
-# Vector2 PointB
-# Vector2 PointC
-# Vector2 PointD
-# number Thickness
-# bool Filled
-# number Transparency

-# examples:
-# local text = Drawing.new("Text")
-# text.Text = "severe drawing library!"
-# text.Visible = true
-# text.Position = {10, 10}
-# text.Color = {255, 255, 255}
-# text.Size = 15
-# wait(5) -- yield for 5 seconds
-# text:Remove()

-# local Image = Drawing.new("Image")
-# Image.Url = "https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTMzN21qODhla2pudGtlZHQ4aXpyMm5rOXlud3hkbjRmcm44MXhkdCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/VrQjb9El7JaQSFYjgJ/giphy-downsized-large.gif"
-# Image.Visible = true
-# Image.Gif = true
-# Image.Delay = 30
-# Image.Position = {400, 100}
-# Image.Size = {500, 500}
-# wait(20) -- yield for 20 seconds
-# Image:Remove()

-# local Image = Drawing.new("Image")
-# Image.Url = "https://letsenhance.io/static/8f5e523ee6b2479e26ecc91b9c25261e/1015f/MainAfter.jpg"
-# Image.Visible = true
-# Image.Position = {1000, 100}
-# Image.Size = {500, 500}
-# wait(10) -- yield for 10 seconds
-# Image:Remove()### == [ internal functions ] ==

-# TYPES
-# 1. qword
-# 2. dword
-# 3. double
-# 4. float
-# 5. string
-# 6. bool

-# [return: qword | dword | double | float | string | bool] <- getmemoryvalue -> [argument: userdata - pointer, number - offset, string - type] - reads the value at specified offset and returns it with the type you want
-# [return: none] <- setmemoryvalue -> [argument: userdata - pointer, number - offset, string - type, number | string - value] - set the value at specified offset with the type you want

-# ! EXAMPLES MAY BE OUTDATED !

-# examples:
-# -- primitive offset: 0x160
-# -- size x offset: 0x2b0
-# -- size y offset: 0x2b4
-# -- size z offset: 0x2b8

-# -- [ fake headless -client sided- scroll in and out of head ] --
-# local head = game.Players.localPlayer.Character.Head
-# local primitive_ptr = head:GetMemoryValue(0x160, "qword")
-# local primitive_ptr_data = pointer_to_table_data(primitive_ptr)
-# primitive_ptr_data:SetMemoryValue(0x2ac, "float", 0) -- x
-# primitive_ptr_data:SetMemoryValue(0x2ac, "float", 0) -- y
-# primitive_ptr_data:SetMemoryValue(0x2ac, "float", 0) -- z

-# -- [ change localplayer username  -client sided- ] --
-# local localplayer = getlocalplayer()
-# -- get the memory value residing at offset: 0x68 with type: qword
-# local nameptr = getmemoryvalue(localplayer, 0x68, "qword")
-# -- convert the pointer to a userdata so it can be used
-# local nameptr_data = pointer_to_user_data(nameptr)
-# -- get the string value residing at offset: 0x0 which represents the name
-# local name = getmemoryvalue(nameptr_data, 0x0, "string")
-# -- print the name
-# print(name)
-# -- set the new localplayer name that you want in memory
-# setmemoryvalue(nameptr_data, 0x0, "string", "hello_severe")
