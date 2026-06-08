# English Study Lab

Site estático para estudo de inglês com:

- 13 textos em estilo natural de conversa.
- 104 linhas com áudio.
- Explicação detalhada linha a linha em português.
- 130 pontos de gramática úteis para conversação.
- Exportação pronta para Anki em TSV.
- Áudios MP3 gerados para cada linha dos textos.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie todos os arquivos deste projeto.
3. Vá em **Settings > Pages**.
4. Escolha **Deploy from a branch**, branch `main`, pasta `/root`.
5. Salve e abra o link gerado.

## Rodar localmente

```bash
python -m http.server 8000
```

Acesse:

```text
http://localhost:8000
```

## Anki

Arquivos:

- `anki/english_lines.tsv`
- `anki/grammar_130.tsv`

Para áudio no Anki, mantenha os MP3 `line-001.mp3` etc. na mesma pasta do TSV durante a importação. O campo de áudio já está assim:

```text
[sound:line-001.mp3]
```

## Scripts

Regenerar TSV:

```bash
python scripts/make_anki.py
```

Regenerar áudio:

```bash
sudo apt install espeak ffmpeg
python scripts/generate_audio.py
```

## Estrutura

```text
index.html
src/app.js
src/styles.css
data/texts.json
data/grammar.json
assets/audio/line-001.mp3 ...
anki/english_lines.tsv
anki/grammar_130.tsv
anki/line-001.mp3 ...
scripts/make_anki.py
scripts/generate_audio.py
```

Observação: os textos são originais e escritos em estilo natural de inglês conversacional. A lista das 130 gramáticas é uma curadoria prática para conversas.
