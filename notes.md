Build a angular checklist

- Import 

- routing

### checklist

1. Main app: *app.component.ts*
  ```ts
  @Component({
  selector: 'pm-root',
  template: `
    <div>
    <h1>{{pageTitle}}</h1>
    <pm-products></pm-products>
    </div>`
  })
  export class AppComponent { }
  ```
2. main app module: *app.module.ts*
  ```ts
  NgModule({
  imports: [ BrowserModule ],
  declarations: [
  AppComponent,
  ProductListComponent ],
  bootstrap: [ AppComponent ]
  })
  export class AppModule { }
  ```

3. sub component: *product-list.component.ts*
  ```ts
  @Component({
  selector: 'pm-products',
  templateURL:
  './product-list.component.html'
  })
  export class ProductListComponent { }
  ```









*Clear name*

-  Class:  PascalCasing

- Data & methods: camelCase 

*export class* *AppComponent {*

*showImage: boolean*



- Bootstrap: compile html templates & component ts



- Interpolation (Custom HTML syntax)

  

- Component -(properties)-> DOM

  ​					<-(events)-

  - Event binding

  - Two way binding

  

  **form module**

- Data pipe







- Directives: Custom HTML

- Built-in structural Directives

  *•\*ngIf: If logic*

  ```ts
  <div class='table-responsive'>
  <table class='table' *ngIf='products.length'>
  </div>
  ```

  *•\*ngFor: For loops*

  ```ts
    <tr *ngFor='let product of products'>
    <td></td>
    <td>{{ product.productName }}</td>
    <td>{{ product.productCode }}</td>
    <td>{{ product.releaseDate }}</td>
    <td>{{ product.price }}</td>
    <td>{{ product.starRating }}</td>
    </tr>
  ```

- ```ts
  let nicknames= ['di', 'boo', 'punkeye'];
  for (let nickname in nicknames) {
  console.log(nickname);
  // di, boo, punkeye
    
  for (let nickname in nicknames) {
  console.log(nickname);
  // 1, 2, 3
    
  ```

  







- Back Ticks



Subscribe, callback







### Parent & Child Components

- [x] https://stackoverflow.com/questions/35267146/accessing-a-property-in-a-parent-component

  How to access parent status:

  Design solutions

  - service shared by parent and injected to the child
  - parent injected to the child and accessed directly by the child
  - Data-binding

- Makes it a input, 

  ```ts
  export class Profile implements OnInit {
    @Input() userStatus:UserStatus;
  }
  <profile [userStatus]="userStatus">
  ```



`{{var}}`





### toggle to show and hide the pic

