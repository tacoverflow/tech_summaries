# SSH says you are ok but GIT does not works

If you are using new versions of windows like windows 10, ssh comes included with the OS so if you install a new version of ssh or git from 3rd party package managers like [**scoop**](https://scoop.sh) it will cause some issues.
You have some thing to fix this issue:

- Disable all ssh included by windows and use the git+ssh from your package manager
	- cons: 
		- this will not be permanent since a windows update can enable it.
- Disable ssh and git from your package manager and use binaries from windows
	- pros:
		- This will be a permanent solution
	- cons:
		-  You have to manually install/remove the programs using an installer
		-  Version management is a manual task
-  Use git from your package manager and ssh from windows
	-   You need to run this to tell github to use ssh from windows
```powershell
# https://github.community/t/git-via-ssh-from-windows-returns-permission-denied/1107/24
git config --global core.sshCommand "C:/Windows/System32/OpenSSH/ssh.exe"
```   
