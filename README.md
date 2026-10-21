# cahnani's house — arquivos iniciais

Este é um protótipo estático, responsivo e em português para o site pessoal **cahnani's house**.

## Como abrir

1. Baixe e extraia o ZIP.
2. Abra `index.html` no navegador do celular ou computador.
3. A fonte Google Fonts precisa de internet; sem internet, o site usa fontes de reserva.
4. O player tem URLs de demonstração. Edite a lista `TRACKS` no início de `script.js` para trocar títulos, artistas e URLs de áudio.

## Onde personalizar

- `index.html`: textos, seções, cartões, filmes e fotografias.
- `style.css`: cores, fontes, espaçamentos e aparência.
- `script.js`: músicas, mensagens aleatórias e funcionamento do desenho.

As três ilustrações da área de fotografias são formas abstratas feitas em CSS, para que o site não fique vazio antes de você adicionar suas próprias fotos.

## Importante sobre a rádio

O protótipo tenta reproduzir uma faixa instrumental de demonstração hospedada no Wikimedia Commons. A disponibilidade de um URL remoto pode mudar. Para suas músicas, use áudio que você tenha direito de hospedar, arquivos próprios ou players oficiais incorporados de serviços de streaming. Não suba músicas comerciais protegidas por direitos autorais sem autorização. Algumas plataformas não permitem reprodução contínua ou em segundo plano.

Para trocar uma faixa, encontre `TRACKS` no começo de `script.js`. Cada faixa tem `title`, `artist`, `src` e `hint`. `src` precisa ser um URL direto de áudio compatível com o navegador, não a URL normal de uma página de música.

## Importante sobre o mural

O desenho funciona e pode ser feito com mouse ou toque. **No estado atual, os envios ficam somente no armazenamento local do mesmo navegador**, como demonstração. Isso significa que o desenho de outra pessoa não chega até você automaticamente.

Para lançar o mural público de verdade, conecte o site a um backend (por exemplo, Supabase):
1. Crie uma tabela de envios com ID, apelido opcional, legenda, caminho do arquivo, estado (`pending`, `approved`, `rejected`) e data.
2. Faça os visitantes enviarem imagens para armazenamento com limite de tamanho e validação.
3. Configure políticas para visitantes criarem envios pendentes, mas nunca aprovarem ou listarem envios pendentes.
4. Crie uma área administrativa protegida por login para você aprovar ou rejeitar.
5. A galeria pública consulta somente os itens aprovados.
6. Adicione limite de envios, proteção contra spam e uma opção de denúncia/remoção.

Não coloque chaves secretas de administrador no JavaScript público. Se você publicar o protótipo como está, deixe claro que o mural ainda é uma demonstração local.

## Publicação

Você pode hospedar os três arquivos em um serviço de hospedagem estática. Para sincronizar o conteúdo entre aparelhos, ter login administrativo, receber desenhos de visitantes e moderá-los, será necessário integrar um backend e configurar as permissões. O protótipo não usa backend ainda.
