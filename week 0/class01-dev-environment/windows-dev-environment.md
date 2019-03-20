# Windows dev tools

### The state of development in Windows
Windows, as a development envrionment, has historically been the realm of proprietary application and software development.  Tools like Visual Studio, and languages such as Java and C++ have been the norm, and Microsoft, and the community at large, have only recently started to push to make Windows a [FOSS](https://en.wikipedia.org/wiki/Free_and_open-source_software)-friendly environment.  As a result, and owing to some inherent differences in how Windows and Mac/Linux function, Windows tools have lagged behind and/or have been relatively more difficult to install.  This has largely changed for the better, though there are still some idiosyncracies that can be a problem.  

Here at ACL, we recommend the following tools: 
### Essentials

- [git bash](https://git-scm.com/download/win) 
- [chocolatey](https://chocolatey.org/install)
- [VS Code](https://chocolatey.org/packages/vscode)
- [Windows Build Tools](https://www.npmjs.com/package/windows-build-tools)

### Helpful tools

- [Agent Ransack](https://chocolatey.org/packages/agentransack)
- [Heroku CLI tools](https://devcenter.heroku.com/articles/heroku-cli)
- [Ruby](https://chocolatey.org/packages/ruby)
- [Vue CLI tools](https://cli.vuejs.org/)
- [Travis CI tools](https://github.com/travis-ci/travis.rb#installation)
- [nvm for Windows](https://github.com/coreybutler/nvm-windows/releases)
- [Fiddler](https://chocolatey.org/packages/fiddler)
- [Postman](https://chocolatey.org/packages/postman)

### Other helpful hints

- [bash aliases](#bash)

### bash

#### A bit of exposition on bash

Bash is a [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) command interpreter that takes input (a command), does the thing, and returns a result.  These are usually referred to as *command shells*, or simply a *shell*. Windows ships with two built in shells, PowerShell, and cmd.exe.  Bash is generally the default shell in the Linux and Mac world, and so adding it to Windows is a logical extension that Github added to better support git commands.  Microsoft has also expanded on this idea with the [Windows Subsystem for Linux](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux), but for [reasons](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/), we don't recommend using that as a developer tool.

When bash starts up, it reads a file called `.bash_profile` which in turn reads a file called `.bashrc`, and this file stores configurations and customzations for your environment.

#### setting up aliases

Aliases in bash are a means of shortening common commands.  For example, I type `ls -l` all the time, so I shortened it to `ll`, and the command to do that is `alias ll='ls -l'`.  If you have an alias you use a great deal, you can add that definition to your `.bashrc` file.  If, like me, you start to accumulate great deal of aliases, you can put them in their own file and read it from `.bashrc`.  My own setup, I have a file called `.bash_aliases` and a line in `.bashrc` that reads it:

`[ -f ~/.bash_aliases ] && source ~/.bash_aliases`

See more at [my dotfiles repo.](https://github.com/goodwid/bashdotfiles/)