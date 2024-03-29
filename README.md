# WGetLlmHug
Status: Development (O_o/'
<br> Work planned for next release...
- Retry download works splendid, but the download function is now broken also, this has become a headache, and I have focused on other parts of the program, even though its the main thing, even feeding it working versions of main scipt from 0.02 has not worked twice.
- Testing of download, to see if will move to completed folder.
- Better display when downloading a model, what options are available, and how can we best visualize the information on a single download...lets make it epic, even if it could potentially defeat some robustness, we want it to look COOL...
<br>Work done for next release...
- If complete files in temporary for a new download, these are moved to completed folder.
- Misc fixes and upgrades
- Complementing Optimizations
- Improvements for UI layout in main script.
- All scripts now have same visual themes
- Retry code re-implemented.
- Setup upgraded to perfection.

## Description
WGetLlmHug is a PowerShell script complemented by Batch scripts, designed to simplify file downloads, specifically for, GGUF and GPTQ, HuggingFace model files, using the `wget` utility. It's tailored for users with limited internet access and older systems, supporting PowerShell 5 for Windows 7/8.1 compatibility, but also works on newer systems, either way for such purposes it is a, robust and optimised, tool.

## Features:
- **Complex URL Reading**: Extracts filenames from HuggingFace URLs containing ".gguf" and ".gptq".
- **Download Method Selection**: Utilizes `wget.exe` for downloads.
- **File Management**: Organizes files into "temporary", "Downloads", and "Completed" folders.
- **Interactive Menus**: Features user-friendly menu systems in both PowerShell and Batch scripts.
- **Installer Script**: Ensures the setup of required folders and downloads `wget.exe` if not present.
- **Launcher Script**: Provides an easy way to run the PowerShell script, especially for users unfamiliar with PowerShell commands.

## Interface:
```

=====================( WGetLmmHug )======================


                   1. Download A Model,
                   2. Scan Folders,

                   0. Exit Program.


\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/

Enter Your Choice:
















```
```
--2023-12-20 13:34:23--  https://cdn-lfs-us-1.huggingface.co
/repos/52/79/5279038ee7db94f4d3fe0026f9ec759ac5211a30aad8ee7
5fd69a470306e8c7f/cbfc52efd83d35ed194f0f33bb588fc6f7bd17b98e
f62ba4e3af13e21e833dd1?response-content-disposition=attachme
nt%3B+filename*%3DUTF-8''quantum-dpo-v0.1.Q8_0.gguf%3B+filen
ame%3D%22quantum-dpo-v0.1.Q8_0.gguf%22%3B&Expires=1703338396
&Policy=eyJTdGF0ZW1lbnQiOlt7IkNvbmRpdGlvbiI6eyJEYXRlTGVzc1Ro
YW4iOnsiQVdTOkVwb2NoVGltZSI6MTcwMzMzODM5Nn19LCJSZXNvdXJjZSI6
Imh0dHBzOi8vY2RuLWxmcy11cy0xLmh1Z2dpbmdmYWNlLmNvL3JlcG9zLzUy
Lzc5LzUyNzkwMzhlZTdkYjk0ZjRkM2ZlMDAyNmY5ZWM3NTlhYzUyMTFhMzBh
YWQ4ZWU3NWZkNjlhNDcwMzA2ZThjN2YvY2JmYzUyZWZkODNkMzVlZDE5NGYw
ZjMzYmI1ODhmYzZmN2JkMTdiOThlZjYyYmE0ZTNhZjEzZTIxZTgzM2RkMT9y
ZXNwb25zZS1jb250ZW50LWRpc3Bvc2l0aW9uPSoifV19&Signature=Z2Xv6
7Eb6QyiFHP1R-MQyiOj6u8Jd42SOX5J5pneGO9H624EOmMD0enBkCfqN9pvB
91ndo6ymJQtGXCIeV18vUpWVu~AWDY2hYgFM2bwSWFYga9nFQznve62I1C1r
D33OKIKPp33Gg3pNbq8iaxTPLt2RC-61vcOMquW1u5gvutCTV-f6LAUFfGdG
P7WVFe34xevc8uZyydGccKHN6fXIY5CnelH0UWJmkC3bI8qNBRolaCTNyuHs
XTAUBjJJm4Xe15kNnaT-C00Kj~p4LfksSYJB2VwuZNNSdN7S4jbhUqY3fwxy
KrB0nnG5atZiD2gM8jT-VEe7gg-NA~4reO1jw__&Key-Pair-Id=KCD77M1F
0VK2B
Resolving cdn-lfs-us-1.huggingface.co (cdn-lfs-us-1.huggingf
ace.co)... 18.244.140.29, 18.244.140.43, 18.244.140.108, ...

Connecting to cdn-lfs-us-1.huggingface.co (cdn-lfs-us-1.hugg
ingface.co)|18.244.140.29|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 7696793728 (7.2G) [binary/octet-stream]
Saving to: './temporary/quantum-dpo-v0.1.Q8_0.gguf'

emporary/quant  38%[>    ]   2.77G  1.49MB/s    eta 58m 57s

```

## Usage
1. Copy WGetLlmHug to its own folder, then run `Setup-Install.Bat`, this sets up, `wget.exe` and folders.
2. Create folder for model to download to, and put in it, config.json and the readme.md, from HuggingFace.
3. Partially download the model file, then cancel the download and copy the link it gave (it must be done like this).
4. Run `WGetLlmHug.Bat`, select `Enter URL`from the menu, and paste the link, it will now download. 
5. When download is finished then move it from `.\Completed` to the model folder you made.

## Requirements
- Windows 7/8.1/10/11
- Processor x32/x64/x64a
- PowerShellCore (get the `.msi` from [Here](https://mirrors.sdu.edu.cn/github-release/1700313102/github-release/PowerShell_PowerShell/v7.4.0/)).
- Internet connection.
- Some libraries installed through "Setup-Install.Bat".
- URL linked to a file with ".gguf" or ".gptq" format.

## Note
WGetLlmHug is a simplified concept compared to "Downlord", WGetLlmHug is focused on language models, where as Downlord is intended as a more general purpose downloader.

## DISCLAIMER
This software is subject to the terms in License.Txt, covering usage, distribution, and modifications. For full details on your rights and obligations, refer to License.Txt.
