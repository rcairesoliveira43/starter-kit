# ngX Starter Kit

Web project starter kit incluindo ferramentas modernas e fluxo de trabalho baseado em
[angular-cli](https://github.com/angular/angular-cli), melhores práticas da comunidade, um modelo base escalável e
uma boa base de aprendizado.

Gerado usando [ngX-Rocket](https://github.com/ngx-rocket/generator-ngx-rocket).

### Beneficios

- Inicie um projeto rapidamente em segundos e concentre-se em recursos, não em estruturas ou ferramentas

- Ferramentas de nível industrial, prontas para uso em um ambiente de integração contínua e DevOps

- Arquitetura escalável com modelo de aplicativo básico, incluindo componentes, serviços e testes de exemplo

# Começando

1. Vá para a pasta do projeto e instale as dependências:
 ```bash
 npm install
 ```
 
2. Inicie o servidor de desenvolvimento e abra `localhost:4200` no seu browser:
 ```bash
 npm start
 ```
 
# Estrutura do Projeto

```
dist/                        compiled version
docs/                        project docs and coding guides
e2e/                         end-to-end tests
src/                         project source code
|- app/                      app components
|  |- @shared/               shared module (common services, components, directives and pipes)
|  |- app.component.*        app root component (shell)
|  |- app.module.ts          app root module definition
|  |- app-routing.module.ts  app routes
|  +- ...                    additional modules and components
|- assets/                   app assets (images, fonts, sounds...)
|- environments/             values for various build environments
|- theme/                    app global scss variables and theme
|- translations/             translations files
|- index.html                html entry point
|- main.scss                 global style entry point
|- main.ts                   app entry point
|- polyfills.ts              polyfills needed by Angular
+- test.ts                   unit tests entry point
reports/                     test and coverage reports
proxy.conf.js                backend proxy configuration
```

# Principais tarefas

A automação de tarefas é baseada em [NPM scripts](https://docs.npmjs.com/misc/scripts).

Tasks                         | Description
------------------------------|---------------------------------------------------------------------------------------
npm start                     | Run development server on `http://localhost:4200/`
npm run build [-- --env=prod] | Lint code and build app for production in `dist/` folder
npm test                      | Run unit tests via [Karma](https://karma-runner.github.io) in watch mode
npm run test:ci               | Lint code and run unit tests once for continuous integration
npm run e2e                   | Run e2e tests using [Protractor](http://www.protractortest.org)
npm run lint                  | Lint code
npm run translations:extract  | Extract strings from code and templates to `src/app/translations/template.json`
npm run docs                  | Display project documentation

Ao construir o aplicativo, você pode especificar o ambiente de destino usando a flag `--env <name>` 
(não esqueça de `--` para passar argumentos para npm scripts).

O ambiente de compilação padrão é `prod`.

## Servidor de desenvolvimento

Execute `npm start` para um ambiente dev server. Navegar com `http://localhost:4200/`. 
O aplicativo será recarregado automaticamente se você alterar qualquer um dos arquivos de origem.
Você não deve usar `ng serve` diretamente, pois não usa a configuração de proxy de back-end por padrão.

## Code scaffolding

Execute `npm run generate -- component <name>` para gerar um novo componente. 
Você também pode usar `npm run generate -- directive|pipe|service|class|module`.

Se você instalou [angular-cli](https://github.com/angular/angular-cli) globalmente com `npm install -g @angular/cli`,
você também pode usar o comando `ng generate` diretamente.

## Additional tools

As tarefas baseiam-se principalmente na ferramenta `angular-cli`. Use `ng help` para obter mais ajuda ou vá para o
[Angular-CLI README](https://github.com/angular/angular-cli).

# What's in the box

O modelo de aplicativo é baseado em 
[HTML5](http://whatwg.org/html), 
[TypeScript](http://www.typescriptlang.org) and
[Sass](http://sass-lang.com). 
Os arquivos de tradução usam o formato comum [JSON](http://www.json.org).

#### Tools

Os processos de desenvolvimento, construção e qualidade são baseados em 
[angular-cli](https://github.com/angular/angular-cli) and
[NPM scripts](https://docs.npmjs.com/misc/scripts), que incluem:

- Processo de compilação e agrupamento otimizado com [Webpack](https://webpack.github.io)
- [Development server](https://webpack.github.io/docs/webpack-dev-server.html) com proxy de back-end e live reload
- Cross-browser CSS com [autoprefixer](https://github.com/postcss/autoprefixer) e
  [browserslist](https://github.com/ai/browserslist)
- Asset revisioning para [better cache management](https://webpack.github.io/docs/long-term-caching.html)
- Unit tests usando [Jasmine](http://jasmine.github.io) e [Karma](https://karma-runner.github.io)
- End-to-end tests usando [Protractor](https://github.com/angular/protractor)
- Static code analysis: [TSLint](https://github.com/palantir/tslint), [Codelyzer](https://github.com/mgechev/codelyzer),
  [Stylelint](http://stylelint.io) e [HTMLHint](http://htmlhint.com/)
- Local knowledgebase server usando [Hads](https://github.com/sinedied/hads)
- Automatic code formatting com [Prettier](https://prettier.io)

#### Libraries

- [Angular](https://angular.io)
- [Bootstrap 4](https://getbootstrap.com)
- [Font Awesome](http://fontawesome.io)
- [RxJS](http://reactivex.io/rxjs)
- [ng-bootstrap](https://ng-bootstrap.github.io)
- [ngx-translate](https://github.com/ngx-translate/core)
- [Lodash](https://lodash.com)

#### Coding guides

- [Angular](docs/coding-guides/angular.md)
- [TypeScript](docs/coding-guides/typescript.md)
- [Sass](docs/coding-guides/sass.md)
- [HTML](docs/coding-guides/html.md)
- [Unit tests](docs/coding-guides/unit-tests.md)
- [End-to-end tests](docs/coding-guides/e2e-tests.md)

#### Other documentation

- [I18n guide](docs/i18n.md)
- [Working behind a corporate proxy](docs/corporate-proxy.md)
- [Updating dependencies and tools](docs/updating.md)
- [Using a backend proxy for development](docs/backend-proxy.md)
- [Browser routing](docs/routing.md)

# License

[MIT](https://github.com/ngx-rocket/generator-ngx-rocket/blob/main/LICENSE)
