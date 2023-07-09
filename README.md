# KiCAD Library

This repository contains a library for KiCAD 7 that includes 3D models, Footprints, and Symbols.

## Repository Structure

The repository is organized as follows:

- 3D Models: Contains all the certified 3D models for components.
- Footprints: Contains the Footprints.pretty file which has all the certified footprints.
- Symbols: Contains the Symbols.kicad_sym file which has all the certified symbols.

## Symbols

All symbols are stored in the `Symbols.kicad_sym` file. You can add new symbols to this library either manually using a text editor or within KiCAD itself.

Each symbol in the library should have the following fields:

- Value: A friendly name for the symbol. For passive components, please include the current and/or voltage rating.
- Footprint: The path to the local project Footprints library where the footprint of the component is stored.
- Datasheet: Download and place the datasheet of the component in the root of the repository's datasheet folder.
- Cost USD Qty 1: An estimate of the component's cost when purchased as a single unit.
- Cost USD Qty 1000+: An estimate of the component's cost when purchased in quantities of 1000 or more.
- Manufacturer Part Number
- Digi-Key Part Number
- LCSC Part Number
- Symbol Name
- Description

## Footprints

Footprints are stored in the `Footprints.pretty` file found in the Footprints folder. If a 3D model is available for a footprint, make sure you have mapped it and placed the model in the 3D Models folder.

All path mapping should be done at the project level using the `{KIPRJMOD}` path variable to ensure compatibility with all user environments.

## Usage

Feel free to use this library for your projects. You may also import other libraries from sources such as SnapEDA and Ultra-Librarian for your design needs. However, there's no need to merge these imported libraries with our library while you're working on your design.

Once you're done with your project, please go back and merge any new symbols and footprints that you've created with our library. Make sure that all additions end up in the `Symbols.kicad_sym` file so it remains as a single, comprehensive library.

After merging locally, please commit your changes to a dev branch and submit a pull request. We'll review your changes and merge them with the master branch once everything is verified.

## Contribution

This repository is intended to be used as a submodule of the KiCAD Template Repository. The following guide will help you understand how to add, pull, and contribute to a submodule.

### Adding the Submodule

To add this library as a submodule in your KiCAD Template Repository, navigate to the root directory of your repository and run:

```sh
git submodule add https://github.com/ShirkyBooi/CreateKiCADProject
```

### Updating the Submodule

To pull the latest changes from the submodule, navigate to the root directory of your repository and run:

```sh
git submodule update --remote --merge
```

This command will fetch the latest changes from the library repository and merge them into your local copy.
