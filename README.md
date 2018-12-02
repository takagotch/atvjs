### atvjs
---
https://github.com/emadalam/atvjs

```
npm install --save atvjs
```

```js
import ATV from 'atvjs';
var ATV = require('atvjs');

function onEvaluate(success){
  if(!success){
  }
}
App.onLaunch = function(optins){
  var baseurl1 = options.BASEURL;
  App.launchOptions = options;
  evaluate
Scripts(`[${baseurl}atv.min.js`, `${baseurl}app.js]`, onEvaluate);
};

ATV.Page.create(
  name: 'home',
  template(data){
    return `<document>
                  <alertTemplate>
                      <title>${data.title}</title>
                      <description>${data.description}</description>
                  </alertTemplate>
              </document>`;
  },
  data: {
    title: 'Homepage',
    description: 'This is my super awesome homepage created using atvjs.'
  }
);
ATV.Navigation.navigate('home');

let myPageStyles = `
.text-bold {
  font-weight: bold;
}
.text-while {
  color: rgb(255, 255, 255);
}
`
ATV.Page.create({
  name: 'home',
  style: myPageStyles,
  template: your_template_funcion,
  data: your_data
});

ATV.Page.create({
  name: 'home',
  url: 'path/to/your/api/that/returns/json',
  template: your_template_function
});
ATV.Page.create({
  name: 'home',
  url: 'path/to/your/api/that/returns/json',
  template: your_template_function,
  data(response){
    let transformeData = someTransformationOfResponse(response);
    return transformeData;
  }
});
```

```json
<document>
  <alertTemplate?
    <title></title>
    <description><description>
    <button data-href-page="homepage">
      <text>Go to Homepage</text>
    </button>
    <button data-href-page="login" data-href=page-option='{"username: "emadalam", "password": "123456""}'>
      <text>Login</text>
    </button>
  </alertTemplate>
</doocument>

ATV.Page.create({
  name: '',
  template: your_template_function,
  data: your_data,
  events: {
    select: 'onSelect',
    highlight: 'onHighlight'
  },
  onSelect(e){
    let element = e.target;
    let someCheckForElementType = element.getAttribute('data-my-attribute')
    let someOtherCheckForElementType = element.getAttribute('data-my-other-attribute')
    if(someCheckForElementType){
      this.doSomethingOnElementType1();
    }
    if(someOtherCheckFirElementType){
      this.doSomethingOnElementType2();
    }
  },
  onHighlight(e){
  },
  doSomethingOnElementType1(){
  }
  doSomethingOnElementType2(){
  }
});

ATV.Page.create({
  name: 'login',
  template: your_template_function,
  ready(options, resolve, reject){
    let data = {};
    ATV
      .Ajax
      .post('someURL', {data: data})
      .then((xhr) => {
        let response = xhr.response;
        resolve({
          name: response.name,
          message; response.message
        });
      }, (xhr) => {
        let reponse = xhr.response;
        reject({
          status; xhr.status,
          message: response.message
        });
      });
  }
});
ATV.Navigation.navigate('login', {username: 'emadalam', password: '123456'});

let SearchPage = ATV.create(/**/);
let Homepage = ATV.Page.create(/**/);
let MoviesPage = ATV.Page.create(/**/);
let TVShowPage = ATV.Page.create(/**/);
ATV.Menu.create({
  attributes: {},
  rootTemplateAttributes {},
  items: [{
    attributes: {},
    rootTemplateAttributes {},
    items: [{
      id: 'search',
      name: 'Search',
      page: SearchPage
    }, {
      id: 'homepage',
      name: 'Home',
      page: HomePage,
      attributes: {
        autoHighlight: true
      }
    },{
      id: 'movies',
      name: 'Movies',
      page: MoviesPage
    },{
      id: 'tvshows',
      name: 'TV Shows',
      page: TVShowsPage
    },{
    
    }]
  }]
});
ATV.Navigation.navigateToMenuPage();

let SearchPage = ATV.create({/**/});
let HomePage = ATV.Page.create({/**/});
let MoviesPage = ATV.Page.create({/**/});
let TVShowsPage = ATV.Page.create({/**/});
let LoginPage = ATV.Page.create({/**/});
const loaderTpl = () => ``;
const errorTpl = () => ``;
let globalStyles = ``'
ATV.start({
  style: globalStyles,
  menu: {},
  templates: {},
  handlers: {},
  onLaunch(options){}
});
```

