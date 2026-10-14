# Formulários do Play Console — Quieto

Respostas para o que o Play Console pergunta antes de publicar. Os nomes das seções seguem o Console em português.

## Antes de tudo: teste fechado obrigatório

Conta pessoal criada depois de novembro de 2023 só libera a publicação pública depois de um **teste fechado com pelo menos 12 testadores, que fiquem com o app instalado por 14 dias seguidos**.

1. Testar e lançar → Testes → Teste fechado → criar faixa.
2. Envie `app-release.aab` (em `app/build/outputs/bundle/release/`).
3. Adicione os e-mails (conta Google) dos 12 testadores e mande o link de convite.
4. Depois dos 14 dias, o Console libera o pedido de acesso à produção.

## Assinatura do app

Na primeira vez que você envia o .aab, aceite a **Assinatura de apps do Google Play**. A sua chave de assinatura vira a *chave de upload*. Guarde uma cópia dela fora do computador: sem ela não dá pra enviar atualizações (dá pra pedir troca ao Google, mas leva dias).

## Segurança dos dados

- O app coleta ou compartilha algum dos tipos de dados do usuário? **Não**.
  - O Quieto não tem permissão de internet. O que ele guarda (ajustes, histórico de uso dos apps, papel de parede) fica só no aparelho. Pela regra do Play, dado processado só no aparelho e que nunca sai dele **não conta como coleta**.
- Os dados são criptografados em trânsito? Não se aplica (nada é transmitido).
- Os usuários podem pedir a exclusão dos dados? Desinstalar o app apaga tudo.

## Classificação do conteúdo

Questionário IARC: categoria **Utilitário / Produtividade / Comunicação / Outro**. Responda **Não** para violência, sexo, linguagem, drogas, apostas, interação entre usuários, compartilhamento de localização e compras digitais. Resultado esperado: Livre.

## Público-alvo

Faixa etária: **18 anos ou mais** (ou 13+). Evite marcar menores de 13, porque isso puxa as exigências do programa Famílias.

## Anúncios

O app contém anúncios? **Não**.

## Acesso ao app

Todas as funcionalidades estão disponíveis sem acesso especial: **sim** (não tem login).

## Declaração de permissões

### Serviço de acessibilidade (obrigatória)

O Play exige uma declaração para apps com AccessibilityService. Em Conteúdo do app → Permissões de acessibilidade:

- **O app é uma ferramenta de acessibilidade?** Não.
- **Uso:** "Bloquear a tela com o gesto de toque duplo na tela inicial do launcher, a pedido do usuário. O serviço só executa a ação global de bloquear a tela: declara o tipo mínimo de evento (typeAnnouncement), tem canRetrieveWindowContent=false, não lê o conteúdo da tela e não coleta dados."
- **Vídeo:** um vídeo curto (YouTube, pode ser não listado) mostrando: Ajustes → Gestos → Bloquear a tela → o guia explicando → ativar em Acessibilidade → voltar e dar toque duplo na tela inicial para bloquear.
- **Divulgação no app:** o guia "Bloquear a tela" explica o que o serviço faz e o que não faz antes de mandar a pessoa às configurações. Isso atende ao requisito de divulgação em destaque.

### Outras permissões do app

| Permissão | Tem formulário? | Para quê |
|---|---|---|
| Acesso a notificações (NotificationListenerService) | Não | Linha de notificações |
| READ_CALENDAR | Não | Próximo compromisso na linha viva |
| REQUEST_DELETE_PACKAGES | Não | "Desinstalar" no toque e segure |
| SET_WALLPAPER | Não | Papel de parede do Quieto também no Android |
| EXPAND_STATUS_BAR | Não | Gesto de abrir as notificações |
| WRITE_SECURE_SETTINGS | Não | Só vale se dada pelo computador (adb). Nenhum usuário da Play recebe ela sozinho |
| USE_BIOMETRIC | Não | Trava dos apps ocultos |

## Política de privacidade

Publique `play/privacidade.html` num endereço público e cole o link em Conteúdo do app → Política de privacidade. Opções grátis:

- **GitHub Pages:** crie um repositório público, suba o arquivo como `index.html` e ative Pages.
- **Google Sites:** crie uma página e cole o texto.
