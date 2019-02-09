# angular-commands
Comandos basicos de angular 6

Create module Command

ng generate component components/footer

o

ng g c components/footer

Para crear partes reutilizables dentro de angular se utiliza dentro de componentes la carpeta llamada shared

ng g c components/shared/navbar

Para crear un componente sin las hojas de estilo lo realizamos de la siguiente manera

ng g c components/casas -is


Instalar plugin angular para crear las rutas manualmente con el comando

ng-routes

Para visualizar las diferentes rutas es necesario declarar la siguiente etiqueta:

< router-outlet></ router-outlet>

dentro de routes manejar lo siguiente si deseamos los hash

imports: [RouterModule.forRoot(routes, {useHash: true})]

Para crear un link se utiliza lo siguiente:

[routerLink]="['home']"
Resultado:
tusitio.com/home

si necesitamos mas informacion en la url colocamos lo siguiente
Resultado:
[routerLink]="['home', 'color', '1']"
tusitio.com/home/color/1

La manera de colocar un link dinamico en angular es de la siguiente manera
Donde i es dinamico y heroe no es una subcarpeta si no como ruta principal

[routerLink]="['/heroe', i]"

Tambien tenemos en el router lo siguiente:

{ path: 'heroe/:id', component: HeroeComponent }


LOS PIPES DISPONIBLES EN ANGULAR SON:

* currency
* date
* uppercase
* json
* limitTo
* lowercase
* async
* decimal
* percent

Ejemplo de uso:
< h1>{{ heroe.nombre | uppercase }} < small>{{ heroe.aparicion | date:'y' }}< /small>< /h1>

para no agregar al componente el archivo de prueba
utilizamos el siguiente comando
ng g c components/heroetarjeta --spec=false
