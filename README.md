# angular2-for-react-developers
Some snippets to help understanding angular2 concepts in terms of react


## Creating a Component

### Angular 2
```typescript
@Component({  
      selector: 'my-app',  
      template: `    <h1>{{title}}</h1>    <h2>My favorite hero is: {{myHero}}</h2>    `})
export class AppComponent {
  @Input name: String;
  title = 'Tour of Heroes';
  myHero = 'Windstorm';
}
```

### React 
```javascript
export class AppComponent extends ReactComponent {
    

    getInitialState() {
       return {title: 'Tour of Heroes', myHero: 'Windstorm'};
    },

    render() {
        var {title, myHero} = this.state;
        var {name} = this.props;
        return <div>
        <h1>{title}</h1>    <h2>My favorite hero is: {myHero}</h2> 
        <h2>My name is: { name} </h2>
        </div>
    }
}

```
