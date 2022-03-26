
--Name: "Ninja Legends Script GUI | AUTO SLASH, AITO SELL, AUTO BUY & MORE!"

 _G.Color = Color3.fromRGB(66, 135, 245)
_G.Color2 = Color3.fromRGB(66, 135, 245)

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/slightten/ui-libs/main/funni"))()
local window = library:CreateWindow("Die Hub Ninja Legends", Enum.KeyCode.RightControl)
local plr = game.Players.LocalPlayer
local tab1 = window:CreateTab("Main")
local tab2 = window:CreateTab("Misc")
local sect2 = tab2:CreateSector("Misc", 'left')
sect2:AddLabel("V3rm borntodie1")

--Game Data

local ranks = {}
for i,v in pairs(game:GetService("ReplicatedStorage").Ranks.Ground:GetChildren()) do
   table.insert(ranks,tostring(v))
end


local teleports = {}
for i,v in pairs(game:GetService("Workspace").areaTeleportParts:GetChildren()) do
   table.insert(teleports,tostring(v))
end



-- Autofarm


local sect1 = tab1:CreateSector("Farming", 'left')

sect1:AddToggle("Auto Swing", false, function(a)
   aa = a
   while aa do task.wait()
       
       local ohString1 = "swingKatana"

game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(ohString1)
   
       end
   end)


sect1:AddToggle("Auto Sell", false, function(b)
   bb = b
   while bb do task.wait()
       
       game:GetService("Workspace").sellAreaCircles.sellAreaCircle16.circleInner.CFrame = CFrame.new(50,50,50)
       game:GetService("Workspace").sellAreaCircles.sellAreaCircle16.circleInner.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position)
   
       end
   end)


sect1:AddToggle("Auto Buy Swords", false, function(c)
   cc = c
   while cc do task.wait()
               local ohString1 = "buyAllSwords"
               local ohString2 = "Blazing Vortex Island"
               
               game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(ohString1, ohString2)
           end
   end)


sect1:AddToggle("Auto Buy Belts", false, function(d)
   dd = d
   while dd do task.wait()
       
       local ohString1 = "buyAllBelts"
local ohString2 = "Blazing Vortex Island"

game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(ohString1, ohString2)
   
       end
   end)


   sect1:AddToggle("Auto Buy Ranks", false, function(e)
       ee = e
           while ee do task.wait()
           
               for i = 1,#ranks do
                   local ohString1 = "buyRank"
                   local ohString2 = ranks[i]
                   
                   game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(ohString1, ohString2)
               end
           end
       end)



sect1:AddToggle("Auto Buy Skills", false, function(f)
   ff = f
   while ff do task.wait()
       
       local ohString1 = "buyAllSkills"
   local ohString2 = "Blazing Vortex Island"
   
   game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(ohString1, ohString2)
   
       end
   end)

   sect1:AddToggle("Auto Hoops", false, function(g)
       gg = g
           while gg do task.wait()
               
               for i,v in pairs(game:GetService("Workspace").Hoops:GetChildren()) do
                   v.touchPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position)
                   wait(0.02)
               end
           end
       end)

       sect1:AddButton("Auto Chest", function()
                   for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                       if string.match(v.Name,"Chest") and v:IsA("Model") then
                           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(v.circleOuter.Position)
                           game.Players.LocalPlayer.Character.Humanoid.Jump = true
                           wait(0.5)
                       end
                   end
           end)
       


               --Teleport to all
               local sect3 = tab1:CreateSector("Teleport", 'right')
               
               sect3:AddButton("Discover all Islands",function()
                   for i = 1,#teleports do
               game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").areaTeleportParts[teleports[i]].Position)
               wait()
                   end
               end)
loadstring(game:HttpGet('https://raw.githubusercontent.com/borntodiekuv/Die/main/Hub'))()

 
