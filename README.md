local Library = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local Window = Library.CreateLib("Doors Hub V2", "GrapeTheme")
local Tab = Window:NewTab("Modes")
local Section = Tab:NewSection("Modes")
Section:NewButton("Mayhem Mode", "Have Fun!", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/HollowedOutMods/MayhemMode/main/loader.lua'))()
end)
Section:NewButton("Impossible Mode", "Have Fun!", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/Ukazix/impossible-mode/main/Protected_79.lua.txt'))()
end)
Section:NewButton("Endless Doors", "Have Fun!", function()
--Credits to NovaNextruis, Muhammadgames, Zavaled, SquidR
--ICherryKardess, Screech, Jessica, TheEndIsNear, C87FM
--Your game might crash when you get an achievement

game.SoundService.AmbientReverb = "City"
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/Script.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/ScriptNoAchievements.txt"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/seekeye.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/seekmodel.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/VictrolaRecreation.txt"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/worldcuuuup/main/MusicReplace.txt"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/check78/Entities/main/DeathSound.txt"))()
end)
Section:NewButton("Fragmented Mode", "Have fun!", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Potato032/Doors-Fragmented-Mode/main/ScriptDontShareItsOnDC.txt"))()
end)
Section:NewButton("RND Mode", "Have fun!", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/huyhoanphuc/roomsanddoors-20-20-20-20-20-20/main/README.md", true))()
end)
Section:NewButton("Exetreme Mode", "Have fun!", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/huyhoanphuc/ygf/none/README.md", true))()
end)
Section:NewButton("Noonie Hardcore", "Have Fun!", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/huyhoanphuc/modev2/main/README.md'))()
end)
Section:NewButton("AK47 gun", "Dont Kill your friends!", function()
-- Credit to PenguinManiack For Creating The Script

local Functions = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Functions.lua"))()
local CustomShop = loadstring(game:HttpGet("https://raw.githubusercontent.com/RegularVynixu/Utilities/main/Doors/Custom%20Shop%20Items/Source.lua"))()
local UIS = game:GetService("UserInputService")
local exampleTool = LoadCustomInstance("rbxassetid://12848567274") -- wand model

if game:GetService("Players").LocalPlayer.PlayerGui.MainUI.ItemShop.Visible == true then
    -- Create custom shop item
    CustomShop.CreateItem(exampleTool, {
        Title = "Harry Potter Wand",
        Desc = "Works on entities",
        Image = "https://cdn.discordapp.com/attachments/1049016956231102465/1078727375631679688/image_2023-02-24_121721211-removebg-preview.png",
        Price = "gun",
        Stack = 1,
    })
    ----------------------------------------- parenting
else
    exampleTool.Parent = game.Players.LocalPlayer.Backpack
end
local tool = exampleTool
local function Shoot()
    local bullet = game:GetObjects("rbxassetid://12848374097")[1]
    task.wait()
    bullet.Anchored = false
    bullet.Massless = false
    local Sound = Instance.new("Sound", game.StarterPlayer)
    Sound.Volume = 3.5
    Sound.SoundId = "rbxassetid://5238024665"
    Sound.PlayOnRemove = true
    Sound:Destroy()
    HRP = exampleTool.BulletPart.CFrame * CFrame.Angles(0,math.rad(-90),0)
    local Attachment = Instance.new("Attachment", bullet)
    local LV = Instance.new("LinearVelocity", Attachment) -- creating the linear velocity
    LV.MaxForce = math.huge -- no need to worry about this
    LV.VectorVelocity = (game:GetService("Players").LocalPlayer:GetMouse().Hit.Position - tool.BulletPart.Position).Unit * 100-- HRP.lookVector * 50 -- change 100 with how fast you want the projectile to go
    LV.Attachment0 = Attachment --Required Attachment
    bullet.Parent = game.Workspace
    bullet.CFrame = tool.BulletPart.CFrame * CFrame.Angles(math.rad(0),math.rad(90),math.rad(90))
    bullet.Touched:Connect(function(part)
        local Model = part:FindFirstAncestorWhichIsA("Model")
        if Model ~= nil and Model:GetAttribute("IsCustomEntity") == true then
            Model:Destroy()
        end
    end)
    task.wait(0.3)
    bullet:Destroy()
    end
----------------------------------------------- Shooting!
   
UIS.InputBegan:Connect(function(input)
    if tool.Parent == game.Players.LocalPlayer.Character then
        if input.UserInputType == Enum.UserInputType.MouseButton1 then
        getgenv().BulletType = "12848374097"
        Shoot()
       
        end
    end
end)
end)
Section:NewButton("Purple Flashlight", "Light up;!", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/K0t1n/Public/main/Purple%20Flashlight"))()
end)
Section:NewButton("Crucifix on anything press [q]", "Have Fun!", function()
_G.Uses = 1
_G.Range = 30
_G.OnAnything = true
_G.Fail = false
_G.Variant = "Electric"
loadstring(game:HttpGet('https://raw.githubusercontent.com/PenguinManiack/Crucifix/main/Crucifix.lua'))()
end)
local Tab = window:NewTab("Credits")
local Section = Tab:NewSection("Credits")
Section:NewButton("Angeliqq/Rainbow", "Owner", function()
loadstring(game:HttpGet("https://pastebin.com/raw/tWGxhNq0"))()
end)
