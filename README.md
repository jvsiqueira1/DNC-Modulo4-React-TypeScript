# Projeto: To-Do List com TypeScript, React e Context API
Este projeto é uma aplicação de To-Do List desenvolvida com TypeScript e React, com o objetivo de aplicar conceitos avançados de tipagem, gerenciamento de estado e comunicação entre componentes. A aplicação permite adicionar, remover e marcar tarefas como concluídas, além de alternar entre temas claro e escuro (dark mode) utilizando a Context API.

# Tecnologias Utilizadas
React: Biblioteca JavaScript para construção de interfaces de usuário.

TypeScript: Superset do JavaScript que adiciona tipagem estática ao código.

Context API: Ferramenta do React para gerenciamento de estado global e compartilhamento de dados entre componentes.

Vite: Ferramenta de build rápida para desenvolvimento moderno.

CSS: Estilização básica da aplicação, com suporte a temas claro e escuro.

# Funcionalidades
### Gerenciamento de Tarefas
Adicionar Tarefas: O usuário pode adicionar novas tarefas à lista digitando no campo de texto e clicando no botão "Adicionar Tarefa".

Remover Tarefas: Cada tarefa possui um botão "Remover" que permite excluí-la da lista.

Marcar Tarefas como Concluídas: As tarefas podem ser marcadas como concluídas ou não concluídas através de um checkbox. Quando marcadas, o texto da tarefa é riscado.

Contagem de Tarefas: A aplicação exibe o número de tarefas concluídas em relação ao total de tarefas.
### Persistência de Dados
As tarefas são salvas no localStorage do navegador, garantindo que não sejam perdidas ao recarregar a página.
### Dark Mode
A aplicação suporta a alternância entre temas claro e escuro. O tema é gerenciado globalmente utilizando a Context API, e a preferência do usuário é aplicada em todos os componentes da aplicação.

O botão "Alterar para o tema escuro/claro" permite alternar entre os temas.
# Estrutura do Projeto
### App.tsx
Componente principal da aplicação, responsável por renderizar a lista de tarefas e gerenciar o estado das tarefas.

Utiliza hooks como useState e useEffect para gerenciar o estado e persistir as tarefas no localStorage.

Implementa funções para adicionar, remover e marcar tarefas como concluídas.
### ThemeContext.tsx
Contexto criado para gerenciar o tema da aplicação (claro ou escuro).

Utiliza a Context API para compartilhar o estado do tema e a função de alternância entre os componentes.

O hook useTheme é utilizado para acessar o tema e a função de alternância em qualquer componente.
### App.css
Estilização da aplicação, com suporte a temas claro e escuro.

As classes .dark são aplicadas dinamicamente com base no tema selecionado, alterando cores de fundo, texto e botões.
### main.tsx
Ponto de entrada da aplicação, onde o componente App é renderizado.

Utiliza o ThemeProvider para envolver a aplicação e fornecer o contexto do tema.

# Como Executar o Projeto
### Clone o repositório:
```
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```
### Instale as dependências:
```
npm install
```
### Execute o projeto:
```
npm run dev
```
### Acesse a aplicação:
Abra o navegador e acesse http://localhost:5173 (ou a porta indicada no terminal).
# Aprendizados e Desafios
### TypeScript e Tipagem
A utilização do TypeScript trouxe maior segurança ao código, permitindo a definição de tipos para estados, props e funções. Isso facilitou a detecção de erros durante o desenvolvimento e melhorou a legibilidade do código.
### Context API e Gerenciamento de Estado Global
A implementação da Context API para gerenciar o tema da aplicação foi um desafio interessante. Aprendi a criar e utilizar contextos para compartilhar dados entre componentes sem a necessidade de prop drilling.
### Persistência de Dados com localStorage
A persistência das tarefas no localStorage garantiu que os dados não fossem perdidos ao recarregar a página. Isso foi implementado utilizando o hook useEffect para sincronizar o estado com o localStorage.
### Dark Mode
A alternância de temas foi implementada com sucesso, utilizando classes CSS dinâmicas e a Context API para gerenciar o estado do tema. Isso proporcionou uma experiência de usuário mais personalizada.
