# DataOps Challenge
Star wars posters

## Recommended Tools
Language(s) of choice
github.com - please name repo `poster-kata`
travis-ci - this has a build system and you can run your tests/docker in its runtime to demonstrate your work.
PostgresQL - (any SQL based db that you can get going in a docker container.)

## Instructions
We want for you to show how to automate pulling data from two sources to get a merged view of the data.

You should use docker/docker-compose to create your fake customer database (named `source`), and a separate merged database (named `dw`).  You will use data from the https://swapi.co/ API as well, to lookup missing product information and filter out certain kinds of items.

### Columns for source
poster_content | string | "Millennium Falcon"
quantity | int | 7
price | decimal | 2.9
email | string | "sally_skywalker@gmail.com"
sales_rep | string | "tej@swposters.com"
promo_code | string | "radio"

We will be looking for realistic looking data and automation around its generation.

### Requirements for dw
Please extract, transform, then load (ETL) the data into the `dw` database with the following requirements in mind:

• "We only care about starship posters, though we sell starship, charactor and planet posters"
• "We need to know which films the ship appears in and when the film was made to understand potential demographic correlations."
• "We want to be able to summarize the data."
• "Customer emails should never be ingested."
• "We only want to ingest data relevant to our mission."