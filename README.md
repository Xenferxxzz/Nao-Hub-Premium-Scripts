repeat wait()
until _G.Key ~= '' and _G.DiscordId ~= ''

Key = _G.Key
DiscordId = _G.DiscordId

local starttime = os.time()
local base_url = 'https://whitelist-by-nao-test-test.nyaouuvictoria.repl.co'
local HttpService = game:GetService('HttpService')
local vixz_requests

local main = {
	["1"] = rconsoleprint,
	["2"] = hookfunc,
	["3"] = hookfunction,
	["4"] = replaceclosure,
	["5"] = setreadonly,
	["6"] = make_writeable,
	["7"] = print,
	["8"] = warn,
	["9"] = writefile,
	["10"] = appendfile,
	["11"] = setclipboard,
}
if getgenv().AntihookFF1 == nil then
	getgenv().AntihookFF1 = {
		["print"] = false, -- ปรับเป็น true =ไห้ไช้ได้
		["hook"] = false
	}
end

local azx 
azx = hookfunc(rconsoleprint, function (...)
	if getgenv().AntihookFF1["print"] == true then
		return azx(...)
	else
		return 
	end
end)
local al 
al = hookfunc(hookfunction, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return al(...)
	else
		return 
	end
	
end)
local al 
al = hookfunc(setclipboard, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return al(...)
	else
		return 
	end
end)
local an 
an = hookfunc(replaceclosure, function (...)
	if getgenv().AntihookFF1["print"] == true then
		return an(...)
	else
		return 
	end
	
end)
local ay 
ay = hookfunc(setreadonly, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return ay(...)
	else
		return 
	end
	
end)
local ae 
ae = hookfunc(make_writeable, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return ae(...)
	else
		return 
	end
end)
local av 
av = hookfunc(print, function (...)
	if getgenv().AntihookFF1["print"] == true then
		return av(...)
	else
		return 
	end
end)
local at 
at = hookfunc(warn, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return at(...)
	else
		return 
	end
end)
local aw 
aw = hookfunc(writefile, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return aw(...)
	else
		return 
	end
end)
local aq
aq = hookfunc(appendfile, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return aq(...)
	else
		return 
	end
end)
local dsa
dsa = hookfunc(clonefunction,function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return dsa(...)
	else
		return 
	end
end)
local as 
as = hookfunc(hookfunc, function (...)
	if getgenv().AntihookFF1["hook"] == true then
		return as(...)
	else
		return 
	end
end)

getgenv().rconsoleprint = function(...)
	if getgenv().AntihookFF1["print"] == true then
		return main["1"](...)
	else
		return "Secret"
	end
end
getgenv().hookfunc = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["2"](...)
	else
		return "Secret"
	end
end
getgenv().hookfunction = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["3"](...)
	else
		return "Secret"
	end
end
getgenv().replaceclosure = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["4"](...)
	else
		return "Secret"
	end
end
getgenv().setreadonly = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["5"](...)
	else
		return "Secret"
	end
end
getgenv().make_writeable = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["6"](...)
	else
		return "Secret"
	end
end
getgenv().print = function(...)
	if getgenv().AntihookFF1["print"] == true then
		return main["7"](...)
	else
		return "Secret"
	end
end
getgenv().warn = function(...)
	if getgenv().AntihookFF1["print"] == true then
		return main["8"](...)
	else
		return "Secret"
	end
end
getgenv().writefile = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["9"](...)
	else
		return "Secret"
	end
end
getgenv().appendfile = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["10"](...)
	else
		return "Secret"
	end
end
getgenv().setclipboard = function(...)
	if getgenv().AntihookFF1["hook"] == true then
		return main["11"](...)
	else
		return "Secret"
	end
end

if syn then
    vixz_requests = syn.request
elseif KRNL_LOADED then
    vixz_requests = request
else
    vixz_requests = fluxus.request
end

local kick = function(msg)
	game.Players.LocalPlayer:Kick(msg)
end

spawn(function()
	game:GetService("RunService").RenderStepped:connect(function()
		game.CoreGui.ChildAdded:connect(function(p1)
			if p1:FindFirstChild("PropertiesFrame") or p1:FindFirstChild("ExplorerPanel") or p1:FindFirstChild("SaveInstance") then -- Dark Dex frames/children
				game.Players.LocalPlayer:Kick("\nNao Hub\nGG WP BY nyaouu#0001")
				wait(.5)
				while true do
					game.Players.LocalPlayer:Kick("\nNao Hub\nGG WP BY nyaouu#0001")
				end
			end
		end)
	end)
end)

spawn(function()
	game:GetService("RunService").RenderStepped:connect(function()
		for i,v in pairs (game:GetService("CoreGui"):GetChildren())do
			if v.Name == "DevConsoleMaster" then
				v.Enabled = false
				v:Destroy()
				game.Players.LocalPlayer:Kick("\nNao Hub\nGG WP BY nyaouu#0001")
				wait(.5)
				while true do
					game.Players.LocalPlayer:Kick("\nNao Hub\nGG WP BY nyaouu#0001")
				end
			end
		end
	end)
end)

local req = vixz_requests({
	Url = base_url .. '/hwid',
	Method = "POST",
	Headers = {
		["Authorization"] = "/20xZxpzveU5jXiYNGjZpzrG/uRBPkITmFQBdGLrhBJxHlWyFhe7H/hxpXgx4Egj+/3pecqXqKRHPG70avOmR4NiBtZnoJ8lj9oLKlzOhjrUQqTIva5wqmvCTfJSNj1EiQRPO4ZTOxw+Wo5YRpSgSIzW8A/un5z1bxUgWG5eJj0=",
		["Content-Type"] = "application/json"
	},
	Body = HttpService:JSONEncode({
		['key'] = Key,
        ['hwid'] = tostring(game:GetService('RbxAnalyticsService'):GetClientId()),
        ['userid'] = DiscordId
	})
})

local req2 = vixz_requests({
	Url = base_url .. '/hwid',
	Method = "POST",
	Headers = {
		["Authorization"] = "/20xZxpzveU5jXiYNGjZpzrG/uRBPkITmFQBdGLrhBJxHlWyFhe7H/hxpXgx4Egj+/3pecqXqKRHPG70avOmR4NiBtZnoJ8lj9oLKlzOhjrUQqTIva5wqmvCTfJSNj1EiQRPO4ZTOxw+Wo5YRpSgSIzW8A/un5z1bxUgWG5eJj0=",
		["Content-Type"] = "application/json"
	},
	Body = HttpService:JSONEncode({
		['key'] = Key,
        ['hwid'] = tostring(game:GetService('RbxAnalyticsService'):GetClientId()),
        ['userid'] = DiscordId
	})
})

local data = HttpService:JSONDecode(req.Body)

if req.StatusMessage == 'OK' and req.Success == true and req.StatusCode == 200 then
    hwid1 = data.message
else
    kick(data.message)
    return false
end

local data2 = HttpService:JSONDecode(req2.Body)

if req2.StatusMessage == 'OK' and req2.Success == true and req2.StatusCode == 200 then
    hwid2 = data2.message
else
    kick(data2.message)
    return false
end

if hwid1 ~= hwid2 then
    kick('Hwid Fuck')
    return false
end

hwid = hwid or hwid2

local req3 = vixz_requests({
	Url = base_url .. '/check',
	Method = "POST",
	Headers = {
		["Authorization"] = "/20xZxpzveU5jXiYNGjZpzrG/uRBPkITmFQBdGLrhBJxHlWyFhe7H/hxpXgx4Egj+/3pecqXqKRHPG70avOmR4NiBtZnoJ8lj9oLKlzOhjrUQqTIva5wqmvCTfJSNj1EiQRPO4ZTOxw+Wo5YRpSgSIzW8A/un5z1bxUgWG5eJj0=",
		["Content-Type"] = "application/json"
	},
	Body = HttpService:JSONEncode({
		['key'] = Key,
        ['hwid'] = hwid,
        ['userid'] = DiscordId
	})
})

local req4 = vixz_requests({
	Url = base_url .. '/check',
	Method = "POST",
	Headers = {
		["Authorization"] = "/20xZxpzveU5jXiYNGjZpzrG/uRBPkITmFQBdGLrhBJxHlWyFhe7H/hxpXgx4Egj+/3pecqXqKRHPG70avOmR4NiBtZnoJ8lj9oLKlzOhjrUQqTIva5wqmvCTfJSNj1EiQRPO4ZTOxw+Wo5YRpSgSIzW8A/un5z1bxUgWG5eJj0=",
		["Content-Type"] = "application/json"
	},
	Body = HttpService:JSONEncode({
		['key'] = Key,
        ['hwid'] = hwid,
        ['userid'] = DiscordId
	})
})

if req3.StatusMessage ~= 'OK' or req3.Success ~= true or req3.StatusCode ~= 200 then
    local data3 = HttpService:JSONDecode(req3.Body)
    kick(data3.message)
    if data3.message == 'Hwid Not Found' then
       setclipboard(hwid) 
    end
    return false
end

if req4.StatusMessage ~= 'OK' or req4.Success ~= true or req4.StatusCode ~= 200 then
    local data4 = HttpService:JSONDecode(req4.Body)
    kick(data4.message)
    if data4.message == 'Hwid Not Found' then
       setclipboard(hwid)
    end
    return false
end

if tonumber(os.time()) < tonumber(starttime) then
    kick('Os time error')
    return
end



print('Successfully')






if not game:IsLoaded() then
    game.Loaded:Wait()
end

repeat
    wait()
until game.Players
repeat
    wait()
until game.Players.LocalPlayer


local placeId = game.PlaceId
if placeId == 2753915549 or placeId == 4442272183 or placeId == 7449423635 then
    BF = true
elseif placeId == 3351674303 then
    DVE = true
end


