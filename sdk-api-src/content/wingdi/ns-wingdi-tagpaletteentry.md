---
UID: NS:wingdi.tagPALETTEENTRY
title: tagPALETTEENTRY
author: windows-sdk-content
description: The PALETTEENTRY structure specifies the color and usage of an entry in a logical palette. A logical palette is defined by a LOGPALETTE structure.
old-location: gdi\paletteentry.htm
tech.root: gdi
ms.assetid: 6430e7cf-c9f2-4376-8b17-28c10d9d0f00
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPPALETTEENTRY, *PPALETTEENTRY, PALETTEENTRY, PALETTEENTRY structure [Windows GDI], PC_EXPLICIT, PC_NOCOLLAPSE, PC_RESERVED, _win32_PALETTEENTRY_str, gdi.paletteentry, tagPALETTEENTRY, wingdi/PALETTEENTRY"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - PALETTEENTRY
product: Windows
targetos: Windows
req.typenames: PALETTEENTRY, *PPALETTEENTRY, *LPPALETTEENTRY
req.redist: 
---

# tagPALETTEENTRY structure


## -description



The <b>PALETTEENTRY</b> structure specifies the color and usage of an entry in a logical palette. A logical palette is defined by a <a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a> structure.




## -struct-fields




### -field peRed

The red intensity value for the palette entry.


### -field peGreen

The green intensity value for the palette entry.


### -field peBlue

The blue intensity value for the palette entry.


### -field peFlags

Indicates how the palette entry is to be used. This member may be set to 0 or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PC_EXPLICIT"></a><a id="pc_explicit"></a><dl>
<dt><b>PC_EXPLICIT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the low-order word of the logical palette entry designates a hardware palette index. This flag allows the application to show the contents of the display device palette.

</td>
</tr>
<tr>
<td width="40%"><a id="PC_NOCOLLAPSE"></a><a id="pc_nocollapse"></a><dl>
<dt><b>PC_NOCOLLAPSE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the color be placed in an unused entry in the system palette instead of being matched to an existing color in the system palette. If there are no unused entries in the system palette, the color is matched normally. Once this color is in the system palette, colors in other logical palettes can be matched to this color.

</td>
</tr>
<tr>
<td width="40%"><a id="PC_RESERVED"></a><a id="pc_reserved"></a><dl>
<dt><b>PC_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the logical palette entry be used for palette animation. This flag prevents other windows from matching colors to the palette entry since the color frequently changes. If an unused system-palette entry is available, the color is placed in that entry. Otherwise, the color is not available for animation.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/342ba106-e87a-43ae-88f9-bb42bb34006a">Color Structures</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a>
 

 

