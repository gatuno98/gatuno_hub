-- Script Hub para Blox Fruits com UI
-- Funciona em PC e Mobile

local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local UIListLayout = Instance.new("UIListLayout")
local AutoFarmButton = Instance.new("TextButton")
local AutoBountyButton = Instance.new("TextButton")
local AutoRaidButton = Instance.new("TextButton")
local ESPButton = Instance.new("TextButton")
local AutoFruitButton = Instance.new("TextButton")
local AutoCDKButton = Instance.new("TextButton")

-- Configuração do UI
ScreenGui.Parent = game.CoreGui
MainFrame.Parent = ScreenGui
MainFrame.Size = UDim2.new(0, 200, 0, 350)
MainFrame.Position = UDim2.new(0.8, 0, 0.2, 0)
MainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)

UIListLayout.Parent = MainFrame
UIListLayout.Padding = UDim.new(0, 5)

-- Função para criar botões
local function CreateButton(name, parent, callback)
    local button = Instance.new("TextButton")
    button.Parent = parent
    button.Size = UDim2.new(1, 0, 0, 50)
    button.Text = name
    button.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.MouseButton1Click:Connect(callback)
    return button
end

-- Criando os botões e funções
CreateButton("Auto Farm", MainFrame, function()
    print("Auto Farm ativado")
    -- Código para farmar NPCs da missão do nível do jogador aqui
end)

CreateButton("Auto Bounty", MainFrame, function()
    print("Auto Bounty ativado")
    -- Código para Auto Bounty aqui
end)

CreateButton("Auto Raid", MainFrame, function()
    print("Auto Raid ativado")
    -- Código para Auto Raid aqui
end)

CreateButton("ESP", MainFrame, function()
    print("ESP ativado")
    -- Código para ESP aqui
end)

CreateButton("Auto Collect Fruits", MainFrame, function()
    print("Auto Collect Fruits ativado")
    -- Código para buscar e coletar frutas no chão aqui
end)

CreateButton("Auto CDK", MainFrame, function()
    print("Auto CDK ativado")
    -- Código para Auto CDK (Cursed Dual Katana) aqui
end)