if BF then


    if not game:IsLoaded() then
        game.Loaded:Wait()
    end
    repeat
        wait()
    until game.Players
    repeat
        wait()
    until game.Players.LocalPlayer
    repeat
        wait()
    until game.ReplicatedStorage
    repeat
        wait()
    until game.ReplicatedStorage:FindFirstChild("Remotes");
    repeat
        wait()
    until game.Players.LocalPlayer:FindFirstChild("PlayerGui");
    repeat
        wait()
    until game.Players.LocalPlayer.PlayerGui:FindFirstChild("Main");

    wait(1)

    if not game:IsLoaded() then
        repeat
            game.Loaded:Wait()
        until game:IsLoaded()
    end

    if game:GetService("Players").LocalPlayer.PlayerGui.Main:FindFirstChild("ChooseTeam") then
        repeat
            wait()
            if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
                if _G.SelectTeam == "Pirate" then
                    for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam
                                                        .Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do
                        v.Function()
                    end
                elseif _G.SelectTeam == "Marine" then
                    for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam
                                                        .Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do
                        v.Function()
                    end
                else
                    for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do
                        v.Function()
                    end
                end
            end
        until game.Players.LocalPlayer.Team ~= nil and game:IsLoaded()
    end



    game:GetService("ReplicatedStorage").Assets.GUI.DamageCounter.Enabled = false 
    AttackRandomType = 1

    ---------toool------------
    -- setclipboard(tosting(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame))

    ------------------- Save

    _G.Settings = {
        ["Select Weapon"] = "Malee", 
        ["Select Boat"] = "PirateBrigade",
        ["Auto Farm Level"] = false,
        ["Auto Electric Claw"] =false,
        ["Auto Drive Boat"]  = false,
        ["Auto Serpent Bow"] = false,
        ["Auto Serpent Bow Hop"]  = false,
        ["Auto Twin Hooks Hop"] =false,
        ["Auto Buddy Swords"] = false,
        ["Auto Buddy Swords Hop"] = false,
        ["Point"] = 3,
        ["Auto Fram Boss"] =false,
        ["Devil Fruit Sniper"] = 'Chop-Chop',
        ["MinHealth"] = 35,
        ["Fps"] = 60,
        ["Auto Look Fps"] = false,
        ["Auto Random Bone"] = false,
        ["Stop at God's Chalice"] = false,
        ["Auto Find Advanced Fruit Dealer"] =false,
        ["Auto Full Moon Hop"] = false,
        ["Auto_Stats_Devil Fruit"] = false,
        ["Auto_Stats_Gun"] = false,
        ["Auto_Stats_Sword"] = false,
        ["Auto White Screen"] =false,
        ["Auto_Stats_Defense"] = false,
        ["Auto_Stats_Melee"] = false,
        ["Auto Farm Ken"] = false,
        ["Auto Random Fruit"] =false,
        ["Auto Grab Chest"] =false,
        ["Auto Farm Dungeon"] = false,
        ["Auto Farm Ken Hop"]  = false,
        ["Auto Dragon Talon"] = false,
        ["Auto Full Moon"] = false,
        ["Auto Yama"] =false,
        ["Auto Tushita"] = false,
        ["Auto Tushita Hop"] = false,
        ["Auto Mythic Island Hop"]  = false,
        ["Auto Mythic Island"] = false,
        ["Auto Farm Bone"]  = false,
        ["Auto Start Dungeon"] =false,
        ["Auto Farm Mastery Gun"] = false,
        ["Fast Attack"] = false,
        ["Auto Kill Aura"] = false,
        ["CD Fast Attack"] = 0.3,
        ["Auto Canvander"] = false,
        ["Auto Canvander Hop"] = false,
        ["Auto Awakened"]  =false,
        ["Super Fast Attack"] = true,
        ["Auto Saber"] = false,
        ["Auto Factory Farm"] = false,
        ["Auto True Triple Katana"] = false,
        ["Auto Dark Dagger"] = false,
        ["Auto Dark Dagger Hop"] = false,
        ["Auto Twin Hooks"]  = false,
        ["Auto New World"] = false,
        ["Auto Third World"] = false,
        ["BuyHakiColor Hop"] = false,
        ["BuyHakiColor"] =false,
        ["Auto Factory Farm Hop"] = false,
        ["Auto Saber Hop"] = false,
        ["Auto Pole Hop"] = false,
        ["Auto Pole"] = false,
        ["Auto_Fram_All_Boss"] = false,
        ["AutoFramBooss"] = {},
        ["Auto Farm Fast Level"]   = false,
        ["Auto Legendary Sword"] = false,
        ["Auto Legendary Sword Hop"] = false,
        ["Auto Farm Mastery Fruits"] = false,
        ["Skill Z"] = true,
        ["Skill X"] = true,
        ["Skill C"] = true,
        ["Skill V"] = true,
        ["Auto Store Fruit"] = false,
        ["Auto Bring Fruit"] =false,
        ["Auto SuperHuman"] = false,
        ["Auto Quest Swan"] = false,
        ["Auto Farm Rengoku"] = false,
        ["Auto Farm Elite Hunter Hop"] = false,
        ["Auto Farm Elite"] = false,
        ["Auto Bartilo Quest"] = false,
        ["Auto Buy Fruit"] = false
    }

    function LoadSettings()
        if readfile and writefile and isfile and isfolder then
            if not isfolder("Nao Hub Premium Scripts") then
                makefolder("Nao Hub Premium Scripts")
            end
            if not isfolder("Nao Hub Premium Scripts/Blox Fruits/") then
                makefolder("Nao Hub Premium Scripts/Blox Fruits/")
            end
            if not isfile("Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json") then
                writefile("Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                    game:GetService("HttpService"):JSONEncode(_G.Settings))
            else
                local Decode = game:GetService("HttpService"):JSONDecode(readfile(
                    "Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json"))
                for i, v in pairs(Decode) do
                    _G.Settings[i] = v
                end
            end
        else
            return warn("Status : Undetected Executor")
        end
    end

    function SaveSettings()
        if readfile and writefile and isfile and isfolder then
            if not isfile("Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json") then
                LoadSettings()
            else
                local Decode = game:GetService("HttpService"):JSONDecode(readfile(
                    "Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json"))
                local Array = {}
                for i, v in pairs(_G.Settings) do
                    Array[i] = v
                end
                writefile("Nao Hub Premium Scripts/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                    game:GetService("HttpService"):JSONEncode(Array))
            end
        else
            return warn("Status : Undetected Executor")
        end
    end

    LoadSettings()
    --

    local id = game.PlaceId
    if id == 2753915549 then
        OldWolrd = true;
    elseif id == 4442272183 then
        SecondSea = true;
    elseif id == 7449423635 then
        ThirdSea = true;
    end

    -------------

    local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Zoydyc/HI1/main/README.md"))()
    local Wait = library.subs.Wait

    wait()



    spawn(function()
        while wait() do
            for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"]:GetChildren()) do
                pcall(function()
                    if v.Name == ("CurvedRing") or v.Name == ("SlashHit") or v.Name == ("SwordSlash") or v.Name == ("SlashTail") or v.Name == ("Sounds") then
                        v:Destroy()
                    end
                end)
            end
        end
    end)

    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") then
        game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
    end

    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn") then
        game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
    end

    if game:GetService("ReplicatedStorage").Assets:FindFirstChild('SlashHit') then
        game:GetService("ReplicatedStorage").Assets:FindFirstChild('SlashHit'):Destroy()
    end

    wait()





    local  PepsisWorld = library:CreateWindow({
        Name = 'Nao Hub Premium Scripts',
        Theme = {
            Image = "rbxassetid://7483871523",
            Info = "Info",
            Background = {
                Asset = "rbxassetid://5553946656"
            }
        }
    })

    local GeneralTab = PepsisWorld:CreateTab({
        Name = "Main"
    })


    local Second = PepsisWorld:CreateTab({
        Name = "AutoMatic"
    })

    local FarmingSection = GeneralTab:CreateSection({
        Name = "// Info //"

    })




    local MiscSection = GeneralTab:CreateSection({
        Name = "Misc",
        Side = "Right"
    })
    local StatusFm = GeneralTab:CreateSection({
        Name = "Auto Mythic Island",
        Side = "Right"
    })




    local FightStlye = GeneralTab:CreateSection({
        Name = "Auto Fighting Style",
        Side = "Right"
    })


    local MythicIsland = GeneralTab:CreateSection({
        Name = "Auto Mythic Island",
        Side = "Right"
    })

    local Moon = GeneralTab:CreateSection({
        Name = "Auto  Find Full Moon",
        Side = "Right"
    })

    local SMastery = GeneralTab:CreateSection({
        Name = "Settings Farm Mastery",
        Side = "Right"
    })

    local Mastery = GeneralTab:CreateSection({
        Name = "Farm Mastery",
        Side = "Right"
    })

    local Main = GeneralTab:CreateSection({
        Name = "// Main //"
    })

        local Boss = GeneralTab:CreateSection({
    
            Name = "// Boss //",
        })




        local Saber = GeneralTab:CreateSection({
            Name = "// Saber //"
        })
        
        local Poloev = GeneralTab:CreateSection({
            Name = "// Pole v1 //"
        })

        local LegS = GeneralTab:CreateSection({
            Name = "// Auto Legendary Sword //"
        })

        
        local Factory = GeneralTab:CreateSection({
            Name = "// Auto Factory Farm //"
        })

        local Swan = GeneralTab:CreateSection({
            Name = "// Auto Swan Glasses //"
        })
    
        local Ken = GeneralTab:CreateSection({
            Name = "// Auto Fram Ken //"
        })


        local OT = GeneralTab:CreateSection({
            Name = "// Other //"
        })














    spawn(function()
        while wait() do
            pcall(function()
                if SelectWeapon == "Melee" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings["Select Weapon"] = v.Name
                            end
                        end
                    end
                elseif SelectWeapon == "Sword" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Sword" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings["Select Weapon"] = v.Name
                            end
                        end
                    end
                elseif SelectWeapon == "Fruit" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Blox Fruit" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings["Select Weapon"] = v.Name
                            end
                        end
                    end
                else
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings["Select Weapon"] = v.Name
                            end
                        end
                    end
                end
            end)
        end
    end)

    -- Weapon = {}
    -- for i, v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    -- 	table.insert(Weapon,v.Name)
    -- end

    FarmingSection:AddLabel({
        Name = 'Enjoy Script :)'

    })

    FarmingSection:AddLabel({
        Name = 'Date | ' .. os.date("%A %B %Y")

    })

    local LabelByNino = FarmingSection:AddLabel({
        Name = 'hi'
    })

    spawn(function()
        while wait() do
            pcall(function()
                A = os.date('%X')
                LabelByNino:Set('Time | ' .. A)
                wait(1)
            end)
        end
    end)




    local click = function()
        game:GetService('VirtualUser'):CaptureController()
        game:GetService('VirtualUser'):Button1Down(Vector2.new(1280, 672))
    end





    FastAttackSet = {
        "Slow",
        "Normal",
        "Fast",
    }




    function UseCode(Text)
        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
    end

    local Code = {"EXP_5B", "CONTROL", "UPDATE11", "XMASEXP", "1BILLION", "ShutDownFix2", "UPD14", "STRAWHATMAINE",
                "TantaiGaming", "Colosseum", "Axiore", "Sub2Daigrock", "Sky Island 3", "Sub2OfficialNoobie",
                "SUB2NOOBMASTER123", "THEGREATACE", "Fountain City", "BIGNEWS", "FUDD10", "SUB2GAMERROBOT_EXP1", "UPD15",
                "2BILLION", "UPD16", "3BVISITS", "fudd10_v2", "Starcodeheo", "Magicbus","JCWK", "Bluxxy", "Sub2Fer999",
                "Enyu_is_Pro"}
    MiscSection:AddButton({
        Name = "Redeem All Code",
        Callback = function()
            for i, v in pairs(Code) do
                UseCode(v)
            end
        end
    })










    local plr = game.Players.LocalPlayer
    local CbFw = getupvalues(require(plr.PlayerScripts.CombatFramework))
    local CbFw2 = CbFw[2]

    function GetCurrentBlade() 
        local p13 = CbFw2.activeController
        local ret = p13.blades[1]
        if not ret then return end
        while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
        return ret
    end

    function AttackNoCD()
                local AC = CbFw2.activeController
                for i = 1, 1 do 
                    local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
                        plr.Character,
                        {plr.Character.HumanoidRootPart},
                        60
                    )
                    local cac = {}
                    local hash = {}
                    for k, v in pairs(bladehit) do
                        if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
                            table.insert(cac, v.Parent.HumanoidRootPart)
                            hash[v.Parent] = true
                        end
                    end
                    bladehit = cac
                    if #bladehit > 0 then
                        local u8 = debug.getupvalue(AC.attack, 5)
                        local u9 = debug.getupvalue(AC.attack, 6)
                        local u7 = debug.getupvalue(AC.attack, 4)
                        local u10 = debug.getupvalue(AC.attack, 7)
                        local u12 = (u8 * 798405 + u7 * 727595) % u9
                        local u13 = u7 * 798405
                        (function()
                            u12 = (u12 * u9 + u13) % 1099511627776
                            u8 = math.floor(u12 / u9)
                            u7 = u12 - u8 * u9
                        end)()
                        u10 = u10 + 1
                        debug.setupvalue(AC.attack, 5, u8)
                        debug.setupvalue(AC.attack, 6, u9)
                        debug.setupvalue(AC.attack, 4, u7)
                        debug.setupvalue(AC.attack, 7, u10)
                        pcall(function()
                            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then
                                AC.animator.anims.basic[1]:Play(0.01,0.01,0.01)
                                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "")
                    end
                end)
            end
        end
        if _G.Kill_Player then
            local Fast = getupvalues(require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework))
            local Lop = Fast[2]
            Lop.activeController.timeToNextAttack = (-math.huge^math.huge*math.huge)
            Lop.activeController.attacking = false
            Lop.activeController.timeToNextBlock = 0
            Lop.activeController.humanoid.AutoRotate = 80
            Lop.activeController.increment = 3
            Lop.activeController.blocking = false
            Lop.activeController.hitboxMagnitude = 80
        end
    end



    spawn(function()
        while wait(.5) do
            pcall(function()
                if _G.FastAttack2 then
                    repeat wait(_G.Fast_Delay)
                        AttackNoCD()
                    until not  _G.FastAttack2
                end
            end)
        end
    end)





    MiscSection:AddToggle({
        Name = "Fast Attack",
        Value = _G.Settings["Super Fast Attack"],
        Flag = "Fast Attack Nao Hub",
        Callback = function(value)
            _G.Settings["Super Fast Attack"] = value
            _G.FastAttack2 = value
            SaveSettings()
            if value == false then

            end
        end
    })


    MiscSection:AddSlider({
        Name = "CD Fast Attack",
        Flag = "CD Fast Attack",
        Value = _G.Settings["CD Fast Attack"],
        Min = 0.1,
        Max = 1,
        Textbox = true,
        Format = function(value)
            _G.Fast_Delay = value
            _G.Settings["CD Fast Attack"] = value
            SaveSettings()
            return "FastAttack CD : ".. tostring(value)
        end
    })




    Weapon = {"Malee", "Sword", "Fruit"}

    MiscSection:AddDropdown({
        Name = "Select Weapon",
        Value = _G.Settings["Select Weapon"], -- ค่าที่จะให้มันเลือก
        List = Weapon,
        Callback = function(value)
            SelectWeapon = value
            _G.Settings["Select Weapon"] = value
            SaveSettings()
        end
    })











    Main:AddToggle({
        Name = "Auto Farm Level",
        Value = _G.Settings["Auto Farm Level"],
        Flag = "Auto Farm Level",
        Callback = function(value)
            _G.Settings["Auto Farm Level"]  = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })

    if OldWolrd and  game:GetService("Players").LocalPlayer.Data.Level.Value <= 700 then
        Main:AddToggle({
            Name = "Auto Farm Fast Level(ฺBeta)",
            Value = _G.Settings["Auto Farm Fast Level"],
            Flag = "Auto Farm Fast Level Beta",
            Callback = function(value)
                _G.Settings["Auto Farm Fast Level"]  = value
                SaveSettings()
                if value == false then
                    pcall(function()
                        tween:Cancel() 
                    end)
                
                    _G.Kill_Player = false
                    _G.AutoFram = false
                    _G.FastFram = false
                    
                end
            end
        })
    end
    if _G.Settings["Auto Farm Fast Level"] == false then
        _G.Kill_Player = false
        _G.AutoFram = false
        _G.FastFram = false
    end


    spawn(function()
        while wait() do
            for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"]:GetChildren()) do
                pcall(function()
                    if v.Name == ("CurvedRing") or v.Name == ("SlashHit") or v.Name == ("SwordSlash") or v.Name == ("SlashTail") or v.Name == ("Sounds") then
                        v:Destroy()
                    end
                end)
            end
        end
    end)

    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") then
        game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
    end

    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn") then
        game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
    end

    if game:GetService("ReplicatedStorage").Assets:FindFirstChild('SlashHit') then
        game:GetService("ReplicatedStorage").Assets:FindFirstChild('SlashHit'):Destroy()
    end



    --  spawn(function()
    --      pcall(function()
    --          game:GetService("RunService").Stepped:Connect(function()
    --              if _G.Settings['Auto Farm Level'] or _G.Auto_New_World or _G.Auto_Third_World or _G.Doing_Items_Or_Quest then
    --                  if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
    --                      local Noclip = Instance.new("BodyVelocity")
    --                      Noclip.Name = "BodyClip"
    --                      Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
    --                      Noclip.MaxForce = Vector3.new(100000,100000,100000)
    --                      Noclip.Velocity = Vector3.new(0,0,0)
    --                  end
    --                  if syn then
    --                      setfflag("HumanoidParallelRemoveNoPhysics", "False")
    --                      setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
    --                  end
    --              else	
    --                  if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
    --                      game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
    --                  end
    --              end
    --          end)
    --      end)
    --  end)

    --  spawn(function()
    --      pcall(function()
    --          game:GetService("RunService").Stepped:Connect(function()
    --              if _G.Settings['Auto Farm Level'] or _G.Auto_New_World or _G.Auto_Third_World or _G.Doing_Items_Or_Quest or _G.No_Clip then
    --                  for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
    --                      if v:IsA("BasePart") then
    --                          v.CanCollide = false
    --                      end
    --                  end
    --              end
    --          end)
    --      end)
    --  end)




    task.spawn(function()
        while task.wait() do 
            if  _G.Settings["Auto Farm Fast Level"] then 
                    if _G.AutoShanda  then
                    _G.FastFram = true
                    _G.Kill_Player = false
                    _G.AutoFram = false
                    elseif not _G.AutoShanda and _G.AutoFramPly then
                    _G.FastFram = false
                    _G.Kill_Player = true
                    _G.AutoFram = false
                    elseif _G.AutoShanda and not _G.AutoFramPly then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                    elseif not _G.AutoShanda and not _G.AutoFramPly then
                        _G.FastFram = false
                        _G.Kill_Player = false
                        _G.AutoFram = true
                    end
                end
        end
    end)



    task.spawn(function()
        while wait() do
            if  _G.Settings["Auto Farm Fast Level"] then 
                if OldWolrd then
                    Playersv = #game:GetService("Players"):GetPlayers()
                    LVA = game:GetService("Players").LocalPlayer.Data.Level.Value
                    if LVA == 1 or LVA <= 10 then
                        _G.AutoFramPly = false
                        _G.AutoShanda = false
                    elseif LVA == 11 or LVA <= 75 then
                        -- print(1)
                        _G.AutoFramPly = false
                        _G.AutoShanda = true         
                    elseif LVA >= 76 and Playersv >= 6 then
                    pcall(function()
                        
                    
                        if game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                            if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter"), "I don't have anything") then
                                _G.AutoFramPly = false
                                _G.AutoShanda = false
                            else
                                _G.AutoFramPly = true
                                _G.AutoShanda = false
                            end
                        end
                    end)
                    elseif LVA >= 76 and Playersv <= 5 then
                        -- print(3)
                        _G.AutoFramPly = false
                        _G.AutoShanda = false
                    else
                        
                        _G.AutoFramPly = false
                        _G.AutoShanda = false
                    end              
                elseif SecondSea or ThirdSea then
                    -- print(4)
                    _G.AutoFramPly = false
                    _G.AutoShanda = false
                end
            end
        end
    end)












    Main:AddToggle({
        Name = "Auto New World",
        Value = _G.Settings["Auto New World"],
        Flag = "Auto New World",
        Callback = function(value)
            _G.AutoNewWorld = value
            FastAttack = value
            if value == false then
                two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                _G.AutoNewWorld = false
            end
        end
    })

    Main:AddToggle({
        Name = "Auto Third World",
        Value = _G.Settings["Auto Third World"],
        Flag = "Auto Third World",
        Callback = function(value)
            _G.Settings["Auto Third World"] = value
            _G.ThirdSea  = value
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })


    if OldWolrd then
    Saber:AddToggle({
        Name = "Auto Saber",
        Value = _G.Settings["Auto Saber"] ,
        Flag = "Auto Saber",
        Callback = function(value)
            _G.Saber = value
            FastAttack = value
            _G.Settings["Auto Saber"] = value
            SaveSettings()
            if value == false then
                tween:Cancel()
                _G.Noclip = false
                _G.Saber =false
            end
        end
    })

    Saber:AddToggle({
        Name = "Auto Saber Hop",
        Value = _G.Settings["Auto Saber Hop"] ,
        Flag = "Auto Saber Hop",
        Callback = function(value)
            _G.Settings["Auto Saber Hop"] = value
            _G.SaberHop = value
            SaveSettings()
            if value == false then
                tween:Cancel()
                _G.Noclip = false
                _G.Saber =false
            end
        end
    })


    Poloev:AddToggle({
        Name = "Auto Pole v1",
        Value = _G.Settings["Auto Pole"],
        Flag = "Auto Pole v1",
        Callback = function(value)
            _G.AutoPole1 = value
            _G.Settings["Auto Pole"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })

    Poloev:AddToggle({
        Name = "Auto Pole v1 Hop",
        Value = _G.Settings["Auto Pole Hop"],
        Flag = "Auto Pole v1 Hop",
        Callback = function(value)
            _G.Settings["Auto Pole Hop"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })
    end
    ---------- S C R I P T -----------------



    -----------



    ---Fast test

    -----------

    -- ท่าไม่ทำงานแก้เป็น

    -----------

    ----------------





    function CheckQuest()
        local MYLEVEL = game:GetService("Players").LocalPlayer.Data.Level.Value
        if OldWolrd then
            if MYLEVEL == 1 or MYLEVEL <= 9 then
                Ms = "Bandit [Lv. 5]"
                NameQuest = "BanditQuest1"
                QuestLv = 1
                NameQ = "Bandit"
                CFrameQ = CFrame.new(1060.0158691406, 16.424287796021, 1547.9769287109)
                CFramePuk = CFrame.new(1073.86414, 16.2736206, 1612.17163, -0.695649207, 0, -0.718381643, 0, 1, 0,
                    0.718381643, 0, -0.695649207)
                NM = 'Windmill'
            elseif MYLEVEL == 10 or MYLEVEL <= 14 then
                Ms = "Monkey [Lv. 14]"
                NameQuest = "JungleQuest"
                QuestLv = 1
                NameQ = "Monkey"
                CFrameQ = CFrame.new(-1601.52808, 36.9774551, 152.812317, -0.0892550573, -7.99012057e-08, -0.996008813,
                    -4.66281733e-08, 1, -7.60429089e-08, 0.996008813, 3.96548572e-08, -0.0892550573)
                CFramePuk = CFrame.new(-1609.71216, 39.8521576, 123.384674, 0.708323717, 6.74341152e-08, 0.705887735,
                    -1.86098941e-08, 1, -7.68568071e-08, -0.705887735, 4.13030072e-08, 0.708323717)
            elseif MYLEVEL == 15 or MYLEVEL <= 29 then
                magbring = 240
                Ms = "Gorilla [Lv. 20]"
                NameQuest = "JungleQuest"
                QuestLv = 2
                NameQ = "Gorilla"
                CFrameQ = CFrame.new(-1600.24353, 36.8521347, 153.224792, 0.0664860159, 1.09421023e-07, -0.997787356,
                    9.55680779e-09, 1, 1.10300476e-07, 0.997787356, -1.68691017e-08, 0.0664860159)
                CFramePuk = CFrame.new(-1260.29321, 18.6214619, -398.3508, 0.816335142, 5.76316722e-07, -0.577578545,
                    8.32609999e-08, 1, 1.11549434e-06, 0.577578545, -9.58707005e-07, 0.816335142)
            elseif MYLEVEL == 30 or MYLEVEL <= 39 then
                Ms = "Pirate [Lv. 35]"
                NameQuest = "BuggyQuest1"
                QuestLv = 1
                NameQ = "Pirate"
                CFrameQ = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0,
                    0.258804798, 0, 0.965929627)
                CFramePuk = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0,
                    0.258804798, 0, 0.965929627)
            elseif MYLEVEL == 40 or MYLEVEL <= 59 then
                Ms = "Brute [Lv. 45]"
                NameQuest = "BuggyQuest1"
                QuestLv = 2
                NameQ = "Brute"
                CFrameQ = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0,
                    0.258804798, 0, 0.965929627)
                CFramePuk = CFrame.new(-1144.44861, 90.5594559, 4307.25928, -0.998438537, 0, 0.0558618344, 0, 1, 0,
                    -0.0558618344, 0, -0.998438537)
            elseif MYLEVEL == 60 or MYLEVEL <= 74 then
                Ms = "Desert Bandit [Lv. 60]"
                NameQuest = "DesertQuest"
                QuestLv = 1
                NameQ = "Desert Bandit"
                CFrameQ = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0,
                    0.573571265, 0, 0.819155693)
                CFramePuk = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0,
                    0.573571265, 0, 0.819155693)
            elseif MYLEVEL == 75 or MYLEVEL <= 89 then
                Ms = "Desert Officer [Lv. 70]"
                NameQuest = "DesertQuest"
                QuestLv = 2
                NameQ = "Desert Officer"
                CFrameQ = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0,
                    0.573571265, 0, 0.819155693)
                CFramePuk = CFrame.new(1580.03198, 4.61375761, 4366.86426)
            elseif MYLEVEL == 90 or MYLEVEL <= 99 then
                Ms = "Snow Bandit [Lv. 90]"
                NameQuest = "SnowQuest"
                QuestLv = 1
                NameQ = "Snow Bandit"
                CFrameQ = CFrame.new(1384.01538, 87.272789, -1296.28137, 0.462413222, -7.79864777e-08, -0.88666451,
                    -1.42050363e-08, 1, -9.53630916e-08, 0.88666451, 5.6692258e-08, 0.462413222)
                CFramePuk = CFrame.new(1372.84326, 105.990303, -1422.19507, 0.719091773, -2.12436309e-08, 0.694915235,
                    9.82151036e-08, 1, -7.10619616e-08, -0.694915235, 1.19351228e-07, 0.719091773)
            elseif MYLEVEL == 100 or MYLEVEL <= 119 then
                Ms = "Snowman [Lv. 100]"
                NameQuest = "SnowQuest"
                QuestLv = 2
                NameQ = "Snowman"
                CFrameQ = CFrame.new(1384.01538, 87.272789, -1296.28137, 0.462413222, -7.79864777e-08, -0.88666451,
                    -1.42050363e-08, 1, -9.53630916e-08, 0.88666451, 5.6692258e-08, 0.462413222)
                CFramePuk = CFrame.new(1220.92712, 138.011871, -1489.01208, 0.389352709, -7.53626693e-07, 0.921088696,
                    1.45705499e-07, 1, 7.56600116e-07, -0.921088696, -1.60376572e-07, 0.389352709)
            elseif MYLEVEL == 120 or MYLEVEL <= 149 then
                Ms = "Chief Petty Officer [Lv. 120]"
                NameQuest = "MarineQuest2"
                QuestLv = 1
                NameQ = "Chief Petty Officer"
                CFrameQ = CFrame.new(-5034.64893, 28.6520348, 4324.53369, -0.0616381466, 5.83357576e-08, 0.998098552,
                    -1.59750098e-08, 1, -5.9433436e-08, -0.998098552, -1.96080023e-08, -0.0616381466)
                CFramePuk = CFrame.new(-4863.61328, 22.6520348, 4306.39307, 0.536051273, 7.00434066e-09, -0.844185412,
                    -5.8011751e-10, 1, 7.92878918e-09, 0.844185412, -3.76051057e-09, 0.536051273)
            elseif MYLEVEL == 150 or MYLEVEL <= 174 then
                Ms = "Sky Bandit [Lv. 150]"
                NameQuest = "SkyQuest"
                QuestLv = 1
                NameQ = "Sky Bandit"
                CFrameQ = CFrame.new(-4843.2041, 717.669617, -2623.13159, -0.775086224, -1.6359829e-08, -0.631855488,
                    -4.10942462e-08, 1, 2.45178793e-08, 0.631855488, 4.49690951e-08, -0.775086224)
                CFramePuk = CFrame.new(-4970.74219, 294.544342, -2890.11353, -0.994874597, -8.61311165e-08, -0.101116329,
                    -9.10836278e-08, 1, 4.43614923e-08, 0.101116329, 5.33441664e-08, -0.994874597)
            elseif MYLEVEL == 175 or MYLEVEL <= 189 then
                Ms = "Dark Master [Lv. 175]"
                NameQuest = "SkyQuest"
                QuestLv = 2
                NameQ = "Dark Master"
                CFrameQ = CFrame.new(-4843.2041, 717.669617, -2623.13159, -0.775086224, -1.6359829e-08, -0.631855488,
                    -4.10942462e-08, 1, 2.45178793e-08, 0.631855488, 4.49690951e-08, -0.775086224)
                CFramePuk = CFrame.new(-5239.94629, 392.217102, -2208.18335, 0.969297886, -5.95604988e-09, -0.245889395,
                    3.87897714e-09, 1, -8.93151775e-09, 0.245889395, 7.70350184e-09, 0.969297886)
            elseif MYLEVEL == 190 or MYLEVEL <= 209 then
                Ms = "Prisoner [Lv. 190]"
                NameQuest = "PrisonerQuest"
                QuestLv = 1
                NameQ = "Prisoner"
                CFrameQ = CFrame.new(5307.95166015625, 1.6809712648391724, 475.1698913574219)
                CFramePuk = CFrame.new(5029.708984375, 68.67806243896484, 445.857177734375)
            elseif MYLEVEL == 210 or MYLEVEL <= 249 then
                Ms = "Dangerous Prisoner [Lv. 210]"
                NameQuest = "PrisonerQuest"
                QuestLv = 2
                NameQ = "Dangerous Prisoner"
                CFrameQ = CFrame.new(5307.95166015625, 1.6809712648391724, 475.1698913574219)
                CFramePuk = CFrame.new(5673.51758, 68.6786652, 783.757629, -0.0514698699, 7.78369369e-08, 0.998674572,
                    8.35602094e-08, 1, -7.36337e-08, -0.998674572, 7.96595359e-08, -0.0514698699)
            elseif MYLEVEL == 250 or MYLEVEL <= 299 then
                Ms = "Toga Warrior [Lv. 250]"
                NameQuest = "ColosseumQuest"
                QuestLv = 1
                NameQ = "Toga Warrior"
                CFrameQ = CFrame.new(-1575.72961, 7.38933659, -2983.39453, 0.52762109, -1.48187587e-06, 0.849479854,
                    2.69328297e-07, 1, 1.57716818e-06, -0.849479854, -6.0335816e-07, 0.52762109)
                CFramePuk = CFrame.new(-1819.12415, 7.28907108, -2744.02539, 0.547199547, 2.10840998e-08, -0.837002158,
                    -1.27399286e-10, 1, 2.51067309e-08, 0.837002158, -1.36317579e-08, 0.547199547)
            elseif MYLEVEL == 300 or MYLEVEL <= 324 then
                Ms = "Military Soldier [Lv. 300]"
                NameQuest = "MagmaQuest"
                QuestLv = 1
                NameQ = "Military Soldier"
                CFrameQ = CFrame.new(-5316.33887, 12.236989, 8517.67285, 0.499506682, -5.08374072e-08, -0.86631006,
                    -1.30872131e-08, 1, -6.62286652e-08, 0.86631006, 4.44192452e-08, 0.499506682)
                CFramePuk = CFrame.new(-5419.0752, 10.9255161, 8464.50488, -0.637788415, -4.55103836e-05, 0.770211577,
                    7.05542743e-06, 1, 6.49305366e-05, -0.770211577, 4.68461185e-05, -0.637788415)
            elseif MYLEVEL == 325 or MYLEVEL <= 374 then
                Ms = "Military Spy [Lv. 325]"
                NameQuest = "MagmaQuest"
                QuestLv = 2
                NameQ = "Military Spy"
                CFrameQ = CFrame.new(-5316.33887, 12.236989, 8517.67285, 0.499506682, -5.08374072e-08, -0.86631006,
                    -1.30872131e-08, 1, -6.62286652e-08, 0.86631006, 4.44192452e-08, 0.499506682)
                CFramePuk = CFrame.new(-5805.42041, 99.5276108, 8782.36719, -0.316935152, -6.4923519e-08, 0.948447227,
                    4.12987404e-08, 1, 8.2252896e-08, -0.948447227, 6.52385026e-08, -0.316935152)
            elseif MYLEVEL == 375 or MYLEVEL <= 399 then
                Ms = "Fishman Warrior [Lv. 375]"
                NameQuest = "FishmanQuest"
                QuestLv = 1
                NameQ = "Fishman Warrior"
                CFrameQ = CFrame.new(61122.2422, 18.4716377, 1568.84778, 0.971045971, -1.77007031e-08, 0.238892734,
                    4.80190776e-09, 1, 5.45760841e-08, -0.238892734, -5.18487475e-08, 0.971045971)
                CFramePuk = CFrame.new(60898.043, 18.4828224, 1550.9906, -0.0750192106, -4.46996573e-09, 0.997182071,
                    3.6461556e-10, 1, 4.51002746e-09, -0.997182071, 7.0192685e-10, -0.0750192106)
                if    (_G.AutoFram  or  _G.Settings["Auto Farm Level"]) and
                    (CFrameQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(61163.8516, 5.43263245, 1819.78418, 1, 6.89280011e-09, 9.74497786e-14, -6.89280011e-09,
                            1, 3.38349579e-08, -9.72165599e-14, -3.38349579e-08, 1))
                end
            elseif MYLEVEL == 400 or MYLEVEL <= 449 then
                Ms = "Fishman Commando [Lv. 400]"
                NameQuest = "FishmanQuest"
                QuestLv = 2
                NameQ = "Fishman Commando"
                CFrameQ = CFrame.new(61122.2422, 18.4716377, 1568.84778, 0.971045971, -1.77007031e-08, 0.238892734,
                    4.80190776e-09, 1, 5.45760841e-08, -0.238892734, -5.18487475e-08, 0.971045971)
                CFramePuk = CFrame.new(61885.4063, 18.4828224, 1500.37195, 0.722261012, 4.84021889e-08, -0.691620588,
                    1.27929427e-08, 1, 8.33434299e-08, 0.691620588, -6.90435726e-08, 0.722261012)
                if    (_G.AutoFram  or  _G.Settings["Auto Farm Level"])and
                    (CFrameQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(61163.8516, 5.43263245, 1819.78418, 1, 6.89280011e-09, 9.74497786e-14, -6.89280011e-09,
                            1, 3.38349579e-08, -9.72165599e-14, -3.38349579e-08, 1))
                end
            elseif MYLEVEL == 450 or MYLEVEL <= 474 then
                Ms = "God's Guard [Lv. 450]"
                NameQuest = "SkyExp1Quest"
                QuestLv = 1
                NameQ = "God's Guard"
                CFrameQ = CFrame.new(-4721.28369, 845.277161, -1954.95154, -0.979754269, -1.72096932e-08, 0.200205252,
                    -2.52417198e-09, 1, 7.36076018e-08, -0.200205252, 7.16119786e-08, -0.979754269)
                CFramePuk = CFrame.new(-4630.00635, 866.902954, -1936.76331, -0.656243384, 9.12737941e-12, 0.754549265,
                    3.58402819e-09, 1, 3.10498938e-09, -0.754549265, 4.74195483e-09, -0.656243384)
                if    (_G.AutoFram  or  _G.Settings["Auto Farm Level"])and
                    (CFrameQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance", Vector3.new(
                        -4607.82275, 872.54248, -1667.55688))
                end
            elseif MYLEVEL == 475 or MYLEVEL <= 524 then
                Ms = "Shanda [Lv. 475]"
                NameQuest = "SkyExp1Quest"
                QuestLv = 2
                NameQ = "Shanda"
                CFrameQ = CFrame.new(-7861.79736, 5545.49316, -379.920776, 0.504107952, -1.41941534e-08, -0.863640666,
                    -1.31181936e-08, 1, -2.40923566e-08, 0.863640666, 2.34745521e-08, 0.504107952)
                CFramePuk = CFrame.new(-7682.69775, 5607.36279, -445.691833, 0.786274791, -4.48163426e-08, -0.617877364,
                    -4.81674345e-09, 1, -7.86622607e-08, 0.617877364, 6.48263239e-08, 0.786274791)
                if    (_G.AutoFram  or  _G.Settings["Auto Farm Level"])and
                    (CFrameQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance", Vector3.new(
                        -7894.6176757813, 5547.1416015625, -380.29119873047))
                end
            elseif MYLEVEL == 525 or MYLEVEL <= 549 then
                Ms = "Royal Squad [Lv. 525]"
                NameQuest = "SkyExp2Quest"
                QuestLv = 1
                NameQ = "Royal Squad"
                CFrameQ = CFrame.new(-7902.23242, 5635.96387, -1411.96741, -0.0435957126, -2.13718043e-09, 0.999049246,
                    4.23562352e-10, 1, 2.15769735e-09, -0.999049246, 5.1722604e-10, -0.0435957126)
                CFramePuk = CFrame.new(-7579.42285, 5628.39111, -1540.75073, -0.0374937952, 1.17099557e-08, 0.999296963,
                    -3.30279164e-08, 1, -1.29574085e-08, -0.999296963, -3.34905081e-08, -0.0374937952)
            elseif MYLEVEL == 550 or MYLEVEL <= 624 then
                Ms = "Royal Soldier [Lv. 550]"
                NameQuest = "SkyExp2Quest"
                QuestLv = 2
                NameQ = "Royal Soldier"
                CFrameQ = CFrame.new(-7902.23242, 5635.96387, -1411.96741, -0.0435957126, -2.13718043e-09, 0.999049246,
                    4.23562352e-10, 1, 2.15769735e-09, -0.999049246, 5.1722604e-10, -0.0435957126)
                CFramePuk = CFrame.new(-7834.84717, 5681.36182, -1790.76782, -0.102890432, 3.28112684e-08, 0.994692683,
                    -6.45397762e-08, 1, -3.96622966e-08, -0.994692683, -6.82781121e-08, -0.102890432)
            elseif MYLEVEL == 625 or MYLEVEL <= 649 then
                Ms = "Galley Pirate [Lv. 625]"
                NameQuest = "FountainQuest"
                QuestLv = 1
                NameQ = "Galley Pirate"
                CFrameQ = CFrame.new(5254.52734, 38.5011368, 4049.80127, -0.0732342899, 2.23174847e-08, -0.997314751,
                    1.2052287e-07, 1, 1.35274023e-08, 0.997314751, -1.19208565e-07, -0.0732342899)
                CFramePuk = CFrame.new(5597.58936, 41.5013657, 3960.55371, -0.584786832, 4.98908861e-08, 0.811187029,
                    4.10757259e-08, 1, -3.18919575e-08, -0.811187029, 1.4670098e-08, -0.584786832)
            elseif MYLEVEL >= 650 then
                Ms = "Galley Captain [Lv. 650]"
                NameQuest = "FountainQuest"
                QuestLv = 2
                NameQ = "Galley Captain"
                CFrameQ = CFrame.new(5254.52734, 38.5011368, 4049.80127, -0.0732342899, 2.23174847e-08, -0.997314751,
                    1.2052287e-07, 1, 1.35274023e-08, 0.997314751, -1.19208565e-07, -0.0732342899)
                CFramePuk = CFrame.new(5705.8252, 52.241478, 4890.11035, -0.969319642, 4.40228476e-09, 0.245803744,
                    -7.88622412e-09, 1, -4.90088397e-08, -0.245803744, -4.94436954e-08, -0.969319642)
            end
        end
        if SecondSea then
            if MYLEVEL == 700 or MYLEVEL <= 724 then
                Ms = "Raider [Lv. 700]"
                NameQuest = "Area1Quest"
                QuestLv = 1
                NameQ = "Raider"
                CFrameQ = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601,
                    -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
                CFramePuk = CFrame.new(-737.026123, 39.1748352, 2392.57959)
            elseif MYLEVEL == 725 or MYLEVEL <= 774 then
                Ms = "Mercenary [Lv. 725]"
                NameQuest = "Area1Quest"
                QuestLv = 2
                NameQ = "Mercenary"
                CFrameQ = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601,
                    -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
                CFramePuk = CFrame.new(-938.497314, 80.9546738, 1443.98608, 0.231955677, 0, 0.972726345, -0, 1, -0,
                    -0.972726345, 0, 0.231955677)
            elseif MYLEVEL == 775 or MYLEVEL <= 874 then
                Ms = "Swan Pirate [Lv. 775]"
                NameQuest = "Area2Quest"
                QuestLv = 1
                NameQ = "Swan Pirate"
                CFrameQ = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771,
                    1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
                CFramePuk = CFrame.new(967.233276, 141.309494, 1210.06384, 0.999673784, 5.40161649e-09, -0.0255404469,
                    -7.62258967e-09, 1, -8.68617107e-08, 0.0255404469, 8.7028063e-08, 0.999673784)
            elseif MYLEVEL == 875 or MYLEVEL <= 899 then
                Ms = "Marine Lieutenant [Lv. 875]"
                NameQuest = "MarineQuest3"
                QuestLv = 1
                NameQ = "Marine Lieutenant."
                CFrameQ = CFrame.new(-2443.04639, 73.0161057, -3220.30225, -0.854058921, -6.13997599e-08, -0.520176232,
                    -1.30658604e-08, 1, -9.65840883e-08, 0.520176232, -7.56919505e-08, -0.854058921)
                CFramePuk = CFrame.new(-2967.00757, 72.9661407, -2972.7478, 0.977851391, 8.27619218e-08, -0.209300488,
                    -6.95268412e-08, 1, 7.05923142e-08, 0.209300488, -5.44767893e-08, 0.977851391)
            elseif MYLEVEL == 900 or MYLEVEL <= 949 then
                Ms = "Marine Captain [Lv. 900]"
                NameQuest = "MarineQuest3"
                QuestLv = 2
                NameQ = "Marine Captain"
                CFrameQ = CFrame.new(-2443.04639, 73.0161057, -3220.30225, -0.854058921, -6.13997599e-08, -0.520176232,
                    -1.30658604e-08, 1, -9.65840883e-08, 0.520176232, -7.56919505e-08, -0.854058921)
                CFramePuk = CFrame.new(-1818.36401, 93.3760834, -3203.57788, 0.315930545, 4.84752114e-08, 0.948782325,
                    1.37578589e-08, 1, -5.56731905e-08, -0.948782325, 3.06420738e-08, 0.315930545)
            elseif MYLEVEL == 950 or MYLEVEL <= 974 then
                Ms = "Zombie [Lv. 950]"
                NameQuest = "ZombieQuest"
                QuestLv = 1
                NameQ = "Zombie"
                CFrameQ = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742,
                    4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
                CFramePuk = CFrame.new(-5736.03516, 126.031998, -728.026184, 0.0818082988, -5.90035434e-08, 0.996648133,
                    3.5947787e-09, 1, 5.89069167e-08, -0.996648133, -1.23634614e-09, 0.0818082988)
            elseif MYLEVEL == 975 or MYLEVEL <= 999 then
                Ms = "Vampire [Lv. 975]"
                NameQuest = "ZombieQuest"
                QuestLv = 2
                NameQ = "Vampire"
                CFrameQ = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742,
                    4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)
                CFramePuk = CFrame.new(-6028.23584, 6.40270138, -1295.4563, 0.667547405, 0, 0.744567394, -0, 1.00000012, -0,
                    -0.744567394, 0, 0.667547405)
            elseif MYLEVEL == 1000 or MYLEVEL <= 1049 then
                Ms = "Snow Trooper [Lv. 1000]"
                NameQuest = "SnowMountainQuest"
                QuestLv = 1
                NameQ = "Snow Trooper"
                CFrameQ = CFrame.new(605.670532, 401.422028, -5370.10107, 0.459257662, -9.56824509e-10, -0.888303101,
                    5.98925964e-10, 1, -7.67489405e-10, 0.888303101, -1.79552401e-10, 0.459257662)
                CFramePuk = CFrame.new(544.207947, 401.422028, -5309.08887, 0.503866196, -2.06684501e-08, 0.86378175,
                    1.27917943e-09, 1, 2.31816841e-08, -0.86378175, -1.05755351e-08, 0.503866196)
            elseif MYLEVEL == 1050 or MYLEVEL <= 1099 then
                Ms = "Winter Warrior [Lv. 1050]"
                NameQuest = "SnowMountainQuest"
                QuestLv = 2
                NameQ = "Winter Warrior"
                CFrameQ = CFrame.new(605.670532, 401.422028, -5370.10107, 0.459257662, -9.56824509e-10, -0.888303101,
                    5.98925964e-10, 1, -7.67489405e-10, 0.888303101, -1.79552401e-10, 0.459257662)
                CFramePuk = CFrame.new(1240.86279, 461.108154, -5191.104, 0.528719008, -7.18234645e-08, 0.848796904,
                    2.89169716e-10, 1, 8.44378363e-08, -0.848796904, -4.4398444e-08, 0.528719008)
            elseif MYLEVEL == 1100 or MYLEVEL <= 1124 then
                Ms = "Lab Subordinate [Lv. 1100]"
                NameQuest = "IceSideQuest"
                QuestLv = 1
                NameQ = "Lab Subordinate"
                CFrameQ = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528,
                    1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
                CFramePuk = CFrame.new(-5833.63379, 48.4371948, -4510.4458, 0.0372838341, 5.56001822e-09, -0.999304712,
                    -6.95599089e-09, 1, 5.30436006e-09, 0.999304712, 6.75338763e-09, 0.0372838341)
            elseif MYLEVEL == 1125 or MYLEVEL <= 1174 then
                Ms = "Horned Warrior [Lv. 1125]"
                NameQuest = "IceSideQuest"
                QuestLv = 2
                NameQ = "Horned Warrior"
                CFrameQ = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528,
                    1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)
                CFramePuk = CFrame.new(-6168.15918, 42.7079964, -6020.96826, -0.744210601, 2.41774178e-09, -0.667945027,
                    -2.3336304e-09, 1, 6.21975493e-09, 0.667945027, 6.18754425e-09, -0.744210601)
            elseif MYLEVEL == 1175 or MYLEVEL <= 1199 then
                Ms = "Magma Ninja [Lv. 1175]"
                NameQuest = "FireSideQuest"
                QuestLv = 1
                NameQ = "Magma Ninja"
                CFrameQ = CFrame.new(-5429.68359, 15.9517593, -5296.70215, 0.919959962, -6.00166317e-08, -0.392012328,
                    2.29238974e-08, 1, -9.93018858e-08, 0.392012328, 8.23673076e-08, 0.919959962)
                CFramePuk = CFrame.new(-5404.85449, 22.8623676, -5896.09033, -0.519595861, 4.74720929e-09, 0.854412138,
                    1.52255595e-08, 1, 3.70304742e-09, -0.854412138, 1.49329917e-08, -0.519595861)
            elseif MYLEVEL == 1200 or MYLEVEL <= 1249 then
                Ms = "Lava Pirate [Lv. 1200]"
                NameQuest = "FireSideQuest"
                QuestLv = 2
                NameQ = "Lava Pirate"
                CFrameQ = CFrame.new(-5429.68359, 15.9517593, -5296.70215, 0.919959962, -6.00166317e-08, -0.392012328,
                    2.29238974e-08, 1, -9.93018858e-08, 0.392012328, 8.23673076e-08, 0.919959962)
                CFramePuk = CFrame.new(-5075.1958, 16.1485081, -4814.36133, -0.800640523, -1.06090866e-07, 0.599145055,
                    -6.59776447e-08, 1, 8.89041587e-08, -0.599145055, 3.16500923e-08, -0.800640523)
            elseif MYLEVEL == 1250 or MYLEVEL <= 1274 then
                Ms = "Ship Deckhand [Lv. 1250]"
                NameQuest = "ShipQuest1"
                QuestLv = 1
                NameQ = "Ship Deckhand"
                CFrameQ = CFrame.new(1038.67456, 125.057098, 32911.3477, 0.120709591, 5.22710089e-08, -0.992687881,
                    7.9174507e-09, 1, 5.36187876e-08, 0.992687881, -1.43318593e-08, 0.120709591)
                CFramePuk = CFrame.new(1215.14063, 125.057114, 33050.7188, 0.527230442, 2.61814961e-08, 0.849722326,
                    -5.66963045e-08, 1, 4.36674741e-09, -0.849722326, -5.04783984e-08, 0.527230442)
            elseif MYLEVEL == 1275 or MYLEVEL <= 1299 then
                Ms = "Ship Engineer [Lv. 1275]"
                NameQuest = "ShipQuest1"
                QuestLv = 2
                NameQ = "Ship Engineer"
                CFrameQ = CFrame.new(1038.67456, 125.057098, 32911.3477, 0.120709591, 5.22710089e-08, -0.992687881,
                    7.9174507e-09, 1, 5.36187876e-08, 0.992687881, -1.43318593e-08, 0.120709591)
                CFramePuk = CFrame.new(862.985413, 40.4428635, 32867.9492, -0.847809434, 8.49998827e-08, -0.530301034,
                    2.99658929e-08, 1, 1.1237865e-07, 0.530301034, 7.93847335e-08, -0.847809434)
            elseif MYLEVEL == 1300 or MYLEVEL <= 1324 then
                Ms = "Ship Steward [Lv. 1300]"
                NameQuest = "ShipQuest2"
                QuestLv = 1
                NameQ = "Ship Steward"
                CFrameQ = CFrame.new(969.268311, 125.057121, 33245.2695, -0.85863924, -4.77058464e-08, -0.512580395,
                    -1.49134394e-08, 1, -6.80880134e-08, 0.512580395, -5.08187057e-08, -0.85863924)
                CFramePuk = CFrame.new(923.611511, 129.555984, 33442.3125, 0.997516274, 9.71936913e-08, 0.0704362914,
                    -9.52239958e-08, 1, -3.13219992e-08, -0.0704362914, 2.45369804e-08, 0.997516274)
            elseif MYLEVEL == 1325 or MYLEVEL <= 1349 then
                Ms = "Ship Officer [Lv. 1325]"
                NameQuest = "ShipQuest2"
                QuestLv = 2
                NameQ = "Ship Officer"
                CFrameQ = CFrame.new(969.268311, 125.057121, 33245.2695, -0.85863924, -4.77058464e-08, -0.512580395,
                    -1.49134394e-08, 1, -6.80880134e-08, 0.512580395, -5.08187057e-08, -0.85863924)
                CFramePuk = CFrame.new(882.275574, 181.057739, 33354.1797, 0.845816016, -3.71928088e-08, -0.533474684,
                    1.28583932e-09, 1, -6.7679359e-08, 0.533474684, 5.65583242e-08, 0.845816016)
            elseif MYLEVEL == 1350 or MYLEVEL <= 1374 then
                Ms = "Arctic Warrior [Lv. 1350]"
                NameQuest = "FrostQuest"
                QuestLv = 1
                NameQ = "Arctic Warrior"
                CFrameQ = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226,
                    -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
                CFramePuk = CFrame.new(5995.9292, 57.0727844, -6184.98926, 0.706337512, 5.23128296e-09, -0.707875192,
                    -2.2285974e-08, 1, -1.48474424e-08, 0.707875192, 2.62629936e-08, 0.706337512)
            elseif MYLEVEL == 1375 or MYLEVEL <= 1424 then
                Ms = "Snow Lurker [Lv. 1375]"
                NameQuest = "FrostQuest"
                QuestLv = 2
                NameQ = "Snow Lurker"
                CFrameQ = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226,
                    -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)
                CFramePuk = CFrame.new(5516.27539, 60.5209846, -6830.82764, 0.219563305, -7.8544824e-09, 0.975598276,
                    4.69439376e-09, 1, 6.99444236e-09, -0.975598276, 3.04411962e-09, 0.219563305)
            elseif MYLEVEL == 1425 or MYLEVEL <= 1449 then
                Ms = "Sea Soldier [Lv. 1425]"
                NameQuest = "ForgottenQuest"
                QuestLv = 1
                NameQ = "Sea Soldier"
                CFrameQ = CFrame.new(-3053.97339, 236.846283, -10146.1484, -0.999963522, -2.10707256e-08, -0.00854360498,
                    -2.09657198e-08, 1, -1.23802275e-08, 0.00854360498, -1.22006529e-08, -0.999963522)
                CFramePuk = CFrame.new(-3026.54834, 29.5403671, -9758.74316, -0.999909937, 1.71713896e-08, -0.0134194754,
                    1.68009748e-08, 1, 2.7715517e-08, 0.0134194754, 2.74875607e-08, -0.999909937)
            elseif MYLEVEL >= 1450 then
                Ms = "Water Fighter [Lv. 1450]"
                NameQuest = "ForgottenQuest"
                QuestLv = 2
                NameQ = "Water Fighter"
                CFrameQ = CFrame.new(-3053.97339, 236.846283, -10146.1484, -0.999963522, -2.10707256e-08, -0.00854360498,
                    -2.09657198e-08, 1, -1.23802275e-08, 0.00854360498, -1.22006529e-08, -0.999963522)
                CFramePuk = CFrame.new(-3262.00098, 298.699615, -10553.6943, -0.233570755, -4.57538185e-08, 0.972339869,
                    -5.80986068e-08, 1, 3.30992194e-08, -0.972339869, -4.87605725e-08, -0.233570755)
            end
        end
        if ThirdSea then
            if MYLEVEL == 1500 or MYLEVEL <= 1524 then
                Ms = "Pirate Millionaire [Lv. 1500]"
                NameQuest = "PiratePortQuest"
                QuestLv = 1
                NameQ = "Pirate Millionaire"
                CFrameQ = CFrame.new(-288.998016, 43.7932205, 5577.68994, -0.943210304, -8.05650799e-08, 0.332196265,
                    -9.89928779e-08, 1, -3.85495724e-08, -0.332196265, -6.92454165e-08, -0.943210304)
                CFramePuk = CFrame.new(-91.8906479, 75.3287811, 5647.7002, 0.571274579, 8.47636343e-08, -0.820758998,
                    -9.5655281e-08, 1, 3.66955462e-08, 0.820758998, 5.75466998e-08, 0.571274579)
            elseif MYLEVEL == 1525 or MYLEVEL <= 1574 then
                Ms = "Pistol Billionaire [Lv. 1525]"
                NameQuest = "PiratePortQuest"
                QuestLv = 2
                NameQ = "Pistol Billionaire"
                CFrameQ = CFrame.new(-288.998016, 43.7932205, 5577.68994, -0.943210304, -8.05650799e-08, 0.332196265,
                    -9.89928779e-08, 1, -3.85495724e-08, -0.332196265, -6.92454165e-08, -0.943210304)
                CFramePuk = CFrame.new(-740.71814, 130.458511, 5869.8623, 0.26613301, -6.96497509e-08, 0.963936329,
                    -2.79989738e-08, 1, 7.99857816e-08, -0.963936329, -4.82760854e-08, 0.26613301)
            elseif MYLEVEL == 1575 or MYLEVEL <= 1599 then
                Ms = "Dragon Crew Warrior [Lv. 1575]"
                NameQuest = "AmazonQuest"
                QuestLv = 1
                NameQ = "Dragon Crew Warrior"
                CFrameQ = CFrame.new(5834.86035, 51.3513641, -1103.34705, -0.919929087, 6.43650253e-08, 0.392084718,
                    7.08298344e-08, 1, 2.02354311e-09, -0.392084718, 2.96328135e-08, -0.919929087)
                CFramePuk = CFrame.new(6498.88623, 51.4962921, -1011.49811, -0.844736993, -1.62814184e-09, -0.535181701,
                    4.04657037e-08, 1, -6.69137634e-08, 0.535181701, -7.81810314e-08, -0.844736993)
            elseif MYLEVEL == 1600 or MYLEVEL <= 1624 then
                Ms = "Dragon Crew Archer [Lv. 1600]"
                NameQuest = "AmazonQuest"
                QuestLv = 2
                NameQ = "Dragon Crew Archer"
                CFrameQ = CFrame.new(5834.86035, 51.3513641, -1103.34705, -0.919929087, 6.43650253e-08, 0.392084718,
                    7.08298344e-08, 1, 2.02354311e-09, -0.392084718, 2.96328135e-08, -0.919929087)
                CFramePuk = CFrame.new(6608.45605, 378.396393, 235.665527, -0.647212744, -5.41171872e-08, 0.762309432,
                    -5.96274674e-08, 1, 2.0366441e-08, -0.762309432, -3.22731637e-08, -0.647212744)
            elseif MYLEVEL == 1625 or MYLEVEL <= 1649 then
                Ms = "Female Islander [Lv. 1625]"
                NameQuest = "AmazonQuest2"
                QuestLv = 1
                NameQ = "Female Islander"
                CFrameQ = CFrame.new(5445.11426, 601.603638, 751.129517, -0.346766561, 5.00326642e-08, -0.937951446,
                    4.48732145e-08, 1, 3.67525779e-08, 0.937951446, -2.93443314e-08, -0.346766561)
                CFramePuk = CFrame.new(4758.92871, 730.33374, 800.998047, -0.100775175, -5.07539504e-08, -0.994909227,
                    -2.28484591e-08, 1, -4.86993095e-08, 0.994909227, 1.78244619e-08, -0.100775175)
            elseif MYLEVEL == 1650 or MYLEVEL <= 1699 then
                Ms = "Giant Islander [Lv. 1650]"
                NameQuest = "AmazonQuest2"
                QuestLv = 2
                NameQ = "Giant Islander"
                CFrameQ = CFrame.new(5445.11426, 601.603638, 751.129517, -0.346766561, 5.00326642e-08, -0.937951446,
                    4.48732145e-08, 1, 3.67525779e-08, 0.937951446, -2.93443314e-08, -0.346766561)
                CFramePuk = CFrame.new(4736.1333, 601.373596, -123.942299, -0.651415646, 1.13692966e-08, -0.758721054,
                    1.02050288e-08, 1, 6.2230785e-09, 0.758721054, -3.6889598e-09, -0.651415646)
            elseif MYLEVEL == 1700 or MYLEVEL <= 1724 then
                Ms = "Marine Commodore [Lv. 1700]"
                NameQuest = "MarineTreeIsland"
                QuestLv = 1
                NameQ = "Marine Commodore"
                CFrameQ = CFrame.new(2180.83911, 28.7054462, -6739.44824, 0.977863014, 6.92042956e-09, -0.20924598,
                    -1.01339639e-08, 1, -1.42855736e-08, 0.20924598, 1.60898246e-08, 0.977863014)
                CFramePuk = CFrame.new(2447, 73.1255493, -7470, 1, 4.06989891e-08, 4.79087976e-15, -4.06989891e-08, 1,
                    2.86651343e-08, -3.62423799e-15, -2.86651343e-08, 1)
            elseif MYLEVEL == 1725 or MYLEVEL <= 1774 then
                Ms = "Marine Rear Admiral [Lv. 1725]"
                NameQuest = "MarineTreeIsland"
                QuestLv = 2
                NameQ = "Marine Rear Admiral"
                CFrameQ = CFrame.new(2180.83911, 28.7054462, -6739.44824, 0.977863014, 6.92042956e-09, -0.20924598,
                    -1.01339639e-08, 1, -1.42855736e-08, 0.20924598, 1.60898246e-08, 0.977863014)
                CFramePuk = CFrame.new(3660.3833, 160.524063, -6971.11328, 0.771100104, -4.33134666e-08, -0.636713922,
                    -7.22266069e-09, 1, -7.67736665e-08, 0.636713922, 6.37989501e-08, 0.771100104)
            elseif MYLEVEL == 1775 or MYLEVEL <= 1800 then
                Ms = "Fishman Raider [Lv. 1775]"
                NameQuest = "DeepForestIsland3"
                QuestLv = 1
                NameQ = "Fishman Raider"
                CFrameQ = CFrame.new(-10582.7578, 331.762634, -8758.56543, 0.911287963, 8.23484143e-08, -0.411769718,
                    -7.27268628e-08, 1, 3.90346848e-08, 0.411769718, -5.62511859e-09, 0.911287963)
                CFramePuk = CFrame.new(-10615.6611, 331.762634, -8446.38574, 0.30275172, -4.96152719e-09, -0.953069448,
                    -2.92618618e-09, 1, -6.13537132e-09, 0.953069448, 4.64635308e-09, 0.30275172)
            elseif MYLEVEL == 1800 or MYLEVEL <= 1824 then
                Ms = "Fishman Captain [Lv. 1800]"
                NameQuest = "DeepForestIsland3"
                QuestLv = 2
                NameQ = "Fishman Captain"
                CFrameQ = CFrame.new(-10582.7578, 331.762634, -8758.56543, 0.911287963, 8.23484143e-08, -0.411769718,
                    -7.27268628e-08, 1, 3.90346848e-08, 0.411769718, -5.62511859e-09, 0.911287963)
                CFramePuk = CFrame.new(-11040.3467, 331.762634, -8957.75684, -0.990780294, -5.54384094e-08, 0.135478467,
                    -4.7334634e-08, 1, 6.30372483e-08, -0.135478467, 5.60432376e-08, -0.990780294)
            elseif MYLEVEL == 1825 or MYLEVEL <= 1849 then
                Ms = "Forest Pirate [Lv. 1825]"
                NameQuest = "DeepForestIsland"
                QuestLv = 1
                NameQ = "Forest Pirate"
                CFrameQ = CFrame.new(-13233.2686, 332.378143, -7627.66455, -0.905921221, 2.69652856e-09, 0.423446268,
                    2.31737229e-09, 1, -1.41026579e-09, -0.423446268, -2.96307007e-10, -0.905921221)
                CFramePuk = CFrame.new(-13479, 332.378143, -7905, 1, -1.27257813e-08, 2.41825958e-15, 1.27257813e-08, 1,
                    -8.67651977e-08, -1.3141047e-15, 8.67651977e-08, 1)
            elseif MYLEVEL == 1850 or MYLEVEL <= 1899 then
                Ms = "Mythological Pirate [Lv. 1850]"
                NameQuest = "DeepForestIsland"
                QuestLv = 2
                NameQ = "Mythological Pirate"
                CFrameQ = CFrame.new(-13233.2686, 332.378143, -7627.66455, -0.905921221, 2.69652856e-09, 0.423446268,
                    2.31737229e-09, 1, -1.41026579e-09, -0.423446268, -2.96307007e-10, -0.905921221)
                CFramePuk = CFrame.new(-13676.1553, 469.788086, -6999.65527, 0.693832397, -2.62738986e-08, 0.720136523,
                    -4.52658462e-08, 1, 8.00970454e-08, -0.720136523, -8.8171511e-08, 0.693832397)
            elseif MYLEVEL == 1900 or MYLEVEL <= 1924 then
                Ms = "Jungle Pirate [Lv. 1900]"
                NameQuest = "DeepForestIsland2"
                QuestLv = 1
                NameQ = "Jungle Pirate"
                CFrameQ = CFrame.new(-12682.1279, 390.860687, -9901.89746, 0.00872628205, 1.59673574e-09, -0.999961913,
                    -5.25600941e-09, 1, 1.55092938e-09, 0.999961913, 5.2422755e-09, 0.00872628205)
                CFramePuk = CFrame.new(-12107, 331.738281, -10549, 1, -2.50327403e-09, -6.22370418e-15, 2.50327403e-09, 1,
                    8.81249651e-09, 6.20164405e-15, -8.81249651e-09, 1)
            elseif MYLEVEL == 1925 or MYLEVEL <= 1974 then
                Ms = "Musketeer Pirate [Lv. 1925]"
                NameQuest = "DeepForestIsland2"
                QuestLv = 2
                NameQ = "Musketeer Pirate"
                CFrameQ = CFrame.new(-12682.1279, 390.860687, -9901.89746, 0.00872628205, 1.59673574e-09, -0.999961913,
                    -5.25600941e-09, 1, 1.55092938e-09, 0.999961913, 5.2422755e-09, 0.00872628205)
                CFramePuk = CFrame.new(-13485.2305, 432.682373, -9857.01074, 0.994504631, 1.2369239e-08, -0.104692325,
                    -8.4907642e-10, 1, 1.1008283e-07, 0.104692325, -1.09388999e-07, 0.994504631)
            elseif MYLEVEL == 1975 or MYLEVEL <= 1999 then
                Ms = "Reborn Skeleton [Lv. 1975]"
                NameQuest = "HauntedQuest1"
                QuestLv = 1
                NameQ = "Reborn Skeleton"
                CFrameQ = CFrame.new(-9482.11035, 142.104828, 5566.32861, 0.0620567501, -4.18429273e-08, -0.998072624,
                    -3.89895867e-08, 1, -4.43479706e-08, 0.998072624, 4.1666528e-08, 0.0620567501)
                CFramePuk = CFrame.new(-8762.33496, 142.104828, 6015.7627, -0.999993861, -2.26600214e-08, 0.00350279221,
                    -2.28456738e-08, 1, -5.29611519e-08, -0.00350279221, -5.30408499e-08, -0.999993861)
            elseif MYLEVEL == 2000 or MYLEVEL <= 2024 then
                Ms = "Living Zombie [Lv. 2000]"
                NameQuest = "HauntedQuest1"
                QuestLv = 2
                NameQ = "Living Zombie"
                CFrameQ = CFrame.new(-9482.11035, 142.104828, 5566.32861, 0.0620567501, -4.18429273e-08, -0.998072624,
                    -3.89895867e-08, 1, -4.43479706e-08, 0.998072624, 4.1666528e-08, 0.0620567501)
                CFramePuk = CFrame.new(-10099.1494, 138.626678, 5930.86279, 0.241616711, -9.62791873e-08, -0.970371783,
                    5.61582709e-08, 1, -8.52357971e-08, 0.970371783, -3.39000081e-08, 0.241616711)
            elseif MYLEVEL == 2025 or MYLEVEL <= 2049 then
                Ms = "Demonic Soul [Lv. 2025]"
                NameQuest = "HauntedQuest2"
                QuestLv = 1
                NameQ = "Demonic Soul"
                CFrameQ = CFrame.new(-9514.25195, 172.104828, 6077.22998, 0.0446508788, -7.60616636e-09, 0.999002635,
                    7.97889257e-08, 1, 4.04755696e-09, -0.999002635, 7.95286255e-08, 0.0446508788)
                CFramePuk = CFrame.new(-9513.54199, 172.104828, 6143.45459, -0.777332306, -2.16450324e-08, -0.62909019,
                    -5.07872073e-08, 1, 2.83480883e-08, 0.62909019, 5.39856195e-08, -0.777332306)
            elseif MYLEVEL == 2050 or MYLEVEL <= 2074 then
                Ms = "Posessed Mummy [Lv. 2050]"
                NameQuest = "HauntedQuest2"
                QuestLv = 2
                NameQ = "Posessed Mummy"
                CFrameQ = CFrame.new(-9514.25195, 172.104828, 6077.22998, 0.0446508788, -7.60616636e-09, 0.999002635,
                    7.97889257e-08, 1, 4.04755696e-09, -0.999002635, 7.95286255e-08, 0.0446508788)
                CFramePuk = CFrame.new(-9580.24609, 5.79254198, 6190.47852, 0.462460369, 5.16216367e-08, -0.886639953,
                    -7.72594788e-08, 1, 1.79240605e-08, 0.886639953, 6.0212173e-08, 0.462460369)
            elseif MYLEVEL == 2075 or MYLEVEL <= 2099 then
                Ms = "Peanut Scout [Lv. 2075]"
                NameQuest = "NutsIslandQuest"
                QuestLv = 1
                NameQ = "Peanut Scout"
                CFrameQ = CFrame.new(-2103.18872, 38.1041794, -10193.7656, 0.7310462, 2.46138327e-08, 0.682327926,
                    -5.02823738e-09, 1, -3.06860635e-08, -0.682327926, 1.90020231e-08, 0.7310462)
                CFramePuk = CFrame.new(-2221.45996, 38.103817, -10086.0762, -0.994582355, 2.09503472e-08, 0.103951879,
                    2.41223095e-08, 1, 2.92565758e-08, -0.103951879, 3.16056337e-08, -0.994582355)
            elseif MYLEVEL == 2100 or MYLEVEL <= 2124 then
                Ms = "Peanut President [Lv. 2100]"
                NameQuest = "NutsIslandQuest"
                QuestLv = 2
                NameQ = "Peanut President"
                CFrameQ = CFrame.new(-2103.18872, 38.1041794, -10193.7656, 0.7310462, 2.46138327e-08, 0.682327926,
                    -5.02823738e-09, 1, -3.06860635e-08, -0.682327926, 1.90020231e-08, 0.7310462)
                CFramePuk = CFrame.new(-2171.88647, 88.2396011, -10531.9512, 0.691500723, 5.31482591e-08, -0.722375751,
                    -2.70291771e-08, 1, 4.7700329e-08, 0.722375751, -1.34595908e-08, 0.691500723)
            elseif MYLEVEL == 2125 or MYLEVEL <= 2149 then
                Ms = "Ice Cream Chef [Lv. 2125]"
                NameQuest = "IceCreamIslandQuest"
                QuestLv = 1
                NameQ = "Ice Cream Chef"
                CFrameQ = CFrame.new(-820.991455, 65.8195343, -10965.4316, 0.832442105, 3.44203599e-08, -0.554112017,
                    -3.14893249e-08, 1, 1.48116621e-08, 0.554112017, 5.11876364e-09, 0.832442105)
                CFramePuk = CFrame.new(-761.110657, 164.200974, -10929.7031, -0.903523564, -2.8124143e-08, 0.428538442,
                    -5.52620127e-09, 1, 5.39766987e-08, -0.428538442, 4.64010306e-08, -0.903523564)
            elseif MYLEVEL == 2150 or MYLEVEL <= 2199 then
                Ms = "Ice Cream Commander [Lv. 2150]"
                NameQuest = "IceCreamIslandQuest"
                QuestLv = 2
                NameQ = "Ice Cream Commander"
                CFrameQ = CFrame.new(-820.991455, 65.8195343, -10965.4316, 0.832442105, 3.44203599e-08, -0.554112017,
                    -3.14893249e-08, 1, 1.48116621e-08, 0.554112017, 5.11876364e-09, 0.832442105)
                CFramePuk = CFrame.new(-683.515137, 97.7532196, -11270.5254, -0.249526113, -3.42524373e-08, -0.968368053,
                    -4.59147245e-08, 1, -2.35401334e-08, 0.968368053, 3.85884746e-08, -0.249526113)
            elseif MYLEVEL == 2200 or MYLEVEL <= 2224 then
                Ms = "Cookie Crafter [Lv. 2200]"
                NameQuest = "CakeQuest1"
                QuestLv = 1
                NameQ = "Cookie Crafter"
                CFrameQ = CFrame.new(-2021.28113, 37.7982178, -12027.1602, 0.876975715, 2.42050024e-08, 0.480534643,
                    -1.83145179e-08, 1, -1.69469878e-08, -0.480534643, 6.06133632e-09, 0.876975715)
                CFramePuk = CFrame.new(-2362.1604, 37.7981148, -12116.2031, 0.428214997, 1.03298156e-07, 0.903676867,
                    -1.24923467e-08, 1, -1.08389123e-07, -0.903676867, 3.51248026e-08, 0.428214997)
            elseif MYLEVEL == 2225 or MYLEVEL <= 2249 then
                Ms = "Cake Guard [Lv. 2225]"
                NameQuest = "CakeQuest1"
                QuestLv = 2
                NameQ = "Cake Guard"
                CFrameQ = CFrame.new(-2021.28113, 37.7982178, -12027.1602, 0.876975715, 2.42050024e-08, 0.480534643,
                    -1.83145179e-08, 1, -1.69469878e-08, -0.480534643, 6.06133632e-09, 0.876975715)
                CFramePuk = CFrame.new(-1560.17944, 37.7981339, -12440.5781, -0.560352206, 1.90654585e-08, -0.828254402,
                    6.60573107e-08, 1, -2.16719656e-08, 0.828254402, -6.68561952e-08, -0.560352206)
            elseif MYLEVEL == 2250 or MYLEVEL <= 2274 then
                Ms = "Baking Staff [Lv. 2250]"
                NameQuest = "CakeQuest2"
                QuestLv = 1
                NameQ = "Baking Staff"
                CFrameQ = CFrame.new(-1929.3186, 37.7981339, -12843.3857, -0.994816065, 6.2958283e-09, 0.101690687,
                    6.02614314e-09, 1, -2.95921043e-09, -0.101690687, -2.33106734e-09, -0.994816065)
                CFramePuk = CFrame.new(-1874.04688, 74.015831, -13002.7959, 0.958144426, -9.20437699e-08, -0.286285222,
                    1.05663617e-07, 1, 3.21261275e-08, 0.286285222, -6.10314004e-08, 0.958144426)
            elseif MYLEVEL == 2275 or MYLEVEL <= 2299 then
                Ms = "Head Baker [Lv. 2275]"
                NameQuest = "CakeQuest2"
                QuestLv = 2
                NameQ = "Head Baker"
                CFrameQ = CFrame.new(-1929.3186, 37.7981339, -12843.3857, -0.994816065, 6.2958283e-09, 0.101690687,
                    6.02614314e-09, 1, -2.95921043e-09, -0.101690687, -2.33106734e-09, -0.994816065)
                CFramePuk = CFrame.new(-2205.25171, 108.351257, -12784.6475, 0.999649942, 1.09295986e-08, -0.0264567528,
                    -9.22357479e-09, 1, 6.46055156e-08, 0.0264567528, -6.43388702e-08, 0.999649942)
            elseif MYLEVEL == 2300 or MYLEVEL <= 2324 then
                Ms = "Cocoa Warrior [Lv. 2300]"
                NameQuest = "ChocQuest1"
                QuestLv = 1
                NameQ = "Cocoa Warrior"
                CFrameQ = CFrame.new(231.562515, 24.7342396, -12196.9277, 0.996608198, -4.87148775e-08, -0.0822927728,
                    4.61355079e-08, 1, -3.32453354e-08, 0.0822927728, 2.93359523e-08, 0.996608198)
                CFramePuk = CFrame.new(-26.0082874, 24.7343502, -12253.001, -0.17375651, 7.9442728e-08, 0.984788656,
                    1.18449632e-08, 1, -7.85798946e-08, -0.984788656, -1.98898231e-09, -0.17375651)
            elseif MYLEVEL == 2325 or MYLEVEL <= 2349 then
                Ms = "Chocolate Bar Battler [Lv. 2325]"
                NameQuest = "ChocQuest1"
                QuestLv = 2
                NameQ = "Chocolate Bar Battler"
                CFrameQ = CFrame.new(231.562515, 24.7342396, -12196.9277, 0.996608198, -4.87148775e-08, -0.0822927728,
                    4.61355079e-08, 1, -3.32453354e-08, 0.0822927728, 2.93359523e-08, 0.996608198)
                CFramePuk = CFrame.new(715.227661, 64.5699463, -12601.4971, 0.375136077, -3.84623213e-08, 0.926969767,
                    1.12107639e-08, 1, 3.69556403e-08, -0.926969767, -3.47135498e-09, 0.375136077)
            elseif MYLEVEL == 2350 or MYLEVEL <= 2374 then
                Ms = "Sweet Thief [Lv. 2350]"
                NameQuest = "ChocQuest2"
                QuestLv = 1
                NameQ = "Sweet Thief"
                CFrameQ = CFrame.new(147.670837, 24.7938328, -12775.2656, -0.274139136, 7.20163911e-08, -0.961690068,
                    7.48291242e-08, 1, 5.35544693e-08, 0.961690068, -5.72810492e-08, -0.274139136)
                CFramePuk = CFrame.new(59.2454491, 57.2388878, -12634.1523, 0.97673136, -3.85135479e-08, 0.214466438,
                    3.43798909e-08, 1, 2.30041923e-08, -0.214466438, -1.50955834e-08, 0.97673136)
            elseif MYLEVEL == 2375 or MYLEVEL <= 2400 then
                Ms = "Candy Rebel [Lv. 2375]"
                NameQuest = "ChocQuest2"
                QuestLv = 2
                NameQ = "Candy Rebel"
                CFrameQ = CFrame.new(147.670837, 24.7938328, -12775.2656, -0.274139136, 7.20163911e-08, -0.961690068,
                    7.48291242e-08, 1, 5.35544693e-08, 0.961690068, -5.72810492e-08, -0.274139136)
                CFramePuk = CFrame.new(72.7375183, 24.7938499, -12939.2383, -0.87948513, 9.16761138e-08, -0.47592634,
                    7.88268579e-08, 1, 4.69590802e-08, 0.47592634, 3.78403309e-09, -0.87948513)
            elseif MYLEVEL == 2400 or MYLEVEL <= 2425 then
                Ms = "Candy Pirate [Lv. 2400]"
                NameQuest = "CandyQuest1"
                QuestLv = 1
                NameQ = "Candy Pirate"
                CFrameQ = CFrame.new(-1151.48987, 16.1422901, -14445.6904, -0.316594511, -6.85698254e-08, -0.948560953, -2.05343067e-08, 1, -6.54346692e-08, 0.948560953, -1.23821675e-09, -0.316594511)
                CFramePuk = CFrame.new(-1408.46521, 16.1423531, -14552.2041, 0.90175873, -8.17216943e-08, -0.432239741, 7.81264475e-08, 1, -2.60746162e-08, 0.432239741, -1.02563433e-08, 0.90175873)
        elseif MYLEVEL >=  2426 then
                Ms = "Snow Demon [Lv. 2425]"
                NameQuest = "CandyQuest1"
                QuestLv = 2
                NameQ = "Snow Demon"
                CFrameQ = CFrame.new(-1151.48987, 16.1422901, -14445.6904, -0.316594511, -6.85698254e-08, -0.948560953, -2.05343067e-08, 1, -6.54346692e-08, 0.948560953, -1.23821675e-09, -0.316594511)
                CFramePuk = CFrame.new(-777.070862, 23.5809536, -14453.0078, 0.33384338, 0, -0.942628562, 0, 1, 0, 0.942628562, 0, 0.33384338)
            end
        end
    end




    function two(gotoCFrame)
        pcall(function()
            game.Players.LocalPlayer.Character.Humanoid.Sit = false
        end)
        if (game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').Position -
            gotoCFrame.Position).Magnitude <= 250 then
            pcall(function()
                tween:Cancel()
            end)
            game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').CFrame = gotoCFrame
        else
            local tween_s = game:service "TweenService"
            local info = TweenInfo.new(
                (game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').Position -
                    gotoCFrame.Position).Magnitude / 300, Enum.EasingStyle.Linear)
            local tween, err = pcall(function()
                tween = tween_s:Create(game.Players.LocalPlayer.Character:WaitForChild('HumanoidRootPart'), info, {
                    CFrame = gotoCFrame
                })
                tween:Play()
            end)
            if not tween then
                return err
            end
        end
    end






    -- function tp(p)
    --     spawn(function()
    --         pcall(function()
    --             repeat task.wait()  
    --                 game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true        
    --                 game.Players.LocalPlayer.Character.Humanoid:ChangeState(15)
    --                 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p         
    --                 game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true 
    --                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
    --                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
    --             until game.Players.LocalPlayer.Character.Humanoid.Health > 0
    --             game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
    --         end)
    --     end)
    -- end


    spawn(function()
        while wait() do
            if _G.WARP then
                game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
            else
                game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
            end
        end
    end)



        

    local canwarp = true
    
    local tp = function(p)
        xenon = 0
            if canwarp then
                canwarp = false
                spawn(function()
                    pcall(function()
                    repeat wait(.1)
                        game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p * CFrame.new(0, math.random(100, 200), 0)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p * CFrame.new(math.random(100, 200), 0, 0)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p * CFrame.new(0, 0, math.random(100, 200))
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        game.Players.LocalPlayer.Character.Humanoid:ChangeState(15)
                        game.Players.LocalPlayer.Character.Humanoid.Health = 0
                        game.Players.LocalPlayer.Character.Head:Destroy()
                        game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
                        wait()
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        game.Players.LocalPlayer.Character.Humanoid:ChangeState(14)
                    until game.Players.LocalPlayer.Character.Humanoid.Health > 0
                    end)
                end)
            end
            wait(7)
            canwarp = true
    end


    local canwarp = true
    -- local tp = function(p)
    --     if canwarp then
    --             game.Players.LocalPlayer.Character.Humanoid:ChangeState(15)
    --             game.Players.LocalPlayer.Character.Humanoid.Health = 0
    --             game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true 
    --             repeat wait()               
    --                 game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
    --                 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p * CFrame.new(0, math.random(100, 200), 0)
    -- 			until (p.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude < 1500 and game.Players.LocalPlayer.Character.Humanoid.Health > 0
    -- 			game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
    --     end
    -- end





    -- local tp = function(p)
    --     xenon = 0
    --         if canwarp then
    --             canwarp = false
    --             spawn(function()
    --                 pcall(function()                 
    --                 repeat wait()  
    --                     game.Players.LocalPlayer.Character.Humanoid.Health = 0                                   
    --                     game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
    --                     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =  p
    --                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
    --                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
    --                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")                                   
    --                 until game.Players.LocalPlayer.Character.Humanoid.Health > 0 and  (p.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude < 1500
    --                 end)
    --             end)
    --         end
    --         wait(10)
    --         canwarp = true
    -- end












    spawn(function()
        while wait() do
            repeat wait() until game.CoreGui:FindFirstChild('RobloxPromptGui')
            local lp,po,ts = game:GetService('Players').LocalPlayer,game.CoreGui.RobloxPromptGui.promptOverlay,game:GetService('TeleportService')							
            po.ChildAdded:connect(function(a)
                if a.Name == 'ErrorPrompt' then
                    repeat wait()
                        ts:Teleport(game.PlaceId)
                        wait(2)
                    until false
                end
            end)
        end
    end)

    spawn(function()
        pcall(function()
            game:GetService("RunService").Stepped:Connect(function()
                if _G.SrepentBow or _G.Settings["Auto Buddy Swords"] or _G.CakePrince or BoneFarm or _G.MythicIsland  or  _G.RainbowHaki  or Noclipboat or _G.Settings["Auto Twin Hooks"] or _G.Settings["Auto Grab Chest"] or _G.Settings["Auto Canvander"] or _G.MidNight or _G.Settings["Auto Dark Dagger"] or _G.Settings["Auto Farm Elite"] or _G.ThirdSea  or NoclipBoos or  _G.Kill_Player  or GrabChest or _G.FramBoos   or _G.BringFruit or _G.BartiloQuest  or GrabChest or _G.Deathstepv2 or  AutoNext or _G.FramKen or _G.SwanGalss or  _G.SharkmanKarate or _G.Rengoku or _G.Starttw or _G.Saber or _G.Noclip or _G.AutoFram or _G.FramSuper or
                _G.FastFram or _G.RiadSuper or _G.Settings["Auto Farm Level"] or _G.AutoPole1 or _G.All_Boss or _G.Settings["Auto_Fram_All_Boss"] or _G.Settings["Auto Farm Mastery Fruits"] or  _G.Auto_Mastery_Gun then
                    if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                        local Noclip = Instance.new("BodyVelocity")
                        Noclip.Name = "BodyClip"
                        Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                        Noclip.MaxForce = Vector3.new(100000,100000,100000)
                        Noclip.Velocity = Vector3.new(0,0,0)
                    end
                else	
                    if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                        game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                    end
                end
            end)
        end)
    end)
    
    spawn(function()
        pcall(function()
            game:GetService("RunService").Stepped:Connect(function()
                if _G.SrepentBow or _G.Settings["Auto Buddy Swords"] or _G.CakePrince or BoneFarm  or Noclipboat or _G.MythicIsland or _G.RainbowHaki or _G.Settings["Auto Twin Hooks"] or _G.Settings["Auto Grab Chest"] or _G.Settings["Auto Canvander"]  or _G.MidNight  or _G.Settings["Auto Dark Dagger"] or _G.Settings["Auto Farm Elite"] or _G.ThirdSea or NoclipBoos or  _G.Kill_Player  or _G.FramBoos   or _G.BringFruit or _G.BartiloQuest  or GrabChest or _G.Deathstepv2 or  AutoNext or _G.FramKen or _G.SwanGalss or  _G.SharkmanKarate or _G.Rengoku or _G.Starttw or _G.Saber or _G.Noclip or _G.AutoFram or _G.FramSuper or
                    _G.FastFram or _G.RiadSuper or _G.Settings["Auto Farm Level"] or _G.AutoPole1 or _G.All_Boss or _G.Settings["Auto_Fram_All_Boss"] or _G.Settings["Auto Farm Mastery Fruits"] or  _G.Auto_Mastery_Gun then
                    for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("BasePart") then
                            v.CanCollide = false    
                        end
                    end
                end
            end)
        end)
    end)









    function itemequip(ToolSe)
        if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
            tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
            wait(.1)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
        end
    end
























    spawn(function()
        while wait() do
            if _G.FastFram   then
                pcall(function()
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true   then
                        canq()
                    end
                    if game:GetService("Workspace").Enemies:FindFirstChild('Shanda [Lv. 475]') then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == 'Shanda [Lv. 475]' then
                                repeat wait( 0.2)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                    end
                                    itemequip(_G.Settings["Select Weapon"])
                                
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                    v.Humanoid.JumpPower = 0
                                    StartMagnetFast = true
                                    v.Humanoid.WalkSpeed = 0
                                    PosMon =  v.HumanoidRootPart.CFrame 
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
        
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                until _G.FastFram == false or v.Humanoid.Health <= 0

                                StartMagnetFast = false
                            end
                        end
                    else
                        cfs = CFrame.new(-7682.69775, 5607.36279, -445.691833, 0.786274791, -4.48163426e-08, -0.617877364,
                            -4.81674345e-09, 1, -7.86622607e-08, 0.617877364, 6.48263239e-08, 0.786274791)
                        if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - cfs.Position).Magnitude <= 500 then
                            two(cfs)
                        else
                            wait(.6)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance", Vector3.new(
                                -7894.6176757813, 5547.1416015625, -380.29119873047))
                        end
                    end

                end)
            end
        end
    end)



    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function() 
            pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if  StartMagnetFast and  (v.HumanoidRootPart.Position - PosMon.Position).magnitude <= 350 then
                            v.HumanoidRootPart.CFrame = PosMon
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
            end)
        end)
    end)





















    function RobloxNotify(tap,sec)
        game.StarterGui:SetCore("SendNotification", {
            Title = "Nao Notification", 
            Text = tostring(tap),
            Icon = "http://www.roblox.com/asset/?id=12711996278",
            Duration = sec
        })
    end

    function checksaber()
        local args = {
            [1] = "LoadItem",
            [2] = "Saber"
        }

        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end

    randdomsaber = 0
    spawn(function()
        while wait() do
            if _G.Saber then
                pcall(function()
                    checksaber()
                    if CheckSw("Saber") then
                        
                    elseif not CheckSw("Saber") then
                        if game:GetService("Players").LocalPlayer.Data.Level.Value >= 200 then

                        if game:GetService("Workspace").Map.Jungle.Final.Part.Transparency == 0 then

                            if game:GetService("Workspace").Map.Jungle.QuestPlates.Door.Transparency == 0 then
                                chekcjg = CFrame.new(-1614.4032, 36.852108, 149.662994, -0.850639939, -3.75066485e-08, -0.52574873, -2.10141184e-08, 1, -3.73395075e-08, 0.52574873, -2.07143316e-08, -0.850639939)
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position -chekcjg.Position).Magnitude <= 1799 then
                                wait(5.5)
                                two(game:GetService("Workspace").Map.Jungle.QuestPlates.Plate1.Button.CFrame)
                                wait(5.5)
                                two(game:GetService("Workspace").Map.Jungle.QuestPlates.Plate2.Button.CFrame)
                                wait(5.5)
                                two(game:GetService("Workspace").Map.Jungle.QuestPlates.Plate3.Button.CFrame)
                                wait(5.5)
                                    two(game:GetService("Workspace").Map.Jungle.QuestPlates.Plate4.Button.CFrame)
                                wait(5.5)
                                two(game:GetService("Workspace").Map.Jungle.QuestPlates.Plate5.Button.CFrame)
                                wait(5.5)
                                else
                                    tp(chekcjg)
                                end
                                
                            else

                                if game:GetService("Workspace").Map.Desert.Burn.Part.Transparency == 0 then
                                    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Torch") or
                                        game.Players.LocalPlayer.Character:FindFirstChild("Torch") then
                                        itemequip("Torch")
                                        TorchCFrame = CFrame.new(1114.61475, 5.04679728, 4350.22803, -0.648466587,
                                            -1.28799094e-09, 0.761243105, -5.70652914e-10, 1, 1.20584542e-09, -0.761243105,
                                            3.47544882e-10, -0.648466587)
                                        if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position -
                                            TorchCFrame.Position).Magnitude <= 3 then
                                            _G.Saber = false
                                            wait(3)
                                            _G.Saber = true
                                        else
                                            two(TorchCFrame)
                                        end

                                    else
                                        repeat wait()
                                            two(CFrame.new(-1610.00757, 11.5049858, 164.001587, 0.984807551, -0.167722285,
                                            -0.0449818149, 0.17364943, 0.951244235, 0.254912198, 3.42372805e-05,
                                            -0.258850515, 0.965917408))
                                            _G.Saber = false
                                            wait(3)
                                            _G.Saber = true
                                        until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Torch") 
                                    end

                                else
                                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress",
                                        "SickMan") ~= 0 then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress",
                                            "GetCup")
                                        wait(0.5)
                                        itemequip("Cup")
                                        wait(0.5)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress",
                                            "FillCup", game:GetService("Players").LocalPlayer.Character.Cup)
                                        wait(0)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress",
                                            "SickMan")
                                    else
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "ProQuestProgress", "RichSon") == nil then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "ProQuestProgress", "RichSon")
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "ProQuestProgress", "RichSon") == 0 then
                                        
                                            if game:GetService("Workspace").Enemies:FindFirstChild("Mob Leader [Lv. 120] [Boss]") then
                                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                    if v.Name == "Mob Leader [Lv. 120] [Boss]" then
                                                        if v:FindFirstChild('Humanoid') then   
                                                        repeat
                                                            wait()
                                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                            end
                                                            itemequip(_G.Settings["Select Weapon"])
                                                            -- FastAttack = true
                                                            if AttackRandomType == 1 then
                                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                                            elseif AttackRandomType == 2 then
                                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                                            elseif AttackRandomType == 3 then
                                                                two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                                            elseif AttackRandomType == 4 then
                                                                two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                                            elseif AttackRandomType == 5 then
                                                                two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                                            end
                                                            v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                                            v.Humanoid.JumpPower = 0
                                                            v.Humanoid.WalkSpeed = 0
                                                            v.HumanoidRootPart.CanCollide = false
                                                            v.Humanoid:ChangeState(14)
                                                            cilck()
                                                        until v.Humanoid.Health <= 0 or _G.Saber == false                 
                                                    end
                                                end
                                            end
                                                else
                                                    two(CFrame.new(-2880.71631, 28.693943, 5430.854, 0.882951856, 0,
                                                        -0.469463557, 0, 1, 0, 0.469463557, 0, 0.882951856))                                     
                                            end
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "ProQuestProgress", "RichSon") == 1 then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "ProQuestProgress", "RichSon")
                                            wait(0.5)
                                            itemequip("Relic")
                                            wait(0.5)
                                            two(CFrame.new(-1404.91504, 29.9773273, 3.80598116, 0.876514494, 5.66906877e-09,
                                                0.481375456, 2.53851997e-08, 1, -5.79995607e-08, -0.481375456,
                                                6.30572643e-08, 0.876514494))
                                        end
                                    end
                                end

                            end
                        else
                            CFrameBossSaber = CFrame.new(-1386.70251, 29.8520298, 14.2350292, 0.585077047, -3.65706043e-09, 0.810977697, 4.80931917e-09, 1, 1.03977948e-09, -0.810977697, 3.29189964e-09, 0.585077047)
                            if game:GetService("Workspace").Enemies:FindFirstChild("Saber Expert [Lv. 200] [Boss]") then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Saber Expert [Lv. 200] [Boss]"      then
                                        repeat
                                            wait()
                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                            end
                                            itemequip(_G.Settings["Select Weapon"])
                                            -- FastAttack = true
                                            if AttackRandomType == 1 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                            elseif AttackRandomType == 2 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                            elseif AttackRandomType == 3 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                            elseif AttackRandomType == 4 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                            elseif AttackRandomType == 5 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                            end
                                            v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(14)
                                            cilck()
                                        until v.Humanoid.Health <= 0 or _G.Saber == false
                                    end
                                end
                            else
                                if not game:GetService("Workspace").Enemies:FindFirstChild("Saber Expert [Lv. 200] [Boss]") then
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameBossSaber.Position).Magnitude <= 10 then
                                    if not game:GetService("Workspace").Enemies:FindFirstChild("Saber Expert [Lv. 200] [Boss]") then
                                    spawn(function()
                                        while wait() do
                                            if  _G.Settings["Auto Saber Hop"] then
                                                Hop()
                                        end
                                        end
                                    end)        
                                    end
                                elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameBossSaber.Position).Magnitude >= 3000 then
                                    tp(CFrameBossSaber)
                                else
                                    two(CFrameBossSaber)
                                    end   
                                end 
                            end


                            end
                        end
                    end
                end)
            end
        end
    end)

    spawn(function()
        while wait() do
            if _G.AutoNewWorld then
                pcall(function()
                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress",
                        "Detective") == 2 and OldWolrd then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")

                    end
                end)
            end
        end
    end)




    spawn(function()
        while wait() do
            if _G.AutoNewWorld then
                pcall(function()
                    if game:GetService("Players").LocalPlayer.Data.Level.Value >= 700 and OldWolrd then
                        _G.Noclip = true

                        if game.Workspace.Map.Ice.Door.CanCollide == true and game.Workspace.Map.Ice.Door.Transparency == 0 then
                            if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Key') then

                                CFneww = CFrame.new(1347.94153, 37.3493652, -1325.65613, 0.563168228, 8.23917858e-08,
                                    0.826342106, -9.30935187e-08, 1, -3.62615928e-08, -0.826342106, -5.65057086e-08,
                                    0.563168228)
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFneww.Position).Magnitude <=
                                    10 then
                                    two(CFneww)
                                    itemequip('Key')
                                elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFneww.Position).Magnitude >=
                                    2000 then
                                    tp(CFneww)
                                else
                                    two(CFneww)
                                end
                            else
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress",
                                    "Detective")
                            end
                        elseif game.Workspace.Map.Ice.Door.CanCollide == false and game.Workspace.Map.Ice.Door.Transparency ==
                            1 then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == 'Ice Admiral [Lv. 700] [Boss]' then
                                    repeat
                                        wait(.1)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                            game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                        end
                                        itemequip(_G.Settings["Select Weapon"])
                                        -- FastAttack = true
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                    
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                    until _G.AutoNewWorld == false or v.Humanoid.Health <= 0
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
                                end
                            end
                            _G.AutoNewWorld = false

                        end
                    elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress",
                        "Detective") == 2 then

                    
                        wait(5)
                    end
                end)
            end
        end
    end)
















    spawn(function()
        while  wait() do
            if _G.AutoPole1 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Thunder God [Lv. 575] [Boss]") then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Thunder God [Lv. 575] [Boss]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                    end
                                    itemequip(_G.Settings["Select Weapon"])
                                    -- FastAttack = true
                                    if AttackRandomType == 1 then
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                    elseif AttackRandomType == 2 then
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                    elseif AttackRandomType == 3 then
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                    elseif AttackRandomType == 4 then
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                    elseif AttackRandomType == 5 then
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                    end
                                    v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(14)
                                    v.Humanoid.Sit = true
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                until not _G.AutoPole1  or v.Humanoid.Health <= 0
                            end 
                        end
                    else
                        CFramePole = CFrame.new(-7710.05811, 5606.89307, -2281.75659, 0.588946104, 0, 0.808172286, 0, 1, 0, -0.808172286, 0, 0.588946104)
                        if not game:GetService("Workspace").Enemies:FindFirstChild("Thunder God [Lv. 575] [Boss]") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFramePole.Position).Magnitude <= 10 then
                                if not game:GetService("Workspace").Enemies:FindFirstChild("Thunder God [Lv. 575] [Boss]") then
                                spawn(function()
                                    while wait do
                                        if  _G.Settings["Auto Pole Hop"] then
                                            Hop()
                                    end
                                        end
                                end)               
                                end
                            elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFramePole.Position).Magnitude >= 3000 then
                                tp(CFramePole)
                            else
                                two(CFramePole)
                                end   
                            end 
                    end
                end)
            end
        end
    end)



    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function() 
            pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if _G.AutoPole1  and v.Name == "Thunder God [Lv. 575] [Boss]" and (v.HumanoidRootPart.Position - PosMon.Position).Magnitude <= 350 then
                            v.HumanoidRootPart.CFrame = PosMon
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
            end)
        end)
    end)




    -- spawn(function()
    --     while wait() do
    --         for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
    --             pcall(function()
    --                 if _G.AutoPole1 and StartMagnetPole and v.Name == 'Thunder God [Lv. 575] [Boss]' and
    --                     v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and
    --                     (v.HumanoidRootPart.Position -
    --                         game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 275 then
    --                     v.HumanoidRootPart.CFrame = CFrame.new(-7811.10938, 5606.90381, -2356.97412, 0.917771518,
    --                         -6.31973833e-08, -0.397108793, 6.74631337e-08, 1, -3.22743898e-09, 0.397108793, -2.38281519e-08,
    --                         0.917771518)
    --                     v.HumanoidRootPart.CanCollide = false
    --                     v.Head.CanCollide = false
    --                     if v.Humanoid:FindFirstChild("Animator") then
    --                         v.Humanoid.Animator:Destroy()
    --                     end
    --                     v.Humanoid:ChangeState(14)
    --                 end
    --             end)
    --         end
    --     end
    -- end)

    TeleportTable = {}

    if OldWolrd then
        TeleportTable = {"WindMill", "Marine", "Middle Town", "Jungle", "Pirate Village", "Desert", "Snow Island",
                        "MarineFord", "Colosseum", "Sky Island 1", "Sky Island 2", "Sky Island 3", "Prison",
                        "Magma Village", "Under Water Island", "Fountain City", "Shank Room", "Mob Island"}
    elseif SecondSea then
        TeleportTable = {"Cafe", "Dock", "Dark Area", "Flamingo Mansion", "Flamingo Room", "Green Zone", "Factory",
                        "Colossuim", "Zombie Island", "Two Snow Mountain", "Punk Hazard", "Cursed Ship", "Ice Castle",
                        "Forgotten Island", "Ussop Island", "Mini Sky Island"}
    elseif ThirdSea then
        TeleportTable  = {"Port Town","Hydra Island","Gaint Tree","Mansion","Castle on the Sea","Graveyard Island","Icecream Island","Peanut Island","Lab","Cake Loaf"}
    end


    if _G.SelectTeleport == nil then
        if OldWolrd then
            _G.SelectTeleport = "WindMill"
        elseif SecondSea then
            _G.SelectTeleport = "Cafe"
        elseif ThirdSea then
            _G.SelectTeleport = "Mansion"
        end
    end




    if _G.SelectTeleport == false then
        if OldWolrd then
            _G.SelectTeleport = "WindMill"
        elseif SecondSea then
            _G.SelectTeleport = "Cafe"
        elseif ThirdSea then
            _G.SelectTeleport = "Mansion"
        end
    end



    BossName = {}
    for i, v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
        if string.find(v.Name, "Boss") then
            if OldWolrd then
                if v.Name == "Ice Admiral [Lv. 700] [Boss]"   then

                
                else
                    table.insert(BossName, v.Name)
                end
            elseif SecondSea then
                if v.Name == "rip_indra [Lv. 1500] [Boss]"   then

                
                else
                    table.insert(BossName, v.Name)
                end
            elseif ThirdSea then
                table.insert(BossName, v.Name)
            end    
        end
    end

    function CheckBossQuest()
        if _G.Settings["AutoFramBooss"] == "Saber Expert [Lv. 200] [Boss]" then
            MsBoss = "Saber Expert [Lv. 200] [Boss]"
            NameBoss = "Saber Expert"
            CFrameBoss = CFrame.new(-1458.89502, 29.8870335, -50.633564, 0.858821094, 1.13848939e-08, 0.512275636,
                -4.85649254e-09, 1, -1.40823326e-08, -0.512275636, 9.6063415e-09, 0.858821094)
        elseif _G.Settings["AutoFramBooss"] == "The Saw [Lv. 100] [Boss]" then
            MsBoss = "The Saw [Lv. 100] [Boss]"
            NameBoss = "The Saw"
            CFrameBoss = CFrame.new(-683.519897, 13.8534927, 1610.87854, -0.290192783, 6.88365773e-08, 0.956968188,
                6.98413629e-08, 1, -5.07531119e-08, -0.956968188, 5.21077759e-08, -0.290192783)
        elseif _G.Settings["AutoFramBooss"] == "Greybeard [Lv. 750] [Raid Boss]" then
            MsBoss = "Greybeard [Lv. 750] [Raid Boss]"
            NameBoss = "Greybeard"
            CFrameBoss = CFrame.new(-4955.72949, 80.8163834, 4305.82666, -0.433646321, -1.03394289e-08, 0.901083171,
                -3.0443168e-08, 1, -3.17633075e-09, -0.901083171, -2.88092288e-08, -0.433646321)
        elseif _G.Settings["AutoFramBooss"] == "The Gorilla King [Lv. 25] [Boss]" then
            MsBoss = "The Gorilla King [Lv. 25] [Boss]"
            NameBoss = "The Gorilla King"
            NameQuestBoss = "JungleQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559,
                1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
            CFrameBoss = CFrame.new(-1223.52808, 6.27936459, -502.292664, 0.310949147, -5.66602516e-08, 0.950426519,
                -3.37275488e-08, 1, 7.06501808e-08, -0.950426519, -5.40241736e-08, 0.310949147)
        elseif _G.Settings["AutoFramBooss"] == "Bobby [Lv. 55] [Boss]" then
            MsBoss = "Bobby [Lv. 55] [Boss]"
            NameBoss = "Bobby"
            NameQuestBoss = "BuggyQuest1"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383,
                -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
            CFrameBoss = CFrame.new(-1147.65173, 32.5966301, 4156.02588, 0.956680477, -1.77109952e-10, -0.29113996,
                5.16530874e-10, 1, 1.08897802e-09, 0.29113996, -1.19218679e-09, 0.956680477)
        elseif _G.Settings["AutoFramBooss"] == "Yeti [Lv. 110] [Boss]" then
            MsBoss = "Yeti [Lv. 110] [Boss]"
            NameBoss = "Yeti"
            NameQuestBoss = "SnowQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(1384.90247, 87.3078308, -1296.6825, 0.280209213, 2.72035177e-08, -0.959938943,
                -6.75690828e-08, 1, 8.6151708e-09, 0.959938943, 6.24481444e-08, 0.280209213)
            CFrameBoss = CFrame.new(1221.7356, 138.046906, -1488.84082, 0.349343032, -9.49245944e-08, 0.936994851,
                6.29478194e-08, 1, 7.7838429e-08, -0.936994851, 3.17894653e-08, 0.349343032)
        elseif _G.Settings["AutoFramBooss"] == "Mob Leader [Lv. 120] [Boss]" then
            MsBoss = "Mob Leader [Lv. 120] [Boss]"
            NameBoss = "Mob Leader"
            CFrameBoss = CFrame.new(-2848.59399, 7.4272871, 5342.44043, -0.928248107, -8.7248246e-08, 0.371961564,
                -7.61816636e-08, 1, 4.44474857e-08, -0.371961564, 1.29216433e-08, -0.92824)
        elseif _G.Settings["AutoFramBooss"] == "Vice Admiral [Lv. 130] [Boss]" then
            MsBoss = "Vice Admiral [Lv. 130] [Boss]"
            NameBoss = "Vice Admiral"
            NameQuestBoss = "MarineQuest2"
            LevelQuestBoss = 2
            CFrameQuestBoss = CFrame.new(-5035.42285, 28.6520386, 4324.50293, -0.0611100644, -8.08395768e-08, 0.998130739,
                -1.57416586e-08, 1, 8.00271849e-08, -0.998130739, -1.08217701e-08, -0.0611100644)
            CFrameBoss = CFrame.new(-5078.45898, 99.6520691, 4402.1665, -0.555574954, -9.88630566e-11, 0.831466436,
                -6.35508286e-08, 1, -4.23449258e-08, -0.831466436, -7.63661632e-08, -0.555574954)
        elseif _G.Settings["AutoFramBooss"] == "Warden [Lv. 175] [Boss]" then
            MsBoss = "Warden [Lv. 175] [Boss]"
            NameBoss = "Warden"
            NameQuestBoss = "ImpelQuest"
            LevelQuestBoss = 1
            CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691,
                1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
            CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697,
                3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
        elseif _G.Settings["AutoFramBooss"] == "Chief Warden [Lv. 200] [Boss]" then
            MsBoss = "Chief Warden [Lv. 200] [Boss]"
            NameBoss = "Chief Warden"
            NameQuestBoss = "ImpelQuest"
            LevelQuestBoss = 2
            CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691,
                1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
            CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697,
                3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
        elseif _G.Settings["AutoFramBooss"] == "Swan [Lv. 225] [Boss]" then
            MsBoss = "Swan [Lv. 225] [Boss]"
            NameBoss = "Swan"
            NameQuestBoss = "ImpelQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691,
                1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
            CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697,
                3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
        elseif _G.Settings["AutoFramBooss"] == "Magma Admiral [Lv. 350] [Boss]" then
            MsBoss = "Magma Admiral [Lv. 350] [Boss]"
            NameBoss = "Magma Admiral"
            NameQuestBoss = "MagmaQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-5317.07666, 12.2721891, 8517.41699, 0.51175487, -2.65508806e-08, -0.859131515,
                -3.91131572e-08, 1, -5.42026761e-08, 0.859131515, 6.13418294e-08, 0.51175487)
            CFrameBoss = CFrame.new(-5530.12646, 22.8769703, 8859.91309, 0.857838571, 2.23414389e-08, 0.513919294,
                1.53689133e-08, 1, -6.91265853e-08, -0.513919294, 6.71978384e-08, 0.857838571)
        elseif _G.Settings["AutoFramBooss"] == "Fishman Lord [Lv. 425] [Boss]" then
            MsBoss = "Fishman Lord [Lv. 425] [Boss]"
            NameBoss = "Fishman Lord"
            NameQuestBoss = "FishmanQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(61123.0859, 18.5066795, 1570.18018, 0.927145958, 1.0624845e-07, 0.374700129,
                -6.98219367e-08, 1, -1.10790765e-07, -0.374700129, 7.65569368e-08, 0.927145958)
            CFrameBoss = CFrame.new(61351.7773, 31.0306778, 1113.31409, 0.999974668, 0, -0.00714713801, 0, 1.00000012, 0,
                0.00714714266, 0, 0.999974549)
        elseif _G.Settings["AutoFramBooss"] == "Wysper [Lv. 500] [Boss]" then
            MsBoss = "Wysper [Lv. 500] [Boss]"
            NameBoss = "Wysper"
            NameQuestBoss = "SkyExp1Quest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-7862.94629, 5545.52832, -379.833954, 0.462944925, 1.45838088e-08, -0.886386991,
                1.0534996e-08, 1, 2.19553424e-08, 0.886386991, -1.95022007e-08, 0.462944925)
            CFrameBoss = CFrame.new(-7925.48389, 5550.76074, -636.178345, 0.716468513, -1.22915289e-09, 0.697619379,
                3.37381434e-09, 1, -1.70304748e-09, -0.697619379, 3.57381835e-09, 0.716468513)
        elseif _G.Settings["AutoFramBooss"] == "Thunder God [Lv. 575] [Boss]" then
            MsBoss = "Thunder God [Lv. 575] [Boss]"
            NameBoss = "Thunder God"
            NameQuestBoss = "SkyExp2Quest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-7902.78613, 5635.99902, -1411.98706, -0.0361216255, -1.16895912e-07, 0.999347389,
                1.44533963e-09, 1, 1.17024491e-07, -0.999347389, 5.6715117e-09, -0.0361216255)
            CFrameBoss = CFrame.new(-7917.53613, 5616.61377, -2277.78564, 0.965189934, 4.80563429e-08, -0.261550069,
                -6.73089886e-08, 1, -6.46515304e-08, 0.261550069, 8.00056768e-08, 0.965189934)
            if _G.Settings["AutoFramBooss"] and
                (CFrameBoss.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance", Vector3.new(
                    -7894.6176757813, 5547.1416015625, -380.29119873047))
            end
        elseif _G.Settings["AutoFramBooss"] == "Cyborg [Lv. 675] [Boss]" then
            MsBoss = "Cyborg [Lv. 675] [Boss]"
            NameBoss = "Cyborg"
            NameQuestBoss = "FountainQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(5253.54834, 38.5361786, 4050.45166, -0.0112687312, -9.93677887e-08, -0.999936521,
                2.55291371e-10, 1, -9.93769547e-08, 0.999936521, -1.37512213e-09, -0.0112687312)
            CFrameBoss = CFrame.new(6041.82813, 52.7112198, 3907.45142, -0.563162148, 1.73805248e-09, -0.826346457,
                -5.94632716e-08, 1, 4.26280238e-08, 0.826346457, 7.31437524e-08, -0.563162148)
            -- New World
        elseif _G.Settings["AutoFramBooss"] == "Diamond [Lv. 750] [Boss]" then
            MsBoss = "Diamond [Lv. 750] [Boss]"
            NameBoss = "Diamond"
            NameQuestBoss = "Area1Quest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601,
                -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
            CFrameBoss = CFrame.new(-1736.26587, 198.627731, -236.412857, -0.997808516, 0, -0.0661673471, 0, 1, 0,
                0.0661673471, 0, -0.997808516)
        elseif _G.Settings["AutoFramBooss"] == "Jeremy [Lv. 850] [Boss]" then
            MsBoss = "Jeremy [Lv. 850] [Boss]"
            NameBoss = "Jeremy"
            NameQuestBoss = "Area2Quest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771,
                1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
            CFrameBoss = CFrame.new(2203.76953, 448.966034, 752.731079, -0.0217453763, 0, -0.999763548, 0, 1, 0,
                0.999763548, 0, -0.0217453763)
        elseif _G.Settings["AutoFramBooss"] == "Fajita [Lv. 925] [Boss]" then
            MsBoss = "Fajita [Lv. 925] [Boss]"
            NameBoss = "Fajita"
            NameQuestBoss = "MarineQuest3"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301,
                5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
            CFrameBoss = CFrame.new(-2297.40332, 115.449463, -3946.53833, 0.961227536, -1.46645796e-09, -0.275756449,
                -2.3212845e-09, 1, -1.34094433e-08, 0.275756449, 1.35296352e-08, 0.961227536)
        elseif _G.Settings["AutoFramBooss"] == "Don Swan [Lv. 1000] [Boss]" then
            MsBoss = "Don Swan [Lv. 1000] [Boss]"
            NameBoss = "Don Swan"
            CFrameBoss = CFrame.new(2288.802, 15.1870775, 863.034607, 0.99974072, -8.41247214e-08, -0.0227668174,
                8.4774733e-08, 1, 2.75850098e-08, 0.0227668174, -2.95079072e-08, 0.99974072)
        elseif _G.Settings["AutoFramBooss"] == "Smoke Admiral [Lv. 1150] [Boss]" then
            MsBoss = "Smoke Admiral [Lv. 1150] [Boss]"
            NameBoss = "Smoke Admiral"
            NameQuestBoss = "IceSideQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-6059.96191, 15.9868021, -4904.7373, -0.444992423, -3.0874483e-09, 0.895534337,
                -3.64098796e-08, 1, -1.4644522e-08, -0.895534337, -3.91229982e-08, -0.444992423)
            CFrameBoss = CFrame.new(-5115.72754, 23.7664986, -5338.2207, 0.251453817, 1.48345061e-08, -0.967869282,
                4.02796978e-08, 1, 2.57916977e-08, 0.967869282, -4.54708946e-08, 0.251453817)
        elseif _G.Settings["AutoFramBooss"] == "Cursed Captain [Lv. 1325] [Raid Boss]" then
            MsBoss = "Cursed Captain [Lv. 1325] [Raid Boss]"
            NameBoss = "Cursed Captain"
            CFrameBoss = CFrame.new(916.928589, 181.092773, 33422, -0.999505103, 9.26310495e-09, 0.0314563364,
                8.42916226e-09, 1, -2.6643713e-08, -0.0314563364, -2.63653774e-08, -0.999505103)
        elseif _G.Settings["AutoFramBooss"] == "Darkbeard [Lv. 1000] [Raid Boss]" then
            MsBoss = "Darkbeard [Lv. 1000] [Raid Boss]"
            NameBoss = "Darkbeard"
            CFrameBoss = CFrame.new(3876.00366, 24.6882591, -3820.21777, -0.976951957, 4.97356325e-08, 0.213458836,
                4.57335361e-08, 1, -2.36868622e-08, -0.213458836, -1.33787044e-08, -0.976951957)
        elseif _G.Settings["AutoFramBooss"] == "Order [Lv. 1250] [Raid Boss]" then
            MsBoss = "Order [Lv. 1250] [Raid Boss]"
            NameBoss = "Order"
            CFrameBoss = CFrame.new(-6221.15039, 16.2351036, -5045.23584, -0.380726993, 7.41463495e-08, 0.924687505,
                5.85604774e-08, 1, -5.60738549e-08, -0.924687505, 3.28013137e-08, -0.380726993)
        elseif _G.Settings["AutoFramBooss"] == "Awakened Ice Admiral [Lv. 1400] [Boss]" then
            MsBoss = "Awakened Ice Admiral [Lv. 1400] [Boss]"
            NameBoss = "Awakened Ice Admiral"
            NameQuestBoss = "FrostQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(5669.33203, 28.2118053, -6481.55908, 0.921275556, -1.25320829e-08, 0.388910472,
                4.72230788e-08, 1, -7.96414241e-08, -0.388910472, 9.17372489e-08, 0.921275556)
            CFrameBoss = CFrame.new(6407.33936, 340.223785, -6892.521, 0.49051559, -5.25310213e-08, -0.871432424,
                -2.76146022e-08, 1, -7.58250565e-08, 0.871432424, 6.12576301e-08, 0.49051559)
        elseif _G.Settings["AutoFramBooss"] == "Tide Keeper [Lv. 1475] [Boss]" then
            MsBoss = "Tide Keeper [Lv. 1475] [Boss]"
            NameBoss = "Tide Keeper"
            NameQuestBoss = "ForgottenQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-3053.89648, 236.881363, -10148.2324, -0.985987961, -3.58504737e-09, 0.16681771,
                -3.07832915e-09, 1, 3.29612559e-09, -0.16681771, 2.73641976e-09, -0.985987961)
            CFrameBoss = CFrame.new(-3570.18652, 123.328949, -11555.9072, 0.465199202, -1.3857326e-08, 0.885206044,
                4.0332897e-09, 1, 1.35347511e-08, -0.885206044, -2.72606271e-09, 0.465199202)
            -- Thire World
        elseif _G.Settings["AutoFramBooss"] == "Stone [Lv. 1550] [Boss]" then
            MsBoss = "Stone [Lv. 1550] [Boss]"
            NameBoss = "Stone"
            NameQuestBoss = "PiratePortQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-290, 44, 5577)
            CFrameBoss = CFrame.new(-1085, 40, 6779)
        elseif _G.Settings["AutoFramBooss"] == "Island Empress [Lv. 1675] [Boss]" then
            MsBoss = "Island Empress [Lv. 1675] [Boss]"
            NameBoss = "Island Empress"
            NameQuestBoss = "AmazonQuest2"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(5443, 602, 752)
            CFrameBoss = CFrame.new(5659, 602, 244)
        elseif _G.Settings["AutoFramBooss"] == "Kilo Admiral [Lv. 1750] [Boss]" then
            MsBoss = "Kilo Admiral [Lv. 1750] [Boss]"
            NameBoss = "Kilo Admiral"
            NameQuestBoss = "MarineTreeIsland"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(2178, 29, -6737)
            CFrameBoss = CFrame.new(2846, 433, -7100)
        elseif _G.Settings["AutoFramBooss"] == "Captain Elephant [Lv. 1875] [Boss]" then
            MsBoss = "Captain Elephant [Lv. 1875] [Boss]"
            NameBoss = "Captain Elephant"
            NameQuestBoss = "DeepForestIsland"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-13232, 333, -7631)
            CFrameBoss = CFrame.new(-13221, 325, -8405)
        elseif _G.Settings["AutoFramBooss"] == "Beautiful Pirate [Lv. 1950] [Boss]" then
            MsBoss = "Beautiful Pirate [Lv. 1950] [Boss]"
            NameBoss = "Beautiful Pirate"
            NameQuestBoss = "DeepForestIsland2"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-12686, 391, -9902)
            CFrameBoss = CFrame.new(5182, 23, -20)
        elseif _G.Settings["AutoFramBooss"] == "Cake Queen [Lv. 2175] [Boss]" then
            MsBoss = "Cake Queen [Lv. 2175] [Boss]"
            NameBoss = "Cake Queen"
            NameQuestBoss = "IceCreamIslandQuest"
            LevelQuestBoss = 3
            CFrameQuestBoss = CFrame.new(-716, 382, -11010)
            CFrameBoss = CFrame.new(-821, 66, -10965)
        elseif _G.Settings["AutoFramBooss"] == "rip_indra True Form [Lv. 5000] [Raid Boss]" then
            MsBoss = "rip_indra True Form [Lv. 5000] [Raid Boss]"
            NameBoss = "rip_indra True Form"
            CFrameBoss = CFrame.new(-5359, 424, -2735)
        elseif _G.Settings["AutoFramBooss"] == "Longma [Lv. 2000] [Boss]" then
            MsBoss = "Longma [Lv. 2000] [Boss]"
            NameBoss = "Longma"
            CFrameBoss = CFrame.new(-10248.3936, 353.79129, -9306.34473)
        elseif _G.Settings["AutoFramBooss"] == "Soul Reaper [Lv. 2100] [Raid Boss]" then
            MsBoss = "Soul Reaper [Lv. 2100] [Raid Boss]"
            NameBoss = "Soul Reaper"
            CFrameBoss = CFrame.new(-9515.62109, 315.925537, 6691.12012)
        end
    end


    if _G.Settings["AutoFramBooss"] == nil then
        _G.Settings["AutoFramBooss"] = " "
    end

    if _G.Settings["AutoFramBooss"] == false then
        _G.Settings["AutoFramBooss"] = " "
    end

    Boss:AddDropdown({
        Name = "Auto Farm Boss",
        List = BossName,
        Value = _G.Settings["AutoFramBooss"],
        Callback = function(value)
            _G.Settings["AutoFramBooss"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })

    Boss:AddButton({
        Name = "Refresh Boss",
        Callback = function()
            table.clear(BossName)

            for i, v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
                    if string.find(v.Name, "Boss") then
                        if OldWolrd then
                            if v.Name == "Ice Admiral [Lv. 700] [Boss]"   then
                
                            
                            else
                                table.insert(BossName, v.Name)
                            end
                        elseif SecondSea then
                            if v.Name == "rip_indra [Lv. 1500] [Boss]"   then
                
                            
                            else
                                table.insert(BossName, v.Name)
                            end
                        elseif ThirdSea then
                            table.insert(BossName, v.Name)
                        end    
                end
            end
        end
    })

    Boss:AddToggle{
        Name = "Auto Fram Boss",
        Flag = "Auto Fram Boss.",
        Value = _G.Settings["Auto Fram Boss"],
        Callback = function(value)
            _G.Settings["Auto Fram Boss"] = value
    
            if value == false then
                tween:Cancel()
            end
        end
    }

    function StopTween(target)
        if not target then
            _G.StopTween = true
            wait()
            two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            wait()
            if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
            _G.StopTween = false
        end
    end





    function StopTween(target)
        if not target then
            _G.StopTween = true
            wait()
            two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            wait()
            if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
            _G.StopTween = false
        end
    end



    Boss:AddToggle{
        Name = "Auto Fram All Boss",
        Flag = "Auto_Fram_Boss",
        Value = _G.Settings["Auto_Fram_All_Boss"],
        Callback = function(value)
            _G.Settings["Auto_Fram_All_Boss"] = value
            _G.FramBoos = value
            -- StopTween(_G.Settings["Auto_Fram_All_Boss"])
            if value == false then
                pcall(function()
                tween:Cancel()  
                game.Players.LocalPlayer.Character.Humanoid.Health = 0                         
                end)
            end
        end
    }














    spawn(function()
        while  wait() do
            if _G.Settings["Auto Fram Boss"] then
                pcall(function()
                    NoclipBoos = true
                    CheckBossQuest()
                    if game:GetService("Workspace").Enemies:FindFirstChild(MsBoss) then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == MsBoss then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                            game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                        end
                                        itemequip(_G.Settings["Select Weapon"])
                                        if AttackRandomType == 1 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                        elseif AttackRandomType == 2 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                        elseif AttackRandomType == 3 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                        elseif AttackRandomType == 4 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                        elseif AttackRandomType == 5 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                        end
                                        v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        v.Humanoid.Sit = true
                                        cilck()
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)                      
                                    until not _G.AutodPole1  or v.Humanoid.Health <= 0
                                end
                            end                 
                    else
                        CheckBossQuest()
                        if not game:GetService("Workspace").Enemies:FindFirstChild(MsBoss) then 
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameBoss.Position).Magnitude <= 3500 then
                                two(CFrameBoss)     
                            else
                                two(CFrameBoss)          
                            end
                        end
                    end
                end)
            else
                NoclipBoos = false
            end
        end
    end)

    spawn(function()
        while wait() do
            if _G.AutoSea_Beast then

                if game:GetService("Workspace").SeaBeasts:FindFirstChild('HumanoidRootPart') then
                    for i, v in pairs(game:GetService("Workspace").SeaBeasts:GetChildren()) do
                        if v:FindFirstChild('HumanoidRootPart') then
                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 500, 20))
                        end
                    end

                else
                    print('Not Find SeaBeast')
                end
            end
        end
    end)

    function Hop()
        local PlaceID = game.PlaceId
        local AllIDs = {}
        local foundAnything = ""
        local actualHour = os.date("!*t").hour
        local Deleted = false
        function TPReturner()
            local Site;
            if foundAnything == "" then
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
            else
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
            end
            local ID = ""
            if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                foundAnything = Site.nextPageCursor
            end
            local num = 0;
            for i,v in pairs(Site.data) do
                local Possible = true
                ID = tostring(v.id)
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        wait()
                        pcall(function()
                            wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
        function Teleport() 
            while wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
        Teleport()
    end



    -- function two(P1)
    --     if not _G.Stop_Tween then
    --         Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    --             if Distance < 200 then
    --                 Speed = 700
    --             elseif Distance < 1000 then
    --                 Speed = 320
    --             elseif Distance >= 1000 then
    --                 Speed = 320
    --             end
    --         Tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,
    --             TweenInfo.new(Distance / Speed, Enum.EasingStyle.Linear), {
    --                 CFrame = P1
    --             })
    --         if _G.Stop_Tween then
    --             tween:Cancel()
    --         elseif game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
    --             Tween:Play()
    --         end
    --     end
    -- end

    function canq()

        local args = {
            [1] = "AbandonQuest"
        }

        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

    end

















    task.spawn(function()
        while wait() do 
            AttackRandomType = math.random(1,5)
            wait(0.5)
        end
    end)

    local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)
    spawn(function()
        while task.wait() do
        if _G.Kill_Player then
            pcall(function()
    quest_title = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
    if string.find(quest_title, "Defeat") and string.find(quest_title, "(0/1)") then
        local Player = string.split(quest_title, " ")[2]
        local PlayerLevel = tonumber(game.Players[Player].Data.Level.Value)
        if game:GetService("Workspace").Characters:FindFirstChild(Player) then
            if PlayerLevel >= 20 and PlayerLevel <= (game.Players.LocalPlayer.Data.Level.Value + 400) then
                for i,v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
                    if v.Name == tostring(Player) and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v.Parent then
                        if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude <= 2100 or (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2100 then
                            starttime = os.time()
                            repeat task.wait(.1)
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude <= 45 or (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 45 then
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                    end
                                    
                                    if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.PvpDisabled.Visible == false then
                                        v.HumanoidRootPart.Size = Vector3.new(80,80,80)
                                        v.HumanoidRootPart.Transparency = 1
                                        FastAttackk = true
                                        if AttackRandomType == 1 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                        elseif AttackRandomType == 2 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 20))
                                        elseif AttackRandomType == 3 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -20))
                                        elseif AttackRandomType == 4 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(20, 1, 0))
                                        elseif AttackRandomType == 5 then
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(-20, 1, 0))
                                        end 
                                        if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                        end
                                        game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                        game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        wait()
                                        game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                        game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                        wait(.1)
                                        game:GetService 'VirtualUser':CaptureController()
                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    else
                                        repeat wait() game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EnablePvp") until game:GetService("Players")["LocalPlayer"].PlayerGui.Main.PvpDisabled.Visible == false
                                    end
                                else
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(30, 5, 0))
                                end
                                if starttime - os.time() > 40 then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                end
                            until not _G.Kill_Player or v.Humanoid.Health <= 0 or not v.Parent or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false or not _G.Settings["Auto Farm Fast Level"]
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                            FastAttackk = false
                        else
                            tp(v.HumanoidRootPart.CFrame)
                        end
                    end
                end
            else
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
            end
        else
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
        end
    else
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
        end
                end)    
            end
        end
    end)

    -- spawn(function()
    --     while wait() do
    --         if _G.Kill_Player   then
    --             pcall(function()
    --             for i,v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
    --            Plytitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text     
    --            if string.find(Plytitle,"(0/1)") and string.find(Plytitle,"Defeat")  then
    --                 if string.find(Plytitle,v.Name) then
    --                     PlayerLevel = tonumber(game.Players[v.Name].Data.Level.Value)
    --                     if game:GetService("Workspace").Characters:FindFirstChild(v.Name) then
    --                         if PlayerLevel >= 20 and PlayerLevel <= (game.Players.LocalPlayer.Data.Level.Value + 400) then
    --                             if v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v.Parent then
    --                                 if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude <= 3000 or (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
    --                                     starttime = os.time()
    --                                     repeat task.wait(.1)
    --                                         if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude <= 50 then
    --                                             v.HumanoidRootPart.Size = Vector3.new(80,80,80)
    --                                             v.HumanoidRootPart.Transparency = 0
    --                                             if AttackRandomType == 1 then
    --                                                 two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
    --                                             elseif AttackRandomType == 2 then
    --                                                 two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 20))
    --                                             elseif AttackRandomType == 3 then
    --                                                 two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -20))
    --                                             elseif AttackRandomType == 4 then
    --                                                 two(v.HumanoidRootPart.CFrame * CFrame.new(20, 1, 0))
    --                                             elseif AttackRandomType == 5 then
    --                                                 two(v.HumanoidRootPart.CFrame * CFrame.new(-20, 1, 0))
    --                                             end
    --                                             FastAttackk = true
    --                                             if game:GetService("Players").LocalPlayer.PlayerGui.Main.SafeZone.Visible == true then
    --                                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
    --                                             end
    --                                             if game:GetService("Players").LocalPlayer.PlayerGui.Main.PvpDisabled.Visible == true then
    --                                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EnablePvp")
    --                                             end  
    --                                             if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
    --                                                 game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
    --                                             end
    --                                             if game:GetService("Players")[v.Name].Data.Level.Value <= 20 then
    --                                                 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
    --                                             end 
    --                                             itemequip(_G.Settings["Select Weapon"])
    --                                             game:GetService("VirtualInputManager"):SendKeyEvent(true, "Z", false, game)
    --                                             game:GetService("VirtualInputManager"):SendKeyEvent(false, "Z", false, game)
    --                                                     task.wait()
    --                                             game:GetService("VirtualInputManager"):SendKeyEvent(true, "X", false, game)
    --                                             game:GetService("VirtualInputManager"):SendKeyEvent(false, "X", false, game)
    --                                             game:GetService 'VirtualUser':CaptureController()
    --                                             game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
    --                                             sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
    --                                         else
    --                                             two(v.HumanoidRootPart.CFrame * CFrame.new(30, 5, 0))
    --                                         end
    --                                         if starttime - os.time() > 60 then
    --                                             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
    --                                         end
    --                                     until  not v.Parent or not _G.Kill_Player or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
    --                                     FastAttackk = false
    --                                 else
    --                                     tp(v.HumanoidRootPart.CFrame)
    --                                 end
    --                             end
    --                         else
    --                             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
    --                         end
    --                              end
    --                         end
    --                     elseif not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"(0/1)") and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Defeat")  then
    --                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
    --                     end
    --                 end
    --             end)
    --         end
    --     end
    -- end)











        spawn(function()
            while true do wait()
                pcall(function()
                    if game.Players.LocalPlayer.Character.Humanoid.Health <= 0 then
                        tween:Cancel() 
                    end
                end)
            end
        end)












    if _G.Settings["MinHealth"] == nil then
        _G.Settings["MinHealth"] = 25
    end





    SMastery:AddSlider({
        Name = "Health For Mastery Farm",
        Flag = "Health_For_Mastery_Farm",
        Value = _G.Settings["MinHealth"],
        Min = 1,
        Max = 100,
        Textbox = true,
        Format = function(value)
            MinHealth = value
            _G.Settings["MinHealth"] = value
            SaveSettings()
            return "Health : ".. tostring(value).." [For Mastery Farm]"
        end
    })







    Mastery:AddToggle({
        Name = "Auto Farm Mastery Fruits",
        Value = _G.Settings["Auto Farm Mastery Fruits"],
        Flag = "Auto Farm Mastery Fruits",
        Callback = function(value)
            _G.Settings["Auto Farm Mastery Fruits"]  = value
            _G.Auto_Mastery_Frutis = value
            SaveSettings()
            if value == false then
                tween:Cancel()
            end
        end
    })

    Mastery:AddToggle({
        Name = "Auto Farm Mastery Gun",
        Value = _G.Settings["Auto Farm Mastery Gun"],
        Flag = "Auto Farm Mastery Gun",
        Callback = function(value)
            _G.Settings["Auto Farm Mastery Gun"]  = value
            _G.Auto_Mastery_Gun = value
            SaveSettings()
            if value == false then
                tween:Cancel()
            end
        end
    })

    if _G.Settings["Skill X"] == true then
        Auto_SkilX = true
    end
    if _G.Settings["Skill Z"] == true then
        Auto_SkilZ = true
    end

    if _G.Settings["Skill C"] == true then
        Auto_SkilC = true
    end

    if _G.Settings["Skill V"] == true  then
        Auto_SkilV = true
    end

    SMastery:AddToggle({
        Name = "Skill Z",
        Value = _G.Settings["Skill Z"],
        Flag = "Skill Z",
        Callback = function(value)
            _G.Settings["Skill Z"]  = value
            Auto_SkilZ = value
            SaveSettings()
            if value == false then
            end
        end
    })





    SMastery:AddToggle({
        Name = "Skill X",
        Value = _G.Settings["Skill X"],
        Flag = "Skill X",
        Callback = function(value)
            _G.Settings["Skill X"]  = value
            Auto_SkilX = value
            SaveSettings()
            if value == false then
            end
        end
    })


    SMastery:AddToggle({
        Name = "Skill C",
        Value = _G.Settings["Skill C"],
        Flag = "Skill C",
        Callback = function(value)
            _G.Settings["Skill C"]  = value
            Auto_SkilC = value
            SaveSettings()
            if value == false then
            end
        end
    })

    SMastery:AddToggle({
        Name = "Skill V",
        Value = _G.Settings["Skill V"],
        Flag = "Skill V",
        Callback = function(value)
            _G.Settings["Skill V"]  = value
            Auto_SkilV = value
            SaveSettings()
            if value == false then
            end
        end
    })






    spawn(function()
        while true  do wait()
            for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"]:GetChildren()) do
                pcall(function()
                    if v.Name == ("CurvedRing") or v.Name == ("SlashHit") or v.Name == ("SwordSlash") or v.Name == ("SlashTail") or v.Name == ("Sounds") then
                        v:Destroy()
                    end
                end)
            end
        end
    end)

    NoDieEffect = true 
    if NoDieEffect then
        if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") then
            game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
        end
        if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn") then
            game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
        end
    end



    spawn(function()
        local gg = getrawmetatable(game)
        local old = gg.__namecall
        setreadonly(gg,false)
        gg.__namecall = newcclosure(function(...)
            local method = getnamecallmethod()
            local args = {...}
            if tostring(method) == "FireServer" then
                if tostring(args[1]) == "RemoteEvent" then
                    if tostring(args[2]) ~= "true" and tostring(args[2]) ~= "false" then
                        if UseSkillMasteryDevilFruit and _G.Auto_Mastery_Frutis then
                            if type(args[2]) == "vector" then 
                                args[2] = PositionSkillMasteryDevilFruit
                            else
                                args[2] = CFrame.new(PositionSkillMasteryDevilFruit)
                            end
                            return old(unpack(args))
                        end
                    end
                end
            end
            return old(...)
        end)
    end)


    local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)
    spawn(function()
        while wait() do
            if _G.Auto_Mastery_Frutis    then
                pcall(function()         
                    CheckQuest()
                        if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                            StartMagnet = false
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                        end
                        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                            StartMagnet = false
                            CheckQuest()                
                            repeat wait()                         
                                if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1700 then
                                    two(CFrameQ) 
                                elseif  (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1700 then
                                    tp(CFrameQ) 
                                end
                            until (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings["Auto Farm Level"]


                            if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                if game.Players.LocalPlayer.Character.Humanoid.Health > 0 and (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                    wait(0.4)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
                                end
                            
                        end
                                            
                        
                        elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            CheckQuest()
                            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        if v.Name == Ms then
                                            repeat wait(_G.Fast_Delay)
                                                HealthMin = v.Humanoid.MaxHealth * MinHealth/100
                                                if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                                                if v.Humanoid.Health <= HealthMin then
                                                    UseSkillMasteryDevilFruit = true
                                                    _G.Settings["Super Fast Attack"] = false
                                                    PositionSkillMasteryDevilFruit = v.HumanoidRootPart.Position
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                                    itemequip(tostring(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value))
                                                    game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value).MousePos.Value = v.HumanoidRootPart.Position
                                                    if Auto_SkilZ  and v.Humanoid.Health > 0 then
                                                        local args = {
                                                            [1] = v.HumanoidRootPart.Position
                                                        }
                                                        game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
                                                        game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                                        wait(.1)
                                                        game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                                    end
                                                    if Auto_SkilX  and v.Humanoid.Health > 0 then
                                                        local args = {
                                                            [1] = v.HumanoidRootPart.Position
                                                        }
                                                        game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
                                                        game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                                        wait(.1)
                                                        game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                                    end
                                                    if Auto_SkilC  and v.Humanoid.Health > 0 then
                                                        local args = {
                                                            [1] = v.HumanoidRootPart.Position
                                                        }
                                                        game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
                                                        game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
                                                        wait(.1)
                                                        game:service('VirtualInputManager'):SendKeyEvent(false, "C", false, game)
                                                    end
                                                    if Auto_SkilV  and v.Humanoid.Health > 0 then
                                                        local args = {
                                                            [1] = v.HumanoidRootPart.Position
                                                        }
                                                        game:GetService("Players").LocalPlayer.Character[game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
                                                        game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                                        wait(.1)
                                                        game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                                    end
                                                
                                                else
                                                    _G.Settings["Super Fast Attack"] = false
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"]) 
                                                    StartMagnet = true                                  
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.HumanoidRootPart.CanCaillde = false  
                                                    game:GetService('VirtualUser'):CaptureController()
                                                    game:GetService('VirtualUser'):ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
                                                end                                      
                                                else
                                                    StartMagnet = false
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                                end
                                            until not _G.Auto_Mastery_Frutis   or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            
                                        end
                                    end
                                end
                            else
                                StartMagnet = false
                                if game:GetService("ReplicatedStorage"):FindFirstChild(Ms) then
                                    two(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame)
                                else	
                                    if AttackRandomType == 1 then
                                        two(CFramePuk * CFrame.new(0, 20, 100))
                                    elseif AttackRandomType == 2 then
                                        two(CFramePuk * CFrame.new(-100, 20, 0))
                                    elseif AttackRandomType == 3 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    elseif AttackRandomType == 4 then
                                        two(CFramePuk * CFrame.new(100, 20, 0))
                                    elseif AttackRandomType == 5 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    end
                                end
                            end
                        end
                    end)
                end    
            end
        end)




    local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)
    spawn(function()
        while wait() do
            if _G.Settings["Auto Farm Level"]    then
                pcall(function()         
                    CheckQuest()
                        if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                            StartMagnet = false
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                        end
                        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                            StartMagnet = false
                            CheckQuest()                
                            repeat wait()                         
                                if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1700 then
                                    two(CFrameQ) 
                                elseif  (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1700 then
                                    tp(CFrameQ) 
                                end
                            until (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings["Auto Farm Level"]


                            if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                if game.Players.LocalPlayer.Character.Humanoid.Health > 0 and (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                    wait(0.4)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
                                end
                            
                        end
                                            
                        
                        elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            CheckQuest()
                            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        if v.Name == Ms then
                                            repeat wait(_G.Fast_Delay)
                                                
                                                if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"]) 
                                                    StartMagnet = true                                  
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.HumanoidRootPart.CanCaillde = false  
                                                else
                                                    StartMagnet = false
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                                end
                                            until not _G.Settings["Auto Farm Level"]   or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            
                                        end
                                    end
                                end
                            else
                                StartMagnet = false
                                if game:GetService("ReplicatedStorage"):FindFirstChild(Ms) then
                                    two(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame)
                                else	
                                    if AttackRandomType == 1 then
                                        two(CFramePuk * CFrame.new(0, 20, 100))
                                    elseif AttackRandomType == 2 then
                                        two(CFramePuk * CFrame.new(-100, 20, 0))
                                    elseif AttackRandomType == 3 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    elseif AttackRandomType == 4 then
                                        two(CFramePuk * CFrame.new(100, 20, 0))
                                    elseif AttackRandomType == 5 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    end
                                end
                            end
                        end
                    end)
                end    
            end
        end)



    local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)
    spawn(function()
        while wait() do
            if _G.AutoFram   then
                pcall(function()         
                    CheckQuest()
                        if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                            StartMagnet = false
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                        end
                        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                            StartMagnet = false
                            CheckQuest()
                            repeat wait() 
                                if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2200 then
                                    tp(CFrameQ)   
                                else
                                    two(CFrameQ)  
                                end
                            until (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.AutoFram 
                            if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                            if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                    wait(0.5)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
                                    wait(0.5)
                                end             
                            end
                        elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            CheckQuest()
                            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        if v.Name == Ms then
                                            repeat wait(_G.Fast_Delay)
                                                
                                                if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"]) 
                                                    StartMagnet = true               
                                                    if AttackRandomType == 1 then
                                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                                    elseif AttackRandomType == 2 then
                                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                                    elseif AttackRandomType == 3 then
                                                        two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                                    elseif AttackRandomType == 4 then
                                                        two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                                    elseif AttackRandomType == 5 then
                                                        two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                                    end
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.HumanoidRootPart.CanCaillde = false  
                                                
                                                else
                                                    StartMagnet = false
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                                end
                                            until not _G.AutoFram   or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            
                                        end
                                    end
                                end
                            else
                                StartMagnet = false
                                if game:GetService("ReplicatedStorage"):FindFirstChild(Ms) then
                                    two(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame)
                                else	
                                    if AttackRandomType == 1 then
                                        two(CFramePuk * CFrame.new(0, 20, 100))
                                    elseif AttackRandomType == 2 then
                                        two(CFramePuk * CFrame.new(-100, 20, 0))
                                    elseif AttackRandomType == 3 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    elseif AttackRandomType == 4 then
                                        two(CFramePuk * CFrame.new(100, 20, 0))
                                    elseif AttackRandomType == 5 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    end
                                end
                            end
                        end
                    end)
                end    
            end
        end)





        


        spawn(function()
            game:GetService("RunService").Heartbeat:Connect(function() CheckQuest()
                pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if (_G.FramSuper or _G.AutoFram or _G.Settings["Auto Farm Level"] or _G.FramDeath or _G.FramShark or _G.Auto_Mastery_Gun or _G.Auto_Mastery_Frutis) and StartMagnet and v.Name == Ms and (v.HumanoidRootPart.Position - PosMon.Position).Magnitude <= 350 then
                            v.HumanoidRootPart.CFrame = PosMon
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
                end)
            end)
        end)



    
        





    
    

    
    




    spawn(function ()
        while task.wait()   do 
            if _G.AutoRejoin then    
                game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(a3)
                    if a3.Name == "ErrorPrompt" and a3:FindFirstChild("MessageArea") and a3.MessageArea:FindFirstChild("ErrorFrame") then
                            game:GetService("TeleportService"):Teleport(game.PlaceId, LocalPlayer)
                    end
                end)
            end
        end
    end)   
                            
                        
            function unEquipWeapon222(Weapon)
                if game.Players.LocalPlayer.Character:FindFirstChild(Weapon) then
                    wait(.5)
                    game.Players.LocalPlayer.Character:FindFirstChild(Weapon).Parent = game.Players.LocalPlayer.Backpack
                    wait(.1)
                end
            end
            

        


        FightStlye:AddToggle({
        Name = "Auto Superhuman",
        Value =  _G.Settings["Auto SuperHuman"],
        Flag = "Auto Superhuman",
        Callback = function(value)
            _G.AutoSuperHumanFully = value
            _G.Settings["Auto SuperHuman"] = value
            if _G.AutoSuperHumanFully == true then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro") 
            end
            
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
                _G.FramSuper  = false
                _G.RiadSuper = false
                end)
            end
        end
    })

    FightStlye:AddToggle({
        Name = "Auto Deathstep",
        Value =  _G.Settings["Auto Deathstep"],
        Flag = "Auto Deathstep",
        Callback = function(value)
            _G.Settings["Auto Deathstep"] = value
            _G.Deathstepv2  = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
                end)
            end
        end
    })


    FightStlye:AddToggle({
        Name = "Auto Sharkman Karate",
        Value =  _G.Settings["Auto Sharkman Karate"],
        Flag = "Auto Sharkman Karate",
        Callback = function(value)
            _G.Settings["Auto Sharkman Karate"] = value
            _G.SharkmanKarate  = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
                end)
            end
        end
    })


    FightStlye:AddToggle({
        Name = "Auto Dragon Talon",
        Value =  _G.Settings["Auto Dragon Talon"],
        Flag = "Auto Dragon Talon",
        Callback = function(value)
            _G.Settings["Auto Dragon Talon"] = value
            _G.DragonTalon  = value
            SaveSettings()
            if value == false then
                pcall(function()
                end)
            end
        end
    })


    FightStlye:AddToggle({
        Name = "Auto Electric Claw",
        Value =  _G.Settings["Auto Electric Claw"],
        Flag = "Auto Electric Claw.",
        Callback = function(value)
            _G.Settings["Auto Electric Claw"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                end)
            end
        end
    })







    spawn(function()
        while wait() do
            if _G.Deathstepv2 then
                pcall(function()
                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep") == 2 then
                    elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep") == 0 then
                        -- Check have Black Leg
                        
                        if not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg') or not game.Players.localPlayer.Character:FindFirstChild('Black Leg') then
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
                        end
                        
                        if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg') and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg').Level.Value <= 400) or (game.Players.localPlayer.Character:FindFirstChild('Black Leg')  and game.Players.localPlayer.Character:FindFirstChild('Black Leg').Level.Value <= 400) then
                        
                            _G.Settings["Select Weapon"] = 'Black Leg'
                        
                            
                        end
                        
                    if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg') and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg').Level.Value >= 400) or (game.Players.localPlayer.Character:FindFirstChild('Black Leg')  and game.Players.localPlayer.Character:FindFirstChild('Black Leg').Level.Value >= 400) then
                            _G.FramDeath = false
                        if game.Players.LocalPlayer.Data.Level.Value > 1100 then  
                            if game:GetService("Players").LocalPlayer.Data.Beli.Value >= 2500000 then
                                if game:GetService("Players").LocalPlayer.Data.Fragments.Value >= 5000 then
                                    _G.RiadD = false
                                    _G.Next = false
                                    _G.KillAura = false
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                                elseif game:GetService("Players").LocalPlayer.Data.Fragments.Value <= 5000 then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                                    _G.FramDeath = false
                                    _G.RiadD = true
                                    _G.Next = true
                                    _G.KillAura = true
                                end
                            elseif game:GetService("Players").LocalPlayer.Data.Beli.Value <= 2500000 then
                                if _G.Settings["Auto Farm Level"]  == false then
                                    _G.Settings["Auto Farm Level"]  = true 
                                end
                                _G.Settings["Select Weapon"] = 'Black Leg'
                            
                            end
                        elseif game.Players.LocalPlayer.Data.Level.Value <= 1099 then  
                            if _G.Settings["Auto Farm Level"]  == false then
                                _G.Settings["Auto Farm Level"]  = true 
                            end
                                    _G.Settings["Select Weapon"] = 'Black Leg'
                        end
                    end
                    end
                end)
            else
                _G.RiadD = false
                _G.Next = false
                _G.KillAura = false
            end
        end
    end)








    spawn(function()
        while wait() do
            if _G.KillAura then
                for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        pcall(function()
                            repeat wait(_G.Fast_Delay)
                                v.Humanoid.Health = 0
                                v.HumanoidRootPart.CanCollide = false
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            until not _G.KillAura  or not v.Parent or v.Humanoid.Health <= 0
                        end)
                    end
                end
            end
        end
    end)


    spawn(function()
        while wait() do
            if _G.Kill_Aura then
                for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        pcall(function()
                            repeat wait(_G.Fast_Delay)
                                v.Humanoid.Health = 0
                                v.HumanoidRootPart.CanCollide = false
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            until not _G.Kill_Aura  or not v.Parent or v.Humanoid.Health <= 0
                        end)
                    end
                end
            end
        end
    end)

    spawn(function()
        while wait() do
            if _G.Kill_AuraShark then
                for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        pcall(function()
                            repeat wait(_G.Fast_Delay)
                                v.Humanoid.Health = 0
                                v.HumanoidRootPart.CanCollide = false
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            until not _G.Kill_AuraShark  or not v.Parent or v.Humanoid.Health <= 0
                        end)
                    end
                end
            end
        end
    end)
    spawn(function()
        while wait() do
            pcall(function()
                if _G.Raid then
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then
                    if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 5" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2300 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 4" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 3" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2100 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 2" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,60,0))
                                --wait(2)
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 1" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,70,0))
                                --wait(2)
                            end
                        end
                    else
                        wait(3)
                    end
                end
                else
                    wait(3)
                end
            end)
        end
    end)



    spawn(function()
        while wait() do   
                if _G.ShakNext then
                    pcall(function()
                        
                
    if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            if v.Name == "Island 5" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
                two(v.CFrame*CFrame.new(0,70,0))
            end
        end
    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            if v.Name == "Island 4" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
                two(v.CFrame*CFrame.new(0,70,0))
            end
        end
    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            if v.Name == "Island 3" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
                two(v.CFrame*CFrame.new(0,70,0))
            end
        end
    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            if v.Name == "Island 2" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
                two(v.CFrame*CFrame.new(0,60,0))
                --wait(2)
            end
        end
    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            if v.Name == "Island 1" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3000 then
                two(v.CFrame*CFrame.new(0,70,0))
                --wait(2)
            end
        end
    end
    end)
            end    
        end
    end)

    -- spawn(function()
    -- 	while wait() do
            
    -- 			if _G.ShakNext then
    --                 -- pcall(function()
    --                 if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then
    -- 				if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
    -- 					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    -- 						if v.Name == "Island 5" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2300 then
    -- 							two(v.CFrame*CFrame.new(0,70,0))
    -- 						end
    -- 					end
    -- 				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
    -- 					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    -- 						if v.Name == "Island 4" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
    -- 							two(v.CFrame*CFrame.new(0,70,0))
    -- 						end
    -- 					end
    -- 				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
    -- 					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    -- 						if v.Name == "Island 3" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2100 then
    -- 							two(v.CFrame*CFrame.new(0,70,0))
    -- 						end
    -- 					end
    -- 				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
    -- 					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    -- 						if v.Name == "Island 2" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
    -- 							two(v.CFrame*CFrame.new(0,60,0))
    -- 							--wait(2)
    -- 						end
    -- 					end
    -- 				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
    -- 					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    -- 						if v.Name == "Island 1" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
    -- 							two(v.CFrame*CFrame.new(0,70,0))
    -- 							--wait(2)
    -- 						end
    -- 					end
    -- 				else
    -- 					wait(3)
    -- 				end
    --             end
    --         -- end)
    -- 			else
    -- 				wait(3)
    -- 			end
            
    -- 	end
    -- end)








    spawn(function()
        while wait() do
            pcall(function()
                if _G.Next then
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then
                    if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 5" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2300 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 4" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 3" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2100 then
                                two(v.CFrame*CFrame.new(0,70,0))
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 2" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,60,0))
                                --wait(2)
                            end
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
                            if v.Name == "Island 1" and (v.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 2000 then
                                two(v.CFrame*CFrame.new(0,70,0))
                                --wait(2)
                            end
                        end
                    else
                        wait(3)
                    end
                end
                else
                    wait(3)
                end
            end)
        end
    end)




    spawn(function()
        while wait() do
            pcall(function()
            if _G.RiadSuper then
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                    _G.Raid = false
                    _G.Kill_Aura = false
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        if SecondSea then
                            fireclickdetector(game.Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true    
                            
                        elseif ThirdSea then
                            fireclickdetector(game.Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true  
                        end
                    elseif not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                        wait(5.666)
                        if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                                if v:IsA ("Tool") then
                                    PsFurits = v.Handle.CFrame
                                    repeat wait()
                                        two(PsFurits)
                                    until (game.Players.LocalPlayer.Character.HumanoidRootPart.Position  - PsFurits.Position) or not _G.RiadSuper
                                end
                            end
                        end
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame"),"You must wait") then
                            Get()
                        end
                    end
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then 
                    _G.Raid = true
                    _G.Kill_Aura = true
                end
            end
        end)
        end
    end)




    spawn(function()
        while wait() do
            pcall(function()
            if _G.RiadSharkMan then
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                    _G.ShakNext = false
                    _G.Kill_AuraShark = false
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        if SecondSea then
                            fireclickdetector(game.Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true    
                            
                        elseif ThirdSea then
                            fireclickdetector(game.Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true  
                        end
                    elseif not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                        wait(5.666)
                        if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                                if v:IsA ("Tool") then
                                    PsFurits = v.Handle.CFrame
                                    repeat wait()
                                        two(PsFurits)
                                    until (game.Players.LocalPlayer.Character.HumanoidRootPart.Position  - PsFurits.Position) or not _G.RiadSharkMan
                                end
                            end
                        end
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame"),"You must wait") then
                            Get()
                        end
                    end
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then 
                    _G.ShakNext = true
                    _G.Kill_AuraShark = true
                end
            end
        end)
        end
    end)



































    spawn(function()
        while wait() do
            pcall(function()
            if _G.RiadD then
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                    _G.Next = false
                    _G.KillAura = false
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        if SecondSea then
                            fireclickdetector(game.Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true    
                            
                        elseif ThirdSea then
                            fireclickdetector(game.Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                            repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true  
                        end
                    elseif not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                        wait(5.666)
                        if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                                if v:IsA ("Tool") then
                                    PsFurits = v.Handle.CFrame
                                    repeat wait()
                                        two(PsFurits)
                                    until (game.Players.LocalPlayer.Character.HumanoidRootPart.Position  - PsFurits.Position) or not _G.RiadSuper
                                end
                            end
                        end
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame"),"You must wait") then
                            Get()
                        end
                    end
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then 
                    _G.Next = true
                    _G.KillAura = true
                end
            end
        end)
        end
    end)


    spawn(function()
        while wait() do
            if _G.Rengoku then
            pcall(function()       

                if CheckSw("Rengoku") then 
                    _G.Rengoku  = false
                    
                elseif not CheckSw("Rengoku") then
                    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') or game.Players.LocalPlayer.Character:FindFirstChild('Hidden Key') then
                        two(CFrame.new(6573.2583, 296.654755, -6963.81152, 0.928839445, -5.45712417e-08, 0.370482504, 1.90914271e-08, 1, 9.94334997e-08, -0.370482504, -8.5284718e-08, 0.928839445))
                        wait(.1)
                        itemequip('Hidden Key')
                    elseif not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') or not game.Players.LocalPlayer.Character:FindFirstChild('Hidden Key') then
                    if game:GetService("Workspace").Enemies:FindFirstChild("Snow Lurker [Lv. 1375]")  then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if  v.Name == "Snow Lurker [Lv. 1375]"  and v.Humanoid.Health > 0  then                    
                                    repeat wait(_G.Fast_Delay)
                                    
                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                end
                                itemequip(_G.Settings["Select Weapon"]) 
                                StartRengokuMagnet = true
                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))        
                                RengokuMon = v.HumanoidRootPart.CFrame
                                v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                v.Humanoid.WalkSpeed = 0
                                v.Head.CanCollide = false
                                v.Humanoid:ChangeState(11)
                            
                            
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                            until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Hidden Key") or _G.Rengoku  == false or not v.Parent or v.Humanoid.Health <= 0
                            StartRengokuMagnet = false  
                            end  
                        end
                            elseif not game:GetService("Workspace").Enemies:FindFirstChild("Snow Lurker [Lv. 1375]")  then
                                CFrameRenGoku = CFrame.new(5681.00977, 74.2431717, -6804.71143, -0.993254781, -7.20735542e-08, 0.115952194, -7.76175568e-08, 1, -4.32975895e-08, -0.115952194, -5.20054648e-08, -0.993254781)
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameRenGoku.Position).Magnitude <= 1700 then
                                    two(CFrameRenGoku)
                                elseif   (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameRenGoku.Position).Magnitude >= 1701  then
                                    tp(CFrameRenGoku)
                                end
                            end
                        end
                end  
            
                end)
            end
        end
    end)

    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            pcall(function()
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if _G.Rengoku  and StartRengokuMagnet and v.Name == "Snow Lurker [Lv. 1375]" and (v.HumanoidRootPart.Position - RengokuMon.Position).Magnitude <= 350 then
                        v.HumanoidRootPart.CFrame = RengokuMon
                        v.HumanoidRootPart.CanCollide = false
                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                        if v.Humanoid:FindFirstChild("Animator") then
                            v.Humanoid.Animator:Destroy()
                        end
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                    end
                end
            end)
        end)
    end)

    -- spawn(function()
    --     while wait() do
    --         if _G.RiadSuper then
    --             if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == false   then   
    --                 if not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Special Microchip') then
    --                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                    
    --                 elseif  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Special Microchip') then
                        
    --             elseif game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true then
    --                 for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                    
    --                         repeat wait()
    --                             v.Humanoid.Health = 0
    -- 							v.HumanoidRootPart.CanCollide = false
    -- 							v.HumanoidRootPart.Size = Vector3.new(50,50,50)
    -- 							v.HumanoidRootPart.Transparency = 1
    --                         until not _G.RiadSuper or v.Humanoid.Health <= 0 or not v.Parent
                                
                    
    --                 end
    --                 if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1') then
    --                     if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').Position).Magnitude <= 3000 then
    --                         two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').CFrame * CFrame.new(0,65,0))
    --                     end
    --                 end
    --             end
    --         end
    --     end
    -- end)

    -- -- spawn(function()
    -- --     while wait() do
    -- --         if _G.RiadSuper then
            
                    
                
            
    -- --                 if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true   then      
    -- --                     if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1') then
    -- --                         if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').Position).Magnitude  > 350 then
    -- --                           two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').CFrame)
    -- --                         elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').Position).Magnitude  <= 299  then
    -- --                             tween:Cancel()
    -- --                             two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 2').CFrame * CFrame.new(0,65,0))
    -- --                          end
    -- --                     elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 2') then
    -- --                         if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 1').Position).Magnitude <= 500 then                   
    -- --                                 tween:Cancel()
    -- --                             two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild('Island 2').CFrame * CFrame.new(0,65,0))
    -- --                         end
    -- --                     end               
    -- --                 end
    -- --             end
            
    -- --         end
    -- --     end
    -- -- end)



    function checkraid()
        spawn(function()
        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == false then
            if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame"),"You must wait") then
                    Get()
                end
            end
        end
        end)
    end


    function unEquipWeapon222(Weapon)
        if game.Players.LocalPlayer.Character:FindFirstChild(Weapon) then
            wait(.5)
            game.Players.LocalPlayer.Character:FindFirstChild(Weapon).Parent = game.Players.LocalPlayer.Backpack
            wait(.1)
        end
    end












    spawn(function()
        while wait() do
            pcall(function()
                if _G.AutoSuperHumanFully  then                
                    if game:GetService("Players").LocalPlayer.Data.Beli.Value >= 500000 and (game.Players.LocalPlayer.Character:FindFirstChild("Combat") or game.Players.LocalPlayer.Backpack:FindFirstChild("Combat")) then
                        _G.Settings["Select Weapon"] = "Combat"
                        local args = {
                            [1] = "BuyElectro"
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    elseif game:GetService("Players").LocalPlayer.Data.Beli.Value <= 500000 and (game.Players.LocalPlayer.Character:FindFirstChild("Combat") or game.Players.LocalPlayer.Backpack:FindFirstChild("Combat")) then
                        _G.Settings["Select Weapon"] = "Combat"
                    end  


                    if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Electro') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Electro').Level.Value <= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Electro') and game.Players.LocalPlayer.Character:FindFirstChild('Electro').Level.Value <= 300) then                        
                        _G.Settings["Select Weapon"] = "Electro"
                    elseif (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Electro') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Electro').Level.Value >= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Electro') and game.Players.LocalPlayer.Character:FindFirstChild('Electro').Level.Value >= 300) then                        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
                    end

                    if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg').Level.Value <= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Black Leg') and game.Players.LocalPlayer.Character:FindFirstChild('Black Leg').Level.Value <= 300) then                        
                        _G.Settings["Select Weapon"] = "Black Leg"
                    elseif (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Black Leg').Level.Value >= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Black Leg') and game.Players.LocalPlayer.Character:FindFirstChild('Black Leg').Level.Value >= 300) then                        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
                    end

                    if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate').Level.Value <= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate') and game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate').Level.Value <= 300) then
                        _G.Settings["Select Weapon"] = "Fishman Karate"
                    elseif (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate').Level.Value >= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate') and game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate').Level.Value >= 300) then                        
                        if  game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2") == 2 then
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
        
                            elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2") == 0  then
                                if game.Players.LocalPlayer.Data.Fragments.Value < 1500 then
                                    if game.Players.LocalPlayer.Data.Level.Value > 1100 then                      
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                                        _G.RiadSuper = true
                                        _G.Raid = true
                                        _G.Kill_Aura = true
                                    elseif game.Players.LocalPlayer.Data.Level.Value <= 1100 then           
                                            _G.Settings["Select Weapon"] = "Fishman Karate"
                                    end
                                elseif game.Players.LocalPlayer.Data.Fragments.Value >= 1500 then
                                    if _G.Atuofarm  == true then
                                        _G.Atuofarm  = false
                                    end
                                    _G.RiadSuper  =  false
                                    _G.Raid = false
                                    _G.Kill_Aura = false
                                    local args = {
                                        [1] = "BlackbeardReward",
                                        [2] = "DragonClaw",
                                        [3] = "2"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                            end
                        end

                        if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Dragon Claw') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Dragon Claw').Level.Value <= 300) or (game.Players.LocalPlayer.Character:FindFirstChild('Dragon Claw') and game.Players.LocalPlayer.Character:FindFirstChild('Dragon Claw').Level.Value <= 300) then
                            _G.Settings["Select Weapon"] = "Dragon Claw"
                            if _G.Atuofarm  == false then
                                _G.Atuofarm  = true
                            end
                        end

                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                            local Beli = game:GetService("Players").LocalPlayer.Data.Beli.Value
                            if Beli >= 300000 then
                                local args = {
                                    [1] = "BuySuperhuman"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            else
                                
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                            end
                        end
                        if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                            local Beli = game:GetService("Players").LocalPlayer.Data.Beli.Value
                            if Beli >= 300000 then
                                local args = {
                                    [1] = "BuySuperhuman"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            else
                                
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                            end
                        end
                end
            end)
        end
    end)









        



























        function Get()
            local Furits = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventoryFruits")
            for i,v in pairs(Furits) do
            if  v.Price <= 999999  then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LoadFruit",v.Name)
                end
            end
        end
    
        if SecondSea then
            CheckL = LegS:AddLabel({
                Name = ''
            })
            LegS:AddToggle({
                Name = "Auto Legendary Sword",
                Value = _G.Settings["Auto Legendary Sword"],
                Flag = "Auto Legendary Sword",
                Callback = function(value)
                    _G.Settings["Auto Legendary Sword"] = value
                    _G.Auto_BuyLegendarySword = value
                    SaveSettings()
                    if value == false then
            
                    end
                end
            })
            LegS:AddToggle({
                Name = "Auto Legendary Sword Hop",
                Value = _G.Settings["Auto Legendary Sword Hop"],
                Flag = "Auto Legendary Sword Hop",
                Callback = function(value)
                    _G.Settings["Auto Legendary Sword Hop"] = value
                    SaveSettings()
                end
            })
            spawn(function()
                while wait(.1) do
                if  _G.Settings["Auto Legendary Sword"] and  _G.Settings["Auto Legendary Sword Hop"] then
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Manager","1"),"Good") then

                        else
                            wait(5)
                            Hop()
                            wait(5)
                        end             
                end
                end
            end)
            
        
            spawn(function()
                while wait() do
                    pcall(function()
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Manager","1"),"Good") then
                            CheckL:Set('Check : Spawn .')
                            wait(.3)
                            CheckL:Set('Check : Spawn ..')
                            wait(.3)
                            CheckL:Set('Check : Spawn ...')
                            wait(.3)
                        else
                            CheckL:Set('Check : Not Spawn .')
                            wait(.3)
                            CheckL:Set('Check : Not Spawn ..')
                            wait(.3)
                            CheckL:Set('Check : Not Spawn ...')
                            wait(.3)
                        end               
                    end)
                end
            end)
        end
    

        spawn(function()
            while wait(.1) do
                pcall(function() 
                    if _G.Auto_BuyLegendarySword then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","1")
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","2")
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer","3")
                    end
                end)
            end
        end)

        spawn(function()
            while wait() do
                if Auto_Swan_Glass then
                    pcall(function()
                        if  game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","1") == 0 then
                            
                        elseif  game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","1") ~= 0 then
                            RobloxNotify('ยังไม่ได้ทำเควสเปิดประตู',5)
                        end
                    end)
                end
            end
        end)





        task.spawn(function()
            while wait() do
                if _G.SharkmanKarate then
                    pcall(function()
                        
                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true) == 1 then
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
                        elseif string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true),"keys")  then
                            if not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') or not game.Players.localPlayer.Character:FindFirstChild('Fishman Karate') then
                                local args = {
                                    [1] = "BuyFishmanKarate"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            end
                            -- Mas 400
                            if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate').Level.Value <= 400) or (game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate') and game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate').Level.Value <= 400) then
                                _G.FramShark  = true
                                _G.Settings["Select Weapon"] = 'Fishman Karate'
                            end   
                            -- Mas >= 400
        
                            if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate').Level.Value >= 400) or (game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate') and game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate').Level.Value >= 400) then
                                if not string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate"), "keys") then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true)
                                end
                            end
        
        
        
                            if (game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate') and  game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Fishman Karate').Level.Value >= 400) or (game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate') and game.Players.LocalPlayer.Character:FindFirstChild('Fishman Karate').Level.Value >= 400) then
                                if game.Players.LocalPlayer.Data.Level.Value <= 1099 then
                                    _G.FramShark  = true
                                    _G.Settings["Select Weapon"] = 'Fishman Karate'
                                elseif game.Players.LocalPlayer.Data.Level.Value >= 1100 then
                                    if game:GetService("Players").LocalPlayer.Data.Beli.Value >= 2500000 then
                                        if game:GetService("Players").LocalPlayer.Data.Fragments.Value >= 5000 then
                                            _G.FramShark  = false
                                            _G.RiadSharkMan = false
                                            _G.ShakNext = false
                                            _G.Kill_AuraShark = false
                                            if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate"), "keys") then
                                                if game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                                    itemequip("Water Key")
                                                    wait(0.5)
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true)
                                                elseif not game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or not game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                                    if game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper [Lv. 1475] [Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Tide Keeper [Lv. 1475] [Boss]") then
                                                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                                if v.Name == "Tide Keeper [Lv. 1475] [Boss]" then
                                                                    if v.Humanoid.Healt > 0 then
                                                                        repeat wait()
                                                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                                            end
                                                                            itemequip(_G.Settings["Select Weapon"]) 
                                                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))        
                                                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                                            v.Humanoid.WalkSpeed = 0
                                                                            v.Head.CanCollide = false
                                                                            v.Humanoid:ChangeState(11)
                                                                            v.Humanoid:ChangeState(14)
                                                                        
                                                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                                                        until  not _G.SharkmanKarate or  game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") 
                                                                    end
                                                                end
                                                            end
        
                                                    elseif not game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper [Lv. 1475] [Boss]") or not game:GetService("Workspace").Enemies:FindFirstChild("Tide Keeper [Lv. 1475] [Boss]") then
                                                    wait(3.5)
                                                        Hop()
                                                    elseif  game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper [Lv. 1475] [Boss]") then
                                                            two(game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper [Lv. 1475] [Boss]").HumanoidRootPart.CFrame*CFrame.new(0,30,0))
                                                    end
                                                end
                                            end
                                        elseif game:GetService("Players").LocalPlayer.Data.Fragments.Value <= 5000 then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select","Flame")
                                            if _G.Settings["Auto Farm Level"]  == true then
                                                _G.Settings["Auto Farm Level"]  = false 
                                            end
                                            _G.RiadSharkMan = true
                                            _G.ShakNext = true
                                            _G.Kill_AuraShark = true
                                        end
                                    elseif game:GetService("Players").LocalPlayer.Data.Beli.Value <= 2500000 then
                                        if _G.Settings["Auto Farm Level"]  == false then
                                            _G.Settings["Auto Farm Level"]  = true 
                                        end
                                        _G.Settings["Select Weapon"] = 'Fishman Karate'
                                    end
                                end
                            end
                        end
                    end)
                else
                    _G.FramShark  = false
                    _G.RiadSharkMan = false
                    _G.ShakNext = false
                    _G.Kill_AuraShark = false
                end
            end
        end)



    if SecondSea then
        


        OT:AddToggle({
            Name = "Auto Quest Swan",
            Value = _G.Settings["Auto Quest Swan"],
            Flag = "Auto Quest Swan",
            Callback = function(value)
                _G.AutoQuestSwan =  value
                _G.Settings["Auto Quest Swan"] = value
                SaveSettings()
                if value == false  then
                    tween:Cancel()
                end
            end
        })

        OT:AddToggle({
            Name = "Auto Rengoku",
            Value = _G.Settings["Auto Farm Rengoku"],
            Flag = "Auto Rengoku",
            Callback = function(value)
                _G.Rengoku = value
                _G.Settings["Auto Farm Rengoku"] = value
                SaveSettings()
                if value == false  then
                    pcall(function()
                        
                
                    tween:Cancel()
                end)
                end
            end
        })


        OT:AddToggle({
            Name = "Auto Bartilo Quest",
            Value = _G.Settings["Auto Bartilo Quest"],
            Flag = "Auto Bartilo Quest",
            Callback = function(value)
                _G.BartiloQuest = value
                _G.Settings["Auto Bartilo Quest"] = value
                SaveSettings()
                if value == false  then
                    pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        OT:AddToggle({
            Name = "Auto Midnight Blade",
            Value = _G.Settings["Auto Midnight Blade"],
            Flag = "Auto Midnight Blade",
            Callback = function(value)
                _G.MidNight = value
                _G.Settings["Auto Midnight Blade"] = value
                SaveSettings()
                if value == false  then
                    pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })


        

        OT:AddToggle({
            Name = "Auto True Triple Katana",
            Value = _G.Settings["Auto True Triple Katana"],
            Flag = "Auto True Triple Katana",
            Callback = function(value)
                _G.Settings["Auto True Triple Katana"]  = value
                _G.TrueTipleKatana = value
                SaveSettings()
                if value == false  then
                    pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

    end

    OT:AddToggle({
        Name = "Auto Grab Chest",
        Value = _G.Settings["Auto Grab Chest"],
        Flag = "Auto Grab Chest",
        Callback = function(value)
            _G.Settings["Auto Grab Chest"] =  value
            SaveSettings()
            if value == false  then
                pcall(function()
                    tween:Cancel()
                    two(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
                    GrabChest = false
                end)
            end
        end
    })


        if ThirdSea then
            OT:AddToggle({
                Name = "Auto Farm Bone",
                Value = _G.Settings["Auto Farm Bone"],
                Flag = "Auto Farm Bone",
                Callback = function(value)
                    _G.Settings["Auto Farm Bone"] =  value
                    BoneFarm = value
                    SaveSettings()
                    if value == false  then
                        pcall(function()
                            tween:Cancel()
                        end)
                    end
                end
            })
            OT:AddToggle({
                Name = "Auto Random Bone",
                Value = _G.Settings["Auto Random Bone"],
                Flag = "Auto Random Bone",
                Callback = function(value)
                    _G.Settings["Auto Random Bone"] =  value
                    RandomBone = value
                    SaveSettings()
                    if value == false  then
                    end
                end
            })
            OT:AddToggle({
                Name = "Auto Yama",
                Value = _G.Settings["Auto Yama"],
                Flag = "Auto Yama",
                Callback = function(value)
                    _G.Settings["Auto Yama"] =  value
                    _G.Auto_Yama = value
                    SaveSettings()
                    if value == false  then
                    end
                end
            })
            OT:AddToggle({
                Name = "Auto Rainbow Haki",
                Value = _G.Settings["Auto Rainbow Haki"],
                Flag = "Auto Rainbow Haki",
                Callback = function(value)
                    _G.Settings["Auto Rainbow Haki"] =  value
                    _G.RainbowHaki = value
                    SaveSettings()
                    if value == false  then
                        pcall(function()
                            tween:Cancel()
                        end)
                    end
                end
            })
        end


        spawn(function()
            while wait() do
                pcall(function()     
                if _G.AutoQuestSwan then
                    if game:GetService("Players").LocalPlayer.Data.Level.Value >= 1200 then
                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","1") ~= 0 then
                            for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventoryFruits")) do
                            if  v.Price >= 1000000  then
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LoadFruit",v.Name)
                                wait(2)
                                itemequip(v.Name)
                                wait(2)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","1")
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","2")
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","3")
                                end
                            end
                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TalkTrevor","1") == 0 then
                            RobloxNotify('Quest ComPlate',3)
                        end
                    end
                end
                end)
            end
        end)




        spawn(function()
            while wait() do
                if _G.TrueTipleKatana then
                    pcall(function()
                        local Beli = game:GetService("Players").LocalPlayer.Data.Beli.Value
                        if Beli >= 3000000 then
                            pcall(function()
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("MysteriousMan","1")
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("MysteriousMan","2")
                            end)
                        end
                    end)
                end
            end
        end)




        spawn(function()
            while wait() do
                if _G.BartiloQuest then
                    pcall(function()
                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 0 and game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 then
                        if  string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Swan Pirates") then
                            if game:GetService("Workspace").Enemies:FindFirstChild('Swan Pirate [Lv. 775]') then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == 'Swan Pirate [Lv. 775]'  then
                                        repeat wait(_G.Fast_Delay)
                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                            end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            BartiloBring = true
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))        
                                            PosMonBarto = v.HumanoidRootPart.CFrame
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.WalkSpeed = 0
                                            v.Head.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                                
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                        until  _G.BartiloQuest == false or not v.Parent or v.Humanoid.Health <= 0 
                                        BartiloBring = false
                                    end
                                end
                            elseif not  game:GetService("Workspace").Enemies:FindFirstChild('Swan Pirate [Lv. 775]') then
                                CFrameJ = CFrame.new(846.6524658203125, 121.58216857910156, 1212.1435546875)
                                two(CFrameJ)
                            end
                        elseif not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Swan Pirates") then
                            CFrameQb = CFrame.new(-459.536499, 73.0200729, 301.540497, 0.618552029, -8.29051032e-08, 0.785743833, 3.4518159e-08, 1, 7.83382887e-08, -0.785743833, -2.13338787e-08, 0.618552029)
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQb.Position).Magnitude <= 8  then
                                wait(.3)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BartiloQuest",1) 
                            elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQb.Position).Magnitude <= 1700 then
                                    two(CFrameQb)                  
                            elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQb.Position).Magnitude >= 1701 then
                                tp(CFrameQb)
                            end
                        end

                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 1 and game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Jeremy [Lv. 850] [Boss]")  then
                                    for i, v in pairs( game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Jeremy [Lv. 850] [Boss]" then
                                            if v:FindFirstChild('Humanoid') then
                                                repeat wait(_G.Fast_Delay)
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"])
                                                    two(v.HumanoidRootPart.CFrame *CFrame.new(0,20,0)) 
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.Head.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                            
                                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                                until _G.BartiloQuest == false or v.Humanoid.Health <= 0 or not v.Parent         
                                            end             
                                        end
                                    end

                            elseif not  game:GetService("Workspace").Enemies:FindFirstChild("Jeremy [Lv. 850] [Boss]") then
                                two(CFrame.new(2195.38916015625, 448.930908203125, 545.3132934570312))
                            end
                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 2 and game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 then
                            CFrameCop = CFrame.new(-1832.87219, 10.4324913, 1691.61743, -0.997044623, 6.64495516e-08, 0.0768243894, 6.98422511e-08, 1, 4.14750225e-08, -0.0768243894, 4.67180392e-08, -0.997044623)
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameCop.Position).Magnitude <= 70 then
                                
                                    wait(2)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate1.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate2.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate3.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate4.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate5.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate6.CFrame * CFrame.new(2,0,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate7.CFrame * CFrame.new(0,2,0)
                                    wait(1)
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.Dressrosa.BartiloPlates.Plate8.CFrame * CFrame.new(0,2,0)
                            else
                                two(CFrameCop)
                            end
                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 3 then
                            
                        end
                    end)
                end
            end
        end)


        spawn(function()
            game:GetService("RunService").Heartbeat:Connect(function()
                pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if _G.BartiloQuest and BartiloBring and v.Name == "Swan Pirate [Lv. 775]" and (v.HumanoidRootPart.Position - PosMonBarto.Position).Magnitude <= 100 then
                            v.HumanoidRootPart.CFrame = PosMonBarto
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
                end)
            end)
        end)



        function Material(matname)
            for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
                if type(v) == "table" then
                    if v.Type == "Material" then
                        if v.Name == matname then
                            return v.Count
                        end
                    end
                end
            end
            return 0
        end

        function CheckSw(Sword)
            for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
                if type(v) == "table" then
                    if v.Type == "Sword" then
                        if v.Name == Sword then
                            RobloxNotify('Have ' ..Sword ,3)
                        end
                    end
                end
            end
        end


        spawn(function()
            while wait() do
                if _G.MidNight then
                    pcall(function()
                            if Material('Ectoplasm') >= 100 then
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","Buy",3)
                                wait()
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","BuyCheck",3)
                            elseif Material('Ectoplasm') <= 100 then
                                
                                if game:GetService("Workspace").Enemies:FindFirstChild('Ship Deckhand [Lv. 1250]') then
                                    for i, v in pairs( game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Ship Deckhand [Lv. 1250]" then
                                            if v:FindFirstChild('Humanoid') then
                                                repeat wait(_G.Fast_Delay)
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"])
                                                    PosMonMidNight = v.HumanoidRootPart.CFrame
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,20,0)) 
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.Head.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                        
                                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                                until _G.MidNight == false or v.Humanoid.Health <= 0 or not v.Parent         
                                            end             
                                        end
                                    end
                                elseif not game:GetService("Workspace").Enemies:FindFirstChild('Ship Deckhand [Lv. 1250]') then
                                    CFrameMb = CFrame.new(639.555603, 125.729118, 32971.9023, 0.989942968, 2.67096762e-08, -0.141467035, -2.37037714e-08, 1, 2.29332162e-08, 0.141467035, -1.93492724e-08, 0.989942968)
                                    if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMb.Position).Magnitude <= 2100 then
                                        two(CFrameMb)
                                    elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameMb.Position).Magnitude >= 2101 then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.2125244140625, 126.97600555419922, 32852.83203125))
                                    end
                                end
                        end
                    end)
                end
            end
        end)






        spawn(function()
            game:GetService("RunService").Heartbeat:Connect(function()
                pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if _G.MidNight and MidNightBring and v.Name == "Ship Deckhand [Lv. 1250]" and (v.HumanoidRootPart.Position - PosMonMidNight.Position).Magnitude <= 350 then
                            v.HumanoidRootPart.CFrame = PosMonMidNight
                            v.Humanoid:ChangeState(14)
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
                end)
            end)
        end)



    FruitList  = {"Bomb-Bomb","Spike-Spike","Chop-Chop","Spring-Spring","Kilo-Kilo","Spin-Spin","Bird: Falcon","Smoke-Smoke","Flame-Flame","Ice-Ice","Sand-Sand","Dark-Dark","Revive-Revive","Diamond-Diamond","Light-Light","Love-Love","Rubber-Rubber","Barrier-Barrier","Magma-Magma","Door-Door","Quake-Quake","Human-Human: Buddha","String-String","Bird-Bird: Phoenix","Rumble-Rumble","Paw-Paw","Gravity-Gravity","Dough-Dough","Shadow-Shadow","Venom-Venom","Control-Control","Soul-Soul","Dragon-Dragon","Leopard-Leopard"}


    local CombatTap = PepsisWorld:CreateTab({
        Name = "Combat"
    })


    local Devil = CombatTap:CreateSection({
        Name = "// Devil Fruits //",
        Side = "Right"
    })


    DevilFruitSniper = {}
    ShopDevilSell = {}


    local GetFruits = game.ReplicatedStorage:FindFirstChild("Remotes").CommF_:InvokeServer("GetFruits");
        


    for i,v in next,GetFruits do
        table.insert(DevilFruitSniper,v.Name)
    end

    if SelectFruits == nil then
        SelectFruits = "Chop-Chop"
    end

    -- Script generated by SimpleSpy - credits to exx#9394





    if SelectFruits == false then
        SelectFruits = "Chop-Chop"
    end



    Devil:AddDropdown({
        Name = "Select Devil Fruit",
        List = DevilFruitSniper,
        Value = _G.Settings["Devil Fruit Sniper"],
        Callback = function(value)
            SelectFruits = value
            _G.Settings["Devil Fruit Sniper"] = value
            SaveSettings()
        end
    })



    Devil:AddToggle{
        Name = "Auto Buy Fruit",
        Flag = "Auto Buy Fruit",
        Value = _G.Settings["Auto Buy Fruit"],
        Callback = function(value)
            _G.AutoSelet = value
            _G.Settings["Auto Buy Fruit"] = value
            SaveSettings()
        end
    }


    Devil:AddToggle{
        Name = "Auto Bring Fruit",
        Flag = "Auto Bring Fruit",
        Value = _G.Settings["Auto Bring Fruit"],
        Callback = function(value)
            _G.BringFruit = value
            _G.Settings["Auto Bring Fruit"] = value
            SaveSettings()
            if value == false  then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    }

    spawn(function()
        while wait() do
            if _G.AutoSelet then
                local args = {
                    [1] = "PurchaseRawFruit",
                    [2] = SelectFruits,
                    [3] = false
                }
                
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))     
            end
        end
    end)




    spawn(function()
        while wait() do
            if _G.BringFruit then
                pcall(function()     
                for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                    if v:IsA ("Tool") then
                        PsFurits = v.Handle.CFrame
                        repeat wait()
                            two(PsFurits)
                        until (game.Players.LocalPlayer.Character.HumanoidRootPart.Position  - PsFurits.Position) or not _G.RiadSuper
                    elseif not v:IsA ("Tool") then
                        end
                    end
                end)
            end
        end
    end)


    Devil:AddToggle{
        Name = "Auto Store Fruit",
        Flag = "Auto Store Fruit",
        Value = _G.Settings["Auto Store Fruit"],
        Callback = function(value)
            _G.StoreFuit = value
            _G.Settings["Auto Store Fruit"] = value
            SaveSettings()
        end
    }


    Devil:AddToggle{
        Name = "Auto Random Fruit",
        Flag = "Auto Random Fruit",
        Value = _G.Settings["Auto Random Fruit"],
        Callback = function(value)
            _G.Settings["Auto Random Fruit"] = value
            _G.Auto_Random_Fruit = value
            SaveSettings()
        end
    }


    function j(str)
        return str:gsub(" Fruit", "")
    end

    spawn(function()
        while wait() do
            if _G.StoreFuit  then
                pcall(function()
                    -- Chekc BackPack
                for i, v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
                        if string.find(v.Name,'Fruit') then
                            itemequip(v.Name)  
                        end
                end  
                -- Check 
                for i,v in pairs (game:GetService("Workspace").Characters[(game.Players.LocalPlayer.Name)]:GetChildren()) do
                        if string.find(v.Name,'Fruit') then
                            Namef = j(v.Name.. '-'..v.Name)
                            print(Namef)
                            local args = {
                                [1] = "StoreFruit",
                                [2] = Namef,
                                [3] = game:GetService("Players").LocalPlayer.Character:FindFirstChild(v.Name)
                            }

                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        end
                    end


                end)
            end
        end
    end)












    local Stast = CombatTap:CreateSection({
        Name = "// Stast //"

    })

    local LabelByNino = Stast:AddLabel({
        Name = ' '
    })

    spawn(function()
        while wait() do
            pcall(function()
                A = game:GetService("Players").LocalPlayer.Data.Points.Value
                LabelByNino:Set('You Stats :  ' .. A)
                wait(1)
            end)
        end
    end)

    Stast:AddToggle{
        Name = "Auto Stats Melee",
        Flag = "Auto_Stats_Melee",
        Value = _G.Settings["Auto_Stats_Melee"],
        Callback = function(value)
            _G.Settings["Auto_Stats_Melee"] = value
            SaveSettings()
        end
    }

    spawn(function()
        while wait() do
            if _G.Settings["Auto_Stats_Melee"] then
                local args = {
                    [1] = "AddPoint",
                    [2] = "Melee",
                    [3] = _G.Point
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    Stast:AddToggle{
        Name = "Auto Stats Defense",
        Flag = "Auto_Stats_Defense",
        Value = _G.Settings["Auto_Stats_Defense"],
        Callback = function(value)
            _G.Settings["Auto_Stats_Defense"] = value
            SaveSettings()
        end
    }

    spawn(function()
        while wait() do
            if _G.Settings["Auto_Stats_Defense"] then
                local args = {
                    [1] = "AddPoint",
                    [2] = "Defense",
                    [3] = _G.Point
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    Stast:AddToggle{
        Name = "Auto Stats Sword",
        Flag = "Auto_Stats_Sword",
        Value = _G.Settings["Auto_Stats_Sword"],
        Callback = function(value)
            _G.Settings["Auto_Stats_Sword"] = value
            SaveSettings()
        end
    }

    spawn(function()
        while wait() do
            if _G.Settings["Auto_Stats_Sword"] then
                local args = {
                    [1] = "AddPoint",
                    [2] = "Sword",
                    [3] = _G.Point
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    Stast:AddToggle{
        Name = "Auto Stats Gun",
        Flag = "Auto_Stats_Gun",
        Value = _G.Settings["Auto_Stats_Gun"],
        Callback = function(value)
            _G.Settings["Auto_Stats_Gun"] = value
            SaveSettings()
        end
    }

    spawn(function()
        while wait() do
            if _G.Settings["Auto_Stats_Gun"] then
                local args = {
                    [1] = "AddPoint",
                    [2] = "Gun",
                    [3] = _G.Point
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    Stast:AddToggle{
        Name = "Auto Stats Devil Fruit",
        Flag = "Auto_Stats_Devil_Fruit",
        Value = _G.Settings["Auto_Stats_Devil Fruit"],
        Callback = function(value)
            _G.Settings["Auto_Stats_Devil Fruit"] = value
            SaveSettings()
        end
    }

    spawn(function()
        while wait() do
            if _G.Settings["Auto_Stats_Devil Fruit"] then
                local args = {
                    [1] = "AddPoint",
                    [2] = "Demon Fruit",
                    [3] = _G.Point
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    Stast:AddSlider({
        Name = "Select Point",
        Flag = "Select_Point",
        Value = _G.Settings["Point"],
        Min = 1,
        Max = 100,
        Textbox = true,
        Format = function(value)
            _G.Point = value
            _G.Settings["Point"] = value
            SaveSettings()
            return "Point : " .. tostring(value)
        end
    })




    local VisualTab = PepsisWorld:CreateTab({
        Name = "Visual"
    })


    local Tps = VisualTab:CreateSection({
        Name = "// Teleprot  //"

    })




    Tps:AddButton({
        Name = "First Sea",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
        end
    })


    Tps:AddButton({
        Name = "Second Sea",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")	
        end
    })


    Tps:AddButton({
        Name = "Third Sea",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
        end
    })


    local Tpst = VisualTab:CreateSection({
        Name = "// Setting  //",
        Side = 'Right'
    })

    Tpst:AddButton({
        Name = "Copy jop id",
        Callback = function()
            setclipboard(game.JobId)
        end
    })
    _G.Jobid = "Enter You Job id"
    Tpst:Textbox ({
            Name = "Enter You Job id",
            Flag = "EnterJobid",
            Value = _G.Jobid,
            Callback = function(value)
                _G.Jobid = value
                SaveSettings()
                return "EnterJobid "
            end
    })

    Tpst:AddButton({
        Name = "Teleport To Job id",
        Callback = function()
            game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, _G.Jobid , game.Players.LocalPlayer)
        end
    })
    Tpst:AddButton({
        Name = "Server Hop",
        Callback = function()
            Hop()
        end
    })
    Tpst:AddButton({
        Name = "ReJoin Sever",
        Callback = function()
            game:GetService("TeleportService"):Teleport(game.PlaceId, LocalPlayer)
        end
    })

    local Tp = VisualTab:CreateSection({
        Name = "// Teleprot  //",
        Side = 'Right'
    })



    Tp:AddDropdown({
        Name = "Select Plante",
        List = TeleportTable,
        Value = _G.SelectTeleport,
        Callback = function(value)
            _G.SelectTeleport = value
        end
    })

    Tp:AddToggle({
        Name = "Teleport",
        Value = _G.Teleport,
        Flag = "Teleport",
        Callback = function(value)
            _G.Starttw = value

            if _G.Starttw == true then
                    if _G.SelectTeleport == "WindMill" then
                        two(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))
                    elseif _G.SelectTeleport == "Marine" then
                        two(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))
                    elseif _G.SelectTeleport == "Middle Town" then
                        two(CFrame.new(-690.33081054688, 15.09425163269, 1582.2380371094))
                    elseif _G.SelectTeleport == "Jungle" then
                        two(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))
                    elseif _G.SelectTeleport == "Pirate Village" then
                        two(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))
                    elseif _G.SelectTeleport == "Desert" then
                        two(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))
                    elseif _G.SelectTeleport == "Snow Island" then
                        two(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))
                    elseif _G.SelectTeleport == "MarineFord" then
                        two(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))
                    elseif _G.SelectTeleport == "Colosseum" then
                        two(CFrame.new(-1427.6203613281, 7.2881078720093, -2792.7722167969))
                    elseif _G.SelectTeleport == "Sky Island 1" then
                        two(CFrame.new(-4869.1025390625, 733.46051025391, -2667.0180664063))
                    elseif _G.SelectTeleport == "Sky Island 2" then
                        two(CFrame.new(-4644.58789, 872.542419, -1742.38269, -0.886984944, -2.65218905e-08, -0.46179834,
                            -4.08027745e-09, 1, -4.95946892e-08, 0.46179834, -4.210548e-08, -0.886984944))
                    elseif _G.SelectTeleport == "Sky Island 3" then
                        two(CFrame.new(-7994.10546875, 5756.033203125, -1942.4979248047))
                    elseif _G.SelectTeleport == "Prison" then
                        two(CFrame.new(4875.330078125, 5.6519818305969, 734.85021972656))
                    elseif _G.SelectTeleport == "Magma Village" then
                        two(CFrame.new(-5247.7163085938, 12.883934020996, 8504.96875))
                    elseif _G.SelectTeleport == "Under Water Island" then
                        two(CFrame.new(3876.6374511719, 5.3731470108032, -1896.9306640625))
                    elseif _G.SelectTeleport == "Fountain City" then
                        two(CFrame.new(5127.1284179688, 59.501365661621, 4105.4458007813))
                    elseif _G.SelectTeleport == "Shank Room" then
                        two(CFrame.new(-1442.16553, 29.8788261, -28.3547478))
                    elseif _G.SelectTeleport == "Mob Island" then
                        two(CFrame.new(-2850.20068, 7.39224768, 5354.99268))
                    elseif _G.SelectTeleport == "Cafe" then
                        two(CFrame.new(-380.47927856445, 77.220390319824, 255.82550048828))
                    elseif _G.SelectTeleport == "Dock" then
                        two(CFrame.new(-11.311455726624, 29.276733398438, 2771.5224609375))
                    elseif _G.SelectTeleport == "Dark Area" then
                        two(CFrame.new(3780.0302734375, 22.652164459229, -3498.5859375))
                    elseif _G.SelectTeleport == "Flamingo Mansion" then
                        two(CFrame.new(-388.409912, 322.048523, 806.840515, -0.999702871, -9.59914885e-08, -0.024374593, -9.76881864e-08, 1, 6.84183021e-08, 0.024374593, 7.07790875e-08, -0.999702871))
                    elseif _G.SelectTeleport == "Flamingo Room" then
                        two(CFrame.new(2284.4140625, 15.152037620544, 875.72534179688))
                    elseif _G.SelectTeleport == "Green Zone" then
                        two(CFrame.new(-2448.5300292969, 73.016105651855, -3210.6306152344))
                    elseif _G.SelectTeleport == "Factory" then
                        two(CFrame.new(424.12698364258, 211.16171264648, -427.54049682617))
                    elseif _G.SelectTeleport == "Colossuim" then
                        two(CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))
                    elseif _G.SelectTeleport == "Zombie Island" then
                        two(CFrame.new(-5622.033203125, 492.19604492188, -781.78552246094))
                    elseif _G.SelectTeleport == "Two Snow Mountain" then
                        two(CFrame.new(753.14288330078, 408.23559570313, -5274.6147460938))
                    elseif _G.SelectTeleport == "Punk Hazard" then
                        two(CFrame.new(-6127.654296875, 15.951762199402, -5040.2861328125))
                    elseif _G.SelectTeleport == "Cursed Ship" then
                        two(CFrame.new(923.40197753906, 125.05712890625, 32885.875))
                    elseif _G.SelectTeleport == "Ice Castle" then
                        two(CFrame.new(6148.4116210938, 294.38687133789, -6741.1166992188))
                    elseif _G.SelectTeleport == "Forgotten Island" then
                        two(CFrame.new(-3032.7641601563, 317.89672851563, -10075.373046875))
                    elseif _G.SelectTeleport == "Ussop Island" then
                        two(CFrame.new(4816.8618164063, 8.4599885940552, 2863.8195800781))
                    elseif _G.SelectTeleport == "Mini Sky Island" then
                        two(CFrame.new(-288.74060058594, 49326.31640625, -35248.59375))
                    elseif _G.SelectTeleport == "Great Tree" then
                        two(CFrame.new(2681.2736816406, 1682.8092041016, -7190.9853515625))
                    elseif _G.SelectTeleport == "Castle On The Sea" then
                        two(CFrame.new(-5044.7612304688, 314.85876464844, -2995.3803710938))
                    elseif _G.SelectTeleport == "MiniSky" then
                        two(CFrame.new(-260.65557861328, 49325.8046875, -35253.5703125))
                    elseif _G.SelectTeleport == "Floating Turtle" then
                        two(CFrame.new(-13274.528320313, 531.82073974609, -7579.22265625))
                    elseif _G.SelectTeleport == "Port Town" then
                            two(CFrame.new(-275.21615600586, 43.755737304688, 5451.0659179688))                 
                    elseif _G.SelectTeleport == "Hydra Island" then
                            two(CFrame.new(5541.2685546875, 668.30456542969, 195.48069763184))          
                    elseif _G.SelectTeleport == "Gaint Tree" then
                            two(CFrame.new(2276.0859375, 25.87850189209, -6493.03125))    
                    elseif _G.SelectTeleport == "Mansion" then
                            local args = {
                                [1] = "requestEntrance",
                                [2] = Vector3.new(-12548.595703125, 337.17001342773, -7554.6103515625)
                            }
                        
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))           
                    elseif _G.SelectTeleport == "Castle on the Sea" then
                            local args = {
                                [1] = "requestEntrance",
                                [2] = Vector3.new(-5079.44677734375, 313.7293395996094, -3151.065185546875)
                            }             
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        elseif _G.SelectTeleport == "Graveyard Island" then
                            two(CFrame.new(-9515.07324, 142.130615, 5537.58398))
                        elseif _G.SelectTeleport == "Icecream Island" then
                            two(CFrame.new(-884.558289, 58.9715157, -10868.5488, -0.900285184, 7.57311795e-08, 0.435300559, 9.98552281e-08, 1, 3.25453406e-08, -0.435300559, 7.27671221e-08, -0.900285184))
                        elseif _G.SelectTeleport == "Peanut Island" then
                            two(CFrame.new(-2124.06738, 44.0723495, -10179.8281, -0.623125494, -2.55908191e-07, -0.782121837, -1.40530574e-07, 1, -2.15235005e-07, 0.782121837, -2.42063933e-08, -0.623125494))      
                        elseif _G.SelectTeleport == "Cake Loaf" then
                            two(CFrame.new(-1977.36767578125, 251.509521484375, -12380.4189453125))
                end
            end
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)     
            end
        end
    })




    if SecondSea then
        Factory:AddToggle({
            Name = "Auto Factory Farm",
            Value = _G.Settings["Auto Factory Farm"],
            Flag = "Auto Factory Farm",
            Callback = function(value)
                _G.Settings["Auto Factory Farm"] = value
                _G.AutoFactory = value
                SaveSettings()
                if value == false then
                    pcall(function()
                        tween:Cancel()
                    end)
                end
            end
        })
        
        
        
        Factory:AddToggle({
            Name = "Auto Factory Farm Hop",
            Value = _G.Settings["Auto Factory Farm Hop"],
            Flag = "Auto Factory Farm Hop",
            Callback = function(value)
                _G.Settings["Auto Factory Farm Hop"] = value
                SaveSettings()
                if value == false then
                    pcall(function()
                        tween:Cancel()
                    end)
                end
            end
        })
    end




    task.spawn(function()
        while wait() do
            if _G.AutoFactory then
                pcall(function()
                    
                
                if  game:GetService("Workspace"):FindFirstChild("Core")  then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if _G.FactoryCore and v.Name == "Core" and v.Humanoid.Health > 0 then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                    end
                                    itemequip(_G.Settings["Select Weapon"])
                                    PosMonMidNight = v.HumanoidRootPart.CFrame
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0)) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.WalkSpeed = 0
                                    v.Head.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                            
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                until not _G.AutoFactory or v.Humanoid.Health <= 0 
                            end
                        end
                elseif not game:GetService("Workspace"):FindFirstChild("Core") and game.ReplicatedStorage:FindFirstChild("Core") then
                    two(CFrame.new(-13.3459644, 149.434006, -226.762894, -0.824662149, 2.60147175e-08, -0.565625608, 3.95481905e-08, 1, -1.1667046e-08, 0.565625608, -3.19908402e-08, -0.824662149))
                
                elseif not game:GetService("Workspace"):FindFirstChild("Core") and not game.ReplicatedStorage:FindFirstChild("Core") then
                wait(2)
                        if  _G.Settings["Auto Factory Farm Hop"] and  _G.Settings["Auto Factory Farm"] then
                            wait(5)
                            Hop()
                            wait(5)            
                        end
                end
            end)
            end
        end
    end)


    if SecondSea then
    Swan:AddToggle({
        Name = "Auto Swan Glasses",
        Value = _G.Settings["Auto Swan Glasses"],
        Flag = "Auto Swan Glasses",
        Callback = function(value)
            _G.Settings["Auto Swan Glasses"] = value
            _G.SwanGalss = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })

    Swan:AddToggle({
        Name = "Auto Swan Glasses Hop",
        Value = _G.Settings["Auto Swan Glasses Hop"],
        Flag = "Auto Swan Glasses",
        Callback = function(value)
            _G.Settings["Auto Swan Glasses Hop"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })
    end


    spawn(function()
        while wait() do
            if _G.SwanGalss then
                pcall(function()
                    if  game:GetService("ReplicatedStorage"):FindFirstChild('Don Swan [Lv. 1000] [Boss]')   and not game:GetService("Workspace").Enemies:FindFirstChild('Don Swan [Lv. 1000] [Boss]') then
                        local args = {
                            [1] = "requestEntrance",
                            [2] = Vector3.new(2284.912109375, 15.537666320800781, 905.48291015625)
                        }

                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    elseif   game:GetService("Workspace").Enemies:FindFirstChild('Don Swan [Lv. 1000] [Boss]') then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == 'Don Swan [Lv. 1000] [Boss]' then
                                    repeat wait()
                                        if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                            game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                        end
                                        itemequip(_G.Settings["Select Weapon"])
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))                
                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)                           
                                    
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.SwanGalss == false
                                end
                            end
                    elseif not game:GetService("ReplicatedStorage"):FindFirstChild('Don Swan [Lv. 1000] [Boss]')   and not  game:GetService("Workspace").Enemies:FindFirstChild('Don Swan [Lv. 1000] [Boss]') then
                        spawn(function()
                            while wait() do
                                if _G.Settings["Auto Swan Glasses Hop"] and _G.Settings["Auto Swan Glasses"] then
                                    wait(5)
                                    Hop()
                                    wait(5)
                                end
                            end
                        end)
                    end 
                end)
            end
        end
    end)





    function ab(str)
        return str:gsub(". You've completely mastered this ability!",' Nao Check')
    end

    function ac(str)
        return str:gsub(". You're gonna have to do better than that!",' Nao Check')
    end

    
    Ken:AddButton({
        Name = "Check Lv Ken",
        Callback = function()
            game:service('VirtualInputManager'):SendKeyEvent(true, "E", false, game)
            wait(3)
            RobloxNotify(game:GetService("Players").LocalPlayer.VisionRadius.Value,3)
        end
    })




    Ken:AddToggle({
        Name = "Auto Farm Ken",
        Value = _G.Settings["Auto Farm Ken"],
        Flag = "Auto Farm Ken",
        Callback = function(value)
            _G.Settings["Auto Farm Ken"]  = value
            _G.FramKen = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })


    Ken:AddToggle({
        Name = "Auto Farm Ken Hop",
        Value = _G.Settings["Auto Farm Ken Hop"],
        Flag = "Auto Farm Ken Hop",
        Callback = function(value)
            _G.Settings["Auto Farm Ken Hop"]  = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })


    spawn(function()
        while wait() do
            if _G.FramKen then
                pcall(function()
                    repeat task.wait()
                        if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                            game:service('VirtualInputManager'):SendKeyEvent(true, "E", false, game)
                        end
                    until game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") or not _G.FramKen
                end)
            end
        end
    end)



    function hopfast()
        pcall(function()
                for count = math.random(1, math.random(40, 75)), 100 do
            local args = {
                        [1] = count
                        }
                TableCahce = {}
            remote = game:GetService("ReplicatedStorage").__ServerBrowser:InvokeServer(unpack(args))
                for _i ,v in pairs(remote) do
                    for _i2 ,v2 in pairs(v) do
                        if tonumber(v['Count']) < 12 then
                            if string.find(v['Region'], 'Sing') then
                                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, _i)
                            end
                        end
                    end    
                end    
            end	
        end) 
    end







    spawn(function()
        while wait() do
            if _G.ThirdSea then
                pcall(function()
                    if SecondSea then          
                        if game:GetService("Players").LocalPlayer.Data.Level.Value >= 1500  then
                            if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ZQuestProgress","Check") == 0 then
                                wait(1.8)
                                if game:GetService("Workspace").Enemies:FindFirstChild("rip_indra [Lv. 1500] [Boss]") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "rip_indra [Lv. 1500] [Boss]" then
                                            repeat wait()
                                                if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                end
                                                itemequip(_G.Settings["Select Weapon"])
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid.WalkSpeed = 0
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
                                                sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                            until _G.ThirdSea == false or v.Humanoid.Health <= 0 or not v.Parent
                                        end
                                    end
                                elseif not game:GetService("Workspace").Enemies:FindFirstChild("rip_indra [Lv. 1500] [Boss]") then
                                    if (CFrame.new(-1926.3221435547, 12.819851875305, 1738.3092041016).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 10 then
                                        wait(1.5)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ZQuestProgress","Begin")
                                    else
                                        two(CFrame.new(-1926.3221435547, 12.819851875305, 1738.3092041016))
                                    end
                                end
                            end
                        end  
                    end
                end)
            end
        end
    end)




    spawn(function()
        while wait() do
            if _G.FramKen then
                pcall(function()
                    if OldWolrd then
                        if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then  
                            if game:GetService("Workspace").Enemies:FindFirstChild('Pirate [Lv. 35]') then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Pirate [Lv. 35]" then
                                    repeat wait()
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                    until not _G.FramKen  or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                end
                            end
                            elseif not game:GetService("Workspace").Enemies:FindFirstChild('Pirate [Lv. 35]') then
                                CFrameMonKen = CFrame.new(-5234.18848, 8.61593533, 8455.24512, 0.693822265, -9.17739271e-08, -0.720146298, 1.16196667e-07, 1, -1.54886486e-08, 0.720146298, -7.29322309e-08, 0.693822265)   
                                two(CFrameMonKen)                 
                            end
                        elseif not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Pirate [Lv. 35]" then
                                        repeat wait()
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                            wait(1)
                                            if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.Settings["Auto Farm Ken Hop"]   == true then
                                                hopfast()
                                            end
                                        until _G.Settings["Auto Farm Ken"]  == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                    end
                                end
                        end
                    elseif SecondSea  then
                        if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then  
                            if game:GetService("Workspace").Enemies:FindFirstChild('Marine Lieutenant [Lv. 875]') then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Marine Lieutenant [Lv. 875]" then
                                    repeat wait()
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                    until not _G.FramKen  or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                end
                            end
                            elseif not game:GetService("Workspace").Enemies:FindFirstChild('Marine Lieutenant [Lv. 875]') then
                                CFrameMonKen = CFrame.new(-2425.8603515625, 91.3018569946289, -3128.84521484375)   
                                two(CFrameMonKen)                 
                            end
                        elseif not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Marine Lieutenant [Lv. 875]" then
                                        repeat wait()
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                            wait(1)
                                            if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.Settings["Auto Farm Ken Hop"]   == true then
                                                hopfast()
                                            end
                                        until _G.Settings["Auto Farm Ken"]  == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                    end
                                end
                        end  
                        elseif ThirdSea then
                            if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then  
                                if game:GetService("Workspace").Enemies:FindFirstChild('Fishman Captain [Lv. 1800]') then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Fishman Captain [Lv. 1800]" then
                                        repeat wait()
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                        until not _G.FramKen  or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                    end
                                end
                                elseif not game:GetService("Workspace").Enemies:FindFirstChild('Fishman Captain [Lv. 1800]') then
                                    CFrameMonKen = CFrame.new(-10988.9199, 331.788422, -8553.98926, -0.714876473, -1.05139231e-08, -0.699250758, -1.61074165e-09, 1, -1.33892479e-08, 0.699250758, -8.44534664e-09, -0.714876473)   
                                    two(CFrameMonKen)                 
                                end
                            elseif not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Fishman Captain [Lv. 1800]" then
                                            repeat wait()
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(4,0,0))
                                                wait(1)
                                                if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.Settings["Auto Farm Ken Hop"]   == true then
                                                    hopfast()
                                                end
                                            until _G.Settings["Auto Farm Ken"]  == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                                        end
                                    end
                            end 
                        end
                end)
            end
        end
    end)

    -- MagnitudeAdd = 0
    -- task.spawn(function()
    -- 	while wait() do 
    -- 		if _G.Settings["Auto Grab Chest"] then
    --             GrabChest = true
    -- 			for i,v in pairs(game:GetService("Workspace"):GetChildren()) do 
    -- 				if v.Name:find("Chest") then
    -- 					if game:GetService("Workspace"):FindFirstChild(v.Name) then
    -- 						if (v.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5000+MagnitudeAdd then
    -- 							repeat wait()
    -- 								if game:GetService("Workspace"):FindFirstChild(v.Name) then
                                        
                                    
    --                                     if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude <= 6 then
    --                                         GrabChest = false 
                                            
    --                                     elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude >= 7 then
    --                                         two(v.CFrame * CFrame.new(1,5,0))
    --                                         GrabChest = true
    --                                     end
    -- 								end
    -- 							until _G.Settings["Auto Grab Chest"] == false or not v.Parent
    -- 							two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
    -- 							MagnitudeAdd = MagnitudeAdd+1500
    -- 							break
    -- 						end
    -- 					end
    -- 				end
    -- 			end
    -- 		end
    -- 	end
    -- end)




    spawn(function()
        while wait() do
            if _G.Settings["Auto Grab Chest"] then
                pcall(function()
                        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                            if v.Name == "Chest1" or v.Name == "Chest2" or v.Name == "Chest3" then
                                repeat wait()
                                    two(v.CFrame * CFrame.new(0,2,0)) 
                                    wait(.1)
                                    game:service('VirtualInputManager'):SendKeyEvent(true, "W", false, game)
                                            wait(.1)
                                    game:service('VirtualInputManager'):SendKeyEvent(false, "W", false, game)
                                until not v.Parent or _G.Settings["Auto Grab Chest"] == false
                                two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                                break
                            end
                        end
                    end)
                end
            end
        end)


    -- spawn(function()
    --     while wait() do
    --         if _G.Settings["Auto Grab Chest"] then
    --             pcall(function()
    --                 for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
    --                     if v.Name == 'Chest1' or v.Name == 'Chest2' or v.Name == 'Chest3' then  
    --                         if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude <= 15000 then
    --                             repeat wait() 
    --                                 two(v.CFrame * CFrame.new(0,2,0)) 
    --                                 game:service('VirtualInputManager'):SendKeyEvent(true, "W", false, game)
    -- 										wait(.1)
    -- 								game:service('VirtualInputManager'):SendKeyEvent(false, "W", false, game)
    --                             until not _G.Settings["Auto Grab Chest"]  or not v.Parent
                            
    --                         end                                 
    --                     end
    --                 end
    --             end)
    --         end
    --     end
    -- end)




    local Color  = Second:CreateSection({
        Name = "// Auto Buy Color Haki //"

    })
    if SecondSea then
        Color:AddToggle({
            Name = "Auto Buy Color Haki",
            Value = _G.Settings["BuyHakiColor"],
            Flag = "BuyHakiColor",
            Callback = function(value)
                _G.Settings["BuyHakiColor"] = value
                _G.BuyHakiColor = value
                SaveSettings()
                if value == false then
        
                end
            end
        })
        
        Color:AddToggle({
            Name = "Auto Buy Color Haki Hop",
            Value = _G.Settings["BuyHakiColor Hop"],
            Flag = "BuyHakiColor",
            Callback = function(value)
                _G.Settings["BuyHakiColor Hop"] = value
                _G.BuyHakiColor = value
                SaveSettings()
                if value == false then
        
                end
            end
        })
    end




    spawn(function()
        while wait() do
        if _G.BuyHakiColor then
            local args = {
                [1] = "ColorsDealer",
                [2] = "2"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end
    end)

    spawn(function()
        while wait() do
            if _G.Settings["BuyHakiColor"] and _G.Settings["BuyHakiColor Hop"] then
                wait(10)
                Hop()
                wait(5)
            end
        end
    end)

    spawn(function()
        while wait() do
            if _G.Settings["Auto Random Fruit"] then
                wait(1) 
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin","Buy")
            end
        end
    end)


    local Raid = VisualTab:CreateSection({
        Name = "// Auto Dungeon  //"

    })



    -- Script generated by SimpleSpy - credits to exx#9394






    Raid:AddDropdown({
        Name = "Select Dungeon",
        Value = _G.Settings["Select Dungeon"], -- ค่าที่จะให้มันเลือก
        List = {"Flame","Ice","Quake","Light","Dark","String","Rumble","Magma","Human: Buddha","Sand","Bird: Phoenix","Dough"},
        Callback = function(value)
            SelectDungeon = value
            _G.Settings["Select Dungeon"] = value
            SaveSettings()
        end
    })

















    Raid:AddToggle({
        Name = "Auto Buy Chip",
        Value = _G.Settings["Auto Buy Chip Dungeon"],
        Flag = "Auto Buy Chip Dungeon",
        Callback = function(value)
            _G.Settings["Auto Buy Chip Dungeon"] = value
            AutoBuyChip = value
            SaveSettings()
        
            

        end
    })
    spawn(function()
        while wait() do
            if _G.Settings["Auto Buy Chip Dungeon"] then
                pcall(function()
                    local args = {
                        [1] = "RaidsNpc",
                        [2] = "Select",
                        [3] = _G.Settings["Select Dungeon"]
                    }
                    
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end)
            end
        end
    end)




    Raid:AddToggle({
        Name = "Auto Start Dungeon",
        Value = _G.Settings["Auto Start Dungeon"],
        Flag = "Auto Farm Dungeon",
        Callback = function(value)
            _G.Settings["Auto Start Dungeon"] = value
            DEugoun = value
            SaveSettings()
        end
    })




    Raid:AddToggle({
        Name = "Auto Farm Dungeon",
        Value = _G.Settings["Auto Farm Dungeon"],
        Flag = "Auto Farm Dungeon .",
        Callback = function(value)
            _G.Settings["Auto Farm Dungeon"] = value
            AutoNext = value
            SaveSettings()
        end
    })


    Raid:AddToggle({
        Name = "Auto Kill Aura",
        Value = _G.Settings["Auto Kill Aura"],
        Flag = "Auto Kill Aura .",
        Callback = function(value)
            _G.Settings["Auto Kill Aura"] = value
            AutoKillAura = value
            SaveSettings()
        end
    })


    Raid:AddToggle({
        Name = "Auto Awakened",
        Value = _G.Settings["Auto Awakened"],
        Flag = "Auto Awakened",
        Callback = function(value)
            _G.Settings["Auto Awakened"] = value
            Awakened = value
            SaveSettings()
        end
    })

    spawn(function()
        while wait() do
            pcall(function()
                if DEugoun then
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                            if SecondSea then
                                fireclickdetector(game.Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                                repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true    
                                
                            elseif ThirdSea then
                                fireclickdetector(game.Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                                repeat wait(2) until  game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true  
                            end
                    end
                    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Timer.Visible == true then

                    end
                end
            end)
        end
    end)

    spawn(function()
        while wait() do
            if AutoKillAura then
                for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        pcall(function()
                            repeat wait()
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                v.Humanoid.Health = 0
                                v.HumanoidRootPart.CanCollide = false
                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                v.HumanoidRootPart.Transparency = 0.5
                            until not AutoKillAura or not v.Parent or v.Humanoid.Health <= 0
                        end)
                    end
                end
            end
        end
    end)

    spawn(function()
        while wait() do
            if Awakened then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener","Awaken")
            end
        end
    end)






    spawn(function()
        while wait() do
                if _G.Settings["Auto Farm Dungeon"] then
                    if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true then
                        if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").Position).Magnitude <= 4000 then
                                two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").CFrame*CFrame.new(5,70,0))
                            end                      
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").Position).Magnitude <= 4000 then
                                two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame*CFrame.new(5,70,0))
                            end
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").Position).Magnitude <= 4000 then
                                two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame*CFrame.new(5,70,0))
                            end
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").Position).Magnitude <= 4000 then
                                two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame*CFrame.new(5,70,0))
                            end
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").Position).Magnitude <= 4000 then
                                two(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame*CFrame.new(5,70,0))
                            end
                        end
                    end
                end
        end
    end)

    task.spawn(function()
        while wait() do
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
                if v:IsA("Tool") then
                    if v:FindFirstChild("RemoteFunctionShoot") then 
                        SelectWeaponGun = v.Name
                    end
                end
            end
        end
    end)

    spawn(function()
        local gt = getrawmetatable(game)
        local old = gt.__namecall
        setreadonly(gt,false)
        gt.__namecall = newcclosure(function(...)
            local args = {...}
            if getnamecallmethod() == "InvokeServer" then 
                if SelectWeaponGun then
                    if SelectWeaponGun == "Soul Guitar" then
                        if tostring(args[2]) == "TAP" then
                            if _G.Auto_Mastery_Gun and UseSkillMasteryGun then
                                args[3] = PositionSkillMasteryGun
                            end
                        end
                    end
                end
            end
            return old(unpack(args))
        end)
        setreadonly(gt,true)
    end)


    local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)
    spawn(function()
        while wait() do
            if _G.Auto_Mastery_Gun    then
                pcall(function()         
                    CheckQuest()
                        if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                            StartMagnet = false
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                        end
                        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                            StartMagnet = false
                            CheckQuest()                
                            repeat wait()                         
                                if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1700 then
                                    two(CFrameQ) 
                                elseif  (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1700 then
                                    tp(CFrameQ) 
                                end
                            until (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings["Auto Farm Level"]


                            if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                if game.Players.LocalPlayer.Character.Humanoid.Health > 0 and (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                    wait(0.4)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
                                end
                            
                        end
                                            
                        
                        elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            CheckQuest()
                            if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        if v.Name == Ms then
                                            repeat wait(_G.Fast_Delay)
                                                
                                                if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameQ) then
                                                    HealthMin = v.Humanoid.MaxHealth * MinHealth/100
                                                
                                                if v.Humanoid.Health <= HealthMin then
                                                    _G.Settings["Super Fast Attack"] = false
                                                    PositionSkillMasteryGun = v.HumanoidRootPart.Position
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                                    itemequip(SelectWeaponGun)
                                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild(SelectWeaponGun) and game:GetService("Players").LocalPlayer.Character:FindFirstChild(SelectWeaponGun):FindFirstChild("RemoteFunctionShoot") then
                                                        click()
                                                        local args = {
                                                            [1] = v.HumanoidRootPart.Position,
                                                            [2] = v.HumanoidRootPart
                                                        }
                                                        game:GetService("Players").LocalPlayer.Character[SelectWeaponGun].RemoteFunctionShoot:InvokeServer(unpack(args))
                                                    end 
                                                else    
                                                    _G.Settings["Super Fast Attack"] = false
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                                    end
                                                    itemequip(_G.Settings["Select Weapon"]) 
                                                    StartMagnet = true                                  
                                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    v.HumanoidRootPart.CanCaillde = false 
                                                    click() 
                                                end
                                                else
                                                    StartMagnet = false
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                            end
                                            until not _G.Auto_Mastery_Gun   or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            
                                        end
                                    end
                                end
                            else
                                StartMagnet = false
                                if game:GetService("ReplicatedStorage"):FindFirstChild(Ms) then
                                    two(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame)
                                else	
                                    if AttackRandomType == 1 then
                                        two(CFramePuk * CFrame.new(0, 20, 100))
                                    elseif AttackRandomType == 2 then
                                        two(CFramePuk * CFrame.new(-100, 20, 0))
                                    elseif AttackRandomType == 3 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    elseif AttackRandomType == 4 then
                                        two(CFramePuk * CFrame.new(100, 20, 0))
                                    elseif AttackRandomType == 5 then
                                        two(CFramePuk * CFrame.new(0, 20, -100))
                                    end
                                end
                            end
                        end
                    end)
                end    
            end
        end)


        function Eh(str)
            return str:gsub(" Fruit", "")
        end
    

        local EliteHunter = Second:CreateSection({
            Name = ' // Auto Farm Elite Hunter //',
        })

        local Elite = EliteHunter:AddLabel({
            Name = ''
        })
        
        spawn(function()
            while wait() do
                pcall(function()
                    Elite:Set('Elite Hunter : ' ..tostring(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter","Progress")))
                end)
            end
        end)

        EliteHunter:AddToggle({
            Name = "Auto Farm Elite Hunter",
            Value = _G.Settings["Auto Farm Elite"],
            Flag = "Auto Farm Elite . ",
            Callback = function(value)
                _G.Settings["Auto Farm Elite"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })


        EliteHunter:AddToggle({
            Name = "Auto Farm Elite Hunter Hop",
            Value = _G.Settings["Auto Farm Elite Hunter Hop"],
            Flag = "Auto Farm Elite Hop ..",
            Callback = function(value)
                _G.Settings["Auto Farm Elite Hunter Hop"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        EliteHunter:AddToggle({
            Name = "Stop at God's Chalice",
            Value = _G.Settings["Stop at God's Chalice"],
            Flag = "Stop at God's Chalice ..",
            Callback = function(value)
                _G.Settings["Stop at God's Chalice"]  = value
                _G.Stop = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        spawn(function()
            while wait() do
                if _G.Settings["Auto Farm Elite"] then
                    pcall(function()
                        if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter"),"I don't have anything for you right now. Come back later.") then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("God's Chalice") or game.Players.LocalPlayer.Character:FindFirstChild("God's Chalice") then
                                if _G.Settings["Auto Farm Elite Hunter Hop"] and _G.Stop then
                                elseif  _G.Settings["Auto Farm Elite Hunter Hop"] and not _G.Stop then 
                                    Hop()
                                end
                            elseif not game.Players.LocalPlayer.Backpack:FindFirstChild("God's Chalice") and not game.Players.LocalPlayer.Character:FindFirstChild("God's Chalice") then
                                if _G.Settings["Auto Farm Elite Hunter Hop"] then
                                    Hop()
                                end
                            end
                            

                        else
                            if game:GetService("ReplicatedStorage"):FindFirstChild("Diablo [Lv. 1750]") and not  game:GetService("Workspace").Enemies:FindFirstChild("Diablo [Lv. 1750]")  then
                            two(game:GetService("ReplicatedStorage"):FindFirstChild("Diablo [Lv. 1750]").HumanoidRootPart.CFrame) 
                            elseif   game:GetService("Workspace").Enemies:FindFirstChild("Diablo [Lv. 1750]") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == 'Diablo [Lv. 1750]' then
                                        repeat wait()
                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                            end
                                            MagnetElite = true
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            ElitePos = v.HumanoidRootPart.CFrame
                                            if AttackRandomType == 1 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                            elseif AttackRandomType == 2 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                            elseif AttackRandomType == 3 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                            elseif AttackRandomType == 4 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                            elseif AttackRandomType == 5 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                            end
                                            v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(14)
                                            v.Humanoid.Sit = true
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                        until not _G.Settings["Auto Farm Elite"] or not v.Parent or v.Humanoid <= 0
                                        MagnetElite = false
                                    end
                                end
                            end
                            if game:GetService("ReplicatedStorage"):FindFirstChild("Urban [Lv. 1750]") and not  game:GetService("Workspace").Enemies:FindFirstChild("Urban [Lv. 1750]")  then
                                two(game:GetService("ReplicatedStorage"):FindFirstChild("Urban [Lv. 1750]").HumanoidRootPart.CFrame)
                            elseif  game:GetService("Workspace").Enemies:FindFirstChild("Urban [Lv. 1750]")  then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == 'Urban [Lv. 1750]' then
                                        repeat wait()
                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                            end
                                            MagnetElite = true
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            ElitePos = v.HumanoidRootPart.CFrame
                                            if AttackRandomType == 1 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                            elseif AttackRandomType == 2 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                            elseif AttackRandomType == 3 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                            elseif AttackRandomType == 4 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                            elseif AttackRandomType == 5 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                            end
                                            v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(14)
                                            v.Humanoid.Sit = true
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                        until not _G.Settings["Auto Farm Elite"] or not v.Parent or v.Humanoid <= 0
                                        MagnetElite = false
                                    end
                                end
                            end
                            if game:GetService("ReplicatedStorage"):FindFirstChild("Deandre [Lv. 1750]") and not  game:GetService("Workspace").Enemies:FindFirstChild("Deandre [Lv. 1750]")  then
                                two(game:GetService("ReplicatedStorage"):FindFirstChild("Deandre [Lv. 1750]").HumanoidRootPart.CFrame)
                            elseif  game:GetService("Workspace").Enemies:FindFirstChild("Deandre [Lv. 1750]")  then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == 'Deandre [Lv. 1750]' then
                                        repeat wait()
                                            MagnetElite = true
                                            if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
                                                game.ReplicatedStorage.Remotes.CommF_:InvokeServer('Buso')
                                            end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            ElitePos = v.HumanoidRootPart.CFrame
                                            if AttackRandomType == 1 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 1))
                                            elseif AttackRandomType == 2 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(0, 1, 10))
                                            elseif AttackRandomType == 3 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(1, 1, -10))
                                            elseif AttackRandomType == 4 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(10, 1, 0))
                                            elseif AttackRandomType == 5 then
                                                two(v.HumanoidRootPart.CFrame * CFrame.new(-10, 1, 0))
                                            end
                                            v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(14)
                                            v.Humanoid.Sit = true
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                        until not _G.Settings["Auto Farm Elite"] or not v.Parent or v.Humanoid <= 0
                                        MagnetElite = false
                                    end
                                end
                            end
                        end
                    end)
                end
            end
        end)

        spawn(function()
            game:GetService("RunService").Heartbeat:Connect(function()
                pcall(function()
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if _G.Settings["Auto Farm Elite"]  and MagnetElite and (v.Name == "Diablo [Lv. 1750]" or v.Name == "Urban [Lv. 1750]" or v.Name == 'Deandre [Lv. 1750]') and (v.HumanoidRootPart.Position - ElitePos.Position).Magnitude <= 350 then
                            v.HumanoidRootPart.CFrame = ElitePos
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
                end)
            end)
        end)




        task.spawn(function()
            while wait() do
                pcall(function()
                    if _G.Settings["Auto Dark Dagger"] then
                        if game:GetService("Workspace").Enemies:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == ("rip_indra True Form [Lv. 5000] [Raid Boss]" or v.Name == "rip_indra True Form [Lv. 5000] [Raid Boss]") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                    repeat wait()                               
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                    until not _G.Settings["Auto Dark Dagger"] or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        else
                        CFrameDrak = CFrame.new(-5429.71729, 313.941254, -2709.80664, -0.973512471, 0, -0.228633925, 0, 1, 0, 0.228633925, 0, -0.973512471) 
                        if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameDrak.Position).Magnitude <= 400 then
                                if not  game:GetService("Workspace").Enemies:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") then
                                    if _G.Settings["Auto Dark Dagger Hop"] then
                                        Hop()
                                    end
                                end
                            else
                                two(CFrameDrak)
                        end
                        end
                    end
                end)
            end
        end)


        local DarkDagger = Second:CreateSection({
            Name = ' // Auto Dark Dagger //',
            Side = "Right"
        })

        local Dark = DarkDagger:AddLabel({
            Name = ''
        })
        
        spawn(function()
            while wait() do
                pcall(function()
                    if game.ReplicatedStorage:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") then
                        Dark:Set('Booss : 🟢 ' )
                    elseif not game.ReplicatedStorage:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") then
                        Dark:Set('Booss : 🔴 ' )
                    end
                    
                end)
            end
        end)

        DarkDagger:AddToggle({
            Name = "Auto Dark Dagger",
            Value = _G.Settings["Auto Dark Dagger"],
            Flag = "Auto Farm Elite",
            Callback = function(value)
                _G.Settings["Auto Dark Dagger"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })
        DarkDagger:AddToggle({
            Name = "Auto Dark Dagger",
            Value = _G.Settings["Auto Dark Dagger Hop"],
            Flag = "Auto Farm Elite",
            Callback = function(value)
                _G.Settings["Auto Dark Dagger Hop"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })







        local TwinHooks = Second:CreateSection({
            Name = ' // Auto Twin Hooks //',
        })

        local Twin = TwinHooks:AddLabel({
            Name = ''
        })
        
        spawn(function()
            while wait() do
                pcall(function()
                    if  game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                        Twin:Set('Booss : 🟢 ' )
                    elseif not game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                        Twin:Set('Booss : 🔴 ' )
                    end
                    
                end)
            end
        end)

        TwinHooks:AddToggle({
            Name = "Auto Twin Hooks",
            Value = _G.Settings["Auto Twin Hooks"],
            Flag = "Auto Twin Hooks",
            Callback = function(value)
                _G.Settings["Auto Twin Hooks"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })


        TwinHooks:AddToggle({
            Name = "Auto Twin Hooks Hop",
            Value = _G.Settings["Auto Twin Hooks Hop"],
            Flag = "Auto Twin Hooks Hop .",
            Callback = function(value)
                _G.Settings["Auto Twin Hooks Hop"]  = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })







        spawn(function()
            while wait() do
                if _G.Settings["Auto Twin Hooks"] then
                    pcall(function()
                        if game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                        two(game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]").HumanoidRootPart.CFrame)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Captain Elephant [Lv. 1875] [Boss]" then
                                        repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings["Auto Twin Hooks"] == false
                                    end
                                end
                        elseif not game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                        if _G.Settings["Auto Twin Hooks Hop"] then
                                Hop()
                        end
                        end
                    end)
                end
            end
        end)



        local Can = Second:CreateSection({
            Name = ' // Auto Canvander //',
            Side = "Right"
        })

        local Canvan = Can:AddLabel({
            Name = ''
        })
        
        spawn(function()
            while wait() do
                pcall(function()
                    if  game.ReplicatedStorage:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                        Canvan:Set('Booss : 🟢 ' )
                    elseif not game.ReplicatedStorage:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                        Canvan:Set('Booss : 🔴 ' )
                    end
        
                end)
            end
        end)

        Can:AddToggle({
            Name = "Auto Canvander",
            Value = _G.Settings["Auto Canvander"],
            Flag = "Farm Canvander",
            Callback = function(value)
                _G.Settings["Auto Canvander"]  = value

                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        Can:AddToggle({
            Name = "Auto Canvander Hop",
            Value = _G.Settings["Auto Canvander Hop"],
            Flag = "Farm Canvander H",
            Callback = function(value)
                _G.Settings["Auto Canvander Hop"]  = value

                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        spawn(function()
            while wait() do
                if _G.Settings["Auto Canvander"] then
                    pcall(function()
                        if  game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Beautiful Pirate [Lv. 1950] [Boss]" then
                                        repeat wait(_G.Fast_Delay)
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings["Auto Canvander"] == false
                                    end
                                end
                        elseif game.ReplicatedStorage:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") and  not game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656))
                        elseif not game.ReplicatedStorage:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") and  not game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                            if _G.Settings["Auto Canvander Hop"] then
                                Hop()
                            end
                        end
                    end)
                end
            end
        end)



    -- Posessed Mummy [Lv. 2050]
    --Living Zombie [Lv. 2000]

    spawn(function()
        while wait() do
            if BoneFarm then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild('Posessed Mummy [Lv. 2050]') and not game:GetService("Workspace").Enemies:FindFirstChild('Living Zombie [Lv. 2000]')  then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Posessed Mummy [Lv. 2050]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.JumpPower = 0
                                    BoneMagnet = true
                                    BonePos = v.HumanoidRootPart.CFrame
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                until not v.Parent or v.Humanoid.Health <= 0 or BoneFarm == false 
                            end
                        end
                    elseif not game:GetService("Workspace").Enemies:FindFirstChild('Posessed Mummy [Lv. 2050]') and  game:GetService("Workspace").Enemies:FindFirstChild('Living Zombie [Lv. 2000]') then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Living Zombie [Lv. 2000]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.JumpPower = 0
                                    BoneMagnet = true
                                    BonePos = v.HumanoidRootPart.CFrame
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                until not v.Parent or v.Humanoid.Health <= 0 or BoneFarm == false 
                            end
                        end
                    elseif  game:GetService("Workspace").Enemies:FindFirstChild('Posessed Mummy [Lv. 2050]') and  game:GetService("Workspace").Enemies:FindFirstChild('Living Zombie [Lv. 2000]') then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Posessed Mummy [Lv. 2050]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.JumpPower = 0
                                    BoneMagnet = true
                                    BonePos = v.HumanoidRootPart.CFrame
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                until not v.Parent or v.Humanoid.Health <= 0 or BoneFarm == false 
                            end
                        end
                    elseif not  game:GetService("Workspace").Enemies:FindFirstChild('Posessed Mummy [Lv. 2050]') and not game:GetService("Workspace").Enemies:FindFirstChild('Living Zombie [Lv. 2000]') then
                        CFramePukBone = CFrame.new(-9466.72949, 171.162918, 6132.01514)
                        if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFramePukBone.Position).Magnitude > 3000 then
                            tp(CFramePukBone)  
                        elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFramePukBone.Position).Magnitude <= 2999 then
                            two(CFramePukBone)  
                        end
                    end
                end)
            end
        end
    end)





    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            pcall(function()
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if BoneFarm and BoneMagnet and (v.Name == 'Posessed Mummy [Lv. 2050]' or v.Name == 'Living Zombie [Lv. 2000]') and (v.HumanoidRootPart.Position - BonePos.Position).magnitude <= 350 then
                        v.HumanoidRootPart.CFrame = BonePos
                        v.HumanoidRootPart.CanCollide = false
                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                        if v.Humanoid:FindFirstChild("Animator") then
                            v.Humanoid.Animator:Destroy()
                        end
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                    end
                end
            end)
        end)
    end)




    spawn(function()
        while wait() do
            if RandomBone then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
            end
        end
    end)


    spawn(function()
        while wait() do
            if _G.Auto_Yama then
                pcall(function()
                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter","Progress") >= 30 then
                        fireclickdetector(game:GetService("Workspace").Map.Waterfall.SealedKatana.Handle.ClickDetector)
                    end
                end)
            end
        end
    end)


    local Halllow = Second:CreateSection({
        Name = ' // Auto Hallow Scythe //'
    })

    local Hl = Halllow:AddLabel({
        Name = ''
    })

    spawn(function()
        while wait() do
            pcall(function()
                if  game.ReplicatedStorage:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") then
                    Hl:Set('Booss : 🟢 ' )
                elseif not game.ReplicatedStorage:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") then 
                    Hl:Set('Booss : 🔴 ' )
                end
    
            end)
        end
    end)

    Halllow:AddToggle({
        Name = "Auto Hallow Scythe",
        Value = _G.Settings["Auto Hallow Scythe"],
        Flag = "Auto Hallow Scythe . ",
        Callback = function(value)
            _G.Settings["Auto Hallow Scythe"]  = value

            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })


    Halllow:AddToggle({
        Name = "Auto Hallow Scythe Hop",
        Value = _G.Settings["Auto Hallow Scythe Hop"],
        Flag = "Auto Hallow Scythe hop.",
        Callback = function(value)
            _G.Settings["Auto Hallow Scythe Hop"]  = value

            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })

        local Srepent = Second:CreateSection({
            Name = ' // Auto Serpent Bow //',
            Side = "Right"
        })
        local Srepentcheck = Srepent:AddLabel({
            Name = ''
        })
        
        spawn(function()
            while wait() do
                pcall(function()
                    if game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]") or  game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                        Srepentcheck:Set('Booss : 🟢 ' )
                    elseif not game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]") and  not game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                        Srepentcheck:Set('Booss : 🔴 ' )
                    end
                end)
            end
        end)

        Srepent:AddToggle({
            Name = "Auto Serpent Bow",
            Value = _G.Settings["Auto Serpent Bow"],
            Flag = "Auto Serpent Bow.",
            Callback = function(value)
                _G.Settings["Auto Serpent Bow"]  = value
                _G.SrepentBow = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })

        Srepent:AddToggle({
            Name = "Auto Serpent Bow Hop",
            Value = _G.Settings["Auto Serpent Bow Hop"],
            Flag = "Auto Serpent Bow Hop.",
            Callback = function(value)
                _G.Settings["Auto Serpent Bow Hop"]  = value
                _G.SrepentBowHop = value
                SaveSettings()
                if value == false then
                pcall(function()
                    tween:Cancel()
                end)
                end
            end
        })


    spawn(function()
        while wait() do
            if _G.Settings["Auto Hallow Scythe"] then
                pcall(function()
                    if game.ReplicatedStorage:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") then
                        two(game.ReplicatedStorage:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]").HumanoidRootPart.CFrame)
                    elseif game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Soul Reaper [Lv. 2100] [Raid Boss]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings["Auto Hallow Scythe"] == false 
                            end
                        end
                    elseif not game.ReplicatedStorage:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper [Lv. 2100] [Raid Boss]") then
                        if _G.Settings["Auto Hallow Scythe Hop"] then
                        elseif not _G.Settings["Auto Hallow Scythe Hop"] then
                            repeat wait()
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
                            until _G.Settings["Auto Hallow Scythe"] == false or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hallow Essence')
                            if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hallow Essence') or game.Players.LocalPlayer.Character:FindFirstChild('Hallow Essence') then
                                itemequip('Hallow Essence')
                                two(CFrame.new(-8932.61426, 143.722458, 6059.33936, -0.999979794, -0, -0.00636155345, -0, 1, -0, 0.00636155345, 0, -0.999979794))

                            end
                        end
                    end
                end)
            end
        end
    end)








    spawn(function()
        while  wait() do
            if _G.RainbowHaki then
                pcall(function()
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("HornedMan","Bet")
                    elseif  string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Stone") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                        if game.ReplicatedStorage:FindFirstChild("Stone [Lv. 1550] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Stone [Lv. 1550] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Stone [Lv. 1550] [Boss]").HumanoidRootPart.CFrame)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Stone [Lv. 1550] [Boss]") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Stone [Lv. 1550] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.RainbowHaki == false 
                                end
                            end
                        end
                    elseif  string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Island Empress") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                        if game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]").HumanoidRootPart.CFrame)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Island Empress [Lv. 1675] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.RainbowHaki == false 
                                end
                            end
                        end
                    elseif  string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Kilo Admiral") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                        if game.ReplicatedStorage:FindFirstChild("Kilo Admiral [Lv. 1750] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Kilo Admiral [Lv. 1750] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Kilo Admiral [Lv. 1750] [Boss]").HumanoidRootPart.CFrame)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Kilo Admiral [Lv. 1750] [Boss]") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Kilo Admiral [Lv. 1750] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.RainbowHaki == false 
                                end
                            end
                        end
                    elseif  string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Captain Elephant") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                        if game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]").HumanoidRootPart.CFrame)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Captain Elephant [Lv. 1875] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.RainbowHaki == false 
                                end
                            end
                        end
                    elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Beautiful Pirate") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                        if game.ReplicatedStorage:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656))
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Beautiful Pirate [Lv. 1950] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.RainbowHaki == false 
                                end
                            end
                        end
                    end
                end)
            end
        end
    end)


    --[[

    local args = {
        [1] = "BuyBoat",
        [2] = "Dinghy"
    }


    ]]--


    local MoonStats = StatusFm:AddLabel({
        Name = ''
    })

    local MythicStats = StatusFm:AddLabel({
        Name = ''
    })

    Moon:AddToggle({
        Name = "Auto Full Moon",
        Value = _G.Settings["Auto Full Moon"],
        Flag = "Auto Full Moon.",
        Callback = function(value)
            _G.Settings["Auto Full Moon"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })

    Moon:AddToggle({
        Name = "Auto Full Moon Hop",
        Value = _G.Settings["Auto Full Moon Hop"],
        Flag = "Auto Full Moon Hop.",
        Callback = function(value)
            _G.Settings["Auto Full Moon Hop"] = value
            SaveSettings()
            if value == false then
                pcall(function()
                end)
            end
        end
    })


    spawn(function()
        while wait() do
            if _G.Settings["Auto Full Moon"] then
                pcall(function()
                    if game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709149431" then
                    else
                        if  _G.Settings["Auto Full Moon Hop"] then
                            Hop()
                        end  
                    end
                end)
            end
        end
    end)






    MythicIsland:AddToggle({
        Name = "Auto Mythic Island",
        Value = _G.Settings["Auto Mythic Island"],
        Flag = "Auto Mythic Island.",
        Callback = function(value)
            _G.Settings["Auto Mythic Island"] = value
            _G.MythicIsland = value
            SaveSettings()
            if value == false then
                pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })


    MythicIsland:AddToggle({
        Name = "Auto Mythic Island Hop",
        Value = _G.Settings["Auto Mythic Island Hop"],
        Flag = "Auto Mythic Island Hop.",
        Callback = function(value)
            _G.Settings["Auto Mythic Island Hop"] = value
            _G.MythicIslandHop = value
            SaveSettings()
            if value == false then
            end
        end
    })




    MythicIsland:AddToggle({
        Name = "Auto Find Advanced Fruit Dealer",
        Value = _G.Settings["Auto Find Advanced Fruit Dealer"],
        Flag = "Auto Find Advanced Fruit Dealer.",
        Callback = function(value)
            _G.FindSellFruits = value
            SaveSettings()
            if value == false then
            end
        end
    })

    MythicIsland:AddToggle({
        Name = "Auto Drive Boat",
        Value = _G.Settings["Auto Drive Boat"],
        Flag = "Auto Drive Boat.",
        Callback = function(value)
            _G.Settings["Auto Drive Boat"] = value
            SaveSettings()
            if value == false then
            end
        end
    })


    Boat = {"Enforcer","Swan","RocketBoost","Dinghy","PirateSloop","PirateBasic","PirateBrigade"}

    MythicIsland:AddDropdown({
        Name = "Select Boat",
        Value = _G.Settings["Select Boat"], 
        List = Boat,
        Callback = function(value)
            SelectBoat = value
            _G.Settings["Select Boat"] = value
            SaveSettings()
        end
    })

    MythicIsland:AddButton({
        Name = "Teleport to Boat Dealer",
        Callback = function()
            CFrameBoat = CFrame.new(-6039.87842, 16.4207401, -2041.06348, -0.392088264, 5.34213314e-08, 0.919927597, 5.53166508e-08, 1, -3.44943665e-08, -0.919927597, 3.73624758e-08, -0.392088264)
            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameBoat.Position).Magnitude >= 80 then
                Noclipboat = false
            else
                
                    Noclipboat = true
                    two(CFrameBoat)
                end          
        end
    })


    MythicIsland:AddButton({
        Name = "Buy Boat",
        Callback = function()
            CFrameBoat = CFrame.new(-6039.87842, 16.4207401, -2041.06348, -0.392088264, 5.34213314e-08, 0.919927597, 5.53166508e-08, 1, -3.44943665e-08, -0.919927597, 3.73624758e-08, -0.392088264)
            if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameBoat.Position).Magnitude <= 80 then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat",_G.Settings["Select Boat"])
                    for i ,v in pairs(game:GetService("Workspace").Boats:GetChildren()) do
                        if game:GetService("Workspace").Boats:FindFirstChild(_G.Settings["Select Boat"]) and  (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.VehicleSeat.Position).Magnitude <= 300 then
                            repeat wait()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.VehicleSeat.CFrame * CFrame.new(0,1,0)
                                wait(.5)
                                game:service('VirtualInputManager'):SendKeyEvent(true, "W", false, game)
                                wait(.1)
                                game:service('VirtualInputManager'):SendKeyEvent(false, "W", false, game)
                            until game.Players.LocalPlayer.Character.Humanoid.Sit  == true
                        end
                    end
                end
            end
    })






    spawn(function()
        while wait() do
            pcall(function()
            wait(.2)
                if game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709149431" then
                    MoonStats:Set('🌕  : Full Moon' )
                else
                    MoonStats:Set('🌑 : Not Full Moon' )    
                end
            end)
        end
    end)


    spawn(function()
        while wait() do
            pcall(function()
            wait(.2)
            if game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                MythicStats:Set('🟢 : Have Mystic Island')
                elseif  not game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then 
                    MythicStats:Set('🔴 : Not Have Mystic Island')
            end
            end)
        end
    end)

    spawn(function()
        while wait() do
            if _G.Settings["Auto Drive Boat"] then
                pcall(function()
                    if game.Players.LocalPlayer.Character.Humanoid.Sit  == true then
                        repeat wait()
                            game:service('VirtualInputManager'):SendKeyEvent(true, "W", false, game)
                            wait(.1)
                            game:service('VirtualInputManager'):SendKeyEvent(false, "W", false, game)
                        until game.Players.LocalPlayer.Character.Humanoid.Sit  == false or game:GetService("Workspace").Map:FindFirstChild("MysticIsland") or not _G.Settings["Auto Drive Boat"]
                    end  
                end)  
            end
        end
    end)


    spawn(function()
        while wait() do
            if _G.MythicIsland then
                pcall(function()
                    if game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                                two(game:GetService("Workspace").Map.MysticIsland.Part.CFrame)
                    elseif  not game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                        if  _G.MythicIslandHop then
                            Hop()
                        end
                    end
                end)
            end
        end
    end)



    spawn(function()
        while wait() do
            pcall(function()
                if _G.DragonTalon then
                    if string.find(game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true),"Set")  then
                        if   game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or  game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                            end
                            if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                            end

                            if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                                if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) 
                                elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                                else
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) 
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon") 
                                end 
                            end

                            if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                _G.Settings["Select Weapon"] = "Dragon Claw"
                                if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) 
                                elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                                else
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) 
                                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                                end 
                            end
                        else
                            local args = {
                                [1] = "BlackbeardReward",
                                [2] = "DragonClaw",
                                [3] = "2"
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        end
                    elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1  then
                            game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                    end
                    
                end
            end)
        end
    end)

    spawn(function()
        while wait() do
            if _G.FindSellFruits then
                    pcall(function()
                    if game:GetService("Workspace").NPCs:FindFirstChild("Advanced Fruit Dealer") then
                        two(game:GetService("Workspace").NPCs["Advanced Fruit Dealer"].HumanoidRootPart.CFrame)
                    end
                end)
            end
        end
    end)

    spawn(function()
        while wait() do
            pcall(function()
                if _G.Settings["Auto Electric Claw"] then
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value < 400 then
                            _G.Settings["Select Weapon"] = "Electro"
                        else
                            local args = {
                                [1] = "BuyElectro"
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        end  
                        if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value < 400 then
                            _G.Settings["Select Weapon"] = "Electro"
                        else
                            local args = {
                                [1] = "BuyElectro"
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        end  
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400 then
                            if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true) == 4 then
                                if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", "Start") == nil then
                                    game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12548, 337, -7481)
                                end
                            else
                                game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("BuyElectricClaw");
                            end
                        end
                        if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400 then
                            if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true) == 4 then
                                if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", "Start") == nil then
                                    game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12548, 337, -7481)
                                end
                            else
                                game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("BuyElectricClaw");
                            end
                        end
                    end

            end)
        end
    end)



    local CakePrince = Second:CreateSection({
        Name = ' // Auto Cake Prince //',
    })

    CakePrince:AddToggle({
        Name = "Auto Cake Prince",
        Value = _G.Settings["Auto Cake Prince"],
        Flag = "Auto Cake Prince.",
        Callback = function(value)
            _G.Settings["Auto Cake Prince"]  = value
            _G.CakePrince = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })

    CakePrince:AddToggle({
        Name = "Auto Cake Prince Hop",
        Value = _G.Settings["Auto Cake Prince Hop"],
        Flag = "Auto Cake Prince Hop.",
        Callback = function(value)
            _G.Settings["Auto Cake Prince Hop"]  = value
            _G.CakePrinceHop = value
            SaveSettings()
            if value == false then
            pcall(function()
                end)
            end
        end
    })

    spawn(function()
        while wait() do
            pcall(function()
                if _G.CakePrince then
                    game.ReplicatedStorage.Remotes.CommF_:InvokeServer("CakePrinceSpawner")
                    if game.ReplicatedStorage:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") then
                            for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                                if v.Name == "Cake Prince [Lv. 2300] [Raid Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.CakePrince == false 
                                end
                            end
                        end
                    else
                        if not _G.CakePrinceHop then
                            if game:GetService("Workspace").Enemies:FindFirstChild('Cookie Crafter [Lv. 2200]') and not game:GetService("Workspace").Enemies:FindFirstChild('Cake Guard [Lv. 2225]')  then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Cookie Crafter [Lv. 2200]" then
                                        repeat wait(_G.Fast_Delay)
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.JumpPower = 0
                                            CakeMagnet = true
                                            Cakepos = v.HumanoidRootPart.CFrame
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.CakePrince == false 
                                    end
                                end
                            elseif not game:GetService("Workspace").Enemies:FindFirstChild('Cookie Crafter [Lv. 2200]') and  game:GetService("Workspace").Enemies:FindFirstChild('Cake Guard [Lv. 2225]') then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Cake Guard [Lv. 2225]" then
                                        repeat wait(_G.Fast_Delay)
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.JumpPower = 0
                                            CakeMagnet = true
                                            Cakepos = v.HumanoidRootPart.CFrame
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.CakePrince == false 
                                    end
                                end
                            elseif  game:GetService("Workspace").Enemies:FindFirstChild('Cookie Crafter [Lv. 2200]') and  game:GetService("Workspace").Enemies:FindFirstChild('Cake Guard [Lv. 2225]') then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Cookie Crafter [Lv. 2200]" then
                                        repeat wait(_G.Fast_Delay)
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            itemequip(_G.Settings["Select Weapon"]) 
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.JumpPower = 0
                                            CakeMagnet = true
                                            Cakepos = v.HumanoidRootPart.CFrame
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                            two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.CakePrince == false 
                                    end
                                end
                            elseif not  game:GetService("Workspace").Enemies:FindFirstChild('Cookie Crafter [Lv. 2200]') and not game:GetService("Workspace").Enemies:FindFirstChild('Cake Guard [Lv. 2225]') then
                                PriceCFram = CFrame.new(-2139.27173, 70.0088272, -12241.6953, -0.940431178, -3.89163013e-08, -0.339984119, -2.99336023e-08, 1, -3.16656212e-08, 0.339984119, -1.96023873e-08, -0.940431178)
                                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - PriceCFram.Position).Magnitude > 3000 then
                                    tp(PriceCFram)  
                                elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - PriceCFram.Position).Magnitude <= 2999 then
                                    two(PriceCFram)  
                                end
                            end
                    elseif _G.CakePrinceHop then
                            Hop()
                        end                
                    end
                end
            end)
        end
    end)


    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            pcall(function()
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if _G.CakePrince and CakeMagnet and (v.Name == 'Cookie Crafter [Lv. 2200]' or v.Name == 'Cake Guard [Lv. 2225]') and (v.HumanoidRootPart.Position - Cakepos.Position).magnitude <= 350 then
                        v.HumanoidRootPart.CFrame = Cakepos
                        v.HumanoidRootPart.CanCollide = false
                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                        if v.Humanoid:FindFirstChild("Animator") then
                            v.Humanoid.Animator:Destroy()
                        end
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                    end
                end
            end)
        end)
    end)

    -- task.spawn(function()
    --     while wait() do
    --         if _G.CakePrince then
    --             game.ReplicatedStorage.Remotes.CommF_:InvokeServer("CakePrinceSpawner")
    --             if game.ReplicatedStorage:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") then
    --                 if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince [Lv. 2300] [Raid Boss]") then
    --                     for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
    --                         if _G.CakePrince and v.Name == "Cake Prince [Lv. 2300] [Raid Boss]" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
    --                             repeat wait()
    --                                 if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
    --                                     Farmtween = toTarget(v.HumanoidRootPart.CFrame)
    --                                 elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
    --                                     if Farmtween then
    --                                         Farmtween:Stop()
    --                                     end
    --                                     FastAttack = true
    --                                     if _G.Settings.Configs["Auto Haki"] then
    --                                         if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
    --                                             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
    --                                         end
    --                                     end
    --                                     if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
    --                                         wait()
    --                                         EquipWeapon(_G.Settings.Configs["Select Weapon"])
    --                                     end
    --                                     PosMon = v.HumanoidRootPart.CFrame
    --                                     if not _G.Settings.Configs["Fast Attack"] then
    --                                         game:GetService'VirtualUser':CaptureController()
    --                                         game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
    --                                     end
    --                                     v.HumanoidRootPart.Size = Vector3.new(60,60,60)
    --                                     if _G.Settings.Configs["Show Hitbox"] then
    --                                         v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
    --                                     else
    --                                         v.HumanoidRootPart.Transparency = 1
    --                                     end
    --                                     v.Humanoid.JumpPower = 0
    --                                     v.Humanoid.WalkSpeed = 0
    --                                     v.HumanoidRootPart.CanCollide = false
    --                                     v.Humanoid:ChangeState(11)
    --                                     toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0,_G.Settings.Configs["Distance Auto Farm"],0))
    --                                 end
    --                             until not _G.CakePrince or not v.Parent or v.Humanoid.Health <= 0
    --                             FastAttack = false
    --                         end
    --                     end
    --                 else
    --                     if game:GetService("Workspace").Map.CakeLoaf.BigMirror.Other.Transparency == 0 and (CFrame.new(-1990.672607421875, 4532.99951171875, -14973.6748046875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude >= 2000 then
    --                         FastAttack = false
    --                         Questtween = toTarget(CFrame.new(-2151.82153, 149.315704, -12404.9053))
    --                         if (CFrame.new(-2151.82153, 149.315704, -12404.9053).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
    --                             if Questtween then Questtween:Stop() end
    --                             game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2151.82153, 149.315704, -12404.9053)
    --                             wait(.1)
    --                         end
    --                     end 
    --                 end
    --             else
    --                 if game:GetService("Workspace").Enemies:FindFirstChild("Cookie Crafter [Lv. 2200]") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Guard [Lv. 2225]") or game:GetService("Workspace").Enemies:FindFirstChild("Baking Staff [Lv. 2250]") or game:GetService("Workspace").Enemies:FindFirstChild("Head Baker [Lv. 2275]") then
    --                     for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
    --                         if (v.Name == "Cookie Crafter [Lv. 2200]" or v.Name == "Cake Guard [Lv. 2225]" or v.Name == "Baking Staff [Lv. 2250]" or v.Name == "Head Baker [Lv. 2275]") and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
    --                             repeat wait()
    --                                 if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
    --                                     Farmtween = toTarget(v.HumanoidRootPart.CFrame)
    --                                 elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
    --                                     if Farmtween then
    --                                         Farmtween:Stop()
    --                                     end
    --                                     FastAttack = true
    --                                     StartMagnet = true
    --                                     if _G.Settings.Configs["Auto Haki"] then
    --                                         if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
    --                                             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
    --                                         end
    --                                     end
    --                                     if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
    --                                         wait()
    --                                         EquipWeapon(_G.Settings.Configs["Select Weapon"])
    --                                     end
    --                                     PosMon = v.HumanoidRootPart.CFrame
    --                                     if not _G.Settings.Configs["Fast Attack"] then
    --                                         game:GetService'VirtualUser':CaptureController()
    --                                         game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
    --                                     end
    --                                     v.HumanoidRootPart.Size = Vector3.new(60,60,60)
    --                                     if _G.Settings.Configs["Show Hitbox"] then
    --                                         v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
    --                                     else
    --                                         v.HumanoidRootPart.Transparency = 1
    --                                     end
    --                                     v.Humanoid.JumpPower = 0
    --                                     v.Humanoid.WalkSpeed = 0
    --                                     v.HumanoidRootPart.CanCollide = false
    --                                     v.Humanoid:ChangeState(11)
    --                                     toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0,_G.Settings.Configs["Distance Auto Farm"],0))
    --                                 end
    --                             until not _G.CakePrince or not v.Parent or v.Humanoid.Health <= 0
    --                             StartMagnet = false
    --                             FastAttack = false
    --                         end
    --                     end
    --                 else
    --                     Questtween = toTarget(CFrame.new(-2077, 252, -12373))
    --                     if (CFrame.new(-2077, 252, -12373).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
    --                         if Questtween then Questtween:Stop() end
    --                         game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2077, 252, -12373)
    --                     end
    --                 end
    --             end
    --         else
    --             toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
    --             break
    --         end
    --     end
    -- end)


    task.spawn(function()
        while wait() do
            if _G.SrepentBow then
                pcall(function()
                    if game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                        two(game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]").HumanoidRootPart.CFrame)
                    elseif  game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Island Empress [Lv. 1675] [Boss]" then
                                repeat wait(_G.Fast_Delay)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                    end
                                    itemequip(_G.Settings["Select Weapon"]) 
                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(14)
                                    two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                    v.HumanoidRootPart.CanCollide = false
                                    v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                until not v.Parent or v.Humanoid.Health <= 0 or _G.SrepentBow == false 
                            end
                        end
                    elseif not game.ReplicatedStorage:FindFirstChild("Island Empress [Lv. 1675] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Island Empress [Lv. 1675] [Boss]") then
                        if _G.SrepentBowHop then
                            Hop()
                        end
                    end
                end)
            end
        end
    end)

    local Tushita = Second:CreateSection({
        Name = ' // Auto Tushita //',
        Side = "Right",
    })

    Tushita:AddToggle({
        Name = "Auto Tushita",
        Value = _G.Settings["Auto Tushita"],
        Flag = "Auto Tushita.",
        Callback = function(value)
            _G.Settings["Auto Tushita"]  = value
            _G.Tushita = value
            SaveSettings()
            if value == false then
            pcall(function()
                tween:Cancel()
            end)
            end
        end
    })


    Tushita:AddToggle({
        Name = "Auto Tushita Hop",
        Value = _G.Settings["Auto Tushita Hop"],
        Flag = "Auto Tushita Hop.",
        Callback = function(value)
            _G.Settings["Auto Tushita Hop"]  = value
            _G.Tushitahop = value
            SaveSettings()
            if value == false then
            pcall(function()
                end)
            end
        end
    })

    local Buddy = Second:CreateSection({
        Name = ' // Auto Buddy Swords //',
    })

    spawn(function()
        while wait() do
            if _G.Tushita then
                pcall(function()
                    local Q_Tushita = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TushitaProgress")
                    if game.Workspace.Enemies:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") or game.ReplicatedStorage:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") then
                            repeat wait(1)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TushitaProgress")
                            until game.Players.LocalPlayer.Backpack:FindFirstChild("Holy Torch") or game.Players.LocalPlayer.Character:FindFirstChild("Holy Torch") or not _G.Tushita
                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TushitaProgress")['Torches'] == false then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("Holy Torch") or game.Players.LocalPlayer.Character:FindFirstChild("Holy Torch") then
                                repeat wait()
                                    two(CFrame.new(-10752, 417, -9366))
                                    itemequip(("Holy Torch"))
                                until not _G.Tushita or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-10752, 417, -9366)).Magnitude <= 10
                                wait(1)
                                repeat wait()
                                    two(CFrame.new(-11672, 334, -9474))
                                    itemequip(("Holy Torch"))
                                until not _G.Tushita or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-11672, 334, -9474)).Magnitude <= 10
                                wait(1)
                                repeat  wait()
                                    two(CFrame.new(-12132, 521, -10655))
                                    itemequip(("Holy Torch"))
                                until not _G.Tushita or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-12132, 521, -10655)).Magnitude <= 10
                                wait(1)
                                repeat wait()
                                    two(CFrame.new(-13336, 486, -6985))
                                    itemequip(("Holy Torch"))
                                until not _G.Tushita or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-13336, 486, -6985)).Magnitude <= 10
                                wait(1)
                                repeat wait()
                                    two(CFrame.new(-13489, 332, -7925))
                                    itemequip(("Holy Torch"))
                                    wait()
                                until not _G.Tushita or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-13489, 332, -7925)).Magnitude <= 10
                            else
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TushitaProgress")
                            end
                        end
                    elseif not game.Workspace.Enemies:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]") and not game.ReplicatedStorage:FindFirstChild("rip_indra True Form [Lv. 5000] [Raid Boss]")  then
                            if _G.Tushitahop then
                                Hop()
                            end
                    elseif Q_Tushita['KilledLongma'] == false then
                        if not game.Workspace.Enemies:FindFirstChild("Longma [Lv. 2000] [Boss]") and  game.ReplicatedStorage:FindFirstChild("Longma [Lv. 2000] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Longma [Lv. 2000] [Boss]").HumanoidRootPart.CFrame)
                        elseif game.Workspace.Enemies:FindFirstChild("Longma [Lv. 2000] [Boss]") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Longma [Lv. 2000] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.Tushita == false 
                                end
                            end
                        end        
                    end
                end)
            end
        end
    end)


    local Shop = PepsisWorld:CreateTab({
        Name = "Shop"
    })

    local FightingStyleShopSection = Shop:CreateSection({
        Name = "// Fighting Style //"

    })

    FightingStyleShopSection:AddButton({
        Name = "Black Leg",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Electro",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Fishman Karate",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "DragonClaw",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","1")
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "SuperHuman",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Death Step",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Sharkman Karate",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true)
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Electric Claw",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "Dragon Talon",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon")
        end
    })

    FightingStyleShopSection:AddButton({
        Name = "God Human",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman")
        end
    })





    local SwordShopSection = Shop:CreateSection({
        Name = "// Sword //",
        Side = "Right"
    })

    SwordShopSection:AddButton({
        Name = "Cutlass",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cutlass")
        end
    })

    SwordShopSection:AddButton({
        Name = "Katana",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Katana")
        end
    })

    SwordShopSection:AddButton({
        Name = "Iron Mace",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Iron Mace")
        end
    })

    SwordShopSection:AddButton({
        Name = "Duel Katana",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Duel Katana")
        end
    })

    SwordShopSection:AddButton({
        Name = "Duel Katana",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Duel Katana")
        end
    })

    SwordShopSection:AddButton({
        Name = "Triple Katana",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Triple Katana")
        end
    })

    SwordShopSection:AddButton({
        Name = "Pipe",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Pipe")
        end
    })

    SwordShopSection:AddButton({
        Name = "Dual-Headed Blade",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Dual-Headed Blade")
        end
    })

    SwordShopSection:AddButton({
        Name = "Bisento",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Bisento")
        end
    })

    SwordShopSection:AddButton({
        Name = "Soul Cane",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Soul Cane")
        end
    })



    local GunShopSection = Shop:CreateSection({
        Name = "// Gun //"
    })

    GunShopSection:AddButton({
        Name = "Slingshot",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Slingshot")
        end
    })

    GunShopSection:AddButton({
        Name = "Musket",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Musket")
        end
    })

    GunShopSection:AddButton({
        Name = "Flintlock",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Flintlock")
        end
    })

    GunShopSection:AddButton({
        Name = "Refined Flintlock",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Refined Flintlock")
        end
    })

    GunShopSection:AddButton({
        Name = "Cannon",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cannon")
        end
    })

    GunShopSection:AddButton({
        Name = "Kabucha",
        Callback = function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Slingshot","1")
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Slingshot","2")
        end
    })

    local RacefragmentSection = Shop:CreateSection({
        Name = "// Fragment //",
        Side = "Right"
    })

    RacefragmentSection:AddButton({
        Name = "Buy Random Race",
        Callback = function()
            local args = {
                [1] = "BlackbeardReward",
                [2] = "Reroll",
                [3] = "2"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    })

    RacefragmentSection:AddButton({
        Name = "Buy Reset Stats",
        Callback = function()
            local args = {
                [1] = "BlackbeardReward",
                [2] = "Refund",
                [3] = "2"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    })

    local Fake = VisualTab:CreateSection({
        Name = "// Fake Stast  //",
    })

    Fake:AddToggle({
        Name = "Enabled Stats",
        Value = false,
        Flag = "Fake Stast.",
        Callback = function(value)
            _G.Fake = value
            SaveSettings()
            if value == false then

            end
        end
    })


    settingLv = "Level"
    Fake:Textbox ({
            Name = "Input Level",
            Flag = "Fake Level.",
            Value = settingLv,
            Callback = function(value)
                settingLv = value
                if _G.Fake then
                    game:GetService("Players").LocalPlayer.Data.Level.Value = tonumber(value)
                end
                return tostring(value)
            end
    })


    settingFragments = "Fragments"
    Fake:Textbox ({
            Name = "Input Fragments",
            Flag = "Fake Fragments.",
            Value = settingFragments,
            Callback = function(value)
                settingLv = value
                if _G.Fake then
                    game:GetService("Players").LocalPlayer.Data.Fragments.Value = tonumber(value)
                end
                return tostring(value)
            end
    })
    settingBeli = "Beli"
    Fake:Textbox ({
            Name = "Input Beli",
            Flag = "Fake Beli.",
            Value = settingBeli,
            Callback = function(value)
                settingBeli = value
                if _G.Fake then
                    game:GetService("Players").LocalPlayer.Data.Beli.Value = tonumber(value)
                end
                return tostring(value)
            end
    })

    settingExp = "Exp"
    Fake:Textbox ({
            Name = "Input Exp",
            Flag = "Fake Exp.",
            Value = settingBeli,
            Callback = function(value)
                settingExp = value
                if _G.Fake then
                    game:GetService("Players").LocalPlayer.Data.Exp.Value = tonumber(value)
                end
                return tostring(value)
            end
    })

    local Gh = VisualTab:CreateSection({
        Name = "// Graphic  //",
        Side = "Right"
    })


    Gh:AddSlider({
        Name = "Fps",
        Flag = "Fps.",
        Value = _G.Settings["Fps"],
        Min = 1,
        Max = 360,
        Textbox = true,
        Format = function(value)
            _G.Settings["Fps"] = value
            return "Fps : ".. tostring(value)
        end
    })



    Gh:AddToggle({
        Name = "Auto Look Fps",
        Value = _G.Settings["Auto Look Fps"],
        Flag = "Auto Look Fps.",
        Callback = function(value)
            _G.Settings["Auto Look Fps"] = value
            SaveSettings()
            if _G.Settings["Fps"] then
                setfpscap(tonumber(_G.Settings["Fps"]))
            end
        end
    })

    Gh:AddToggle({
        Name = "Auto White Screen",
        Value = _G.Settings["Auto White Screen"],
        Flag = "Auto White Screen.",
        Callback = function(value)
            WhiteScreen = value
            SaveSettings()
            if WhiteScreen then
                game:GetService("RunService"):Set3dRenderingEnabled(false)
            else
                game:GetService("RunService"):Set3dRenderingEnabled(true)
            end
        end
    })


    Gh:AddButton({
        Name = "Boost FPS",
        Callback = function()
            FPSBooster()
        end
    })

    function FPSBooster()
        local decalsyeeted = true
        local g = game
        local w = g.Workspace
        local l = g.Lighting
        local t = w.Terrain
        sethiddenproperty(l,"Technology",2)
        sethiddenproperty(t,"Decoration",false)
        t.WaterWaveSize = 0
        t.WaterWaveSpeed = 0
        t.WaterReflectance = 0
        t.WaterTransparency = 0
        l.GlobalShadows = false
        l.FogEnd = 9e9
        l.Brightness = 0
        settings().Rendering.QualityLevel = "Level01"
        for i, v in pairs(g:GetDescendants()) do
            if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then
                v.Material = "Plastic"
                v.Reflectance = 0
            elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
                v.Transparency = 1
            elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
                v.Lifetime = NumberRange.new(0)
            elseif v:IsA("Explosion") then
                v.BlastPressure = 1
                v.BlastRadius = 1
            elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
                v.Enabled = false
            elseif v:IsA("MeshPart") then
                v.Material = "Plastic"
                v.Reflectance = 0
                v.TextureID = 10385902758728957
            end
        end
        for i, e in pairs(l:GetChildren()) do
            if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
                e.Enabled = false
            end
        end
    end
    local Noti = VisualTab:CreateSection({
        Name = "// Notifly  //",
        Side = "Right"
    })







    swordlist = {}
    for i , v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer('getInventory')) do
        if type(v) == "table" then
        if v.Type == "Sword" then
                table.insert(swordlist,v.Name)
        end
        end
    end

    local AllSword = ""
    for i , v in pairs(swordlist) do
        AllSword = AllSword .. v .. ","
    end


    gunlist = {}
    for i , v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer('getInventory')) do
        if type(v) == "table" then
            if v.Type == "Gun" then
                table.insert(gunlist,v.Name)
            end
        end
    end
    
    local AllGun = ""
        for i , v in pairs(gunlist) do
            AllGun = AllGun .. v .. ","
        end


        AllMelee = ""

        BuyDragonTalon = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon",true))
        if BuyDragonTalon then
            if BuyDragonTalon == 1 then
                AllMelee = AllMelee .. "Dragon Talon , "
            end
        end
        BuySuperhuman = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman",true))
        if BuySuperhuman then
            if BuySuperhuman == 1 then
                AllMelee = AllMelee .. "Superhuman , "
            end
        end
        BuySharkmanKarate = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true))
        if BuySharkmanKarate then
            if BuySharkmanKarate == 1 then
                AllMelee = AllMelee .. "SharkmanKarate , "
            end
        end
        BuyDeathStep = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep",true))
        if BuyDeathStep then
            if BuyDeathStep == 1 then
                AllMelee = AllMelee .. "Death Step , "
            end
        end
        BuyElectricClaw = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw",true))
        if BuyElectricClaw then
            if BuyElectricClaw == 1 then
                AllMelee = AllMelee .. "Electric Claw , "
            end
        end
        BuyGod = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman",true))
        if BuyGod then
            if BuyGod == 1 then
                AllMelee = AllMelee .. "Godhuman , "
            end
        end



    function SendWeb()
            

    local  data = {
        ["embeds"] = {
            {
                ["title"] = "[👑]  UserName :".. " "..tostring(game.Players.LocalPlayer.Name),
                ["author"] = {
                    ["name"] = "Nao Hub | Webhook (Check)",
                    
                },
                ["color"] = 1279470,
                ["description"] = "[💻]Level : ".. tostring(game:GetService("Players").LocalPlayer.Data.Level.Value) .. "\n [💸]Beli : ".. tostring(game:GetService("Players").LocalPlayer.Data.Beli.Value) .. "\n [💷]Fragments :" .. tostring(game:GetService("Players").LocalPlayer.Data.Fragments.Value) .. "\n [🍎]DevilFruit : " .. tostring(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value) .."\n\n\ninventory\n  ```\n".. "[⚔]".. " Sword\n" ..tostring(AllSword).."\n🔫 Gun \n"..tostring(AllGun).."\n👊 FightingStyle \n"..AllMelee.."\n```",
                ["image"] = {
                    ["url"] = "https://staticg.sportskeeda.com/editor/2022/11/a402f-16694231050443-1920.jpg"
                },
            }
        }
    }





    local newdata = game:GetService("HttpService"):JSONEncode(data)

    local headers = {
    ["content-type"] = "application/json"

    }
    if syn then
        Nao_requests = syn.request
    elseif KRNL_LOADED then
        Nao_requests = request
    else
        Nao_requests = fluxus.request
    end
    local abcdef = {Url =  _G.Link, Body = newdata, Method = "POST", Headers = headers}
    Nao_requests(abcdef)
    end




    _G.Link = "URL"
    Noti:Textbox ({
            Name = "URL",
            Flag = "URL.",
            Value = _G.Link,
            Callback = function(value)
                _G.Link = value
                return tostring(_G.Link)
            end
    })

    Noti:AddButton({
        Name = "Send Webhook",
        Callback = function()
            SendWeb()
        end
    })


    local Bd = Buddy:AddLabel({
        Name = ''
    })


    Buddy:AddToggle({
        Name = "Auto Buddy Swords",
        Value = _G.Settings["Auto Buddy Swords"],
        Flag = "Auto Buddy Swords.",
        Callback = function(value)
            _G.Settings["Auto Buddy Swords"]  = value
            SaveSettings()
            if value == false then
            pcall(function()
                    tween:Cancel()
                end)
            end
        end
    })

    Buddy:AddToggle({
        Name = "Auto Buddy Swords Hop",
        Value = _G.Settings["Auto Buddy Swords Hop"],
        Flag = "Auto Buddy Swords.",
        Callback = function(value)
            _G.Settings["Auto Buddy Swords Hop"]  = value
            SaveSettings()
            if value == false then
            pcall(function()
                end)
            end
        end
    })



    spawn(function()
        while wait() do
            pcall(function()
                if  game.ReplicatedStorage:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
                    Bd:Set('Booss : 🟢 ' )
                elseif not game.ReplicatedStorage:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") and not game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then 
                    Bd:Set('Booss : 🔴 ' )
                end
    
            end)
        end
    end)

    spawn(function()
        while wait() do
            if _G.Settings["Auto Buddy Swords"] then
                pcall(function()
                    if  game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Cake Queen [Lv. 2175] [Boss]" then
                                    repeat wait(_G.Fast_Delay)
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        itemequip(_G.Settings["Select Weapon"]) 
                                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(14)
                                        two(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        if v.Humanoid:FindFirstChild("Animator") then
                                            v.Humanoid.Animator:Destroy()
                                        end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings["Auto Buddy Swords"] == false
                                end
                            end
                    elseif game.ReplicatedStorage:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") and  not game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
                            two(game.ReplicatedStorage:FindFirstChild("Cake Queen [Lv. 2175] [Boss]").HumanoidRootPart.CFrame)
                    elseif not game.ReplicatedStorage:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") and  not game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
                        if _G.Settings["Auto Buddy Swords Hop"] then
                            Hop()
                        end
                    end
                end)
            end
        end
    end)

    -- {End} --
    return library, library_flags, library.subs
elseif DVE then
   


    if not game:IsLoaded() then
        game.Loaded:Wait()
    end
    repeat
        wait()
    until game.Players
    repeat
        wait()
    until game.Players.LocalPlayer
    repeat
        wait()
    until game.ReplicatedStorage
    repeat
        wait()
    until game.ReplicatedStorage:FindFirstChild("Remotes");
    repeat
        wait()
    until game.Players.LocalPlayer:FindFirstChild("PlayerGui");

   

    repeat wait()
        if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("Loading") then
            for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui:GetChildren()) do
                if v.Name == "Loading" then
                    if v:FindFirstChild("Menu").Main.Play then
                        for s,d in pairs(getconnections(v:FindFirstChild("Menu").Main.Play.Activated)) do
                                d.Function()  
                                if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("Loading") and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") and game:GetService("Players").LocalPlayer.PlayerGui.MainHUD.SideHUD.Buttons.Column1.Teleport.Visible == true and game:GetService("Players").LocalPlayer.PlayerGui.Loading.Menu.Visible == true then                                   
                                    wait(.3)
                                    game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("Loading"):Destroy()
                                    
                                end
                            end
                        end
                end
            end
    end
    
    until not game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("Loading")
    

    wait(3)




    _G.Settings = {
        ["AutoFarm"] = false,
        ["Select Car"] = "",
        ["Cash Select"] = "Cash Select",
        ["webhooks"] = "WebHook Here",
        ['Loock Cash'] = false
    }
    
    function LoadSettings()
        if readfile and writefile and isfile and isfolder then
            if not isfolder("Nao Hub Premium Scripts") then
                makefolder("Nao Hub Premium Scripts")
            end
            if not isfolder("Nao Hub Premium Scripts/Driving Empire/") then
                makefolder("Nao Hub Premium Scripts/Driving Empire/")
            end
            if not isfile("Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json") then
                writefile("Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json",
                    game:GetService("HttpService"):JSONEncode(_G.Settings))
            else
                local Decode = game:GetService("HttpService"):JSONDecode(readfile(
                    "Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json"))
                for i, v in pairs(Decode) do
                    _G.Settings[i] = v
                end
            end
        else
            return warn("Status : Undetected Executor")
        end
    end
    
    function SaveSettings()
        if readfile and writefile and isfile and isfolder then
            if not isfile("Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json") then
                LoadSettings()
            else
                local Decode = game:GetService("HttpService"):JSONDecode(readfile(
                    "Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json"))
                local Array = {}
                for i, v in pairs(_G.Settings) do
                    Array[i] = v
                end
                writefile("Nao Hub Premium Scripts/Driving Empire/" .. game.Players.LocalPlayer.Name .. ".json",
                    game:GetService("HttpService"):JSONEncode(Array))
            end
        else
            return warn("Status : Undetected Executor")
        end
    end
    
    LoadSettings()
    
    
    local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Zoydyc/HI1/main/README.md"))()
    local Wait = library.subs.Wait
    
    wait()
    local  PepsisWorld = library:CreateWindow({
        Name = 'Nao Hub Premium Scripts',
        Theme = {
            Image = "rbxassetid://7483871523",
            Info = "Info",
            Background = {
                Asset = "rbxassetid://5553946656"
            }
        }
    })
    
    local GeneralTab = PepsisWorld:CreateTab({
        Name = "Main"
    })
    
    local MiscSection = GeneralTab:CreateSection({
        Name = "Main",
        Side = "Left"
    })
    
    local MiscSection2 = GeneralTab:CreateSection({
        Name = "Main",
        Side = "Right"
    })
    
    MiscSection:AddLabel({
        Name = 'Enjoy Script :)'
    
    })
    
    MiscSection:AddLabel({
        Name = 'Date | ' .. os.date("%A %B %Y")
    
    })
    
    local LabelByNino = MiscSection:AddLabel({
        Name = 'hi'
    })
    
    spawn(function()
        while wait() do
            pcall(function()
                A = os.date('%X')
                LabelByNino:Set('Time | ' .. A)
                wait(1)
            end)
        end
    end)
    
    MiscSection:AddToggle({
        Name = "AutoFarm",
        Value = _G.Settings["AutoFarm"],
        Callback = function(value)
            _G.Autofarm = value
            _G.Settings["AutoFarm"] = value
            SaveSettings()
        end
    })
    
    carlist = {}
    
    for i,v in pairs(game:GetService("Players")[game.Players.LocalPlayer.Name].PlayerGui.MainHUD.Vehicles.Container.List:GetChildren()) do
        if v.Name == "UIGridLayout" then
             
          elseif v.Name == "Template" then
          else
                table.insert(carlist,v.Name)
           end
      end
    
    MiscSection2:AddDropdown({
        Name = "Select Car",
        List = carlist,
        Value = _G.Settings["Select Car"],
        Callback = function(value)
            _G.Settings["Select Car"] =value
            _G.SelectCar = value
            SaveSettings()
        end
    })
    
    
    MiscSection2:AddButton({
        Name = "Clear List",
        Callback = function()
            table.clear(carlist)
            for i,v in pairs(game:GetService("Players")[game.Players.LocalPlayer.Name].PlayerGui.MainHUD.Vehicles.Container.List:GetChildren()) do
                if v.Name == "UIGridLayout" then
                     
                  elseif v.Name == "Template" then
                  else
                        table.insert(carlist,v.Name)
                   end
              end
        end
    })

    MiscSection2:Textbox ({
        Name = "Enter Your Cash Select",
        Flag = "EnterCash",
        Value =  _G.Settings["Cash Select"],
        Callback = function(value)
            _G.Settings["Cash Select"] = value
            _G.cashlock = value
            SaveSettings()
            return "EnterCash"
        end
    })

    MiscSection2:Textbox ({
        Name = "Enter Your WebHook",
        Flag = "EnterWebHook",
        Value = _G.Settings["webhooks"],
        Callback = function(value)
            _G.Settings["webhooks"] = value
            _G.webhooks = value
            SaveSettings()
            return "EnterWebHook"
        end
    })
    
    MiscSection2:AddButton({
        Name = "Send Webhook",
        Callback = function()
            Web()
        end
    })

    MiscSection2:AddToggle({
        Name = "Auto Lock Cash",
        Value = _G.Settings['Loock Cash'],
        Callback = function(value)
            _G.Settings['Loock Cash'] = value
            _G.Autolockcash = value
            SaveSettings()
        end
    })
    

 


    
    
    spawn(function()
        while wait() do
            if _G.Autolockcash then
                pcall(function()
                    if game:GetService("Players").LocalPlayer.leaderstats.Cash.Value >= tonumber(_G.cashlock) then
                        game.Players.localPlayer:Kick('Cash is Max')

                    end

                end)
            end
        end
    end)
    






    spawn(function()
        while wait() do
            if _G.Autofarm then
                pcall(function()
                    local farm = CFrame.new(-32021.1367, 35.0249443, -27819.5938, -0.895553231, -0.00541085703, -0.444921434, -0.00320587913, 0.999978542, -0.00570821203, 0.444942802, -0.0036856432, -0.895551383)
                    if (farm.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1 then
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-32021.1367, 35.0249443, -27819.5938, -0.895553231, -0.00541085703, -0.444921434, -0.00320587913, 0.999978542, -0.00570821203, 0.444942802, -0.0036856432, -0.895551383)
                    end
    
                    if game.Players.LocalPlayer.Character.Humanoid.Sit == false then
                           repeat wait()
                            game:GetService("ReplicatedStorage").Remotes.VehicleEvent:FireServer("Spawn",_G.SelectCar)
                           until game.Players.LocalPlayer.Character.Humanoid.Sit == true
                    end
                    
    
                    if (farm.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1 and game:GetService("Workspace").Vehicles:FindFirstChild(game.Players.LocalPlayer.Name) then
                        repeat wait(math.random(5, 15))
                            local carr = game:GetService("Workspace").Vehicles[game.Players.LocalPlayer.Name]
                            carr:SetPrimaryPartCFrame(CFrame.new(-32021.1367, 35.0249443, -27819.5938, -0.895553231, -0.00541085703, -0.444921434, -0.00320587913, 0.999978542, -0.00570821203, 0.444942802, -0.0036856432, -0.895551383))
                        until not _G.Autofarm
                    end
    
                end)
            end
        end
    end)
    

    spawn(function()
        while wait() do
            if   _G.Autofarm and game.Players.LocalPlayer.Character.Humanoid.Sit == false then
                game:GetService("VirtualInputManager"):SendKeyEvent(false,"W",false,game.Players.LocalPlayer.Character.HumanoidRootPart) 
                repeat wait()
                    game:GetService("ReplicatedStorage").Remotes.VehicleEvent:FireServer("Spawn",_G.SelectCar)
                until game.Players.LocalPlayer.Character.Humanoid.Sit == true
            end
        end
    end)


    spawn(function()
        while wait() do
            if   _G.Autofarm and game.Players.LocalPlayer.Character.Humanoid.Sit == true then
                repeat wait()
                game:GetService("VirtualInputManager"):SendKeyEvent(true,"W",false,game.Players.LocalPlayer.Character.HumanoidRootPart) 
                until not _G.Autofarm
            elseif _G.Autofarm == false then
                game:GetService("VirtualInputManager"):SendKeyEvent(false,"W",false,game.Players.LocalPlayer.Character.HumanoidRootPart) 
            elseif  _G.Autofarm and game.Players.LocalPlayer.Character.Humanoid.Sit == false then
                repeat wait()
                    game:GetService("ReplicatedStorage").Remotes.VehicleEvent:FireServer("Spawn",_G.SelectCar)
                   until game.Players.LocalPlayer.Character.Humanoid.Sit == true
            end  
        end
    end)
    
    function Web()
            

        local  data = {
            ["embeds"] = {
                {
                    ["title"] = "[👑]  UserName :".. " "..tostring(game.Players.LocalPlayer.Name),
                    ["author"] = {
                        ["name"] = "Nao Hub | Webhook (Check)",
                        
                    },
                    ["color"] = 1279470,
                    ["description"] = "[💸]Cash : " ..tostring(game:GetService("Players").LocalPlayer.leaderstats.Cash.Value) .. "\n [💻] Miles :" ..tostring(game:GetService("Players").LocalPlayer.leaderstats.Miles.Value) .. "\n[👽] Bounty :".. tostring(game:GetService("Players").LocalPlayer.leaderstats.Bounty.Value),
                    ["image"] = {
                        ["url"] = "https://media.pocketgamer.com/artwork/ra-91313-1659160460/driving-empire_png_820.jpg"
                    },
                }
            }
        }
    
    
    
    
    
        local newdata = game:GetService("HttpService"):JSONEncode(data)
    
        local headers = {
        ["content-type"] = "application/json"
    
        }
        if syn then
            Nao_requests = syn.request
        elseif KRNL_LOADED then
            Nao_requests = request
        else
            Nao_requests = fluxus.request
        end
        local abcdef = {Url =  _G.webhooks, Body = newdata, Method = "POST", Headers = headers}
        Nao_requests(abcdef)
    end


    -- {End} --
    return library, library_flags, library.subs

else
    game.Players.localPlayer:Kick('Not Find Game')
end
