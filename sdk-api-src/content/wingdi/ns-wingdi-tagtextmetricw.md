---
UID: NS:wingdi.tagTEXTMETRICW
title: tagTEXTMETRICW
author: windows-sdk-content
description: The TEXTMETRIC structure contains basic information about a physical font. All sizes are specified in logical units; that is, they depend on the current mapping mode of the display context.
old-location: gdi\textmetric.htm
old-project: gdi
ms.assetid: 0a46da58-5d0f-4db4-bba6-9e1b6c1f892c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPTEXTMETRICW, *NPTEXTMETRICW, *PTEXTMETRICW, PTEXTMETRIC, PTEXTMETRIC structure pointer [Windows GDI], TEXTMETRIC, TEXTMETRIC structure [Windows GDI], TEXTMETRICA, TEXTMETRICW, _win32_TEXTMETRIC_str, gdi.textmetric, tagTEXTMETRICW, wingdi/PTEXTMETRIC, wingdi/TEXTMETRIC, wingdi/TEXTMETRICA, wingdi/TEXTMETRICW"
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
req.unicode-ansi: TEXTMETRICW (Unicode) and TEXTMETRICA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TEXTMETRICW, *PTEXTMETRICW, *NPTEXTMETRICW, *LPTEXTMETRICW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagTEXTMETRICW structure


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

The four high-order bits of <b>tmPitchAndFamily</b> designate the font's font family. An application can use the value 0xF0 and the bitwise AND operator to mask out the four low-order bits of <b>tmPitchAndFamily</b>, thus obtaining a value that can be directly compared with font family names to find an identical match. For information about font families, see the description of the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure.


### -field tmCharSet

The character set of the font. The character set can be one of the following values.

<ul>
<li>ANSI_CHARSET</li>
<li>BALTIC_CHARSET</li>
<li>CHINESEBIG5_CHARSET</li>
<li>DEFAULT_CHARSET</li>
<li>EASTEUROPE_CHARSET</li>
<li>GB2312_CHARSET</li>
<li>GREEK_CHARSET</li>
<li>HANGUL_CHARSET</li>
<li>MAC_CHARSET</li>
<li>OEM_CHARSET</li>
<li>RUSSIAN_CHARSET</li>
<li>SHIFTJIS_CHARSET</li>
<li>SYMBOL_CHARSET</li>
<li>TURKISH_CHARSET</li>
<li>VIETNAMESE_CHARSET</li>
</ul>
<b>Korean language edition of Windows:</b>

<ul>
<li>
JOHAB_CHARSET

</li>
</ul>
<b>Middle East language edition of Windows:</b>

<ul>
<li>
ARABIC_CHARSET

</li>
<li>
HEBREW_CHARSET

</li>
</ul>
<b>Thai language edition of Windows:</b>

<ul>
<li>
THAI_CHARSET

</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>
 

 

