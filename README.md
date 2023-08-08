# Minecraft 3dst Parser

A Minecraft: 3DS Edition 3dst Image File Parser and Assembler

## How To Use

* Download `MC3dstParser.java` from [Releases](https://github.com/BJTMastermind/MC3dst-Parser/releases) tab.
* Add the library into your project.
* Import `me.bjtmastermind.mc3dstparser.MC3dstFile` to use.

Example Code:

```java
// Create a new instance of the MC3dstFile
MC3dstFile mc3dstFile = new MC3dstFile();

// Use the parse method to parse a 3dst image
mc3dstFile.parse("/path/to/image.3dst");

// Use the replace method to replace the image in a parsed 3dst image
BufferedImage image = ImageIO.read(new File("/path/to/replacementImage.png"));
// Choose your desired ColorFormat of ABGR, BGR, or RGBA5551
mc3dstFile.replace(image, ColorFormat.ABGR); // this will override the existing 3dst image data

// Create a new 3dst image from scratch
mc3dstFile.assemble(image, ColorFormat.ABGR, "/path/to/output.3dst");
```

## Minimum Java Version

* Java 8

## 3dst File Format

* Coming Soon