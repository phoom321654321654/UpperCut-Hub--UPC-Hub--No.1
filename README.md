





if game.PlaceId == 2753915549 then
        W = true
    elseif game.PlaceId == 4442272183 then
        W2 = true
    elseif game.PlaceId == 7449423635 then
        W3 = true
    end




game.StarterGui:SetCore("SendNotification", {
      Icon = "rbxassetid://11915607895"; -- ใส่หน้าพ่อมึงมึง
      Title = "Upper Cut Hub", 
      Text = "Check Key Success",
  })



function gotopos(cfr)
    local Distance2 = (cfr.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = cfr})
     tween:Play()
end

function tween_cancel()
    local Distance2 = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame})
     tween:Play()
end









_G.Team = "Pirate"


if game:GetService("Players").LocalPlayer.PlayerGui.Main:FindFirstChild("ChooseTeam") then
	repeat wait()
		if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
			if _G.Team == "Pirate" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			elseif _G.Team == "Marine" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
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
_G.Color = Color3.fromRGB(0, 150, 255) -- Color Gui (1)
_G.Color2 = Color3.fromRGB(0, 150, 255) -- Color Gui (2)
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
library:CreateWatermark("Start Script Hub") -- Config แตกนะเดียวค่อยแก้รอเน็ตมาก่อน By MeowX#0001
local CenterHubNo1 = library:CreateWindow("UPPERCUT HUB PREMIUM SCRIPTS | [🔥RACE V4] Blox Fruits",Enum.KeyCode.RightControl)
local Tab = CenterHubNo1:CreateTab("MAIN")
local Sector1 = Tab:CreateSector("General","left")
Sector1:AddLabel("---------AutoFarm----------")
Sector1:AddToggle("AutoFarm Lv.",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)
Sector1:AddToggle("AutoFarm Lv.",false,function(t)
   print("นี่คือฟามเลเวลเเบบลัดฟามเเละฆ่าคน")
end)
Sector1:AddToggle("Fast Attack",true,function(value)

_G.UpperCutFastAttack = value

local Module = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
local CombatFramework = debug.getupvalues(Module)[2]
local CameraShakerR = require(game.ReplicatedStorage.Util.CameraShaker)
spawn(function()
while true do
	if _G.UpperCutFastAttack then
		pcall(function()
			CameraShakerR:Stop()
			CombatFramework.activeController.attacking = false
			CombatFramework.activeController.timeToNextAttack = 0 --0
			CombatFramework.activeController.increment = 0  --3
			CombatFramework.activeController.hitboxMagnitude = 150
			CombatFramework.activeController.blocking = false
			CombatFramework.activeController.timeToNextBlock = 0 --0
			CombatFramework.activeController.focusStart = 0
			CombatFramework.activeController.humanoid.AutoRotate = true
		end)
	end
	task.wait()
end
end)

spawn(function()
  while wait() do
  if _G.UpperCutFastAttack then
	for i, v in pairs(game.Workspace["_WorldOrigin"]:GetChildren()) do
		if v.Name == "CurvedRing" or v.Name == "SlashHit" or v.Name == "DamageCounter" or v.Name == "SwordSlash" or v.Name == "SlashTail" or v.Name == "Sounds" then
			v:Destroy() 
		end
	end
end
end
end) 
getgenv().A = require(game:GetService("ReplicatedStorage").CombatFramework.RigLib).wrapAttackAnimationAsync
getgenv().B = require(game.Players.LocalPlayer.PlayerScripts.CombatFramework.Particle).play
spawn(function()
while wait() do
  if _G.UpperCutFastAttack then
		pcall(function()
			require(game:GetService("ReplicatedStorage").CombatFramework.RigLib).wrapAttackAnimationAsync =function(a1,a2,a3,a4,a5)
				local GetBladeHits = require(game:GetService("ReplicatedStorage").CombatFramework.RigLib).getBladeHits(a2,a3,a4)
				if GetBladeHits then
					 require(game:GetService("ReplicatedStorage").CombatFramework.RigLib).play = function() end
					a1:Play(0.2, 0.2, 0.2)
					a5(GetBladeHits)
					 require(game:GetService("ReplicatedStorage").CombatFramework.RigLib).play = getgenv().B 
					wait(.5)
					a1:Stop()
				end
			end
		end)
	 end
end
end)
end)








