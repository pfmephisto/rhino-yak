# Yak packet maneger action

Publish a Rhino/Grasshopper plug-in using Yak streight from a GitHub action.

The action is curently set up as a simple composit action, but it resides in the template for a full javascript action.
The intent is to further develop the capabilities of this action over time.

## Usage

To use it simply call the following code from your github action.

```yaml
uses: pfmephisto/rhino-yak@v1
with:
  build-directory: #The directory where the compiled project files are
  version: #The version number of the current build
```
Currently I obtain the version number using `dotnet/nbgv@master` and pass it in as a variable.
Also for Yak to work the yak token must be set as an enviroment variable.
This can be done like so. If GitHub secrets are being used.
```yaml
env:
  YAK_TOKEN: ${{ secrets.GitHub_SECTRET_NAME }}
```
