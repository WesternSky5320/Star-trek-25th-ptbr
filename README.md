# Star Trek: 25th Anniversary — Tradução PT-BR (GOG / DOSBox)

Tradução não oficial para português do Brasil do clássico de aventura **Star Trek: 25th Anniversary** (Interplay, 1992), para a versão **GOG.com** que roda no DOSBox.

> **Status: beta.** A tradução foi feita e verificada estruturalmente (arquivos, tamanhos, referências de texto), mas ainda **precisa de testes jogando**. Se encontrar texto cortado, símbolos estranhos ou travamentos, abra uma *issue* informando a tela.

## O que foi traduzido

- Diálogos, descrições de objetos, textos das missões e menus dentro das salas (cerca de 3.300 trechos).
- A **biblioteca do computador** (186 verbetes) e as palavras-chave de busca em português.
- Mensagens do executável: salvar/carregar jogo, relatórios do Scott, falas da ponte.
- **Fonte nova com acentos** (á é í ó ú â ê ô ã õ à ç).
- Opcional: **tempo extra de leitura** — a legenda fica na tela de 2 a 7 segundos depois que a voz termina.

## O que NÃO foi traduzido

- O **áudio falado** continua em inglês (as legendas aparecem em português).
- Textos que fazem parte de imagens.
- Alguns nomes de personagens e de missões, que não cabiam no espaço original.

## Requisitos

- Windows.
- Uma cópia **própria** do jogo na versão **GOG.com** (instalada, por exemplo, em `C:\GOG Games\Star Trek 25th Anniversary`).
- O jogo roda pelo **DOSBox** do GOG. **ScummVM não é suportado** por esta versão da tradução.

Este repositório **não** inclui o jogo. Você precisa ter o jogo original.

## Como instalar

1. Baixe `Instalar_Traducao_ST25_PTBR.exe` na página de [Releases](../../releases).
2. Feche o jogo.
3. Dê dois cliques no instalador. Ele procura sozinho a pasta `TREKCD` do jogo.
   - Se não encontrar, digite ou arraste a pasta `TREKCD` (a que contém o `DATA.001`) para a janela.
4. Escolha uma opção e aperte Enter:

   | Opção | O que faz |
   |------:|-----------|
   | 1 | Tradução com o tempo original das falas |
   | 2 | Tradução + legenda fica **2 s** a mais depois da voz |
   | 3 | Tradução + legenda fica **4 s** a mais depois da voz *(recomendado)* |
   | 4 | Tradução + legenda fica **7 s** a mais depois da voz |
   | 5 | **Restaurar** o jogo original |

5. Abra o jogo pelo atalho normal do GOG.
6. Para o tempo extra funcionar, no jogo vá em **Opções > Exibir texto** e escolha **Legendas**.

O instalador guarda os arquivos originais com a extensão `.ORIG` na primeira execução, e só altera o jogo se os arquivos tiverem o tamanho esperado da versão GOG.

### Instalação manual

1. Faça backup de `DATA.001`, `DATA.DIR`, `DATA.RUN` e `STARTREK.EXE` da pasta `TREKCD`.
2. Copie os mesmos arquivos da tradução por cima.

### Desinstalar

Rode o instalador de novo e escolha a opção **5**, ou restaure os arquivos `.ORIG` renomeando-os para o nome original.

## Pausa

O DOSBox já tem pausa: **Alt+Pause**. O repositório também traz `Pausa_ST25.exe`, um botão de **Pausar / Continuar** com atalho **Ctrl+Alt+P**. Na ponte da nave, a tecla **P** também pausa o jogo.

## Controles resumidos

- **Em terra:** botão esquerdo anda e seleciona; botão direito ou espaço abre o painel de ações (Falar, Olhar, Pegar, Usar, Opções). Atalhos: `T` falar, `L` olhar, `G` pegar, `U` usar, `I` inventário, `W` andar.
- **Na ponte:** botão esquerdo dispara phasers; botão direito ou espaço, torpedos. `S` escudos, `O` órbita, `N` mapa estelar, `D` reparos, `K` opções do Kirk, `Tab` alterna mover/escolher oficial, `1`–`0` velocidade.
- **DOSBox:** `Alt+Enter` alterna tela cheia/janela.

Manual e cartão de referência originais: [manual](https://mocagh.org/miscgame/startrek25thenh-manual.pdf) · [cartão de referência](https://mocagh.org/miscgame/startrek25th-refcard.pdf).

## Problemas conhecidos

- Não testado extensivamente em jogo (veja o status acima).
- Jogos salvos antigos podem não carregar; comece um jogo novo.
- As opções 2 a 4 usam um executável descompactado e modificado. Se o jogo travar, use a opção 1 ou 5.
- O tempo extra vale para qualquer fala com voz, inclusive no modo "Sem texto".

## Como funciona (resumo técnico)

- Os recursos do jogo (`DATA.DIR`/`DATA.RUN`/`DATA.001`) são extraídos, os textos são traduzidos e os arquivos são reempacotados; as strings maiores que o original são realocadas e todas as referências no código das salas são ajustadas.
- A fonte `FONT.FNT` ganhou glifos acentuados, trocando 12 códigos reservados.
- O tempo extra de leitura altera 3 pontos do código do executável (descompactado de EXEPACK).

## Aviso legal

Projeto de fãs, sem fins lucrativos e **sem afiliação** com Paramount, CBS, Interplay ou GOG. *Star Trek* é marca registrada de seus respectivos donos. Este repositório não distribui o jogo; é necessário possuir uma cópia legítima.
