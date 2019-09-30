---
UID: NF:wingdi.SetDIBColorTable
title: SetDIBColorTable function (wingdi.h)
author: windows-sdk-content
description: The SetDIBColorTable function sets RGB (red, green, blue) color values in a range of entries in the color table of the DIB that is currently selected into a specified device context.
old-location: gdi\setdibcolortable.htm
tech.root: gdi
ms.assetid: f301c34d-6e8e-4dc8-b3f3-0fdc658d09e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetDIBColorTable, SetDIBColorTable function [Windows GDI], _win32_SetDIBColorTable, gdi.setdibcolortable, wingdi/SetDIBColorTable
ms.topic: function
f1_keywords: 
 - "wingdi/SetDIBColorTable"
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
 - Ext-MS-Win-GDI-Draw-L1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetDIBColorTable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetDIBColorTable function


## -description


The <b>SetDIBColorTable</b> function sets RGB (red, green, blue) color values in a range of entries in the color table of the DIB that is currently selected into a specified device context.


## -parameters




### -param hdc [in]

A device context. A DIB must be selected into this device context.


### -param iStart [in]

A zero-based color table index that specifies the first color table entry to set.


### -param cEntries [in]

The number of color table entries to set.


### -param prgbq [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a> structures containing new color information for the DIB's color table.


## -returns



If the function succeeds, the return value is the number of color table entries that the function sets.

If the function fails, the return value is zero.




## -remarks



This function should be called to set the color table for DIBs that use 1, 4, or 8 bpp. The <b>BitCount</b> member of a bitmap's associated bitmap information header structure.


<a href="https://docs.microsoft.com/previous-versions/dd183376(v=vs.85)">BITMAPINFOHEADER
        </a> structure specifies the number of bits-per-pixel. Device-independent bitmaps with a <b>biBitCount</b> value greater than 8 do not have a color table.

The <b>bV5BitCount</b> member of a bitmap's associated <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header">BITMAPV5HEADER</a> structure specifies the number of bits-per-pixel. Device-independent bitmaps with a <b>bV5BitCount</b> value greater than 8 do not have a color table.

<b>ICM:</b> No color management is performed.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/dd183376(v=vs.85)">BITMAPINFOHEADER
      </a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getdibcolortable">GetDIBColorTable
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD
      </a>
 

 

