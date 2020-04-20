---
UID: NS:wingdi.tagLOGPALETTE
title: LOGPALETTE (wingdi.h)
description: The LOGPALETTE structure defines a logical palette.helpviewer_keywords: ["*LPLOGPALETTE","*NPLOGPALETTE","*PLOGPALETTE","LOGPALETTE","LOGPALETTE structure [Windows GDI]","_win32_LOGPALETTE_str","gdi.logpalette","tagLOGPALETTE","wingdi/LOGPALETTE"]
old-location: gdi\logpalette.htm
tech.root: gdi
ms.assetid: 99d70a0e-ac61-4a88-a500-66443e7882ad
ms.date: 12/05/2018
ms.keywords: '*LPLOGPALETTE, *NPLOGPALETTE, *PLOGPALETTE, LOGPALETTE, LOGPALETTE structure [Windows GDI], _win32_LOGPALETTE_str, gdi.logpalette, tagLOGPALETTE, wingdi/LOGPALETTE'
f1_keywords:
- wingdi/LOGPALETTE
dev_langs:
- c++
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
- LOGPALETTE
targetos: Windows
req.typenames: LOGPALETTE, *PLOGPALETTE, *NPLOGPALETTE, *LPLOGPALETTE
req.redist: 
ms.custom: 19H1
---

# LOGPALETTE structure


## -description



The <b>LOGPALETTE</b> structure defines a logical palette.




## -struct-fields




### -field palVersion

The version number of the system.


### -field palNumEntries

The number of entries in the logical palette.


### -field palPalEntry

Specifies an array of <a href="https://docs.microsoft.com/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures that define the color and usage of each entry in the logical palette.


## -remarks



The colors in the palette-entry table should appear in order of importance because entries earlier in the logical palette are most likely to be placed in the system palette.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/color-structures">Color Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colors">Colors Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="https://docs.microsoft.com/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>
 

 