local x2Code = {
        "GAMERROBOT_YT",
        "SUBGAMERROBOT_RESET",
        "ADMINGIVEAWAY",
        "GAMER_ROBOT_1M",
        "3BVISITS",
        "UPD16",
        "FUDD10",
        "BIGNEWS",
        "THEGREATACE",
        "SUB2GAMERROBOT_EXP1",
        "StrawHatMaine",
        "Sub2OfficialNoobie",
        "SUB2NOOBMASTER123",
        "Sub2Daigrock",
        "Axiore",
        "TantaiGaming",
        "STRAWHATMAINE",
        "Enyu_is_Pro",
        "Magicbus",
        "Sub2Fer999",
        "Starcodeheo",
        "JCWK",
        "KittGaming",
        "Bluxxy",
        "TheGreatAce"
    }
function RedeemCode(value)
       game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(value)
end

Sector1:AddButton("Redeem All Code",function()
     for i,v in pairs(x2Code) do
        RedeemCode(v)
    end
end)



    local Selectweapon = Tab:CreateSector("select weapon","Right")
    Selectweapon:AddLabel("select")
    Weapon = {}
    for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
        if v:IsA"Tool" then
            table.insert(Weapon,v.Name)
    end
end
    local WE = Selectweapon:AddDropdown("Select Weapon",Weapon,"Select Weapon",false,function(t)
        _G.SelectWeapon = t
    end)
function Equip(ToolX)
    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(ToolX) then
        getgenv().Tol = game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(ToolX)
        game.Players.LocalPlayer.Character.Humanoid:EquipTool(Tol)
    end
end
function click()
   game:GetService'VirtualUser':CaptureController()
   game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end

Sector1:AddDropdown("select",{"Boss","Boss","Boss"},"",function(t)
    pcall (function()
    end)
    end)




local Sector1 = Tab:CreateSector("---🍬Farm Candy🍭---","Right")
Sector1:AddLabel("----------🍬Candy🍭---------")


local Candyz = Sector1:AddLabel("🍬Candy🍭 : 0")


spawn(function()
    while wait(3) do
        pcall(function()
for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
    if v["Type"] == "Material" then
    if v.Name == "Candy" then
            Candyz:Set("🍬Candy🍭 : "..v.Count)
    end
    end
end

        end)
    end
end)


Sector1:AddToggle("🍬AuToFarm Candy🍭",false,function(t)
   _G.AUTOBONE = t
   tween_cancel()
end)




    spawn(function()
        game:GetService("RunService").RenderStepped:Connect(function()
            pcall(function()
                if _G.AUTOBONE then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Candy Pirate [Lv. 2400]") then
                            MonZ = "Candy Pirate [Lv. 2400]"
                            CFMN = CFrame.new(-1290.6978759765625, 14.821269035339355, -14544.4189453125)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Snow Demon [Lv. 2425]") then
                            MonZ = "Snow Demon [Lv. 2425]"
                            CFMN = CFrame.new(-899.1539306640625, 26.603485107421875, -14432.8408203125)
                            end
                    end
                end)
               end)
    end)
        


    spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                if game:GetService("Workspace").Enemies:FindFirstChild("Candy Pirate [Lv. 2400]") or game:GetService("Workspace").Enemies:FindFirstChild("Snow Demon [Lv. 2425]") then
                gotopos(game:GetService("Workspace").Enemies[MonZ].HumanoidRootPart.CFrame * CFrame.new(0,45,0))
        local CombatFramework = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
            local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
            Camera:Stop()
            getupvalues(CombatFramework)[2].activeController.hitboxMagnitude = 80
