# chatbot-hajar

Página de teste do assistente virtual da **Hajar Imóveis** (Palmeira/PR). O chat é um widget que conversa com um fluxo do n8n por webhook.

## Arquivos

- `index.html` — tela simplificada para teste com usuários: uma tela só, sem scroll, com o chat já aberto no canto inferior direito de um container de 900px.
- `index-completo.html` — réplica do layout completo do site, com o widget no canto da tela.
- `chatbot.iife.js` — widget de chat já compilado (React + Tailwind). Não temos o código-fonte nesta pasta.
- `hero.jpg` — arte do banner, usada como fundo.

## Como rodar

Sirva a pasta com qualquer servidor estático, por exemplo:

```sh
python -m http.server 8765
```

Depois abra `http://localhost:8765/`. O endereço do webhook fica em `WEBHOOK_URL`, no fim de cada HTML. Para testar com o workflow aberto no editor do n8n, troque `/webhook/` por `/webhook-test/`.

## Observações

- `ChatBot.open()` e `ChatBot.close()` não funcionam neste build do widget. Na `index.html`, o chat é aberto clicando via script no botão flutuante, que fica oculto.
- A posição e o tamanho do painel são ajustados por CSS na própria página, que sobrescreve as classes do widget.
