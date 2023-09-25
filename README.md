# Hullabalook Technical Assessment

You are provided with a set of products and are required to create a products listing page for a footwear retailer.

Write functionality and styling to:

- Lay out all products in a responsive product grid
- Create a filter toggle that shows only available products
- Create a checkbox brand filter that shows only toggled brand products
- Add a counter for the number of resulting products
- Create a dropdown to sort all products into ascending or descending price order
- Add an option to sort all products by relevance - with all available products shown first in ascending rank order, then all unavailable products in ascending rank order.

You will be assessed on both behaviour and design. Don't spend more than 2 hours on this.

## Instructions

To start, fork [this](https://stackblitz.com/edit/vue-hulla-ta) project and set the project name to include your name. When you're finished, connect this to your GitHub account, push the changes and email the links to the repo and this project back to us.

If you wish to continue past the allocated time, please create another fork.

# design

Here's my design decisions for this PLP:

- Lay out all products in a responsive product grid

  - use grid in to render the items in a grid
    - added a basic grid style

- Mutate a computed products array

  - Create a filter toggle that shows only available products

    - filter method removes any products with stock less than zero

  - Create a checkbox brand filter that shows only toggled brand products

    - filter method shows only checked brand products

  - Create a dropdown to sort all products into ascending or descending price order

    - select box sorts according to price or reverse
      - sort method should also reset the relevance value so the price sort can still be used after sort by relevance is set

  - Add an option to sort all products by relevance - with all available products shown first in ascending rank order, then all unavailable products in ascending rank order.
    - sort by relevance button
      - method sortByRelevance
        - filter the products objects and iterate available/not

- Add a counter for the number of resulting products
  - counter for length of products rendered alongside the Filters tag

Depending on the application, this could be modified to work with v-show. It might be more responsive than iterating through the whole product list every time a filter is applied.

Given more time i'd style the filters bar to scroll with the page and render in line for UX
