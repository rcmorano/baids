# Description

'baids' stands for "bash aids" and it's just a way for managing your daily bash aliases and functions.

# Installation

Just call the main script with the "install" argument:

```
curl -sSL https://raw.githubusercontent.com/rcmorano/baids/master/baids | bash -s install
```

Example:

```
root@6169068ffaa9:/# curl -sSL https://raw.githubusercontent.com/rcmorano/baids/master/baids | bash -s install
Cloning into '/root/.baids'...
remote: Counting objects: 33, done.
remote: Compressing objects: 100% (20/20), done.
remote: Total 33 (delta 11), reused 28 (delta 6)
Unpacking objects: 100% (33/33), done.

[+] 'baids' is now installed!
[-] Now please, load 'baids' executing:

    source /root/.baids/baids
root@6169068ffaa9:/#
```

It just clones the project at '~/.baids/' and adds an include in your '.bashrc'.

# Upgrade

Just call 'baids-upgrade' or its alias 'bu':

```
root@6169068ffaa9:/# bu 
remote: Counting objects: 7, done.
remote: Compressing objects: 100% (1/1), done.
remote: Total 4 (delta 2), reused 4 (delta 2)
Unpacking objects: 100% (4/4), done.
From https://github.com/rcmorano/baids
   2093d14..b3d2ad4  master     -> origin/master
   First, rewinding head to replay your work on top of it...
   Fast-forwarded master to b3d2ad4623f1371ef1044932518ab98200017f32.
root@6169068ffaa9:/#
```

# Usage

You will usually type the first letter of the function or alias you'd like to use and press \<TAB\> to complete :]

Here is the current functions list and some info. Although most are self explanatory, some need notes:

* **baids-reload**: reload aliases and functions
* **baids-remap**: recreates alias files from functions in 'functions.d' dir, then reloads them.
It makes acronym-based aliases for each function in a separated file in 'aliases.d'. In e.g.:
```
# contents of $HOME/.baids/aliases.d/00-baids
alias br='baids-reload'
alias bre='baids-remap'
alias bu='baids-upgrade'
```
* **baids-upgrade**: pull rebases your baids installation. Be careful :]

# Extending/Contributing

1. Fork project
2. Put some bash functions in 'functions.d' dir 
3. Execute 'baids-remap' and get shortened aliases for your functions
4. Commit your changes
5. Optionally, if you consider that your functions are generic enough to help someone out there, send me a pull request! 

# License and Author                                                             
                                                                                 
Author:: Roberto C. Morano (<rcmova@gmail.com>)                                  
                                                                                 
Copyright:: 2014, Roberto C. Morano (<rcmova@gmail.com>)                         
                                                                                 
Licensed under the Apache License, Version 2.0 (the "License");                  
you may not use this file except in compliance with the License.                 
You may obtain a copy of the License at                                          
                                                                                 
    http://www.apache.org/licenses/LICENSE-2.0                                   
                                                                                 
Unless required by applicable law or agreed to in writing, software              
distributed under the License is distributed on an "AS IS" BASIS,                
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.         
See the License for the specific language governing permissions and              
limitations under the License.
