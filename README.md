### Description

`split_segy_by_turns` will split a SEG-Y file based on the rate of turning.
Turns are identified by calculating the running turning radius, very short lines
are merged with the adjacent lines.
Trace headers and samples in the output files are preserved.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jonnyford/turn-detection
   cd turn-detection
   ```
2. Install Python dependencies
   ```sh
   pip install -r requirements.txt
   ```
3. Make script executable (probably not necessary)
   ```sh
   chmod +x split_segy_by_turns
   ```

### Usage

```sh
./split_segy_by_turns --dry-run Line1.sgy Line2.sgy Line3.sgy
```
or
```sh
./split_segy_by_turns --dry-run Line*.sgy
```
The `--dry-run` flag will output some information about the split lines but will not
write the new SEG-Ys. Removing this flag will write the SEG-Ys.

Some helpful parameters to tune can be found in `./split_segy_by_turns --help`.