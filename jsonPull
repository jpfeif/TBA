import requests
import json


event = "2019wimi"

eventTeams = "https://www.thebluealliance.com/api/v3/event/" + event + "/teams"

teamsRaw = requests.get(eventTeams, params={'X-TBA-Auth-Key': 'oJ8q81FBEVKJlR3rVaVKhgJ3nGxjeGNy44DktYMHxdtBRjTPLBI2hIZX95SRNxXk'})
matchesRaw = requests.get("https://www.thebluealliance.com/api/v3/event/" + event + "/matches", params ={'X-TBA-Auth-Key': 'oJ8q81FBEVKJlR3rVaVKhgJ3nGxjeGNy44DktYMHxdtBRjTPLBI2hIZX95SRNxXk'})

teamsData = teamsRaw.json()
matchesData = matchesRaw.json()
#Creats list keys
keys = []
matchesKey = []

#looks for team key in data and saves to list keys
for key in teamsData:
    keys.append(key['key'])


for key in matchesData:
    matchesKey.append(key['key'])

teamCount = len(keys)


while teamCount != 0:
    teamCount = teamCount - 1
    teamNum = teamsData[teamCount]
    string = keys[teamCount]
    fileName = 'team' + string +  '.txt'
    file = open("fileName", "w+")
    file.write(requests.get("https://www.thebluealliance.com/api/v3/event/" + event + "/matches", params ={'X-TBA-Auth-Key': 'oJ8q81FBEVKJlR3rVaVKhgJ3nGxjeGNy44DktYMHxdtBRjTPLBI2hIZX95SRNxXk'}))

   



