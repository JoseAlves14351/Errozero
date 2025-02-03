# ErroZero - Sistema de Reportagem de Problemas

ErroZero é um sistema de gerenciamento de reportes de problemas em computadores para ambiente escolar. O sistema permite que alunos reportem problemas em equipamentos e que administradores gerenciem estes reportes.

## Requisitos do Sistema

- PHP 8.2 ou superior
- MySQL/MariaDB 10.4 ou superior
- Servidor web (Apache/Nginx)
- Composer (opcional, para dependências futuras)

## Configuração do Ambiente

1. **Configuração do Banco de Dados**
   - Crie um banco de dados chamado `errozero_db`
   - Importe o arquivo `errozero_db.sql` para criar as tabelas e dados iniciais
   ```sql
   mysql -u root -p errozero_db < errozero_db.sql
   ```

2. **Configuração do Servidor Web**
   - Clone ou copie todos os arquivos para o diretório do seu servidor web
   - Certifique-se que o diretório tem permissões de leitura e escrita apropriadas
   - Configure o documento root para apontar para o diretório do projeto

3. **Configuração do PHP**
   - Verifique se as extensões necessárias estão habilitadas no php.ini:
     - mysqli
     - session
     - json

## Estrutura de Arquivos

```
errozero/
├── admin.css
├── admin.js
├── admin.php
├── frontend.html
├── frontend.php
├── frontend-css.css
├── index.php
├── processaLogin.php
├── reports.php
├── session_verify.php
└── vendor/
    └── ... (arquivos de dependências)
```

## Credenciais de Acesso

### Administrador
- Email: admin@oficina.pt
- Senha: admin

### Aluno
- Email: aluno@oficina.pt
- Senha: aluno

## Executando o Sistema

1. Inicie seu servidor web e MySQL/MariaDB
2. Abra seu navegador e acesse: `http://localhost/errozero`
3. Faça login com uma das credenciais acima

## Funcionalidades

### Painel do Aluno
- Reportar problemas em computadores
- Selecionar sala, componente e tipo de problema
- Descrever detalhadamente o problema

### Painel do Administrador
- Visualizar todos os reportes
- Atualizar status dos reportes (Pendente, Em Análise, Resolvido)
- Acompanhar histórico de mudanças

## Solução de Problemas

### Erro de Conexão com Banco de Dados
- Verifique se o serviço MySQL está rodando
- Confirme as credenciais em `processaLogin.php` e `frontend.php`
- Verifique se o banco de dados `errozero_db` existe

### Erro de Permissão
- Certifique-se que o usuário do servidor web tem permissões de leitura/escrita
- Verifique as permissões das pastas e arquivos (geralmente 755 para pastas e 644 para arquivos)

### Problemas de Login
- Limpe os cookies do navegador
- Verifique se as sessões PHP estão funcionando
- Confirme se as credenciais estão corretas no banco de dados

## Segurança

- Todas as senhas são armazenadas com hash usando `password_hash()`
- Validação de sessão implementada
- Sanitização de inputs
- Proteção contra SQL Injection usando prepared statements

## Suporte

Para reportar problemas ou sugerir melhorias, entre em contato com a equipe de desenvolvimento.- a14351@oficina.pt


