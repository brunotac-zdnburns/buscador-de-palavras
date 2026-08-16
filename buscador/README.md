# buscador-de-palavras
Buscador de palavras em vários idiomas ou em listas personalizadas, para fins lúdicos. Muito útil para ajuda em jogos como Wordle, Scrabble, Termo, Forca e outros jogos de adivinhação de palavras.


### 📝 Resumo de Alterações (Changelog / Release Notes) de 2026-08-15

#### 🌐 1. Expansão de Idiomas e Listas
 * **Novos idiomas adicionados:** Inclusão de Espanhol (es.txt), Francês (fr.txt), Italiano (it.txt), Alemão (de.txt) e Nederlandês (nl.txt), todos com seus respectivos dicionários integrados (como RAE, Larousse e Google Tradutor).
 * **Remoção de pré-requisitos no topo da lista:** O leitor de arquivos de texto (.txt) não exige/remove mais siglas de idioma na primeira linha nem pressupõe ordens específicas nos arquivos enviados.

#### 🔢 2. Controle de Tamanho e Botões (+ / -)
 * **Controle duplo (+ e -):** Adição de dois botões de ajuste rápido integrados ao campo de número de letras sem afetar o alinhamento visual da página.
 * **Ciclo com estado Vazio:** * Clicar em **+**: Vazio ➔ 3 ➔ 4 ➔ 5 ➔ 6 ➔ 7 ➔ 8 ➔ Vazio...
   * Clicar em **-**: Vazio ➔ 8 ➔ 7 ➔ 6 ➔ 5 ➔ 4 ➔ 3 ➔ Vazio...

#### 🧩 3. Seções Dinâmicas para Busca sem Tamanho Fixo (Tamanho = Vazio)
 * Quando nenhum valor de tamanho é selecionado:
   * **Seção 5:** Alterna dinamicamente para campos de inclusão **"Começar com:"** e **"Terminar com:"**.
   * **Seção 6:** Alterna dinamicamente para campos de exclusão **"NÃO começar com:"** e **"NÃO terminar com:"**.
 * Quando um número (ex: 5) é definido, as seções voltam automaticamente para as caixas de **posições exatas** e **posições proibidas por letra**.

#### ⚡ 4. Tratamento, Ordenação e Limite de Carga
 * **Mensagem de Carga Dinâmica:** A badge de status exibe sempre Lista carregada com {qtde} palavras no painel de resultados a cada nova seleção ou upload de dicionário.
 * **Ordenação Acentuada (localeCompare):** A lista final de palavras é ordenada respeitando as regras gramaticais em português, intercalando acentos na posição correta (ex: *a, á, à, ã, b...*).
 * **Suporte a Limite por Frequência (slice):** Adicionada a constante configurável LIMITE_PALAVRAS (ex: 40000) para carregar apenas as *top N* palavras mais frequentes em listas vindas de ferramentas como *Wordfreq*.

