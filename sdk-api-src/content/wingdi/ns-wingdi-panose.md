---
UID: NS:wingdi.tagPANOSE
title: PANOSE (wingdi.h)
description: The PANOSE structure describes the PANOSE font-classification values for a TrueType font. These characteristics are then used to associate the font with other fonts of similar appearance but different names.
helpviewer_keywords: ["*LPPANOSE","LPPANOSE","LPPANOSE structure pointer [Windows GDI]","PANOSE","PANOSE structure [Windows GDI]","_win32_PANOSE_str","gdi.panose","wingdi/LPPANOSE","wingdi/PANOSE"]
old-location: gdi\panose.htm
tech.root: gdi
ms.assetid: 18aa4a36-8e47-4e35-973f-376d412ed923
ms.date: 12/05/2018
ms.keywords: '*LPPANOSE, LPPANOSE, LPPANOSE structure pointer [Windows GDI], PANOSE, PANOSE structure [Windows GDI], _win32_PANOSE_str, gdi.panose, wingdi/LPPANOSE, wingdi/PANOSE'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PANOSE, *LPPANOSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPANOSE
 - wingdi/tagPANOSE
 - LPPANOSE
 - wingdi/LPPANOSE
 - PANOSE
 - wingdi/PANOSE
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
 - PANOSE
---

# PANOSE structure


## -description

The <b>PANOSE</b> structure describes the PANOSE font-classification values for a TrueType font. These characteristics are then used to associate the font with other fonts of similar appearance but different names.

## -struct-fields

### -field bFamilyType

For Latin fonts, one of one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_FAMILY_TEXT_DISPLAY</td>
<td>Text and display</td>
</tr>
<tr>
<td>PAN_FAMILY_SCRIPT</td>
<td>Script</td>
</tr>
<tr>
<td>PAN_FAMILY_DECORATIVE</td>
<td>Decorative</td>
</tr>
<tr>
<td>PAN_FAMILY_PICTORIAL</td>
<td>Pictorial</td>
</tr>
</table>

### -field bSerifStyle

The serif style. For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_SERIF_COVE</td>
<td>Cove</td>
</tr>
<tr>
<td>PAN_SERIF_OBTUSE_COVE</td>
<td>Obtuse cove</td>
</tr>
<tr>
<td>PAN_SERIF_SQUARE_COVE</td>
<td>Square cove</td>
</tr>
<tr>
<td>PAN_SERIF_OBTUSE_SQUARE_COVE</td>
<td>Obtuse square cove</td>
</tr>
<tr>
<td>PAN_SERIF_SQUARE</td>
<td>Square</td>
</tr>
<tr>
<td>PAN_SERIF_THIN</td>
<td>Thin</td>
</tr>
<tr>
<td>PAN_SERIF_BONE</td>
<td>Bone</td>
</tr>
<tr>
<td>PAN_SERIF_EXAGGERATED</td>
<td>Exaggerated</td>
</tr>
<tr>
<td>PAN_SERIF_TRIANGLE</td>
<td>Triangle</td>
</tr>
<tr>
<td>PAN_SERIF_NORMAL_SANS</td>
<td>Normal sans serif</td>
</tr>
<tr>
<td>PAN_SERIF_OBTUSE_SANS</td>
<td>Obtuse sans serif</td>
</tr>
<tr>
<td>PAN_SERIF_PERP_SANS</td>
<td>Perp sans serif</td>
</tr>
<tr>
<td>PAN_SERIF_FLARED</td>
<td>Flared</td>
</tr>
<tr>
<td>PAN_SERIF_ROUNDED</td>
<td>Rounded</td>
</tr>
</table>

