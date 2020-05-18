# PDF to PDF/A converter

Guide and script for conversion PDF to PDF/A

## Prerequisites

In order to make the script work the following two packages are needed:

* pdftops (poppler package)
* gs (ghostscript package)

## Installation

### Check

Check if both commands are already installed trying:

* `pdftops -v`
* `gs -v`

Both commands should give version and copyright. If the fail, go to installation guide.

### Linux installation

Use your favorite package distribution tool to install poppler-utils (in some distribution named simply poppler) and ghostscript.

For Debian distributions:

```
apt install -y poppler-utils ghostscript
```

### MacOS installation

Install `brew` CLI (HomeBrew https://brew.sh/index_it), then launch:

```
brew install poppler
brew install ghostscript
```

### Verify

After installation verify existence and installations of commands, as in "Check" section above.

## Execution permissions

Give execution permissions for script:

```
chmod 777 convert_pdf.sh
```


## Script quick usage

Move the script in same folder of file to be converted.

Open the terminal and launch:

```
./convert_pdf.sh <filename>.pdf
```

The result will be the presence of two new files:

* `<filename>.ps` # PostScript file created during process
* `<filename>_a.pdf` # PDF/A wanted file

## Script global usage

Move script to local bin folder:

```
cp convert_pdf.sh /usr/local/bin/convert_pdf
```

After this copy, the command `convert_pdf` will be available in terminal. So in any folder it is possible to run:

```
convert_pdf <filename>.pdf
```

The result will be the same as before.
