# Template expansion

1. YAML files are text on disk
2. Azure Pipelines reads YAML to build an object in memory
3. When it sees `template`, that’s a new file but the same object
4. `parameters` on the template define a contract; on the consumer, define arguments
5. When it sees `${{  }}`, that switches to an expression parser
6. After templates bottom out and expressions are parsed, the final object is sent to the plan compiler.
