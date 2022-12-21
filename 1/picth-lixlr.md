Fala pessoal! Este é o meu primeiro post de muitos (eu espero) por aqui. Antes de mais nada gostaria de agradecer à todos por esta comunidade maravilhosa.

Sério, estou muito feliz por ter chegado até aqui neste projeto. Eu sei, ainda falta muito pra terminar ~~embora softwares nunca fiquem realmente prontos~~, mas já está com um resultado muito legal (na minha humilde opinião).

**Uma imagem vale mais do que mil palavras?**

![Lixlr Cover](https://raw.githubusercontent.com/dhrleandro/tabposts/main/1/lixlr_cover.PNG)


- - -

# Prólogo

Minha motivação incial era estudar um pouco mais do React e do Typescript. Então, eu queria mesmo era ter desenvolvido um game (só Typescript), mas por quê não criar logo um software para editar pixel art?

Embora existam diversos editores por aí, muito melhores do que o meu, não encontrei nenhum feito em React. Então, aderi ao meu próprio desafio.

O primeiro ponto a destacar é que a engine do editor deveria ser o mais separada possível do React, assim ficaria mais facil se no futuro eu quisesse reeescrever a UI em Vue.js, por exemplo. Não é algo tão importante para este projeto, mas eu quiz fazer assim porque eu queria ver se conseguiria e também porque esse projeto pode ser utilizado como base para um editor mais avançado, então fazer a engine (que é o coração do app) misturada com a biblioteca de UI deixaria tudo mais bagunçado do que provavelmente já está :D.

# Um breve resumo da estrutura de pastas

Vou tentar resumir mais ou menos a responsabilidade de cada parte do app através da estrutura de pastas.

- components: *Componentes React*
- context: *Contexto do Theme Switcher*
- core: *Motor principal do app, separado da UI*
  - entities: *Entidades básicas*
  - state: *Estado inicial do aplicativo, enums de Actions, função Redutora*
  - tools: *Comportamento das ferramentas separas em classes*
  - utils: *Função úteis*
- hooks: *Hook que cria o core/App e armazena em uma React.useRef*
- icons: *Ícones em SVG, do Heroicons*
- screens: *Componente React principal, instanciado dentro do componente App*
- state: *Estado da aplicação React, utiliza react-tracked e depende do core/state*
- styles: *Estilos em CSS Modules*

# Features

Atualmente o Lixlr faz poucas coisas, mas pretendo ir adicionando mais features ao poucos. Dependendo de quando você estiver lendo isso as coisas já podem ter mudado, o código de referência deste post vai até o commit [b03c68e6103a4f68105bd11e328db0b532074aef](https://github.com/dhrleandro/lixlr/tree/b03c68e6103a4f68105bd11e328db0b532074aef).

**Implementado:**

- Theme switcher
- Gerenciador de Camadas (fiquei orgulhoso de ter conseguido isso :D)
- Zoom e Pan
  - Gire a roda do mouse para aumentar ou diminuir o zoom
  - Use o gesto de pinça em telas touch aumentar ou diminuir o zoom
  - Pressione a roda do mouse para mover a tela com qualquer ferramenta selecionada
- Seletor de cores (muito simples)
- Ferramentas
  - Lápis
  - Pincel com ajuste de tamanho
  - Borracha com ajuste de tamanho
  - Linha
  - Retângulo
  - Balde de tinta
  - Mão (para mover a tela clicando e arrastando com ou mouse ou touch)


**Falta implementar:**

Muitas coisas, a principal é o botão Desfazer e Refazer. Estou com dor de cabeça só de pensar em implementar, mas estou fazendo, aguardem!

- Desfazer / Refazer
- Salvar a imagem
- Ferramenta Elipse
- Renomear as camadas
- Definir outros tamanhos de imagem
- Permitir controle de pressão em tablets como Wacom

Acho que tem muitas outras coisas, mas estas são as que me lembro agora.

# Fim

Por enquanto é isto! Pretendo fazer outras postagens aqui sobre os desafios que tive durante a implementação de algumas partes do aplicativo, mas no momento estou desenvolvendo o botão Desfazer / Refazer, como um simples botão pode dar tanto trabalho (ironia)?

Caso queira testar o aplicativo em seu estado atual, segue o link abaixo:

[Lixlr - Pixel Art Editor](https://dhrleandro.github.io/lixlr/)

Sim, coloquei minha foto e redes sociais no modal da tela inicial, afinal este aplicativo fará parte do meu portfolio. É apenas marketing pessoal, pessoal :D! Como já dizia o Renato Russo, cresça e apareça ~~embora na música O Reggae, ele dissesse que quando cresceu, não viu nada~~.

Sinta-se avontade para clonar e modificar o código fonte. Ficarei feliz em ver suas criações!

No momento não vou abrir o repositório para contribuição, mas quando a primeira versão sair, vou criar um repositório para tentarmos transformar este app em um projeto maior, como o LibreSprite, quem sabe?

[Repositório no Github](https://github.com/dhrleandro/lixlr)

Obrigado pela atenção pessoal!
