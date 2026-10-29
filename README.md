

## Important .gen compatibility note

The supplied binary `.gen` file is not a NAM JSON model. NeuralAmpModelerCore does not define a universal decoder for arbitrary `.gen` extensions. This project keeps the explicit rejection path rather than falsely reporting a successful load. To implement a real decoder, the generating application and its documented file format or redistributable SDK are required.


## FIXED46 model loader and defaults

- PEAK REDUCTION parameter default is 25.0; GAIN remains 50.0.
- `.nam` files are parsed as UTF-8 JSON and passed to NeuralAmpModelerCore using its JSON configuration loader. The loader validates the NAM document fields before Core construction.
- Runtime loading still needs validation in the Windows GitHub Actions build and a DAW. No successful runtime claim is made until that test is run.
