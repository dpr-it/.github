## Hi there 👋

## To Publish a applicaiton/microtool to the launcher:

paste this into your repo's github actions

```yml
name: Publish microtool
on:
  push:
    tags: ['v*.*.*']
  workflow_dispatch:

jobs:
  publish:
    uses: dpr-it/.github/.github/workflows/publish-microtool.yml@main
    with:
      app_id: **my-tool-id**
      app_name: **My Tool Name**
      description: **What the tool does.**
      executable_path: **My Tool Name.exe**
      owner: **DPR VDC**
      spec_file: my_tool.spec
    secrets: inherit
```
