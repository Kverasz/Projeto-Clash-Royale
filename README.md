# Sistema de Cartas – Clash Royale

Este é um sistema criado em **Python + PyQt5** para gerenciar cartas personalizadas no estilo Clash Royale.  
O sistema permite **criar cartas**, **exibir cartas**, **selecionar cartas predefinidas**, **listar cartas criadas** e **remover cartas do banco**.

---

## Funcionalidades Principais

### **1. Criar cartas personalizadas**
- Permite escolher uma imagem do computador.
- Insere o nome da carta.
- Salva tudo automaticamente no banco SQLite.

### **2. Visualizar cartas criadas**
- Exibe até 6 cartas criadas.
- Cada carta pode ser clicada para substituír a carta atual da tela principal.

### **3. Cartas predefinidas**
Inclui cartas fixas:
- Mago  
- Pekka  
- Executor  
- Fornalha  
- Porcos Reais  
- Príncipe  

### **4. Remover cartas**
- Tela dedicada para excluir uma carta criada.
- Remove do banco de dados e atualiza todas as telas automaticamente.

### **5. Exibir carta atual**
A carta escolhida (criada ou predefinida) aparece na tela principal, sempre **redimensionada corretamente**.

---

## Estrutura do Banco de Dados

Banco utilizado: **SQLite – cartas.db**

### Tabela: `cartas`

| Campo   | Tipo     | Descrição                       |
|---------|----------|---------------------------------|
| id      | INTEGER  | Chave primária (autoincrement)  |
| nome    | TEXT     | Nome da carta                   |
| imagem  | TEXT     | Caminho da imagem no computador |

---

## Imagens no Sistema

Todas as imagens são redimensionadas para:
230 x 275px

Com opções ativadas:

- `Qt.KeepAspectRatio` → evita distorção  
- `Qt.SmoothTransformation` → mantém alta qualidade  

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
|------------|-----|
| **Python 3** | Linguagem principal |
| **PyQt5** | Interface gráfica |
| **SQLite3** | Armazenamento de dados |
| **QPixmap** | Manipulação de imagens |
| **Qt Widgets** | Construção das telas |

---

## Telas do Sistema

### 1️⃣ Primeira Tela — *Tela Principal*
- Exibe a carta atual.
- Botões:
  - Criar Carta
  - Cartas Criadas
  - Mudar Carta
  - Remover Carta

### 2️⃣ Segunda Tela — *Criar Carta*
- Campo para escrever nome.
- Botão para escolher imagem.
- Salva diretamente no banco.

### 3️⃣ Terceira Tela — *Cartas Criadas*
- Mostra até 6 cartas criadas.
- Ao clicar em uma carta, ela aparece na tela principal.

### 4️⃣ Quarta Tela — *Cartas Predefinidas*
- Lista de cartas padrão (Mago, Pekka, etc).
- Substitui a carta atual.

### 5️⃣ Quinta Tela — *Remover Cartas*
- Lista todas as cartas criadas.
- Ao clicar em uma e pressionar “Apagar”, remove do banco.

---

## Requisitos para Rodar o Projeto

### Instalar dependências:
```bash
pip install PyQt5

```
## Confirmar instalação do SQLite (já vem no Python)

```bash
python -c "import sqlite3"
```

---

## Rodar o sistema

```bash
python main.py
```

---

## Membros da Equipe

- Kennedy Veras  

---

## Estrutura do Código

```
ProjetoClashRoyale.py
├── PrimeiraTela
├── SegundaTela
├── TerceiraTela
├── QuartaTela
└── QuintaTela
```

Cada tela é uma classe separada.  
Funções organizadas para:

- criar o banco SQLite  
- listar cartas  
- atualizar imagens  
- manipular dados do sistema  

---

## Conclusão

Este sistema oferece uma interface intuitiva e completa para gerenciamento de cartas personalizadas, incluindo criação, visualização, seleção e exclusão — tudo com imagens redimensionadas corretamente e banco de dados integrado.
