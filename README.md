# Reader Affect Model (Source Code)

Contains all dev-related files for the [Reader Affect Model MS thesis](https://github.com/users/addicteduser/projects/1).

## File Structure
    .
    +-- MATLAB
    +-- ReaderAffectModelProjects
    |   +-- DataCollector
    |   +-- DataPreprocessor
    |   +-- ReaderAffectModelProjects.sln

* **MATLAB** contains the MATLAB functions for extracting the features (see `EegFeaturesExtractor.m`) and building the datasets (see `BatchDataProcessor.m`, `DataProcessor.m`, and `BuildDataset.m`).
* **ReaderAffectModelProjects** is a Microsoft Visual Studio [solution](https://docs.microsoft.com/en-us/visualstudio/ide/solutions-and-projects-in-visual-studio?view=vs-2017) for data acquisition (see `/DataCollector`) and preprocessing (see `/DataPreprocessor`)

## Usage/Development

#### Data Acquisition
Build and run the `/ReaderAffectModelProjects/DataCollector` project. The output (EEG recording, emotion annotation, video recording) will be in the `/ReaderAffectModelProjects/DataCollector/Results` folder.

#### Data Preprocessing
Build and run the `/ReaderAffectModelProjects/DataPreprocessor` project. The output will be in the `/ReaderAffectModelProjects/DataPreprocessor/Results` folder.

#### Feature Extraction
Run the MATLAB `EegFeaturesExtractor()` function.

#### Build Dataset
_**DISCLAIMER:** I haven't opened this in years. I'm just trying to document the steps from memory_ 😂. I forgot what exactly each function does, but I think these are the important functions to invoke: `BatchDataProcessor()`, `DataProcessor()`, and `BuildDataset()`. `DataProcessor()` processes a single file, whereas `BatchDataProcessor()` allows you to call `DataProcessor()` for a list of files.