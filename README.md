## Build- & Flash-Umgebung (ab Phase 1)

Der lauffähige TFLM-Prototyp wird über die **YAHAL**-Integration des
betreuenden Professors gebaut und geflasht (nicht mehr über das
ursprünglich vendored tflite-micro in diesem Repo).

- Repository: YAHAL_with_examples (Kurs-Repo, separat ausgecheckt)
- Beispiel: `examples/rp2350-launchpad/tflite_example/`
- Board: Terstegge RP2350B LaunchPad, Flash über onboard Picoprobe (SWD)

### Setup (einmalig)
    git submodule update --init --recursive
    cd YAHAL/lib/tflite-micro && sh setup.sh   # aus Git Bash, nicht cmd

### Build & Flash
    cd examples/rp2350-launchpad/tflite_example/Build
    cmake -G "MinGW Makefiles" ..
    cmake --build .

Phase 1 verifiziert: Flash + LED-Helligkeit + serielle Ausgabe (PuTTY) OK.
