# Andheim

## GameCI

### Environment Variables

The following variables are required to configure build automation with GameCI:

> UNITY_LICENSE  
> UNITY_EMAIL  
> UNITY_PASSWORD  

In order to obtain `UNITY_LICENSE` please follow the directions at <https://game.ci/docs/github/activation>.

### Notes

In GitHub project settings, grant your runner Read/Write permissions.

Add these lines to the `.gitignore`:

```yaml
# GameCI
/[Aa]rtifacts/
/[Cc]odeCoverage/
```

In Unity, disable `Compression Format` under `Player Settings -> WebGL -> Publishing Settings`.  This substantially improves build times (`40mins -> 5mins`). To verify this change was successful, you can check `ProjectSettings.asset` for the line `webGLCompressionFormat: 2`.

In Unity, enable `Run In Background` under `Player Settings -> WebGL -> Resolution and Presentation`. To verify this change was successful you can check `ProjectSettings.asset` for the line `runInBackground: 1`.
