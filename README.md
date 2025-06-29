# Projeto: Gerenciador de Tarefas v2.0

## 1. Visão Geral

Este é um projeto de um Gerenciador de Tarefas via terminal, desenvolvido em Python. A base do projeto oferece funcionalidades para adicionar, listar, concluir e remover tarefas. O objetivo deste trabalho é estender a funcionalidade do sistema e demonstrar um fluxo de trabalho de desenvolvimento profissional utilizando Git e GitHub.

## 2. Configuração Inicial

1.  **Fork:** Realize um fork deste repositório para a sua conta pessoal no GitHub.
2.  **Clone:** Clone o repositório que você criou (o seu fork) para o seu ambiente de desenvolvimento local.
    ```bash
    git clone [https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git](https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git)
    ```

## 3. Especificações da Tarefa

Você deve implementar as **duas** novas funcionalidades descritas abaixo.

### Funcionalidade 1: Prioridade de Tarefas

* **Estrutura de Dados:** A estrutura de dados de cada tarefa deve ser alterada para incluir um campo `prioridade`.
* **Adicionar Tarefa:** A função de adição deve ser modificada para solicitar ao usuário um nível de prioridade (`Alta`, `Média`, `Baixa`). Uma entrada inválida deve resultar na prioridade padrão `Baixa`.
* **Listar Tarefas:** A função de listagem deve ser atualizada para exibir a prioridade de cada tarefa.

### Funcionalidade 2: Edição de Descrição da Tarefa

* **Menu:** Uma nova opção para "Editar Tarefa" deve ser adicionada ao menu principal.
* **Implementação:** Deve ser criada uma função que permita ao usuário:
    1.  Selecionar uma tarefa existente pelo seu índice.
    2.  Visualizar a descrição atual.
    3.  Inserir uma nova descrição para substituí-la.
* **Feedback:** O sistema deve informar ao usuário se a operação foi bem-sucedida.

## 4. Requisitos de Entrega e Fluxo de Trabalho

A avaliação levará em conta a organização do seu repositório e o uso correto das ferramentas.

* **README.md:** Este arquivo deve ser atualizado com a seção "Minhas Contribuições" devidamente preenchida.
* **`.gitignore`:** O repositório precisa conter um arquivo `.gitignore` configurado adequadamente para projetos Python, ignorando arquivos e pastas como `__pycache__` e `venv/`.
* **Fluxo com Branches:** Cada uma das duas funcionalidades deve ser desenvolvida em uma *feature branch* separada (ex: `feature/task-priority` e `feature/edit-task-description`). Após a finalização, cada branch deve ser mesclada (`merge`) de volta à branch `main`.
* **Histórico de Commits:** É exigido um histórico com um mínimo de **8 a 10 commits atômicos**. As mensagens de commit devem ser claras e refletir o trabalho realizado em cada etapa.

## 5. Critérios de Avaliação

* **README:** Clareza e detalhamento da seção "Minhas Contribuições".
* **Git:** Qualidade das mensagens de commit e demonstração do fluxo de trabalho com branches e merges.
* **Funcionalidade:** Implementação correta e funcional das modificações solicitadas.
* **Código:** Legibilidade, organização e qualidade geral do código implementado.

---

## (Template para o Aluno)

## Minhas Contribuições

* **Nome:**  Bruna Warnk da Rosa Anderson
* **GitHub:** https://github.com/swyangel

### Modificação 1: Prioridade de Tarefas

**Lógica Implementada:**
A lógica central desta modificação foi **aprimorar a estrutura de cada tarefa para incluir um campo de `prioridade`**. Ao adicionar uma nova tarefa, o programa agora **solicita ao usuário que defina essa prioridade (Alta, Média ou Baixa)**. Uma validação é aplicada: se a entrada for inválida, a prioridade é automaticamente definida como `"Baixa"`, garantindo que toda tarefa tenha uma prioridade válida. Por fim, a função de visualização de tarefas foi atualizada para **exibir essa prioridade** junto com a descrição e o status, fornecendo ao usuário uma visão mais completa e organizada de suas tarefas.

**Como Testar:**
1.  Execute o programa no seu terminal (ex: `python seu_arquivo_do_projeto.py`).
2.  No menu principal, selecione a opção **`1. Adicionar Tarefa`**.
3.  Quando solicitado, digite a descrição da tarefa (ex: "Fazer trabalho de Python").
4.  Em seguida, o programa pedirá a prioridade. Digite uma das opções válidas: **`Alta`**, **`Media`**, **`Baixa`**.
5.  Repita o Passo 2 e 3, mas desta vez, ao pedir a prioridade, digite uma palavra **inválida** (ex: "Urgente", "Muito Alta"). Observe se o programa informa que a prioridade é inválida e a define como "Baixa" por padrão.
6.  Após adicionar as tarefas de teste, selecione a opção **`2. Listar Tarefas`**.
7.  **Verifique** se a prioridade (Alta, Média, Baixa ou Baixa por padrão) aparece corretamente ao lado de cada tarefa na lista.

### Modificação 2: Editar Descrição da Tarefa

**Lógica Implementada:**
Esta modificação focou em **permitir que o usuário altere descrições de tarefas já criadas**. Para isso, **uma nova opção foi adicionada ao menu principal**. Ao ser selecionada, uma nova função é ativada: ela **solicita o número (ID) da tarefa** que o usuário deseja editar, valida se o ID é existente e numérico, e então **exibe a descrição atual antes de pedir a nova**. A tarefa correspondente na lista é atualizada com a nova descrição, e mensagens de feedback são fornecidas para confirmar a edição ou informar sobre erros, como IDs inválidos ou descrições vazias.

**Como Testar:**
1.  Execute o programa no seu terminal (ex: `python seu_arquivo_do_projeto.py`).
2.  Adicione algumas tarefas utilizando a opção **`1. Adicionar Tarefa`**. Crie pelo menos duas para ter opções para editar.
3.  No menu principal, selecione a nova opção **`5. Editar Descrição da Tarefa`**.
4.  O programa listará as tarefas. Digite o **número (ID)** de uma tarefa existente que você deseja alterar (ex: `1`).
5.  Quando solicitado, forneça a **nova descrição** para a tarefa (ex: "Ir ao mercado comprar leite desnatado").
6.  Selecione a opção **`2. Listar Tarefas`** para confirmar que a descrição da tarefa foi atualizada com sucesso.
7.  **Teste entradas inválidas:**
    * Selecione a opção **`5. Editar Descrição da Tarefa` novamente**.
    * Tente digitar um **número de tarefa que não existe** (ex: um número muito alto como `99`). Verifique se a mensagem de erro apropriada é exibida.
    * Tente digitar **texto ao invés de um número** para o ID da tarefa (ex: "abc"). Verifique se a mensagem de erro para entrada inválida é exibida.
    * Tente editar uma tarefa, mas digite uma **descrição vazia** ao pedir a nova descrição. Verifique se a tarefa não é alterada e uma mensagem de feedback aparece.