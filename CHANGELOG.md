## 3.2.0

- **(BREAKING CHANGE)** renamed `PosListComponent` to `PosList`
- add new `PosDelegate`

## 3.1.0

- add new `PosListComponent`
- fix bug on `CapabilityProfile` where path to `capabilities.json` was "wrong"
- move `gbk_codec` to `src` folder

## 3.0.0

- add declarative-style classes
- refactor `Generator`

## 2.0.1+6

- pre-cache capabilities

## 2.0.1+5

- add paper size mm72 by keep mm80 as 576

## 2.0.1+4

- change paper size width back from 576 to 558

## 2.0.1+3

- change paper size width from 372 to 384 and 558 to 576

## 2.0.1+2

- hotfix resource

## 2.0.1+1

- hotfix resource

## 2.0.1

- included gbk_codec directly

## 2.0.0

- nullable implemented

## 1.0.0

- `Ticket` class replaced by `Generator`.
- New code generation concept: Unlike `Ticket`, each method returns corresponding command's byte code

## 0.4.9

- Xprinter profile: added cp1258 (vietnamese)

## 0.4.8

- Replace some non-ascii characters

## 0.4.7

- Printing a long text col splits the data to the next row (case when col contains chinese characters taking 2 bytes)

## 0.4.6

- Bug fix: printing a long text col splits the data to the next row
- Ticket class : added named parameter `spaceBetweenRows`

## 0.4.5

- Updated example and README (using CapabilityProfiles)

## 0.4.4

- Setting code page before printing to support some printer models

## 0.4.3

- Set Kanji mode 0ff before setting a code page to support some printer models

## 0.4.2

- Update printer profiles

## 0.4.1

- Using flutter assets to load capabilities.json

## 0.4.0

- PosCodeTable replaced by CapabilitiesProfile

## 0.3.7

- Fixed merged text on some printers when using chinese + latin together in one string

## 0.3.6

- Print QR Codes using native function

## 0.3.5

- Added `Ticket.setGlobalFont` method
- `Ticket.codeTable` renamed to `Ticket.printCodeTable`
- Added `maxCharsPerLine` custom config + default values depending on current font and ticket size
- Code refactoring

## 0.3.4

- Added hr method
- Updated commands (using hex codes)
- setStyles bug fix

## 0.3.3

- Slow printing issue on some printer models fixed

## 0.3.2

- `PosColumn` can contain encoded text (`textEncoded` field)
- Bug fix: Columns with `PosTextSize` > `size1`
- Added Barcode Code128
- Added new code pages
- `imageRaster` bug fixed
- Ticket bytecode optimization: do not generate align left command (it's a default value)
- Added new image print function: `GS ( L`

## 0.3.1

- Added Open cash drawer command

## 0.3.0

- Image alignment (left, center, right). Align center by default.
- Barcode alignment (left, center, right). Align center by default.
- `PosTextAlign` renamed to `PosAlign`

## 0.2.0

- `Ticket._text` function takes an Uint8List of bytes instead of a String
- `Ticket._text` function refactored: removed styling commands when it's unnecessary which makes ticket's final byte code much shorter
- `PosCodeTable`: private constructor replaced by public one to allow passing custom code table code
- `PosCodeTable`: added new predefined code tables
- Added `Ticket.textEncoded` function taking Uint8List textBytes (encoded text) to support different languages

## 0.1.0 - 0.1.2

- Initial release
