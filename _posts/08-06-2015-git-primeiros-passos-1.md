---
layout: post
title: "Git primeiros passos. #1"
category: 
- git
- guia
permalink: git-primeiros-passos
meta_description: 'Git primeiros passos #1'
browser_title: 'Git primeiros passos #1'
---

Esse post abordará os primeiros passos usando Git. Explicarei rapidamente alguns fundamentos sobre ferramentas de controle de versão, então como instalar o Git no ubuntu e alguns passos para que você já possa compartilhar seu código com seus amigos.


O Git é uma ferramenta bastante utilizada hoje em dia para o controle de versão, você pode versionar praticamente qualquer tipo de arquivo, com ele e um repositório remoto para auxiliar nesse controle. O controle de versão lhe permite recuperar arquivos removidos, arquivos modificados para versões anteriores, também facilita o trabalho em equipe e o Git especialmente, pois existem outras ferramentas de versionamento, permite que tenha vários fluxos de trabalho, ou seja, equipes trabalhando no mesmo projetos porém em fases diferentes. Vamos ao que mais interessa!!!

### Step 1 - Instalando o Git no Ubuntu e configurando o repositório

Abra o terminal do ubuntu e digite o seguinte comando:

<pre>
<code>sudo apt-get install git</code>
</pre>

Após a instalção se quiser verificar a versão do Git instalada é só digitar:

<pre>
<code>git --version</code>
</pre>

Agora considerando que você já tenha um código fonte ou algum arquivo que queira versionar basta ir até o diretorio onde se encontra o arquivo a ser versionado e iniciar o git.

<pre>
<code>git init</code>
</pre>

Neste momento você já pode modificar seus arquivos e verificar as mudanças com o git.

### Step 2 - Bora comitar nosso código

Vamos abrir o terminal novamente e navegar até o diretório do nosso projeto em seguida vamos verificar o estado dos nossos arquivos.

<pre>
<code>git status</code>
</pre>

Por padrão os arquivos modificados aparecerão em vermelho.

Agora iremos adicionar esses arquivos modificados à area de transição conhecida como stage, é um local onde adicionamos os arquivos antes de comitar, assim só colocamos os arquivos que realmente queremos comitar. O comando a seguir adiciona todos os arquivos a stage.

<pre>
<code>git add --all</code>
</pre>

Nesse momento todos os arquivos modificados estão na stage, se você der o comando 'git status' novamente, irá perceber que a cor ficou verde, isso significa que estão prontos para serem comitados, vamos lá.

<pre>
<code>git commit -m "Primeiro commit"</code>
</pre>

Acabamos de comitar nossas modificações com a mensagem de 'Primeiro commit', ao dar o comando git status agora não verá mais nenhum arquivo.

Mas calma, nesse momento só mandamos os arquivos para o nosso repositório local, só está na nossa máquina.

### Step 3 - Uhull!! vamos compartilhar nosso projeto com o mundo!!

Para subir nosso código fonte precisamos de um repositório remoto, temos dois caras mais conhecidos que são o [Bitbucket](https://bitbucket.org){:target="_blank"} e o [Github](https://github.com){:target="_blank"}. Eu uso mais o Bitbucket pois me permite ter repositórios privados para quando estou iniciando ou testando e o GitHub para compartilhar meus projetos públicos.

Para criar um repositório em qualquer um dos dois é bem intuitivo, basta se cadastrar e seguir as instruções.

Criado o repositório remoto agora precisamos subir nosso projeto. No terminal novamente vá até ao diretório do seu projeto e digite o seguinte comando:

<pre>
<code>git remote add origin (url)</code>
#=> ex.: git remote add origin https://RRN@bitbucket.org/RRN/teste.git
</pre>

A url refere se ao caminho do seu repositório remoto, você pode encontra la clicando em 'Clone' ou na hora em que criar o repositório no Bitbucket ele lhe fornecerá junto com algumas instruções. O remote é feito uma única vez, no inicio do versionamento.

Agora vamos de fato enviar nossas modificações para repositório remoto.

<pre>
<code>git push origin master</code>
</pre>

Após o comando anterior o Git lhe pedirá uma senha, a mesma que cadastrou no repositório remoto, digitado a senha pressione enter. 

Agora você já pode verificar no seu repositório remoto o código fonte versionado. Mágico neh! rsrs.

Bom galera, por hoje é isso, quem quiser ver um pouco mais pode acessar o video no canal do youtube [Git primeiros passos #1](https://youtu.be/9u7ko4eWY0o?list=PLxeD05pg5n4kuzIUdIOmojstvH4HueJz-){:target="_blank"}, espero que tenham gostado ai do pouco que passei hoje e que venham mais!! Deixe seu feedback, dúvidas, críticas é tudo bem vindo. 

Nós estamos na web, somos livres para expor nossos pensamentos!!

Sucesso a todos, forte abraço!!