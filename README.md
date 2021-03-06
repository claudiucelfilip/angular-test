## Main Objectives
Implement the bare minimum functionality for an Album Manager. 
User must be able to:
- view a list of albums
- view details of an album
- create a new album
- remove an album

## Optional Objectives
Implement any of the following for extra appreciation points:
- dynamic search on album list (on the client side)
- implement the edit album page
- form validation
- create a directive
- create a custom pipe
- create a few e2e and unit tests
- use observables
- use route resolvers
- lazy load part a of functionality

### Template Files
The Static server provides static HTML templates for the 3 pages:
- templates/index.html - album listing;
- templates/details.html - album details;
- templates/add.html - album create/edit;

The templates use boostrap 4 CSS and FontAwesome icons.
Feel free to add/remove any needed/missing components to them.

### API Endpoints
There is an API for persisting changes at:
http://angular-test.getsandbox.com

There are 5 endpoints:
- "GET /": "retrieve a list of supported endpoints",
- "GET /albums": "retrieve all the albums",
- "POST /albums": "create a new album",
- "GET /albums/{albumId}": "retrieve album with {albumId}",
- "POST /albums/{albumId}": "update album with {albumId}",
- "DELETE /albums/{albumId}": "remove album with {albumId}"

All POST and DELETE endpoints respond with {"status": "ok"} if successfull.

There's no schema validation on but the following is preferred:
Album Object
```
{
    "id": "number",  // optional, automatically generated on server side
    "title": "string",
    "artist": "string",
    "year": "number",
    "type": "string"
}
```

### Development Info
The project is setup with Angular 6 CLI; for which you'll need node 8.9 or greater to run.
Run `npm start` for a dev server. This will open two browser tabs:
- `http://localhost:4200/` - serves Angular App;
- `http://localhost:4201/` - serves Static Template Files;

Angular App should autoreload on code change (as per ng-cli).
Static Template Files can be found in the templates folder.

#### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

#### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

#### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
