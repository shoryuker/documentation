# Record Format
Each account will build one JSON file and each entry and game will recorded and built upon in the file. The record will have unchangeable information before entry lines. <br>

## Record Filename Format
UUID<br>
Example: 8374464.json

# Entry Structure
Each entries in each profile have the following contents with attributes or booleans that gets pulled from the database.<br>

## Contents for Entry
Game Type<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Casual<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ranked<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tournament<br>
Set Type<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;First to ??? - Example: FT[UserInput] = FT5<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Best of ??? - Example: BO[UserInput] = BO3<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Continuous Sets<br>
End Score<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Round W/L Count *(If Game Type is Ranked or Casual)* - Example: [W/L/D], [W/L/D], [W/L/D] = W, L, W<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Placement *(If Game Type is Tournament)* - Example: [userInput] out of [userInput] = 3rd out of 10<br>
Date Played</br>
***(Optional)*** Entry Name - Example: [userInput] = vs. Hollis <br> 
***(Optional)*** VOD Link<br>
Character(s) Played<br>
Miscellaneous Content **(Varies Between Game Pages)**<br>

# Record & Entry Example
Filename: 5434567.json
```json
[
    {
        "user": {
            "uuid": 5434567,
            "email": "brandon8750@outlook.com",
            "emailVerified": true,
            "lastLogon": 1710046552
        }
    },

    {
        "gameID": "cvs2fc" {
            "entryID": 7 {
                "gameType": "ranked",
                "setType": "ft3",
                "endScore": "W, W, W",
                "datePlayed": "03102024",
                "entryName": "vs. Merlinksz",
                "vodRedirect": "N/A",
                "charactersPlayed": {
                    "r1": "rock, sagat, iori",
                    "r2": "rock, sagat, iori",
                    "r3": "hibiki, rock, akuma"
                },
                "grooveChosen": {
                    "r1": "n-groove",
                    "r2": "n-groove",
                    "r3": "a-groove"
                }       
            }
            "entryID": 8 {
                "gameType": "casual",
                "setType": "ft1",
                "endScore": "L",
                "datePlayed": "03152024",
                "entryName": "vs. USERKID",
                "vodRedirect": "N/A",
                "charactersPlayed": {
                    "r1": "ryu, ken"
                },
                "grooveChosen": {
                    "r1": "n-groove"
                },
            },
        },
        "gameID": "t824" {
            "entryID": 2 {
                "gameType": "casual",
                "setType": "ft1",
                "endScore": "L",
                "datePlayed": "03132024",
                "entryName": "tore up  JonathanDingusTeague, he is so trash",
                "vodRedirect": "N/A",
                "charactersPlayed": {
                    "r1": "bryan"
                },
            },
        },
    },
    
]
```