getupvalues(CombatFramework)[2]['activeController']:attack()  
elseif not game:GetService("Workspace").Enemies:FindFirstChild("Candy Pirate [Lv. 2400]") and not game:GetService("Workspace").Enemies:FindFirstChild("Snow Demon [Lv. 2425]") then
gotopos(CFrame.new(-1209.776123046875, 25.28952980041504, -14858.7587890625))
    end
            end
                end)
               end)
    end)
        
        
                   spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                for i2,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == MonZ and v2.Name == MonZ then
                                        v2.HumanoidRootPart.CFrame = CFMN
                                        v2.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                    end
                                end
            end
                        
                    end
                end)
                end)
                end)
                   
                               spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                    if game:GetService("Workspace").Enemies[MonZ].Humanoid.Health == 0 then
        game:GetService("Workspace").Enemies[MonZ]:Destroy()
        end
        end
        end)
        end)
                               end)
                               
spawn(function()
    while task.wait() do
        pcall(function()
            if _G.AUTOBONE then 
                if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000,100000,100000)
                    Noclip.Velocity = Vector3.new(0,0,0)
                end
            else
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
        end)
    end
end)

spawn(function()
    pcall(function()
        game:GetService("RunService").Stepped:Connect(function()
            if _G.AUTOBONE then
                for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                    if v:IsA("BasePart") then
                        v.CanCollide = false    
                    end
                end
            end
        end)
        
        
                                       spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                        while true do wait()
                        local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)

CombatFrameworkR = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)

y = debug.getupvalues(CombatFrameworkR)[2]

spawn(function()

    game:GetService("RunService").RenderStepped:Connect(function()

        if _G.FastAttack then

            if typeof(y) == "table" then

                pcall(function()

                    CameraShaker:Stop()

                    y.activeController.timeToNextAttack = (math.huge^math.huge^math.huge)

                    y.activeController.timeToNextAttack = 0

                    y.activeController.hitboxMagnitude = 60.9

                    y.activeController.active = false

                    y.activeController.timeToNextBlock = 0

                    y.activeController.focusStart = 1655503339.0980349

                    y.activeController.increment = 1

                    y.activeController.blocking = false

                    y.activeController.attacking = false

                    y.activeController.humanoid.AutoRotate = true

                end)

            end

        end

    end)

end)
end
end
end)
end)
end)
end)
end)


















local Sector1 = Tab:CreateSector("---🦴Farm Bones🗿---","Right")
Sector1:AddLabel("----------🦴Bones🗿---------")


local Boness = Sector1:AddLabel("🦴Bones🗿 : 0")

spawn(function()
    while wait(3) do
        pcall(function()
for i,v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
    if v["Type"] == "Material" then
    if v.Name == "Bones" then
            Boness:Set("🦴Bones🗿 : "..v.Count)
    end
    end
end

        end)
    end
end)



Sector1:AddToggle("🦴AuToFarm Bones🗿",false,function(t)
   _G.AUTOBONE = t
   tween_cancel()
end)




    spawn(function()
        game:GetService("RunService").RenderStepped:Connect(function()
            pcall(function()
                if _G.AUTOBONE then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy [Lv. 2050]") then
                            MonZ = "Posessed Mummy [Lv. 2050]"
                            CFMN = CFrame.new(-9579.24121, 5.85520077, 6201.396, -0.78157568, -7.62796262e-08, 0.62381041, -8.98267487e-08, 1, 9.73568248e-09, -0.62381041, -4.84256901e-08, -0.78157568)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul [Lv. 2025]") then
                            MonZ = "Demonic Soul [Lv. 2025]"
                            CFMN = CFrame.new(-9518.125, 172.16748, 6142.5459, 0.597414613, 3.36901813e-08, 0.801932514, -2.49106016e-08, 1, -2.3453623e-08, -0.801932514, -5.96508443e-09, 0.597414613)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie [Lv. 2000]") then
                            MonZ = "Living Zombie [Lv. 2000]"
                            CFMN = CFrame.new(-10171.2461, 138.689331, 5955.48779, -0.762927949, -6.17750899e-08, 0.646483541, -9.17780483e-08, 1, -1.27535298e-08, -0.646483541, -6.90630202e-08, -0.762927949)
                        elseif game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton [Lv. 1975]") then
                            MonZ = "Reborn Skeleton [Lv. 1975]"
                            CFMN = CFrame.new(-8765.23926, 142.16748, 6015.74268, 0.578889489, 1.17372441e-08, -0.815406024, 2.22573107e-08, 1, 3.01957144e-08, 0.815406024, -3.56287266e-08, 0.578889489)
                            end
                    end
                end)
               end)
    end)
        


    spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                if game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy [Lv. 2050]") or game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul [Lv. 2025]") or game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie [Lv. 2000]") or game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton [Lv. 1975]") then
                gotopos(game:GetService("Workspace").Enemies[MonZ].HumanoidRootPart.CFrame * CFrame.new(0,45,0))
        local CombatFramework = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
            local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
            Camera:Stop()
            getupvalues(CombatFramework)[2].activeController.hitboxMagnitude = 80