### -field bWeight

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_WEIGHT_VERY_LIGHT</td>
<td>Very light</td>
</tr>
<tr>
<td>PAN_WEIGHT_LIGHT</td>
<td>Light</td>
</tr>
<tr>
<td>PAN_WEIGHT_THIN</td>
<td>Thin</td>
</tr>
<tr>
<td>PAN_WEIGHT_BOOK</td>
<td>Book</td>
</tr>
<tr>
<td>PAN_WEIGHT_MEDIUM</td>
<td>Medium</td>
</tr>
<tr>
<td>PAN_WEIGHT_DEMI</td>
<td>Demibold</td>
</tr>
<tr>
<td>PAN_WEIGHT_BOLD</td>
<td>Bold</td>
</tr>
<tr>
<td>PAN_WEIGHT_HEAVY</td>
<td>Heavy</td>
</tr>
<tr>
<td>PAN_WEIGHT_BLACK</td>
<td>Black</td>
</tr>
<tr>
<td>PAN_WEIGHT_NORD</td>
<td>Nord</td>
</tr>
</table>

### -field bProportion

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_PROP_OLD_STYLE</td>
<td>Old style</td>
</tr>
<tr>
<td>PAN_PROP_MODERN</td>
<td>Modern</td>
</tr>
<tr>
<td>PAN_PROP_EVEN_WIDTH</td>
<td>Even width</td>
</tr>
<tr>
<td>PAN_PROP_EXPANDED</td>
<td>Expanded</td>
</tr>
<tr>
<td>PAN_PROP_CONDENSED</td>
<td>Condensed</td>
</tr>
<tr>
<td>PAN_PROP_VERY_EXPANDED</td>
<td>Very expanded</td>
</tr>
<tr>
<td>PAN_PROP_VERY_CONDENSED</td>
<td>Very condensed</td>
</tr>
<tr>
<td>PAN_PROP_MONOSPACED</td>
<td>Monospaced</td>
</tr>
</table>

### -field bContrast

For Latin fonts,  one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_CONTRAST_NONE</td>
<td>None</td>
</tr>
<tr>
<td>PAN_CONTRAST_VERY_LOW</td>
<td>Very low</td>
</tr>
<tr>
<td>PAN_CONTRAST_LOW</td>
<td>Low</td>
</tr>
<tr>
<td>PAN_CONTRAST_MEDIUM_LOW</td>
<td>Medium low</td>
</tr>
<tr>
<td>PAN_CONTRAST_MEDIUM</td>
<td>Medium</td>
</tr>
<tr>
<td>PAN_CONTRAST_MEDIUM_HIGH</td>
<td>Medium high</td>
</tr>
<tr>
<td>PAN_CONTRAST_HIGH</td>
<td>High</td>
</tr>
<tr>
<td>PAN_CONTRAST_VERY_HIGH</td>
<td>Very high</td>
</tr>
</table>

### -field bStrokeVariation

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_STROKE_GRADUAL_DIAG</td>
<td>Gradual/diagonal</td>
</tr>
<tr>
<td>PAN_STROKE_GRADUAL_TRAN</td>
<td>Gradual/transitional</td>
</tr>
<tr>
<td>PAN_STROKE_GRADUAL_VERT</td>
<td>Gradual/vertical</td>
</tr>
<tr>
<td>PAN_STROKE_GRADUAL_HORZ</td>
<td>Gradual/horizontal</td>
</tr>
<tr>
<td>PAN_STROKE_RAPID_VERT</td>
<td>Rapid/vertical</td>
</tr>
<tr>
<td>PAN_STROKE_RAPID_HORZ</td>
<td>Rapid/horizontal</td>
</tr>
<tr>
<td>PAN_STROKE_INSTANT_VERT</td>
<td>Instant/vertical</td>
</tr>
</table>

### -field bArmStyle

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_STRAIGHT_ARMS_HORZ</td>
<td>Straight arms/horizontal</td>
</tr>
<tr>
<td>PAN_STRAIGHT_ARMS_WEDGE</td>
<td>Straight arms/wedge</td>
</tr>
<tr>
<td>PAN_STRAIGHT_ARMS_VERT</td>
<td>Straight arms/vertical</td>
</tr>
<tr>
<td>PAN_STRAIGHT_ARMS_SINGLE_SERIF</td>
<td>Straight arms/single-serif</td>
</tr>
<tr>
<td>PAN_STRAIGHT_ARMS_DOUBLE_SERIF</td>
<td>Straight arms/double-serif</td>
</tr>
<tr>
<td>PAN_BENT_ARMS_HORZ</td>
<td>Nonstraight arms/horizontal</td>
</tr>
<tr>
<td>PAN_BENT_ARMS_WEDGE</td>
<td>Nonstraight arms/wedge</td>
</tr>
<tr>
<td>PAN_BENT_ARMS_VERT</td>
<td>Nonstraight arms/vertical</td>
</tr>
<tr>
<td>PAN_BENT_ARMS_SINGLE_SERIF</td>
<td>Nonstraight arms/single-serif</td>
</tr>
<tr>
<td>PAN_BENT_ARMS_DOUBLE_SERIF</td>
<td>Nonstraight arms/double-serif</td>
</tr>
</table>

