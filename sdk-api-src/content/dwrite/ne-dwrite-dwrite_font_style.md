---
UID: NE:dwrite.DWRITE_FONT_STYLE
title: DWRITE_FONT_STYLE (dwrite.h)
description: Represents the style of a font face as normal, italic, or oblique.
helpviewer_keywords: ["DWRITE_FONT_STYLE","DWRITE_FONT_STYLE enumeration [Direct Write]","DWRITE_FONT_STYLE_ITALIC","DWRITE_FONT_STYLE_NORMAL","DWRITE_FONT_STYLE_OBLIQUE","directwrite.dwrite_font_style","dwrite/DWRITE_FONT_STYLE","dwrite/DWRITE_FONT_STYLE_ITALIC","dwrite/DWRITE_FONT_STYLE_NORMAL","dwrite/DWRITE_FONT_STYLE_OBLIQUE"]
old-location: directwrite\dwrite_font_style.htm
tech.root: DirectWrite
ms.assetid: e48a3b82-4a60-472d-8cb8-a6f63d7eeefc
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_STYLE, DWRITE_FONT_STYLE enumeration [Direct Write], DWRITE_FONT_STYLE_ITALIC, DWRITE_FONT_STYLE_NORMAL, DWRITE_FONT_STYLE_OBLIQUE, directwrite.dwrite_font_style, dwrite/DWRITE_FONT_STYLE, dwrite/DWRITE_FONT_STYLE_ITALIC, dwrite/DWRITE_FONT_STYLE_NORMAL, dwrite/DWRITE_FONT_STYLE_OBLIQUE
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_FONT_STYLE
 - dwrite/DWRITE_FONT_STYLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_FONT_STYLE
---

# DWRITE_FONT_STYLE enumeration


## -description

Represents the style of a font face as normal, italic, or oblique.

## -enum-fields

### -field DWRITE_FONT_STYLE_NORMAL

Font style : Normal.

### -field DWRITE_FONT_STYLE_OBLIQUE

Font style : Oblique.

### -field DWRITE_FONT_STYLE_ITALIC

Font style : Italic.

## -remarks

Three terms categorize the slant of a font: normal, italic, and oblique.
  

<table>
<tr>
<th>Font style</th>
<th>Description</th>
</tr>
<tr>
<td>Normal</td>
<td>The characters in a normal, or roman, font are upright. 
</td>
</tr>
<tr>
<td>Italic 
</td>
<td>The characters in an italic font are truly slanted and appear as they were designed. 
</td>
</tr>
<tr>
<td>Oblique</td>
<td>The characters in an oblique font are artificially slanted.</td>
</tr>
</table>
 

For Oblique, the slant is achieved by performing a shear transformation on the characters from a normal font. When a true italic font is not available on a computer or printer, an oblique style can be generated from the normal font and used to simulate an italic font. 

The following illustration shows the normal, italic, and oblique font styles for the Palatino Linotype font. Notice how the italic font style has a more flowing and visually appealing appearance than the oblique font style, which is simply created by skewing the normal font style version of the text.

<img alt="Illustration of normal, italic, and oblique font styles" src="./images/FontStyle_for_Palatino.png"/>

<div class="alert"><b>Note</b>   Values other than the ones defined in the enumeration are considered to be invalid, and they are rejected by font API functions.</div>
<div> </div>

