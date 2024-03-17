# OpenClino - Open-source 3D clinostat

Open-source 3D clinostat. A clinostat is a small scale [microgravity simulator](https://en.wikipedia.org/wiki/Random_positioning_machine).

![Clinostat cad!](docs/images/openclino_cad.gif "cadModel")
![Clinostat real!](docs/images/openclino_real.gif "realBuilt")

This is based on the European Space Agency's work, specifically on [Jack Van Loon's clinorotation work](https://doi.org/10.3389/fpls.2019.01577).

I have provided 3d print files, arduino, and raspberry pi-code. This is a side project for me and is very much work in progress.
It is very difficult to access a 3D clinostat, there are some companies that sell it but can be prohibitively expensive for gravity research. OpenClino can be built for £100 using off the shelf parts. OpenClino can run in continuous clinorotation or as a Random Positioning Machine (RPM).

OpenClino is designed to be simple, accessible, affordable, and **reliable**. It is designed to make use of 3D printing's strengths and requires *no machining* and minimum tools. To build OpenClino all non-printed parts are available off the shelf, mainly 3d printer stepper motors, belts, controllers, and skateboard bearings. All these parts are rated for thousands of hours of operation, and I have fully tested OpenClino to run for a minimum of 100 hrs without fault.

## Documentation

<img src="docs/images/build_guide/0_exploded_view.jpg" alt="Clinostat build!" width="400"/>

I have provided:
- Docs in [`docs/1_.md/`](docs/1_documentation.md)
- Code in [`src/`](src/clinostat.ino)
- 3D print files as .3MF in [`3d_files/`](3d_files/)
- Bill of materials in [`docs/2_BOM.md/`](docs/2_BOM.md/)
- Build guide in [`docs/3_build_guide.md/`](docs/3_build_guide.md/)

I will provide (TODO):

- code documentation.


## Usage

To run in clinorotation mode simply add these to your arduino's loop function, this will run the x axis at 30 rpm and the y axis at 60:

```cpp
void loop() {
    spin_continuous(30,60);
}
```

Or to run as a random positioning machine, this will run a random walk routine as specified in ESA's work:


```cpp
void loop() {
    RPM();
}
```

Don't forget to set the output pins for you motor controllers!

## Collaboration

Please contact me on LinkedIn or raise an issue.

I would be happy to collaborate on this.

## Contributors

[@dragomda](https://github.com/dragomda)
