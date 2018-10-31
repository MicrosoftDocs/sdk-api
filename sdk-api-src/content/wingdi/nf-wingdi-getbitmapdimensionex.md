---
UID: NF:wingdi.GetBitmapDimensionEx
title: GetBitmapDimensionEx function
author: windows-sdk-content
description: The GetBitmapDimensionEx function retrieves the dimensions of a compatible bitmap. The retrieved dimensions must have been set by the SetBitmapDimensionEx function.
old-location: gdi\getbitmapdimensionex.htm
tech.root: gdi
ms.assetid: 3e4f5afc-26d3-4fb2-8d00-183165fdf471
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetBitmapDimensionEx, GetBitmapDimensionEx function [Windows GDI], _win32_GetBitmapDimensionEx, gdi.getbitmapdimensionex, wingdi/GetBitmapDimensionEx
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetBitmapDimensionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetBitmapDimensionEx function


## -description


The <b>GetBitmapDimensionEx</b> function retrieves the dimensions of a compatible bitmap. The retrieved dimensions must have been set by the <a href="https://msdn.microsoft.com/23960533-de71-4bff-a43f-75e5fe38fbec">SetBitmapDimensionEx</a> function.


## -parameters




### -param hbit [in]

A handle to a compatible bitmap (DDB).


### -param lpsize [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure to receive the bitmap dimensions. For more information, see Remarks.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The function returns a data structure that contains fields for the height and width of the bitmap, in .01-mm units. If those dimensions have not yet been set, the structure that is returned will have zeros in those fields.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/23960533-de71-4bff-a43f-75e5fe38fbec">SetBitmapDimensionEx</a>
 

 

