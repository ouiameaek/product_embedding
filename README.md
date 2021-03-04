# Product Embedding for Retail

🚧 Blog post in the works

### Intro

In this project, we would like to lean semantic representations (**embeddings**) for products (and eventually customers, or any other "abstraction" that can be derived from product vectors). The *product* here is a reference to retail use cases, but it can be anything, [Spotify does it for songs](https://read.hyperight.com/how-spotify-knows-what-music-you-like-hint-with-machine-learning/) for example.

These embeddings can be used for many purposes:

- features in  models to improve the accuracy of scores and recommendations
- cluster and analyze embeddings to gain insights into the semantics of customer behavior
- perform other analytics that use embeddings to measure the proximity between products and customers etc.

We will be exploring an NLP inspired method (**word2vec**) to do it, where a *document* <=> **user** and *word* <=> **product**. Here, we represent a **user** with the list of the product they purchased.

The data needed to reproduce this "analysis" for your use case is:
 
* user products : Dataset with user product interactions:
 
| user_id       | product_id    |
| ------------- |:-------------:|
| 1             | 12783,16311,12771,19677 |
 
 where **product_id** is comma separated values of the product ids you'd like to embed

* product information : Dataset with details about products, whatever you have on your data base. Here, for instance, we have information about the sports associated to the products.
 
| product_id       | product_label    | sport_id    | sport_label    |
| ---------------- |:----------------:|:-----------:|:--------------:|
| 12783            | socks | 30 | tennis |

*PS : The data used in this project is not available for public use*

Main notebooks so far : `product2vec_v0.ipynb`

### Next steps:

- Explore adding adding meta data
- Explore customer2vec

### Appendix

Inspiration [article](https://blog.griddynamics.com/customer2vec-representation-learning-and-automl-for-customer-analytics-and-personalization/) (very interesting)
