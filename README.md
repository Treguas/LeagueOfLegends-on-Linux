Este artigo vai te ajudar a verificar e instalar o que precisa para rodar League Of Legends no Linux.

## Antes de seguir estes passos instale todas as dependências do Wine
Embora a Lutris forneça e use suas próprias compilações do Wine, ainda recomendamos que você instale todas as dependências do Wine para garantir uma experiência de trabalho. A maneira mais fácil de obtê-los é instalar o Wine em todo o sistema por meio do gerenciador de pacotes.

A versão do Wine instalada não importa, nem mesmo é necessário que o Wine esteja presente, desde que todas as dependências sejam satisfeitas. Embora, o Lutris exibirá uma mensagem de aviso se não puder detectar uma instalação existente do Wine.

# Abaixo está uma lista de comandos específicos para sua distribuição.

## Ubuntu/Linux Mint/Ubuntu derivatives

Enable 32 bit architecture (if you haven't already): 

    sudo dpkg --add-architecture i386 

Download and add the repository key:

    wget -nc https://dl.winehq.org/wine-builds/winehq.key
    sudo apt-key add winehq.key

Add the repository:

|For this version: | Use this command:          
|------------------|--------------------------------
|Ubuntu 20.04      | sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main'
|Ubuntu 19.10      | sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ eoan main'
|Ubuntu 19.04      | sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ disco main'
|Ubuntu 18.10      | sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ cosmic main'
|Ubuntu 18.04<br>Linux Mint 19.x | sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ bionic main'

**Only for Ubuntu 18.04:**
Add SDL2 Backports PPA (for Faudio package):

    sudo add-apt-repository ppa:cybermax-dexter/sdl2-backport

Update packages:

    sudo apt-get update
    
Install Wine

    sudo apt-get install --install-recommends winehq-staging

If you receive this error: `The following packages have unmet dependencies`, execute following command instead:

For compatibility reasons, install these additional libraries:

>sudo apt-get install libgnutls30:i386 libldap-2.4-2:i386 libgpg-error0:i386 libxml2:i386 libasound2-plugins:i386 libsdl2-2.0-0:i386 libfreetype6:i386 libdbus-1-3:i386 libsqlite3-0:i386


These libraries may be used by games, launchers, or applications. E.g. Origin, Battle.net, Uplay etc. It's good practice to install these in addition to Wine.

## Install

> 1. Go to: https://lutris.net/

> 2. Go to Downloads:

Packages compatible with Ubuntu and derivatives are available on the PPA.
You can add a repository using terminal to receive automatic updates:

sudo add-apt-repository ppa:lutris-team/lutris
sudo apt update
sudo apt install lutris

> 3. Go to Games:
Upgrade your system:

    3.1 Search League of legends and Install, prefer use the first Gold works flawlessly with some minor tweaking
    3.2 Now follow next step.
    3.3 the last step uncheck Launch League of Legends now?
    3.4 Create desktop shortcut and Create application menu shortcut
    
> 4. Open Lutris, League of Legends appear and open and update League.(before play reboot system)


IMPORTANT: Uncheck 'Launch League of Legends now?' at the end of the League install wizard.
