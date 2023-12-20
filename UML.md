
# BANCO DE BANCO DADOS


### Diagrama Banco de Dados.




## Banco de Dados

#### Tabela Users

```
  Users
```

| Coluna   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `bigInt` | **Autoincremnto**.  |
| `email` | `varchar(255)` | **Obrigatório**.  |
| `senha` | `varchar(255)` | **Obrigatório**.  |
| `created_at` | `DateTime` | **Data Criado**.  |
| `update_at` | `DateTime` | **Altera Data ao alterar dado**.  |

#### Tabela Projects

```
  Projects
```

| Coluna   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `bigInt` | **Autoincremnto**.  |
| `user_id` | `bigInt` | **Usuário que criou projeto**.  |
| `title` | `varchar(255)` | **Titulo Projeto**.  |
| `description` | `text` | **Descrição Proejeto**.  |
| `image` | `varchar(255)` | **Logo Projeto**.  |
| `created_at` | `DateTime` | **Data Criado**.  |
| `update_at` | `DateTime` | **Altera Data ao alterar dado**.  |

#### Tabela Tasks

| Coluna   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `bigInt` | **Autoincremnto**.  |
| `assigned_id` | `bigInt` | **Usuário que tarefa foi atribuida**.  |
| `project_id` | `bigInt` | **Projeto **.  |
| `title` | `varchar(255)` | **Titulo Tarefa**.  |
| `description` | `text` | **Descrição Tarefa**.  |
| `date_deadline` | `dateTime` | **Data Entrega**.  |
| `time_estimated` | `int` | **Quantidade Horas Finalizar**.  |
| `priority` | `tinyint` | **Prioridades Urgente, **.  |
| `status` | `enum` | **Status Projetos, **.  |
| `created_at` | `DateTime` | **Data Criado**.  |
| `update_at` | `DateTime` | **Altera Data ao alterar dado**.  |

#### Tabela users_tasks

```
  usres_tasks
```

| Coluna   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `user_id` | `bigInt` | **Usuário que criou tarefa**.  |
| `task_id` | `bigint` | **Tarefa que foi criada**.  |
| `created_at` | `DateTime` | **Data Criado**.  |
| `update_at` | `DateTime` | **Altera Data ao alterar dado**.  |

#### Tabela Tasks Itens

```
  tasks_itens
```

| Coluna   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `bigInt` | **Autoincremnto**.  |
| `users_id` | `bigInt` | ** Usuário que adicionou item**.  |
| `task_id` | `bigInt` | ** Referente a Tarefa **.  |
| `title` | `varchar(255)` | **Titulo do Item Tarefa**.  |
| `description` | `text` | **Descrição do Item  Tarefa**.  |
| `image` | `varchar(255)` | **Imagem Entrega**.  |
| `status` | `enum` | ** Status Item ativo ou inativo **.  |
| `created_at` | `DateTime` | **Data Criado**.  |
| `update_at` | `DateTime` | **Altera Data ao alterar dado**.  |


