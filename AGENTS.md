# Continuidade de modificações Android

Antes de alterar um APK, leia `reports/LATEST.md`, os relatórios anteriores e o histórico Git remoto atualizado. Preserve mudanças existentes e não sobrescreva trabalho de outros chats. Trabalhe no checkout existente; não crie worktrees sem solicitação.

O usuário solicita reutilizar sua chave `bitlife-sign.p12` para as futuras versões modificadas. Nesta máquina há uma cópia privada em `/workspace/.private-signing/bitlife-sign.p12`, fora deste repositório. A presença em outras máquinas não é garantida. Nunca versionar a chave, a senha, credenciais ou extrações de chave privada. Não imprimir segredos em comandos, logs ou relatórios. Se a chave ou uma forma segura de fornecer a senha estiver indisponível, informar o bloqueio; não gerar outra chave silenciosamente.

Antes de assinar, validar a chave e identificar alias e SHA-256 do certificado público. Comparar com o APK anterior. Para atualização, preservar application ID e usar versionCode adequado. A mesma chave não garante atualização sobre APKs assinados por outra chave. Não afirmar teste em aparelho/emulador sem executá-lo.

Após cada alteração, criar relatório em `reports/` e atualizar `reports/LATEST.md`. Registrar pedido, base utilizada (commit e SHA-256 do APK), alterações e arquivos afetados, ferramentas/versões, pacote, versionCode/versionName, hash do APK final, SHA-256 do certificado público, verificações executadas e resultados, testes não executados, defeitos e próximos passos. Incluir instruções suficientes para reproduzir a alteração; um relatório sozinho não substitui fontes ou patches necessários à reprodução. Não versionar APKs ou conteúdo de terceiros sem necessidade e autorização.

O usuário autoriza enviar os relatórios ao repositório GitHub. Fazer commit e push dos relatórios após cada entrega; conferir o sucesso do push e informar falhas. Consultar o remoto antes de retomar em outro chat e não usar force push.
