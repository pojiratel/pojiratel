loadstring(game:HttpGet("https://raw.githubusercontent.com/TR1V5/TR1V5-V1/main/Main2"))()
loadstring(game:HttpGet('https://pastebin.com/raw/fttSzNs8'))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Schervi/FloppaHub/main/FloppaHubMain.lua"))()
loadstring(game:HttpGet("https://raw.githubusercontent.com/BLACKGAMER1221/Pet-Simulator-X/main/BK%20Pet.lua"))()
local Toggle = false

local GUI = Instance.new("ScreenGui")
local Button = Instance.new("TextButton")

GUI.Name = "GUI"
GUI.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")



Button.Name = "Button"
Button.Parent = GUI
Button.BackgroundColor3 = Color3.new(0.117647, 0.117647, 0.117647)
Button.BackgroundTransparency = 0.30000001192093
Button.BorderSizePixel = 0
Button.Position = UDim2.new(0.5, 0, 0.5, 0)
Button.Size = UDim2.new(0, 83, 0, 34)
Button.Font = Enum.Font.SourceSans
Button.Text = "TOGGLE"
Button.TextColor3 = Color3.new(1, 1, 1)
Button.TextSize = 20
Button.Draggable = true

Button.MouseButton1Click:connect(function()
    Toggle = not Toggle
end)

game:GetService('RunService').Stepped:connect(function()
    if Toggle then
        local args
= {
[1] = {
[1] = "Egg of Many Gifts", --Name EGG
[2] = false
}
}
workspace.__THINGS.__REMOTES:FindFirstChild("buy egg"):InvokeServer(unpack(args))
    end
end)
