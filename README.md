# Asgard Field — Start & Cronômetro

*De jogador, para jogador.*

Ferramenta do árbitro para dar o start e cronometrar a rodada, feita para o **Asgard Field** (campo de speedsoft, Rua Conselheiro Brotero, 521 – Barra Funda/SP).

## O que faz

- **Start:** fala "10 seconds", 9 beeps com 1 segundo de intervalo e o sinal final. O áudio é a gravação real do campo (`start.mp3`), e o número na tela acompanha o som.
- **Tempo de partida:** o árbitro escolhe **Só o start**, **3**, **5** ou **10 minutos** antes de iniciar. O cronômetro começa junto com o sinal final.
- **Último minuto:** aviso sonoro e a fala "One minute".
- **Fim do tempo:** buzina e a mensagem "Tempo esgotado".
- **Cancelar** a qualquer momento (start queimado, por exemplo) e **Nova rodada** ao final.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site inteiro (visual e lógica) |
| `start.mp3` | Áudio do start; precisa ficar na mesma pasta do `index.html` |
| `README.md` | Este guia |

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub.
2. Em **Add file → Upload files**, envie `index.html`, `start.mp3` e `README.md` na raiz e confirme com **Commit changes**.
3. Vá em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
4. Em alguns minutos o site fica em `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Dicas de uso

- No iPhone, deixe o **modo silencioso desligado** (o aviso de 1 minuto e a buzina final usam o áudio do navegador, que o modo silencioso corta).
- Toque em **Iniciar** para o som liberar; navegadores só tocam áudio depois de um toque.
- Em campo, teste o volume antes da primeira partida.

## Trocar o áudio do start

Substitua `start.mp3` por outro arquivo e ajuste, no início do `<script>` do `index.html`, a constante `CUES`:

- `beeps`: o segundo em que cada beep começa (na ordem 9 → 1);
- `horn`: o segundo em que começa o sinal final.
