# @pnp/graph/sites

The search module allows you to access the Microsoft Graph Sites API.

[![Selective Imports Banner](https://img.shields.io/badge/Selective%20Imports-informational.svg)](../concepts/selective-imports.md)  

## Call graph.sites

```TypeScript
import { graphfi } from "@pnp/graph";
import "@pnp/graph/sites";

const graph = graphfi(...);

const sitesInfo = await graph.sites();
```

## Call graph.sites.getById

```TypeScript
import { graphfi } from "@pnp/graph";
import "@pnp/graph/sites";

const graph = graphfi(...);

const siteInfo = await graph.sites.getById("{site identifier}")();
```

## Make additional calls

We don't currently implement all of the available options in graph for sites, rather focusing on the sp library. While we do accept PRs to add functionality, you can also make calls by path:

### Get list items

```TypeScript
import { Site } from "@pnp/graph/sites";

const sites = graph.sites.getById("{site id}");

const users = await Site(sites, "lists/{listid}/items")();
```

### Get File/Item version information

```TypeScript
import { Site } from "@pnp/graph/sites";

const sites = graph.sites.getById("{site id}");

const users = await Site(sites, "lists/{listid}/items/{item id}/versions")();
```
