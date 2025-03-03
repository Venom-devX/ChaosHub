local Webhook_URL = "https://discord.com/api/webhooks/1344091222918168610/EErNNCtTPtf5pU4ZWk0Xs3mA4Of2uUV0F_78nmiyQ227xNrMTlB1QMyvN9w4LJjw4nqh"
local event = "Chaos Hub Brookhaven Brasil 🇧🇷"
local Players = game:GetService("Players")
local player = Players.LocalPlayer

local username = player.Name -- Nome do jogador
local userId = player.UserId -- ID do jogador
local accountAge = player.AccountAge -- Dias da conta no Roblox
local jobId = game.JobId -- ID do servidor

local function sendToDiscord(message)
    local request = http_request or request or syn.request or http.request
    if not request then
        warn("Executor não suporta HTTP Requests.")
        return
    end

    local data = {
        ["content"] = message,
        ["embeds"] = {{
            ["title"] = "Chaos Hub Brookhaven Executado 🧙‍♀️🇧🇷",
            ["fields"] = {
                {["name"] = "Player:", ["value"] = "```" .. username .. "```", ["inline"] = false},
                {["name"] = "Player ID:", ["value"] = "```" .. tostring(userId) .. "```", ["inline"] = false},
                {["name"] = "Idade da Conta (Dias):", ["value"] = "```" .. tostring(accountAge) .. "```", ["inline"] = false},
                {["name"] = "Server ID:", ["value"] = "```" .. jobId .. "```", ["inline"] = false},
                {["name"] = "Chaos Hub Version:", ["value"] = "```" .. event .. "```", ["inline"] = false}
            },
            ["color"] = 16711680
        }}
    }

    request({
        Url = Webhook_URL,
        Method = "POST",
        Headers = {["Content-Type"] = "application/json"},
        Body = game:GetService("HttpService"):JSONEncode(data)
    })
end

-- Envia a mensagem para o Discord assim que o script for executado
sendToDiscord("Obrigado Por usad Chaos Hub! 🇧🇷🎉🧙‍♀️")

-- Exibe uma mensagem no servidor
game.StarterGui:SetCore("ChatMakeSystemMessage", {
    Text = "Obrigado por usar Chaos Hub! 🇧🇷🧙‍♀️🎉",
    Color = Color3.fromRGB(255, 223, 0),
    Font = Enum.Font.SourceSansBold,
    FontSize = Enum.FontSize.Size24
})

wait(0.3)

local OrionLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/Lusca885/Text-orion/refs/heads/main/README.md"))()

-- Create a window
local Window = OrionLib:MakeWindow({
    Name = "Chaos Hub V1 BROOKHAVEN 🏠",
    HidePremium = false,
    SaveConfig = true,
    IntroText = "Chaos Hub V1 BROOKHAVEN 🏠",
    IntroIcon = "rbxassetid://131669852271916",
    ConfigFolder = "OrionTest"
})

game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName", " 🎩 Bem Vindo ao Chaos HUB 🎩")

