---
UID: NS:wingdi.tagLOGPALETTE
title: tagLOGPALETTE
author: windows-sdk-content
description: The LOGPALETTE structure defines a logical palette.
old-location: gdi\logpalette.htm
tech.root: gdi
ms.assetid: 99d70a0e-ac61-4a88-a500-66443e7882ad
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPLOGPALETTE, *NPLOGPALETTE, *PLOGPALETTE, LOGPALETTE, LOGPALETTE structure [Windows GDI], _win32_LOGPALETTE_str, gdi.logpalette, tagLOGPALETTE, wingdi/LOGPALETTE"
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
 - LOGPALETTE
product: Windows
targetos: Windows
req.typenames: LOGPALETTE, *PLOGPALETTE, *NPLOGPALETTE, *LPLOGPALETTE
req.redist: 
---

# tagLOGPALETTE structure


## -description



The <b>LOGPALETTE</b> structure defines a logical palette.




## -struct-fields




### -field palVersion

The version number of the system.


### -field palNumEntries

The number of entries in the logical palette.


### -field palPalEntry

Specifies an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures that define the color and usage of each entry in the logical palette.


## -remarks



The colors in the palette-entry table should appear in order of importance because entries earlier in the logical palette are most likely to be placed in the system palette.




## -see-also




<a href="https://msdn.microsoft.com/342ba106-e87a-43ae-88f9-bb42bb34006a">Color Structures</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>
 

 

