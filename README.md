# TypeScriptBuildIssueDemo

Issue: a Razor Class Library with TypeScript files does not consistently build successfully in .NET 9+

# Reproduction Steps
1. Clone the repository.
2. Open the solution in Visual Studio 2022 or later.
3. Build the solution or main project (Blazor app `TypeScriptBuildIssueDemo`).
4. Right-click and Re-build the solution or main project.

You should see the build failing alternating times with the following error:

```
System.InvalidOperationException: No file exists for the asset at either location 'D:\TypeScriptBuildIssueDemo\TypeScriptBuildIssueDemo.Library\wwwroot\js\app.js' or 'wwwroot\js\app.js'.
   at Microsoft.AspNetCore.StaticWebAssets.Tasks.StaticWebAsset.ResolveFile(String identity, String originalItemSpec)
   at Microsoft.AspNetCore.StaticWebAssets.Tasks.DefineStaticWebAssets.ResolveFileDetails(String originalItemSpec, String identity)
   at Microsoft.AspNetCore.StaticWebAssets.Tasks.DefineStaticWebAssets.Execute()
```