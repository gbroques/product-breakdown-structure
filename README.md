# Product Breakdown Structure

[Product Breakdown Structure (PBS)](https://en.wikipedia.org/wiki/Product_breakdown_structure) is a hierarchical numbering system detailing the components of a machine.

Given this numbering system, analytics can be derived which helps teams work together in a [Work Breakdown Structure (WBS)](https://en.wikipedia.org/wiki/Work_breakdown_structure). For example, determining the total number of parts and assemblies; as well as progress of their completion.

## Marble Machine Scheme

The following PBS numbering scheme was used by [Martin Molin](https://en.wikipedia.org/wiki/Martin_Molin), Swedish member of the [Wintergarten](https://en.wikipedia.org/wiki/Wintergatan) band, for the Marble Machine X.

A PBS number consists of a two-part six digit number in the form:

    [0-9A-Z]{3}-[0-9A-Z]{3}

The first three digits describe the assembly:

1. 1st digit - Top-level assembly
2. 2nd digit - Main assembly
3. 3rd digit - Sub-assembly

While the last three digits describe the part.

Depending on how many assemblies and parts exist, then you may include characters from the alphabet. For example, A = 10 (see [Base36](https://en.wikipedia.org/wiki/Base36)).

Assembly numbers always end with triple zeros, and part numbers end with digits.

For example, #110-000 is an assembly and #110-001 is a part.

|PBS Number|Name|
|---|---|
|#000-000|Marble Machine X|
|#100-000|Base|
|#110-000|Base Frame|
|#110-001|Front|
|#110-001|Back|

Top-level assemblies of the Marble Machine X are:

1. #100-000 - Base
2. #200-000 - Mid section
3. #300-000 - Top section
4. #400-000 - Instruments
5. #500-000 - Sides

Note, #000-000 is reserved to refer to the overall machine or root-level.

In the above scheme, the maximum levels of hierarchy and number of parts is fixed.

**Source:** [How to Organize Your Project with a PBS System - Marble Machine X #57](https://www.youtube.com/watch?v=zVyEsMiwvVc)

## Applying to FreeCAD

FreeCAD [object names](https://wiki.freecadweb.org/Object_name), and hence document names, have the following restrictions:

1. the `Name` can only include simple alphanumeric characters, and the underscore, `[_0-9a-zA-Z]`
2. the `Name` cannot start with a number; it must start with a letter or the underscore, `[_a-zA-Z]`
3. and the `Name` must be unique.

Thus, one scheme to convert the #110-001 Front part number and name to a FreeCAD document name could be:

    N_110_001_Front
