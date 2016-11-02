# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Main tasks performed inside Ember Application Router:
    To coordinate view states beyond "superficial" methods like jQuery. It is
    done with different urls (examples: /index, /departments, /workers, etc)
    Main tasks performed inside an Ember Route:
    Rendering templates for the view state specified (view state for /index,
    view state for /departments, etc)
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
      {{#link-to 'campus.boston'}}Boston{{/link-to}}
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
    1. Both are nested, but the nesting is created in two different ways (ie
    with a function in the first one, specifying nested path in the second)
    2. ??
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    '/movies/:movie_id' , if I'm interpreting the question correctly.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Not sure what the question is exactly... But if I'm interpreting it
    correctly, I'd like to say that it can be rendered with an each loop in
    Handlebars.
    ```
