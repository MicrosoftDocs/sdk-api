---
UID: NF:wingdi.SetPaletteEntries
title: SetPaletteEntries function
author: windows-sdk-content
description: The SetPaletteEntries function sets RGB (red, green, blue) color values and flags in a range of entries in a logical palette.
old-location: gdi\setpaletteentries.htm
tech.root: gdi
ms.assetid: df38f482-75ba-4800-8b26-92204c63255e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetPaletteEntries, SetPaletteEntries function [Windows GDI], _win32_SetPaletteEntries, gdi.setpaletteentries, wingdi/SetPaletteEntries
ms.topic: function
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetPaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetPaletteEntries function


## -description


The <b>SetPaletteEntries</b> function sets RGB (red, green, blue) color values and flags in a range of entries in a logical palette.


## -parameters




### -param hpal [in]

A handle to the logical palette.


### -param iStart [in]

The first logical-palette entry to be set.


### -param cEntries [in]

The number of logical-palette entries to be set.


### -param pPalEntries [in]

A pointer to the first member of an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures containing the RGB values and flags.


## -returns



If the function succeeds, the return value is the number of entries that were set in the logical palette.

If the function fails, the return value is zero.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

Even if a logical palette has been selected and realized, changes to the palette do not affect the physical palette in the surface. <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> must be called again to set the new logical palette into the surface.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/5e72e881-32e1-458e-a09e-91fa13abe178">GetPaletteEntries</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>
 

 

