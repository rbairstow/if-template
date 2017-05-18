# If template
Within your theme you might need to add some custom content to a product form but only for selected products.
It is easy to set this up using liquid

1. Start by creating a custom product template and give it the name: custom
2. Edit your product-form.liquid or short-form.liquid ( depending on your theme ) to include:

```html
{% if product.template_suffix == 'custom' %}
   add some custom code
{% endif %}
```
Note the usage of 'custom' this is the suffix of the product template that you have just created.
If you had named the template: my-new-template then you would instead add:  'my-new-template'

This will then only show that code to a product that is using this particular template.
