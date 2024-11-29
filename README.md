# Windows fresh install

This is mine comprehensive guide for myself of what to do after a fresh install
of windows.\
I should not use this ofter but, but i'll update and use it as necessary of
course.

1_ When installing win11, turn off the internet by removing the cable or
executing the command `ipconfig /release` in the `shift + f10` console, and in
the same console insert command `oobe\bypassnro` to skip microsoft email
binding.

2_ After getting in the workspace for the first time, execute the following
command on powershell and chose the settings as normal:

```ps
& ([scriptblock]::Create((irm "https://win11debloat.raphi.re/")))
```

And wait it to run it trough.\
If the script not work, or something seems wrong, always consult original github
repo: [Win11Debloat](https://github.com/Raphire/Win11Debloat)

3_ Install all windows updates, reboot windows multiple times if necessary.

4_ Install necessary drivers, currently they can be found at:

- [Gigabyte Motherboard](https://www.gigabyte.com/br/Motherboard/X670-GAMING-X-AX-V2-rev-10/support)
- [AMD Graphics Card](https://www.amd.com/pt/support/download/drivers.html)

4_ Install some apps I normally use and don't download through scoop:

- [Firefox](https://www.mozilla.org/pt-BR/firefox/download/thanks/)
- [Discord](https://discord.com/)
- [Vencord](https://vencord.dev/)
- [Steam](https://store.steampowered.com/?l=portuguese)
- [Vscode](https://code.visualstudio.com/)
- [Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701)

5_ Install [Scoop](https://scoop.sh/) with the following command:

```ps
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

6_ Install Scoop buckets and apps from backup list using command:

```ps
scoop install git
scoop import .\app_list.json
```

usually I keep a copy of this in my OneDrive, but any backup might serve.\
Remember to import reg file from 7zip using `reg import ".\file.reg"` but not
from git.

7_ Install additional apps thats not strictly necessary: 
- [Taiga](https://taiga.moe/)

8_ Install current played game, this will be probably remembered every time that I need a clean install, but no harm to remember.
