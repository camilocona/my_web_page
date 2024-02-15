Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page
$ git init
Initialized empty Git repository in C:/Desarrollo_Web/my_web_page/.git/

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ touch index.html

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ ls
index.html

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git add index.html

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html


Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git commit -m "Mi primer commit agregando un nuevo index.html"
[master (root-commit) ed59db2] Mi primer commit agregando un nuevo index.html
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git status
On branch master
nothing to commit, working tree clean

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git log
commit ed59db25d783640b6b2651760b1a25d033ed1155 (HEAD -> master)
Author: camilocona <camilocona2@gmail.com>
Date:   Thu Feb 15 18:13:09 2024 -0500

    Mi primer commit agregando un nuevo index.html

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git remote add origin git@github.com:camilocona/my_web_page.git

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (master)
$ git branch -M main

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ git push -u origin main
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ssh-keygen -t rsa -b 4096 -C "camilocona2@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/SPB_Data/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/SPB_Data/.ssh/id_rsa
Your public key has been saved in /c/SPB_Data/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:Znrfte12L9Oo5KOKx0k1foLMreT0osbjO/cnmNAvcKI camilocona2@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|                 |
|                 |
|                 |
|          o      |
|       +S= .     |
|      ++X + .    |
|     o.@.B o. .o |
|    E =o%.++o.+o+|
|     o=B.=+++o.=*|
+----[SHA256]-----+

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ssh-add /c/SPB_Data/.ssh/id_rsa
Could not open a connection to your authentication agent.

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ eval `ssh-agent -s`
Agent pid 1190

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ssh-add /c/SPB_Data/.ssh/id_rsa
Identity added: /c/SPB_Data/.ssh/id_rsa (camilocona2@gmail.com)

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ cat ~/c/SPB_Data/.ssh/id_rsa.pub
cat: /c/SPB_Data/c/SPB_Data/.ssh/id_rsa.pub: No such file or directory

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ls /c/SPB_Data/.ssh/id_rsa
/c/SPB_Data/.ssh/id_rsa

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ cd /c/SPB_Data/.ssh/id_rsa
bash: cd: /c/SPB_Data/.ssh/id_rsa: Not a directory

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ cd /c/SPB_Data/.ssh/

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ ls
id_rsa  id_rsa.pub  id_rsa_ssh  id_rsa_ssh.pub  known_hosts

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ $ cat ~/c/SPB_Data/.ssh/id_rsa_ssh.pub
bash: $: command not found

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ ^[[200~cat ~/c/SPB_Data/.ssh/id_rsa_ssh.pub
bash: $'\E[200~cat': command not found

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ cat ~/c/SPB_Data/.ssh/id_rsa_ssh.pub
cat: /c/SPB_Data/c/SPB_Data/.ssh/id_rsa_ssh.pub: No such file or directory

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ cat /c/SPB_Data/.ssh/id_rsa_ssh.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCmUZn/J282kKV82NNmBoNv+c3zKfcT4QxkKtDodXgl8+7Z07gqOGtSrqtsjtLJXVf4dAv27CyT9Q2b82H8kAHI6DEY5fuEO3RZBUAPNA575XVoING+GaiJk0W0sUgko5DjEdLZLFrKwfoAhm+FjpAcuaAVBMMEY/9feOxY1StCcnHV/oQmmSMFXfZMxprhlCV3MUBVxDxdR46erRQKnt5WI8LNZGgdqc/wFa8dBlmCOXj/DYVqnyVimn6djbMsybK7Xq4mNUG06LEUIRECufhBACElXvcm/s1b13pa1vKBU4JTje2GumSve1h1Z0tTiNLRiFYAE0ZTQuNR5xR75K4Z0F/emVWoqpIrZOQb+YHDdzzwoeZB7fZiFrMo6zo1XMa9dOdhSjpB3Gy6i1R26CwV3DQxDsgsCVOb241kvk+lm9x4eBl5VwlRl32zk9HTegIKIGCgprGF9OjgDruMkaeCnKL3Nhl/UHueYMD0dNQXsrBU+hRh0xtRgb46QnafLYR4F7bvtrjTHeGG87c65w8tuk+Ikk0j3xEuNPvtiTSdyWG6bj6+wP0X5pJDxMcIgo46OLiHxHgbirLMt10BRqJXCZRNIdqkYYMa18vFweC6gOKckvZP43FXBsK9do6FK5AjdKssfNWGYpir5J/ubmvJ8bkWUHO5e+jjfoNCy7hTDw== camilocona2@gmail.com

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ git remote -v
fatal: not a git repository (or any of the parent directories): .git

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~/.ssh
$ cd ..

Camilo Anacona@LAPTOP-SD759LKP MINGW64 ~
$ cd /c

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c
$ cd /Desarrollo_Web/my_web_page
bash: cd: /Desarrollo_Web/my_web_page: No such file or directory

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c
$ ls
'$Recycle.Bin'/             OneDriveTemp/                 Users/
'$WinREAgent'/              OrCAD/                        Windows/
 4DefaultTempSaveScan/      P6/                           XboxGames/
'Archivos de programa'@     PARCIAL_FINAL/                devlist.txt
 Codigos_P4/                PerfLogs/                     eSupport/
 Desarrollo_Web/           'Program Files'/               femm42/
 Digitales2/               'Program Files (x86)'/         flexlm/
'Documents and Settings'@   ProgramData/                  hiberfil.sys
 DumpStack.log              QueryAllDevice.xml            intelFPGA_lite/
 DumpStack.log.tmp          Recovery/                     mintic_prueba/
 GetDeviceCap.xml           SPB_Data/                     pagefile.sys
 GetDeviceStatus.xml        SetMatrixLEDScript.xml        practica7/
 Intel/                    'System Volume Information'/   swapfile.sys

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c
$ cd Desarrollo_Web

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web
$ ls
my_web_page/

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web
$ cd my_web_page

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ git remote -v
origin  git@github.com:camilocona/my_web_page.git (fetch)
origin  git@github.com:camilocona/my_web_page.git (push)

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ git push origin main
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=camilocona
user.email=camilocona2@gmail.com
core.repositoryformatversion=0
core.filemode=false
core.bare=false

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ssh -vT git@github.com
OpenSSH_9.3p1, OpenSSL 3.1.1 30 May 2023
debug1: Reading configuration data /etc/ssh/ssh_config
debug1: Connecting to github.com [140.82.114.3] port 22.
debug1: Connection established.
debug1: identity file /c/SPB_Data/.ssh/id_rsa type 0
debug1: identity file /c/SPB_Data/.ssh/id_rsa-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_ecdsa type -1
debug1: identity file /c/SPB_Data/.ssh/id_ecdsa-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_ecdsa_sk type -1
debug1: identity file /c/SPB_Data/.ssh/id_ecdsa_sk-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_ed25519 type -1
debug1: identity file /c/SPB_Data/.ssh/id_ed25519-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_ed25519_sk type -1
debug1: identity file /c/SPB_Data/.ssh/id_ed25519_sk-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_xmss type -1
debug1: identity file /c/SPB_Data/.ssh/id_xmss-cert type -1
debug1: identity file /c/SPB_Data/.ssh/id_dsa type -1
debug1: identity file /c/SPB_Data/.ssh/id_dsa-cert type -1
debug1: Local version string SSH-2.0-OpenSSH_9.3
debug1: Remote protocol version 2.0, remote software version babeld-57ca1323
debug1: compat_banner: no match: babeld-57ca1323
debug1: Authenticating to github.com:22 as 'git'
debug1: load_hostkeys: fopen /c/SPB_Data/.ssh/known_hosts2: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts2: No such file or directory
debug1: SSH2_MSG_KEXINIT sent
debug1: SSH2_MSG_KEXINIT received
debug1: kex: algorithm: curve25519-sha256
debug1: kex: host key algorithm: ssh-ed25519
debug1: kex: server->client cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
debug1: kex: client->server cipher: chacha20-poly1305@openssh.com MAC: <implicit> compression: none
debug1: expecting SSH2_MSG_KEX_ECDH_REPLY
debug1: SSH2_MSG_KEX_ECDH_REPLY received
debug1: Server host key: ssh-ed25519 SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
debug1: load_hostkeys: fopen /c/SPB_Data/.ssh/known_hosts2: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts: No such file or directory
debug1: load_hostkeys: fopen /etc/ssh/ssh_known_hosts2: No such file or directory
debug1: Host 'github.com' is known and matches the ED25519 host key.
debug1: Found key in /c/SPB_Data/.ssh/known_hosts:1
debug1: rekey out after 134217728 blocks
debug1: SSH2_MSG_NEWKEYS sent
debug1: expecting SSH2_MSG_NEWKEYS
debug1: SSH2_MSG_NEWKEYS received
debug1: rekey in after 134217728 blocks
debug1: get_agent_identities: bound agent to hostkey
debug1: get_agent_identities: agent returned 1 keys
debug1: Will attempt key: /c/SPB_Data/.ssh/id_rsa RSA SHA256:Znrfte12L9Oo5KOKx0k1foLMreT0osbjO/cnmNAvcKI agent
debug1: Will attempt key: /c/SPB_Data/.ssh/id_ecdsa
debug1: Will attempt key: /c/SPB_Data/.ssh/id_ecdsa_sk
debug1: Will attempt key: /c/SPB_Data/.ssh/id_ed25519
debug1: Will attempt key: /c/SPB_Data/.ssh/id_ed25519_sk
debug1: Will attempt key: /c/SPB_Data/.ssh/id_xmss
debug1: Will attempt key: /c/SPB_Data/.ssh/id_dsa
debug1: SSH2_MSG_EXT_INFO received
debug1: kex_input_ext_info: server-sig-algs=<ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-rsa-cert-v01@openssh.com,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,ssh-ed25519,ecdsa-sha2-nistp521,ecdsa-sha2-nistp384,ecdsa-sha2-nistp256,rsa-sha2-512,rsa-sha2-256,ssh-rsa>
debug1: SSH2_MSG_SERVICE_ACCEPT received
debug1: Authentications that can continue: publickey
debug1: Next authentication method: publickey
debug1: Offering public key: /c/SPB_Data/.ssh/id_rsa RSA SHA256:Znrfte12L9Oo5KOKx0k1foLMreT0osbjO/cnmNAvcKI agent
debug1: Authentications that can continue: publickey
debug1: Trying private key: /c/SPB_Data/.ssh/id_ecdsa
debug1: Trying private key: /c/SPB_Data/.ssh/id_ecdsa_sk
debug1: Trying private key: /c/SPB_Data/.ssh/id_ed25519
debug1: Trying private key: /c/SPB_Data/.ssh/id_ed25519_sk
debug1: Trying private key: /c/SPB_Data/.ssh/id_xmss
debug1: Trying private key: /c/SPB_Data/.ssh/id_dsa
debug1: No more authentication methods to try.
git@github.com: Permission denied (publickey).

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ ssh-add -l -E sha256
4096 SHA256:Znrfte12L9Oo5KOKx0k1foLMreT0osbjO/cnmNAvcKI camilocona2@gmail.com (RSA)

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ cat /c/SPB_Data/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCr7Ilz9Ty3CMG7K6oJQtVV0ybVo2zV3E9WUvvFbROAPG6Xl1bAREyCwz3Bcm2Fm+wzeoGwLRok1u2lp+TjP6Hrxlr93i4EtCCmlGRjP/X3kqYCB8VPnt4XdUObkTu8I58ty7ef6Ymvp1fmm2LRRVY7C9SnRF4//fw5gDcMKOqMnXhGUkrjiJC6UmZFNQAxf0p1eP4jFr/ku+TBGRk7J++31GL+6opsceo/mZG0iqsOzQK8lfATJI1GuwuQgP0M5UQm8M2qm0eKVnzq8SgKUURnbFbfpLU1UgLOTSqrUljJ84k0WLKPHTKcddn+SebDEqDgHScF/JwEbIQP/wDZnE+AmQeP8ug32WKH6qUqXpJ0hsHxaBMWUBPxazLuuzhtG4cusjqNYd4lBercqf6sFBWXfCHSDIhAeOd/uDmfE6cRQFpmdyLtY02NNxcyXY+wJa896vDL9wfw3N8eUNxYqYtdK7oWij7ijuaBPccim2xWxbWXL/et9/qfpdcPq5HNOUuvhde1PV7qFLZTWw0p8qYqyDuLtW6vgmPl8r9dZD2/Ksp912tyMItrYXLZsW1w0dooQ9fpgKQI1xJ+dtRACrjWyD+nXu+mSAfdiDw0p9PjfEF/hZS3s6HAjqQhz1zIRaXkdyq9oYQSS2g1UmpcgCoi9snZePwgbDdvBumyH9NWkw== camilocona2@gmail.com

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 77.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:camilocona/my_web_page.git
 * [new branch]      main -> main

Camilo Anacona@LAPTOP-SD759LKP MINGW64 /c/Desarrollo_Web/my_web_page (main)
$
