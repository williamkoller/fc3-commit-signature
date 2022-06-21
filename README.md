### Commands

1 - instalar
  - `sudo apt update && sudp apt install -y gnupg`

2 - verificar se existe alguma chave criada
  - `gpg --list-secret-key --keyid-form LONG`

3 - gerar a chave
  - `gpg --full-generate-key`

4 - verificar a chave publica
  - `gpg --armor --export chave`

5 - adicionar a chave no git
  - `git config --global user.signingkey chave`

6 - adicionar no variavel de ambiente `zshrc`
  - `export GPG_TTY=$(tty)`
  - `source ~/.zshrc`

7 - assinar os commits por padrao
  - `git config --global commit.gpgsign true`
  - assinar as tags `git config --global tag.gpgSign true`

8 - verificar se o commit esta assinado
  - `git log --show-signature -1`