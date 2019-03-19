---
UID: NF:wingdi.GetEnhMetaFilePaletteEntries
title: GetEnhMetaFilePaletteEntries function (wingdi.h)
author: windows-sdk-content
description: The GetEnhMetaFilePaletteEntries function retrieves optional palette entries from the specified enhanced metafile.
old-location: gdi\getenhmetafilepaletteentries.htm
tech.root: gdi
ms.assetid: 2d61fd6a-cebd-457e-ad00-d3e8bd15584a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnhMetaFilePaletteEntries, GetEnhMetaFilePaletteEntries function [Windows GDI], _win32_GetEnhMetaFilePaletteEntries, gdi.getenhmetafilepaletteentries, wingdi/GetEnhMetaFilePaletteEntries
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
 - Ext-MS-Win-GDI-Metafile-L1-1-2.dll
 - GDI32Full.dll
api_name:
 - GetEnhMetaFilePaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetEnhMetaFilePaletteEntries function


## -description


The <b>GetEnhMetaFilePaletteEntries</b> function retrieves optional palette entries from the specified enhanced metafile.


## -parameters




### -param hemf [in]

A handle to the enhanced metafile.


### -param nNumEntries [in]

The number of entries to be retrieved from the optional palette.


### -param lpPaletteEntries [out]

A pointer to an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures that receives the palette colors. The array must contain at least as many structures as there are entries specified by the <i>cEntries</i> parameter.


## -returns



If the array pointer is <b>NULL</b> and the enhanced metafile contains an optional palette, the return value is the number of entries in the enhanced metafile's palette; if the array pointer is a valid pointer and the enhanced metafile contains an optional palette, the return value is the number of entries copied; if the metafile does not contain an optional palette, the return value is zero. Otherwise, the return value is GDI_ERROR.




## -remarks



An application can store an optional palette in an enhanced metafile by calling the <a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a> and <a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a> functions before creating the picture and storing it in the metafile. By doing this, the application can achieve consistent colors when the picture is displayed on a variety of devices.

An application that displays a picture stored in an enhanced metafile can call the <b>GetEnhMetaFilePaletteEntries</b> function to determine whether the optional palette exists. If it does, the application can call the <b>GetEnhMetaFilePaletteEntries</b> function a second time to retrieve the palette entries and then create a logical palette (by using the <a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a> function), select it into its device context (by using the <a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a> function), and then realize it (by using the <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function). After the logical palette has been realized, calling the <a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a> function displays the picture using its original colors.




## -see-also




<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>
 

 

