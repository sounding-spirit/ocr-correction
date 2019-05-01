# About
This repository holds scripts for working with [ALTO XML files](https://www.loc.gov/standards/alto/).

The `alto_to_editable.xsl` script takes an ALTO file and, for each String element, copies the value of the CONTENT attribute and inserts it into the String element. It also places a CSS stylesheet reference to `alto-style.css`. This creates a file that can be more easily edited using [Oxygen XML Editor's Author Mode](https://www.oxygenxml.com/doc/versions/21.0/ug-editor/topics/editing-xml-documents-author.html).

The `editable_to_alto.xsl` script returns the editable files to the ALTO format.

## Usage
`java -jar saxon9he.jar -s:/path/to/ALTO_files_directory -o:/path/to/editable_files_directory -xsl:alto_to_editable.xsl`

`java -jar saxon9he.jar -s:/path/to/editable_files_directory -o:/path/to/ALTO_files_directory -xsl:editable_to_alto.xsl`
