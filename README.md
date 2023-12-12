# The scenario is not properly defined

The current issue is the result of the webassembly incorrectly using a type in a lazy loaded assembly before it is loaded.

There is already an enhancement tracking loading lazy assemblies during startup when they've been rendered on the server, but it's the app responsibility to get this right.

Counter.razor includes changes to demonstrate loading the assembly and delaying the rendering of the component until the assembly is loaded.

https://github.com/dotnet/aspnetcore/issues/26601