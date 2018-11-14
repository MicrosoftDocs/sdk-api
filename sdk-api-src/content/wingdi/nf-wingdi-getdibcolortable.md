---
UID: NF:wingdi.GetDIBColorTable
title: GetDIBColorTable function
author: windows-sdk-content
description: The GetDIBColorTable function retrieves RGB (red, green, blue) color values from a range of entries in the color table of the DIB section bitmap that is currently selected into a specified device context.
old-location: gdi\getdibcolortable.htm
tech.root: gdi
ms.assetid: 3e3319be-8a3d-4ac2-ba36-9dbf18243472
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDIBColorTable, GetDIBColorTable function [Windows GDI], _win32_GetDIBColorTable, gdi.getdibcolortable, wingdi/GetDIBColorTable
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-GDI-Draw-L1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetDIBColorTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetDIBColorTable
: 
---

# GetDIBColorTable function


## -description


The <b>GetDIBColorTable</b> function retrieves RGB (red, green, blue) color values from a range of entries in the color table of the DIB section bitmap that is currently selected into a specified device context.


## -parameters




### -param hdc [in]

A handle to a device context. A DIB section bitmap must be selected into this device context.


### -param iStart [in]

A zero-based color table index that specifies the first color table entry to retrieve.


### -param cEntries [in]

The number of color table entries to retrieve.


### -param prgbq [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a> data structures containing color information from the DIB color table. The buffer must be large enough to contain as many <b>RGBQUAD</b> data structures as the value of <i>cEntries</i>.


## -returns



If the function succeeds, the return value is the number of color table entries that the function retrieves.

If the function fails, the return value is zero.




## -remarks



The <b>GetDIBColorTable</b> function should be called to retrieve the color table for DIB section bitmaps that use 1, 4, or 8 bpp. The <b>biBitCount</b> member of a bitmap associated <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure specifies the number of bits-per-pixel. DIB section bitmaps with a <b>biBitCount</b> value greater than eight do not have a color table, but they do have associated color masks. Call the <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> function to retrieve those color masks.




## -see-also




<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a>



<a href="https://msdn.microsoft.com/f301c34d-6e8e-4dc8-b3f3-0fdc658d09e3">SetDIBColorTable</a>
 

 

