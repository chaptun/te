
_G.Color = Color3.fromRGB(212, 0, 255)
_G.Color2 = Color3.fromRGB(255, 255, 255)
join = game.Players.localPlayer.Neutral == false
if _G.Team == nil then
    _G.Team = "Pirates"
end
if _G.Team == "Pirates" or _G.Team == "Marines" and not join then
    repeat wait()
        pcall(function()
            join = game.Players.localPlayer.Neutral == false
            if _G.Team == "Pirates" then
                for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
                    v.Function()
                end
            elseif _G.Team == "Marines" then
                for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
                    v.Function()
                end
            else
                for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
                    v.Function()
                end
            end
        end)
    until join == true
    game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Visible = false
end
wait(1)
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
library:CreateWatermark("Edog Hub")
local EdogHub1 = library:CreateWindow("Edog Hub | Blox Fruit",Enum.KeyCode.RightControl)

local Tab1 = EdogHub1:CreateTab("Main")

local Sector1 = Tab1:CreateSector("Auto Farm Level","left")

function loadcheck()
    if isfile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json") then
        else
            writefile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json",game:GetService("HttpService"):JSONEncode(_G.Save))
        return
    end
end
pcall(function()
	_G.Save = {
		--AutoFarm--
		['AutoFarm'] = false,
        ['FastFarm'] = false,
        ['Weapon'] = "",
        ['Fast_Attack'] = true,
        ['Select Mode'] = "Gun", --Gun,Fruit
        ['Farm_Mastery'] = false,
        ['HealthPersen'] = 20,
		['AutoMeleekaitun'] = false,
		----AutoSworld/Melee/Acces----
		['Auto_Rengoku'] = false,
		['Auto_Rengoku_Hop'] = false,
		['Auto_Buddy'] = false,
		['Auto_Buddy_Hop'] = false,
		['Auto_Yama'] = false,
		['Auto_Yama_Hop'] = false,
		['Auto_Legendaly'] = false,
		['Auto_Legendaly_Hop'] = false,
		['Auto_Canvender'] = false,
		['Auto_Canvender_Hop'] = false,
		['Auto_Hallow_Scythe'] = false,
		['Auto_Bone'] = false,
		['Auto_Enchancement'] = false,
		['Autothird'] = false,
		['AutoNewWorld'] = false,
		['Auto_Rainbow_Haki'] = false,
		['Auto_Observations_V2'] = false,
		['SEAKING'] = false,
		['SEAKINGHOP'] = false,
		--AutoSkill--
		['SKILLZ'] = false,
		['SKILLX'] = false,
		['SKILLC'] = false,
		['SKILLV'] = false,
		--Acces--
		['SwanGlasses'] = false,
		--Melee--
		['Superhuman'] = false,
		['DargonTalon'] = false,
		['DeathStep'] = false,
		['Electricclow'] = false,
		--Misc
		['Auto_Trade_Death_King'] = false,
		----Auto Stats----
		['Melee'] = false,
		['Defense'] = false,
		['Sword'] = false,
		['Blox_Fruit'] = false,
		['Gun'] = false,
		--ESP,Autoplayer--
		['ESPPlayer'] = false,
		['ChestESP'] = false,
		--Raid--
		['SelectRaid'] = "ice", --,"Ice","Quake","Light","Dark","String","Rumble","Magma","Human: Buddha","Sand" เธฃเธฒเธขเธเธทเนเธญRaids
		['AutoRaid'] = false,
		['Killaura'] = false,
		['NextIsland'] = false,
		['AutoAwakener'] = false,
	}
end)
function LoadSetting()
    if isfile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json") then
        vb = game:GetService("HttpService"):JSONDecode(readfile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json"))
        _G.Save = vb
    else
        loadcheck()
    end
end

function SaveSetting()
    if isfile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json") then
        writefile("Edog hub Premium_"..game.Players.LocalPlayer.Name..".json",game:GetService("HttpService"):JSONEncode(_G.Save))
    else
        loadcheck()
    end
end

loadcheck()
LoadSetting()
SaveSetting()
local placeId = game.PlaceId
if placeId == 2753915549 then
	OldWorld = true
elseif placeId == 4442272183 then
	NewWorld = true
elseif placeId == 7449423635 then
	ThreeWorld = true
else
	game.Players.LocalPlayer:Kick("รันผิดเกม อย่า เล่น เก")
end
function CheckQuest()
	local MyLevel = game.Players.LocalPlayer.Data.Level.Value
	if OldWorld then
		if MyLevel == 1 or MyLevel <= 9 then -- Bandit
			Ms = "Bandit [Lv. 5]"
			NaemQuest = "BanditQuest1"
			LevelQuest = 1
			NameMon = "Bandit"
			ISLANDPOS = CFrame.new(1211.88525, 36.7203407, 1500.03467, 0.615429699, -0.788191795, -6.02006912e-06, 6.02006912e-06, 1.23977661e-05, -1, 0.788191795, 0.615429759, 1.23977661e-05)
			CFrameQuest = CFrame.new(1061.66699, 16.5166187, 1544.52905, -0.942978859, -3.33851502e-09, 0.332852632, 7.04340497e-09, 1, 2.99841325e-08, -0.332852632, 3.06188177e-08, -0.942978859)
			CFrameMon = CFrame.new(1158.19287, 16.7761078, 1598.75024, 0.728623271, -2.60434244e-05, -0.684914768, 5.54633402e-07, 1, -3.74343144e-05, 0.684914768, 2.68956283e-05, 0.728623271)
		elseif MyLevel == 10 or MyLevel <= 14 then -- Monkey
			Ms = "Monkey [Lv. 14]"
			NaemQuest = "JungleQuest"
			LevelQuest = 1
			NameMon = "Monkey"
			ISLANDPOS = CFrame.new(-1180.99561, 21.0006905, 187.688171, -0.866141438, -2.23321149e-05, -0.499799222, 2.23321149e-05, 1, -8.33832528e-05, 0.499799222, -8.33832528e-05, -0.866141438)
			CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			CFrameMon = CFrame.new(-1612.77039, 37.1953545, 150.217361, -0.325320244, 5.01602138e-09, -0.945603907, -1.28536748e-09, 1, 5.74677994e-09, 0.945603907, 3.08499248e-09, -0.325320244)
		elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla
			Ms = "Gorilla [Lv. 20]"
			NaemQuest = "JungleQuest"
			LevelQuest = 2
			NameMon = "Gorilla"
			ISLANDPOS = CFrame.new(-1180.99561, 21.0006905, 187.688171, -0.866141438, -2.23321149e-05, -0.499799222, 2.23321149e-05, 1, -8.33832528e-05, 0.499799222, -8.33832528e-05, -0.866141438)
			CFrameQuest = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
			CFrameMon = CFrame.new(-1223.52808, 6.27936459, -502.292664, 0.310949147, -5.66602516e-08, 0.950426519, -3.37275488e-08, 1, 7.06501808e-08, -0.950426519, -5.40241736e-08, 0.310949147)
		elseif MyLevel == 30 or MyLevel <= 39 then -- Pirate
			Ms = "Pirate [Lv. 35]"
			NaemQuest = "BuggyQuest1"
			LevelQuest = 1
			NameMon = "Pirate"
			ISLANDPOS = CFrame.new(-825.657349, 3.63657403, 4123.30811, -0.138172507, 0.0225743353, -0.990150809, 0.0865087882, 0.996194243, 0.0106400847, 0.98662281, -0.0841865838, -0.139599562)
			CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			CFrameMon = CFrame.new(-1169.5365, 5.09531212, 3933.84082, -0.971822679, -3.73200315e-09, 0.235713184, -4.16762763e-10, 1, 1.41145424e-08, -0.235713184, 1.3618596e-08, -0.971822679)
		elseif MyLevel == 40 or MyLevel <= 59 then -- Brute
			Ms = "Brute [Lv. 45]"
			NaemQuest = "BuggyQuest1"
			LevelQuest = 2
			NameMon = "Brute"
			ISLANDPOS = CFrame.new(-825.657349, 3.63657403, 4123.30811, -0.138172507, 0.0225743353, -0.990150809, 0.0865087882, 0.996194243, 0.0106400847, 0.98662281, -0.0841865838, -0.139599562)
			CFrameQuest = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
			CFrameMon = CFrame.new(-1165.09985, 15.1531372, 4363.51514, -0.962800264, 1.17564889e-06, 0.270213336, 2.60172015e-07, 1, -3.4237969e-06, -0.270213336, -3.22613073e-06, -0.962800264)
		elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit
			Ms = "Desert Bandit [Lv. 60]"
			NaemQuest = "DesertQuest"
			LevelQuest = 1
			NameMon = "Desert Bandit"
			ISLANDPOS = CFrame.new(921.289673, 6.45703602, 4334.47803, -0.207233012, 8.06497269e-08, 0.978291631, 3.10611412e-08, 1, -7.58596244e-08, -0.978291631, 1.46662362e-08, -0.207233012)
			CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			CFrameMon = CFrame.new(932.788818, 6.8503746, 4488.24609, -0.998625934, 3.08948351e-08, 0.0524050146, 2.79967303e-08, 1, -5.60361286e-08, -0.0524050146, -5.44919629e-08, -0.998625934)
		elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre
			Ms = "Desert Officer [Lv. 70]"
			NaemQuest = "DesertQuest"
			LevelQuest = 2
			NameMon = "Desert Officer"
			ISLANDPOS = CFrame.new(1658.85876, 4.64293623, 4318.07129, -0.0864315033, -0.000185585552, 0.996257842, -6.89026783e-05, 1, 0.000180304938, -0.996257842, -5.30608231e-05, -0.0864315033)
			CFrameQuest = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)
			CFrameMon = CFrame.new(1617.07886, 1.5542295, 4295.54932, -0.997540116, -2.26287735e-08, -0.070099175, -1.69377223e-08, 1, -8.17798806e-08, 0.070099175, -8.03913949e-08, -0.997540116)
		elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits
			Ms = "Snow Bandit [Lv. 90]"
			NaemQuest = "SnowQuest"
			LevelQuest = 1
			NameMon = "Snow Bandits"
			ISLANDPOS = CFrame.new(1336.02625, 34.1970673, -1331.23267, 0.671367824, 0.741124272, -1.77025795e-05, 1.77025795e-05, -3.9935112e-05, -1, -0.741124272, 0.671367764, -3.9935112e-05)
			CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			CFrameMon = CFrame.new(1328.92578, 87.6160507, -1374.14551, -0.548407137, 5.60746427e-09, 0.836211503, 2.07008033e-09, 1, -5.34818945e-09, -0.836211503, -1.2019602e-09, -0.548407137)
		elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman
			Ms = "Snowman [Lv. 100]"
			NaemQuest = "SnowQuest"
			LevelQuest = 2
			NameMon = "Snowman"
			ISLANDPOS = CFrame.new(1336.02625, 34.1970673, -1331.23267, 0.671367824, 0.741124272, -1.77025795e-05, 1.77025795e-05, -3.9935112e-05, -1, -0.741124272, 0.671367764, -3.9935112e-05)
			CFrameQuest = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)
			CFrameMon = CFrame.new(1046.19983, 106.109909, -1486.0741, 0.455472827, -1.03902529e-07, -0.89024967, 1.33861127e-08, 1, -1.09863016e-07, 0.89024967, 3.81226357e-08, 0.455472827)
		elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer
			Ms = "Chief Petty Officer [Lv. 120]"
			NaemQuest = "MarineQuest2"
			LevelQuest = 1
			NameMon = "Chief Petty Officer"
			ISLANDPOS = CFrame.new(-5138.81104, 23.1043854, 4103.9624, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
			CFrameQuest = CFrame.new(-5035.0835, 28.6520386, 4325.29443, 0.0243340395, -7.08064647e-08, 0.999703884, -6.36926814e-08, 1, 7.23777944e-08, -0.999703884, -6.54350671e-08, 0.0243340395)
			CFrameMon = CFrame.new(-4850.8623, 21.0520386, 4390.53516, 0.273695946, -5.40380647e-08, -0.96181643, 4.37720793e-08, 1, -4.37274998e-08, 0.96181643, -3.01326679e-08, 0.273695946)
		elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit
			Ms = "Sky Bandit [Lv. 150]"
			NaemQuest = "SkyQuest"
			LevelQuest = 1
			NameMon = "Sky Bandit"
			ISLANDPOS = CFrame.new(-4899.46777, 723.834229, -2575.20142, 0.933587551, 0, 0.358349502, 0, -1.00000048, 0, 0.358349502, 0, -0.933587909)
			CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)
			CFrameMon = CFrame.new(-4996.53906, 278.410187, -2828.92822, -0.984909654, 0, 0.173069984, 0, 1, 0, -0.173069984, 0, -0.984909654)
		elseif MyLevel == 175 or MyLevel <= 249 then 
			Ms = "Dark Master [Lv. 175]"
			NaemQuest = "SkyQuest"
			LevelQuest = 2
			NameMon = "Dark Master"
			ISLANDPOS = CFrame.new(-4899.46777, 723.834229, -2575.20142, 0.933587551, 0, 0.358349502, 0, -1.00000048, 0, 0.358349502, 0, -0.933587909)
			CFrameQuest = CFrame.new(-4841.83447, 717.669617, -2623.96436)
			CFrameMon = CFrame.new(-5220.58594, 430.693298, -2278.17456)
		elseif MyLevel == 250 or MyLevel <= 274 then 
			Ms = "Toga Warrior [Lv. 250]"
			NaemQuest = "ColosseumQuest"
			LevelQuest = 1
			NameMon = "Toga Warrior"
			ISLANDPOS = CFrame.new(-1690.47278, 10.2532501, -3086.04272, 0.74314785, -0, -0.669127226, 0, 1, -0, 0.669127226, 0, 0.74314785)
			CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762)
			CFrameMon = CFrame.new(-1779.97583, 44.6077499, -2736.35474)
		elseif MyLevel == 275 or MyLevel <= 299 then -- Gladiato
			Ms = "Gladiator [Lv. 275]"
			NaemQuest = "ColosseumQuest"
			LevelQuest = 2
			NameMon = "Gladiato"
			ISLANDPOS = CFrame.new(-1690.47278, 10.2532501, -3086.04272, 0.74314785, -0, -0.669127226, 0, 1, -0, 0.669127226, 0, 0.74314785)
			CFrameQuest = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)
			CFrameMon = CFrame.new(-1279.38416, 7.78580666, -3268.23047, -0.385674238, -3.25503358e-08, -0.922634542, 5.95089811e-10, 1, -3.55285259e-08, 0.922634542, -1.42514862e-08, -0.385674238)
		elseif MyLevel == 300 or MyLevel <= 324 then -- Military Soldier
			Ms = "Military Soldier [Lv. 300]"
			NaemQuest = "MagmaQuest"
			LevelQuest = 1
			NameMon = "Military Soldier"
			ISLANDPOS = CFrame.new(-5213.3374, 3.3397336, 8443.05957, 0.927179396, 0, 0.374617696, 0, 1, 0, -0.374617696, 0, 0.927179396)
			CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			CFrameMon = CFrame.new(-5483.29248, 9.33393669, 8413.07031, 0.909917235, -1.46153933e-09, -0.414789826, -6.77904288e-10, 1, -5.01067277e-09, 0.414789826, 4.84048535e-09, 0.909917235)
		elseif MyLevel == 325 or MyLevel <= 374 then -- Military Spy
			Ms = "Military Spy [Lv. 325]"
			NaemQuest = "MagmaQuest"
			LevelQuest = 2
			NameMon = "Military Spy"
			ISLANDPOS = CFrame.new(-5213.3374, 3.3397336, 8443.05957, 0.927179396, 0, 0.374617696, 0, 1, 0, -0.374617696, 0, 0.927179396)
			CFrameQuest = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)
			CFrameMon = CFrame.new(-5883.50049, 77.5739212, 8823.88965, 0.983678341, -1.19359456e-08, 0.179935962, -8.52669757e-09, 1, 1.12948371e-07, -0.179935962, -1.12639128e-07, 0.983678341)
		elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior
			Ms = "Fishman Warrior [Lv. 375]"
			NaemQuest = "FishmanQuest"
			LevelQuest = 1
			NameMon = "Fishman Warrior"
			CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			CFrameMon = CFrame.new(60889.6328, 18.8148994, 1432.98425, 0.345049709, 0, -0.938584328, 0, 1, 0, 0.938584328, 0, 0.345049709)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando
			Ms = "Fishman Commando [Lv. 400]"
			NaemQuest = "FishmanQuest"
			LevelQuest = 2
			NameMon = "Fishman Commando"
			CFrameQuest = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)
			CFrameMon = CFrame.new(61885.5039, 18.4828243, 1504.17896, 0.577502489, 0, -0.816389024, -0, 1.00000012, -0, 0.816389024, 0, 0.577502489)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards
			Ms = "God's Guard [Lv. 450]"
			NaemQuest = "SkyExp1Quest"
			LevelQuest = 1
			NameMon = "God's Guards"
			CFrameQuest = CFrame.new(-4721.71436, 845.277161, -1954.20105, -0.999277651, -5.56969759e-09, 0.0380011722, -4.14751478e-09, 1, 3.75035256e-08, -0.0380011722, 3.73188307e-08, -0.999277651)
			CFrameMon = CFrame.new(-4720.3291, 845.620422, -1859.63074, 0.712942302, 0, -0.701222718, -0, 1, -0, 0.701222718, 0, 0.712942302)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
			end
		elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas
			Ms = "Shanda [Lv. 475]"
			NaemQuest = "SkyExp1Quest"
			LevelQuest = 2
			NameMon = "Shandas"
			CFrameQuest = CFrame.new(-7863.63672, 5545.49316, -379.826324, 0.362120807, -1.98046344e-08, -0.93213129, 4.05822291e-08, 1, -5.48095125e-09, 0.93213129, -3.58431969e-08, 0.362120807)
			CFrameMon = CFrame.new(-7636.17285, 5545.83643, -551.851685, 0.995675743, 0, -0.0928966552, 0, 1, 0, 0.0928966552, 0, 0.995675743)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
			end
		elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad
			Ms = "Royal Squad [Lv. 525]"
			NaemQuest = "SkyExp2Quest"
			LevelQuest = 1
			NameMon = "Royal Squad"
			CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			CFrameMon = CFrame.new(-7654.80615, 5607.22168, -1497.61304, 0.655299842, -1.01422131e-07, -0.75536871, 8.79199114e-09, 1, -1.26641098e-07, 0.75536871, 7.63466659e-08, 0.655299842)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
			end
		elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier
			Ms = "Royal Soldier [Lv. 550]"
			NaemQuest = "SkyExp2Quest"
			LevelQuest = 2
			NameMon = "Royal Soldier"
			CFrameQuest = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)
			CFrameMon = CFrame.new(-7966.58252, 5637.42529, -1744.18347, 0.116254926, -8.58390649e-07, -0.99321878, 2.4797064e-08, 1, -8.61348838e-07, 0.99321878, 7.55070602e-08, 0.116254926)
			if _G.AutoFarm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 1000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
			end
		elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate
			Ms = "Galley Pirate [Lv. 625]"
			NaemQuest = "FountainQuest"
			LevelQuest = 1
			NameMon = "Galley Pirate"
			ISLANDPOS = CFrame.new(5454.30957, 136.634079, 4622.60059, 0.74314785, 0, -0.669127226, 0, -1, -0, -0.669127226, 0, -0.74314785)
			CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			CFrameMon = CFrame.new(5684.73096, 38.8443985, 3927.60498, 0.999752343, -6.81844494e-06, -0.0222478025, 5.87542536e-06, 1, -4.24524987e-05, 0.0222478025, 4.2311276e-05, 0.999752343)
		elseif MyLevel >= 650 then -- Galley Captain
			Ms = "Galley Captain [Lv. 650]"
			NaemQuest = "FountainQuest"
			LevelQuest = 2
			NameMon = "Galley Captain"
			ISLANDPOS = CFrame.new(5454.30957, 136.634079, 4622.60059, 0.74314785, 0, -0.669127226, 0, -1, -0, -0.669127226, 0, -0.74314785)
			CFrameQuest = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)
			CFrameMon = CFrame.new(5658.5752, 38.5361786, 4928.93506, -0.996873081, 2.12391046e-06, -0.0790185928, 2.16989656e-06, 1, -4.96097414e-07, 0.0790185928, -6.66008248e-07, -0.996873081)
		end
	end
	
	if NewWorld then
		Nonquest = false
		if MyLevel == 700 or MyLevel <= 724 then -- Raider [Lv. 700]
			Ms = "Raider [Lv. 700]"
			NaemQuest = "Area1Quest"
			LevelQuest = 1
			NameMon = "Raider"
			CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
			CFrameMon = CFrame.new(-737.026123, 10.1748352, 2392.57959, 0.272128761, 0, -0.962260842, -0, 1, -0, 0.962260842, 0, 0.272128761)
		elseif MyLevel == 725 or MyLevel <= 774 then -- Mercenary [Lv. 725]
			Ms = "Mercenary [Lv. 725]"
			NaemQuest = "Area1Quest"
			LevelQuest = 2
			NameMon = "Mercenary"
			CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
			CFrameMon = CFrame.new(-1022.21271, 72.9855194, 1891.39148, -0.990782857, 0, -0.135460541, 0, 1, 0, 0.135460541, 0, -0.990782857)
		elseif MyLevel == 775 or MyLevel <= 799 then -- Swan Pirate [Lv. 775]
			Ms = "Swan Pirate [Lv. 775]"
			NaemQuest = "Area2Quest"
			LevelQuest = 1
			NameMon = "Swan Pirate"
			CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
			CFrameMon = CFrame.new(976.467651, 111.174057, 1229.1084, 0.00852567982, -4.73897828e-08, -0.999963999, 1.12251888e-08, 1, -4.7295778e-08, 0.999963999, -1.08215579e-08, 0.00852567982)
		elseif MyLevel == 800 or MyLevel <= 874 then -- Factory Staff [Lv. 800]
			Ms = "Factory Staff [Lv. 800]"
			NaemQuest = "Area2Quest"
			LevelQuest = 2
			NameMon = "Factory Staff"
			CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
			CFrameMon = CFrame.new(336.74585, 73.1620483, -224.129272, 0.993632793, 3.40154607e-08, 0.112668738, -3.87658332e-08, 1, 3.99718729e-08, -0.112668738, -4.40850592e-08, 0.993632793)
		elseif MyLevel == 875 or MyLevel <= 899 then -- Marine Lieutenant [Lv. 875]
			Ms = "Marine Lieutenant [Lv. 875]"
			NaemQuest = "MarineQuest3"
			LevelQuest = 1
			NameMon = "Marine Lieutenant"
			CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
			CFrameMon = CFrame.new(-2842.69922, 72.9919434, -2901.90479, -0.762281299, 0, -0.64724648, 0, 1.00000012, 0, 0.64724648, 0, -0.762281299)
		elseif MyLevel == 900 or MyLevel <= 949 then -- Marine Captain [Lv. 900]
			Ms = "Marine Captain [Lv. 900]"
			NaemQuest = "MarineQuest3"
			LevelQuest = 2
			NameMon = "Marine Captain"
			CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
			CFrameMon = CFrame.new(-1814.70313, 72.9919434, -3208.86621, -0.900422215, 7.93464423e-08, -0.435017526, 3.68856199e-08, 1, 1.06050372e-07, 0.435017526, 7.94441988e-08, -0.900422215)
		elseif MyLevel == 950 or MyLevel <= 974 then -- Zombie [Lv. 950]
			Ms = "Zombie [Lv. 950]"
			NaemQuest = "ZombieQuest"
			LevelQuest = 1
			NameMon = "Zombie"
			CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
			CFrameMon = CFrame.new(-5649.23438, 126.0578, -737.773743, 0.355238914, -8.10359282e-08, 0.934775114, 1.65461245e-08, 1, 8.04023372e-08, -0.934775114, -1.3095117e-08, 0.355238914)
		elseif MyLevel == 975 or MyLevel <= 999 then -- Vampire [Lv. 975]
			Ms = "Vampire [Lv. 975]"
			NaemQuest = "ZombieQuest"
			LevelQuest = 2
			NameMon = "Vampire"
			CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
			CFrameMon = CFrame.new(-6030.32031, 0.4377408, -1313.5564, -0.856965423, 3.9138893e-08, -0.515373945, -1.12178942e-08, 1, 9.45958547e-08, 0.515373945, 8.68467822e-08, -0.856965423)
		elseif MyLevel == 1000 or MyLevel <= 1049 then -- Snow Trooper [Lv. 1000] **
			Ms = "Snow Trooper [Lv. 1000]"
			NaemQuest = "SnowMountainQuest"
			LevelQuest = 1
			NameMon = "Snow Trooper"
			CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
			CFrameMon = CFrame.new(621.003418, 391.361053, -5335.43604, 0.481644779, 0, 0.876366913, 0, 1, 0, -0.876366913, 0, 0.481644779)
		elseif MyLevel == 1050 or MyLevel <= 1099 then -- Winter Warrior [Lv. 1050]
			Ms = "Winter Warrior [Lv. 1050]"
			NaemQuest = "SnowMountainQuest"
			LevelQuest = 2
			NameMon = "Winter Warrior"
			CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
			CFrameMon = CFrame.new(1295.62683, 429.447784, -5087.04492, -0.698032081, -8.28980049e-08, -0.71606636, -1.98835952e-08, 1, -9.63858184e-08, 0.71606636, -5.30424877e-08, -0.698032081)
		elseif MyLevel == 1100 or MyLevel <= 1124 then -- Lab Subordinate [Lv. 1100]
			Ms = "Lab Subordinate [Lv. 1100]"
			NaemQuest = "IceSideQuest"
			LevelQuest = 1
			NameMon = "Lab Subordinate"
			CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
			CFrameMon = CFrame.new(-5769.2041, 37.9288292, -4468.38721, -0.569419742, -2.49055017e-08, 0.822046936, -6.96206541e-08, 1, -1.79282633e-08, -0.822046936, -6.74401548e-08, -0.569419742)
		elseif MyLevel == 1125 or MyLevel <= 1174 then -- Horned Warrior [Lv. 1125]
			Ms = "Horned Warrior [Lv. 1125]"
			NaemQuest = "IceSideQuest"
			LevelQuest = 2
			NameMon = "Horned Warrior"
			CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
			CFrameMon = CFrame.new(-6401.27979, 15.9775667, -5948.24316, 0.388303697, 0, -0.921531856, 0, 1, 0, 0.921531856, 0, 0.388303697)
		elseif MyLevel == 1175 or MyLevel <= 1199 then -- Magma Ninja [Lv. 1175]
			Ms = "Magma Ninja [Lv. 1175]"
			NaemQuest = "FireSideQuest"
			LevelQuest = 1
			NameMon = "Magma Ninja"
			CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
			CFrameMon = CFrame.new(-5466.06445, 57.6952019, -5837.42822, -0.988835871, 0, -0.149006829, 0, 1, 0, 0.149006829, 0, -0.988835871)
		elseif MyLevel == 1200 or MyLevel <= 1249 then 
			Ms = "Lava Pirate [Lv. 1200]"
			NaemQuest = "FireSideQuest"
			LevelQuest = 2
			NameMon = "Lava Pirate"
			CFrameQuest = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)
			CFrameMon = CFrame.new(-5169.71729, 34.1234779, -4669.73633, -0.196780294, 0, 0.98044765, 0, 1.00000012, -0, -0.98044765, 0, -0.196780294)
		elseif MyLevel == 1250 or MyLevel <= 1274 then 
			Ms = "Ship Deckhand [Lv. 1250]"
			NaemQuest = "ShipQuest1"
			LevelQuest = 1
			NameMon = "Ship Deckhand"
			CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
			CFrameMon = CFrame.new(1163.80872, 138.288452, 33058.4258, -0.998580813, 5.49076979e-08, -0.0532564968, 5.57436763e-08, 1, -1.42118655e-08, 0.0532564968, -1.71604082e-08, -0.998580813)
		elseif MyLevel == 1275 or MyLevel <= 1299 then 
			Ms = "Ship Engineer [Lv. 1275]"
			NaemQuest = "ShipQuest1"
			LevelQuest = 2
			NameMon = "Ship Engineer"
			CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)
			CFrameMon = CFrame.new(921.30249023438, 125.400390625, 32937.34375)
		elseif MyLevel == 1300 or MyLevel <= 1324 then 
			Ms = "Ship Steward [Lv. 1300]"
			NaemQuest = "ShipQuest2"
			LevelQuest = 1
			NameMon = "Ship Steward"
			CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
			CFrameMon = CFrame.new(917.96057128906, 136.89932250977, 33343.4140625)
		elseif MyLevel == 1325 or MyLevel <= 1349 then 
			Ms = "Ship Officer [Lv. 1325]"
			NaemQuest = "ShipQuest2"
			LevelQuest = 2
			NameMon = "Ship Officer"
			CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)
			CFrameMon = CFrame.new(944.44964599609, 181.40081787109, 33278.9453125)
		elseif MyLevel == 1350 or MyLevel <= 1374 then 
			Ms = "Arctic Warrior [Lv. 1350]"
			NaemQuest = "FrostQuest"
			LevelQuest = 1
			NameMon = "Arctic Warrior"
			CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
			CFrameMon = CFrame.new(5878.23486, 81.3886948, -6136.35596, -0.451037169, 2.3908234e-07, 0.892505825, -1.08168464e-07, 1, -3.22542007e-07, -0.892505825, -2.4201924e-07, -0.451037169)
		elseif MyLevel == 1375 or MyLevel <= 1424 then -- Snow Lurker [Lv. 1375]
			Ms = "Snow Lurker [Lv. 1375]"
			NaemQuest = "FrostQuest"
			LevelQuest = 2
			NameMon = "Snow Lurker"
			CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
			CFrameMon = CFrame.new(5513.36865, 60.546711, -6809.94971, -0.958693981, -1.65617333e-08, 0.284439981, -4.07668654e-09, 1, 4.44854642e-08, -0.284439981, 4.14883701e-08, -0.958693981)
		elseif MyLevel == 1425 or MyLevel <= 1449 then -- Sea Soldier [Lv. 1425]
			Ms = "Sea Soldier [Lv. 1425]"
			NaemQuest = "ForgottenQuest"
			LevelQuest = 1
			NameMon = "Sea Soldier"
			CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
			CFrameMon = CFrame.new(-3115.78223, 63.8785706, -9808.38574, -0.913427353, 3.11199457e-08, 0.407000452, 7.79564235e-09, 1, -5.89660658e-08, -0.407000452, -5.06883708e-08, -0.913427353)
		elseif MyLevel >= 1450 then -- Water Fighter [Lv. 1450]
			Ms = "Water Fighter [Lv. 1450]"
			NaemQuest = "ForgottenQuest"
			LevelQuest = 2
			NameMon = "Water Fighter"
			CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
			CFrameMon = CFrame.new(-3212.99683, 263.809296, -10551.8799, 0.742111444, -5.59139615e-08, -0.670276582, 1.69155214e-08, 1, -6.46908234e-08, 0.670276582, 3.66697037e-08, 0.742111444)
		end
	end
	--w3q
	if ThreeWorld then
		if MyLevel == 1500 or MyLevel <= 1524 then
			Ms = "Pirate Millionaire [Lv. 1500]"
			NaemQuest = "PiratePortQuest"
			LevelQuest = 1
			NameMon = "Pirate Millionaire"
			ISLANDPOS = CFrame.new(-627.095825, 68.8230591, 5444.96973, 1.2755394e-05, 0.965938866, 0.258770198, -0.99999994, 1.2755394e-05, 1.66893005e-06, -1.66893005e-06, -0.258770198, 0.965938926)
			CFrameQuest = CFrame.new(-288.5224, 43.8218307, 5580.43408, -0.999959528, -8.31576159e-08, 0.0089966096, -8.37007832e-08, 1, -5.99984915e-08, -0.0089966096, -6.07490875e-08, -0.999959528)
			CFrameMon = CFrame.new(-30.9287148, 44.1632271, 5626.03564, -0.984395564, 6.69860825e-08, 0.175970018, 6.64483224e-08, 1, -8.94841801e-09, -0.175970018, 2.88413116e-09, -0.984395564)
		elseif MyLevel == 1525 or MyLevel <= 1624 then
			Ms = "Pistol Billionaire [Lv. 1525]"
			NaemQuest = "PiratePortQuest"
			LevelQuest = 2
			NameMon = "Pistol Billionaire"
			ISLANDPOS = CFrame.new(-627.095825, 68.8230591, 5444.96973, 1.2755394e-05, 0.965938866, 0.258770198, -0.99999994, 1.2755394e-05, 1.66893005e-06, -1.66893005e-06, -0.258770198, 0.965938926)
			CFrameQuest = CFrame.new(-288.5224, 43.8218307, 5580.43408, -0.999959528, -8.31576159e-08, 0.0089966096, -8.37007832e-08, 1, -5.99984915e-08, -0.0089966096, -6.07490875e-08, -0.999959528)
			CFrameMon = CFrame.new(-27.2507839, 73.7850037, 6110.73438, 0.94821614, 2.10991633e-08, -0.317625821, -1.09169083e-08, 1, 3.3837221e-08, 0.317625821, -2.86175066e-08, 0.94821614)
		elseif MyLevel == 1625 or MyLevel <= 1649 then
			Ms = "Female Islander [Lv. 1625]"
			NaemQuest = "AmazonQuest2"
			LevelQuest = 1
			NameMon = "Female Islander"
			ISLANDPOS = CFrame.new(5406.33643, 655.403625, 594.461853, -0.417002439, -0.417307526, -0.807442605, -0.388651222, 0.884923458, -0.256633431, 0.821619928, 0.206796795, -0.531202316)
			CFrameQuest = CFrame.new(5447.18555, 601.684814, 750.161804, -0.0492943414, 5.47278347e-08, -0.998784304, 1.11371856e-10, 1, 5.4788952e-08, 0.998784304, 2.5895488e-09, -0.0492943414)
			CFrameMon = CFrame.new(5635.42676, 782.124878, 857.546997, -0.990593493, 2.96959286e-07, 0.136837229, 1.91843185e-07, 1, -7.81369522e-07, -0.136837229, -7.47768354e-07, -0.990593493)
		elseif MyLevel == 1650 or MyLevel <= 1724 then
			Ms = "Giant Islander [Lv. 1650]"
			NaemQuest = "AmazonQuest2"
			LevelQuest = 2
			NameMon = "Giant Islander"
			ISLANDPOS = CFrame.new(5406.33643, 655.403625, 594.461853, -0.417002439, -0.417307526, -0.807442605, -0.388651222, 0.884923458, -0.256633431, 0.821619928, 0.206796795, -0.531202316)
			CFrameQuest = CFrame.new(5447.18555, 601.684814, 750.161804, -0.0492943414, 5.47278347e-08, -0.998784304, 1.11371856e-10, 1, 5.4788952e-08, 0.998784304, 2.5895488e-09, -0.0492943414)
			CFrameMon = CFrame.new(4803.53516, 601.884644, 21.1627445, -0.945538223, -9.67994662e-09, -0.3255108, 9.0386223e-09, 1, -5.59929489e-08, 0.3255108, -5.58856534e-08, -0.945538223)
		elseif MyLevel == 1700 or MyLevel <= 1724 then
			Ms = "Marine Commodore [Lv. 1700]"
			NaemQuest = "MarineTreeIsland"
			LevelQuest = 1
			NameMon = "Marine Commodore"
			ISLANDPOS = CFrame.new(2661.02368, 42.0330811, -6470.3667, 0.365655482, 0.720300019, 0.589461029, -0.890152395, 0.455640078, -0.00459471345, -0.271891713, -0.523029923, 0.807783842)
			CFrameQuest = CFrame.new(2181.47559, 29.3805466, -6739.75488, 0.972898781, 3.13111634e-08, -0.231231317, -4.68299923e-08, 1, -6.1625208e-08, 0.231231317, 7.07836563e-08, 0.972898781)
			CFrameMon = CFrame.new(2879.39746, 73.1276932, -7823.78613, 0.987131357, 2.83766557e-08, -0.159911677, -3.10919681e-08, 1, -1.4477993e-08, 0.159911677, 1.92636502e-08, 0.987131357)
		elseif MyLevel >= 1725 and MyLevel <= 1774 then
			Ms = "Marine Rear Admiral [Lv. 1725]"
			NaemQuest = "MarineTreeIsland"
			LevelQuest = 2
			NameMon = "Marine Rear Admiral"
			ISLANDPOS = CFrame.new(2661.02368, 42.0330811, -6470.3667, 0.365655482, 0.720300019, 0.589461029, -0.890152395, 0.455640078, -0.00459471345, -0.271891713, -0.523029923, 0.807783842)
			CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
			CFrameMon = CFrame.new(3684.00586, 160.514099, -7128.87354, -0.570743263, 0, 0.821128547, 0, 1, -0, -0.821128547, 0, -0.570743)
		elseif MyLevel >= 1775 and MyLevel <= 1799 then
			Ms = "Fishman Raider [Lv. 1775]"
			NaemQuest = "DeepForestIsland3"
			LevelQuest = 1
			NameMon = "Fishman Raider"
			ISLANDPOS = CFrame.new(-11478.541, 333.637207, -10379.043, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
			CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
			CFrameMon = CFrame.new(-10364.5967, 332.095978, -8353.88672, 0.923343658, 1.48868907e-07, -0.383972943, -5.46038343e-08, 1, 2.56400227e-07, 0.383972943, -2.15779068e-07, 0.923343658)
		elseif MyLevel >= 1800 and MyLevel <= 1824 then
			Ms = "Fishman Captain [Lv. 1800]"
			NaemQuest = "DeepForestIsland3"
			LevelQuest = 2
			NameMon = "Fishman Captain"
			ISLANDPOS = CFrame.new(-11478.541, 333.637207, -10379.043, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
			CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
			CFrameMon = CFrame.new(-10973.4004, 331.752991, -8883.54004, 0.678526163, 1.54081761e-08, 0.734575987, 4.41213963e-08, 1, -6.17304465e-08, -0.734575987, 7.42963024e-08, 0.678526163)
		elseif MyLevel >= 1825 and MyLevel <= 1849 then
			Ms = "Forest Pirate [Lv. 1825]"
			NaemQuest = "DeepForestIsland"
			LevelQuest = 1
			NameMon = "Forest Pirate"
			ISLANDPOS = CFrame.new(-12550.3164, 332.712402, -7492.83398, 1, 0, 0, 0, 1, 0, 0, 0, 1)
			CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
			CFrameMon = CFrame.new(-13594.2119, 332.368225, -7930.59912, 0.955262423, 2.26471002e-08, -0.295761019, -1.30703626e-08, 1, 3.43570647e-08, 0.295761019, -2.89543038e-08, 0.955262423)
		elseif MyLevel == 1850 or MyLevel <= 1899 then
			Ms = "Mythological Pirate [Lv. 1850]"
			NaemQuest = "DeepForestIsland"
			LevelQuest = 2
			NameMon = "Mythological Pirate"
			ISLANDPOS = CFrame.new(-12550.3164, 332.712402, -7492.83398, 1, 0, 0, 0, 1, 0, 0, 0, 1)
			CFrameQuest = CFrame.new(-13230.9658, 332.413177, -7624.93457, 0.455187887, -8.75483792e-08, 0.890395403, -4.99329189e-10, 1, 9.85805499e-08, -0.890395403, -4.53172717e-08, 0.455187887)
			CFrameMon = CFrame.new(-13654.9893, 469.822784, -6970.78369, 0.952340543, 2.57623842e-08, -0.305036813, 8.97913299e-09, 1, 1.1248995e-07, 0.305036813, -1.09867713e-07, 0.952340543)
		elseif MyLevel == 1900 or MyLevel <= 1924 then
			Ms = "Jungle Pirate [Lv. 1900]"
			NaemQuest = "DeepForestIsland2"
			LevelQuest = 1
			NameMon = "Jungle Pirate"
			ISLANDPOS = CFrame.new(-11478.541, 333.637207, -10379.043, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
			CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
			CFrameMon = CFrame.new(-11775.0195, 332.071625, -10628.4648, 0.0879710168, 3.94232338e-05, 0.996122956, 6.06110871e-06, 1, -4.01119505e-05, -0.996122956, 9.56629265e-06, 0.0879710168)
		elseif MyLevel <= 1974 then
			Ms = "Musketeer Pirate [Lv. 1925]"
			NaemQuest = "DeepForestIsland2"
			LevelQuest = 2
			NameMon = "Musketeer Pirate"
			ISLANDPOS = CFrame.new(-11478.541, 333.637207, -10379.043, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
			CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
			CFrameMon = CFrame.new(-13305.2227, 391.878998, -9774.5791, 0.373675853, 1.90769788e-05, 0.927559018, 7.93608251e-07, 1, -2.08865713e-05, -0.927559018, 8.54091832e-06, 0.373675853)
		elseif MyLevel <= 1999 then
			Ms = "Reborn Skeleton [Lv. 1975]"
			NaemQuest = "HauntedQuest1"
			LevelQuest = 1
			NameMon = "Reborn Skeleton"
			ISLANDPOS = CFrame.new(-9538.98145, 140.898499, 5513.27588, 0.998163939, 0, -0.0605702288, 0, 1, 0, 0.0605702288, 0, 0.998163939)
			CFrameQuest = CFrame.new(-9480.87012, 142.43811, 5566.2002, -0.00248356303, -5.78340327e-08, -0.999996901, -2.37339948e-09, 1, -5.78283164e-08, 0.999996901, 2.2297717e-09, -0.00248356303)
			CFrameMon = CFrame.new(-8759.74316, 142.43811, 6018.50879, 0.995956361, 1.53021293e-08, -0.089838393, -1.4131051e-08, 1, 1.3671424e-08, 0.089838393, -1.23466313e-08, 0.995956361)
		elseif MyLevel <= 2024 then
			Ms = "Living Zombie [Lv. 2000]"
			NaemQuest = "HauntedQuest1"
			LevelQuest = 2
			NameMon = "Living Zombie"
			ISLANDPOS = CFrame.new(-9538.98145, 140.898499, 5513.27588, 0.998163939, 0, -0.0605702288, 0, 1, 0, 0.0605702288, 0, 0.998163939)
			CFrameQuest = CFrame.new(-9480.87012, 142.43811, 5566.2002, -0.00248356303, -5.78340327e-08, -0.999996901, -2.37339948e-09, 1, -5.78283164e-08, 0.999996901, 2.2297717e-09, -0.00248356303)
			CFrameMon = CFrame.new(-10147.8926, 139.959961, 5972.49316, 0.917640984, 0.000120363518, -0.397410452, -1.50241667e-05, 0.99999994, 0.000268177944, 0.397410452, -0.000240120396, 0.917640984)
		elseif MyLevel <= 2049 then
			Ms = "Demonic Soul [Lv. 2025]"
			NaemQuest = "HauntedQuest2"
			LevelQuest = 1
			NameMon = "Demonic Soul"
			ISLANDPOS = CFrame.new(-9538.98145, 140.898499, 5513.27588, 0.998163939, 0, -0.0605702288, 0, 1, 0, 0.0605702288, 0, 0.998163939)
			CFrameQuest = CFrame.new(-9514.59668, 172.43811, 6077.85791, -0.025661787, -1.8103858e-08, 0.999670684, -2.63411728e-08, 1, 1.74336368e-08, -0.999670684, -2.58851198e-08, -0.025661787)
			CFrameMon = CFrame.new(-9502.1377, 172.43811, 6153.22559, 0.998965919, 8.14885152e-06, -0.0454591215, -3.61834987e-06, 1, 9.97435855e-05, 0.0454591215, -9.94759685e-05, 0.998965919)
		elseif MyLevel <= 2074 then
			Ms = "Posessed Mummy [Lv. 2050]"
			NaemQuest = "HauntedQuest2"
			LevelQuest = 2
			NameMon = "Posessed Mummy"
			ISLANDPOS = CFrame.new(-9538.98145, 140.898499, 5513.27588, 0.998163939, 0, -0.0605702288, 0, 1, 0, 0.0605702288, 0, 0.998163939)
			CFrameQuest = CFrame.new(-9514.59668, 172.43811, 6077.85791, -0.025661787, -1.8103858e-08, 0.999670684, -2.63411728e-08, 1, 1.74336368e-08, -0.999670684, -2.58851198e-08, -0.025661787)
			CFrameMon = CFrame.new(-9579.89551, 6.1257925, 6194.25684, -0.994989395, -9.60423137e-08, -0.0999803767, -9.48566452e-08, 1, -1.66128302e-08, 0.0999803767, -7.04578706e-09, -0.994989395)
		elseif MyLevel <= 2099 then
			Ms = "Peanut Scout [Lv. 2075]"
			NaemQuest = "NutsIslandQuest"
			LevelQuest = 1
			NameMon = "Peanut Scout"
			ISLANDPOS = CFrame.new(-2120.65259, 42.5805931, -10177.0498, 0.769644201, 0, 0.638473034, 0, 1, 0, -0.638473034, 0, 0.769644201)
			CFrameQuest = CFrame.new(-2105.16504, 38.4474411, -10193.708, 0.786417007, -1.17257759e-08, 0.617695928, -2.06460027e-09, 1, 2.16116245e-08, -0.617695928, -1.82710451e-08, 0.786417007)
			CFrameMon = CFrame.new(-2235.11646, 88.5827332, -10398.1094, -0.832571924, -2.27626842e-07, -0.553917289, -2.47123836e-07, 1, -3.94977633e-08, 0.553917289, 1.04001408e-07, -0.832571924)
		elseif MyLevel <= 2124 then
			Ms = "Peanut President [Lv. 2100]"
			NaemQuest = "NutsIslandQuest"
			LevelQuest = 2
			NameMon = "Peanut President"
			ISLANDPOS = CFrame.new(-2120.65259, 42.5805931, -10177.0498, 0.769644201, 0, 0.638473034, 0, 1, 0, -0.638473034, 0, 0.769644201)
			CFrameQuest = CFrame.new(-2105.16504, 38.4474411, -10193.708, 0.786417007, -1.17257759e-08, 0.617695928, -2.06460027e-09, 1, 2.16116245e-08, -0.617695928, -1.82710451e-08, 0.786417007)
			CFrameMon = CFrame.new(-2235.11646, 88.5827332, -10398.1094, -0.832571924, -2.27626842e-07, -0.553917289, -2.47123836e-07, 1, -3.94977633e-08, 0.553917289, 1.04001408e-07, -0.832571924)
		elseif MyLevel <= 2149 then
			Ms = "Ice Cream Chef [Lv. 2125]"
			NaemQuest = "IceCreamIslandQuest"
			LevelQuest = 1
			NameMon = "Ice Cream Chef"
			ISLANDPOS = CFrame.new(-779.823547, 65.9448471, -10919.1182, -0.786368072, 0, 0.617758334, 0, 1, 0, -0.617758334, 0, -0.786368072)
			CFrameQuest = CFrame.new(-820.017212, 66.1628113, -10965.9189, 0.764226615, 5.82622519e-08, -0.644947827, -5.33253548e-08, 1, 2.71488592e-08, 0.644947827, 1.36441916e-08, 0.764226615)
			CFrameMon = CFrame.new(-830.885742, 144.121704, -11091.0156, -0.329080194, 5.0881642e-08, 0.944301963, 6.449892e-08, 1, -3.14055519e-08, -0.944301963, 5.05715114e-08, -0.329080194)
		elseif MyLevel <= 2199 then 
			Ms = "Ice Cream Commander [Lv. 2150]"
			NaemQuest = "IceCreamIslandQuest"
			LevelQuest = 2
			NameMon = "Ice Cream Commander"
			ISLANDPOS = CFrame.new(-779.823547, 65.9448471, -10919.1182, -0.786368072, 0, 0.617758334, 0, 1, 0, -0.617758334, 0, -0.786368072)
			CFrameQuest = CFrame.new(-820.017212, 66.1628113, -10965.9189, 0.764226615, 5.82622519e-08, -0.644947827, -5.33253548e-08, 1, 2.71488592e-08, 0.644947827, 1.36441916e-08, 0.764226615)
			CFrameMon = CFrame.new(-830.885742, 144.121704, -11091.0156, -0.329080194, 5.0881642e-08, 0.944301963, 6.449892e-08, 1, -3.14055519e-08, -0.944301963, 5.05715114e-08, -0.329080194)
		elseif MyLevel <= 2224 then
			Ms = "Cookie Crafter [Lv. 2200]"
			NaemQuest = "CakeQuest1"
			LevelQuest = 1
			NameMon = "Cookie Crafter"
			ISLANDPOS = CFrame.new(-2099.33154, 66.9970703, -12128.585, 0.997561574, 0, 0.0697919354, 0, 1, 0, -0.0697919354, 0, 0.997561574)
			CFrameQuest = CFrame.new(-2021.40833, 36.5925713, -12029.417, 0.940247118, -1.22227597e-08, 0.340492785, 1.01512621e-08, 1, 7.86525867e-09, -0.340492785, -3.93885546e-09, 0.940247118)
			CFrameMon = CFrame.new(-2123.25659, 111.625145, -11933.5938, 0.908894241, 1.12659599e-07, 0.417026669, -1.22163556e-07, 1, -3.89866006e-09, -0.417026669, -4.74019899e-08, 0.908894241)
		elseif MyLevel <= 2249 then
			Ms = "Cake Guard [Lv. 2225]"
			NaemQuest = "CakeQuest1"
			LevelQuest = 2
			NameMon = "Cake Guard"
			ISLANDPOS = CFrame.new(-2099.33154, 66.9970703, -12128.585, 0.997561574, 0, 0.0697919354, 0, 1, 0, -0.0697919354, 0, 0.997561574)
			CFrameQuest = CFrame.new(-2021.40833, 36.5925713, -12029.417, 0.940247118, -1.22227597e-08, 0.340492785, 1.01512621e-08, 1, 7.86525867e-09, -0.340492785, -3.93885546e-09, 0.940247118)
			CFrameMon = CFrame.new(-1559.19348, 89.0205154, -12584.1943, 0.843241334, -3.36266659e-08, 0.537535131, -8.12348055e-09, 1, 7.53006049e-08, -0.537535131, -6.78632404e-08, 0.843241334)
		elseif MyLevel <= 2274 then
			Ms = "Baking Staff [Lv. 2250]"
			NaemQuest = "CakeQuest2"
			LevelQuest = 1
			NameMon = "Baking Staff"
			ISLANDPOS = CFrame.new(-2099.33154, 66.9970703, -12128.585, 0.997561574, 0, 0.0697919354, 0, 1, 0, -0.0697919354, 0, 0.997561574)
			CFrameQuest = CFrame.new(-1927.9281, 36.6931343, -12842.1777, -0.999484241, -1.02355763e-07, 0.0321136042, -1.04146537e-07, 1, -5.40911991e-08, -0.0321136042, -5.74078207e-08, -0.999484241)
			CFrameMon = CFrame.new(-1819.08472, 93.1109695, -12884.9492, -0.761556745, -7.28589171e-08, 0.64809829, -7.16595849e-08, 1, 2.82149788e-08, -0.64809829, -2.49551455e-08, -0.761556745)
		elseif MyLevel > 2275 then
			Ms = "Head Baker [Lv. 2275]"
			NaemQuest = "CakeQuest2"
			LevelQuest = 2
			NameMon = "Head Baker"
			ISLANDPOS = CFrame.new(-2099.33154, 66.9970703, -12128.585, 0.997561574, 0, 0.0697919354, 0, 1, 0, -0.0697919354, 0, 0.997561574)
			CFrameQuest = CFrame.new(-1927.9281, 36.6931343, -12842.1777, -0.999484241, -1.02355763e-07, 0.0321136042, -1.04146537e-07, 1, -5.40911991e-08, -0.0321136042, -5.74078207e-08, -0.999484241)
			CFrameMon = CFrame.new(-2103.4707, 101.819008, -12790.4863, 0.914387882, 1.96595877e-08, 0.404839277, 1.38365364e-09, 1, -5.16866443e-08, -0.404839277, 4.78217963e-08, 0.914387882)
		end
	end
end
function EquipWeapon(ToolSe)
    pcall(function()
        if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
            local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
        end
    end)
end
function TweenFarm(gotoCFrame)
	pcall(function()
		game.Players.LocalPlayer.Character.Humanoid.Sit = false
		game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
	end)
	if (game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').Position - gotoCFrame.Position).Magnitude <= 200 then
		pcall(function() 
			tween:Cancel()
		end)
		game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').CFrame = gotoCFrame
	else
		local tween_s = game:service"TweenService"
		local info = TweenInfo.new((game:GetService("Players")["LocalPlayer"].Character:WaitForChild('HumanoidRootPart').Position - gotoCFrame.Position).Magnitude/300, Enum.EasingStyle.Linear)
		local tween, err = pcall(function()
			tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = gotoCFrame})
			tween:Play()
		end)
		if not tween then return err end
	end
end
Sector1:AddToggle("Auto Farm",_G.Save['AutoFarm'],function(value)
    _G.AutoFarm = value
    _G.Save['AutoFarm'] = value
    SaveSetting()
    if value == false then
        TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
    end
end)
Sector1:AddToggle("Fast Farm (Beta)",_G.Save['FastFarm'],function(value)
    _G.FastFarm = value
    _G.Save['FastFarm'] = value
    SaveSetting()
    if value == false then
        TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
	end
end)
Sector1:AddToggle("Bring Mon (Bug)",true,function(value)
	getgenv().Number1 = value 
    
end)



spawn(function()
	while task.wait(.0000001) do
		if getgenv().Number1 then
			pcall(function()
				CheckLevel()
				for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
					if getgenv().Number1 and UseMagnet and v.Name == Ms and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and (Ms == "Factory Staff [Lv. 800]" or Ms == "Monkey [Lv. 14]" or Ms == "Dragon Crew Warrior [Lv. 1575]" or Ms == "Dragon Crew Archer [Lv. 1600]" or Ms == "Head Baker [Lv. 2275]" or Ms == "Baking Staff [Lv. 2250]" or Ms == "Cake Guard [Lv. 2225]") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 225 then
						v.HumanoidRootPart.CFrame = CFrameMon
						v.Humanoid:ChangeState(14)
						v.Humanoid.WalkSpeed = 0
						v.HumanoidRootPart.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
					elseif getgenv().Number1 and UseMagnet and v.Name == Ms and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and string.find(Ms, "Fishman") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 170 then
						v.HumanoidRootPart.CFrame = CFrameMon
						v.Humanoid:ChangeState(14)
						v.Humanoid.WalkSpeed = 0
						v.HumanoidRootPart.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
					elseif getgenv().Number1 and UseMagnet and v.Name == Ms and v.Humanoid.Health > 0 and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 270 then
						v.HumanoidRootPart.CFrame = CFrameMon
						v.Humanoid:ChangeState(14)
						v.Humanoid.WalkSpeed = 0
						v.HumanoidRootPart.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
					end
				end
			end
            )
		end
	end
end
)
Sector1:AddToggle("AutoNewWorld",_G.Save['AutoNewWorld'],function(value)
    _G.AutoNewWorld = value
	_G.Save['AutoNewWorld'] = value
    SaveSetting()
end)
Sector1:AddToggle("AutoThirdWorld",_G.Save['Autothird'],function(value)
    _G.Autothird = value
	_G.Save['Autothird'] = value
    SaveSetting()
end)

spawn(function()
	while wait() do
		if _G.Autothird then
			local MyLevel = game.Players.localPlayer.Data.Level.Value
			if MyLevel >= 1500 and NewWorld and _G.Autothird then
				if Auto_Farm then
					MainAutoFarmFunction:Stop()
				end
				if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 3 then
					if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess ~= nil then
						local args = {
							[1] = "TravelZou" -- OLD WORLD to NEW WORLD
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						
						if game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("ZQuestProgress", "Check") == 0 then
							if game.Workspace.Enemies:FindFirstChild("rip_indra [Lv. 1500] [Boss]") then 	
								for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
									if v.Name == "rip_indra [Lv. 1500] [Boss]" and v:FindFirstChild("Humanoid")and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
										repeat wait()
											if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
												Farmtween = toTarget(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
											elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
												if Farmtween then
													Farmtween:Stop()
												end
												EquipWeapon(SelectToolWeapon)
												Usefastattack = true
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
												Click()
											end 
										until not _G.Autothird or not v.Parent or v.Humanoid.Health <= 0 
										wait(.5)
										asmrqq = 2
										repeat wait()
											local args = {
												[1] = "TravelZou" -- OLD WORLD to NEW WORLD
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										until asmrqq == 1
										Usefastattack = false
									end
								end
							else -- SlashHit : rbxassetid://2453605589
								local string_1 = "ZQuestProgress";
								local string_2 = "Check";
								local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
								Target:InvokeServer(string_1, string_2);
								wait()
								local string_1 = "ZQuestProgress";
								local string_2 = "Begin";
								local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
								Target:InvokeServer(string_1, string_2);
							end
						elseif game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("ZQuestProgress", "Check") == 1 then
							local args = {
								[1] = "TravelZou" -- OLD WORLD to NEW WORLD
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						else
							if game.Workspace.Enemies:FindFirstChild("Don Swan [Lv. 1000] [Boss]") then 	
								for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
									if v.Name == "Don Swan [Lv. 1000] [Boss]" and v:FindFirstChild("Humanoid")and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
										repeat wait()
											if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
												Farmtween = toTarget(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
											elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
												if Farmtween then
													Farmtween:Stop()
												end
												EquipWeapon(_G.Select_Weapon)
												Usefastattack = true
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
												Click()
											end 
										until not _G.Autothird or not v.Parent or v.Humanoid.Health <= 0 
										Usefastattack = false
									end
								end
							else -- SlashHit : rbxassetid://2453605589
								TweenDonSwanthireworld = toTarget(CFrame.new(2288.802, 15.1870775, 863.034607).Position,CFrame.new(2288.802, 15.1870775, 863.034607))
								if (CFrame.new(2288.802, 15.1870775, 863.034607).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
									if TweenDonSwanthireworld then
										TweenDonSwanthireworld:Stop()
										game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2288.802, 15.1870775, 863.034607)
									end
								end
							end
						end
					else
						if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess == nil then
							TabelDevilFruitStore = {}
							TabelDevilFruitOpen = {}

							for i,v in pairs(game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("getInventoryFruits")) do
								for i1,v1 in pairs(v) do
									if i1 == "Name" then 
										table.insert(TabelDevilFruitStore,v1)
									end
								end
							end

							for i,v in next,game.ReplicatedStorage:WaitForChild("Remotes").CommF_:InvokeServer("GetFruits") do
								if v.Price >= 1000000 then  
									table.insert(TabelDevilFruitOpen,v.Name)
								end
							end

							for i,DevilFruitOpenDoor in pairs(TabelDevilFruitOpen) do
								for i1,DevilFruitStore in pairs(TabelDevilFruitStore) do
									if DevilFruitOpenDoor == DevilFruitStore and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess == nil then    
										if not game.Players.LocalPlayer.Backpack:FindFirstChild(DevilFruitStore) then   
											local string_1 = "LoadFruit";
											local string_2 = DevilFruitStore;
											local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
											Target:InvokeServer(string_1, string_2);
										else
											local string_1 = "TalkTrevor";
											local string_2 = "1";
											local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
											Target:InvokeServer(string_1, string_2);
											local string_1 = "TalkTrevor";
											local string_2 = "2";
											local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
											Target:InvokeServer(string_1, string_2);
											local string_1 = "TalkTrevor";
											local string_2 = "3";
											local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
											Target:InvokeServer(string_1, string_2);
										end
									end
								end
							end

							local string_1 = "TalkTrevor";
							local string_2 = "1";
							local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
							Target:InvokeServer(string_1, string_2);
							local string_1 = "TalkTrevor";
							local string_2 = "2";
							local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
							Target:InvokeServer(string_1, string_2);
							local string_1 = "TalkTrevor";
							local string_2 = "3";
							local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
							Target:InvokeServer(string_1, string_2);
						end
					end
				else
					if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 0 then
						if string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Swan Pirates") and string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then 
							if game.Workspace.Enemies:FindFirstChild("Swan Pirate [Lv. 775]") then
								for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
									if v.Name == "Swan Pirate [Lv. 775]" then
										pcall(function()
											repeat wait()
												if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
													Farmtween = toTarget(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
												elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
													if Farmtween then
														Farmtween:Stop()
													end
													EquipWeapon(_G.Select_Weapon)
													Usefastattack = true
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														local args = {
															[1] = "Buso"
														}
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
													end
													game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
													Click()
												end 
											until not v.Parent or v.Humanoid.Health <= 0 or _G.Autothird == false or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
											AutoBartiloBring = false
											Usefastattack = false
										end)
									end
								end
							else
								Questtween = toTarget(CFrame.new(1057.92761, 137.614319, 1242.08069).Position,CFrame.new(1057.92761, 137.614319, 1242.08069))
								if (CFrame.new(1057.92761, 137.614319, 1242.08069).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
									if Questtween then
										Questtween:Stop()
									end
									game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1057.92761, 137.614319, 1242.08069)
								end
							end
						else
							Bartilotween = toTarget(CFrame.new(-456.28952, 73.0200958, 299.895966).Position,CFrame.new(-456.28952, 73.0200958, 299.895966))
							if ( CFrame.new(-456.28952, 73.0200958, 299.895966).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
								if Bartilotween then
									Bartilotween:Stop()
								end
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =  CFrame.new(-456.28952, 73.0200958, 299.895966)
								local args = {
									[1] = "StartQuest",
									[2] = "BartiloQuest",
									[3] = 1
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							end
						end 
					elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 1 then
						if game.Workspace.Enemies:FindFirstChild("Jeremy [Lv. 850] [Boss]") then
							Ms = "Jeremy [Lv. 850] [Boss]"
							for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
								if v.Name == Ms then
									repeat wait()
										if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
											Farmtween = toTarget(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
										elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
											if Farmtween then
												Farmtween:Stop()
											end
											EquipWeapon(_G.Select_Weapon)
											Usefastattack = true
											if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
												local args = {
													[1] = "Buso"
												}
												game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
											end
											game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
											Click()
										end 
									until not v.Parent or v.Humanoid.Health <= 0 or _G.Autothird == false
									Usefastattack = false
								end
							end
						else
							Bartilotween = toTarget(CFrame.new(2099.88159, 448.931, 648.997375).Position,CFrame.new(2099.88159, 448.931, 648.997375))
							if (CFrame.new(2099.88159, 448.931, 648.997375).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
								if Bartilotween then
									Bartilotween:Stop()
								end
								game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2099.88159, 448.931, 648.997375)
							end
						end
					elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 2 then
						if (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
							Bartilotween = toTarget(CFrame.new(-1836, 11, 1714).Position,CFrame.new(-1836, 11, 1714))
						elseif (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
							if Bartilotween then
								Bartilotween:Stop()
							end
							game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1836, 11, 1714)
							wait(.5)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1850.49329, 13.1789551, 1750.89685)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1858.87305, 19.3777466, 1712.01807)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1803.94324, 16.5789185, 1750.89685)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1858.55835, 16.8604317, 1724.79541)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1869.54224, 15.987854, 1681.00659)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1800.0979, 16.4978027, 1684.52368)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1819.26343, 14.795166, 1717.90625)
							wait(.1)
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1813.51843, 14.8604736, 1724.79541)
						end
					end
				end
			end
		end
	end
end)
function bypasstp(x)
    spawn(function()
		pcall(function()
			game.Players.localPlayer.Character.Head:Destroy()
			task.wait(0.5)
			game.Players.localPlayer.Character.HumanoidRootPart.CFrame = x
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
		end)
    end)
end

spawn(function()
    while wait() do
        pcall(function()
            if _G.FastFarm then
                local LV = game:GetService("Players").LocalPlayer.Data.Level.Value
                if LV == 10 then
                    _G.AutoFarm = false
                    _G.Farm2 = true
                elseif LV >= 60 and _G.AutoFarm then
                    _G.Farm2 = false
                    _G.AutoFarm = true
                end
            end
        end)
    end
end)

spawn(function()
	pcall(function()
		while task.wait() do
			if _G.AutoFarm then
				function UseCode(Text)
					game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
				end
				UseCode("Sub2Fer999")
				UseCode("Enyu_is_Pro")
				UseCode("Magicbus")
				UseCode("JCWK")
				UseCode("Starcodeheo")
				UseCode("Bluxxy")
				UseCode("fudd10_v2")
				UseCode("FUDD10")
				UseCode("BIGNEWS")
				UseCode("SUB2NOOBMASTER123")
				UseCode("Sub2Daigrock")
				UseCode("Axiore")
				UseCode("TantaiGaming")
				UseCode("STRAWHATMAINE")
				UseCode("3BVISITS")
				UseCode("THEGREATACE")
				UseCode("Bignews ")
				UseCode("TantaiGaming")
				UseCode("SUB2GAMERROBOT_EXP1")
			end
		end
	end)
 end)
function Check()
    if _G.Farm2 then
        MS = "Shanda [Lv. 475]"
    end
end

spawn(function()
    while wait() do
        pcall(function()
            if _G.Farm2 then
                Check()
                if game:GetService("Workspace").Enemies:FindFirstChild(MS) then
                    for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if v.Name == MS then
                            repeat wait()
                                TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                EquipWeapon(_G.Select_Weapon)
                                if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                    local args = {
                                        [1] = "Buso"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if v.Humanoid:FindFirstChild("Animator") then
                                    v.Humanoid.Animator:Destroy()
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                    game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                    game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                end
                                StartMagnet3 = true 
                                PosMon2 = v.HumanoidRootPart.CFrame 
                            until not _G.Farm2 or v.Humanoid.Health <= 0
                        end
                    end
                else
                    StartMagnet3 =false
					if (game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047)).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1500 then
                    	TweenFarm(CFrame.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
					else
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
					end
                end
            end
        end)
    end
end)
posrandom = 0
spawn(function()
	while task.wait() do
		pcall(function()
			if _G.AutoFarm then
				game.Players.LocalPlayer.Character.Humanoid.Sit = false
				QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
				if not string.find(QuestTitle, NameMon) then 
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest") 
				end
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					StartMagnet = false
					CheckQuest()
					if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1500 then
						wait(1)
						TweenFarm(CFrameQuest)
					else
						bypasstp(CFrameQuest)
					end
					if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						wait(1.1)
						game.ReplicatedStorage.Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
					else
						wait(1)
						TweenFarm(CFrameQuest)
					end
				elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					pcall(function()
						CheckQuest()
						if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == Ms and v:FindFirstChild("Humanoid") then
									if v:WaitForChild('Humanoid').Health > 0 then
										repeat wait()
											pcall(function()
												if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
													if string.find(QuestTitle, NameMon) then
                                                        spawn(function()
                                                            if posrandom <= 1 then
                                                                TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,10,50))
                                                                posrandom = posrandom + 0.1
                                                            elseif posrandom >= 1 and posrandom <= 2 then
                                                                TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(50,10,0))
                                                                posrandom = posrandom + 0.1
                                                            elseif posrandom >= 2 and posrandom <= 3 then
                                                                TweenFarm(v.HumanoidRootPart.CFrame *CFrame.new(0,10,-50))
                                                                posrandom = posrandom + 0.1
                                                            elseif posrandom >= 3 and posrandom <= 4  then
                                                                TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(-50,10,0))
                                                                posrandom = posrandom + 0.1
                                                            elseif posrandom >=4 and posrandom <= 5 then
                                                                TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
                                                                posrandom = 0
                                                            end
                                                        end)
                                                        EquipWeapon(_G.Select_Weapon)
                
														if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
															local args = {
																[1] = "Buso"
															}
															game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
														end
														if v.Humanoid:FindFirstChild("Animator") then
															v.Humanoid.Animator:Destroy()
														end
														v.HumanoidRootPart.Size = Vector3.new(10,10,10)
														v.HumanoidRootPart.Transparency = 0.5
														if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
															game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
															game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
														end
                                                        PosMon = v.HumanoidRootPart.CFrame 
														StartMagnet = true
													else
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")  
													end
												else
													if (CFrameMon.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude >= 1500 then
														StatrMagnet = false
														CheckQuest()
														TweenFarm(CFrameMon)
													end
												end
											end)
										until not v:FindFirstChild("Humanoid") or not v:FindFirstChild("HumanoidRootPart") or not v.Parent or v.Humanoid.Health <= 0 or _G.AutoFarm == false or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
									end
								end
							end
						else
							StartMagnet = false
							TweenFarm(game:GetService("ReplicatedStorage"):FindFirstChild(Ms).HumanoidRootPart.CFrame * CFrame.new(1,10,0))
						end
					end)
				end
			end
		end)
	end
end)
spawn(function()
    while true do game:GetService("RunService").RenderStepped:Wait()
        for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
			CheckQuest()
            if _G.AutoFarm and v.Name ~= "Ice Admiral [Lv. 700] [Boss]" and v.Name ~= "Don Swan [Lv. 3000] [Boss]" and v.Name ~= "Saber Expert [Lv. 200] [Boss]" and v.Name ~= "Longma [Lv. 2000] [Boss]" and StartMagnet and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                if syn then
					if isnetworkowner(v.HumanoidRootPart) then
						v.HumanoidRootPart.CFrame = PosMon
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
					end
				else
					v.HumanoidRootPart.CFrame = PosMon
					if v.Humanoid:FindFirstChild("Animator") then
						v.Humanoid.Animator:Destroy()
					end
					sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
				end	
            end
        end
    end
end)
spawn(function()
    while task.wait() do
        for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
			CheckQuest()
            if _G.Farm2 and v.Name ~= "Ice Admiral [Lv. 700] [Boss]" and v.Name ~= "Don Swan [Lv. 3000] [Boss]" and v.Name ~= "Saber Expert [Lv. 200] [Boss]" and v.Name ~= "Longma [Lv. 2000] [Boss]" and StartMagnet3 and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                if syn then
					if isnetworkowner(v.HumanoidRootPart) then
						v.HumanoidRootPart.CFrame = PosMon2
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
					end
				else
					v.HumanoidRootPart.CFrame = PosMon2
					if v.Humanoid:FindFirstChild("Animator") then
						v.Humanoid.Animator:Destroy()
					end
					sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
				end	
            end
        end
    end
end)

spawn(function()
     game:GetService("RunService").Stepped:Connect(function()
        if _G.AutoFarm or AutoRaids then
            if not KRNL_LOADED and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
               setfflag("HumanoidParallelRemoveNoPhysics", "False")
              setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
              game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
             else
if not game:GetService("Workspace"):FindFirstChild("LOL") then
local LOL = Instance.new("Part")
LOL.Name = "LOL"
LOL.Parent = game.Workspace
LOL.Anchored = true
LOL.Transparency = 0.8
LOL.Size = Vector3.new(50,0.5,50)
elseif game:GetService("Workspace"):FindFirstChild("LOL") then
game.Workspace["LOL"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.9,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
end
end
for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
if v:IsA("BasePart") then
v.CanCollide = false
end
end
end
     end)
end)
spawn(function()
	pcall(function()
		game:GetService("RunService").Heartbeat:Connect(function()
			if _G.AutoFarm or _G.AutoRaid or NextIsland or statetp1 or _G.Nocliptp or _G.Auto_Observations_V2 or _G.Auto_Rainbow_Haki or _G.TeleportPlayer or _G.Noclip or _G.Auto_Enchancement or _G.Auto_Bone or _G.Hallow_Scythe or _G.Auto_Yama or _G.Auto_Rengoku or _G.Farm_Mas or _G.Farm2 or _G.AutoThird or _G.AutoBuddy or _G.AutoCavender or _G.Canvender or _G.Buddy or _G.Yamma or AutoShrakman or _G.Auto_Bone or _G.FARMPLAYERS or _G.autoraid or getgenv().AutoNew or statetp1 or Autothird or _G.AutoTEST or _G.AutoFarmMBF or _G.AutoFarmGun or _G.KenHaki then
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
	while game:GetService("RunService").Stepped:wait(10) do
		character = game.Players.LocalPlayer.Character 
		if _G.AutoFarm or _G.AutoRaid or NextIsland or statetp1 or _G.Nocliptp or _G.Auto_Observations_V2 or _G.Auto_Rainbow_Haki or _G.TeleportPlayer or _G.Auto_Enchancement or _G.Auto_Bone or _G.Hallow_Scythe or _G.Auto_Yama or _G.Auto_Rengoku or _G.Farm_Mas or _G.Farm2 or _G.AutoThird or _G.AutoBuddy or _G.AutoCavender or _G.Canvender or _G.Noclip or _G.Buddy or _G.Auto_Bone or _G.Yamma or _G.AutoFarm or KillPlayer or getgenv().AutoNew or Autothird or Autothird or Factory or NextIsland or TweenIsland or _G.AutoTEST or _G.AutoFarmMBF or _G.AutoFarmGun then
			pcall(function()
				for _, v in pairs(character:GetDescendants()) do
					pcall(function()
						if v:IsA("BasePart") then
							pcall(function()
							v.CanCollide = false
							end)
						end
					end)
				end
			end)
		end
	end
end)
local Sector2 = Tab1:CreateSector("Auto Farm Settings","Reft")

Weapon = {}
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
	if v:IsA("Tool") then
		table.insert(Weapon ,v.Name)
	end
end
for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
	if v:IsA("Tool") then
		table.insert(Weapon, v.Name)
	end
end
_G.Select_Weapon = _G.Save['Weapon']
local D = Sector2:AddDropdown("Select Weapon / Combat",Weapon,"Select Weapon / Combat",false,function(value)
	_G.Select_Weapon = value
    _G.Save['Weapon'] = value
    SaveSetting()
end)
Sector2:AddButton("Refresh Weapon",function()
	pcall(function()
		D:Clear()
		for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
			if v:IsA ("Tool") then
				table.insert(Weapon,v.Name)
				D:Add(v.Name)
			end
		end
	end)
end)
Sector2:AddToggle("AutoEquipMelee",_G.Save['AutoMeleekaitun'],function(value)
    _G.AutoMeleekaitun = value
	while _G.AutoMeleekaitun  == true do
		wait(2)
			for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
				if v.ClassName == "Tool" then
					if v.ToolTip == "Melee" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							local ToolSe = tostring(v.Name)
							local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
							game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
						end
					end
				end
			end

		print("test")
		end
		_G.Save['AutoMeleekaitun'] = value
		SaveSetting()	
end)
Sector2:AddToggle("Fast Attack",_G.Save['Fast_Attack'],function(value) 
    _G.Fast_Attack = value
    SaveSetting()
end)
local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
local plr = game.Players.LocalPlayer
local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]
do
    Camera:Stop()
end
function GetCurrentBlade() 
    local p13 = CbFw2.activeController
    local ret = p13.blades[1]
    if not ret then return end
    while ret.Parent~=game.Players.LocalPlayer.Character do 
		ret=ret.Parent 
	end
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
                for k, v in pairs(AC.animator.anims.basic) do
                    v:Play()
                end                  
            end)
            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
            end
        end
    end
end
local cac
if _G.SuperFastMode then 
    cac=task.wait
else
    cac=wait
end
spawn(function()
	while cac() do
		pcall(function()
			if _G.Fast_Attack then
				AttackNoCD()
			end
		end)
	end
end)
local Sector3 = Tab1:CreateSector("Auto Farm Mastery","left")
_G.Select_Mode = _G.Save['Select Mode']
Sector3:AddDropdown("Select Mode Mastery",{'Fruit','Gun','Sword'},"Select Mode",false,function(value)
    _G.Select_Mode = value
    _G.Save['Select Mode'] = value
    SaveSetting()
end)
Sector3:AddToggle("Auto Farm Mastery",_G.Save['Farm_Mastery'],function(value)
	_G.Farm_Mas = value
	_G.Save['Farm_Mastery'] = value
    SaveSetting()
end)
spawn(function()
	pcall(function()
		while wait() do
			for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
				if v:IsA("Tool") then
					if v:FindFirstChild("RemoteFunctionShoot") then 
						SelectToolWeaponGun = v.Name
					end
				end
			end
		end
	end)
end)
spawn(function()
   pcall(function()
      while wait() do
         for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
            if v:IsA("Tool") then
               if v:FindFirstChild('RemoteFunction') then
                  Sword = v.Name
               end
            end
        end
      end
   end)
end)
spawn(function()
	pcall(function() 
		while wait() do
			if _G.Farm_Mas then
				if _G.Select_Mode == "Fruit" then
					if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
						CheckQuest()
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1500 then
							TweenFarm(CFrameQuest)
						else
							bypasstp(CFrameQuest)
						end
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
							wait(1.1)
							game.ReplicatedStorage.Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
						if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
							for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == Ms then
									pcall(function()
										repeat wait()
											CheckQuest()
											PosMonSkil = v.HumanoidRootPart.CFrame
											HealthMin = v.Humanoid.MaxHealth * HealthPersen/100
											if v.Humanoid.Health <= HealthMin then
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												EquipWeapon(tostring(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value))
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
												UESSKILL = true
												StartMagnetSKILL = true
												_G.Fast_Attack = false
											else
												_G.Fast_Attack = true
												UESSKILL = false
												StartMagnetSKILL = true
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												EquipWeapon(_G.Select_Weapon)
												v.HumanoidRootPart.Size = Vector3.new(10,10,10)
												v.HumanoidRootPart.Transparency = 0.5
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
											end
										until not _G.Farm_Mas or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
									end)
								end
							end
						else
							UESSKILL = false
							TweenFarm(CFrameMon)
						end
					end
				end
				if _G.Select_Mode == "Gun" then
					if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
						CheckQuest()
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1500 then
							TweenFarm(CFrameQuest)
						else
							bypasstp(CFrameQuest)
						end
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
							wait(1.1)
							game.ReplicatedStorage.Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
						if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
							for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == Ms then
									pcall(function()
										repeat wait()
											CheckQuest()
											HealthMin = v.Humanoid.MaxHealth * HealthPersen/100
											if v.Humanoid.Health <= HealthMin then
												EquipWeapon(tostring(SelectToolWeaponGun))
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												CbFw2.activeController.hitboxMagnitude = 100000
												local args = {
													[1] = v.HumanoidRootPart.Position,
													[2] = v.HumanoidRootPart
												}
												game:GetService("Players").LocalPlayer.Character[SelectToolWeaponGun].RemoteFunctionShoot:InvokeServer(unpack(args))
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
												_G.Fast_Attack = false
											else
												_G.Fast_Attack = true
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												EquipWeapon(_G.Select_Weapon)
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
											end
										until not _G.Farm_Mas or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
									end)
								end
							end
						else
							TweenFarm(CFrameMon)
						end
					end
				end
				if _G.Select_Mode == "Sword" then
					if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
						CheckQuest()
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1500 then
							TweenFarm(CFrameQuest)
						else
							bypasstp(CFrameQuest)
						end
						if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
							wait(1.1)
							game.ReplicatedStorage.Remotes.CommF_:InvokeServer("StartQuest", NaemQuest, LevelQuest)
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
						if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
							for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == Ms then
									pcall(function()
										repeat wait()
											CheckQuest()
											HealthMin = v.Humanoid.MaxHealth * HealthPersen/100
											if v.Humanoid.Health <= HealthMin then
												EquipWeapon(tostring(Sword))
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												CbFw2.activeController.hitboxMagnitude = 55
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
												_G.Fast_Attack = false
											else
												_G.Fast_Attack = true
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													local args = {
														[1] = "Buso"
													}
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
												end
												EquipWeapon(_G.Select_Weapon)
												TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
												game:GetService("VirtualUser"):CaptureController()
												game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
											end
										until not _G.Farm_Mas or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
									end)
								end
							end
						else
							TweenFarm(CFrameMon)
						end
					end
				end
			end
		end
	end)
end)
spawn(function()
	while wait() do
		if UESSKILL then
			pcall(function()
				CheckQuest()
				for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
					if game:GetService("Players").LocalPlayer.Character:FindFirstChild(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value) then
						MasBF = game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Data.DevilFruit.Value].Level.Value
					elseif game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value) then
						MasBF = game:GetService("Players").LocalPlayer.Backpack[game:GetService("Players").LocalPlayer.Data.DevilFruit.Value].Level.Value
					end
					if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon-Dragon") then                      
						if SKILLZ then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                        
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
						end
						if SKILLX then          
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))               
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
						end
						if SKILLC then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                          
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
							wait(2)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
						end
					elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom-Venom") then   
						if SKILLZ then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                        
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
						end
						if SKILLX then        
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))               
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
						end
						if SKILLC then 
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                          
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
							wait(2)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
						end
					elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha") then
						if SKILLZ and game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Size == Vector3.new(2, 2.0199999809265, 1) then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                         
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
						end
						if SKILLX then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                           
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
						end
						if SKILLC then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                           
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
						end
						if SKILLV then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"V",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"V",false,game)
						end
					elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value) then
						if SKILLZ then 
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                         
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
						end
						if SKILLX then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                           
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
						end
						if SKILLC then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))                           
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
						end
						if SKILLV then
							local args = {
								[1] = PosMonSkil.Position
							}
							game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Tool").Name].RemoteEvent:FireServer(unpack(args))
							game:GetService("VirtualInputManager"):SendKeyEvent(true,"V",false,game)
							game:GetService("VirtualInputManager"):SendKeyEvent(false,"V",false,game)
						end
					end
				end
			end)
		end
	end
