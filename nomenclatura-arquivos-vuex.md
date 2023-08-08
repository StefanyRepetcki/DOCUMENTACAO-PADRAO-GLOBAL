# Melhores Práticas de Nomenclatura para Stores no Vuex

Neste guia, exploraremos as melhores práticas para nomenclatura de stores no Vuex, a gerência de estado oficial do Vue.js. Uma nomenclatura consistente e bem escolhida para suas stores ajuda a manter a organização, legibilidade e escalabilidade do código. Abordaremos questões como maiúsculas e minúsculas, bem como onde armazenar diferentes tipos de informações.

## Nomenclatura em Minúsculas ou Maiúsculas?

**Recomendação:** Utilize letras minúsculas para o nome das stores.

- **Por quê?** Usar letras minúsculas segue a convenção de nomenclatura em JavaScript, tornando seu código mais consistente e alinhado com as práticas da linguagem.

**Exemplo:**

```javascript
// Bom
const store = createStore({
  state: { /* ... */ },
  // ...
});
```
## Estrutura de Stores
**Recomendação:** Organize suas stores com base nas funcionalidades do aplicativo.
**Por quê?** Organizar as stores por funcionalidades facilita a localização e manutenção do código relacionado.

**Exemplo:**
```
src/
|-- store/
|   |-- user/
|   |   |-- index.js
|   |   |-- actions.js
|   |   |-- mutations.js
|   |   |-- getters.js
|   |   |-- state.js
|   |-- cart/
|   |   |-- index.js
|   |   |-- actions.js
|   |   |-- mutations.js
|   |   |-- getters.js
|   |   |-- state.js
|   |-- ...
```
##  Nomenclatura de Módulos
**Recomendação:** Utilize camelCase para nomear módulos e evite abreviações desnecessárias.

**Por quê?** CamelCase é uma convenção amplamente usada em JavaScript e ajuda a tornar o código mais legível. Evitar abreviações mantém a clareza do nome do módulo.

**Exemplo:**
```javascript
// Bom
const store = createStore({
  modules: {
    userAuth: { /* ... */ },
    shoppingCart: { /* ... */ },
    // ...
  },
});
```
##  Nomenclatura de Estados, Ações, Mutations e Getters
**Recomendação:** Utilize camelCase para nomear estados, ações, mutations e getters.
**Por quê?** Manter a consistência com as convenções de JavaScript resulta em um código mais claro e alinhado.
**Exemplo:**
```javascript
const store = createStore({
  state: {
    isLoggedIn: false,
  },
  actions: {
    loginUser: /* ... */,
  },
  mutations: {
    SET_LOGIN_STATE: /* ... */,
  },
  getters: {
    userIsLoggedIn: /* ... */,
  },
});
```

##  Uso de "SET" e Maiúsculas em Mutations
**Explicação:** A convenção de começar uma mutation com "SET" e usar letras maiúsculas segue um padrão para denotar que a mutation é responsável por definir o valor de um estado específico.
**Por quê?** Essa prática de nomenclatura ajuda a identificar rapidamente as mutations que alteram estados, tornando o código mais legível e descritivo.
**Exemplo:**
```javascript
// Bom
mutations: {
  SET_USER: /* ... */,
  SET_CART_ITEMS: /* ... */,
},
```
## Conclusão
A nomenclatura adequada das stores no Vuex é fundamental para manter um código claro, organizado e facilmente compreensível. Ao seguir práticas como a utilização de letras minúsculas, camelCase e a organização baseada em funcionalidades, você contribui para a escalabilidade e a manutenção do seu aplicativo Vue.js.
Lembre-se de que a consistência é essencial. Ao adotar essas práticas, você garante um código coeso e bem estruturado, facilitando a colaboração e o desenvolvimento em equipe.

Referências:
Vuex Documentation

