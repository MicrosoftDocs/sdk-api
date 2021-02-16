---
UID: NS:winddi._FONTDIFF
title: FONTDIFF (winddi.h)
description: The FONTDIFF structure describes all of the characteristics that are different between a base font and one of its simulations.
helpviewer_keywords: ["FONTDIFF","FONTDIFF structure [Display Devices]","display.fontdiff","grstrcts_f0aab188-5a92-48b3-be9d-464e22f4b260.xml","winddi/FONTDIFF"]
old-location: display\fontdiff.htm
tech.root: display
ms.assetid: c590359b-4652-4673-9e43-bf76a0a45d58
ms.date: 12/05/2018
ms.keywords: FONTDIFF, FONTDIFF structure [Display Devices], display.fontdiff, grstrcts_f0aab188-5a92-48b3-be9d-464e22f4b260.xml, winddi/FONTDIFF
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FONTDIFF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FONTDIFF
 - winddi/_FONTDIFF
 - FONTDIFF
 - winddi/FONTDIFF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FONTDIFF
---

# FONTDIFF structure


## -description

The FONTDIFF structure describes all of the characteristics that are different between a base font and one of its simulations.

## -struct-fields

### -field jReserved1

### -field jReserved2

### -field jReserved3

Are reserved for system use.

### -field bWeight

Specifies the Panose weight.

### -field usWinWeight

Specifies the weight of the font in the range 0 to 1000 (for example, 400 is normal and 700 is bold). This value is provided to the application in the <b>lfWeight</b> member of the Win32 LOGFONT structure.

### -field fsSelection

Specifies a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FM_SEL_BOLD

</td>
<td>
Set if the characters of the font are bold.

</td>
</tr>
<tr>
<td>
FM_SEL_ITALIC

</td>
<td>
Set if the characters of the font are italic.

</td>
</tr>
<tr>
<td>
FM_SEL_NEGATIVE

</td>
<td>
Set if the characters of the font have the foreground and background reversed.

</td>
</tr>
<tr>
<td>
FM_SEL_OUTLINED

</td>
<td>
Set if the characters of the font are hollow.

</td>
</tr>
<tr>
<td>
FM_SEL_REGULAR

</td>
<td>
Set if the characters of the font are normal weight.

</td>
</tr>
<tr>
<td>
FM_SEL_STRIKEOUT

</td>
<td>
Set if the characters of the font are struck out by default; otherwise strikeouts must be simulated.

</td>
</tr>
<tr>
<td>
FM_SEL_UNDERSCORE

</td>
<td>
Set if all the characters of the font are underscored by default; otherwise underscoring must be simulated.

</td>
</tr>
</table>

### -field fwdAveCharWidth

Specifies the arithmetic average of the width of all of the 26 lower case letters 'a' through 'z' of the Latin alphabet and the space character. If any of the 26 lowercase letters are not present, then this member should be set equal to the weighted average of all glyphs in the font.

### -field fwdMaxCharInc

Specifies the maximum character increment of all glyphs in the font.

### -field ptlCaret

Specifies a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that indicates the direction of the ascender direction of the font. For example, the value for a nonitalicized Latin font is (0,1) while an italicized Latin font might specify a value of (2,5).

## -remarks

If a font has already been emboldened, the only possible remaining simulation is italicization, yielding a bold italic simulation. Similarly, an italicized font can only be emboldened, also yielding a bold italic simulation.

For descriptions of the FSHORT and FWORD data types, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontsim">FONTSIM</a>