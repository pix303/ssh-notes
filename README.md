# ssh-notes

## Basic command to genereate keys pair

Create a keys pair with command
`ssh-keygen -t rsa`

`-t` set type encoding.
At prompt *Enter file* set path file, in case of input only a name current path will be used. Convention folder is `~/.ssh`

## Multiple keys for multiple server/repos

In case of managing multiple servers create a file **~/.ssh/config** to define a map key server
```
Host domain.server.one
    HostName domain.server.one
    IdentityFile ~/.ssh/id_rsa
    User git

Host domain.another.server
    HostName domain.another.server
    IdentityFile ~/.ssh/id_rsa_alternative
    User git
```

## Permission for keys

Permission for private key must be `-rw-r--r--`. 
Permission for config must be `-rw-r--r--`. 
