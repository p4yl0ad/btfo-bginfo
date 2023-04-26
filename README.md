# btfo-bginfo

Edit example.vbs and execute with the following:
```
Bginfo64.exe working.bgi /timer:0 /nolicprompt
```


This strangely only detects based on two cli flags 
https://github.com/SigmaHQ/sigma/blob/master/rules/windows/process_creation/proc_creation_win_lolbin_bginfo.yml
```
detection:
    selection:
        Image|endswith: '\bginfo.exe'
        CommandLine|contains|all:
            - '/popup'
            - '/nolicprompt'
```