### -field bLetterform

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_CONTACT</td>
<td>Normal/contact</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_WEIGHTED</td>
<td>Normal/weighted</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_BOXED</td>
<td>Normal/boxed</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_FLATTENED</td>
<td>Normal/flattened</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_ROUNDED</td>
<td>Normal/rounded</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_OFF_CENTER</td>
<td>Normal/off center</td>
</tr>
<tr>
<td>PAN_LETT_NORMAL_SQUARE</td>
<td>Normal/square</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_CONTACT</td>
<td>Oblique/contact</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_WEIGHTED</td>
<td>Oblique/weighted</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_BOXED</td>
<td>Oblique/boxed</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_FLATTENED</td>
<td>Oblique/flattened</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_ROUNDED</td>
<td>Oblique/rounded</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_OFF_CENTER</td>
<td>Oblique/off center</td>
</tr>
<tr>
<td>PAN_LETT_OBLIQUE_SQUARE</td>
<td>Oblique/square</td>
</tr>
</table>

### -field bMidline

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_MIDLINE_STANDARD_TRIMMED</td>
<td>Standard/trimmed</td>
</tr>
<tr>
<td>PAN_MIDLINE_STANDARD_POINTED</td>
<td>Standard/pointed</td>
</tr>
<tr>
<td>PAN_MIDLINE_STANDARD_SERIFED</td>
<td>Standard/serifed</td>
</tr>
<tr>
<td>PAN_MIDLINE_HIGH_TRIMMED</td>
<td>High/trimmed</td>
</tr>
<tr>
<td>PAN_MIDLINE_HIGH_POINTED</td>
<td>High/pointed</td>
</tr>
<tr>
<td>PAN_MIDLINE_HIGH_SERIFED</td>
<td>High/serifed</td>
</tr>
<tr>
<td>PAN_MIDLINE_CONSTANT_TRIMMED</td>
<td>Constant/trimmed</td>
</tr>
<tr>
<td>PAN_MIDLINE_CONSTANT_POINTED</td>
<td>Constant/pointed</td>
</tr>
<tr>
<td>PAN_MIDLINE_CONSTANT_SERIFED</td>
<td>Constant/serifed</td>
</tr>
<tr>
<td>PAN_MIDLINE_LOW_TRIMMED</td>
<td>Low/trimmed</td>
</tr>
<tr>
<td>PAN_MIDLINE_LOW_POINTED</td>
<td>Low/pointed</td>
</tr>
<tr>
<td>PAN_MIDLINE_LOW_SERIFED</td>
<td>Low/serifed</td>
</tr>
</table>

### -field bXHeight

For Latin fonts, one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PAN_ANY</td>
<td>Any</td>
</tr>
<tr>
<td>PAN_NO_FIT</td>
<td>No fit</td>
</tr>
<tr>
<td>PAN_XHEIGHT_CONSTANT_SMALL</td>
<td>Constant/small</td>
</tr>
<tr>
<td>PAN_XHEIGHT_CONSTANT_STD</td>
<td>Constant/standard</td>
</tr>
<tr>
<td>PAN_XHEIGHT_CONSTANT_LARGE</td>
<td>Constant/large</td>
</tr>
<tr>
<td>PAN_XHEIGHT_DUCKING_SMALL</td>
<td>Ducking/small</td>
</tr>
<tr>
<td>PAN_XHEIGHT_DUCKING_STD</td>
<td>Ducking/standard</td>
</tr>
<tr>
<td>PAN_XHEIGHT_DUCKING_LARGE</td>
<td>Ducking/large</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-extlogfonta">EXTLOGFONT</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a>