# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    When you first load a page, the router matches the URL to the route defined
    by the user. Use a model hook to load the appropriate model to draw
    information from.

    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
  {{#link-to '/campus/boston' }}Boston Campus{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    1) The first route definition's path leads directly to an individual product
    by its id. While the second path includes the products page and a product's
    individual id.
    2) I am not 100% confident that the first route's path will lead anywhere,
    while the second route's path seems uniform to how we have learned about
    paths in ember route definitions.
    3) The first route definition is nested and the second is not.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md

movie.id

    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Handlebars expression. {{data-name}}.
    ```
