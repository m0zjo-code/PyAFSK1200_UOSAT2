# PyAFSK1200 - UOSAT2 Decoder

This is a quick n' dirty decoder for UOSAT2. This has been used with files from the SATNOGS project -->> [SATNOGS](https://network.satnogs.org)

## Installation and Usage

Clone the repo and run as follows:
```bash
py afsk1200decode.py -i <input wav> -o <processing id>
```

### Dependencies

- Numpy
- Scipy
- Matplotlib
- wavio

These can be installed using PIP

### Example

An example can be run using the included example file (this SATNOGS UOSAT2 observation here -->> [https://network.satnogs.org/observations/1505004/](https://network.satnogs.org/observations/1505004/))
```bash
py afsk1200decode.py -i satnogs_1505004_2020-01-07T12-42-50.wav -o UOSAT_Data
```

To use other SATNOGS observations, you'll need to convert the file to a WAV file. This can be done using your preferred audio maipulation program but I use SoX -->> [http://sox.sourceforge.net/Main/HomePage](http://sox.sourceforge.net/Main/HomePage)

A text file is output with the decoded data, an example data frame can be seen here:
```
---Record Separator---
UOSAT-2           1.02104083325
000000010001020002030003040004050005060006070007080008090009
100001110000120003130002140005150004160007170006180009190008
20000221000322000023000124000625000726000427000528000A29000B
30000331000232000133000034000735000636000537000438000B39000A
40000441000542000643000744000045000146000247000348000C49000D
50000551000452000753000654000155000056000357000258000D59000C
60800E615FC1620105633305644402651E0C66200267000168000E69000F
---Record Separator---
```
Unfortunately most of the telemetry channels are returning zeros, there are a few that appear to be working though.

## License
[MIT](https://choosealicense.com/licenses/mit/)
