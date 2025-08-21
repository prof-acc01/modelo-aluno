# Repo-modelo-aluno

Este reposiório é um repositório base para que os professores criem o repositório modelo para os alunos.

Instruções ao professor:
- Configure os diretórios de forma que para cada exercicio (.zip) no repositório de soluções tenha uma pasta dentro da pasta problemas/ neste repositório.

-  É necessário fazer mudanças no arquivo .github/workflows/**trigger.yml**, siga as instruções abaixo:
    - linha 70: if [ "$GITHUB_ACTOR" = "bot" ] || [ "$GITHUB_ACTOR" = "insira aqui o usuario dono do repositório hub" ]; then
    - linha 86: se renomeou o repositório hub de outro nome, modificar para tal nome
    - linha 87: modifique para seu usuario
    - linha 97: se renomeou o repositório hub de outro nome, modificar para tal nome
    - linha 98: modifique para seu usuario

Após isso transforme seu repositório em um [repositório template](https://docs.github.com/pt/repositories/creating-and-managing-repositories/creating-a-template-repository#creating-a-template-repository) para que os alunos possam utilizar. Peça para que os alunos mudem a configuração de visibilidade do repositório para privado e que façam um convite para que a conta do repositório hub seja um colaborador.

Instruções ao aluno:

- mude as configurações de visibilidade do repositório para privado
- crie um [PAT (Personal Acess Token)](https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#como-criar-um-personal-access-token-classic)
- crie um [secret](https://docs.github.com/pt/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets#creating-secrets-for-a-repository) com o nome PAT e insira o PAT criado.
- caso tenha dado um nome diferente ao secret modifique a linha 84 do arquivo **trigger**:  token: ${{ secrets.NOME_DO_SECRET }}


