---
UID: NS:wingdi._OUTLINETEXTMETRICA
title: OUTLINETEXTMETRICA (wingdi.h)
description: The OUTLINETEXTMETRIC structure contains metrics describing a TrueType font. (ANSI)
helpviewer_keywords: ["*LPOUTLINETEXTMETRICA","*NPOUTLINETEXTMETRICA","*POUTLINETEXTMETRICA","OUTLINETEXTMETRIC","OUTLINETEXTMETRIC structure [Windows GDI]","OUTLINETEXTMETRICA","OUTLINETEXTMETRICW","POUTLINETEXTMETRIC","POUTLINETEXTMETRIC structure pointer [Windows GDI]","_win32_OUTLINETEXTMETRIC_str","gdi.outlinetextmetric","wingdi/OUTLINETEXTMETRIC","wingdi/OUTLINETEXTMETRICA","wingdi/OUTLINETEXTMETRICW","wingdi/POUTLINETEXTMETRIC"]
old-location: gdi\outlinetextmetric.htm
tech.root: gdi
ms.assetid: 79d77df0-193a-49a8-b93d-4ef5807c3c9b
ms.date: 12/05/2018
ms.keywords: '*LPOUTLINETEXTMETRICA, *NPOUTLINETEXTMETRICA, *POUTLINETEXTMETRICA, OUTLINETEXTMETRIC, OUTLINETEXTMETRIC structure [Windows GDI], OUTLINETEXTMETRICA, OUTLINETEXTMETRICW, POUTLINETEXTMETRIC, POUTLINETEXTMETRIC structure pointer [Windows GDI], _win32_OUTLINETEXTMETRIC_str, gdi.outlinetextmetric, wingdi/OUTLINETEXTMETRIC, wingdi/OUTLINETEXTMETRICA, wingdi/OUTLINETEXTMETRICW, wingdi/POUTLINETEXTMETRIC'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OUTLINETEXTMETRICW (Unicode) and OUTLINETEXTMETRICA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OUTLINETEXTMETRICA, *POUTLINETEXTMETRICA, *NPOUTLINETEXTMETRICA, *LPOUTLINETEXTMETRICA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OUTLINETEXTMETRICA
 - wingdi/_OUTLINETEXTMETRICA
 - POUTLINETEXTMETRICA
 - wingdi/POUTLINETEXTMETRICA
 - OUTLINETEXTMETRICA
 - wingdi/OUTLINETEXTMETRICA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - OUTLINETEXTMETRIC
 - OUTLINETEXTMETRICA
 - OUTLINETEXTMETRICW
---

# OUTLINETEXTMETRICA structure


## -description

The <b>OUTLINETEXTMETRIC</b> structure contains metrics describing a TrueType font.

## -struct-fields

### -field otmSize

The size, in bytes, of the <b>OUTLINETEXTMETRIC</b> structure.

### -field otmTextMetrics

A <a href="/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a> structure containing further information about the font.

### -field otmFiller

A value that causes the structure to be byte-aligned.

### -field otmPanoseNumber

The PANOSE number for this font.

### -field otmfsSelection

The nature of the font pattern. This member can be a combination of the following bits.

<table>
<tr>
<th>Bit</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Italic</td>
</tr>
<tr>
<td>1</td>
<td>Underscore</td>
</tr>
<tr>
<td>2</td>
<td>Negative</td>
</tr>
<tr>
<td>3</td>
<td>Outline</td>
</tr>
<tr>
<td>4</td>
<td>Strikeout</td>
</tr>
<tr>
<td>5</td>
<td>Bold</td>
</tr>
</table>

### -field otmfsType

Indicates whether the font is licensed. Licensed fonts must not be modified or exchanged. If bit 1 is set, the font may not be embedded in a document. If bit 1 is clear, the font can be embedded. If bit 2 is set, the embedding is read-only.

### -field otmsCharSlopeRise

The slope of the cursor. This value is 1 if the slope is vertical. Applications can use this value and the value of the <b>otmsCharSlopeRun</b> member to create an italic cursor that has the same slope as the main italic angle (specified by the <b>otmItalicAngle</b> member).

### -field otmsCharSlopeRun

The slope of the cursor. This value is zero if the slope is vertical. Applications can use this value and the value of the <b>otmsCharSlopeRise</b> member to create an italic cursor that has the same slope as the main italic angle (specified by the <b>otmItalicAngle</b> member).

### -field otmItalicAngle

The main italic angle of the font, in tenths of a degree counterclockwise from vertical. Regular (roman) fonts have a value of zero. Italic fonts typically have a negative italic angle (that is, they lean to the right).

### -field otmEMSquare

The number of logical units defining the x- or y-dimension of the em square for this font. (The number of units in the x- and y-directions are always the same for an em square.)

### -field otmAscent

The maximum distance characters in this font extend above the base line. This is the typographic ascent for the font.

### -field otmDescent

The maximum distance characters in this font extend below the base line. This is the typographic descent for the font.

### -field otmLineGap

The typographic line spacing.

### -field otmsCapEmHeight

Not supported.

### -field otmsXHeight

Not supported.

### -field otmrcFontBox

The bounding box for the font.

### -field otmMacAscent

The maximum distance characters in this font extend above the base line for the Macintosh computer.

### -field otmMacDescent

The maximum distance characters in this font extend below the base line for the Macintosh computer.

### -field otmMacLineGap

The line-spacing information for the Macintosh computer.

### -field otmusMinimumPPEM

The smallest recommended size for this font, in pixels per em-square.

### -field otmptSubscriptSize

The recommended horizontal and vertical size for subscripts in this font.

### -field otmptSubscriptOffset

The recommended horizontal and vertical offset for subscripts in this font. The subscript offset is measured from the character origin to the origin of the subscript character.

### -field otmptSuperscriptSize

The recommended horizontal and vertical size for superscripts in this font.

### -field otmptSuperscriptOffset

The recommended horizontal and vertical offset for superscripts in this font. The superscript offset is measured from the character base line to the base line of the superscript character.

### -field otmsStrikeoutSize

The width of the strikeout stroke for this font. Typically, this is the width of the em dash for the font.

### -field otmsStrikeoutPosition

The position of the strikeout stroke relative to the base line for this font. Positive values are above the base line and negative values are below.

### -field otmsUnderscoreSize

The thickness of the underscore character for this font.

### -field otmsUnderscorePosition

The position of the underscore character for this font.

### -field otmpFamilyName

The offset from the beginning of the structure to a string specifying the family name for the font.

### -field otmpFaceName

The offset from the beginning of the structure to a string specifying the typeface name for the font. (This typeface name corresponds to the name specified in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.)

### -field otmpStyleName

The offset from the beginning of the structure to a string specifying the style name for the font.

### -field otmpFullName

The offset from the beginning of the structure to a string specifying the full name for the font. This name is unique for the font and often contains a version number or other identifying information.

## -remarks

The sizes returned in <b>OUTLINETEXTMETRIC</b> are specified in logical units; that is, they depend on the current mapping mode of the specified display context.

Note, <b>OUTLINETEXTMETRIC</b> is defined using the current pack setting. To avoid problems, make sure that the application is built using the platform default packing. For example, 32-bit Windows uses a default of 8-byte packing. For more information, see [C-Compiler Packing Issues](/windows/win32/midl/c-compiler-packing-issues).

> [!NOTE]
> The wingdi.h header defines OUTLINETEXTMETRIC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a>
