# Descrição 
Passo a passo para lidar com o github action. Este exemplo ira usar o nest.js

# Regra da Master

Criando uma regra para que a master não receba commits

```
Va em settings > branches > Add Rule
```

Coloca o nome da master, para atribuir a master uma rule

Selecione as Opções

* Incluir para administrador
* Restrict who can push to master(deixei vazio)
* Marcar opção que requer code review tendo pelo menos 1 aceito para poder entrar

Salve a role. E se quise testar basta tentar fazer um push na master que dará erro

# Criando Dev

Crie uma branch chamada dev

```
git checkout -b dev
```

Faça o push

```
git push origin dev
```

Va no git e crie uma pull request. Ela nao pode ser mergiada pq alguem tem que fazer o code review dela

# Criando os CODEROWNERS

Cria um arquivo na raiz do projeto chamado CODEOWNERS(vulgo os donos da bola kkkkk)

A regra é muito simples:
```
*.ts(todos arquivos de typescript) @usuario(usuario que sera usado no codereview)
```

Volte em branches edit a regra da branch master e abilite a opção Require review from Code Owners