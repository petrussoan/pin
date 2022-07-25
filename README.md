	local function work()
			local e = game:GetService("Workspace").Ignored.Handle.Mesh 
			e.MeshId = 'rbxassetid://430748458'
			e.Scale = Vector3.new(0.01, 0.01, 0.01)
			e.TextureId = 'http://www.roblox.com/asset/?id=430751682'
		end
	
		function char()
			for i,v in pairs(game.Players.LocalPlayer:GetDescendants()) do
				if v.Name == "[Grenade]" and v:IsA("Tool") then
					v.Handle.Mesh.MeshId = 'rbxassetid://430748458'
					v.Handle.Mesh.Scale = Vector3.new(0.01, 0.01, 0.01)
					v.Handle.Mesh.TextureId = 'http://www.roblox.com/asset/?id=430751682'
				end
			end
		end
	
		local function hand()
			for i,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
				if v.Name == "[Grenade]" and v:IsA("Tool") then
					v.Handle.Mesh.MeshId = 'rbxassetid://430748458'
					v.Handle.Mesh.Scale = Vector3.new(0.01, 0.01, 0.01)
					v.Handle.Mesh.TextureId = 'http://www.roblox.com/asset/?id=430751682'
				end
			end
		end
	
	
	
		while wait() do
			pcall(function()
				hand()
				char()
				work()
			end)
		end
