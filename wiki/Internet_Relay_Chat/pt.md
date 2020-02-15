# O que é IRC?

[IRC](http://en.wikipedia.org/wiki/Internet_Relay_Chat) é um protocolo de comunicação para bate-papo com muitos clientes disponíveis para se conectar.

<center>
</center>
# osu! Chat

osu! usa o protocolo IRC para o [chat do jogo](PT:Chat_Console "wikilink"). Você pode se conectar com um cliente externo e conversar com seus osu!amigos mesmo quando não está jogando. Note que o osu! Bancho usa uma implementação personalizada do protocolo IRC, e não possui todas as funcionalidades conhecidas; Nem todas as ferramentas do seu cliente IRC externo vão funcionar corretamente.

**Observação: [HexChat](http://hexchat.github.io/) é conhecido por ter problemas com o IRC do osu!** ([histórico de bugs do HexChat's no GitHub](http://github.com/hexchat/hexchat/issues/818)), considere usar outro cliente caso isso te incomode.

## Como Se Conectar

Uma vez que você instalou um cliente externo você precisa se conectar usando seu nome de usuário do osu! em

` `[`cho.ppy.sh`](irc://cho.ppy.sh)` OU `[`irc.ppy.sh`](irc://irc.ppy.sh)` (ambos destinam-se para o mesmo host) na porta `<b>`6667`</b>` (a porta padrão do IRC)`

## Autenticando-se no Bancho

Quando você se conecta ao bancho você recebe uma mensagem assim:

`* Welcome to osu!bancho. (Bem vindo ao osu!bancho)`
`* -`
`* - You are required to authenticate before accessing this service. (Faça uma autenticação para acessar esse serviço)`
`* - Please click the following link to complete this process: (Clique no link abaixo para completar esse processo)`

Quando você entrar no endereço informado você verá uma tela com a opção "Authorise IRC connection" (Autorizar conexão IRC). Ao simplesmente clicar nesse botão você estará autenticado e será conectado automaticamente em [\#osu](irc://cho.ppy.sh/osu).

Se você não deseja fazer essa autenticação toda vez que se conecta você pode pode incluir o código de autenticação no seu perfil do IRC ou use quando estiver conectando.

`Para autorizar seu cliente permanentemente, mude a autenticação do servidor para: XXXXXXX`

# Comandos Básicos do IRC

| Descrição                              | Comando                 |
|----------------------------------------|-------------------------|
| Se juntar a um canal (Exemplo \#lobby) | /join \#nomedocanal     |
| Sair de um canal                       | /part                   |
| Ignorar nick                           | /ignore nome do jogador |
| Mudar nickname                         | /nick novo nome         |
| Executar ações                         | /me faz alguma coisa    |

# Desativando mensagens de Join/Part

Toda vez que alguém entra ou sai do canal, uma mensagem assim aparece:

`nomedojogador has joined #algumcanal`
`nomedojogador has quit #algumcanal`

Caso esteja em canais com poucas pessoas isso não é incomodo, mas pessoas entram e saem do \#osu constantemente tornando difícil acompanhar o chat.

## Desativando mensagens de Join/Part nos clientes externos mais populares

| Client                                    | Comandos                                                                                                                                                                                                                                                               |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HexChat](http://hexchat.github.io/)      | a. Clique com o direito do mouse no canal que você quer configurar, abaixa do submenu de configurações, cheque "Hide Join/Part Messages" (Mensagens de Entrada/Saída)  

                                             b. Vá para Configurações » Preferências, abaixo de Conversa » Geral, cheque "Hide join and part Messages" (Mensagens de Entrada/Saída)                                                                                                                                  |
| [ircII](http://www.eterna.com.au/ircii/)  | /ignore                                                                                                                                                                                                                                                                |
| [Irssi](http://www.irssi.org)             | /ignore -channels \#nomedocal \* JOINS PARTS SAIU                                                                                                                                                                                                                      |
| [Weechat](http://www.weechat.org)         | /filter add irc\_smart\_weechat irc.algumnome.\#filtro\_inteligente\_irc dealgumcanal \*  

                                             **Note:** algumnome é o nome que você escolheu quando adicionou o sevidor IRC ao Weechat.                                                                                                                                                                               |
| [KVIrc](http://www.kvirc.net)             | Consulte [this thread](http://www.kvirc.ru/forum/?topic=609.0) nos forums oficiais do KVIrc.                                                                                                                                                                           |
| [mIRC](http://www.mirc.com/)              | Ferramentas » Opções » selecione "IRC". Clique no botão"Events...". Mude "joins", "parts", "quits", e "nicks" para as configurações desejadas: "No Status" ou "Esconder" são boas opções [1](http://i.clintecker.com/disable-irc-msgs.html).                           |
| [Quassel IRC](http://www.quassel-irc.org) | Clique com o direito na janela de conversa, então escolha Esconder Eventos » Join/Part/Quit.                                                                                                                                                                           |
| [XChat](http://www.xchat.org)             | Clique com o direito na aba que quer mudar. No submenu do nome do canal, tem uma caixa de seleção "Show join/part messages", simplesmente desmarque isso. Ou digite/set irc\_conf\_mode 1 [2](http://xchat.org/faq/#q211) para desativar mensagens de todos os canais. |

Se seu cliente externo não está listado aqui então confira sua documentação, a maioria dos clientes externos possuem uma forma de fazer isso.
