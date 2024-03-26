# extfilter

Powershell Script to list and copy files to a particular directory.

```powershell
./extfilter.ps1
```

```

  ░▒▓█▓▒░░▒▓█▓▒░░▒▓████████▓▒░░▒▓█▓▒░       ░▒▓█▓▒░       ░▒▓██████▓▒░       ░▒▓█▓▒░░▒▓█▓▒░░▒▓███████▓▒░  ░▒▓██████▓▒░  
  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒░       ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░ 
  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒░       ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒▒▓█▓▒░ ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░ 
  ░▒▓████████▓▒░░▒▓██████▓▒░  ░▒▓█▓▒░       ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒▒▓█▓▒░ ░▒▓███████▓▒░ ░▒▓█▓▒░░▒▓█▓▒░ 
  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒░       ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░        ░▒▓█▓▓█▓▒░  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░ 
  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░       ░▒▓█▓▒░       ░▒▓█▓▒░      ░▒▓█▓▒░░▒▓█▓▒░        ░▒▓█▓▓█▓▒░  ░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░░▒▓█▓▒░ 
  ░▒▓█▓▒░░▒▓█▓▒░░▒▓████████▓▒░░▒▓████████▓▒░░▒▓████████▓▒░░▒▓██████▓▒░          ░▒▓██▓▒░   ░▒▓█▓▒░░▒▓█▓▒░ ░▒▓██████▓▒░  
                                                                                                                                                                                                                                                
                ⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⡤⠖⠒⠢⢄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⠀⠀⠀⡴⠃⠀⠀⠀⠀⠀⠙⢦⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⠀⠀⣰⠁⠀⠀⠀⠀⠀⠀⠀⠈⠳⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⠀⡰⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
                ⠀⠀⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⠀⠂⠀⠤⠤⡀⠈⠳⣄⠀⠀⠀⠀⠀⠀⠀⠀
                ⠀⠀⣠⠞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠑⢄⠀⠀⠀⠀⠀⠀
                ⢠⠞⠁⠀⣀⣠⣤⠤⠤⠤⠤⢤⣤⠤⠤⠤⠤⣤⣀⣀⡀⠀⠀⠀⠑⢤⠀⠀⠀⠀
                ⣣⠔⠚⠻⣄⣡⣞⣄⣠⣆⠀⢼⣼⣄⣀⣀⣠⣆⠜⡘⡻⠟⠙⣲⠦⣈⢳⡀⠀⠀
                ⡇⠒⢲⡤⡜⠉⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠉⠙⠛⠤⣖⠬⠓⠂⠉⣿⠇⠀⠀
                ⠙⠲⠦⠬⣧⡀⠀⠀⠀⠀⠀⣠⣿⣿⣷⡄⠀⠀⠀⠀⠀⣞⠀⢀⣲⠖⠋⠀⠀⠀
                ⠀⠀⠀⠀⠘⣟⢢⠃⠀⠀⠀⠉⠙⠻⠛⠁⠀⠀⠀⢀⡜⠒⢋⡝⠁⢀⣀⣤⠂⠀
                ⠀⠀⠀⠀⠀⡇⠷⠆⠶⠖⠀⠀⠀⠀⠀⠀⠀⠀⣠⠮⠤⠟⠉⠀⢰⠱⡾⣧⠀⠀
                ⠀⠀⠀⠀⠀⠹⢄⣀⣀⠀⠀⠀⠀⠀⠀⣀⡤⠚⠁⠀⢠⣤⡀⣼⢾⠀⠀⡟⠀⠀
                ⠀⠀⠀⠀⠀⠀⠀⠀⠙⠛⠛⠒⡏⠀⡡⠣⢖⣯⠶⢄⣀⣿⡾⠋⢸⢀⡶⠿⠲⡀
                ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡰⣹⠃⣀⣤⠞⠋⠀⠉⠢⣿⣿⡄⠀⣿⠏⠀⠀⠐⢣
                ⠀⠀⠀⠀⠀⠀⠀⠀⣠⠞⢱⢡⡾⠋⠀⠀⢀⡐⣦⣀⠈⠻⣇⢸⢁⣤⡙⡆⠈⡏
                ⠀⠀⠀⠀⠀⠀⣠⠎⢁⠔⡳⡟⠀⠐⠒⠒⠋⠀⠠⡯⠙⢧⡈⠻⣮⠯⣥⠧⠞⠁
                ⠀⠀⠀⣀⠴⠋⠀⢶⠋⢸⡝⠀⠀⠀⠀⠀⠀⠀⠀⣸⢦⠀⠙⡆⠘⠦⢄⡀⠀⠀
                ⠀⠀⣸⠅⢀⡤⢺⢸⠀⢸⡃⠤⠀⠀⠀⠀⣀⡤⢚⣋⣿⢄⡀⢇⡀⠀⠀⣝⡶⠀
                ⠀⠀⢿⠀⡏⠀⠘⠞⠀⢸⡵⣦⠤⠤⠖⣿⠥⠞⠉⠀⢸⠖⠁⠀⠙⠢⣑⠶⣽⢂
                ⠀⠀⠸⠤⠃⠀⠀⠀⠀⠀⠉⢳⠂⠈⡽⠁⠀⠀⠀⢀⡼⠒⠓⢤⠀⠀⠀⠙⠚⠛
                ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠓⡎⠀⠀⠀⠀⢠⠎⣠⠀⠀⠈⢳⠀⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡇⠀⠀⢸⡶⠗⠋⣱⠄⠀⠀⠀⣧⠀⠀⠀⢀
                ⠀⠀⠀⠀⠀⠀⠀⣀⠴⠒⠒⠦⣤⣷⠂⢀⡸⠁⠀⡼⠁⠀⠀⠀⠈⢺⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⢠⠋⢀⣀⡀⠀⠀⠀⠀⠀⠈⡇⠀⠀⠙⠢⠤⠤⣄⡤⠼⠀⠀⠀⠀
                ⠀⠀⠀⠀⠀⠀⠑⢦⣄⣉⣑⠢⠄⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
                    ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠉⠙⠓⠒⠒⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀

  ▓█████ ▒██   ██▒▄▄▄█████▓     █████▒██▓ ██▓  ▄▄▄█████▓▓█████  ██▀███  
  ▓█   ▀ ▒▒ █ █ ▒░▓  ██▒ ▓▒   ▓██   ▒▓██▒▓██▒  ▓  ██▒ ▓▒▓█   ▀ ▓██ ▒ ██▒
  ▒███   ░░  █   ░▒ ▓██░ ▒░   ▒████ ░▒██▒▒██░  ▒ ▓██░ ▒░▒███   ▓██ ░▄█ ▒
  ▒▓█  ▄  ░ █ █ ▒ ░ ▓██▓ ░    ░▓█▒  ░░██░▒██░  ░ ▓██▓ ░ ▒▓█  ▄ ▒██▀▀█▄  
  ░▒████▒▒██▒ ▒██▒  ▒██▒ ░    ░▒█░   ░██░░██████▒▒██▒ ░ ░▒████▒░██▓ ▒██▒
  ░░ ▒░ ░▒▒ ░ ░▓ ░  ▒ ░░       ▒ ░   ░▓  ░ ▒░▓  ░▒ ░░   ░░ ▒░ ░░ ▒▓ ░▒▓░
   ░ ░  ░░░   ░▒ ░    ░        ░      ▒ ░░ ░ ▒  ░  ░     ░ ░  ░  ░▒ ░ ▒░
     ░    ░    ░    ░          ░ ░    ▒ ░  ░ ░   ░         ░     ░░   ░ 
     ░  ░ ░    ░                      ░      ░  ░          ░  ░   ░                                                                             

```
