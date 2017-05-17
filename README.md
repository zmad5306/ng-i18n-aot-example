# Angular 2 i18n AOT example

See: https://angular.io/docs/ts/latest/cookbook/i18n.html for more info

When running with AOT multiple builds must be deployed. Each build ('ng serve' or 'ng build' from angualr cli) need passed the following args

$ ng serve --aot \
           --i18n-file=src/i18n/messages.es.xlf \
           --locale=es \
           --i18n-format=xlf

see start-es npm script in package.json

'ng serve --aot' has issues when only changing template files. if a ts file is changed it will rebuild. if no ts is changed then the rebuild does not compile the templates. 