getupvalues(CombatFramework)[2]['activeController']:attack()  
elseif not game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy [Lv. 2050]") and not game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul [Lv. 2025]") and not game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie [Lv. 2000]") and not game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton [Lv. 1975]") then
gotopos(CFrame.new(-9518.125, 172.16748, 6142.5459, 0.597414613, 3.36901813e-08, 0.801932514, -2.49106016e-08, 1, -2.3453623e-08, -0.801932514, -5.96508443e-09, 0.597414613))
    end
            end
                end)
               end)
    end)
        
        
                   spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                for i2,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == MonZ and v2.Name == MonZ then
                                        v2.HumanoidRootPart.CFrame = CFMN
                                        v2.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                    end
                                end
            end
                        
                    end
                end)
                end)
                end)
                   
                               spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                    if game:GetService("Workspace").Enemies[MonZ].Humanoid.Health == 0 then
        game:GetService("Workspace").Enemies[MonZ]:Destroy()
        end
        end
        end)
        end)
                               end)
                               
spawn(function()
    while task.wait() do
        pcall(function()
            if _G.AUTOBONE then 
                if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000,100000,100000)
                    Noclip.Velocity = Vector3.new(0,0,0)
                end
            else
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
        end)
    end
end)

spawn(function()
    pcall(function()
        game:GetService("RunService").Stepped:Connect(function()
            if _G.AUTOBONE then
                for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                    if v:IsA("BasePart") then
                        v.CanCollide = false    
                    end
                end
            end
        end)
        
        
                                       spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.AUTOBONE then
                        while true do wait()
                        local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)

CombatFrameworkR = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)

y = debug.getupvalues(CombatFrameworkR)[2]

spawn(function()

    game:GetService("RunService").RenderStepped:Connect(function()

        if _G.FastAttack then

            if typeof(y) == "table" then

                pcall(function()

                    CameraShaker:Stop()

                    y.activeController.timeToNextAttack = (math.huge^math.huge^math.huge)

                    y.activeController.timeToNextAttack = 0

                    y.activeController.hitboxMagnitude = 60.9

                    y.activeController.active = false

                    y.activeController.timeToNextBlock = 0

                    y.activeController.focusStart = 1655503339.0980349

                    y.activeController.increment = 1

                    y.activeController.blocking = false

                    y.activeController.attacking = false

                    y.activeController.humanoid.AutoRotate = true

                end)

            end

        end

    end)

end)
end
end
end)
end)
end)
end)
end)






















