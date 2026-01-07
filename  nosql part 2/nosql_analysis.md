# NoSQL Analysis

## Section A: Limitations of RDBMS

Relational databases work best when data follows a fixed and well-defined schema. In a product catalog where products have different attributes, such as laptops having RAM and processor details while shoes have size and color, an RDBMS struggles because all records must conform to the same table structure. This leads to many unused or NULL columns or requires creating multiple tables and complex joins.

Frequent schema changes are another challenge. Adding new product types often requires ALTER TABLE operations, which can be time-consuming and risky in production systems. These changes may also affect existing queries and applications.

RDBMS → Structured, table-based, strict rules
MongoDB → Flexible, document-based, modern apps

Storing customer reviews as nested data is also inefficient in RDBMS. Reviews usually require separate tables and joins, increasing query complexity and reducing performance when fetching product details along with reviews.



## Section B: NoSQL Benefits

MongoDB solves these problems by using a flexible, document-based schema. Each product can store only the attributes relevant to it, allowing laptops and shoes to coexist in the same collection without unused fields. New product types can be added without modifying existing documents or schemas.

MongoDB supports embedded documents, making it easy to store customer reviews directly inside product documents. This improves read performance and simplifies data retrieval since product and review data can be fetched together.

Additionally, MongoDB provides horizontal scalability through sharding. It can easily handle growing product catalogs and high traffic by distributing data across multiple servers.



## Section C: Trade-offs

One disadvantage of using MongoDB instead of MySQL is weaker support for complex joins and relational queries. This makes MongoDB less suitable for applications that rely heavily on multi-table relationships.

Another drawback is data consistency. While MongoDB supports transactions, relational databases like MySQL provide stronger ACID guarantees by default, making them more reliable for highly transactional systems.