end)
spawn(function()
	game:GetService("RunService").RenderStepped:Connect(function()
		pcall(function()
			if UESSKILL then
				for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Notifications:GetChildren()) do
					if v.Name == "NotificationTemplate" then
						if string.find(v.Text, "Skill locked!") then
							v:Destroy()
						end
					end
				end
			end
		end)
	end)
end)
spawn(function()
	pcall(function()
		game:GetService("RunService").RenderStepped:Connect(function()
			if UESSKILL then
				local args = {
					[1] = PosMonSkil.Position
				}
				game:GetService("Players").LocalPlayer.Character[game:GetService("Players").LocalPlayer.Data.DevilFruit.Value].RemoteEvent:FireServer(unpack(args))
			end
		end)
	end)
end)

spawn(function()
    while true do game:GetService("RunService").RenderStepped:Wait()
        for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
			CheckQuest()
            if _G.Farm_Mas and v.Name ~= "Ice Admiral [Lv. 700] [Boss]" and v.Name ~= "Don Swan [Lv. 3000] [Boss]" and v.Name ~= "Saber Expert [Lv. 200] [Boss]" and v.Name ~= "Longma [Lv. 2000] [Boss]" and StartMagnetSKILL and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                if syn then
					if isnetworkowner(v.HumanoidRootPart) then
						v.HumanoidRootPart.CFrame = PosMonSkil
						v.HumanoidRootPart.Size = Vector3.new(10,10,10)
						v.HumanoidRootPart.Transparency = 0.5
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
					end
				else
					v.HumanoidRootPart.CFrame = PosMonSkil
					v.HumanoidRootPart.Size = Vector3.new(10,10,10)
					v.HumanoidRootPart.Transparency = 0.5
					if v.Humanoid:FindFirstChild("Animator") then
						v.Humanoid.Animator:Destroy()
					end
					sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
				end	
            end
        end
    end
end)
HealthPersen = 20
Sector3:AddSlider("Health %",1,HealthPersen,100,1,function(value)
	HealthPersen = value
end)
local Sector4 = Tab1:CreateSector("Settings Farm Mastery","Right")
Sector4:AddToggle("Skill Z",_G.Save['SKILLZ'],function(t)
	SKILLZ = t
	_G.Save['SKILLZ'] = value
    SaveSetting()
end)
Sector4:AddToggle("Skill X",_G.Save['SKILLX'],function(t)
	SKILLX = t
	_G.Save['SKILLX'] = value
    SaveSetting()
end)
Sector4:AddToggle("Skill C",_G.Save['SKILLC'],function(t)
	SKILLC = t
	_G.Save['SKILLC'] = value
    SaveSetting()
end)
Sector4:AddToggle("Skill V",_G.Save['SKILLV'],function(t)
	SKILLV = t
	_G.Save['SKILLV'] = value
    SaveSetting()
end)
local Sector5 = Tab1:CreateSector("Auto Sword","left")
Sector5:AddSeperator("Auto Rengoku Sword")
Sector5:AddToggle("Auto Rengoku",_G.Save['Auto_Rengoku'],function(t)
	_G.Auto_Rengoku = t
	_G.Save['Auto_Rengoku'] = t
end)
Sector5:AddToggle("Auto Rengoku Hop",_G.Save['Auto_Rengoku_Hop'],function(t)
	_G.Auto_Rengoku_Hop = t
	_G.Save['Auto_Rengoku_Hop'] = t
end)
task.spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Rengoku then
				if NewWorld then
					if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') then
						EquipWeapon('Hidden Key')
						if game:GetService("Players").LocalPlayer.Character:FindFirstChild('Hidden Key') then
							if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - CFrame.new(6571.22754, 294.103394, -6967.38184, -0.838688731, 0, -0.544611216, 0, 1, 0, 0.544611216, 0, -0.838688731).Position).Magnitude <= 100 then
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6571.22754, 294.103394, -6967.38184, -0.838688731, 0, -0.544611216, 0, 1, 0, 0.544611216, 0, -0.838688731)
							else
								TweenFarm(CFrame.new(6571.22754, 294.103394, -6967.38184, -0.838688731, 0, -0.544611216, 0, 1, 0, 0.544611216, 0, -0.838688731))
							end
						end
					else
						if game:GetService("Workspace").Enemies:FindFirstChild('Awakened Ice Admiral [Lv. 1400] [Boss]') then
							for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == "Awakened Ice Admiral [Lv. 1400] [Boss]" and v:FindFirstChild('HumanoidRootPart') and v:FindFirstChild('Humanoid') and v.Humanoid.Health > 0 then
									pcall(function()
										repeat wait()
											if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
												local args = {
													[1] = "Buso"
												}
												game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
											end
											EquipWeapon(_G.Select_Weapon)
											TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
											v.HumanoidRootPart.CanCollide = false
											v.HumanoidRootPart.Size = Vector3.new(100, 100, 100)
											game:GetService("VirtualUser"):CaptureController()
											game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
										until not _G.Auto_Rengoku or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') or game:GetService("Players").LocalPlayer.Character:FindFirstChild('Hidden Key')
									end)
								end
							end
						else
							if (CFrame.new(6383.93066, 296.65329, -6876.88965, 0.509762347, 5.02991782e-09, -0.860315263, -2.02902815e-08, 1, -6.17599616e-09, 0.860315263, 2.06043289e-08, 0.509762347).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
								bypasstp(CFrame.new(6383.93066, 296.65329, -6876.88965, 0.509762347, 5.02991782e-09, -0.860315263, -2.02902815e-08, 1, -6.17599616e-09, 0.860315263, 2.06043289e-08, 0.509762347))
							else
								TweenFarm(CFrame.new(6383.93066, 296.65329, -6876.88965, 0.509762347, 5.02991782e-09, -0.860315263, -2.02902815e-08, 1, -6.17599616e-09, 0.860315263, 2.06043289e-08, 0.509762347))
							end
							if _G.Auto_Rengoku_Hop and not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') and not game:GetService("Players").LocalPlayer.Character:FindFirstChild('Hidden Key') then
								if not game:GetService("ReplicatedStorage"):FindFirstChild('Awakened Ice Admiral [Lv. 1400] [Boss]') and not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('Hidden Key') and not game:GetService("Players").LocalPlayer.Character:FindFirstChild('Hidden Key') then
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
							end
						end
					end
				else
					local args = {
                        [1] = "TravelDressrosa" -- OLD WORLD to NEW WORLD
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
			end
		end)
	end
end)



