# Adicionar chave SSH ao GitHub



## 1 . Gerar Nova Chave SSH

1.1 Abra o Git Bash;

 1.2 Copie e cole o comando `ssh-keygen -t ed25519 -C "your_email@example.com"`.  *Substituir por seu e-mail cadastrado no GitHub*;

1.3 Logo após retornará o seguinte: 

`>Generating public/private	ed25519 key pair.`

`> Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519)` *Pressione Enter*

`> Enter passphrase (empty for no passphrase)`  <!--ATENÇÃO!!-->   *digitar uma senha qualquer, você não irá  ver o que esta digitando na tela. Essa senha será solicitada quando clonar ou comitar arquivos/repositórios*. 

`> Enter same passphrase again` *Digitar a mesma senha novamente*. 



**Pronto! Uma nova chave SSH foi criada com sucesso!!**

A chave foi salva como um arquivo, tendo seu e-mail fornecido como rótulo e está armazenada em local padrão.





## 2 Adicionar Chave SSH ao Agente SSH 



2.1 Digite o comando `$ ls -al ~/.ssh`  para conferir se existe a chave ssh:

```
`> [...] Sep  7 15:38 ../`
`> [...] Sep  7 17:05 id_ed25519`
`> [...] Sep  7 17:05 id_ed25519.pub`
```

com essa resposta, confirmamos que a chave esta criada;



2.2 Para iniciar o agente SSH digite o comando  

```
$ eval "$(ssh-agent -s)"`

  ` > Agent pid 59566
```

 ;



2.3 Digite o comando `$ ssh-add ~/.ssh/id_ed25519` para adicionar sua chave privada SSH ao agente ssh.



**PRONTO! Sua chave SSH já pode ser adicionada à sua conta no GitHub!!**



## 3 Adicionar chave SSH ao GitHub

3.1 Copie a chave pública SSH para sua área de transferência, seguindo os seguintes passos:

- [ ] **Disco local (C:)** 

- [ ] **Clique em Usuários** <!--selecione seu usuário-->

- [ ] **Clique na pasta `.ssh`** 

- [ ] **abra com um editor de texto o arquivo - *id_ed25519* do tipo *arquivo PUB*** -

- [ ] **Copie todo o texto**  <!--Lembre-se que seu e-mail estará como rótulo na chave e também deve ser copiado--> ;

  

3.2  No GitHub clique na sua **foto de perfil** e em **definições**:

![](C:\Users\Jessica\Desktop\gh1.png)





3.3 Na barra lateral, clique nas **chaves SSH e GPG**:

![](C:\Users\Jessica\Desktop\gh2.png)



3.4 Clique em **Nova chave SSH**:

![](C:\Users\Jessica\Desktop\gh3.png)



3.5 No campo "Título", adicione um rótulo descritivo para a nova chave;



3.6 Cole sua chave no campo "Chave";



3.7 Clique em **Adicionar chave SSH**;



3.8  Se solicitado, confirme sua senha do GitHub.



## Procedimento Realizado com Sucesso!! 





