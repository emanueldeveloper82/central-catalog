# Domínio Financeiro - Zetra Bank

Bem-vindo à documentação do **Domínio Financeiro**. Esta página centraliza as diretrizes, arquitetura macro e objetivos de negócio de todas as nossas verticais financeiras.

## 🏛️ Estrutura do Domínio

Este domínio é gerenciado pela **Diretoria Financeira** e engloba os seguintes sistemas críticos:

* **Banking System:** Motores de conta corrente, saldo e rotinas de relatórios batch.
* **Pix Ecosystem:** Liquidação instantânea e comunicação com o BACEN.
* **Card Services:** Motores de crédito, autorização de transações e prevenção a fraudes.

## 🔒 Diretrizes e Compliance

Todas as APIs e serviços contidos neste domínio devem seguir rigidamente as normas do Banco Central do Brasil (BACEN) e os padrões internos de segurança:

1.  **Criptografia:** Transações em trânsito devem utilizar TLS 1.3.
2.  **Idempotência:** APIs de escrita (como transferências e saques) devem exigir `X-Idempotency-Key`.
3.  **Logs:** Dados sensíveis de cartões (PAN) ou senhas nunca devem ser logados em texto limpo.