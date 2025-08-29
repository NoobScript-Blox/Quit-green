-- Script Local para Roblox: UI MR.QUIT com botão de sair do jogo
-- UI arredondada, botão logo abaixo do nome, digital canto inferior esquerdo
-- Mensagem de quit: "Clicou Quitou -Mr.Green dd/mm/aaaa"
-- Coloque este script em StarterPlayerScripts ou execute como LocalScript

local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Função para expulsar o jogador do jogo com mensagem personalizada
local function quitGame()
    -- Data atual formatada
    local date = os.date("%d/%m/%Y")
    local msg = "Clicou Quitou -Mr.Green " .. date
    player:Kick(msg)
end

-- Criação da UI
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "MR_QUIT"
screenGui.Parent = player:WaitForChild("PlayerGui")

-- Fundo Verde (janela menor e arredondada)
local background = Instance.new("Frame")
background.Size = UDim2.new(0, 220, 0, 110)
background.Position = UDim2.new(0.5, -110, 0.5, -55)
background.BackgroundColor3 = Color3.fromRGB(0, 170, 0)
background.BorderSizePixel = 0
background.Parent = screenGui
background.Active = true -- Necessário para Draggable
background.Draggable = true -- Torna a janela movível

-- Arredondamento do fundo
local uiCorner = Instance.new("UICorner")
uiCorner.CornerRadius = UDim.new(0, 16)
uiCorner.Parent = background

-- Título da UI
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 32)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundTransparency = 1
title.Text = "MR.GREEN"
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.Font = Enum.Font.SourceSansBold
title.TextScaled = true
title.Parent = background

-- Botão QUIT logo abaixo do nome, também arredondado
local quitButton = Instance.new("TextButton")
quitButton.Size = UDim2.new(0.7, 0, 0, 28)
quitButton.Position = UDim2.new(0.15, 0, 0, 36)
quitButton.BackgroundColor3 = Color3.fromRGB(85, 255, 127)
quitButton.Text = "QUIT"
quitButton.TextColor3 = Color3.fromRGB(0, 0, 0)
quitButton.Font = Enum.Font.SourceSansBold
quitButton.TextScaled = true
quitButton.Parent = background

-- Arredondamento do botão
local btnCorner = Instance.new("UICorner")
btnCorner.CornerRadius = UDim.new(0, 12)
btnCorner.Parent = quitButton

quitButton.MouseButton1Click:Connect(function()
    quitGame()
end)

-- Símbolo de digital no canto inferior esquerdo
local fingerprint = Instance.new("ImageLabel")
fingerprint.Size = UDim2.new(0, 32, 0, 32)
fingerprint.Position = UDim2.new(0, 4, 1, -36)
fingerprint.BackgroundTransparency = 1
fingerprint.Image = "rbxassetid://14242582203" -- Exemplo de imagem de digital, troque se preferir outro ID
fingerprint.Parent = background
