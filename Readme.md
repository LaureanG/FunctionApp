# Install prerequisites
- latest JDK (v21) from Oracle
- maven via choco
- Visual Studio Code and Azure Functions extension.
- Azure Functions Core Tools (https://docs.microsoft.com/azure/azure-functions/functions-run-local)

# Login to azure from VS Code
- use the Azure extension and click on Resources

# Create a Function app in Java using the steps described bellow:
https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions

# Run the function locally
- Edit the worker.config.json (using VS Code since it requires Admin privileges) from C:\Program Files\Microsoft\Azure Functions Core Tools\workers\java
- You need to change the value of defaultExecutablePath from "%JAVA_HOME%/bin/java to 
- either the absolute path of your java executable (e.g. /usr/bin/java).
    - "defaultExecutablePath": "C:\\Program Files\\Java\\jdk-21\\bin"
    - "defaultExecutablePath": "C:\\Program Files\\Common Files\\Oracle\\Java\\javapath", taken from env vars.
- or set "defaultExecutablePath": "%JAVA_HOME%", and in local.settings.json add "JAVA_HOME": "C:\\Program Files\\Java\\jdk-17\\bin"
- Start VS Code in Admin mode is not solving the issue.