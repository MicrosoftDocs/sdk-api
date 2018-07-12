---
UID: NS:wingdi.tagNEWTEXTMETRICA
title: tagNEWTEXTMETRICA
author: windows-sdk-content
description: The NEWTEXTMETRIC structure contains data that describes a physical font.
old-location: gdi\newtextmetric.htm
old-project: gdi
ms.assetid: 0dd7fee0-0771-4c72-9843-0fee308da5cc
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPNEWTEXTMETRICA, *NPNEWTEXTMETRICA, *PNEWTEXTMETRICA, NEWTEXTMETRIC, NEWTEXTMETRIC structure [Windows GDI], NEWTEXTMETRICA, NEWTEXTMETRICW, PNEWTEXTMETRIC, PNEWTEXTMETRIC structure pointer [Windows GDI], _win32_NEWTEXTMETRIC_str, gdi.newtextmetric, tagNEWTEXTMETRICA, wingdi/NEWTEXTMETRIC, wingdi/NEWTEXTMETRICA, wingdi/NEWTEXTMETRICW, wingdi/PNEWTEXTMETRIC"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NEWTEXTMETRICW (Unicode) and NEWTEXTMETRICA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NEWTEXTMETRICA, *PNEWTEXTMETRICA, *NPNEWTEXTMETRICA, *LPNEWTEXTMETRICA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - NEWTEXTMETRIC
 - NEWTEXTMETRICA
 - NEWTEXTMETRICW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagNEWTEXTMETRICA structure


## -description



The <b>NEWTEXTMETRIC</b> structure contains data that describes a physical font.




## -struct-fields




### -field tmHeight

The height (ascent + descent) of characters.


### -field tmAscent

The ascent (units above the base line) of characters.


### -field tmDescent

The descent (units below the base line) of characters.


### -field tmInternalLeading

The amount of leading (space) inside the bounds set by the <b>tmHeight</b> member. Accent marks and other diacritical characters may occur in this area. The designer may set this member to zero.


### -field tmExternalLeading

The amount of extra leading (space) that the application adds between rows. Since this area is outside the font, it contains no marks and is not altered by text output calls in either OPAQUE or TRANSPARENT mode. The designer may set this member to zero.


### -field tmAveCharWidth

The average width of characters in the font (generally defined as the width of the letter x). This value does not include overhang required for bold or italic characters.


### -field tmMaxCharWidth

The width of the widest character in the font.


### -field tmWeight

The weight of the font.


### -field tmOverhang

The extra width per string that may be added to some synthesized fonts. When synthesizing some attributes, such as bold or italic, graphics device interface (GDI) or a device may have to add width to a string on both a per-character and per-string basis. For example, GDI makes a string bold by expanding the spacing of each character and overstriking by an offset value; it italicizes a font by shearing the string. In either case, there is an overhang past the basic string. For bold strings, the overhang is the distance by which the overstrike is offset. For italic strings, the overhang is the amount the top of the font is sheared past the bottom of the font.

The <b>tmOverhang</b> member enables the application to determine how much of the character width returned by a <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> function call on a single character is the actual character width and how much is the per-string extra width. The actual width is the extent minus the overhang.


### -field tmDigitizedAspectX

The horizontal aspect of the device for which the font was designed.


### -field tmDigitizedAspectY

The vertical aspect of the device for which the font was designed. The ratio of the <b>tmDigitizedAspectX</b> and <b>tmDigitizedAspectY</b> members is the aspect ratio of the device for which the font was designed.


### -field tmFirstChar

The value of the first character defined in the font.


### -field tmLastChar

The value of the last character defined in the font.


### -field tmDefaultChar

The value of the character to be substituted for characters that are not in the font.


### -field tmBreakChar

The value of the character to be used to define word breaks for text justification.


### -field tmItalic

An italic font if it is nonzero.


### -field tmUnderlined

An underlined font if it is nonzero.


### -field tmStruckOut

A strikeout font if it is nonzero.


### -field tmPitchAndFamily

The pitch and family of the selected font. The low-order bit (bit 0) specifies the pitch of the font. If it is 1, the font is variable pitch (or proportional). If it is 0, the font is fixed pitch (or monospace). Bits 1 and 2 specify the font type. If both bits are 0, the font is a raster font; if bit 1 is 1 and bit 2 is 0, the font is a vector font; if bit 1 is 0 and bit 2 is set, or if both bits are 1, the font is some other type. Bit 3 is 1 if the font is a device font; otherwise, it is 0.

The four high-order bits designate the font family. The <b>tmPitchAndFamily</b> member can be combined with the hexadecimal value 0xF0 by using the bitwise AND operator and can then be compared with the font family names for an identical match. For more information about the font families, see <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>.


### -field tmCharSet

The character set of the font.


### -field ntmFlags

Specifies whether the font is italic, underscored, outlined, bold, and so forth. May be any reasonable combination of the following values.

<table>
<tr>
<th>Bit</th>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>NTM_ITALIC</td>
<td>italic</td>
</tr>
<tr>
<td>5</td>
<td>NTM_BOLD</td>
<td>bold</td>
</tr>
<tr>
<td>8</td>
<td>NTM_REGULAR</td>
<td>regular</td>
</tr>
<tr>
<td>16</td>
<td>NTM_NONNEGATIVE_AC</td>
<td> no glyph in a font at any size has a negative A or C space.</td>
</tr>
<tr>
<td>17</td>
<td>NTM_PS_OPENTYPE</td>
<td> PostScript OpenType font</td>
</tr>
<tr>
<td>18</td>
<td>NTM_TT_OPENTYPE</td>
<td> TrueType OpenType font</td>
</tr>
<tr>
<td>19</td>
<td>NTM_MULTIPLEMASTER</td>
<td> multiple master font</td>
</tr>
<tr>
<td>20</td>
<td>NTM_TYPE1</td>
<td> Type 1 font</td>
</tr>
<tr>
<td>21</td>
<td>NTM_DSIG</td>
<td> font with a digital signature. This allows traceability and ensures that the font has been tested and is not corrupted</td>
</tr>
</table>
 


### -field ntmSizeEM

The size of the em square for the font. This value is in notional units (that is, the units for which the font was designed).


### -field ntmCellHeight

The height, in notional units, of the font. This value should be compared with the value of the <b>ntmSizeEM</b> member.


### -field ntmAvgWidth

The average width of characters in the font, in notional units. This value should be compared with the value of the <b>ntmSizeEM</b> member.


## -remarks



The last four members of the <b>NEWTEXTMETRIC</b> structure are not included in the <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a> structure; in all other respects, the structures are identical.

The sizes in the <b>NEWTEXTMETRIC</b> structure are typically specified in logical units; that is, they depend on the current mapping mode of the display context.




## -see-also




<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>
 

 

