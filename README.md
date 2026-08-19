# CysTerra Message Repository
CysTerra is a universal geohazard information platform that fetches information related to earthquakes, tsunamis, volcanoes, etc. from various event sources, and combines them into a unified interface with text description, map representation, and text-to-speech output.

This is the message repository of CysTerra, containing the localized strings used in the project.

If you simply want to use the app, please visit the [project page](https://www.cryville.world/Projects/A017) instead.

If you want to learn about extension development, please refer to the [CysTerra extension development documentation](https://docs.eew.cryville.world/).

## Repository Structure
- [`Cryville.EEW.Android.Messages`](Cryville.EEW.Android.Messages) contains the messages for the Android build.
- [`Cryville.EEW.Core.Messages`](Cryville.EEW.Core.Messages) contains all the other messages.
  
  This directory used to contain messages for all the event source implementations. As the implementations are refactored to extensions, these messages were moved into the corresponding project directory of their extensions. See the [`Extensions` directory in the public repository](https://github.com/cryville/CysTerra.Public/tree/main/Extensions) for these messages.

## Contribution Guide
Contributions are welcomed. You are free to fork this repository and make changes.

> [!TIP]
> Messages for our extensions are located in the [public repository](https://github.com/cryville/CysTerra.Public). To translate them, make pull requests there instead.

To create translations to a new language, duplicate an existing message `.json` file and change the file name to the BCP 47 language tag of the target language. Inside the JSON, set the `Culture` field to that language tag as well, and then start translating all the JSON values. Do not change any key unless specified.

You can also review existing strings and propose changes. Create a pull request when you are done.

Please prioritize the translations for the following directories:

- `Cryville.EEW.Core.Messages/Cryville.EEW.Core`
- `Cryville.EEW.Core.Messages/Cryville.EEW.Avalonia`
- `Cryville.EEW.Core.Messages/Cryville.EEW.FERegion`
- `Cryville.EEW.Core.Messages/Cryville.EEW.Measure`
- `Cryville.EEW.Core.Messages/Cryville.EEW.TaggedProperties`

Strings in other directories are to be deprecated or to be moved to elsewhere soon. Translating them are not recommended at the moment.
