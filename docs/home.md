<a id="home" style="position: absolute; top: 0"></a>

# Vuex Pathify

> Pathify provides a declarative, state-based, path interface to your Vuex store

With Pathify, you access Vuex by **path**:

```pathify
'foo/bar@a.b.c'
```

Paths can reference any **module**, **property** or **sub-property**:

![pathify-diagram](assets/img/readme/pathify-diagram.png)


**Get** or **set** data without **syntax juggling** or worrying about **implementation**:

```pathify
store.get('loaded')
```
```pathify
store.set('loaded', true)
```


Set up **one or two-way** data binding on **any** store value without **bloat** or **fuss**:

```pathify
computed: {
      products: get('products'),
      category: sync('filters@category'),
}
```



Wire **multiple** properties (or sub-properties) using **array**, **object** and **wildcard** formats:

```pathify
...sync('filters@sort', [
      'order', 
      'key'
])
```
```pathify
...sync('filters@sort', {
      sortOrder: 'order',
      sortKey: 'key'
})
```
```pathify
...sync('filters@*')
```


Set up your store – **no matter how complex** – in a single line:

```pathify
make.mutations(state)
```


And... that's it!


In practical terms, Pathify results in:

- less cognitive overhead
- zero store boilerplate
- one-liner wiring
- cleaner code
- lighter files

For a deeper insight check out the [code comparison](https://codesandbox.io/s/github/davestewart/vuex-pathify/tree/master/demo?initialpath=code) demo which illustrates a reduction Vuex code of between **2 and 14 times** (at least) depending on store size and setup.

### Next steps

To get started:

- Read the [Intro](/guide/intro.md) for an overview of the Pathify mechanism
- Visit the [Setup](/guide/setup.md) page to install and use Pathify now
- Read the [API](/api) section for a deep dive into Pathify's features

To see Pathify in action:

- Check the editable CodeSandbox [demo](https://codesandbox.io/s/github/davestewart/vuex-pathify/tree/master/demo)
