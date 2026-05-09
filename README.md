# Visualizador de Perfil do GitHub

Um projeto simples em JavaScript que busca e mostra informações de um usuário do GitHub, incluindo perfil e repositórios.

## Funcionalidades

- Busca de usuário por nome de usuário do GitHub
- Renderiza dados do perfil:
  - nome
  - bio
  - avatar
  - seguidores
  - seguindo
- Mostra até 10 repositórios do usuário
- Exibe em cada repositório:
  - nome
  - stars
  - forks
  - watchers
  - linguagem principal
- Suporte à busca via clique no botão e ao pressionar `Enter`

## Como usar

1. Abra `index.html` em um servidor local.
2. Digite o nome de usuário do GitHub no campo de pesquisa.
3. Clique em `Buscar` ou pressione `Enter`.

## Endpoints da API do GitHub usados

- Perfil: `GET https://api.github.com/users/:username`
- Repositórios: `GET https://api.github.com/users/:username/repos?per_page=10&sort=created`

## Estrutura do projeto

- `index.html` — marcação da página
- `src/css/` — estilos do projeto
- `src/js/githubApi.js` — funções para chamar a API do GitHub
- `src/js/profileView.js` — renderização dos dados na tela
- `src/js/index.js` — lógica de interação e busca

## Rodar localmente

Para evitar problemas de CORS, abra o projeto em um servidor local.

Exemplos:

- `npx http-server` (se você tiver Node.js)
- `python -m http.server` (se tiver Python instalado)

## Observações

- Repositórios são ordenados por data de criação.
- Se o usuário não existir ou ocorrer erro na requisição, uma mensagem de alerta será exibida.
