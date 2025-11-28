# Portfólio de Fernando - Guia de Configuração Local

Este guia descreve como configurar e executar o projeto em sua máquina local, com um foco especial para ambientes onde você não possui permissão de administrador.

## 1. Pré-requisitos

- **Node.js**: O projeto requer Node.js (versão 20.x ou superior). Se você não puder instalá-lo normalmente, siga o **Método Portátil** abaixo.
- **VS Code**: Recomendado para editar o código e usar o terminal integrado.

---

## 2. Configuração (Método Portátil - Sem permissão de Admin)

Este método permite que você rode o Node.js sem precisar instalá-lo no sistema.

### Passo 2.1: Baixar o Node.js Portátil

1.  Acesse a página de downloads do Node.js: [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
2.  Na seção de versões, procure pela **LTS (Long Term Support)**.
3.  Baixe o arquivo binário para Windows no formato **`.zip`** (ex: `node-v20.xx.x-win-x64.zip`).

### Passo 2.2: Extrair os Arquivos

1.  Extraia o conteúdo do arquivo `.zip` para uma pasta de fácil acesso onde você tenha permissão, por exemplo, em `Meus Documentos`.
    - _Exemplo de caminho final:_ `C:\Users\SeuUsuario\Documents\nodejs`

### Passo 2.3: Configurar o Terminal no VS Code

Toda vez que você abrir um novo terminal para trabalhar no projeto, precisará dizer a ele onde encontrar o Node.js.

1.  Abra o projeto no VS Code.
2.  Abra um novo terminal (`View` > `Terminal` ou `Ctrl+'`).
3.  Execute o comando abaixo no terminal do VS Code para configurar o `PATH` apenas para a sessão atual. **Substitua o caminho pelo local onde você extraiu o Node.js**.

    ```powershell
    # Exemplo de comando para o terminal PowerShell (padrão no VS Code)
    $env:Path += ";C:\Users\SeuUsuario\Documents\nodejs"
    ```

4.  **Verifique se funcionou**. Se os comandos abaixo mostrarem as versões, você está pronto!
    ```powershell
    node -v
    npm -v
    ```

---

## 3. Instalando as Dependências do Projeto

Com o Node.js configurado no terminal, navegue até a pasta do projeto e instale as dependências.

1.  **Instale os pacotes:**
    ```bash
    npm install
    ```
2.  **Se encontrar um erro `ERESOLVE`**: Este erro de conflito de dependências é comum. Resolva-o usando o comando abaixo, que instrui o NPM a usar uma lógica de resolução mais antiga e geralmente resolve o problema sem efeitos colaterais.
    ```bash
    npm install --legacy-peer-deps
    ```

---

## 4. Executando o Projeto

Após a instalação das dependências, inicie o servidor de desenvolvimento.

antes de qualquer coisa use isso.

##

1. $env:Path += ";C:\Users\Escola\Documents\nodejs"

1. Execute o comando:
   ```bash
   npm run dev
   ```
1. Abra seu navegador e acesse a URL indicada no terminal, geralmente [http://localhost:9002](http://localhost:9002).

O site estará rodando localmente, e qualquer alteração no código será refletida automaticamente no navegador.
