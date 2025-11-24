# 1. Copia de .env.example
Copiar .env.example para .env (na raiz)

# 2. Limpar cache e builds antigos e Reinstalar dependências (se necessário)
pnpm clean && pnpm install (na raiz)

# 3. Subir o ambiente completo de desenvolvimento
pnpm go  (na raiz)

# 4. Merge PR para main
Subir sempre as alterações para DEV fazer Merge PR para main, isso vai acionar um workflow no github actions que fará o build da imagem docker publicará para ghcr do sync-adm onde o coolify já tem permissão para acessar através do PAT de sync-adm já configurado. Em caso de dúvidas, verificar: https://docs.sync.com.br/workspace/f4504f7f-4e25-41a0-8218-3fdbc743178d/2griBWcau6RaZf_CS06w3

# 5. Acessar Coolify e fazer redeploy
Quando a imagem docker estiver pronta, acessar o coolify > projetos > Sync Forms > Redeploy. Isso pegará a images mais recentes desde que a tag :latest esteja sendo marcada

# Obervações Gerais
Essa versão é a 4.1.1 do formbricks. Foi clonada da branch main deles. Não vamos atualizar ela, pois a aplicação já está bem madura e vai nos atender.

Todas as features enterprise habilitadas:
✅ Multi-organização (isMultiOrgEnabled)
✅ Projetos ilimitados (projects: null)
✅ Autenticação de dois fatores (twoFactorAuth)
✅ SSO e SAML (sso, saml)
✅ White label e remoção de branding (whitelabel, removeBranding)
✅ Contatos (contacts)
✅ IA (ai)
✅ Proteção anti-spam (spamProtection)
✅ Logs de auditoria (auditLogs)
✅ Pesquisas multi-idioma (multiLanguageSurveys)
✅ Controle de acesso (accessControl)
✅ Quotas (quotas)
