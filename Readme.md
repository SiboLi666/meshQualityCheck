### Mesh Quality Check ###

*  The meshQuality function object can be used to write different mesh quality fields as volScalarFields or surfaceScalarFields to help analysis the mesh quality in paraview.

## Compilation ##

To build it, use the following command:
```bash
wmake libso
```

## Usage ##
To use the function object, you can go to any OpenFOAM case (a mesh has to be available) and run:

```bash
postProcess -func meshQuality
```

If you get a message that the meshQuality dict is not found you have to create it manually. For that we first copy an existing one:

```bash
foamGet age
```

Now open the file (`system/age`) and change the type to `meshQuality` and remove the `nCorr` entry. Finally, rename the file

```bash
mv system/age system/meshQuality
```



