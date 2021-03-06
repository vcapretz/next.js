# Declarative State & Side-effect management with [CerebralJS](https://cerebraljs.com/)

Use [CerebralJS](https://cerebraljs.com/) to manage an apps state and side effects in a declarative manner:

Declarative CerebralJS:

```js
;[
  setLoading(true),
  getUser,
  {
    success: setUser,
    error: setError,
  },
  setLoading(false),
]
```

vs imperative JS:

```js
function getUser() {
  this.isLoading = true
  ajax
    .get('/user')
    .then(user => {
      this.data = user
      this.isLoading = false
    })
    .catch(error => {
      this.error = error
      this.isLoading = false
    })
}
```

## Deploy your own

Deploy the example using [ZEIT Now](https://zeit.co/now):

[![Deploy with ZEIT Now](https://zeit.co/button)](https://zeit.co/import/project?template=https://github.com/zeit/next.js/tree/canary/examples/with-cerebral)

## How to use

### Using `create-next-app`

Execute [`create-next-app`](https://github.com/zeit/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init) or [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) to bootstrap the example:

```bash
npm init next-app --example with-cerebral with-cerebral-app
# or
yarn create next-app --example with-cerebral with-cerebral-app
```

### Download manually

Download the example:

```bash
curl https://codeload.github.com/zeit/next.js/tar.gz/master | tar -xz --strip=2 next.js-master/examples/with-cerebral
cd with-cerebral
```

Install it and run:

```bash
npm install
npm run dev
# or
yarn
yarn dev
```

Deploy it to the cloud with [ZEIT Now](https://zeit.co/import?filter=next.js&utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).
