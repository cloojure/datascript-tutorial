## CRUD

How can we achieve something akin to *CRUD* with Datomic/Datascript?

The *Pull API* looks to be perfect for simple CRUD-like queries.

We can easily get one or more entities with specific attributes as a high performant batch query (using indexes).

### Create

Uses so called "upserts" by default, ie. facts are created or updated as needed automatically. An "update" is simply a new commit with an add (create).

### Update

See "upserts" for Create.

### Delete

Use `retract`

### Read

Pull API for most cases. Queries for advanced queries, such as aggregation.
Combination!?