local args = {
    [1] = "PickingRPNameColor",
    [2] = Color3.new(0, 1, 0.9960999488830566)
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1RPNam1eColo1r"):FireServer(unpack(args))


local args = {
    [1] = "RolePlayBio",
    [2] = "Scripter"
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1RPNam1eTex1t"):FireServer(unpack(args))

local args = {
    [1] = "PickingRPBioColor",
    [2] = Color3.new(0.4561024606227875, 0.4561024606227875, 0.4561024606227875)
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1RPNam1eColo1r"):FireServer(unpack(args))



-- Create a tab
local Tab = Window:MakeTab({
    Name = "Info",
    Icon = "rbxassetid://15309138473",
    PremiumOnly = false
})

-- Add a section to the tab
local Section = Tab:AddSection({
    Name = "Informações do script"
})

Tab:AddParagraph("Feito por:", "Lusquinha_067") 

Tab:AddParagraph("Você esta usando :", "Chaos HUB BROOKHAVEN 🏡 V1") 

local Section = Tab:AddSection({
    Name = "Discord"
})

-- Add a button to copy the link to the clipboard
Tab:AddButton({
    Name = "Link Discord (Atualizado)",
    Callback = function()
        -- Script to copy the link to the clipboard
        setclipboard("https://discord.gg/bNdhFkUtHe")
        OrionLib:MakeNotification({
            Name = "Link Copiado",
            Content = "link do Discord copiado ",
            Image = "rbxassetid://131669852271916",
            Time = 5
        })
    end
})

-- Create a tab
local Tab = Window:MakeTab({
    Name = "👾 - Aba Troll",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local Section = Tab:AddSection({
    Name = "Velocidade, Gravidade e Pulo"
})

Tab:AddTextbox({
Name = "Velocidade do Player",
Default = "",
TextDisappear = true,
Callback = function(value)
local speed = tonumber(value)
if speed then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = speed
end
end
})

Tab:AddTextbox({
Name = "Tamanho do Pulo ",
Default = "",
TextDisappear = true,
Callback = function(value)
local jumpHeight = tonumber(value)
if jumpHeight then
game.Players.LocalPlayer.Character.Humanoid.JumpPower = jumpHeight
end
end
})

Tab:AddTextbox({
Name = "Gravidade",
Default = "",
TextDisappear = true,
Callback = function(value)
local gravity = tonumber(value)
if gravity then
workspace.Gravity = gravity
end
end
})

Tab:AddButton({
Name = "Resetar velocidade",
Callback = function()
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
end
})

Tab:AddButton({
Name = "Resetar Pulo",
Callback = function()
game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
end
})

Tab:AddButton({
Name = "Resetar Gravidade",
Callback = function()
workspace.Gravity = 196.2
end
})

local Section = Tab:AddSection({
    Name = "Black Hole"
})

Tab:AddButton({
    Name = "Black Hole",
    Callback = function()

loadstring(game:HttpGet("https://pastebin.com/raw/bK8NvmwB"))()
   end
})

Tab:AddLabel("Ativando isso voce puxa Parts ate seu Personagem")


local Section = Tab:AddSection({
    Name = "Puxar parts"
})

Tab:AddButton({
    Name = "Puxar Parts",
    Callback = function()

loadstring(game:HttpGet("https://pastebin.com/raw/e6dmzQX5"))()
   end
})

Tab:AddLabel("Para usar chegue perto do Player Selecionado")

local Section = Tab:AddSection({
    Name = "Invisivel"
})

Tab:AddToggle({
Name = "Ficar Invisivel",
Default = false,
Callback = function(state)
if state then
-- Ficar invisível
local args = {
[1] = "CharacterSizeDown",
[2] = 4
}
game:GetService("ReplicatedStorage").RE:FindFirstChild("1Clothe1s"):FireServer(unpack(args))
else
-- Voltar ao normal
local args = {
[1] = "CharacterSizeUp",
[2] = 1
}
game:GetService("ReplicatedStorage").RE:FindFirstChild("1Clothe1s"):FireServer(unpack(args))
end
end
})

Tab:AddLabel("Ficar invisível FE")

local Section = Tab:AddSection({
    Name = "Avatar RGB"
})

local colors = {
    "Bright red",    -- Vermelho
    "Lime green",    -- Verde limão
    "Bright blue",   -- Azul
    "Bright yellow", -- Amarelo
    "Bright cyan",   -- Ciano
    "Hot pink",      -- Magenta
    "Royal purple"   -- Roxo
}

-- Variável para controlar o estado do toggle
local rgbEnabled = false

-- Função para mudar a cor do corpo
local function changeColor(color)
    local args = {
        [1] = "skintone",
        [2] = color
    }
    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Updat1eAvata1r"):FireServer(unpack(args))
end

-- Função para iniciar/pausar a mudança de cores
local function toggleRGBCharacter(enabled)
    rgbEnabled = enabled
    if rgbEnabled then
        while rgbEnabled do
            for _, color in ipairs(colors) do
                if not rgbEnabled then return end
                changeColor(color)
                wait(0.5) -- Espera 0.5 segundos antes de mudar para a próxima cor
            end
        end
    end
end

-- Adiciona o toggle à aba
Tab:AddToggle({
    Name = "RGB Character",
    Default = false,
    Callback = function(value)
        toggleRGBCharacter(value)
    end    
})

Tab:AddLabel("Deixar seu Avatar RGB ")

local Section = Tab:AddSection({
    Name = "Cabelo RGB"
})

-- Defina as cores específicas que você deseja alternar
local colors = {
    Color3.new(1, 1, 0),       -- Amarelo
    Color3.new(0, 0, 1),       -- Azul
    Color3.new(1, 0, 1),       -- Rosa
    Color3.new(1, 1, 1),       -- Branco
    Color3.new(0, 1, 0),       -- Verde
    Color3.new(0.5, 0, 1),     -- Roxo
    Color3.new(1, 0.647, 0),   -- Laranja
    Color3.new(0, 1, 1)        -- Ciano
}

local isActive = false -- Controle da ativação do loop

-- Função para alternar entre as cores
local function changeHairColor()
    local i = 1
    while isActive do
        -- Verifica se o botão foi desmarcado e interrompe o loop se necessário
        if not isActive then break end

        local args = {
            [1] = "ChangeHairColor2",
            [2] = colors[i] -- Usa a cor da lista
        }

        -- Envia a solicitação para mudar a cor
        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Max1y"):FireServer(unpack(args))

        -- Atraso entre as trocas de cor (ajuste conforme necessário)
        wait(0.1)

        -- Avança para a próxima cor, e volta para a primeira cor após a última
        i = i % #colors + 1
    end
end

-- Criação do botão de toggle
Tab:AddToggle({
    Name = "Cabelo RGB",
    Default = false,
    Callback = function(value)
        isActive = value -- Alterna o valor de "isActive" para ativar/desativar a mudança de cor
        if isActive then
            changeHairColor() -- Inicia o processo de alteração de cor
        end
    end
})

Tab:AddLabel("Deixa o seu Cabelo RGB ")

local Section = Tab:AddSection({
    Name = "Anti Sit"
})

Tab:AddToggle({
    Name = "Anti Sit",
    Default = false,
    Callback = function(Value)
        local player = game.Players.LocalPlayer
        local connections = {}
        local runService = game:GetService("RunService")

        -- Função para desabilitar a habilidade de sentar
        local function preventSitting(humanoid)
            if humanoid then
                humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
                -- Conecta a função ao evento StateChanged do Humanoid
                local sitConnection = humanoid.StateChanged:Connect(function(_, newState)
                    if newState == Enum.HumanoidStateType.Seated then
                        humanoid:ChangeState(Enum.HumanoidStateType.GettingUp)
                    end
                end)
                table.insert(connections, sitConnection)
            end
        end

        -- Função para monitorar mudanças no personagem e impedir a habilidade de sentar
        local function monitorCharacter()
            -- Função para lidar com o personagem atual e novos personagens
            local function onCharacterAdded(character)
                local humanoid = character:WaitForChild("Humanoid")
                preventSitting(humanoid)
            end

            -- Conecta a função ao evento CharacterAdded para lidar com respawns
            local characterAddedConnection = player.CharacterAdded:Connect(onCharacterAdded)
            table.insert(connections, characterAddedConnection)

            -- Verifica se o personagem já existe quando o script é executado
            if player.Character then
                onCharacterAdded(player.Character)
            end
        end

        -- Função para desconectar todas as conexões e permitir sentar novamente
        local function resetSitting()
            -- Desconectar todas as conexões existentes
            for _, connection in ipairs(connections) do
                connection:Disconnect()
            end
            connections = {}

            -- Permitir que o personagem sente novamente
            local humanoid = player.Character and player.Character:FindFirstChildOfClass("Humanoid")
            if humanoid then
                humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
            end
        end

        if Value then
            -- Quando o toggle está ativado (Value é true), iniciar a monitorCharacter
            monitorCharacter()

            -- Adicionar uma checagem contínua no Heartbeat para garantir que o estado "Seated" esteja sempre desabilitado
            local heartbeatConnection = runService.Heartbeat:Connect(function()
                local humanoid = player.Character and player.Character:FindFirstChildOfClass("Humanoid")
                if humanoid then
                    humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
                end
            end)
            table.insert(connections, heartbeatConnection)
        else
            -- Quando o toggle está desativado (Value é false), resetar as configurações de sentar
            resetSitting()
        end
    end    
})

Tab:AddLabel("Não deixa o seu personagem sentar ")



local FlingTab = Window:MakeTab({
    Name = "🌪 - Flings",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local Section = FlingTab:AddSection({
    Name = "Fling Player"
})

FlingTab:AddButton({
    Name = "🥶 - Fling Player Counch MELHOR !(BETA)",
    Callback = function()

loadstring(game:HttpGet("https://pastebin.com/raw/GMNFW8E8"))()
   end
})
        
-- Seção "Fling all"
local Section = FlingTab:AddSection({
    Name = "Flingar todos os jogadores"
})

-- Botão "Fling All"
FlingTab:AddButton({
    Name = "🔱 - Flingar Geral (Remake Muito Melhor)",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/ZCyQ1Wcf"))()
    end    
})

-- Label "Use the sofa"
FlingTab:AddLabel("100 % Automatico")

local Players = game:GetService("Players")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local playerNames = {}
local selectedPlayerName = nil
local destination = Vector3.new(265.46, -450.83, -59.93)
local originalPosition = nil
local spectating = false

local BusaoTab = Window:MakeTab({
    Name = "🚎 - Matar Player 1",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local Section = BusaoTab:AddSection({
    Name = "Selecione o Player que deseja Matar"
})

-- Criar dropdown para selecionar jogadores
local playerDropdown = BusaoTab:AddDropdown({
    Name = "Selecionar Jogador",
    Options = {}, -- Inicialmente vazio
    Callback = function(selected)
        selectedPlayerName = selected
    end
})

-- Função para atualizar a Player List no Dropdown
local function updatePlayerList()
    playerNames = {}  -- Limpa a lista de nomes

    for _, player in pairs(Players:GetPlayers()) do
        table.insert(playerNames, player.Name) -- Adiciona os jogadores na lista
    end

    -- Atualiza as opções do dropdown
    playerDropdown:Refresh(playerNames, true) -- Atualiza e reseta a seleção
end

-- Botão para atualizar a Player List
BusaoTab:AddButton({
    Name = "Atualizar Player List",
    Callback = function()
        updatePlayerList() -- Atualiza a dropdown quando clicar no botão
    end
})

-- Inicializa a lista de jogadores
updatePlayerList()


BusaoTab:AddButton({
    Name = "Matar Player com Carro",
    Callback = function()
        if not selectedPlayerName then
            print("Nenhum jogador selecionado!")
            return
        end

        local player = Players.LocalPlayer    
        local character = player.Character or player.CharacterAdded:Wait()    
        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")    

        -- Armazena a posição inicial do player antes do fling    
        originalPosition = humanoidRootPart.CFrame    

        -- Função para obter o ônibus    
        local function GetBus()    
            local vehicles = Workspace:FindFirstChild("Vehicles")    
            if vehicles then    
                return vehicles:FindFirstChild(player.Name.."Car")    
            end    
            return nil    
        end    

        local bus = GetBus()    

        -- Se o ônibus não existir, tenta spawnar um    
        if not bus then    
            humanoidRootPart.CFrame = CFrame.new(1118.81, 75.998, -1138.61)    
            task.wait(0.5)    
            local remoteEvent = ReplicatedStorage:FindFirstChild("RE")    
            if remoteEvent and remoteEvent:FindFirstChild("1Ca1r") then    
                remoteEvent["1Ca1r"]:FireServer("PickingCar", "SchoolBus")    
            end    
            task.wait(1)    
            bus = GetBus()    
        end    

        -- Se conseguiu spawnar, tenta sentar no banco do motorista    
        if bus then    
            local seat = bus:FindFirstChild("Body") and bus.Body:FindFirstChild("VehicleSeat")    
            if seat and character:FindFirstChildOfClass("Humanoid") and not character.Humanoid.Sit then    
                repeat    
                    humanoidRootPart.CFrame = seat.CFrame * CFrame.new(0, 2, 0)    
                    task.wait()    
                until character.Humanoid.Sit or not bus.Parent    
            end    
        end    

local function TrackPlayer()  
        while true do  
            if selectedPlayerName then  
                local targetPlayer = Players:FindFirstChild(selectedPlayerName)  
                if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then  
                    local targetHumanoid = targetPlayer.Character:FindFirstChildOfClass("Humanoid")  
                    if targetHumanoid and targetHumanoid.Sit then  
                        if character.Humanoid then  
                            bus:SetPrimaryPartCFrame(CFrame.new(destination))   
                            print("Jogador sentou, levando ônibus para o void!")  

                            task.wait(0.2)  

                            local function simulateJump()  
                                local humanoid = player.Character and player.Character:FindFirstChildWhichIsA("Humanoid")  
                                if humanoid then  
                                    humanoid:ChangeState(Enum.HumanoidStateType.Jumping)  
                                end  
                            end  

                            simulateJump()  
                            print("Simulando pulo!")  

                            task.wait(0.2)  
                            humanoidRootPart.CFrame = originalPosition  
                            print("Player voltou para a posição inicial!")  
                        end  

                        break  
                    else  
                        local targetRoot = targetPlayer.Character.HumanoidRootPart  
                        local time = tick() * 30  -- Aumenta a frequência  

                        local lateralOffset = math.sin(time) * 8  -- Movimento lateral rápido  
                        local frontBackOffset = math.cos(time) * 8  -- Movimento para frente/trás rápido  
                          
                        bus:SetPrimaryPartCFrame(targetRoot.CFrame * CFrame.new(lateralOffset, 0, frontBackOffset))  
                    end  
                end  
            end  
            RunService.RenderStepped:Wait()  
        end  
    end  

    spawn(TrackPlayer)  
end

})

local Section = BusaoTab:AddSection({
    Name = "Spectar jogador"
})

local function startSpectating()
    while spectating do
        if selectedPlayerName then
            local targetPlayer = Players:FindFirstChild(selectedPlayerName)
            if targetPlayer and targetPlayer.Character then
                local camera = Workspace.CurrentCamera
                camera.CameraSubject = targetPlayer.Character:FindFirstChild("Humanoid") or targetPlayer.Character:WaitForChild("Humanoid")
            end
        end
        RunService.RenderStepped:Wait()
    end
end

BusaoTab:AddToggle({
    Name = "Spectar Jogador",
    Default = false,
    Callback = function(state)
        spectating = state
        if spectating then
            spawn(startSpectating)
            print("Agora espectando o jogador: " .. selectedPlayerName)
        else
            local camera = Workspace.CurrentCamera
            camera.CameraSubject = Players.LocalPlayer.Character:WaitForChild("Humanoid")
            print("Deixou de espectar o jogador.")
        end
    end
})

local Section = BusaoTab:AddSection({
    Name = "Teleportar para jogador"
})

BusaoTab:AddButton({
    Name = "Teleportar até Jogador",
    Callback = function()
        if selectedPlayerName then
            local targetPlayer = Players:FindFirstChild(selectedPlayerName)
            if targetPlayer and targetPlayer.Character then
                local targetPosition = targetPlayer.Character.HumanoidRootPart.Position
                local player = Players.LocalPlayer
                player.Character:SetPrimaryPartCFrame(CFrame.new(targetPosition))
                print("Teleportando até o jogador: " .. selectedPlayerName)
            end
        else
            print("Nenhum jogador selecionado!")
        end
    end
})

local VoidTab = Window:MakeTab({
    Name = "🔫 - Matar Player 2",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local Section = VoidTab:AddSection({
    Name = "Puxar ou Matar Player"
})

-- Definição das variáveis e funções para o Fling Player
local selectedKillAdvancedPlayer = nil
local originalPosition = nil
local couchEquipped = false
local platform = nil

local function getCouch()
    local character = game.Players.LocalPlayer.Character
    if character then
        local backpack = game.Players.LocalPlayer.Backpack
        if not backpack:FindFirstChild("Couch") and not character:FindFirstChild("Couch") then
            local args = {
                [1] = "PickingTools",
                [2] = "Couch"
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
        end
        local couch = backpack:FindFirstChild("Couch") or character:FindFirstChild("Couch")
        if couch then
            couch.Parent = character
            couchEquipped = true
            print("Couch equipado.")
        else
            print("Couch não encontrado.")
        end
    end
end

-- Função modificada para teleportar abaixo do jogador alvo e criar uma plataforma temporária
local function teleportBelowPlayer(targetPlayer, offset)
    local targetHRP = targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart")
    if targetHRP then
        local targetPosition = targetHRP.Position
        -- Ajusta a nova posição para ficar completamente abaixo do jogador alvo (altura negativa)
        local newPosition = Vector3.new(targetPosition.X, targetPosition.Y - offset, targetPosition.Z)
        
        -- Criação da plataforma temporária
        if not platform then
            platform = Instance.new("Part")
            platform.Size = Vector3.new(10, 1, 10)
            platform.Anchored = true
            platform.CanCollide = true
            platform.Transparency = 0.5
            platform.Parent = game.Workspace
        end
        platform.Position = newPosition - Vector3.new(0, 3, 0) -- Posicione a plataforma um pouco abaixo do jogador

        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(newPosition)
        print("Teletransportado para abaixo do jogador alvo.")
    else
        print("HumanoidRootPart não encontrado no jogador alvo.")
    end
end

-- Função modificada para o Fling Player
local function killAdvancedPlayer()
    if selectedKillAdvancedPlayer then
        local player = game.Players:FindFirstChild(selectedKillAdvancedPlayer)
        if player then
            originalPosition = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame

            getCouch()

            while true do
                teleportBelowPlayer(player, 4.5)
                wait(0.01)

                if player.Character:FindFirstChild("Humanoid") and player.Character.Humanoid.SeatPart then
                    local skyPosition = CFrame.new(265.46, -450.83, -59.93)
                    player.Character.HumanoidRootPart.CFrame = skyPosition
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = skyPosition

                    wait(0.5)

                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = originalPosition
                    break
                end
            end

            if couchEquipped then
                local character = game.Players.LocalPlayer.Character
                if character then
                    local couch = character:FindFirstChild("Couch")
                    if couch then
                        couch.Parent = game.Players.LocalPlayer.Backpack
                        couchEquipped = false
                        print("Couch desequipado.")
                    end
                end
            end
        else
            print("Jogador não encontrado.")
        end
    else
        print("Nenhum jogador selecionado para o Fling Avançado.")
    end
end

-- Botão "Fling Player"
VoidTab:AddButton({
    Name = "Matar Player Selecionado",
    Description = "Equipa o item 'Couch' e teleporta o jogador selecionado.",
    Callback = function()
        killAdvancedPlayer()
    end,
})

-- Função modificada para o Pull Player
local function pullPlayer()
    if selectedKillAdvancedPlayer then
        local player = game.Players:FindFirstChild(selectedKillAdvancedPlayer)
        if player then
            originalPosition = game.Players.LocalPlayer.Character.HumanoidRootPart.Position

            getCouch()

            while true do
                teleportBelowPlayer(player, 4.5)
                wait(0.01)

                if player.Character:FindFirstChild("Humanoid") and player.Character.Humanoid.SeatPart then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(originalPosition)
                    wait(0.7)

                    if couchEquipped then
                        local character = game.Players.LocalPlayer.Character
                        if character then
                            local couch = character:FindFirstChild("Couch")
                            if couch then
                                couch.Parent = game.Players.LocalPlayer.Backpack
                                couchEquipped = false
                                print("Couch desequipado.")
                            end
                        end
                    end
                    break
                end
            end
        else
            print("Jogador não encontrado.")
        end
    else
        print("Nenhum jogador selecionado para o Pull.")
    end
end

-- Botão "Pull Player"
VoidTab:AddButton({
    Name = "Puxar Player Selecionado",
    Description = "Equipa o item 'Couch' e teleporta o jogador selecionado.",
    Callback = function()
        pullPlayer()
    end,
})

-- Atualização e manipulação da lista de jogadores
local killAdvancedPlayerList = {}
local spectating = false
local originalCameraSubject
local playerDropdown

local function updatePlayerList()
    killAdvancedPlayerList = {}
    for _, player in ipairs(game.Players:GetPlayers()) do
        table.insert(killAdvancedPlayerList, player.Name)
    end
    if playerDropdown then
        playerDropdown:Refresh(killAdvancedPlayerList, true)
    end
end

local function startSpectate(playerName)
    local player = game.Players:FindFirstChild(playerName)
    if player and player.Character and player.Character:FindFirstChild("Humanoid") then
        originalCameraSubject = game.Workspace.CurrentCamera.CameraSubject
        game.Workspace.CurrentCamera.CameraSubject = player.Character.Humanoid
        spectating = true
    end
end

local function stopSpectate()
    if originalCameraSubject then
        game.Workspace.CurrentCamera.CameraSubject = originalCameraSubject
        spectating = false
    end
end

local function teleportToPlayer(playerName)
    local player = game.Players:FindFirstChild(playerName)
    local localPlayer = game.Players.LocalPlayer
    
    if player and player.Character and localPlayer.Character and localPlayer.Character:FindFirstChild("HumanoidRootPart") then
        local targetPosition = player.Character.HumanoidRootPart.Position
        
        -- Teleporta o jogador local para a posição do jogador alvo.
        localPlayer.Character:MoveTo(targetPosition)
        print("Teletransportado para o jogador alvo.")
    else
        print("Não foi possível encontrar o jogador alvo ou o HumanoidRootPart.")
    end
end

updatePlayerList()

playerDropdown = VoidTab:AddDropdown({
    Name = "Selecione o jogador que deseja Matar Puxar",
    Description = "Selecione o jogador alvo para o Fling [BETA]",
    Options = killAdvancedPlayerList,
    Callback = function(playerName)
        selectedKillAdvancedPlayer = playerName
    end,
})

VoidTab:AddButton({
    Name = "Atualizar Player List",
    Description = "Clique para resetar a lista de jogadores",
    Callback = function()
        updatePlayerList()
    end,
})

local Section = VoidTab:AddSection({
    Name = "Spectar player"
})

VoidTab:AddToggle({
    Name = "Spectar Player",
    Description = "Ative para spectar o jogador selecionado",
    Default = false,
    Callback = function(state)
        if state then 
            startSpectate(selectedKillAdvancedPlayer) 
        else 
            stopSpectate() 
        end 
    end,
})

local Section = VoidTab:AddSection({
    Name = "Teleport to player"
})

VoidTab:AddButton({
    Name = "Teleporte para o jogador selecionado",
    Description = "Clique para teleportar para o jogador selecionado",
    Callback = function()
        teleportToPlayer(selectedKillAdvancedPlayer)
    end,
})

-- Cria a aba "🛍️ - Avatar"
local Tab = Window:MakeTab({
    Name = "🛍️ - Avatar",
    Icon = "rbxassetid://10734952036",
    PremiumOnly = false
})

local Section = Tab:AddSection({
    Name = "Copiar Skin"
})

local selectedPlayer = nil

local function RESETBLOCK()
    local args = {
        [1] = "CharacterChange",
        [2] = {0, 0, 0, 0, 0, 0},
        [3] = "AllBlocky"
    }
    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Avata1rOrigina1l"):FireServer(unpack(args))
end

local function APPLY_SKINTONE(Player)
    local c = Player.Character or Player.CharacterAdded:Wait()
    local h = c:FindFirstChildOfClass("Humanoid")
    if not h then return end

    local bodyColors = c:FindFirstChildOfClass("BodyColors")
    if not bodyColors then return end

    local skinToneName = bodyColors.HeadColor.Name
    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Updat1eAvata1r"):FireServer("skintone", skinToneName)
end

local function Wear(id)
    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Updat1eAvata1r"):FireServer("wear", id)
end

local function COPYCLOTHING(Player)
    local h = Player.Character and Player.Character:FindFirstChildOfClass("Humanoid")
    if not h then return end

    local d = h:GetAppliedDescription()
    local cIds = {d.Shirt, d.Pants, d.GraphicTShirt}

    for _, id in ipairs(cIds) do
        if id ~= 0 then
            task.wait(1)
            Wear(id)
        end
    end
end

local function COPYBODYPART(Player)
    local h = Player.Character and Player.Character:FindFirstChildOfClass("Humanoid")
    if not h then return end

    local d = h:GetAppliedDescription()
    local bIds = {d.Torso, d.RightArm, d.LeftArm, d.RightLeg, d.LeftLeg, d.Head}

    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Avata1rOrigina1l"):FireServer("CharacterChange", bIds, "GAZE")
end

local function COPYACCESSORIES(Player)
    local h = Player.Character and Player.Character:FindFirstChildOfClass("Humanoid")
    if not h then return end

    local d = h:GetAppliedDescription()
    local aIds = {}

    for _, aList in ipairs({
        d.HatAccessory, d.HairAccessory, d.FaceAccessory, d.NeckAccessory,
        d.ShouldersAccessory, d.FrontAccessory, d.BackAccessory, d.WaistAccessory
    }) do
        for id in string.gmatch(aList, "%d+") do
            table.insert(aIds, tonumber(id))
        end
    end

    for _, id in ipairs(aIds) do
        task.wait(1)
        Wear(id)
    end
end

local function START()
    if selectedPlayer then
        local player = game.Players:FindFirstChild(selectedPlayer)
        if player then
            COPYACCESSORIES(game.Players.LocalPlayer)
            COPYACCESSORIES(player)
            task.wait(1)
            RESETBLOCK()
            task.wait(3)
            COPYBODYPART(player)
            COPYCLOTHING(player)
            APPLY_SKINTONE(player)
        end
    else
        OrionLib:MakeNotification({
            Name = "Erro",
            Content = "Nenhum jogador selecionado!",
            Image = "rbxassetid://4483345998",
            Time = 3
        })
    end
end

local Dropdown = Tab:AddDropdown({
    Name = "Selecione um Player",
    Default = "",
    Options = {},
    Callback = function(Value)
        selectedPlayer = Value
    end
})

Tab:AddButton({
    Name = "Copiar Skin do Player",
    Callback = function()
        START()
    end
})

local function UpdatePlayerList()
    local currentPlayers = {}
    
    for _, player in ipairs(game.Players:GetPlayers()) do
        table.insert(currentPlayers, player.Name)
    end
    
    Dropdown:Refresh(currentPlayers, true) -- Remove os antigos e adiciona apenas os novos corretamente
end

Tab:AddButton({
    Name = "Atualizar Player List",
    Callback = function()
        UpdatePlayerList()
    end
})

UpdatePlayerList()

-- Adiciona uma seção para "🎃 - Headless" abaixo do botão de clonar skin
local headlessSection = Tab:AddSection({
    Name = "🎃 - Sem Cabeça"
})

-- Adiciona o botão "🎃 - Headless"
Tab:AddButton({
  Name = "🎃 - Sem Cabeça",
  Callback = function()
    local args = {
        [1] = "CharacterChange",
        [2] = {
            [1] = 1,
            [2] = 1,
            [3] = 1,
            [4] = 1,
            [5] = 1,
            [6] = 134082579
        },
        [3] = "by:REDz"
    }

    game:GetService("ReplicatedStorage").RE:FindFirstChild("1Avata1rOrigina1l"):FireServer(unpack(args))
  end    
})

-- Função para pegar as chaves de uma tabela
local function getTableKeys(tbl)
    local keys = {}
    for key, _ in pairs(tbl) do
        table.insert(keys, key)
    end
    return keys
end

-- Adiciona uma seção para "💀 - Korblox"
local korbloxSection = Tab:AddSection({
    Name = "💀 - Korblox"
})

-- Lista de skins de Korblox
local korbloxSkins = {
    ["🦵 - Perna Esquerda Korblox"] = {
        "CharacterChange", 
        {1, 1, 1, 1, 139607673, 1}, 
        "by:REDz"
    },
    ["🦵 - Perna Direita Korblox"] = {
        "CharacterChange", 
        {1, 1, 1, 139607718, 1, 1}, 
        "by:REDz"
    }
}

Tab:AddDropdown({
    Name = "Selecione uma Skin de Korblox",
    Options = getTableKeys(korbloxSkins), -- Usando a função para pegar as chaves
    Callback = function(selectedKorbloxSkin)
        local args = korbloxSkins[selectedKorbloxSkin]
        if args then
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Avata1rOrigina1l"):FireServer(unpack(args))
        end
    end
})

-- Seção para "💨 - Gelo"
local iceSection = Tab:AddSection({
    Name = "💨 - Ice"
})

local iceSkins = {
    ["🦿 - Perna Esquerda de Gelo"] = { "CharacterChange", { 1, 1, 1, 1, 139572789, 1 }, "by:REDz" },
    ["🦿 - Perna Direita de Gelo"] = { "CharacterChange", { 1, 1, 1, 139572888, 1, 1 }, "by:REDz" }
}

Tab:AddDropdown({
    Name = "Selecione a Skin de Gelo",
    Options = {"🦿 - Perna Esquerda de Gelo", "🦿 - Perna Direita de Gelo"}, -- Aqui você coloca as opções diretamente
    Callback = function(selectedIceSkin)
        local args = iceSkins[selectedIceSkin]
        if args then
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Avata1rOrigina1l"):FireServer(unpack(args))
        end
    end
})

-- Seção para "🧚‍♂️ - Fadas"
local fadasSection = Tab:AddSection({
    Name = "🧚‍♂️ - Fadas"
})

local FadaDropdown = Tab:AddDropdown({
    Name = "Escolha uma Fada",
    Default = "Fada Roxa",
    Options = {"Fada Roxa", "Fada do Inverno", "Fada do Dia de São Patrício", "Fada do Outono"},
    Callback = function(selected)
        local fadas = {
            ["Fada Roxa"] = 150381051,
            ["Fada do Inverno"] = 141742418,
            ["Fada do Dia de São Patrício"] = 226189871,
            ["Fada do Outono"] = 128217885
        }

        local args = {
            [1] = "wear",
            [2] = fadas[selected]
        }

        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Updat1eAvata1r"):FireServer(unpack(args))
    end
})

-- Seção para "👔 - Skins"
local skinsSection = Tab:AddSection({
    Name = "👔 - Skins"
})

local skins = {
    ["🍟 - Gangue das Batatas"] = { "CharacterChange", { 5392155773, 5392150804, 5392146467, 5392152751, 5392148570, 1 }, "by:REDz" },
    ["🎩 - O Supervisor"] = { "CharacterChange", { 81725326, 81725366, 81725392, 1, 1, 1 }, "by:REDz" },
    ["👺 - Skin Korblox Completa"] = { "CharacterChange", { 139607770, 139607625, 139607570, 139607718, 139607673, 1 }, "by:REDz" },
    ["❄ - Guerreiro de Gelo"] = { "CharacterChange", { 1, 139572697, 139572600, 139572888, 139572789, 139572973 }, "by:REDz" },
    ["🪓 - Jeff, o Assassino"] = { "wear", 14502327402 },
    ["🟢 - Mario Vítima 1"] = { "wear", 14732524763 },
    ["👁 - Olhos de Jermas"] = { "wear", 14817978441 },
    ["👀 - Munci Raivoso & Olhos Assustadores"] = { "wear", 14701936208 },
    ["🔒 - Prisão"] = { "wear", 11148843650 }

}

Tab:AddDropdown({
    Name = "Selecione uma Skin",
    Options = {"🍟 - Gangue das Batatas", "🎩 - O Supervisor", "👺 - Skin Korblox Completa", "❄ - Guerreiro de Gelo", "🪓 - Jeff, o Assassino", "🟢 - Mario Vítima 1", "👁 - Olhos de Jermas", "👀 - Munci Raivoso & Olhos Assustadores", "🔒 - Prisão"},
    Callback = function(selectedSkin)
        local args = skins[selectedSkin]
        if args then
            if args[1] == "CharacterChange" then
                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Avata1rOrigina1l"):FireServer(unpack(args))
            else
                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Updat1eAvata1r"):FireServer(unpack(args))
            end
        end
    end
})

-- Seção para "🎃 Abóboras [Efeitos]"
local pumpkinsSection = Tab:AddSection({
    Name = "🎃 Abóboras [Efeitos]"
})

local pumpkins = {
    ["Abóbora Com Efeitos Azuis"] = { "wear", 183468963 },
    ["Abóbora Com Efeitos Verdes"] = { "wear", 132809431 }
}

Tab:AddDropdown({
    Name = "Selecione uma Abóbora",
    Options = {"Abóbora Com Efeitos Azuis", "Abóbora Com Efeitos Verdes"},
    Callback = function(selectedPumpkin)
        local args = pumpkins[selectedPumpkin]
        if args then
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Updat1eAvata1r"):FireServer(unpack(args))
        end
    end
})


-- Defina as cores vibrantes que você deseja usar
local colors = {
    Color3.new(1, 0, 0),       -- Vermelho
    Color3.new(0, 1, 0),       -- Verde
    Color3.new(0, 0, 1),       -- Azul
    Color3.new(1, 1, 0),       -- Amarelo
    Color3.new(0, 1, 1),       -- Ciano
    Color3.new(1, 0, 1)        -- Magenta
}

-- Variável para controlar o estado do toggle House RGB
local isHouseRGBActive = false

-- Função para alterar a cor da casa
local function changeColor()
    -- Pegue o serviço ReplicatedStorage e o remote event
    local replicatedStorage = game:GetService("ReplicatedStorage")
    local remoteEvent = replicatedStorage:WaitForChild("RE"):WaitForChild("1Player1sHous1e")

    -- Loop infinito para mudar a cor a cada 0,5 segundos
    while isHouseRGBActive do
        for _, color in ipairs(colors) do
            if not isHouseRGBActive then return end -- Se o toggle estiver desativado, sair do loop
            local args = {
                [1] = "ColorPickHouse",
                [2] = color
            }
            remoteEvent:FireServer(unpack(args))
            wait(0.8) -- Espera 0,5 segundos antes de mudar para a próxima cor
        end
    end
end

-- Função para iniciar ou parar a mudança de cor
local function toggleHouseRGB(state)
    isHouseRGBActive = state
    if isHouseRGBActive then
        print("House RGB Activated")
        changeColor()
    else
        print("House RGB Deactivated")
    end
end

local isUnbanActive = false -- Variável para controlar o estado do toggle

local HouseTab = Window:MakeTab({
    Name = "🏡 - Casa",
    Icon = "rbxassetid://4483345998"
})

local Section = HouseTab:AddSection({
    Name = "Permissão Casas"
})

local selectedCasaNumber = nil

local TextBox = HouseTab:AddTextbox({
    Name = "Digite o número da casa",
    Default = "",
    TextDisappear = false,
    Callback = function(number)
        selectedCasaNumber = tonumber(number)
    end
})

HouseTab:AddButton({
    Name = "Pegar Permissão",
    Callback = function()
        if selectedCasaNumber then
            local args = {
                [1] = "GivePermissionLoopToServer",
                [2] = game:GetService("Players").LocalPlayer,
                [3] = selectedCasaNumber
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Playe1rTrigge1rEven1t"):FireServer(unpack(args))
        else
            print("Nenhum número de casa selecionado.")
        end
        print("Clicked!")
    end
})

HouseTab:AddLabel("Não Clique muitas vezes Risco de Kick")

local Section = HouseTab:AddSection({
    Name = "Permissão Todas as Casas do Server"
})

HouseTab:AddButton({
    Name = "Pegar Permissão de Todas as Casas do Server",
    Callback = function()
        for i = 1, 35 do
            if i ~= 8 and i ~= 9 and i ~= 10 then
                local args = {
                    [1] = "GivePermissionLoopToServer",
                    [2] = game:GetService("Players").LocalPlayer,
                    [3] = i
                }
                game:GetService("ReplicatedStorage").RE:FindFirstChild("1Playe1rTrigge1rEven1t"):FireServer(unpack(args))
            end
        end
        print("Permissions for all houses granted!")
    end
})

HouseTab:AddLabel("Não Clique muitas vezes Risco de Kick")

local Section = HouseTab:AddSection({
    Name = "Teleportar para o cofre de uma casa"
})

local safeselect = nil

-- Função para obter o cofre de uma casa
local function GetHouseSafe(houseName)
    local house = workspace["001_Lots"]:FindFirstChild(houseName .. "House")

    if house then
        local picked = house:FindFirstChild("HousePickedByPlayer")
        if picked then
            local model = picked:FindFirstChild("HouseModel")
            if model then
                local safe = model:FindFirstChild("001_Safe")
                if safe then
                    local door = safe:FindFirstChild("OpenSafeDoorButton")
                    if door then
                        return door
                    end
                end
            end
        end
    else
        OrionLib:MakeNotification({
            Name = "Erro",
            Content = "Casa não encontrada, atualize a tabela ou tente novamente com uma existente.",
            Image = "rbxassetid://4483345998",
            Time = 3
        })
    end

    return nil
end

-- Função para obter as casas existentes
local function GetExistentHouses()
    local houseTable = {}
    for _, v in pairs(workspace["001_Lots"]:GetChildren()) do
        if string.find(v.Name, "House") and v:FindFirstChild("HousePickedByPlayer") then
            table.insert(houseTable, v.Owner.Value .. "-" .. v.Number.Number.Value)
        end
    end
    return houseTable
end

-- Criando dropdown inicial
local safehouse
local function CreateDropdown()
    safehouse = HouseTab:AddDropdown({
        Name = "Selecionar Cofre da casa:",
        Default = "",
        Options = GetExistentHouses(),
        Callback = function(Value)
            if Value and Value ~= "" then
                local a = string.split(Value, "-")
                safeselect = tostring(a[1])
            end
        end
    })
end

CreateDropdown() -- Inicializa o dropdown ao carregar o script

-- Função para atualizar a lista de casas corretamente
local function UpdateHouseList()
    safeselect = nil -- Remove qualquer seleção ativa
    
    -- Remove o dropdown antigo e cria um novo atualizado
    safehouse:Destroy()
    CreateDropdown()
    
    OrionLib:MakeNotification({
        Name = "Atualizado",
        Content = "Lista de casas atualizada!",
        Image = "rbxassetid://4483345998",
        Time = 3
    })
end

-- Botão para teleportar
HouseTab:AddButton({
    Name = "Teleportar Para o Cofre",
    Callback = function()
        if not safeselect then return end
        local lots = workspace["001_Lots"]
        if lots:FindFirstChild(safeselect .. "House") then
            local safeDoor = GetHouseSafe(safeselect)
            if safeDoor then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(safeDoor.Position) -- Teleporta até o botão do cofre
            else
                OrionLib:MakeNotification({
                    Name = "Erro",
                    Content = "Cofre não encontrado na casa " .. tostring(safeselect),
                    Image = "rbxassetid://4483345998",
                    Time = 3
                })
            end
        else
            OrionLib:MakeNotification({
                Name = "Erro",
                Content = "Casa não encontrada, atualize a tabela ou selecione uma existente.",
                Image = "rbxassetid://4483345998",
                Time = 3
            })
        end
    end
})

-- Botão para atualizar a lista de casas
HouseTav:AddButton({
    Name = "Atualizar House List",
    Callback = function()
        UpdateHouseList()
    end
})

local Section = HouseTab:AddSection({
    Name = "Kill House"
})

HouseTab:AddLabel("Para Usar Você precisa ter a casa 17 Spawnada")

-- Variáveis principais
local selectedKillAdvancedPlayer = nil
local originalPosition = nil
local couchEquipped = false
local running = false

-- Função para equipar o Couch
local function getCouch()
    local character = game.Players.LocalPlayer.Character
    if character then
        local backpack = game.Players.LocalPlayer.Backpack
        if not backpack:FindFirstChild("Couch") and not character:FindFirstChild("Couch") then
            local args = { "PickingTools", "Couch" }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
        end

        local couch = backpack:FindFirstChild("Couch") or character:FindFirstChild("Couch")
        if couch then
            couch.Parent = character
            couchEquipped = true
            print("Couch equipado.")
        else
            print("Couch não encontrado.")
        end
    end
end

-- Função para banir todos que entrarem na casa, exceto o dono do script
local function BanirPlayer()
    local player = game.Players.LocalPlayer
    local replicatedStorage = game:GetService("ReplicatedStorage")
    local event = replicatedStorage:WaitForChild("RE"):WaitForChild("1Playe1rTrigge1rEven1t")

    for _, v in pairs(game.Players:GetPlayers()) do
        if v ~= player and v.Character and v.Character:FindFirstChild("HumanoidRootPart") then -- Evita banir o próprio jogador
            local args = { "BanPlayerFromHouse", v, workspace:WaitForChild(v.Name) }
            event:FireServer(unpack(args))
        end
    end
end

-- Função para teleportar abaixo do jogador alvo
local function teleportBelowPlayer(targetPlayer, offset)
    local targetHRP = targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart")
    if targetHRP then
        local newPosition = Vector3.new(targetHRP.Position.X, targetHRP.Position.Y - offset, targetHRP.Position.Z)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(newPosition)
    end
end

-- Função para criar um bloco invisível gigantesco abaixo do mapa
local function createInvisibleBlock()
    local part = Instance.new("Part")
    part.Size = Vector3.new(999, 40, 999)  -- Bloco gigante, ajustado conforme o tamanho do mapa
    part.Position = Vector3.new(0, -500, 0)  -- Posicionado abaixo do mapa
    part.Anchored = true
    part.CanCollide = false  -- Não colide com os outros objetos
    part.Transparency = 1  -- Invisível
    part.Parent = workspace
end

-- Função para movimentação lateral rápida enquanto no loop de teleporte
local function sideMovement()
    local humanoidRootPart = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
    if not humanoidRootPart then return end

    while running do
        humanoidRootPart.CFrame = humanoidRootPart.CFrame * CFrame.new(10, 0, 0) -- Pequeno movimento para a direita
        wait(0.1)
        humanoidRootPart.CFrame = humanoidRootPart.CFrame * CFrame.new(-4, 0, 0) -- Pequeno movimento para a esquerda
        wait(0.1)
        humanoidRootPart.CFrame = humanoidRootPart.CFrame * CFrame.new(10, 0, 0) -- Volta ao centro
    end
end

-- Função principal para o Fling
local function killAdvancedPlayer()
    if not selectedKillAdvancedPlayer then
        print("Nenhum jogador selecionado para o Fling Avançado.")
        return
    end

    local player = game.Players:FindFirstChild(selectedKillAdvancedPlayer)
    if not player then
        print("Jogador não encontrado.")
        return
    end

    running = true
    originalPosition = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame

    getCouch()
    createInvisibleBlock()  -- Cria o bloco invisível ao iniciar o script

    -- Inicia movimentação lateral rápida
    task.spawn(sideMovement)

    while running do
        teleportBelowPlayer(player, 5.1)
        wait(0.0001)

        -- Verifica se o player alvo sentou
        if player.Character:FindFirstChild("Humanoid") and player.Character.Humanoid.SeatPart then
            running = false  -- Para a movimentação lateral
            local skyPosition = CFrame.new(-188.67, 38.02, -209.08) -- Coordenada ajustada
            player.Character.HumanoidRootPart.CFrame = skyPosition
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = skyPosition

            -- Desequipando o Couch 0.2 segundos antes de banir o jogador
            wait(0.2)
            if couchEquipped then
                local character = game.Players.LocalPlayer.Character
                if character then
                    local couch = character:FindFirstChild("Couch")
                    if couch then
                        couch.Parent = game.Players.LocalPlayer.Backpack
                        couchEquipped = false
                        print("Couch desequipado.")
                    end
                end
            end

            -- Banindo o jogador após 0.2 segundos
            BanirPlayer()
            wait(0.5)

            -- Teleportando de volta para a posição original
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = originalPosition
        end
    end
end

-- Botão para ativar o Fling
HouseTab:AddButton({
    Name = "Kill House Casa 17",
    Description = "Fica teleportando abaixo do player e o arremessa quando sentar",
    Callback = function()
        killAdvancedPlayer()
    end,
})

-- Atualização da lista de jogadores
local killAdvancedPlayerList = {}
local playerDropdown

local function updatePlayerList()
    killAdvancedPlayerList = {}
    for _, player in ipairs(game.Players:GetPlayers()) do
        table.insert(killAdvancedPlayerList, player.Name)
    end
    if playerDropdown then
        playerDropdown:Refresh(killAdvancedPlayerList, true)
    end
end

updatePlayerList()

playerDropdown = HouseTab:AddDropdown({
    Name = "Selecione o jogador que deseja Matar",
    Description = "Selecione o jogador alvo para o Fling",
    Options = killAdvancedPlayerList,
    Callback = function(playerName)
        selectedKillAdvancedPlayer = playerName
    end,
})

HouseTab:AddButton({
    Name = "Atualizar Player List",
    Description = "Clique para resetar a lista de jogadores",
    Callback = function()
        updatePlayerList()
    end,
})

HouseTab:AddLabel("Não Use muitas vezes de uma vez Risco de kick")

local Section = HouseTab:AddSection({
    Name = "Teleporte Para Casas"
})

local casas = {
    ["Casa 1"] = Vector3.new(260.29, 4.37, 209.32),
    ["Casa 2"] = Vector3.new(234.49, 4.37, 228.00),
    ["Casa 3"] = Vector3.new(262.79, 21.37, 210.84),
    ["Casa 4"] = Vector3.new(229.60, 21.37, 225.40),
    ["Casa 5"] = Vector3.new(173.44, 21.37, 228.11),
    ["Casa 6"] = Vector3.new(-43, 21, -137),
    ["Casa 7"] = Vector3.new(-40, 36, -137),
    ["Casa 11"] = Vector3.new(-21, 40, 436),
    ["Casa 12"] = Vector3.new(155, 37, 433),
    ["Casa 13"] = Vector3.new(255, 35, 431),
    ["Casa 14"] = Vector3.new(254, 38, 394),
    ["Casa 15"] = Vector3.new(148, 39, 387),
    ["Casa 16"] = Vector3.new(-17, 42, 395),
    ["Casa 17"] = Vector3.new(-189, 37, -247),
    ["Casa 18"] = Vector3.new(-354, 37, -244),
    ["Casa 19"] = Vector3.new(-456, 36, -245),
    ["Casa 20"] = Vector3.new(-453, 38, -295),
    ["Casa 21"] = Vector3.new(-356, 38, -294),
    ["Casa 22"] = Vector3.new(-187, 37, -295),
    ["Casa 23"] = Vector3.new(-410, 68, -447),
    ["Casa 24"] = Vector3.new(-348, 69, -496),
    ["Casa 28"] = Vector3.new(-103, 12, 1087),
    ["Casa 29"] = Vector3.new(-730, 6, 808),
    ["Casa 30"] = Vector3.new(-245, 7, 822),
    ["Casa 31"] = Vector3.new(639, 76, -361),
    ["Casa 32"] = Vector3.new(-908, 6, -361),
    ["Casa 33"] = Vector3.new(-111, 70, -417),
    ["Casa 34"] = Vector3.new(230, 38, 569),
    ["Casa 35"] = Vector3.new(-30, 13, 2209)
}

-- Criando uma lista com os nomes das casas e ordenando corretamente
local casasNomes = {}
for nome, _ in pairs(casas) do
    table.insert(casasNomes, nome)
end

table.sort(casasNomes, function(a, b)
    local numA = tonumber(a:match("%d+")) or 0
    local numB = tonumber(b:match("%d+")) or 0
    return numA < numB
end)

HouseTab:AddDropdown({
    Name = "Selecionar Casa",
    Options = casasNomes,
    Callback = function(casaSelecionada)
        local player = game.Players.LocalPlayer
        if player and player.Character then
            player.Character.HumanoidRootPart.CFrame = CFrame.new(casas[casaSelecionada])
        end
    end
})

HouseTab:AddLabel("Teleporte para a Casa que Quiser")

local Section = HouseTab:AddSection({
    Name = "Auto Unban"
})

HouseTab:AddToggle({
    Name = "Auto Unban",
    Default = false,
    Callback = function(state)
        isUnbanActive = state
        if isUnbanActive then
            print("Auto Unban Activated")
            startAutoUnban()
        else
            print("Auto Unban Deactivated")
        end
    end
})

HouseTab:AddLabel("Te desbane automaticamente das Casas")

local Section = HouseTab:AddSection({
    Name = "Casa RGB"
})

HouseTab:AddToggle({
    Name = "Casa RGB",
    Default = false,
    Callback = function(state)
        toggleHouseRGB(state)
    end
})

HouseTab:AddLabel("Deixa a sua casa RGB")

function startAutoUnban()
    while isUnbanActive do
        for i, v in pairs(game:GetService("Workspace"):WaitForChild("001_Lots"):GetDescendants()) do
            -- houses
            if v.Name == "BannedBlock1" or v.Name == "BannedBlock2" or v.Name == "BannedBlock3" or v.Name == "BannedBlock4" or v.Name == "BannedBlock5" or v.Name == "BannedBlock6" or v.Name == "BannedBlock7" or v.Name == "BannedBlock11" or v.Name == "BannedBlock12" or v.Name == "BannedBlock13" or v.Name == "BannedBlock14" or v.Name == "BannedBlock15" or v.Name == "BannedBlock16" or v.Name == "BannedBlock17" or v.Name == "BannedBlock18" or v.Name == "BannedBlock19" or v.Name == "BannedBlock20" or v.Name == "BannedBlock21" or v.Name == "BannedBlock21" or v.Name == "BannedBlock22" or v.Name == "BannedBlock23" or v.Name == "BannedBlock24" or v.Name == "BannedBlock30" or v.Name == "BannedBlock31" or v.Name == "BannedBlock32" or v.Name == "BannedBlock33" or v.Name == "BannedBlock34" or v.Name == "BannedBlock35" then                -- destroy
                v:Destroy()
            end
        end
        wait(1) -- Espera 5 segundos antes de repetir a verificação
    end
end

local Tab = Window:MakeTab({Name = "🌐 - Audio All", Icon = "rbxassetid://4483345998", PremiumOnly = false})

local Section = Tab:AddSection({
    Name = "Audio Todos os Players"
})

-- Lista de áudios
local audios = {
    {name = "Sonic.exe ", id = 2496367477},
    {name = "Tubers93 1", id = 6129291390},
    {name = "Tubers93 2", id = 9032712619},
    {name = "John's Laugh ", id = 130759239},
    {name = "Chucky Laugh", id = 132179181},
    {name = "Grito ", id = 80156405968805},
    {name = "Sus Audio", id = 7705506391},
    {name = "AAAH", id = 7772283448},
    {name = "Monstro Gritando", id = 2738830850},
    {name = "Bat Hit", id = 7129073354},
    {name = "Nuclear Siren", id = 675587093},
    {name = "Sem ideia de nome KK", id = 7520729342},
    {name = "Estora tímpano", id = 268116333} 
}

-- Variável para controlar o ID do áudio selecionado
local selectedAudioID

-- Adicionar uma dropdown para selecionar o áudio
local audioNames = {}
for _, audio in ipairs(audios) do
    table.insert(audioNames, audio.name)
end

Tab:AddTextbox({
    Name = "Insira o ID do Áudio ou Musica",
    Default = "",
    Callback = function(value)
        -- Atualiza o ID do áudio baseado no valor inserido na TextBox
        selectedAudioID = tonumber(value)
    end
})

Tab:AddDropdown({
    Name = "Selecione o Áudio",
    Default = audioNames[1],
    Options = audioNames,
    Callback = function(value)
        for _, audio in ipairs(audios) do
            if audio.name == value then
                selectedAudioID = audio.id
                break
            end
        end
    end
})

-- Variável para controlar o loop do áudio
local audioLoop = false
local currentSound = nil  -- Variável para armazenar a referência do áudio tocando

local Section = Tab:AddSection({
    Name = "Loop de Audio"
})

-- Adicionar um toggle para o loop do áudio
Tab:AddToggle({
    Name = "Loop Tocar Áudio",
    Default = false,
    Callback = function(value)
        audioLoop = value
        if not audioLoop and currentSound then
            currentSound:Stop()  -- Para o áudio caso o loop seja desativado
            currentSound = nil  -- Limpa a referência
        elseif audioLoop and not currentSound then
            playAudio()  -- Reinicia o áudio se o loop for ativado
        end
    end
})

Tab:AddLabel("Loop de tocar Áudio (Todos players do Server ouvem)")

-- Função para tocar o áudio
local function playAudio()
    if selectedAudioID then
        -- Se já houver um áudio tocando, pare-o antes de começar outro
        if currentSound then
            currentSound:Stop()
        end

        local args = {
            [1] = game:GetService("Workspace"),
            [2] = selectedAudioID,
            [3] = 1,
        }
        game:GetService("ReplicatedStorage").RE:FindFirstChild("1Gu1nSound1s"):FireServer(unpack(args))

        -- Cria e toca o áudio
        currentSound = Instance.new("Sound")
        currentSound.SoundId = "rbxassetid://"..selectedAudioID
        currentSound.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
        currentSound:Play()

        -- Espera até o som acabar e começa novamente se o loop estiver ativado
        currentSound.Ended:Connect(function()
            if audioLoop then
                playAudio()  -- Reinicia o som imediatamente
            end
        end)
    else
        warn("Nenhum áudio selecionado!")
    end
end

local Section = Tab:AddSection({
    Name = "Tocar Áudio"
})

-- Adicionar um botão para tocar o áudio
Tab:AddButton({
    Name = "Tocar Áudio",
    Callback = function()
        playAudio()
    end
})

Tab:AddLabel("Todos do server ouvem o áudio")

-- Loop do áudio para garantir que o loop funcione corretamente
task.spawn(function()
    while true do
        if audioLoop and not currentSound then
            playAudio()  -- Reinicia o áudio se o loop estiver ativado
        end
        task.wait(0.1) -- Pequeno intervalo para evitar sobrecarga de CPU
    end
end)


local Tab = Window:MakeTab({Name = "🧨 - Lag Server FE", Icon = "rbxassetid://4483345998", PremiumOnly = false})

local Section = Tab:AddSection({
    Name = "Lag Extintor"
})

-- Variável para armazenar o estado do toggle
local toggles = { DupeExtintor = false }

-- Função para simular um clique normal
local function clickNormally(object)
    local clickDetector = object:FindFirstChildWhichIsA("ClickDetector")
    if clickDetector then
        fireclickdetector(clickDetector) -- Clica normalmente
    end
end

-- Função para duplicar o extintor
local function dupeItem(itemPath, maxTeleports)
    if itemPath then
        local teleportCount = 0
        while teleportCount < maxTeleports and toggles.DupeExtintor do
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = itemPath.CFrame
            clickNormally(itemPath)
            teleportCount = teleportCount + 1
            wait(0.01) -- Tempo de espera para evitar travamento
        end
    else
        warn("Extintor não encontrado.")
    end
end

-- Criando Toggle para Dupe Extintor
Tab:AddToggle({
    Name = "Lag Extintor",
    Default = false,
    Callback = function(state)
        toggles.DupeExtintor = state
        if state then
            local fireXPath = workspace:FindFirstChild("WorkspaceCom"):FindFirstChild("001_GiveTools"):FindFirstChild("FireX")
            if fireXPath then
                spawn(function()
                    dupeItem(fireXPath, 999999)
                end)
            else
                warn("Extintor não encontrado.")
            end
        else
            print("Dupe Extintor desligado.")
        end
    end
})

Tab:AddLabel("o script começa a fazer o efeito lagar depois de 35 segundos ")
 
local Section = Tab:AddSection({
    Name = "Lag Maca Hospital"
})

-- Variável para armazenar o estado do toggle
local toggles = { LagPhone = false }

-- Função para simular um clique normal
local function clickNormally(object)
    local clickDetector = object:FindFirstChildWhichIsA("ClickDetector")
    if clickDetector then
        fireclickdetector(clickDetector) -- Clica normalmente
    end
end

-- Função para lagar o jogo com o "Phone"
local function lagarJogoPhone(phonePath, maxTeleports)
    if phonePath then
        local teleportCount = 0
        while teleportCount < maxTeleports and toggles.LagPhone do
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = phonePath.CFrame
            clickNormally(phonePath)
            teleportCount = teleportCount + 1
            wait(0.01) -- Tempo de espera para evitar travamento
        end
    else
        warn("Phone não encontrado.")
    end
end

-- Criando Toggle para Lag Phone
Tab:AddToggle({
    Name = "Lag Phone",
    Default = false,
    Callback = function(state)
        toggles.LagPhone = state
        if state then
            local phonePath = workspace:FindFirstChild("WorkspaceCom"):FindFirstChild("001_CommercialStores"):FindFirstChild("CommercialStorage1"):FindFirstChild("Store"):FindFirstChild("Tools"):FindFirstChild("Iphone")
            if phonePath then
                spawn(function()
                    lagarJogoPhone(phonePath, 999999) -- Aqui usamos um número grande para o máximo de teletransportes
                end)
            else
                warn("Phone não encontrado.")
            end
        else
            print("Lag Phone desligado.")
        end
    end
})

Tab:AddLabel("o script começa a fazer o efeito lagar depois de 35 segundos ") 

-- Criação da aba
local Tab = Window:MakeTab({
    Name = "🔮 - Nomes",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

-- Seção dentro da aba
local Section = Tab:AddSection({
    Name = "Nome RGB"
})

-- Variáveis para rastrear os estados dos toggles
local isNameActive = false
local isBioActive = false

-- Toggle para ativar/desativar o RGB Name
Tab:AddToggle({
    Name = "Nome RGB",
    Default = false,
    Callback = function(value)
        isNameActive = value -- Define o estado baseado no toggle
        if isNameActive then
            print("RGB Name ativado")
        else
            print("RGB Name desativado")
        end
    end    
})

-- Label explicativo para o RGB Name
Tab:AddLabel("Ativar Nome RGB")

local Section = Tab:AddSection({
    Name = "RGB BIO"
})

-- Toggle para ativar/desativar o RGB BIO
Tab:AddToggle({
    Name = "RGB BIO",
    Default = false,
    Callback = function(value)
        isBioActive = value -- Define o estado baseado no toggle
        if isBioActive then
            print("RGB BIO ativado")
        else
            print("RGB BIO desativado")
        end
    end    
})


-- Label explicativo para o RGB BIO
Tab:AddLabel("Ativar RGB BIO")

-- Thread separada para o RGB Name
spawn(function()
    local vibrantColors = {
        Color3.fromRGB(255, 0, 0),   -- Vermelho
        Color3.fromRGB(0, 255, 0),   -- Verde
        Color3.fromRGB(0, 0, 255),   -- Azul
        Color3.fromRGB(255, 255, 0), -- Amarelo
        Color3.fromRGB(255, 0, 255), -- Magenta
        Color3.fromRGB(0, 255, 255), -- Ciano
        Color3.fromRGB(255, 165, 0), -- Laranja
        Color3.fromRGB(128, 0, 128), -- Roxo
        Color3.fromRGB(255, 20, 147) -- Rosa choque
    }

    while true do
        if isNameActive then
            local randomColor = vibrantColors[math.random(#vibrantColors)]
            local args = {
                [1] = "PickingRPNameColor",
                [2] = randomColor
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1RPNam1eColo1r"):FireServer(unpack(args))
        end
        wait(0.7) -- Ajuste o tempo de espera conforme necessário
    end
end)

-- Thread separada para o RGB BIO
spawn(function()
    local vibrantColors = {
        Color3.fromRGB(255, 0, 0),   -- Vermelho
        Color3.fromRGB(0, 255, 0),   -- Verde
        Color3.fromRGB(0, 0, 255),   -- Azul
        Color3.fromRGB(255, 255, 0), -- Amarelo
        Color3.fromRGB(255, 0, 255), -- Magenta
        Color3.fromRGB(0, 255, 255), -- Ciano
        Color3.fromRGB(255, 165, 0), -- Laranja
        Color3.fromRGB(128, 0, 128), -- Roxo
        Color3.fromRGB(255, 20, 147) -- Rosa choque
    }

    while true do
        if isBioActive then
            local randomColor = vibrantColors[math.random(#vibrantColors)]
            local args = {
                [1] = "PickingRPBioColor",
                [2] = randomColor
            }
            game:GetService("ReplicatedStorage").RE:FindFirstChild("1RPNam1eColo1r"):FireServer(unpack(args))
        end
        wait(0.7) -- Ajuste o tempo de espera conforme necessário
    end
end)

-- Add a section to the tab
local Section = Tab:AddSection({
    Name = "Adicionar Nomes no jogador" 
})

Tab:AddButton({
  Name = "Name: 👾 Anonymus 👾",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","👾 Anonymus 👾")
  end
})

Tab:AddButton({
  Name = "Name: 🏴‍☠️PRO 🏴‍☠️",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","🏴‍☠️ PRO 🏴‍☠️")
  end
})

Tab:AddButton({
  Name = "Name: ⚡️ ERR0R_666 ⚡️",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","⚡️ ERR0R_666 ⚡️")
  end
})

Tab:AddButton({
  Name = "Name: 👾 DARKNE1SSS 👾",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","👾 DARKNE1SSS 👾")
  end
})

Tab:AddButton({
  Name = "Name: 👻GHOST👻",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","👻 GHOST 👻")
  end
})

Tab:AddButton({
  Name = "Name: 🤡 JOKER 🤡",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","🤡 JOKER 🤡")
  end
})

Tab:AddButton({
  Name = "Name: 🌍 ADMIN 🌍 ",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","🌍 ADMIN 🌍")
  end
})

Tab:AddButton({
  Name = "Name: ☠️ TUBERS93 ☠️",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","☠️ TUBERS 93 ☠️")
  end
})

Tab:AddButton({
  Name = "Name: 👹 CO0LKID 👹",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","👹 CO0 LKID 👹")
  end
})

Tab:AddButton({
  Name = "Name: 👻 GAME ATTACKED BY CHAOS 👻",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName"," 👻 GAME ATTACKED BY CHAOS 👻")
  end
})

Tab:AddButton({
  Name = "Name: 🏴‍☠️ INC0MUN🏴‍☠️",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","🏴‍☠️ INC0MUN🏴‍☠️")
  end
})

Tab:AddButton({
  Name = "Name: 🏴‍☠️ BAD BOY🏴‍☠️",
  Callback = function()
    game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer("RolePlayName","🏴‍☠️BAD BOY 🏴‍☠️")
  end
})

-- Define as cores principais vibrantes, incluindo roxo e laranja
local colors = {
    Color3.new(1, 0, 0),     -- Vermelho
    Color3.new(0, 1, 0),     -- Verde
    Color3.new(0, 0, 1),     -- Azul
    Color3.new(1, 1, 0),     -- Amarelo
    Color3.new(1, 0, 1),     -- Magenta
    Color3.new(0, 1, 1),     -- Ciano
    Color3.new(0.5, 0, 0.5), -- Roxo
    Color3.new(1, 0.5, 0)    -- Laranja
}

-- Serviço de Replicação
local replicatedStorage = game:GetService("ReplicatedStorage")
local remoteEvent = replicatedStorage:WaitForChild("RE"):WaitForChild("1Player1sCa1r")

local isColorChanging = false
local colorChangeCoroutine = nil

-- Função para alternar cores
local function changeCarColor()
    while isColorChanging do
        for _, color in ipairs(colors) do
            if not isColorChanging then return end
            local args = {
                [1] = "PickingCarColor",
                [2] = color
            }
            remoteEvent:FireServer(unpack(args))
            wait(1)
        end
    end
end

local SoundTab = Window:MakeTab({
    Name = "🎵 - Sons com Sniper FE",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local sounds = {
    {name = "I See You [HORROR]", id = 2663254285},
    {name = "Sonic.exe [HORROR]", id = 2496367477},
    {name = "Tubers93 [FUNNY]", id = 6129291390},
    {name = "Tubers93 [FUNNY] 2", id = 9032712619},
    {name = "John's Laugh [FUNNY]", id = 130759239},
    {name = "Chucky Laugh [HORROR]", id = 132179181},
    {name = "Horror Bell [HORROR]", id = 9065965545},
    {name = "Garota Gritanndo [HORROR]", id = 7861818231},
    {name = "Goofy Scream [FUNNY]", id = 528432644}
}

local soundNames = {}
for _, sound in ipairs(sounds) do
    table.insert(soundNames, sound.name)
end

local function equipSniper()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local backpack = player.Backpack
    local sniperTool = character:FindFirstChild("Sniper") or backpack:FindFirstChild("Sniper")
    
    if not sniperTool then
        local args = {
            [1] = "PickingTools",
            [2] = "Sniper"
        }
        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Too1l"):InvokeServer(unpack(args))
        wait(0.1)
        character.Humanoid:EquipTool(backpack["Sniper"])
    elseif backpack:FindFirstChild("Sniper") then
        character.Humanoid:EquipTool(backpack["Sniper"])
    end
end

local function playSound(soundId)
    equipSniper()
    
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local sniperHandle = character:FindFirstChild("Sniper") and character.Sniper:FindFirstChild("Handle")
    
    if sniperHandle then
        local volume = 0.1
        local sound = Instance.new("Sound")
        sound.SoundId = "rbxassetid://" .. soundId
        sound.Volume = volume
        sound.Looped = false
        sound.Parent = player:WaitForChild("PlayerGui")
        sound:Play()
        sound.Ended:Connect(function()
            sound:Destroy()
        end)
    end

    local args = {
        [1] = sniperHandle,
        [2] = soundId,
        [3] = 1
    }
    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Gu1nSound1s"):FireServer(unpack(args))
end

local Section = SoundTab:AddSection({
    Name = "Selecione o Seu som Free e FE"
})

SoundTab:AddDropdown({
    Name = "Selecione seu som Gratis e FE! ",
    Default = "Select a sound...",
    Options = soundNames,
    Callback = function(selected)
        for _, sound in ipairs(sounds) do
            if sound.name == selected then
                playSound(sound.id)
                break
            end
        end
    end
})

SoundTab:AddLabel("Todos os sons são Gratis e FE")

local CarTab = Window:MakeTab({
    Name = "🚗 - Carro",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

local Section = CarTab:AddSection({
    Name = "Aumentar Velocidade do Carro"
})

-- Criando uma caixa de texto para definir a velocidade
CarTab:AddTextbox({
    Name = "Velocidade do Carro",
    Default = "",
    TextDisappear = false,
    Callback = function(Value)
        local pl = game.Players.LocalPlayer
        local Car = workspace.Vehicles:FindFirstChild(pl.Name .. "Car")
        local Speed = tonumber(Value)

        if Speed and Speed >= 0 and Speed <= 500 then
            if Car then
                Car.Body.VehicleSeat.TopSpeed.Value = Speed
            end
        end
    end
})

CarTab:AddLabel(" O carro vai até a Velocidade 200, não precisa de Gamepass")

local musicIds = {
    "81452315991527",
    "93786060174790",
    "74752089069476",
    "131592235762789",
    "132081774507495",
    "124394293950763",
    "16190782181",
    "1841682637",
    "3148329638",
    "124928367733395",
    "106317184644394",
    "100247055114504" ,
    "125259969174449",
    "89269071829332",
    "88094479399489",
    "72440232513341",
    "92893359226454",
    "111281710445018",
    "98677515506006",
    "105882833374061",
    "104541292443133",
    "105832154444494",
    "84733736048142",
    "94718473830640",
    "130324826943718",
    "123039027577735",
    "113312785512702",
    "139161205970637",
    "113768944849093",
    "135667903253566",
    "81335392002580",
    "77428091165211",
    "14145624031",                                                                                                         
    "8080255618",
    "8654835474",
    "13530439502",
    "18841894272",
    "90323407842935",
    "136932193331774",
    "113504863495384",
    "1836175030",
    "79998949362539"
}

-- Função para tocar música no carro
local function playCarMusic(musicId)
    if musicId and musicId ~= "" then
        local carArgs = {
            [1] = "PickingCarMusicText",
            [2] = musicId
        }
        game:GetService("ReplicatedStorage").RE:FindFirstChild("1Player1sCa1r"):FireServer(unpack(carArgs))
    else
        print("Por favor, insira um ID de música válido.")
    end
end

-- Função para tocar música no scooter
local function playScooterMusic(musicId)
    if musicId and musicId ~= "" then
        local scooterArgs = {
            [1] = "PickingScooterMusicText",
            [2] = musicId
        }
        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1NoMoto1rVehicle1s"):FireServer(unpack(scooterArgs))
    else
        print("Por favor, insira um ID de música válido.")
    end
end

-- Função para tocar música na casa
local function playHouseMusic(musicId)
    if musicId and musicId ~= "" then
        local houseArgs = {
            [1] = "PickHouseMusicText",
            [2] = musicId
        }
        game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Player1sHous1e"):FireServer(unpack(houseArgs))
    else
        print("Por favor, insira um ID de música válido.")
    end
end

-- Função para criar a interface do player de música
local function createMusicPlayerUI(tab)
    -- Adiciona a TextBox à aba fornecida
    tab:AddTextbox({
        Name = "Musica ID (Precisa da Gamepass)",
        Default = "",
        TextDisappear = false, -- Mantém o texto na TextBox
        Callback = function(value)
            playCarMusic(value)
            playScooterMusic(value)
            playHouseMusic(value)
        end
    })

    -- Adiciona uma lista de IDs de músicas à aba fornecida
    tab:AddDropdown({
        Name = "Seleciona a sua Musica FE (Precisa da Gamepass de Musica)",
        Options = musicIds,
        Callback = function(value)
            playCarMusic(value)
            playScooterMusic(value)
            playHouseMusic(value)
        end
    })
end

local Section = CarTab:AddSection({
    Name = "Musica Carros, Casas"
})

-- Chamada para criar a interface do player de música
createMusicPlayerUI(CarTab)

CarTab:AddLabel("O Script de Musica Funciona em todos os carros, Casas")

local Section = CarTab:AddSection({
    Name = "Carro RGB"
})

-- Adiciona o botão toggle para ativar/desativar a alternância de cores
CarTab:AddToggle({
    Name = "Carro RGB",
    Default = false,
    Callback = function(state)
        isColorChanging = state
        if isColorChanging then
            colorChangeCoroutine = coroutine.create(changeCarColor)
            coroutine.resume(colorChangeCoroutine)
        end
    end
})

CarTab:AddLabel("Ativando isso deixará seu carro RGB")

-- Supondo que você já tenha inicializado a Orion Library e criado uma janela e uma aba
-- Adicione este código onde você quiser criar o botão toggle

local args = { "Horn" }
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local remoteEvent = ReplicatedStorage:WaitForChild("RE"):WaitForChild("1Player1sCa1r")
local spamming = false

-- Função para spam da buzina
local function spamHorn()
    while spamming do
        remoteEvent:FireServer(unpack(args))
        wait(0.1) -- Espera 0.1 segundos antes de disparar novamente. Ajuste conforme necessário.
    end
end

-- Adicionar botão toggle à aba existente
CarTab:AddToggle({
    Name = "Spam Busina de Veiculo",
    Default = false,
    Callback = function(value)
        spamming = value
        if spamming then
            spawn(spamHorn)
        end
    end
})

local Section = CarTab:AddSection({
    Name = "Fly Car"
})

CarTab:AddButton({
    Name = "Fly Car",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/J4Te0hfn"))()
    end
})

CarTab:AddLabel("Ativand isso Você pode voar com o Seu carro")

local Section = CarTab:AddSection({
    Name = "Spamar Carros"
})

-- Lista de carros a serem spawnados
local carList = {
    "SchoolBus",
    "SmartCar",
    "FarmTruck",
    "Cadillac",
    "Excavator",
    "Jeep",
    "NascarTruck",
    "TowTruck",
    "Snowplow",
    "MilitaryTruck",
    "Tank",
    "Limo",
    "FireTruck"
}

-- Variável para controlar o loop
local spamCarsActive = false

-- Função para spawnar um carro
local function spawnCar(carName)
    local args = {
        [1] = "PickingCar",
        [2] = carName
    }
    game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Ca1r"):FireServer(unpack(args))
end

-- Toggle Spam Cars
CarTab:AddToggle({
    Name = "Spamar Cars",
    Default = false,
    Callback = function(state)
        spamCarsActive = state -- Ativa ou desativa o loop

        if spamCarsActive then
            -- Inicia o loop de spam de carros
            task.spawn(function()
                while spamCarsActive do
                    for _, carName in ipairs(carList) do
                        if not spamCarsActive then break end -- Sai do loop se o toggle for desativado
                        spawnCar(carName)
                        wait(0.4)
                    end
                end
            end)
        end
    end
})

CarTab:AddLabel("Spamar Varios carros ")

-- Teleport Tab 
local TeleportTab = Window:MakeTab({
    Name = "🏂 - Teleports",
    Icon = "rbxassetid://12941020168"
})

-- Add a section to the tab
local Section = TeleportTab:AddSection({
    Name = "Teleport Para os Locais "
})

-- Teleport to Criminal Button Function
local function teleportToCriminal()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-119, -28, 235)
end

TeleportTab:AddButton({
    Name = "🥷 - Crime Não é o Creme",
    Description = "Teleport to Criminal coordinates",
    Callback = function()
        teleportToCriminal()
    end
})

-- Teleport to House Abandoned Button Function
local function teleportToHouseAbandoned()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(986, 4, 63)
end

TeleportTab:AddButton({
    Name = "🧟‍♂️ - Casa Abandonada",
    Description = "Teleport to House Abandoned coordinates",
    Callback = function()
        teleportToHouseAbandoned()
    end
})

-- Teleport to Portal Agency Button Function
local function teleportToPortalAgency()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(672, 4, -296)
end

TeleportTab:AddButton({
    Name = "🏢 - Agencia",
    Description = "Teleport to Portal Agency coordinates",
    Callback = function()
        teleportToPortalAgency()
    end
})

-- Teleport to Secret Location Button Function
local function teleportToSecretLocation()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(505, -75, 143)
end

TeleportTab:AddButton({
    Name = "🤫 - Local Secreto",
    Description = "Teleport to Secret Location coordinates",
    Callback = function()
        teleportToSecretLocation()
    end
})

-- Teleport to School Button Function
local function teleportToSchool()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-312, 4, 211)
end

TeleportTab:AddButton({
    Name = "🏫 - Escola do Djabo",
    Description = "Teleporta para as coordenadas da Escola",
    Callback = function()
        teleportToSchool()
    end
})

-- Teleport to Brooks Diner Button Function
local function teleportToBrooksDiner()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(161, 8, 52)
end

TeleportTab:AddButton({
    Name = "🍔 - Hamburgueria",
    Description = "Teleporta para as coordenadas do Brooks Diner",
    Callback = function()
        teleportToBrooksDiner()
    end
})

-- Teleport to Hospital Button Function
local function teleportToHospital()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-309, 4, 71)
end

TeleportTab:AddButton({
    Name = "🏥 - Hospital",
    Description = "Teleporta para as coordenadas do Hospital",
    Callback = function()
        teleportToHospital()
    end
})

-- Teleport to Arch Button Function
local function teleportToArch()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-589, 141, -59)
end

TeleportTab:AddButton({
    Name = "🏹 - Arco",
    Description = "Teleporta para as coordenadas do Arco",
    Callback = function()
        teleportToArch()
    end
})

-- Teleport to Agency Button Function
local function teleportToAgency()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(179, 4, -464)
end

local ToolsTab = Window:MakeTab({
    Name = "🏑 - Itens",
    Icon = "rbxassetid://12580712235",
    PremiumOnly = false
})

local Section = ToolsTab:AddSection({
    Name = "All Tools"
})

ToolsTab:AddButton({
    Name = " Get all Tools",
    Description = "It's in beta, there are still some bugs",
    Callback = function()

local items = {
    "PropMaker", "Laptop", "ShoppingCart", "Paperbag", "Sign", "Book", "Envelope", "Paper",
    "ClipBoard", "Ticket", "BabyBoy", "BabyGirl", "Licence", "BabyHippo", "Stroller",
    "BabyBottle", "BabyMonkey", "Wagon", "Medicine", "Stethoscope", "Stretcher", "Toothbrush",
    "Hairbrush", "Ear", "Bloxaide", "BottledWater", "Milk", "Mocha", "CakePink", "GlockBrown",
    "Shotgun", "Glock", "Assault", "Sniper", "SwordWood", "Bow", "Bomb", "DuffleBag", "Cuffs", "Taser","Couch"
}

local remote = game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Too1l")

for _, item in ipairs(items) do
    remote:InvokeServer("PickingTools", item)
end
   end
})

ToolsTab:AddButton({
    Name = "Clear All Tools",
    Description = "It's in beta, there are still some bugs",
    Callback = function()

local args = {
    [1] = "ClearAllTools"
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer(unpack(args))
  end
})

ToolsTab:AddButton({
    Name = "Clear All Tools",
    Description = "It's in beta, there are still some bugs",
    Callback = function()

local args = {
    [1] = "ClearAllTools"
}

game:GetService("ReplicatedStorage"):WaitForChild("RE"):WaitForChild("1Clea1rTool1s"):FireServer(unpack(args))
  end
})

local Section = ToolsTab:AddSection({
    Name = "Sofa"
})

ToolsTab:AddButton({
    Name = "Pegar Sofa ",
    Description = "It's in beta, there are still some bugs",
    Callback = function()
        local args = {
            [1] = "PickingTools",
            [2] = "Couch"
        }
        game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
        print('Hello!')
    end
})

ToolsTab:AddLabel("Pegar o Item Sofa ")

local Section = ToolsTab:AddSection({
    Name = "Carrinho de Supermercado"
})

ToolsTab:AddButton({
    Name = " Pegar Carrinho de Supermercado",
    Description = "It's in beta, there are still some bugs",
    Callback = function()
local args = {
    [1] = "PickingTools",
    [2] = "ShoppingCart"
}

game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
   end
})

ToolsTab:AddLabel("Pegar o Item Carrinho de Supermercado ")

local Section = ToolsTab:AddSection({
    Name = "Carrinho de Hospital"
})

ToolsTab:AddButton({
    Name = " Carrinho de Hospital",
    Description = "It's in beta, there are still some bugs",
    Callback = function()
local args = {
    [1] = "PickingTools",
    [2] = "Stretcher"
}

game:GetService("ReplicatedStorage").RE:FindFirstChild("1Too1l"):InvokeServer(unpack(args))
   end
})

ToolsTab:AddLabel("Pegar o Item Carrinho de Hospital ")

-- Create a tab
local Tab = Window:MakeTab({
    Name = "Scripts Universais",
    Icon = "rbxassetid://15678286262",
    PremiumOnly = false
})

-- Add a section to the tab
local Section = Tab:AddSection({
    Name = "Scripts Universais"
})

Tab:AddButton({
    Name = "🏡 - Rael Hub brook",
    Callback = function()

loadstring(game:HttpGet("https://rawscripts.net/raw/The-Mimic-Rael-Hub-20921"))()
   end
})


Tab:AddButton({
    Name = "🏡 - Sander X brook",
    Callback = function()

loadstring(game:HttpGet("https://rawscripts.net/raw/Brookhaven-RP-Sander-x-22769"))()
   end
})

Tab:AddButton({
  Name = "🕳 -  ShiftLock",
  Callback = function()

loadstring(game:HttpGet("https://pastebin.com/raw/N2tiHgyv"))()
   end
})

Tab:AddButton({
    Name = "✍ - Chat Bypasser",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Chat-Bypasser-V3-24610"))()
    end
})

Tab:AddButton({
    Name = " ✔ - Anti Ban por Chat ",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/AnthonyIsntHere/anthonysrepository/main/scripts/AntiChatLogger.lua", true))()
    end
})

Tab:AddButton({
    Name = "👻 - Ghost Hub",
    Callback = function()

loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-GhostHub-16534"))()
   end
})

Tab:AddButton({
    Name = "🪙 - InfiniteYield - Cmd",
    Callback = function()
      loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
    end    
})

Tab:AddButton({
  Name = "⚙️ -  TP Tool",
  Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/err0r129/KptHadesBlair/main/Bao.lua"))()
       end
})

Tab:AddButton({
    Name = "🌊 - Fly Gui",
    Callback = function()
      loadstring(game:HttpGet("https://scriptblox.com/raw/Universal-Script-Fly-v3-7412"))()
    end    
})

Tab:AddButton({
    Name = "💎 - Nameless Admin - Cmd",
    Callback = function()
      loadstring(game:HttpGet("https://raw.githubusercontent.com/FilteringEnabled/NamelessAdmin/main/Source"))()
    end    
})

Tab:AddButton({
    Name = "📍- Telekinesis",
    Callback = function()
      loadstring(game:HttpGet(('https://raw.githubusercontent.com/SAZXHUB/Control-update/main/README.md'),true))()
    end    
})


OrionLib:MakeNotification({
    Name = "🌐 - Bem vindo ao Chaos Hub🌐",
    Content = "Obrigado por usarem minha Hub! ass: Luscaa ❤",
    Image = "rbxassetid://131669852271916",
    Time = 5
})

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "ScreenGui"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ResetOnSpawn = false

local Toggle = Instance.new("ImageButton")  -- Use ImageButton instead of TextButton
Toggle.Name = "Toggle"
Toggle.Parent = ScreenGui
Toggle.BackgroundColor3 = Color3.fromRGB(25, 25, 25)  -- Black background color
Toggle.BackgroundTransparency = 1  -- Set the button transparency to 
Toggle.Position = UDim2.new(0, 0, 0.454706937, 0)
Toggle.Size = UDim2.new(0, 30, 0, 30)  -- Smaller size for a compact circular button
Toggle.Image = "rbxassetid://131669852271916"  -- Replace IMAGE_ID with your image asset ID
Toggle.Draggable = true

local Corner = Instance.new("UICorner")
Corner.CornerRadius = UDim.new(0.5, 0)  -- Make the button circular
Corner.Parent = Toggle

local isOn = false  -- Initial state is off

-- Function to handle the "On" state
local function onButtonClicked()
    -- Add your code for what should happen when the button is in the "On" state
    if gethui():FindFirstChild("Orion") then
        gethui().Orion.Enabled = not gethui().Orion.Enabled
    end
end

-- Function to handle the "Off" state
local function offButtonClicked()
    -- Add your code for what should happen when the button is in the "Off" state
    if gethui():FindFirstChild("Orion") then
        gethui().Orion.Enabled = not gethui().Orion.Enabled
    end
end

Toggle.MouseButton1Click:Connect(function()
    isOn = not isOn  -- Toggle state
    if isOn then
        onButtonClicked()  -- Call the function for "On" state
    else
        offButtonClicked()  -- Call the function for "Off" state
    end
end)
