# Software de Orçamento para Loja de Quadros

Este é um software de desktop desenvolvido em Python para auxiliar no cálculo de orçamentos, cadastro de molduras, visualização de relatórios e edição de preços de materiais para uma loja de quadros.

## Funcionalidades

*   **Orçamento:** Calcula o preço final de um quadro com base nas dimensões (largura, altura) e materiais selecionados (vidro, fundo, passepartout, impressão, chassi, moldura), aplicando uma margem de 10%.
*   **Cadastro:** Permite cadastrar, editar e excluir modelos de molduras e seus respectivos preços por metro linear.
*   **Relatórios:** Exibe um histórico dos orçamentos calculados nos últimos 30 dias e estatísticas de uso das molduras (mais e menos usadas).
*   **Editar:** Permite visualizar e atualizar os preços dos materiais base (vidros, fundos, impressões, etc.) usados nos cálculos.

## Tecnologias Utilizadas

*   **Linguagem:** Python 3.11
*   **Interface Gráfica:** CustomTkinter
*   **Hasheamento de senhas:** Bcrypt
*   **Banco de Dados:** SQLite3

## Estrutura do Projeto

```
loja_quadros_app/
├── calc/
│   └── calculations.py   # Lógica de cálculo de orçamento
├── db/
│   ├── database.py       # Funções de interação com o banco de dados
│   └── loja_quadros.db   # Arquivo do banco de dados SQLite (criado na primeira execução)
├── ui/
│   ├── ui_cadastro.py    # Interface da aba de Cadastro
│   ├── ui_editar.py      # Interface da aba de Edição de Preços
│   ├── ui_orcamento.py   # Interface da aba de Orçamento
│   └── ui_relatorios.py  # Interface da aba de Relatórios
├── main.py               # Interface pós Login
├── login.py              # Ponto de entrada principal da aplicação
├── cadastro.py           # interface da aba de criação de usuarios
└── requirements.txt      # Dependências Python
```

## Como Executar Localmente

**Pré-requisitos:**

*   Python 3.10 ou superior instalado.
*   `pip` (gerenciador de pacotes Python).
*   Um ambiente com suporte a interface gráfica (Windows, macOS, Linux com desktop environment).

**Passos:**

1.  **Descompacte** o arquivo `loja_quadros_app.zip` em um diretório de sua preferência.
2.  **Abra um terminal** ou prompt de comando nesse diretório.
3.  **(Opcional, mas recomendado) Crie um ambiente virtual:**
    ```bash
    python -m venv venvs
    ```
    *   Ative o ambiente virtual:
        *   Windows: `.\venv\Scripts\activate`
        *   macOS/Linux: `source venv/bin/activate`
4.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```
    *Observação:* Pode ser necessário instalar o `tkinter` separadamente dependendo do seu sistema operacional e instalação Python (ex: `sudo apt-get install python3-tk` em sistemas Debian/Ubuntu).
5.  **Execute a aplicação:**
    ```bash
    python main.py
    ```

A janela principal da aplicação deverá abrir.

## Observações

*   O banco de dados (`loja_quadros.db`) será criado automaticamente no diretório `db/` na primeira vez que a aplicação for executada.
*   Os preços iniciais dos materiais no banco de dados são valores padrão e podem ser ajustados na aba "Editar".
*   A aplicação foi desenvolvida e testada quanto à lógica e sintaxe, mas a validação completa da interface gráfica e da experiência do usuário deve ser feita em um ambiente com suporte gráfico.