local Sector1 = Tab:CreateSector("AuTo Melee Coming Soon...","left")
Sector1:AddToggle("Auto Superhuman🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)







Sector1:AddToggle("Auto DeathStep🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)





Sector1:AddToggle("Auto SharkmanKarate🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)





Sector1:AddToggle("Auto ElectricClaw🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)







Sector1:AddToggle("Auto DragonTalon🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)









Sector1:AddToggle("Auto Godhuman🔴only",false,function(t)
   print("นี่คือฟาร์มเลเวลเเบบไม่มีลัดฟามไม่ฆ่าคน")
end)


local Tab = CenterHubNo1:CreateTab("Buy Item")
local Sector1 = Tab:CreateSector("Buy Melee","Left")
local Sector2 = Tab:CreateSector("Ability","Right")


Sector1:AddButton("DragonTalon",function()
    pcall (function()
        local args = {
    [1] = "BuyDragonTalon"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
end)


Sector1:AddButton("ElectricClaw",function()
    pcall (function()
        local args = {
    [1] = "BuyElectricClaw"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)

Sector1:AddButton("SharkmanKarate",function()
    pcall (function()
        local args = {
    [1] = "BuySharkmanKarate"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector1:AddButton("DeathStep",function()
    pcall (function()
        local args = {
    [1] = "BuyDeathStep"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector1:AddButton("Godhuman",function()
    pcall (function()
        local args = {
    [1] = "BuyGodhuman"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector1:AddButton("BlackLeg",function()
    pcall (function()
        local args = {
    [1] = "BuyBlackLeg"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector1:AddButton("Electro",function()
    pcall (function()
        local args = {
    [1] = "BuyElectro"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector1:AddButton("FishmanKarate",function()
    pcall (function()
        local args = {
    [1] = "BuyFishmanKarate"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end)
end)

Sector1:AddButton("DragonClaw",function()
    pcall (function()
        local args = {
    [1] = "BlackbeardReward",
    [2] = "DragonClaw",
    [3] = "2"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)

Sector1:AddButton("Superhuman",function()
    pcall (function()
        local args = {
    [1] = "BuySuperhuman"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)


Sector2:AddButton("Geppo",function()
    pcall (function()
        local args = {
    [1] = "BuyHaki",
    [2] = "Geppo"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

    end)
end)

Sector2:AddButton("Buso",function()
    pcall (function()
        local args = {
    [1] = "BuyHaki",
    [2] = "Buso"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

    end)
end)

Sector2:AddButton("Soru",function()
    pcall (function()
        local args = {
    [1] = "BuyHaki",
    [2] = "Soru"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

    end)
end)




local Tab = CenterHubNo1:CreateTab("Teleport")
local Sector3 = Tab:CreateSector("Part","Right")
Sector3:AddButton("Stop Tween",function()
    pcall(function()
        TP(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
		_G.Part = false
    end)
end)
Sector3:AddButton("Part",function()
    pcall (function()
                _G.Farm = true
spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if _G.Farm then
            if not game:GetService("Workspace"):FindFirstChild("LOL") then
                local LOL = Instance.new("Part")
                LOL.Name = "LOL"
                LOL.Parent = game.Workspace
                LOL.Anchored = true
                LOL.Transparency = 1
                LOL.Size = Vector3.new(50,0.5,50)
                LOL.Material = "Neon"
            elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                game.Workspace["LOL"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,-2,0)
            end
        else
            if game:GetService("Workspace"):FindFirstChild("LOL") then
                game:GetService("Workspace"):FindFirstChild("LOL"):Destroy()
            end
        end
    end)
end)
    end)
end)



Sector3:AddButton("false Part",function()
    pcall (function()
        _G.Farm = false
spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if _G.Farm then
            if not game:GetService("Workspace"):FindFirstChild("LOL") then
                local LOL = Instance.new("Part")
                LOL.Name = "LOL"
                LOL.Parent = game.Workspace
                LOL.Anchored = true
                LOL.Transparency = 1
                LOL.Size = Vector3.new(50,0.5,50)
                LOL.Material = "Neon"
            elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                game.Workspace["LOL"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,-2,0)
            end
        else
            if game:GetService("Workspace"):FindFirstChild("LOL") then
                game:GetService("Workspace"):FindFirstChild("LOL"):Destroy()
            end
        end
    end)
end)
    end)
end)


if W then
local Sector3 = Tab:CreateSector("Teleport in World 1","Left")
Sector3:AddButton("Starter Islands",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(976.1187133789062, 16.516620635986328, 1428.2723388671875))
    end)
end)
        Sector3:AddButton("Jungle",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1605.92236, 36.8521347, 149.120728, 0.0171093047, 4.86186309e-08, -0.999853611, -9.45663103e-08, 1, 4.70075463e-08, 0.999853611, 9.37481985e-08, 0.0171093047))
            end)
end)
        Sector3:AddButton("Middle Island",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-784.29248046875, 33.65190124511719, 1606.9835205078125))
            end)
end)
        Sector3:AddButton("Desert",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(1330.142333984375, 101.86573791503906, 4489.53955078125))
            end)
end)
        Sector3:AddButton("Pirate Village",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1252.4139404296875, 44.55205535888672, 3820.52392578125))
            end)
end)
        Sector3:AddButton("Frozen Village",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(1222.4112548828125, 70.81449127197266, -1243.112548828125))
            end)
end)
        Sector3:AddButton("Prison",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(5010.4150390625, 88.6519775390625, 738.5647583007812))
            end)
end)
        Sector3:AddButton("Marine Fortress",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5150.67724609375, 375.9053649902344, 4443.45654296875))
            end)
end)
        Sector3:AddButton("Colosseum",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1829.173583984375, 80.37115478515625, -3054.580810546875))
            end)
end)
        Sector3:AddButton("Fountain City",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(5190.37939453125, 38.50114059448242, 4154.75830078125))
            end)
end)
        Sector3:AddButton("Underwater City",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(4049.18798828125, 1.9886010885238647, -1815.5950927734375))
            end)
end)

        Sector3:AddButton("Sky 1",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-4911.6884765625, 737.6860961914062, -2577.429443359375))
            end)
