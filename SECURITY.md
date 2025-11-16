# 🛡️ Política de Segurança do PortfolioHUB

O projeto PortfolioHUB está comprometido com a segurança e a integridade dos dados, tanto do código-fonte quanto dos dados de usuário (via integração com GitHub OAuth).

## 1. Versões Suportadas

Como o PortfolioHUB é um projeto de Bootcamp em fase de implementação, apenas o **branch** principal (`main`) recebe suporte e atualizações de segurança.

| Versão | Status | Observação |
| :--- | :--- | :--- |
| **`main`** (Versão Atual) | ✅ **Suportada** | Recebe correções imediatas de segurança. |
| **Outros `branches`** | ❌ **Não Suportada** | Ramificações de funcionalidade (`feature branches`) não são consideradas estáveis ou seguras para uso em produção. |

## 2. Gestão de Segredos (Secrets Management)

A robustez de segurança é garantida pela estrita política de não armazenar dados sensíveis no repositório.

### Política:

* **Proibido Hard-Coding:** É estritamente proibido armazenar chaves API, **Client Secrets** (do GitHub OAuth), tokens de acesso, credenciais de banco de dados ou quaisquer outras informações confidenciais diretamente nos arquivos de código-fonte.
* **Armazenamento Seguro:** Todas as credenciais de acesso devem ser gerenciadas por meio de **Variáveis de Ambiente** (e.g., arquivo `.env`) e configuradas para serem ignoradas pelo Git (listadas no `.gitignore`).
* **Uso de GitHub Secrets:** Para fluxos de Integração Contínua (CI/CD) via GitHub Actions, as credenciais são armazenadas de forma segura nas configurações de **Secrets** do repositório, garantindo que nunca sejam expostas nos logs ou no código.

## 3. Varredura de Vulnerabilidades e Dependências

O PortfolioHUB utiliza as ferramentas nativas do GitHub para monitorar e mitigar vulnerabilidades em dependências de terceiros.

* **Dependabot:** O GitHub Dependabot está habilitado para escanear dependências e criar alertas de segurança e *Pull Requests* automáticos quando vulnerabilidades (CVEs) são detectadas em bibliotecas de terceiros.
* **Prioridade de Correção:** Todos os alertas de segurança (Code Scanning ou Dependabot) recebem a prioridade máxima para correção imediata, visando manter o projeto sempre na versão mais segura.

## 4. Como Reportar uma Vulnerabilidade

Se você é um colaborador, testador ou revisor de código e encontrar uma falha de segurança no PortfolioHUB:

1.  **Contato Direto:** Por favor, não abra uma *Issue* pública. Entre em contato diretamente com o proprietário do repositório (`Jota0404`) por meio de um canal
