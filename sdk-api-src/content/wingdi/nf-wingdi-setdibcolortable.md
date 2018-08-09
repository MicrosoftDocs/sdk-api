---
UID: NF:wingdi.SetDIBColorTable
title: SetDIBColorTable function
author: windows-sdk-content
description: The SetDIBColorTable function sets RGB (red, green, blue) color values in a range of entries in the color table of the DIB that is currently selected into a specified device context.
old-location: gdi\setdibcolortable.htm
old-project: gdi
ms.assetid: f301c34d-6e8e-4dc8-b3f3-0fdc658d09e3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetDIBColorTable, SetDIBColorTable function [Windows GDI], _win32_SetDIBColorTable, gdi.setdibcolortable, wingdi/SetDIBColorTable
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
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

A pointer to an array of <a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a> structures containing new color information for the DIB's color table.


## -returns



If the function succeeds, the return value is the number of color table entries that the function sets.

If the function fails, the return value is zero.




## -remarks



This function should be called to set the color table for DIBs that use 1, 4, or 8 bpp. The <b>BitCount</b> member of a bitmap's associated bitmap information header structure.


<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER
        </a> structure specifies the number of bits-per-pixel. Device-independent bitmaps with a <b>biBitCount</b> value greater than 8 do not have a color table.

The <b>bV5BitCount</b> member of a bitmap's associated <a href="https://msdn.microsoft.com/ec5db6f9-93fa-4dbe-afdb-c039292b26e3">BITMAPV5HEADER</a> structure specifies the number of bits-per-pixel. Device-independent bitmaps with a <b>bV5BitCount</b> value greater than 8 do not have a color table.

<b>ICM:</b> No color management is performed.




## -see-also




<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER
      </a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection
      </a>



<a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION
      </a>



<a href="https://msdn.microsoft.com/3e3319be-8a3d-4ac2-ba36-9dbf18243472">GetDIBColorTable
      </a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject
      </a>



<a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD
      </a>
 

 