end)
        Sector3:AddButton("Sky 2",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-7761.7216796875, 5644.8818359375, -1882.1690673828125))
            end)
end)
        Sector3:AddButton("Sky warp",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-4610.22216796875, 851.630859375, -1706.4027099609375))
            end)
end)

        Sector3:AddButton("Magma Village",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5193.35498046875, 8.59068489074707, 8569.5634765625))
            end)
end)
end
if W2 then
local Sector3 = Tab:CreateSector("Teleport in World 2","Left")
Sector3:AddButton("Defualt life",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-16.07593536376953, 39.18061447143555, 2689.6982421875))
            end)
end)
Sector3:AddButton("colossem",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1939.60400390625, 241.62832641601562, 1750.9613037109375))
            end)
end)
Sector3:AddButton("Mansion",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-512.3316040039062, 331.8605651855469, 590.0559692382812))
            end)
end)
Sector3:AddButton("Cafe",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-387.33868408203125, 135.02029418945312, 367.1448974609375))
            end)
end)
Sector3:AddButton("Boost Race V.3",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1990.0743408203125, 125.49332427978516, -70.82737731933594))
            end)
end)
Sector3:AddButton("Factory",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(426.4340515136719, 211.22866821289062, -425.4928894042969))
            end)
end)
Sector3:AddButton("Green Beach & Boost Race V.2",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-2775.84375, 72.96612548828125, -3569.595947265625))
            end)
end)
Sector3:AddButton("Iceland",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(632.2200927734375, 401.42193603515625, -5397.30615234375))
            end)
end)
Sector3:AddButton("Dark Area",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(3779.3388671875, 22.652170181274414, -3499.4306640625))
            end)
end)
Sector3:AddButton("Ice Castle",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(6290.19970703125, 300.7259826660156, -6949.89794921875))
            end)
end)
Sector3:AddButton("Usoupp",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(4785.8193359375, 7.9396586418151855, 2919.791748046875))
            end)
end)
Sector3:AddButton("Christmas Day",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5293.6904296875, 14.616416931152344, 1514.9449462890625))
            end)
end)
Sector3:AddButton("Land ?",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5102.8349609375, 3.220874071121216, 2468.238525390625))
            end)
end)
Sector3:AddButton("Tomb",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5649.466796875, 266.3584289550781, -756.30419921875))
            end)
end)
Sector3:AddButton("Boat",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-6501.90576171875, 83.16971588134766, -123.83794403076172))
            end)
end)

Sector3:AddButton("Cool Land",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-6442.8896484375, 742.6068725585938, -4961.25634765625))
            end)
end)

Sector3:AddButton("Buy Microchip",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-6472.0908203125, 250.61964416503906, -4440.02685546875))
            end)
end)

Sector3:AddButton("Hot Land",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5317.6728515625, 23.808900833129883, -5447.85302734375))
            end)
