# Curso Completo de Git para Trabalhar em Empresas

Este curso abrange os comandos e conceitos essenciais para usar o Git de forma eficiente no ambiente corporativo. Está dividido em seções que simulam situações reais que você encontrará no dia a dia.

---

## **Capítulo 1: Configuração Inicial do Git**

Antes de usar o Git, configure suas informações pessoais e ferramentas:

### **1.1 Configurar nome e e-mail**
```bash
# Configurar o nome do usuário
git config --global user.name "Seu Nome"

# Configurar o e-mail do usuário
git config --global user.email "seu.email@empresa.com"
```

### **1.2 Configurar o editor padrão**
```bash
# Configurar o VS Code como editor padrão
git config --global core.editor "code --wait"
```

### **1.3 Verificar configurações**
```bash
# Listar as configurações atuais do Git
git config --list
```

---

## **Capítulo 2: Criando e Clonando Repositórios**

### **2.1 Criando um novo repositório**
```bash
# Criar uma pasta para o projeto e inicializar o Git
mkdir meu-projeto
cd meu-projeto
git init
```

### **2.2 Clonando um repositório existente**
```bash
# Clonar um repositório remoto
git clone https://github.com/empresa/meu-projeto.git
```

---

## **Capítulo 3: Gerenciando Arquivos no Repositório**

### **3.1 Adicionando arquivos para rastreamento**
```bash
# Adicionar arquivos específicos à área de preparação
git add arquivo.txt

# Adicionar todos os arquivos modificados
git add .
```

### **3.2 Criando commits**
```bash
# Criar um commit com uma mensagem descritiva
git commit -m "Implementa funcionalidade X"
```

### **3.3 Removendo arquivos do repositório**
```bash
# Remover um arquivo do repositório e da pasta
git rm arquivo.txt

# Remover um arquivo apenas do repositório
git rm --cached arquivo.txt
```

---

## **Capítulo 4: Trabalhando com Branches**

### **4.1 Criar e trocar de branch**
```bash
# Criar um novo branch
git branch nome-da-feature

# Trocar para o novo branch
git checkout nome-da-feature
```

### **4.2 Criar e trocar de branch em um único comando**
```bash
git checkout -b nome-da-feature
```

### **4.3 Listar branches**
```bash
# Listar todos os branches locais
git branch

# Listar branches locais e remotos
git branch -a
```

### **4.4 Deletar branches**
```bash
# Deletar um branch local
git branch -d nome-da-feature

# Forçar a deleção de um branch local
git branch -D nome-da-feature
```

---

## **Capítulo 5: Sincronizando com o Repositório Remoto**

### **5.1 Enviar commits para o repositório remoto**
```bash
# Enviar commits do branch atual para o remoto
git push origin nome-do-branch
```

### **5.2 Atualizar o branch local com mudanças remotas**
```bash
# Baixar e aplicar mudanças remotas ao branch atual
git pull origin nome-do-branch
```

### **5.3 Buscar mudanças sem aplicá-las**
```bash
# Buscar mudanças do repositório remoto
git fetch origin
```

---

## **Capítulo 6: Resolvendo Conflitos**

### **6.1 O que são conflitos no Git?**
Conflitos ocorrem quando dois commits alteram a mesma parte de um arquivo. O Git solicita que você resolva manualmente.

### **6.2 Passos para resolver conflitos**
1. Edite os arquivos em conflito e escolha as alterações que deseja manter.
2. Adicione os arquivos resolvidos à área de preparação:
   ```bash
   git add arquivo-com-conflito.txt
   ```
3. Conclua o processo de merge ou rebase:
   ```bash
   git merge --continue
   ```

### **6.3 Cancelar operações em andamento**
```bash
# Cancelar um merge ou rebase
git merge --abort
git rebase --abort
```

---

## **Capítulo 7: Organizando o Repositório**

### **7.1 Ignorar arquivos indesejados**
Crie um arquivo `.gitignore` para listar arquivos ou pastas que não devem ser rastreados.

**Exemplo de `.gitignore`:**
```
# Ignorar arquivos temporários
*.log
*.tmp

# Ignorar pastas específicas
/node_modules
/dist
```

### **7.2 Limpando arquivos não rastreados**
```bash
# Listar arquivos não rastreados
git clean -n

# Remover arquivos não rastreados
git clean -f
```

---

## **Capítulo 8: Navegando pelo Histórico do Git**

### **8.1 Visualizar o histórico de commits**
```bash
# Ver detalhes dos commits recentes
git log

# Ver histórico de commits de forma resumida
git log --oneline
```

### **8.2 Recuperar um estado anterior**
```bash
# Restaurar um arquivo de um commit anterior
git checkout hash-do-commit -- arquivo.txt

# Reverter todo o branch para um commit anterior
git reset --hard hash-do-commit
```

---

## **Capítulo 9: Rebase e Reorganização de Commits**

### **9.1 Aplicar commits sobre outro branch**
```bash
# Reaplicar commits do branch atual sobre outro
git rebase main
```

### **9.2 Resolver conflitos durante rebase**
1. Resolva os conflitos manualmente.
2. Adicione os arquivos resolvidos:
   ```bash
   git add arquivo.txt
   ```
3. Continue o rebase:
   ```bash
   git rebase --continue
   ```

---

## **Capítulo 10: Comandos Avançados e Ferramentas do Git**

### **10.1 Reverter um commit específico**
```bash
# Criar um commit que desfaz alterações de outro commit
git revert hash-do-commit
```

### **10.2 Trabalhar com Stash**
```bash
# Guardar mudanças temporariamente
git stash

# Recuperar mudanças salvas
git stash apply

# Listar mudanças salvas no stash
git stash list
```

---

## **Conclusão: Preparação para o Ambiente Corporativo**

Com este guia, você aprendeu os comandos e práticas fundamentais para trabalhar com Git em um ambiente corporativo. Pratique regularmente para ganhar confiança e aplicar esses conceitos de maneira eficiente em projetos reais!
