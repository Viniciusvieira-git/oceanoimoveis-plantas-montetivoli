# Monte Tivoli · GitHub Pages Ready

Esta pasta ja esta no formato ideal para um repositorio comum no GitHub com publicacao via GitHub Pages usando `docs/`.

## O que esta pronto aqui

- `docs/index.html`: pagina principal
- `docs/404.html`: fallback util para navegacao no Pages
- `docs/data/units.json`: valores exatos por unidade
- `docs/assets/`: plantas, ficha tecnica, implantacao solar, galeria e logo otimizados
- `docs/scripts/build_units.py`: script para regenerar a base se chegar tabela nova

## Estrutura recomendada no GitHub

Deixe o repositorio assim:

```text
seu-repo/
  docs/
    index.html
    404.html
    assets/
    data/
    scripts/
```

## Se voce quiser publicar sem mexer em nada

1. Crie um repositorio novo no GitHub ou abra o seu repositorio existente.
2. Envie exatamente o conteudo desta pasta `GITHUB_PAGES_READY` para a raiz do repositorio.
3. No GitHub, abra `Settings > Pages`.
4. Em `Build and deployment`, escolha:
   - `Deploy from a branch`
   - branch `main`
   - folder `/docs`
5. Salve.
6. Aguarde o link do site aparecer na mesma tela.

## Resultado esperado

O site vai abrir em algo como:

```text
https://seu-usuario.github.io/seu-repo/
```

## Antes de publicar

- confirme se o numero do WhatsApp continua certo no `docs/index.html`
- confirme se quer manter o texto `abril/2026`
- teste localmente com `python -m http.server 8000` dentro de `docs/`

## Se chegar nova tabela

1. Troque o caminho do PDF ou passe o PDF como argumento para o script.
2. Rode:

```powershell
python docs/scripts/build_units.py "C:\caminho\da\nova_tabela.pdf"
```

3. Suba de novo o arquivo `docs/data/units.json`
