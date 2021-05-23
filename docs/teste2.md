Nesse guia será abordado em detalhes a arquitetura do projeto, como é organizado a estrutura de pastas e arquivos além de abordar os arquivos padrões utilizados em todos projetos

Visão geral da arquitetura de um projeto mobile: 

****** AQUI VAI A IMAGEM DA ARQUITETURA 

# App1/

-

-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
# App2/
---

Pasta que contém os arquivos que compõe a aplicação, ou seja, vai conter os arquivos referentes a aplicação e também os seus modulos. 

Estrutura da pasta app/ de forma resumida: 

1. **app.view.dart -** Camada visual do app. 
2. **app.controller.dart -** Camada controller do aplicativo, responsável por disponibilizar a regra de negócios referente a aplicação. 
3. **modulos/  -** 

## 1. app.view.dart

Camada visual da aplicação. 

## 2. app.controller.dart

Camada onde esta localizada a regra de negócios geral do app. 

Exemplo de uma classe appController padrão:

```dart hl_lines="2 3"
class AppController extends CustomAppController {
  
  @override
  AppConfig appConfig;

  @override
  AuthPreferences authPreferences = AuthPreferences(privateRoute: "/teste");

  AppStartConfig appStartConfig;

  static final AppController instance = AppController._();

  AppController._() {
    appStartConfig = AppStartConfig(appSession: appSession);

    appConfig = AppConfig(
      setInitialRoute: appStartConfig.initialRoute,
    );
  }
}
```

## 3. modulos/

Descricao sobre......

[Acesse o guia "modulos" para ver os passos para criar um modulo.](https://www.notion.so/Modulos-e780518fa42d49cda77c972afd378e97) 

# Core/

---

Pasta que contém arquivos globais que serão utilizados em diversas partes da nossa Aplicação.