end)

Sector3:AddButton("Buy Microchip Koko",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-4973.7431640625, 143.73207092285156, -5394.0947265625))
            end)
end)

Sector3:AddButton("Start chip Koko",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5570.89306640625, 332.4136047363281, -5963.54052734375))
            end)
end)

Sector3:AddButton("skull island",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-2732.982666015625, 238.84622192382812, -10255.689453125))
            end)
end)
Sector3:AddButton("skull island Boss",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-3729.0712890625, 106.87252044677734, -11775.447265625))
end)
end)
end




if W3 then
local Sector3 = Tab:CreateSector("Teleport in World 3","Left")
Sector3:AddButton("Port Town",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-206.20391845703125, 73.72992706298828, 6016.48828125))
            end)
end)
Sector3:AddButton("Door Open Quest Tushita",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(5165.650390625, 141.7864532470703, 909.8078002929688))
            end)
end)
Sector3:AddButton("PvP",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(60.49848556518555, -1451.315185546875))
            end)
end)
Sector3:AddButton("Hydra",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(5436.1396484375, 601.569091796875, -52.467742919921875))
            end)
end)
Sector3:AddButton("Tree",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(2499.233154296875, 190.39747619628906, -7135.740234375))
            end)
end)
Sector3:AddButton("Big Mom",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-909.1905517578125, 58.94573974609375, -10877.4501953125))
            end)
end)
Sector3:AddButton("Cake Land",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-2161.356689453125, 70.31721496582031, -12385.4873046875))
            end)
end)
Sector3:AddButton("Peanut",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-2376.5546875, 63.33401107788086, -10125.3642578125))
            end)
end)
Sector3:AddButton("Mansion",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-12550.6650390625, 333.41455078125, -7585.21728515625))
            end)
end)
Sector3:AddButton("Spawn Fire Tushita 1",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-10752.2607421875, 412.2037353515625, -9364.638671875))
            end)
end)
Sector3:AddButton("Spawn Fire Tushita 2",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-11673.80078125, 331.72320556640625, -9473.9169921875))
            end)
end)
Sector3:AddButton("Spawn Fire Tushita 3",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-12133.310546875, 519.4494018554688, -10653.5458984375))
            end)
end)
Sector3:AddButton("Spawn Fire Tushita 4",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-13336.58984375, 485.28173828125, -6983.318359375))
            end)
end)
Sector3:AddButton("Spawn Fire Tushita 5",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-13487.7587890625, 332.3781433105469, -7925.45751953125))
            end)
end)
Sector3:AddButton("Castle",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5234.9833984375, 1088.724609375, -2578.825927734375))
            end)
end)
Sector3:AddButton("Spawn Haki White",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-4971.9013671875, 335.91192626953125, -3720.261962890625))
            end)
end)
Sector3:AddButton("Spawn Haki Red",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5414.90966796875, 314.2118835449219, -2212.645751953125))
            end)
end)
Sector3:AddButton("Spawn Haki Pink",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-5421.01513671875, 1089.311767578125, -2665.997314453125))
            end)
end)
Sector3:AddButton("Chocolate Bar",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(217.13331604003906, 126.59196472167969, -12598.041015625))
            end)
end)
Sector3:AddButton("Christmas Land",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-1078.312255859375, 14.614645957946777, -14470.537109375))
            end)
end)
Sector3:AddButton("Ghost Land",function()
    pcall (function()
        function TP(P1)
            local Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        Speed = 600
    elseif Distance < 500 then
        Speed = 500
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 250
    end
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
        ):Play()
        if _G.Stop_Tween then
        game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P1}
        ):Cancel()
        end
    end
TP(CFrame.new(-9501.4326171875, 580.0858154296875, 6033.39599609375))
            end)
end)
end


local Sector3 = Tab:CreateSector("Server","Right")
Sector3:AddButton("TravelMain",function()
    pcall (function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
    end)
end)


Sector3:AddButton("TravelDressrosa",function()
    pcall (function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
    end)
end)


