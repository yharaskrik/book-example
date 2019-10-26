npx create-nx-workspace@latest example

choose: angular + nest
application name: admin

Add all of the capabilities: yarn add -D @nrwl/angular @nrwl/web @nrwl/react @nrwl/node @nrwl/express @nrwl/nest @nrwl/next @nrwl/workspace

to test everything went ok: ng s and ng s api
note: admin is set to the default app

Will see welcome message on localhost:4200
note: proxy.conf.json

tests default to jest and cypress

When generating the form is ng g @nrwl/<capability>:<type> <name>

ng g @nrwl/next:application payment

Generate a next app, if you get cannot find module @nrwl/workspace run yarn add -D @nrwl/next again to make sure it was added correctly

if running at the same time as the angular application append --port=4201

ng g @nrwl/angular:ngrx app --module=apps/admin/src/app/app.module.ts --root --minimal

choose no for facade
discuss runtime checks and storedevtools module
discuss effects later

display affected:build, affected:test and affected:dep-graph

show ng test <project>
show ng build <project>

for all angular, nest and react same tool used for everything

Building Next app:
Add production configuration in the build target for the next app
change the output path to /dist/apps/payment/.next
ng build payment --prod

Building and Serving Angular app:
ng build admin --prod
install a server to serve it: yarn add -D http-server

run `http-server dist/apps/admin`
go to 127.0.0.1:8080

Building and serving api
ng build api --prod
node dist/apps/api/main.js
