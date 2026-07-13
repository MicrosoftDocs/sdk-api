---
UID: NS:wingdi.tagTEXTMETRICW
title: TEXTMETRICW (wingdi.h)
description: The TEXTMETRIC structure contains basic information about a physical font. All sizes are specified in logical units; that is, they depend on the current mapping mode of the display context. (Unicode)
helpviewer_keywords: ["*LPTEXTMETRICW","*NPTEXTMETRICW","*PTEXTMETRICW","PTEXTMETRIC","PTEXTMETRIC structure pointer [Windows GDI]","TEXTMETRIC","TEXTMETRIC structure [Windows GDI]","TEXTMETRICA","TEXTMETRICW","_win32_TEXTMETRIC_str","gdi.textmetric","wingdi/PTEXTMETRIC","wingdi/TEXTMETRIC","wingdi/TEXTMETRICA","wingdi/TEXTMETRICW"]
old-location: gdi\textmetric.htm
tech.root: gdi
ms.assetid: 0a46da58-5d0f-4db4-bba6-9e1b6c1f892c
ms.date: 12/05/2018
ms.keywords: '*LPTEXTMETRICW, *NPTEXTMETRICW, *PTEXTMETRICW, PTEXTMETRIC, PTEXTMETRIC structure pointer [Windows GDI], TEXTMETRIC, TEXTMETRIC structure [Windows GDI], TEXTMETRICA, TEXTMETRICW, _win32_TEXTMETRIC_str, gdi.textmetric, wingdi/PTEXTMETRIC, wingdi/TEXTMETRIC, wingdi/TEXTMETRICA, wingdi/TEXTMETRICW'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TEXTMETRICW (Unicode) and TEXTMETRICA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TEXTMETRICW, *PTEXTMETRICW, *NPTEXTMETRICW, *LPTEXTMETRICW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTEXTMETRICW
 - wingdi/tagTEXTMETRICW
 - PTEXTMETRICW
 - wingdi/PTEXTMETRICW
 - TEXTMETRICW
 - wingdi/TEXTMETRICW
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
 - TEXTMETRIC
 - TEXTMETRICA
 - TEXTMETRICW
---

# TEXTMETRICW structure


## -description

The <b>TEXTMETRIC</b> structure contains basic information about a physical font. All sizes are specified in logical units; that is, they depend on the current mapping mode of the display context.

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

The average width of characters in the font (generally defined as the width of the letter <i>x</i> ). This value does not include the overhang required for bold or italic characters.

### -field tmMaxCharWidth

The width of the widest character in the font.

### -field tmWeight

The weight of the font.

### -field tmOverhang

The extra width per string that may be added to some synthesized fonts. When synthesizing some attributes, such as bold or italic, graphics device interface (GDI) or a device may have to add width to a string on both a per-character and per-string basis. For example, GDI makes a string bold by expanding the spacing of each character and overstriking by an offset value; it italicizes a font by shearing the string. In either case, there is an overhang past the basic string. For bold strings, the overhang is the distance by which the overstrike is offset. For italic strings, the overhang is the amount the top of the font is sheared past the bottom of the font.

The <b>tmOverhang</b> member enables the application to determine how much of the character width returned by a <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a> function call on a single character is the actual character width and how much is the per-string extra width. The actual width is the extent minus the overhang.

### -field tmDigitizedAspectX

The horizontal aspect of the device for which the font was designed.

### -field tmDigitizedAspectY

The vertical aspect of the device for which the font was designed. The ratio of the <b>tmDigitizedAspectX</b> and <b>tmDigitizedAspectY</b> members is the aspect ratio of the device for which the font was designed.

### -field tmFirstChar

The value of the first character defined in the font.

### -field tmLastChar

The value of the last character defined in the font.

### -field tmDefaultChar

The value of the character to be substituted for characters not in the font.

### -field tmBreakChar

The value of the character that will be used to define word breaks for text justification.

### -field tmItalic

Specifies an italic font if it is nonzero.

### -field tmUnderlined

Specifies an underlined font if it is nonzero.

### -field tmStruckOut

A strikeout font if it is nonzero.

### -field tmPitchAndFamily

Specifies information about the pitch, the technology, and the family of a physical font.

The four low-order bits of this member specify information about the pitch and the technology of the font. A constant is defined for each of the four bits.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>TMPF_FIXED_PITCH</td>
<td>If this bit is set the font is a variable pitch font. If this bit is clear the font is a fixed pitch font. Note very carefully that those meanings are the opposite of what the constant name implies.</td>
</tr>
<tr>
<td>TMPF_VECTOR</td>
<td>If this bit is set the font is a vector font.</td>
</tr>
<tr>
<td>TMPF_TRUETYPE</td>
<td>If this bit is set the font is a TrueType font.</td>
</tr>
<tr>
<td>TMPF_DEVICE</td>
<td>If this bit is set the font is a device font.</td>
</tr>
</table>
 

An application should carefully test for qualities encoded in these low-order bits, making no arbitrary assumptions. For example, besides having their own bits set, TrueType and PostScript fonts set the TMPF_VECTOR bit. A monospace bitmap font has all of these low-order bits clear; a proportional bitmap font sets the TMPF_FIXED_PITCH bit. A Postscript printer device font sets the TMPF_DEVICE, TMPF_VECTOR, and TMPF_FIXED_PITCH bits.

The four high-order bits of <b>tmPitchAndFamily</b> designate the font's font family. An application can use the value 0xF0 and the bitwise AND operator to mask out the four low-order bits of <b>tmPitchAndFamily</b>, thus obtaining a value that can be directly compared with font family names to find an identical match. For information about font families, see the description of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.

### -field tmCharSet

The character set of the font. For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT structure</a>.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines TEXTMETRIC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