Sector3:AddButton("TravelZou",function()
    pcall (function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
    end)
end)
Sector3:AddLabel("---------------------------")
Sector3:AddButton("Hopserver",function()
    pcall (function()
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
                                 -- delfile("NotSameServers.json")
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
                        -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                        wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                     end)
                     wait(.1)
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
    end)
end)

Sector3:AddButton("Rejoin",function()
    pcall (function()
        local ts = game:GetService("TeleportService")

local p = game:GetService("Players").LocalPlayer

 

ts:Teleport(game.PlaceId, p)
end)
end)


Sector3:AddButton("Copy Job Id",function()
    setclipboard(game.JobId)
Library:Notify('Copy : '..game.JobId, 5)
    end)
    
    
    
Sector3:AddButton("Join Job Id",function()
game:GetService'TeleportService':TeleportToPlaceInstance(game.PlaceId,_G.JobID,game:GetService'Players'.LocalPlayer)
    end)

Sector3:AddToggle("Auto rejoin when is error",function()
    pcall (function()
        spawn(function() 
    while true do wait()
        getgenv().rejoin = game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(Kick)

                if Kick.Name == 'ErrorPrompt' and Kick:FindFirstChild('MessageArea') and Kick.MessageArea:FindFirstChild("ErrorFrame") then
                    game:GetService("TeleportService"):Teleport(game.PlaceId)
                    wait(50)
                end
        end)
    end
end)
end)
end)




local Sector3 = Tab:CreateSector("Function others","Right")
Sector3:AddToggle("Set spawn point",function()
    pcall (function()
                    task.spawn(function()
    pcall(function()
        while task.wait(0.1) do
            if _G.A and game.Players.LocalPlayer.Character.Humanoiud.Health > 0 then
                -- Script generated by SimpleSpy - credits to exx#9394

                local args = {
                    [1] = "SetSpawnPoint"
                }

                game:GetService("ReplicatedStorage").Remotes.CommF:InvokeServer(unpack(args))
            end
        end
    end)
end)
        end)
end)



spawn(function() 
    while true do wait()
        getgenv().rejoin = game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(Kick)

                if Kick.Name == 'ErrorPrompt' and Kick:FindFirstChild('MessageArea') and Kick.MessageArea:FindFirstChild("ErrorFrame") then
                    game:GetService("TeleportService"):Teleport(game.PlaceId)
                    wait(50)
                end
        end)
    end
end)


Sector3:AddToggle("Anti Afk",true,function()
    pcall (function()
        local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
wait(1)
vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
end)
end)

task.spawn(function()
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

local Tab = CenterHubNo1:CreateTab("Visual")
local Sector4 = Tab:CreateSector("Function","Left")
Sector4:AddButton("Fake Kroblox",function()
    pcall (function()
        game.Players.LocalPlayer.Character.RightUpperLeg.MeshId="rbxassetid://902942096"
wait()
game.Players.LocalPlayer.Character.RightUpperLeg.TextureID="rbxassetid://902843398"
wait()
game.Players.LocalPlayer.Character.RightLowerLeg.Transparency=1
wait()
game.Players.LocalPlayer.Character.RightFoot.Transparency=1
end)
end)
Sector4:AddButton("Auto Store Fruit",function()
    pcall (function()
            local args = {
    [1] = "Cousin",
    [2] = "Buy"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
end)

local Sector5 = Tab:CreateSector("Buy Raid","Right")
Sector5:AddButton("Flame",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Flame"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Ice",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Ice"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Quake",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Quake"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Light",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Light"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Dark",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Dark"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("String",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "String"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Rumble",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Rumble"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Magma",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Magma"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Human: Buddha",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Human: Buddha"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)
Sector5:AddButton("Sand",function()
    pcall (function()
        local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Sand"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end)
end)



local Tab = CenterHubNo1:CreateTab("MAIN")
local Sector5 = Tab:CreateSector("General","left")
local ping = game:GetService("Stats").Network.ServerStatsItem["Data Ping"]:GetValueString()
Sector5:AddLabel("local ping")













while wait() do --Loop
    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then --เช็คว่าเปิดHakiอยู่ไหม
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")--RemoteเปิดHaki
    end --EndของIf
end --EndของLoop
