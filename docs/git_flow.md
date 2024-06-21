# Git Flow

Git Flow é uma metodologia de branching para Git, que define uma estrutura clara e robusta para o gerenciamento de versões e desenvolvimento colaborativo. Ele define diferentes tipos de branches e o fluxo de trabalho entre eles, facilitando o desenvolvimento contínuo e a integração de novas funcionalidades.

## Branches do Git Flow

Git Flow utiliza sete tipos principais de branches:

| Branch       | Descrição                                                                                       |
|--------------|-------------------------------------------------------------------------------------------------|
| `main`       | Contém o histórico oficial do projeto. Cada commit no branch `main` representa uma versão de produção. |
| `develop`    | Contém o histórico de desenvolvimento. É a base para novas funcionalidades e a próxima versão.  |
| `feature`    | Usado para desenvolver novas funcionalidades. Branches `feature` são derivados de `develop`.    |
| `release`    | Suporta a preparação de uma nova versão de produção. Branches `release` são derivados de `develop` e mesclados em `main` e `develop` ao final. |
| `hotfix`     | Usado para aplicar correções urgentes em produção. Branches `hotfix` são derivados de `main` e mesclados em `main` e `develop` ao final. |
| `bugfix`     | Usado para corrigir bugs identificados durante o ciclo de desenvolvimento. Branches `bugfix` são derivados de `develop` e mesclados de volta em `develop` quando concluídos. |
| `support`    | Suporta manutenção de versões antigas do software. Branches `support` são derivados de versões específicas do `main` e mantêm correções necessárias. |

## Exemplos de Comandos Git Flow

Aqui estão alguns exemplos de como usar os comandos Git Flow no seu projeto:

### Inicializando Git Flow

Para inicializar o Git Flow em um repositório existente, execute:

```sh
git flow init
```

### Criando uma Nova Feature

Para iniciar uma nova feature, execute:

```sh
git flow feature start minha-feature
```

Para finalizar a feature e mesclar com develop, execute:

```sh
git flow feature finish minha-feature
```

### Criando um Release

Para iniciar um novo release, execute:

```sh
git flow release start 1.0.0
```

Para finalizar o release, mesclar com main e develop, e criar uma tag, execute:

```sh
git flow release finish 1.0.0
```

### Criando um Hotfix

Para iniciar um hotfix, execute:

```sh
git flow hotfix start correcao-urgente
```

Para finalizar o hotfix e mesclar com main e develop, execute:

```sh
git flow hotfix finish correcao-urgente
```

### Criando um Bugfix

Para iniciar um bugfix, execute:

```sh
git flow bugfix start correcao-bug
```

Para finalizar o bugfix e mesclar com develop, execute:

```sh
git flow bugfix finish correcao-bug
```

### Criando um Support

Para iniciar um branch de suporte, execute:

```sh
git flow support start suporte-versao-antiga main
```
