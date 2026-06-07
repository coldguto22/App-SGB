# AppSGB - Sprint Consulta

Implementacao inicial de consultas com dados reais da API para o app Android.

## O que foi implementado

- Tela principal com tabs para:
  - Acervo de Livros
  - Emprestimos
- Menu na Toolbar com navegacao para:
  - Usuarios
  - Unidades
  - Atualizar
- Consumo da API real usando Retrofit (`Call.enqueue`) via `SgbRepository`.
- Estados de UI:
  - carregando
  - lista vazia
  - erro com `Toast`
- Itens de lista com layouts XML dedicados:
  - `item_livro.xml`
  - `item_emprestimo.xml`
  - `item_usuario.xml`
  - `item_unidade.xml`

## Arquivos principais

- `app/src/main/java/com/fatec/sgb/MainActivity.kt`
- `app/src/main/java/com/fatec/sgb/ConsultaListaActivity.kt`
- `app/src/main/java/com/fatec/sgb/retrofit/SgbRepository.kt`
- `app/src/main/java/com/fatec/sgb/adapters/*`
- `app/src/main/res/layout/*`
- `app/src/main/res/menu/menu_main.xml`

## Como validar

1. Build do projeto:

```powershell
.\gradlew.bat assembleDebug
```

2. Abrir o app e validar:

- Carregamento inicial de livros e emprestimos
- Refresh pelo FAB e menu
- Navegacao pelo menu para Usuarios e Unidades
- Exibicao de listas vazias quando nao houver dados


