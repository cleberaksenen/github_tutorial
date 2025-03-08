# Tutorial sobre o Git e GitHub
Git é um software para gerenciamento de versão para gerenciamento de arquivos de texto no computador.

## O problema
Git e GitHub buscam resolver problemas ligados a:
- Diversas alterações em projetos
- Reversão de alterações
- Múltiplos contribuidores
- Distribuição de funções

## Instalação
```
sudo apt install git
```

***

## Conceitos
### 1. Commit (checkpoint/save)
- Cada vez que se avança, é possível salvar o progresso (criar versões - versionando).
- Dessa forma, teremos um caminho principal e posíveis caminhos secundários.
![Diagrama em branco (4)](https://github.com/user-attachments/assets/223fb24e-8347-4e04-ac88-a2639565d66a)

### 2. Untracked files
- Arquvos que ainda não foram apresentados ao Git como sendo passíveis a serem versionados.

***

## Comandos
- Tornar a pasta especial (possibilidade de versionar os arquivos dentro dela), inicializando um repositório vazio:
```
git init .
```

- Configurar o e-mail e usuário a ser utilizado:
```
git config --global user.email "email@exemplo.com"
git config --global user.name "seunome"
```

- Verificar o status do repositório:
```
git status
```

#### Prepara aquilo que vai para o commit:
- OBS. Cada commit terá um identificador único
##### Passo 1: Adicionar o arquivo:
```
git add [arquivo]
```
-> Quero voltar atrás:
```
git reset [arquivo]
```

##### Passo 2: Realiza o commit (checkpoint), juntamente a uma mensagem (descrição):
```
git commit -m "mensagem"
```
- Todos os commits ficam dentro da pasta "./git"
- Posso ver todos os checkpoints com:
```
git log
```
- Para saber o que foi alterado no arquivo:
```
git diff [arquivo]
```

##### Passo 3 (opcional): Criar uma banch (ramificação)
- Estamos fazendo tudo na branch *main*
- Podemos criar ou mudar para uma nova branch:
```
git branch [nome da banch]
```
- Podemos trocar para a branch que acabamos de criar:
```
git checkout [nome da banch]
```
- Podemos saber em qual branch estamos com apenas:
```
git branch
```
- Podemos deletar uma brnach criada com:
```
git branch -D [nome da banch]
```

##### Observação:
- As informações criadas nessa nova branch não se comunicam com a principal.
- Trocando para a branch *main*, podemos "trazer" as informações de uma outra branch com:
```
git merge [nome da branch]
```
-> Nada acontece com a outra branch
![Diagrama em branco (5)](https://github.com/user-attachments/assets/6f1648e6-e66e-45e2-8166-773c0cf1601f)



