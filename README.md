# `api` GraphQL API Server

Based on the provided GraphQL schema, the `api` API server is structured to handle specific queries and mutations related to caching operations. Here's an updated overview and usage guide considering this GraphQL implementation.

## Overview

**The `api` is a GraphQL API server** for a file-based caching system. It enables clients to interact with a caching mechanism through GraphQL queries and mutations. This system uses *Apollo Server* for handling GraphQL requests and is ideal for applications that require efficient, file-based data caching with the ease and flexibility of GraphQL.

## GraphQL Schema

The GraphQL schema defines the following operations:

### Queries

- **get**: Retrieve a value from the cache by its key.
  - `key`: The unique identifier for the cache entry.

### Mutations

- **set**: Add a new entry to the cache or update an existing one.
  - `key`: The unique identifier for the cache entry.
  - `value`: The data to be stored in the cache.
  - `ttl`: Time-to-live (in seconds) for the cache entry.
- **delete**: Remove an entry from the cache.
  - `key`: The unique identifier for the cache entry to be deleted.
- **clear**: Remove all entries from the cache.

## Usage

Clients can interact with the caching system using GraphQL operations. Here are some examples:

### Set Cache Entry

To set a cache entry:

``` graphql
mutation {
  set(key: "user1", value: "John Doe", ttl: 3600)
}
```

## Getting Started
To utilize this GraphQL-based caching system, follow the setup instructions in the README. Ensure you have Apollo Server and other dependencies installed.

## Contribution
If you wish to contribute to enhancing the GraphQL schema or other aspects of this project, please adhere to the contribution guidelines.

