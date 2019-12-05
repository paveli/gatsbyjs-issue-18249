# GatsbyJS issue 18249 reproduction

This is a set up to reproduce GatsbyJS [isssue #18249](https://github.com/gatsbyjs/gatsby/issues/18249).
It is a simple gatsby starter with `gatsby-source-shopify` included.
The set up is made with a Public App [Storefront Access Token](https://help.shopify.com/en/api/reference/access/storefrontaccesstoken)

Test store has several pages created on Shopify side.

```
https://storefrontify.com/pages/test-page
https://storefrontify.com/pages/second-test-page
```

To reproduce the issue please clone the repo, install the dependencies and run gatsby.

```
git clone https://github.com/paveli/gatsbyjs-issue-18249.git
yarn install
gatsby develop
```

Go to http://localhost:8000/___graphql to see that allShopifyPage was not created.

Storefront Access Token info:

```
{
  "storefront_access_tokens": [
    {
      "access_token": "73fc00421a7a3809a2b4fa2d7cc4aaf5",
      "access_scope": "unauthenticated_read_content,unauthenticated_read_product_tags,unauthenticated_read_product_listings,unauthenticated_read_collection_listings,unauthenticated_write_checkouts,unauthenticated_read_checkouts,unauthenticated_write_customers,unauthenticated_read_customers",
      "created_at": "2019-10-08T04:46:48-04:00",
      "id": 31477039188,
      "admin_graphql_api_id": "gid://shopify/StorefrontAccessToken/31477039188",
      "title": "Gatsby Storefront Access Token"
    }
  ]
}
```
