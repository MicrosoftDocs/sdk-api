---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

<img alt="Illustration of normal, italic, and oblique font styles" src="images/FontStyle_for_Palatino.png"/>

<div class="alert"><b>Note</b>   Values other than the ones defined in the enumeration are considered to be invalid, and they are rejected by font API functions.</div>
<div> </div>


