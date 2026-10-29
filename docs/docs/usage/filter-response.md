# Filter response with JQ

## With `# @jq` directive

You can use `# @jq` directive to filter the response JSON.

```http
# @jq { "username": .username, "password": .password }
POST https://httpbin.org/post HTTP/1.1
Content-Type: application/json

{
  "username": "{{USERNAME}}",
  "password": "{{PASSWORD}}",
}
```

## Manually in the response buffer

Press `F` to edit the JQ filter via the input prompt, prefilled with the current filter (if any).

Enter a [jq](https://jqlang.github.io/jq/manual/) query to apply it, or leave it empty and submit to remove the filter and show the unfiltered body.
