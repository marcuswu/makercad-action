# makercad-action

To use this action, create a workflow yaml including the following step (modifying the entry point for your project as necessary):

```yaml
    - uses: marcuswu/makercad-action@v4
      with:
        entry: 'main.go'
```

If the project exports any models, you can upload artifacts using a step something like this:

```yaml
    - name: Collect build artifacts
      uses: actions/upload-artifact@v4
      with:
        name: model-exports
        path: |
          *.stl
          *.step
```
