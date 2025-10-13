# 📋 Workflow Padrão - Branches

## 🌳 Estrutura de Branches

### Branch Principal
- **`master`** - código estável, pronto para produção

### Branches de Funcionalidades
- **`feature/nome-da-funcionalidade`** - novas funcionalidades
- **`feature/login`**
- **`feature/carrinho-compras`**
- **`feature/pagamento`**

### Branches de Correção
- **`bugfix/nome-do-bug`** - correção de bugs
- **`hotfix/problema-critico`** - correções urgentes

## 🔄 Workflow Recomendado

### 1. Criar nova funcionalidade:
```bash
# Sempre partir da master atualizada
git checkout master
git pull

# Criar branch para a funcionalidade
git checkout -b feature/nova-funcionalidade

# Trabalhar na funcionalidade
git add .
git commit -m "Implementando nova funcionalidade"
```

### 2. Finalizar funcionalidade:
```bash
# Voltar para master
git checkout master
git pull

# Fazer merge da funcionalidade
git merge feature/nova-funcionalidade

# Limpar branch antiga
git branch -d feature/nova-funcionalidade

# Enviar para o repositório
git push
```

## 📝 Convenções de Nomenclatura

- Use **kebab-case** (palavras separadas por hífen)
- Seja **descritivo** mas **conciso**
- Prefixos obrigatórios: `feature/`, `bugfix/`, `hotfix/`

### Exemplos bons:
- `feature/login-usuario`
- `feature/carrinho-compras`
- `bugfix/corrigir-validacao-email`
- `hotfix/problema-pagamento`

### Exemplos ruins:
- `minha-branch`
- `teste123`
- `branch-do-joao`