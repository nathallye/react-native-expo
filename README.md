# Ignite - I'm Here

## React Native

Framework open source, Cross Platform(multiplataforma). Todo código desenvolvido é convertido para a linguagem nativa do sistema operacional. Conseguimos desenvolver aplicações para Android e iOS utilizando um código único.

> [Documentação](https://reactnative.dev).

## Expo & CLI

### Expo

O Expo é uma ferramenta bem abrangente que permite a criação de apps universais em React Native. E não apenas isso, ele tem um ecossistema bem interessante para a manutenção do seu app.

O objetivo é facilitar a configuração do seu app e também o acesso e instalação de vários frameworks que permitem o acesso a APIs nativas mais comuns.

Facilita (e muito) rodar seu projeto em dispositivos físicos. No seu ecossistema, o Expo, oferece um app para Android e para iOS que possibilita você rodar seu código no dispositivo. Isso mesmo, não precisa provisionar seu iPhone, só configurar certinho o app do Expo e rodar, mesmo de um sistema Linux ou Windows.

#### Managed workflow x Bare workflow

![Captura de tela 2023-08-21 232131](https://github.com/nathallye/ignite-im-here/assets/86172286/93be5d5a-1867-495b-a54f-628fb058200b)

### CLI

Também chamado de Bare Workflow. É a forma nativa padrão de se criar um projeto em React Native. Ele também oferece alguns templates de projeto como Blank, TabBar ou outro customizado que queira utilizar.

O resultado da criação do projeto utilizando esta forma é bem enxuta. Tem o básico para funcionar e rodar.

O React Native pode ser atualizado a qualquer momento, inclusive versões alfa ou beta. Você pode tanto fazer um upgrade quanto um downgrade do core do React Native sem ter que esperar uma série de validações como no caso do Expo.

## Preparando o ambiente React Native - Linux

**Dependências**

Para configurar o ambiente Android e iOS no Linux (Ubuntu) utilizando `Expo Managed Workflow` (Expo GO), precisamos de 6 ferramentas principais:

- cURL
- Node.js (LTS);
- npm (já vem instalado com o Node);
- git
- expo-cli local
- Expo GO (app a ser instalado no dispositivo Android e/ou iOS)

### Instalando cURL

> O cURL pode já vir instalado. Para verificar, basta executar `curl --version` no terminal.

Para instalar no sistema, basta executar no terminal o comando abaixo:

```
sudo apt-get install curl
```

Para verificar se a instalação foi um sucesso, basta executar o comando abaixo:

```
curl --version
```

Se foi apresentado o valor da versão, a instalação foi um sucesso.

### Instalando Node.js (LTS) e npm

Em seguida é preciso instalar o **Node.js (LTS)** e **npm** no nosso sistema.

Para instalar, podemos utilizar um gerenciador de pacotes como o `n` ou instalar utilizando o NodeSource. Nesse guia iremos utilizar o `NodeSource`, então basta acessar abrir o terminal e executar os comandos abaixo:

```
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs
```

> Se já tiver o Node.js instalado em sua máquina, certifique-se que sua versão é a 14 ou mais recente.

Para verificar se a instalação foi um sucesso, basta executar os comandos abaixo:

```
node -v
npm -v
```

### Git

> O git pode já vir instalado. Para verificar, basta executar `git --version` no seu terminal.

Para instalar no sistema, basta executar no seu terminal o comando abaixo:

```
sudo apt-get install git
```

Para verificar se a instalação foi um sucesso, basta executar o comando abaixo:

```
git --version
```

Se foi apresentado o valor da versão, a instalação foi um sucesso.

### expo-cli

Não é mais recomendado instalar no sistema a Expo CLI global, devemos utilizar a Expo CLI local.

Para executar os comandos com a Expo CLI local, basta adicionar o `npx` na frente, exemplos:

```
npx expo --version
npx expo -h
```

> Não se utiliza a Expo CLI local para criação de projetos. Para iniciar um novo projeto, vamos utilizar o comando `npx create-expo-app --template`.

### Expo GO

Para executar o app no celular (ou emulador) é necessário instalar o aplicativo Expo GO. Ele é o responsável por pegar o código que o metro bundler envia e exibir em tela o seu app React Native.

Para instalá-lo no dispositivo físico, basta buscar nas lojas o aplicativo Expo Go:

- Play Store
- Apple Store

Para instalá-lo no emulador, basta executar o comando `npx expo start` e escolher qual emulador deseja executar. Caso o Expo GO não esteja instalado, ele irá solicitar a autourização para instalar a versão necessária.

### Emulador

#### Android

Com o **Android Studio**, é possível configurar um emulador Android e executar a aplicação nele.

Porém, esses emuladores consomem bastante recursos do computador. Por isso, se possuir um dispositivo físico Android e a máquina utilizada possuir configurações modestas (ex.: ⬇ i3, ⬇ 4gb RAM), é recomendado executar a aplicação no dispositivo físico pelo Expo GO.

#### iOS

> Disponível apenas para máquinas macOS. Windows e Linux não suportam iOS simulator.

### Executando aplicação

Agora que possuimos tudo que é necessário para executar uma aplicação Expo, basta seguirmos os seguintes passos:

- Acessar a pasta do projeto pelo terminal;
- Executar o comando `npx expo start`;
- Abrir o app no dispositivo via Expo GO;
- Se for dispositivo físico Android, basta abrir o app Expo GO, selecionar a opção S`can QR code` e ler o QR Code apresentado no terminal;
- Se for dispositivo físico iOS, basta abrir o app de camera do iOS, ler o QR Code apresentado no terminal e clicar no popup `Open with Expo Go app`;
- Se for emulador Android, basta digitar `a` no terminal.

Seguindo esses passo o app deve abrir com sucesso no dispositivo! 🎉

### Estrutura de pastas

- **assets**
- **node_modules**
- **.gitignore**
- **app.json**: informações da aplicacação;
- **App.tsx**: arquivo da aplicação;
- **babel.config.js** : arquivo de configuração do babel, já vem configurado, faz compilação para as versões mais antigas do JS;
- **package.json**
- **tsconfig.json**

