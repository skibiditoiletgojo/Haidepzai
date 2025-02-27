getgenv().Mirage = function()
    local url = 'https://piphuc273.vercel.app/mirage'
    local chooses
    local foundServers = game:GetService('HttpService'):JSONDecode(game:HttpGet(url))
    for i, v in foundServers do
        if v.jobId ~= game.JobId then
            chooses = v
        end
    end
    game:GetService("TeleportService"):TeleportToPlaceInstance(7449423635, chooses.jobId, game.Players.LocalPlayer)
end

function CheckIsland()
    return game.Workspace._WorldOrigin.Locations:FindFirstChild("Mirage Island")
end

spawn(function()
    while task.wait(4) do
        pcall(function()
            if not CheckIsland() then
                return Mirage()
            end
        end)
    end
end)