Sector5:AddSeperator("Auto Buddy Sword")
Sector5:AddToggle("Auto Buddy",_G.Save['Auto_Buddy'],function(t)
	_G.Auto_Buddy = t
	_G.Save['Auto_Buddy'] = t
end)
Sector5:AddToggle("Auto Buddy Hop",_G.Save['Auto_Buddy_Hop'],function(t)
	_G.Auto_Buddy_Hop = t
	_G.Save['Auto_Buddy_Hop'] = t
end)
_G.AutoNewWorld = Value
local Plr = game:GetService("Players").LocalPlayer
local VirtualUser = game:GetService('VirtualUser')
function Tween(gotoCFrame)
	pcall(function()
		game.Players.LocalPlayer.Character.Humanoid.Sit = false
	end)
	if (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude <= 200 then
		pcall(function() 
			tween:Cancel()
		end)
		game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.CFrame = gotoCFrame
	else
		local args = {
			[1] = "SetSpawnPoint"
		}
		
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		local tween_s = game:service"TweenService"
		local info = TweenInfo.new((game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude/300, Enum.EasingStyle.Linear)
		local tween, err = pcall(function()
			tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = gotoCFrame})
			tween:Play()
		end)
		if not tween then return err end
	end
end
spawn(function()
    while wait() do
        if _G.AutoNewWorld then
            if game.Players.localPlayer.Data.Level.Value >= 700 then
                if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("DressrosaQuestProgress", "Dressrosa") ~= 0 then
                    if Workspace.Map.Ice.Door.Transparency == 1 then
                        if (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 250 then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") then
                                local tool = game.Players.LocalPlayer.Backpack:FindFirstChild("Key")
                                wait(.4)
                                game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
                            end
                            Tween(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                            if (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                                Tween(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                            end
                        elseif game.Workspace.Enemies:FindFirstChild("Ice Admiral [Lv. 700] [Boss]") and game.Workspace.Map.Ice.Door.CanCollide == false and game.Workspace.Map.Ice.Door.Transparency == 1 and (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                            for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                                if v.Name == "Ice Admiral [Lv. 700] [Boss]" and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and v.Name == "Ice Admiral [Lv. 700] [Boss]" then
                                    repeat wait()
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            local args = {
                                                [1] = "Buso"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.AutoNewWorld == false
                                end
                            end
                        else
                            _G.FastAttack = true
                        end 
                    else
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") or game.Players.LocalPlayer.Character:FindFirstChild("Key") then
                            Tween(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                            if (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                                Tween(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                                local args = {
                                    [1] = "DressrosaQuestProgress",
                                    [2] = "Detective"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                wait(0.5)
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") then
                                    local tool = game.Players.LocalPlayer.Backpack:FindFirstChild("Key")
                                    wait(.4)
                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
                                end
                            end
                        else
                            Tween(CFrame.new(4849.29883, 5.65138149, 719.611877))
                            if (CFrame.new(4849.29883, 5.65138149, 719.611877).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                                Tween(CFrame.new(4849.29883, 5.65138149, 719.611877))
                                local args = {
                                    [1] = "DressrosaQuestProgress",
                                    [2] = "Detective"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                wait(0.5)
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Key") then
                                    local tool = game.Players.LocalPlayer.Backpack:FindFirstChild("Key")
                                    wait(.4)
                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
                                end
                            end
                        end
                    end
                else
					local args = {
						[1] = "TravelDressrosa" -- OLD WORLD to NEW WORLD
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
			end
		end
	end
end)
task.spawn(function()
	while task.wait() do
		if _G.Auto_Buddy then
			pcall(function()
				if game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == "Cake Queen [Lv. 2175] [Boss]" then
							if v:WaitForChild("Humanoid").Health > 0 then
								repeat task.wait()
									if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
										local args = {
											[1] = "Buso"
										}
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
									end
									TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.CanCollide = false
									v.HumanoidRootPart.Size = Vector3.new(100, 100, 100)
									game:GetService("VirtualUser"):CaptureController()
									game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
								until not _G.Auto_Buddy or not v.Parent or v.Humanoid.Health <= 0
							end
						end
					end
				else
					if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrame.new(-676.0181274414062, 381.592041015625, -11180.0615234375).Position).Magnitude <= 1500 then
						TweenFarm(CFrame.new(-676.0181274414062, 381.592041015625, -11180.0615234375))
					else
						bypasstp(CFrame.new(-676.0181274414062, 381.592041015625, -11180.0615234375))
					end
					if _G.Auto_Buddy_Hop then
						if not game:GetService("ReplicatedStorage"):FindFirstChild("Cake Queen [Lv. 2175] [Boss]") then
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
					end
				end
			end)
		end
	end
end)
Sector5:AddSeperator("Auto Yama Sword")
Sector5:AddToggle("Auto Yama",_G.Save['Auto_Yama'],function(t)
	_G.Auto_Yama = t
	_G.Save['Auto_Yama'] = t
	SaveSetting()
end)
Sector5:AddToggle("Auto Yama Hop",_G.Save['Auto_Yama_Hop'],function(t)
	_G.Auto_Yama_Hop = t
	_G.Save['Auto_Yama_Hop'] = t
	SaveSetting()
end)
function Tween(gotoCFrame)
	pcall(function()
		game.Players.LocalPlayer.Character.Humanoid.Sit = false
	end)
	if (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude <= 200 then
		pcall(function() 
			tween:Cancel()
		end)
		game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.CFrame = gotoCFrame
	else
		local tween_s = game:service"TweenService"
		local info = TweenInfo.new((game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude/320, Enum.EasingStyle.Linear)
		local tween, err = pcall(function()
			tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = gotoCFrame})
			tween:Play()
		end)
		if not tween then return err end
	end
end
spawn(function()
    pcall(function()
        while wait() do
            if _G.Auto_Yama then
                if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter","Progress") < 30 then
                    local args = {
                        [1] = "EliteHunter"
                    }
                
                    remote = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					if string.find(remote, "I don't have anything") then
						PosElite = nil
						for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
							if v:IsA("Tool") then
								if string.find(v.Name, 'God') then
									if _G.Yamma then
										GodSummon = true
									end
								end
							end
						end
						for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
							if v:IsA("Tool") then
								if string.find(v.Name, 'God') then
									if _G.Yamma then
										GodSummon = true
									end
								end
							end
						end
						if _G.Auto_Yama_Hop and not GodSummon then
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
					end
					PosElite = nil
                    if string.find(remote, 'Hydra Island') then
                        EliteHunterName = string.split(string.split(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, 'Defeat')[2], ' ')[2]:gsub(' ', '')
                        for _i, v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
                            if v:IsA('Model') then
                                if string.find(v.Name, EliteHunterName) then
                                    if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - v.HumanoiPartdRootPart.CFrame.Position).Magnitude >= 4000 then
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(-75, 75, 75))
                                    end
                                end
                            end
                        end
                        for _i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if string.find(v.Name, EliteHunterName) and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                repeat wait()
                                    if not PosElite then
                                        PosElite = v.HumanoidRootPart.CFrame
                                    end
                                    v.HumanoidRootPart.CFrame = PosElite
                                    EquipWeapon(_G.Select_Weapon)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                        local args = {
                                        [1] = "Buso"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    Tween(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                    v.Humanoid:ChangeState(14)
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid.WalkSpeed = 0
                                    v.Humanoid.JumpPower = 0
                                    v.HumanoidRootPart.Size = Vector3.new(10,10,10)
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                    game:GetService'VirtualUser':CaptureController()
                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                until not v:FindFirstChild("Humanoid") or  not v:FindFirstChild("HumanoidRootPart") or not v.Humanoid.Health > 0 or not _G.Auto_Yama
                            end
                        end
                    end
                    if string.find(remote, 'Turtle') then
                        EliteHunterName = string.split(string.split(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, 'Defeat')[2], ' ')[2]:gsub(' ', '')
                        for _i, v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
                            if v:IsA('Model') then
                                if string.find(v.Name, EliteHunterName) then
                                    if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - v.HumanoidRootPart.CFrame.Position).Magnitude >= 4000 then
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(-75, 75, 75))
                                    end
                                end
                            end
                        for _i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if string.find(v.Name, EliteHunterName) and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                repeat wait()
                                    if not PosElite then
                                        PosElite = v.HumanoidRootPart.CFrame
                                    end
                                    v.HumanoidRootPart.CFrame = PosElite
                                    EquipWeapon(_G.Select_Weapon)
                                    _G.Fastattack = true
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                        local args = {
                                        [1] = "Buso"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    Tween(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                    v.Humanoid:ChangeState(14)
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid.WalkSpeed = 0
                                    v.Humanoid.JumpPower = 0
                                    v.HumanoidRootPart.Size = Vector3.new(10,10,10)
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                    game:GetService'VirtualUser':CaptureController()
                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                    until not v:FindFirstChild("Humanoid") or  not v:FindFirstChild("HumanoidRootPart") or not v.Humanoid.Health > 0 or not _G.Auto_Yama
                                end
                            end
                        end
                    end
                    if not string.find(remote, 'Turtle') and not string.find(remote, 'Hydra Island')  then
                        EliteHunterName = string.split(string.split(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, 'Defeat')[2], ' ')[2]:gsub(' ', '')
                        for _i, v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
                            if v:IsA('Model') then
                                if string.find(v.Name, EliteHunterName) then
                                    if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - v.HumanoidRootPart.CFrame.Position).Magnitude >= 4000 then
                                            Tween(v.HumanoidRootPart.CFrame * CFrame.new(-75, 75, 75))
                                        end
                                    end
                                end
                            end
                        for _i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if string.find(v.Name, EliteHunterName) and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                repeat wait()
                                    if not PosElite then
                                        PosElite = v.HumanoidRootPart.CFrame
                                    end
                                    v.HumanoidRootPart.CFrame = PosElite
                                    EquipWeapon(_G.Select_Weapon)
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                        local args = {
                                        [1] = "Buso"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    Tween(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                                    v.Humanoid:ChangeState(14)
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid.WalkSpeed = 0
                                    v.Humanoid.JumpPower = 0
                                    v.HumanoidRootPart.Size = Vector3.new(10,10,10)
                                    if v.Humanoid:FindFirstChild("Animator") then
                                        v.Humanoid.Animator:Destroy()
                                    end
                                    game:GetService'VirtualUser':CaptureController()
                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                                until not v:FindFirstChild("Humanoid") or  not v:FindFirstChild("HumanoidRootPart") or not v.Humanoid.Health > 0 or not _G.Auto_Yama
                            end
                        end
                    end
                else
                    PosGhostYamma = nil
                    Tween(CFrame.new(5227.13037109375, 8.086737632751465, 1100.6697998046875) * CFrame.new(0, 40,0))
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if string.find(v.Name, 'Ghost') and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                            if not PosGhostYamma then
                                PosGhostYamma = v.HumanoidRootPart.CFrame
                            end
                            v.HumanoidRootPart.CFrame = PosGhostYamma
                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                local args = {
                                [1] = "Buso"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            end
                            Tween(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                            v.Humanoid:ChangeState(14)
                            v.HumanoidRootPart.CanCollide = false
                            v.Humanoid.WalkSpeed = 0
                            v.Humanoid.JumpPower = 0
                            v.HumanoidRootPart.Size = Vector3.new(10,10,10)
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius",  math.huge)
                        end
                    end
                end
            end
        end
    end)
end)
Sector5:AddSeperator("Auto Legendaly Sword")
Sector5:AddToggle("Auto Legendaly",_G.Save['Auto_Legendaly'],function(t)
	_G.Auto_Legendaly = t
	_G.Save['Auto_Legendaly'] = t
	SaveSetting()
end)
Sector5:AddToggle("Auto Legendaly Hop",_G.Save['Auto_Legendaly_Hop'],function(t)
	_G.Auto_Legendaly_Hop = t
	_G.Save['Auto_Legendaly_Hop'] = t
	SaveSetting()
end)

function Hop()
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
        pcall(function()
            if _G.Auto_Legendaly then
                local args = {
                    [1] = "LegendarySwordDealer",
                    [2] = "2"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
            if _G.Auto_Legendaly_Hop then
                local args = {
                    [1] = "LegendarySwordDealer",
                    [2] = "2"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                wait(0.7)
                Hop()
            end
        end)
    end
end)
Sector5:AddSeperator("Auto Canvender Sword")
Sector5:AddToggle("Auto Canvender",_G.Save['Auto_Canvender'],function(t)
	_G.Auto_Canvender = t
	_G.Save['Auto_Canvender'] = t
	SaveSetting()
end)
Sector5:AddToggle("Auto Canvender Hop",_G.Save['Auto_Canvender_Hop'],function(t)
	_G.Auto_Canvender_Hop = t
	_G.Save['Auto_Canvender_Hop'] = t
	SaveSetting()
end)

task.spawn(function()
	while wait() do
		if _G.Auto_Canvender then
			pcall(function()
				if game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == "Beautiful Pirate [Lv. 1950] [Boss]" then
							if v:WaitForChild("Humanoid").Health > 0 then
								repeat task.wait()
									if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
										local args = {
											[1] = "Buso"
										}
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
									end
									TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.CanCollide = false
									v.HumanoidRootPart.Size = Vector3.new(100, 100, 100)
									game:GetService("VirtualUser"):CaptureController()
									game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
								until not _G.Auto_Canvender or not v.Parent or v.Humanoid.Health <= 0
							end
						end
					end
				else
					if (game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(5314.58203125, 25.419387817383, -125.94227600098)).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(5314.58203125, 25.419387817383, -125.94227600098))
					else
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(5314.58203125, 25.419387817383, -125.94227600098))
					end
					if _G.Auto_Canvender_Hop then
						if not game:GetService("ReplicatedStorage"):FindFirstChild("Beautiful Pirate [Lv. 1950] [Boss]") then
							Hop()
						end
					end
				end
			end)
		end
	end
end)
Sector5:AddSeperator("Auto Hallow Scythe Sword")
Sector5:AddToggle("Auto Hallow Scythe",_G.Save['Auto_Hallow_Scythe'],function(t)
	_G.Hallow_Scythe = t
	_G.Save['Auto_Hallow_Scythe'] = t
	SaveSetting()
end)

task.spawn(function()
	while wait() do
		pcall(function()
			if _G.Hallow_Scythe then
				if game:GetService("Workspace").Enemies:FindFirstChild('Soul Reaper [Lv. 2100] [Raid Boss]') then
					for _,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == 'Soul Reaper [Lv. 2100] [Raid Boss]' or v:FindFirstChild('HumanoidRootPart') or v:FindFirstChild('Humanoid') then
							repeat wait()
								if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
									local args = {
										[1] = "Buso"
									}
									game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
								end
								TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
								v.HumanoidRootPart.CanCollide = false
								v.HumanoidRootPart.Size = Vector3.new(60,60,60)
								game:GetService("VirtualUser"):CaptureController()
								game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
							until v.Humanoid.Health <= 0 or not _G.Hallow_Scythe
						end
					end
				else
					pcall(function()
						if not game:GetService("ReplicatedStorage"):FindFirstChild('Soul Reaper [Lv. 2100] [Raid Boss]') then
							if game.Players.LocalPlayer.Backpack:FindFirstChild("Hallow Essence") then
								EquipWeapon('Hallow Essence')
								if game.Players.LocalPlayer.Character:FindFirstChild("Hallow Essence") then
									TweenFarm(CFrame.new(-8933.13, 146.822, 6064.42))
									if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - CFrame.new(-8933.13, 146.822, 6064.42).Position).Magnitude >= 1500 then
										bypasstp(CFrame.new(-8933.13, 146.822, 6064.42))
									else
										TweenFarm(CFrame.new(-8933.13, 146.822, 6064.42))
									end
								end
							else
								TweenFarm(CFrame.new(-8722.19629, 141.519562, 6247.646, 0, 0, 1, 0, 1, -0, -1, 0, 0))
								if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - CFrame.new(-8722.19629, 141.519562, 6247.646, 0, 0, 1, 0, 1, -0, -1, 0, 0).Position).Magnitude <= 20 then
									repeat wait()
										local args = {
											[1] = "Bones",
											[2] = "Buy",
											[3] = 1,
											[4] = 1
										}
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
									until game.Players.LocalPlayer.Backpack:FindFirstChild("Hallow Essence") or game.Players.LocalPlayer.Character:FindFirstChild("Hallow Essence") or not _G.Hallow_Scythe
								else
									TweenFarm(CFrame.new(-8722.19629, 141.519562, 6247.646, 0, 0, 1, 0, 1, -0, -1, 0, 0))
								end
							end
						end
					end)
				end
			end
		end)
	end
end)
local Sector6 = Tab1:CreateSector("Others","Reft")
Sector6:AddToggle("Auto Legendaly",_G.Save['Auto_Legendaly'],function(t)
	_G.Auto_Legendaly = t
	_G.Save['Auto_Legendaly'] = t
	SaveSetting()
end)
spawn(function()
    while wait() do
        pcall(function()
            if _G.Auto_Legendaly then
                local args = {
                    [1] = "LegendarySwordDealer",
                    [2] = "2"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end)
    end
end)
Sector6:AddToggle("Auto Bone,Money",_G.Save['Auto_Bone'],function(t)
	_G.Auto_Bone = t
	_G.Save['Auto_Bone'] = t
	SaveSetting()
end)
spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Bone then
				if game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton [Lv. 1975]") or game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie [Lv. 2000]") or game:GetService("Workspace").Enemies:FindFirstChild("Domenic Soul [Lv. 2025]") or game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy [Lv. 2050]") then
					if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
					end
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == "Reborn Skeleton [Lv. 1975]" or v.Name == "Living Zombie [Lv. 2000]" or v.Name == "Demonic Soul [Lv. 2025]" or v.Name == "Posessed Mummy [Lv. 2050]" then
							if v:WaitForChild("Humanoid").Health > 0 then
								repeat wait()
									if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
										local args = {
											[1] = "Buso"
										}
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
									end
									EquipWeapon(_G.Select_Weapon)
									TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.CanCollide = false
									v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
									game:GetService("VirtualUser"):CaptureController()
									game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									MainMonBone = v.HumanoidRootPart.CFrame
									BoneMagnet = true
								until _G.Auto_Bone == false or not v.Parent or v.Humanoid.Health <= 0
							end
						end
					end
				else
					BoneMagnet = false
					if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - CFrame.new(-9501.64453, 582.052612, 6034.20117).Position).Magnitude >= 1500 then
						bypasstp(CFrame.new(-9501.64453, 582.052612, 6034.20117))
					else
						TweenFarm(CFrame.new(-9501.64453, 582.052612, 6034.20117))
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
				if _G.Auto_Bone and BoneMagnet  then
					if (v.Name == "Reborn Skeleton [Lv. 1975]" or v.Name == "Living Zombie [Lv. 2000]" or v.Name == "Demonic Soul [Lv. 2025]" or v.Name == "Posessed Mummy [Lv. 2050]") and (v.HumanoidRootPart.Position - MainMonBone.Position).Magnitude <= 300 then
                        v.Head.CanCollide = false
                        v.HumanoidRootPart.CanCollide = false
                        v.Humanoid.Sit = false
                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                        v.HumanoidRootPart.CFrame = MainMonBone
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
					end
				end
			end
		end)
	end)
end)
Sector6:AddToggle("Auto Enchancement",_G.Save['Auto_Enchancement'],function(t)
	_G.Auto_Enchancement = t
	_G.Save['Auto_Enchancement'] = t
	SaveSetting()
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Enchancement then
				if game:GetService("Workspace").Enemies:FindFirstChild("Ship Deckhand [Lv. 1250]") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Engineer [Lv. 1275]") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Steward [Lv. 1300]") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Officer [Lv. 1325]") then
					if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
					end
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == "Ship Deckhand [Lv. 1250]" or v.Name == "Ship Engineer [Lv. 1275]" or v.Name == "Ship Steward [Lv. 1300]" or v.Name == "Ship Officer [Lv. 1325]" then
							if v:WaitForChild("Humanoid").Health > 0 then
								repeat wait()
									if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
										local args = {
											[1] = "Buso"
										}
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
									end
									EquipWeapon(_G.Select_Weapon)
									TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.CanCollide = false
									v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
									game:GetService("VirtualUser"):CaptureController()
									game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									ENCPOS = v.HumanoidRootPart.CFrame
									Enchancement = true
								until _G.Auto_Enchancement == false or not v.Parent or v.Humanoid.Health <= 0
							end
						end
					end
				else
					Enchancement = false
					if (game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Position - CFrame.new(944.44964599609, 181.40081787109, 33278.9453125).Position).Magnitude >= 1500 then
						bypasstp(CFrame.new(944.44964599609, 181.40081787109, 33278.9453125))
					else
						TweenFarm(CFrame.new(944.44964599609, 181.40081787109, 33278.9453125))
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
				if _G.Auto_Enchancement and Enchancement  then
					if (v.Name == "Ship Deckhand [Lv. 1250]" or v.Name == "Ship Engineer [Lv. 1275]" or v.Name == "Ship Steward [Lv. 1300]" or v.Name == "Ship Officer [Lv. 1325]") and (v.HumanoidRootPart.Position - ENCPOS.Position).Magnitude <= 300 then
                        v.Head.CanCollide = false
                        v.HumanoidRootPart.CanCollide = false
                        v.Humanoid.Sit = false
                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                        v.HumanoidRootPart.CFrame = ENCPOS
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
					end
				end
			end
		end)
	end)
end)
Sector6:AddToggle("Auto Rainbow Haki",_G.Save['Auto_Rainbow_Haki'],function(t)
	_G.Auto_Rainbow_Haki = t
	if t == false then
		TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
	end
	_G.Save['Auto_Rainbow_Haki'] = value
    SaveSetting()
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Rainbow_Haki then
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					if (CFrame.new(-11893.7, 929.661, -8760.59).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2000 then
						bypasstp(CFrame.new(-11893.7, 929.661, -8760.59))
					else
						wait(1)
						TweenFarm(CFrame.new(-11893.7, 929.661, -8760.59))
					end
					if (CFrame.new(-11893.7, 929.661, -8760.59).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						wait(1.1)
						local args = {
							[1] = "HornedMan",
							[2] = "Bet"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))				
					else
						wait(1)
						TweenFarm(CFrame.new(-11893.7, 929.661, -8760.59))	
					end
				else
					if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == 'Defeat Stone (0/1)' then
						if game:GetService("Workspace").Enemies:FindFirstChild('Stone [Lv. 1550] [Boss]') then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == 'Stone [Lv. 1550] [Boss]' then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											local args = {
												[1] = "Buso"
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										game:GetService("VirtualUser"):CaptureController()
										game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									until not _G.Auto_Rainbow_Haki or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
								end
							end
						else
							if (CFrame.new(-1085, 40, 6779).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2500 then
								bypasstp(CFrame.new(-1085, 40, 6779))
							else
								wait(1)
								wait(TweenFarm(CFrame.new(-1085, 40, 6779)))
							end
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == 'Defeat Island Empress (0/1)' then
						if game:GetService("Workspace").Enemies:FindFirstChild('Island Empress [Lv. 1675] [Boss]') then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == 'Island Empress [Lv. 1675] [Boss]' then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											local args = {
												[1] = "Buso"
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										game:GetService("VirtualUser"):CaptureController()
										game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									until not _G.Auto_Rainbow_Haki or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
								end
							end
						else
							if (CFrame.new(5702.2724609375, 601.94860839844, 201.07873535156).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2500 then
								local args = {
									[1] = "requestEntrance",
									[2] = Vector3.new(5742.9599609375, 613.9691772460938, -283.685546875)
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							else
								wait(1)
								wait(TweenFarm(CFrame.new(5702.2724609375, 601.94860839844, 201.07873535156)))
							end
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat Kilo Admiral (0/1)" then
						if game:GetService("Workspace").Enemies:FindFirstChild('Kilo Admiral [Lv. 1750] [Boss]') then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == 'Kilo Admiral [Lv. 1750] [Boss]' then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											local args = {
												[1] = "Buso"
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										game:GetService("VirtualUser"):CaptureController()
										game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									until not _G.Auto_Rainbow_Haki or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
								end
							end
						else
							if (CFrame.new(2861.53515625, 423.58441162109, -7254.0751953125).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2500 then
								bypasstp(CFrame.new(2861.53515625, 423.58441162109, -7254.0751953125))
							else
								wait(1)
								wait(TweenFarm(CFrame.new(2861.53515625, 423.58441162109, -7254.0751953125)))
							end
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat Captain Elephant (0/1)" then
						if game:GetService("Workspace").Enemies:FindFirstChild('Captain Elephant [Lv. 1875] [Boss]') then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == 'Captain Elephant [Lv. 1875] [Boss]' then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											local args = {
												[1] = "Buso"
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										game:GetService("VirtualUser"):CaptureController()
										game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									until not _G.Auto_Rainbow_Haki or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
								end
							end
						else
							if (CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2500 then
								local args = {
									[1] = "requestEntrance",
									[2] = Vector3.new(-12462.1162109375, 374.94024658203125, -7543.33251953125)
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							else
								wait(1)
								wait(TweenFarm(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875)))
							end
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat Beautiful Pirate (0/1)" then
						if game:GetService("Workspace").Enemies:FindFirstChild('Beautiful Pirate [Lv. 1950] [Boss]') then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == 'Beautiful Pirate [Lv. 1950] [Boss]' then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											local args = {
												[1] = "Buso"
											}
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
										EquipWeapon(_G.Select_Weapon)
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										game:GetService("VirtualUser"):CaptureController()
										game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
									until not _G.Auto_Rainbow_Haki or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
								end
							end
						else
							if (CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2500 then
								local args = {
									[1] = "requestEntrance",
									[2] = Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656)
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							else
								wait(1)
								wait(TweenFarm(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875)))
							end
						end
					end
				end
			end
		end)
	end
end)

Sector6:AddToggle("Auto Observations V2",_G.Save['Auto_Observations_V2'],function(t)
	_G.Auto_Observations_V2 = t
	_G.Save['Auto_Observations_V2'] = value
	if t == false then
		TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
	end
	
    SaveSetting()
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Observations_V2 then
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					TweenFarm(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
					if (CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
						bypasstp(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
					else
						wait(1)
						TweenFarm(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
					end
					if (CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","CitizenQuest",1)
					else
						wait(1)
						TweenFarm(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
					end
				else
					if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Defeat 50 Forest Pirates") then
						if game:GetService("Workspace").Enemies:FindFirstChild("Forest Pirate [Lv. 1825]") then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == "Forest Pirate [Lv. 1825]" then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
										end
										EquipWeapon(_G.Select_Weapon)
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(1,20,1))
										if sethiddenproperty then
											sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
										end
										v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(50,50,50)
										game:GetService'VirtualUser':CaptureController()
										game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
										PosHee = v.HumanoidRootPart.CFrame
										StatrMagnet = true
									until _G.Auto_Observations_V2 == false or v.Humanoid.Health <= 0
									StatrMagnet = false
								end
							end
						else
							TweenFarm(CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625))
							if (CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
								bypasstp(CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625))
							else
								wait(1)
								TweenFarm(CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625))
							end
						end
					elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat Captain Elephant (0/1)" then 
						if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant [Lv. 1875] [Boss]") then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == "Captain Elephant [Lv. 1875] [Boss]" then
									repeat wait()
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
										end
										EquipWeapon(_G.Select_Weapon)
										TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(1,20,1))										
										if sethiddenproperty then
											sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
										end
										v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(50,50,50)
										game:GetService'VirtualUser':CaptureController()
										game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									until _G.Auto_Observations_V2 == false or v.Humanoid.Health <= 0
								end
							end
						else
							TweenFarm(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875))
							if (CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
								bypasstp(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875)) 
							else
								wait(1)
								TweenFarm(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875))
							end
						end 
					end
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Banana") and  game.Players.LocalPlayer.Backpack:FindFirstChild("Apple") and game.Players.LocalPlayer.Backpack:FindFirstChild("Pineapple") then
						TweenFarm(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
					elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Fruit Bowl") or game.Players.LocalPlayer.Character:FindFirstChild("Fruit Bowl") then
						TweenFarm(CFrame.new(-10920.125, 624.20275878906, -10266.995117188))
					else
						for i,v in pairs(game.Workspace:GetDescendants()) do
							if v.Name == "Apple" or v.Name == "Banana" or v.Name == "Pineapple" then
								v.Handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,1,10)
								wait()
								firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart,v.Handle,0)    
								wait()
							end
						end 
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
				if _G.Auto_Observations_V2 and StatrMagnet  then
					if (v.Name == "Forest Pirate [Lv. 1825]") and (v.HumanoidRootPart.Position - PosHee.Position).Magnitude <= 300 then
                        v.Head.CanCollide = false
                        v.HumanoidRootPart.CanCollide = false
                        v.Humanoid.Sit = false
                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                        v.HumanoidRootPart.CFrame = PosHee
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
					end
				end
			end
		end)
	end)
end)
Sector6:AddToggle("Auto Trade Death King",_G.Save['Auto_Trade_Death_King'],function(t)
	_G.Auto_Trade_Death_King = t
	if t == false then
		_G.Save['Auto_Trade_Death_King'] = t
	SaveSetting()

	end
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Auto_Trade_Death_King then
				local args = {
					[1] = "Bones",
					[2] = "Buy",
					[3] = 1,
					[4] = 1
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end
		end)
	end
end)

Sector6:AddToggle("Auto SwanGlasses",_G.Save['SwanGlasses'],function(t)
	_G.SwanGlasses = t
	if t == false then
		TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
		_G.Save['SwanGlasses'] = t
	SaveSetting()
	end
end)
spawn(function()
	while wait() do
		if _G.SwanGlasses then
			if game:GetService("Workspace").Enemies:FindFirstChild("Don Swan [Lv. 1000] [Boss]") then
				for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
					if v.Name == "Don Swan [Lv. 1000] [Boss]" and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
						repeat wait()
							pcall(function()
								if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
									local args = {
										[1] = "Buso"
									}
									game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
								end
								EquipWeapon(_G.Select_Weapon)
								v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
								v.HumanoidRootPart.CanCollide = false
								TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(1,20,1))
								game:GetService'VirtualUser':CaptureController()
								game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
							end)
						until _G.SwanGlasses == false or v.Humanoid.Health <= 0
					end
				end
			end
		end
	end
end)

Sector6:AddSeperator("Sea Beasts")


Sector6:AddToggle("Auto Farm Sea Beasts",_G.Save['SEAKING'],function(t)
	_G.SEAKING = t
	if t == false then
		TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
	end
	_G.Save['SEAKING'] = value
    SaveSetting()
end)
Sector6:AddToggle("Auto Farm Sea Beasts Hop",_G.Save['SEAKINGHOP'],function(t)
	_G.SEAKINGHOP = t
	if t == false then
		TweenFarm(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
	end
	_G.Save['SEAKINGHOP'] = value
    SaveSetting()
end)
spawn(function()
	while wait() do
		pcall(function()
			if _G.SEAKING then
				for i,v in pairs(game.Workspace.SeaBeasts:GetChildren()) do
					if v:FindFirstChild("HumanoidRootPart") then
						_G.SEAKINGHOP = false
						TweenFarm(v.HumanoidRootPart.CFrame * CFrame.new(1,100,1))
					end
				end
				if _G.SEAKINGHOP then
					if not game.Workspace.SeaBeasts:FindFirstChild('HumanoidRootPart') then
						Hop()
					end
				end
			end
		end)
	end
end)

local Sector7 = Tab1:CreateSector("Fighting style","Reft")
Sector7:AddToggle("Auto Superhuman",_G.Save['Superhuman'],function(value)
	_G.Superhuman = value
	_G.Save['Superhuman'] = value
    SaveSetting()
end)

spawn(function()
	while wait() do
		if _G.Superhuman and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
			if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
				local args = {
					[1] = "BuyBlackLeg"
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end   
			if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
				_G.Select_Weapon = "Superhuman"
			end  
			if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299 then
					_G.Select_Weapon = "Black Leg"
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299 then
					_G.Select_Weapon = "Electro"
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299 then
					_G.Select_Weapon = "Fishman Karate"
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299 then
					_G.Select_Weapon = "Dragon Claw"
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300 then
					local args = {
						[1] = "BuyElectro"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
				if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300 then
					local args = {
						[1] = "BuyElectro"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 300 then
					local args = {
						[1] = "BuyFishmanKarate"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
				if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300 then
					local args = {
						[1] = "BuyFishmanKarate"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300 then
					local args = {
						[1] = "BlackbeardReward",
						[2] = "DragonClaw",
						[3] = "1"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					local args = {
						[1] = "BlackbeardReward",
						[2] = "DragonClaw",
						[3] = "2"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
				end
				if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300 then
					local args = {
						[1] = "BlackbeardReward",
						[2] = "DragonClaw",
						[3] = "1"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					local args = {
						[1] = "BlackbeardReward",
						[2] = "DragonClaw",
						[3] = "2"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
				end
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 then
					local args = {
						[1] = "BuySuperhuman"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
				if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 then
					local args = {
						[1] = "BuySuperhuman"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end 
			end
		end
	end
end)
Sector7:AddToggle("Auto Dagon Talon",_G.Save['DargonTalon'],function(t)
	_G.DargonTalon = t
	if t then
		local args = {
			[1] = "BlackbeardReward",
			[2] = "DragonClaw",
			[3] = "2"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end
	_G.Save['DargonTalon'] = t
    SaveSetting()
end)
spawn(function()
	if _G.DargonTalon and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
		if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
			_G.Select_Weapon = "Dragon Claw"
		end
		if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
			_G.Select_Weapon = "Dragon Claw"
		end
		if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
			_G.Select_Weapon = "Dragon Claw"
			if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
				local string_1 = "Bones";
				local string_2 = "Buy";
				local number_1 = 1;
				local number_2 = 1;
				local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
				Target:InvokeServer(string_1, string_2, number_1, number_2);

				local string_1 = "BuyDragonTalon";
				local bool_1 = true;
				local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
				Target:InvokeServer(string_1, bool_1);
			elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
				game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
			else
				local string_1 = "BuyDragonTalon";
				local bool_1 = true;
				local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
				Target:InvokeServer(string_1, bool_1);
				local string_1 = "BuyDragonTalon";
				local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
				Target:InvokeServer(string_1);
			end 
		end
	end
end)
Sector7:AddToggle("Auto Death Step",_G.Save['DeathStep'],function(value)
	_G.DeathStep = value
	if t then
		local args = {
			[1] = "BuyBlackLeg"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end
	_G.Save['DeathStep'] = value
    SaveSetting()
end)
spawn(function() 
    
	while wait() do
		pcall(function()
			if _G.DeathStep and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 400 then
					local args = {
						[1] = "BuyDeathStep"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					_G.Select_Weapon = "Death Step"
				end  
				if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 400 then
					local args = {
						[1] = "BuyDeathStep"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					
					_G.Select_Weapon = "Death Step"
				end  
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value < 400 then
					_G.Select_Weapon = "Black Leg"
				end 
			end
		end)
	end
end)
Sector7:AddToggle("Auto Electric Claw",_G.Save['Electricclow'],function(t)
	_G.Electricclow = t
	if t then
		local args = {
			[1] = "BuyElectro"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end
	_G.Save['Electricclow'] = t
    SaveSetting()
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Electricclow and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value < 400 then
					
					_G.Select_Weapon = "Electro"
				end  
				if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value < 400 then
					_G.Select_Weapon = "Electro"
				end  
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400 then
					local v175 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true);
					if v175 == 4 then
						local v176 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", "Start");
						if v176 == nil then
							TweenFarm(CFrame.new(-12548, 337, -7481))
						end
					else
						local args = {
							[1] = "BuyElectricClaw"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					end
				end
				if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400 then
					local v175 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true);
					if v175 == 4 then
						local v176 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", "Start");
						if v176 == nil then
							TweenFarm(CFrame.new(-12548, 337, -7481))
						end
					else
						local args = {
							[1] = "BuyElectricClaw"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					end
				end
			end
		end)
	end
end)

local Tab2 = EdogHub1:CreateTab("Character - Players")

local Sector8 = Tab2:CreateSector("Auto Stats","left")
Sector8:AddToggle("Auto Melee",_G.Save['Auto_Melee'],function(t)
	_G.Melee = t
	_G.Save['Auto_Melee'] = t
	SaveSetting()
end)
Sector8:AddToggle("Auto Defense",_G.Save['Auto_Defense'],function(t)
	_G.Defense = t
	_G.Save['Auto_Defense'] = t
	SaveSetting()
end)
Sector8:AddToggle("Auto Sword",_G.Save['Auto_Sword'],function(t)
	_G.Sword = t
	_G.Save['Auto_Sword'] = t
	SaveSetting()
end)
Sector8:AddToggle("Auto Gun",_G.Save['Auto_Gun'],function(t)
	_G.Gun = t
	_G.Save['Auto_Gun'] = t
	SaveSetting()
end)
Sector8:AddToggle("Auto Blox Fruit",_G.Save['Auto_Blox_Fruit'],function(t)
	_G.Blox_Fruit = t
	_G.Save['Auto_Blox_Fruit'] = t
	SaveSetting()
end)
PointStats = 1
Sector8:AddSlider("Point",1,PointStats,100,1,function(value)
	PointStats = value
end)
spawn(function()
	while wait() do
	   	if game.Players.localPlayer.Data.Points.Value >= PointStats then
			if _G.Melee then
				local args = {
					[1] = "AddPoint",
					[2] = "Melee",
					[3] = PointStats
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end 
			if _G.Defense then
				local args = {
					[1] = "AddPoint",
					[2] = "Defense",
					[3] = PointStats
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end 
			if _G.Sword then
				local args = {
					[1] = "AddPoint",
					[2] = "Sword",
					[3] = PointStats
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end 
			if _G.Gun then
				local args = {
					[1] = "AddPoint",
					[2] = "Gun",
					[3] = PointStats
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end 
			if _G.Blox_Fruit then
				local args = {
					[1] = "AddPoint",
					[2] = "Demon Fruit",
					[3] = PointStats
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end
		end
	end
end)
local Sector9 = Tab2:CreateSector("ESP","Reft")
function isnil(thing)
	return (thing == nil)
end
local function round(n)
	return math.floor(tonumber(n) + 0.5)
end
Number = math.random(1, 1000000)
function UpdatePlayerChams()
	for i,v in pairs(game:GetService'Players':GetChildren()) do
		pcall(function()
			if not isnil(v.Character) then
				if ESPPlayer then
					if not isnil(v.Character.Head) and not v.Character.Head:FindFirstChild('NameEsp'..Number) then
						local bill = Instance.new('BillboardGui',v.Character.Head)
						bill.Name = 'NameEsp'..Number
						bill.ExtentsOffset = Vector3.new(0, 1, 0)
						bill.Size = UDim2.new(1,200,1,30)
						bill.Adornee = v.Character.Head
						bill.AlwaysOnTop = true
						local name = Instance.new('TextLabel',bill)
						name.Font = "GothamBold"
						name.FontSize = "Size14"
						name.TextWrapped = true
						name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
						name.Size = UDim2.new(1,0,1,0)
						name.TextYAlignment = 'Top'
						name.BackgroundTransparency = 1
						name.TextStrokeTransparency = 0.5
						if v.Team == game.Players.LocalPlayer.Team then
							name.TextColor3 = Color3.new(0,255,0)
						else
							name.TextColor3 = Color3.new(255,0,0)
						end
					else
						v.Character.Head['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
					end
				else
					if v.Character.Head:FindFirstChild('NameEsp'..Number) then
						v.Character.Head:FindFirstChild('NameEsp'..Number):Destroy()
					end
				end
			end
		end)
	end
end
function UpdateChestChams() 
	for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			if string.find(v.Name,"Chest") then
				if ChestESP then
					if string.find(v.Name,"Chest") then
						if not v:FindFirstChild('NameEsp'..Number) then
							local bill = Instance.new('BillboardGui',v)
							bill.Name = 'NameEsp'..Number
							bill.ExtentsOffset = Vector3.new(0, 1, 0)
							bill.Size = UDim2.new(1,200,1,30)
							bill.Adornee = v
							bill.AlwaysOnTop = true
							local name = Instance.new('TextLabel',bill)
							name.Font = "GothamBold"
							name.FontSize = "Size14"
							name.TextWrapped = true
							name.Size = UDim2.new(1,0,1,0)
							name.TextYAlignment = 'Top'
							name.BackgroundTransparency = 1
							name.TextStrokeTransparency = 0.5
							if v.Name == "Chest1" then
								name.TextColor3 = Color3.fromRGB(109, 109, 109)
								name.Text = ("Chest 1" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							end
							if v.Name == "Chest2" then
								name.TextColor3 = Color3.fromRGB(173, 158, 21)
								name.Text = ("Chest 2" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							end
							if v.Name == "Chest3" then
								name.TextColor3 = Color3.fromRGB(85, 255, 255)
								name.Text = ("Chest 3" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
							end
						else
							v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
						end
					end
				else
					if v:FindFirstChild('NameEsp'..Number) then
						v:FindFirstChild('NameEsp'..Number):Destroy()
					end
				end
			end
		end)
	end
end
Sector9:AddToggle("ESP Players",_G.Save['ESPPlayer'],function(t)
	ESPPlayer = t
	UpdatePlayerChams()
	_G.Save['ESPPlayer'] = value
    SaveSetting()
end)
Sector9:AddToggle("ESP Chest",_G.Save['ChestESP'],function(t)
	ChestESP = t
	UpdateChestChams()
	_G.Save['ChestESP'] = value
    SaveSetting() 
end)

local Sector10 = Tab2:CreateSector("Players","left")

PlayersList = {}

for i,v in pairs(game:GetService("Players"):GetChildren()) do
	table.insert(PlayersList,v.Name)
end

Sector10:AddDropdown("Select Players",PlayersList,"Select Players",false,function(t)
	_G.Select_Players = t
end)
Sector10:AddToggle("Kill Player",false,function(bool)
	KillPlayer = bool
	KillTween = bool
end)
Sector10:AddToggle("Aimbot Gun",false,function(bool)
	if _G.Select_Players == "" and bool then
		Aimbot = bool
	end
end)
Sector10:AddToggle("AutoEquipGun",false,function(value)
    _G.AutoEquipGun = value
	while _G.AutoEquipGun  == true do
		wait(2)
			for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
				if v.ClassName == "Tool" then
					if v.ToolTip == "Gun" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							local ToolSe = tostring(v.Name)
							local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
							game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
						end
					end
				end
			end

		print("test")
		end
end)
local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
	if Aimbot and game.Players.LocalPlayer.Character:FindFirstChild(_G.AutoEquipGun) and game:GetService("Players"):FindFirstChild(_G.Select_Players) then
		tool = game:GetService("Players").LocalPlayer.Character[_G.AutoEquipGun]
		v17 = workspace:FindPartOnRayWithIgnoreList(Ray.new(tool.Handle.CFrame.p, (game:GetService("Players"):FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Position - tool.Handle.CFrame.p).unit * 100), { game.Players.LocalPlayer.Character, workspace._WorldOrigin });
		game:GetService("Players").LocalPlayer.Character[_G.AutoEquipGun].RemoteFunctionShoot:InvokeServer(game:GetService("Players"):FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Position, (require(game.ReplicatedStorage.Util).Other.hrpFromPart(v17)));
	end 
end)
Sector10:AddButton("Reset Character",function(t)
	game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)
Sector10:AddToggle("Teleport To Players",false,function(t)
	_G.TeleportPlayer = t
end)
Sector10:AddToggle("Spectate Player",false,function(t)
	Sp = t
	local plr1 = game.Players.LocalPlayer.Character.Humanoid
	local plr2 = game.Players:FindFirstChild(_G.Select_Players)
	repeat wait(.1)
	   game.Workspace.Camera.CameraSubject = plr2.Character.Humanoid
	until Sp == false 
	game.Workspace.Camera.CameraSubject = game.Players.LocalPlayer.Character.Humanoid
end)
Sector10:AddToggle("Kill Player Behind",false,function(bool)
	KillPlayer = bool
end)
Sector10:AddToggle("Bring Players",false,function(bool)
	_G.BringPlayer = bool
end)
spawn(function()
	while wait() do
		if _G.BringPlayer then
			pcall(function()
				game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-3)
			end)
		end
	end
end)

spawn(function()
	while wait() do
		if KillPlayer then
			game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.CFrame * CFrame.new(0,0,distance)
			game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Size = Vector3.new(60,60,60)
			game.Players.LocalPlayer.Character.Humanoid.Health = 0
						wait(0.5)
														local args = {
															[1] = "SetSpawnPoint"
														}
														
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				
			game:GetService'VirtualUser':CaptureController()
			game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
			
		end
	end
end)
spawn(function()
	while wait() do
		if KillPlayer then
			if game.Players:FindFirstChild(_G.Select_Players) and (game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude >= 300 then
				KillTween = toTarget(game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Position,game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.CFrame)
			elseif game.Players:FindFirstChild(_G.Select_Players) and (game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude >= 300 then
				game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.CFrame * CFrame.new(0,25,0)
				game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.CanCollide = false
				game.Players:FindFirstChild(_G.Select_Players).Character.HumanoidRootPart.Size = Vector3.new(50,50,50)
				EquipWeapon(_G.AutoEquipGun)
				if game.Players.LocalPlayer.Character:FindFirstChild(_G.AutoEquipGun) then
					spawn(function()
						pcall(function()
							local args = {
								[1] = v.HumanoidRootPart.Position,
								[2] = v.HumanoidRootPart
							}
							game:GetService("Players").LocalPlayer.Character[SelectToolWeaponGun].RemoteFunctionShoot:InvokeServer(unpack(args))
						end)
					end)
				end 
			end
		end 
		if Skillaimbot then
			if game.Players:FindFirstChild(_G.Select_Players) and game.Players:FindFirstChild(_G.Select_Players).Character:FindFirstChild("HumanoidRootPart") and game.Players:FindFirstChild(_G.Select_Players).Character:FindFirstChild("Humanoid") and game.Players:FindFirstChild(_G.Select_Players).Character.Humanoid.Health > 0 then
				AimBotSkillPosition = game.Players:FindFirstChild(_G.Select_Players).Character:FindFirstChild("HumanoidRootPart").Position
			end
		end
	end
end)
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
					if UseSkillMasteryDevilFruit then
						args[2] = PositionSkillMasteryDevilFruit
						return old(unpack(args))
					elseif Skillaimbot then
						args[2] = AimBotSkillPosition
						return old(unpack(args))
					end
				end
			end
		end
		return old(...)
	end)
end)
spawn(function()
	while wait() do
		pcall(function()
			if _G.TeleportPlayer then
				if (game.Players[_G.Select_Players].Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
					bypasstp(game.Players[_G.Select_Players].Character.HumanoidRootPart.CFrame * CFrame.new(0,0,0))
				else
					wait(1)
					TweenFarm(game.Players[_G.Select_Players].Character.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
				end
			end
		end)
	end
end)

local Tab3 = EdogHub1:CreateTab("Teleport - Raids")
local Sector12 = Tab3:CreateSector("Teleport","left")

Sector12:AddSeperator("Teleport World")
if OldWorld or NewWorld or ThreeWorld then
	Sector12:AddButton("Teleport to First World",function()
		local args = {
			[1] = "TravelMain"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end)
end
if OldWorld or NewWorld then
	Sector12:AddButton("Teleport to Second World",function()
		local args = {
			[1] = "DressrosaQuestProgress",
			[2] = "Dressrosa"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		local args = {
			[1] = "TravelDressrosa"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end)
end
if NewWorld or ThreeWorld then
	Sector12:AddButton("Teleport to Third World",function()
		local args = {
			[1] = "ZQuestProgress",
			[2] = "Zou"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		local args = {
			[1] = "TravelZou"
		}
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	end)
end

Sector12:AddSeperator("Teleport Island")

placeinGAME = {}
for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
    if v.Name == "Sea" or string.find(v.Name,"Island ") then
    else
        table.insert(placeinGAME,v.Name)
    end
end
Sector12:AddDropdown("Select Place",placeinGAME,"Select here",false,function(t)
	tpto = t
end)
Sector12:AddToggle("Tween to Place",false,function(statetp)
	statetp1 = statetp
    if statetp1 then
        repeat wait()
            Nocliptp = true
            if game:GetService("Workspace")["_WorldOrigin"].Locations[tpto].Position.Y < 1 then
                TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations[tpto].CFrame*CFrame.new(0,1000,0))
            elseif game:GetService("Workspace")["_WorldOrigin"].Locations[tpto].Position.Y < 300 then
                TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations[tpto].CFrame*CFrame.new(0,700,0))
            else
                TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations[tpto].CFrame*CFrame.new(0,500,0))
            end
        until not statetp1 or raidiing
        Nocliptp = false
    end 
end)
local Sector13 = Tab3:CreateSector("Server","Reft")

Sector13:AddButton("Re join",function()
	game:GetService("TeleportService"):Teleport(game.PlaceId)
end)
Sector13:AddButton("Server Hop",function()
	Hop()
end)
function HopLowerServer()
	local maxplayers, gamelink, goodserver, data_table = math.huge, "https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100"
	if not _G.FailedServerID then _G.FailedServerID = {} end
	local function serversearch()
		data_table = game:GetService"HttpService":JSONDecode(game:HttpGetAsync(gamelink))
		for _, v in pairs(data_table.data) do
			pcall(function()
				if type(v) == "table" and v.id and v.playing and tonumber(maxplayers) > tonumber(v.playing) and not table.find(_G.FailedServerID, v.id) then
					maxplayers = v.playing
					goodserver = v.id
				end
			end)
		end
	end
	function getservers()
		pcall(serversearch)
		for i, v in pairs(data_table) do
			if i == "nextPageCursor" then
				if gamelink:find"&cursor=" then
					local a = gamelink:find"&cursor="
					local b = gamelink:sub(a)
					gamelink = gamelink:gsub(b, "")
				end
				gamelink = gamelink .. "&cursor=" .. v
				pcall(getservers)
			end
		end
	end
	pcall(getservers)
	if goodserver == game.JobId or maxplayers == #game:GetService"Players":GetChildren() - 1 then
	end
	table.insert(_G.FailedServerID, goodserver)
	game:GetService"TeleportService":TeleportToPlaceInstance(game.PlaceId, goodserver)
end

Sector13:AddButton("Low People",function()
	HopLowerServer()
end)

local Sector14 = Tab3:CreateSector("Dungeon","Reft")

Sector14:AddSeperator("Raids")
Sector14:AddDropdown("Select Dungeon",{"Flame","Ice","Quake","Light","Dark","String","Rumble","Magma","Human: Buddha","Sand"},"Select Dungeon",false,function(vu)
	_G.SelectRaid = vu
	_G.Save['SelectRaid'] = vu
	SaveSetting()
end)
Sector14:AddToggle("Auto Dungeon",_G.Save['AutoRaid'],function(t)
	_G.AutoRaid = t
	_G.Save['AutoRaid'] = vu
	SaveSetting()
end)
Sector14:AddToggle("Kill Aura",_G.Save['Killaura'],function(t)
	Killaura = t
	_G.Save['Killaura'] = vu
	SaveSetting()
end)
Sector14:AddToggle("Auto Next Island",_G.Save['NextIsland'],function(t)
	NextIsland = t
	_G.Save['NextIsland'] = vu
	SaveSetting()
end)
Sector14:AddToggle("Auto Awakenr", _G.Save['AutoAwakener'],function(vu)
    AutoAwakener = vu
	_G.Save['AutoAwakener'] = vu
	SaveSetting()
end)
spawn(function()
	while wait(.1) do
		if _G.AutoRaid or RaidSuperhuman then
			pcall(function()
				if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == false then
					if AutoSuperhuman then
						if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") and not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") then
							for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
								if not string.find(v.Name, "Fruit") then
									game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin","Buy")
								end
							end
						end
					end
					if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc", "Select", _G.SelectRaid)
					end
					if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
						print('1')
					end
					if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") and game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") or  game.Players.LocalPlayer.Character:FindFirstChild("Special Microchip")  then
						if NewWorld then
							fireclickdetector(game:GetService("Workspace").Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
						elseif ThreeWorld then
							fireclickdetector(game:GetService("Workspace").Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
						end
					end
				end
			end)
		end
	end
end)

spawn(function()
	pcall(function()
		while wait(.1) do
			if AutoAwakener then
				local args = {
					[1] = "Awakener",
					[2] = "Check"
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				local args = {
					[1] = "Awakener",
					[2] = "Awaken"
				}
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			end
		end
	end)
end)

spawn(function()
    while wait() do
        if Killaura or _G.AutoRaid or RaidSuperhuman then
            for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                    pcall(function()
                        repeat wait(.1)
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            v.Humanoid.Health = 0
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            v.HumanoidRootPart.Transparency = 0.8
                        until not Killaura or not _G.AutoRaid or not RaidSuperhuman or not v.Parent or v.Humanoid.Health <= 0
                    end)
                end
            end
        end
    end
end)

spawn(function()
	pcall(function()
		while game:GetService("RunService").Heartbeat:wait() do
			if NextIsland or RaidSuperhuman or _G.AutoRaid then
				if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true and game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
					if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
						TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 5"].CFrame*CFrame.new(4,65,10))
					elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
						TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 4"].CFrame*CFrame.new(4,65,10))
					elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
						TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 3"].CFrame*CFrame.new(4,65,10))
					elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
						TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 2"].CFrame*CFrame.new(4,65,10))
					elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
						TweenFarm(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 1"].CFrame*CFrame.new(4,65,10))
					end
				elseif NewWorld then
					TweenFarm(CFrame.new(-6438.73535, 250.645355, -4501.50684))
				elseif ThreeWorld then
					TweenFarm(CFrame.new(-5057.146484375, 314.54132080078, -2934.7995605469))
				end
			end
		end
	end)
end)
local Tab4 = EdogHub1:CreateTab("Settings - Misc")

local Sector15 = Tab4:CreateSector("Shop","left")

Sector15:AddSeperator("fighting style")

Sector15:AddButton("BlackLeg",function()
    local args = {
        [1] = "BuyBlackLeg"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("FishmanKarate",function()
local args = {
	[1] = "BuyFishmanKarate"
}
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Electro",function()
    local args = {
        [1] = "BuyElectro"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

end)
Sector15:AddButton("DragonClaw",function()
    local args = {
        [1] = "BlackbeardReward",
        [2] = "DragonClaw",
        [3] = "1"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BlackbeardReward",
        [2] = "DragonClaw",
        [3] = "2"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Superhuman",function()
    local args = {
        [1] = "BuySuperhuman"
    }

    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("DeathStep",function()
    local args = {
        [1] = "BuyDeathStep"
    }

    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("SharkmanKarate",function()
	local args = {
		[1] = "BuySharkmanKarate",
		[2] = true
	}
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
	local args = {
		[1] = "BuySharkmanKarate"
	}
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("BuyElectricClaw",function()
    local args = {
        [1] = "BuyElectricClaw"
        }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("BuyDragonTalon",function()
    local args = {
        [1] = "BuyDragonTalon",
        [2] = true
        }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyDragonTalon"
        }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddSeperator("style")

Sector15:AddButton("Sky Jump",function()
	local args = {
        [1] = "BuyHaki",
        [2] = "Geppo"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Buso Haki",function()
	local args = {
        [1] = "BuyHaki",
        [2] = "Buso"
    }

    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Soru",function()
	local args = {
        [1] = "BuyHaki",
        [2] = "Soru"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Observation haki",function()
	local args = {
        [1] = "KenTalk",
        [2] = "Buy"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddSeperator("Sworld")
Sector15:AddButton("Katana ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Cutlass ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Cutlass"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

Sector15:AddButton("Dual Katana",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Dual Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Iron Mace",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Iron Mace"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Triple Katana",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Triple Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Pipe",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Pipe"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Soul Cane",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Soul Cane"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Dual-Headed Blade ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Dual-Headed Blade"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Bisento",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Bisento"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Buy AllSword",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Bisento"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Dual-Headed Blade"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Soul Cane"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Pipe"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Triple Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Iron Mace"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Dual Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Cutlass"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BuyItem",
        [2] = "Katana"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddSeperator("Gun")
Sector15:AddButton("Slingshot ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Slingshot"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Musket ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Musket"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Flintlock ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Flintlock"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Refined Slingshot ",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Refined Slingshot"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Refined Flintlock",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Refined Flintlock"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Kabucha)",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Kabucha"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddSeperator("Acces")
Sector15:AddButton("Black Cape",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Black Cape"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Swordsman Hat",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Swordsman Hat"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Tomoe Ring",function(Value)
    local args = {
        [1] = "BuyItem",
        [2] = "Tomoe Ring"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddSeperator("Fragments")
Sector15:AddButton("Race Ghoul",function()
    local args = {
        [1] = "Ectoplasm",
        [2] = "BuyCheck",
        [3] = 4
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "Ectoplasm",
        [2] = "Change",
        [3] = 4
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Race Cyborg",function()
    local args = {
        [1] = "CyborgTrainer",
        [2] = "Buy"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Random Race ",function()
    local args = {
        [1] = "BlackbeardReward",
        [2] = "Reroll",
        [3] = "2"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector15:AddButton("Reset Stats ",function()
    local args = {
        [1] = "BlackbeardReward",
        [2] = "Refund",
        [3] = "2"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
local Sector16 = Tab4:CreateSector("Team","Reft")

Sector16:AddButton("Pirates",function()
	local args = {
		[1] = "SetTeam",
		[2] = "Pirates"
	}
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
Sector16:AddButton("Marines",function()
	local args = {
		[1] = "SetTeam",
		[2] = "Marines"
	}
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)
local Sector17 = Tab4:CreateSector("Graphics","Reft")
Sector17:AddButton("FPS Boost", function()
	local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
	local g = game
	local w = g.Workspace
	local l = g.Lighting
	local t = w.Terrain
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
end)
Sector17:AddButton("Super FPS Boost", function()
	for i,v in pairs(game.Workspace.Map:GetDescendants()) do
		if v.Name == "Tavern" or v.Name == "SmileFactory" or v.Name == "Tree" or v.Name == "Rocks" or v.Name == "PartHouse" or v.Name == "Hotel" or v.Name == "WallPiece" or v.Name == "MiddlePillars" or v.Name == "Cloud" or v.Name == "PluginGrass" or v.Name == "BigHouse" or v.Name == "SmallHouse" or v.Name == "Detail" then
			v:Destroy()
		end
	end 
	for i,v in pairs(game.ReplicatedStorage.Unloaded:GetDescendants()) do
		if v.Name == "Tavern" or v.Name == "SmileFactory" or v.Name == "Tree" or v.Name == "Rocks" or v.Name == "PartHouse" or v.Name == "Hotel" or v.Name == "WallPiece" or v.Name == "MiddlePillars" or v.Name == "Cloud" or v.Name == "PluginGrass" or v.Name == "BigHouse" or v.Name == "SmallHouse" or v.Name == "Detail" then
			v:Destroy()
		end
	end
	for i,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
		if v:IsA("Accessory") or v.Name == "Pants" or v.Name == "Shirt" then
			v:Destroy()
		end
	end
	local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
	local g = game
	local w = g.Workspace
	local l = g.Lighting
	local t = w.Terrain
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
end)
Sector17:AddToggle("Whlite Screen",false,function(value)
	ws = value
		if ws == true then
			ws = true
			game:GetService("RunService"):Set3dRenderingEnabled(false)
		else 
		   ws = false 
			game:GetService("RunService"):Set3dRenderingEnabled(true)
		end 
	

end)
Sector17:AddButton("Head Fire",function()
	local Fire = Instance.new("Fire")
	Fire.Parent = game.Players.LocalPlayer.Character.Head
	Fire.Heat = 5
	Fire.Size = 5
	for i,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
			if v:IsA("Accessory")  then
				v:Destroy()
			end
		end
    
end)
Sector17:AddButton("Sit",function()
	game.Players.LocalPlayer.Character.Humanoid.Sit = true
    
end)
Sector17:AddButton("Sit Ice Wall",function()
	game.Players.LocalPlayer.Character.Humanoid.Sit = true

	local a = Instance.new("Part",game:GetService("Workspace"))
	a.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
	a.Anchored = true
	a.Size = Vector3.new(20,10,3)
	a.BrickColor = BrickColor.new("Pastel Blue")
end)
Sector17:AddButton("Av",function()
	local Fire = Instance.new("Fire")
Fire.Parent = game.Players.LocalPlayer.Character.RightHand
Fire.Heat = 5
Fire.Size = 5
local Fire = Instance.new("Fire")
Fire.Parent = game.Players.LocalPlayer.Character.LeftHand
Fire.Heat = 5
Fire.Size = 5
    
end)
Sector17:AddButton("HandFire",function()
	local Fire = Instance.new("Fire")
Fire.Parent = game.Players.LocalPlayer.Character.RightHand
Fire.Heat = 5
Fire.Size = 5
local Fire = Instance.new("Fire")
Fire.Parent = game.Players.LocalPlayer.Character.LeftHand
Fire.Heat = 5
Fire.Size = 5
    
end)
        ws = false
        game:GetService("UserInputService").InputBegan:Connect(function(input,chat)
            if chat then return end
            if input.KeyCode == Enum.KeyCode.P then 
                if ws == false then
                    ws = true
                    game:GetService("RunService"):Set3dRenderingEnabled(false)
                else 
                   ws = false 
                    game:GetService("RunService"):Set3dRenderingEnabled(true)
                end 
            end
        end)

