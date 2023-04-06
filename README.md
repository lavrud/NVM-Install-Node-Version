# NVM-Install-Node-Versions

<img height="100em" src="https://raw.githubusercontent.com/nvm-sh/logos/bf1f9618e83e5098024b18c73ada1b0f542db5f8/nvm-logo-tag-white.svg" />

Este tutorial trata-se de como configurar o NVM. O nvm comando é um script bash compatível com POSIX que facilita o gerenciamento de várias versões do Node.js em um único ambiente.

## Baixe o script de instalação:

• Usando curl ou wget, baixe o script de instalação. No URL abaixo:<br>
`curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh -o install_nvm.sh`

Este script clona o repositório nvm em ~/.nvm . Em seguida, ele atualiza seu perfil ( ~/.bash_profile , ~/.zshrc , ~/.profile ou ~/.bashrc ) para originar o nvm.sh que ele contém.<br>

Você pode confirmar se seu perfil está atualizado observando a saída do script de instalação para determinar qual arquivo foi usado. Procure algo como o seguinte nesse arquivo:<br>

``export NVM_DIR="$HOME/.nvm"
  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
  [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion``

## Reinicie seu terminal:

Para obter as alterações em seu perfil, feche e reabra o terminal ou obtenha manualmente seu respectivo ~/.profile.<br>

Exemplo:<br>
`source ~/.bash_profile`

## Verifique se funcionou:

Por fim, você pode verificar se está instalado com o _command_ comando:<br>

`command -v nvm`

Deve retornar _nvm_

## Use o nvm para instalar a versão LTS mais recente do Node.js:

Agora que você instalou o nvm, vamos usá-lo para instalar e usar a versão LTS atual do Node.js.

`nvm install --lts`<br>

``# Output
Installing latest LTS version.
Downloading and installing node v10.16.3...
Downloading https://nodejs.org/dist/v10.16.3/node-v10.16.3-darwin-x64.tar.xz...
######################################################################## 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v10.16.3 (npm v6.9.0)
Creating default alias: default -> lts/* (-> v10.16.3)``

Verifique se funcionou e se a versão está correta: <br>

node --version
`# => v10.16.3`
which node
`# => /home/lavrud/.nvm/versions/node/v18.15.0/bin/node`

## Listar versões disponíveis:

`nvm ls-remote`<br>

## Instalar uma versão específica:

`nvm install 8.16.2`

## Instale a versão mais recente:

`nvm install node`

## Listar versões instaladas:

`nvm ls`

## Alternar para outra versão

Para mudar para outra versão do shell ativo, use _[nvm use]_.

Para uma versão específica, forneça um número de versão:

nvm use 10.16.3
`# => Now using node v10.16.3 (npm v6.9.0)`
